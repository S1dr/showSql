# showSql
This repository was created on the day of demonstrating basic functions and understanding of the sql language

Sql работа с таблицей.(ВЫБОРКА)

SELECT * FROM employee ORDER BY country_of_birth
(Выборка сотрудников по странам. В алфавитном порядке)

SELECT * FROM employee ORDER BY country_of_birth DESC;
 (Выборка сотруднико в по странам, в обратном алфавитном порядке(функция DESC) 

SELECT country_of_birth FROM employee ORDERED BY country_of_birth; 
(Выборка сотрудников по странам в алфавитном порядке)

SELECT DISTINCT counry_of_birth FROM employee ORDERED BY country_of_birth; 
(Выборка сотрудников в алфавитном порядке, но страны не будут повторяться. К примеру что бы понять сколько всего стран у нас в комманде)

SELECT * FROM employee WHERE gender = 'Female';
(Выборка только девушек, которые работают в нашей компании)

SELECT * FROM employee WHERE gender = 'Female' and country_of_birth = 'Argentina';
(Выборка всех девушек которые работают в компании с родом из Аргентины)

SELECT * FROM employee WHERE gender = 'Femail' AND (country_of_birth = 'Czech Republic' OR country_of_birth = 'Slovakia');
(Выборка всех девушек которые работают в компании из Чехии и Словакии)

SELECT * FROM employee LIMIT 20
(Выборка из первых 20 работников)


SELECT * FROM employee OFFSET 10 LIMIT 5;
Выборка с 11 позиции нацинается. Показывает слудующие 5 позиций


SELECT * FROM employee WHERE country_of_birth IN ('China' , 'Argwntina' , 'Kazakstan');
(Альтернативный способ выборки работников с конкретных стран. Запрос занимает гараздо меньше места.)

SELECT * FROM employee WHERE date_of_birth BETWEEN '2019-01-01' AND '2020-01-01';
(Выборка по датам)

SELECT * FROM employee WHERE email LIKE '%.com';
(Выборка по шаблону . В данном запросе выведуться все почты которые заканчиваются на .com)

SELECT * FROM employee WHERE country_of_birth LIKE 'P%';
(В данном запросе выведуться все страны на "P")


SELECT country_of_birth, COUNT(*) FROM employee GROUP BY country_of_birth;
(Данный запрос посчитает сколько у нас сотрудников с каждой страны.)

SELECT first_name, COUNT(*) FROM employee GROUP BY country_of_birth;
(Запрос позволяющий узнать колличество сотрудниклв с одинаковыми именами )


Агрегаты и Базовая Арифметика 
В таблице можно добавить к примеру зарплату, sql позволяет нам совершить арефметические вычисление. Среднее максимальное минимальное значение. И Т Д Сортировать по нашим предпочтениям.

Так же есть возможность объединения таблиц и дальнейцая их сортировка.



