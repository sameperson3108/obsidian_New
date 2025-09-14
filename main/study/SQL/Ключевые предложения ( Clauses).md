Ключевые предложения (Clauses) - 

WHERE - фильтрация строк
SELECT * FROM users WHERE age > 18 AND city = 'Moscow';

ORDER BY - сортировка результатов
SELECT * FROM products ORDER BY price DESC, name ASC;

LIMIT/OFFSET - ограничение количества результатов и пагинация
SELECT * FROM logs ORDER BY created_at DESC LIMIT 10 OFFSET 20;

DISTINCT - выбор уникальных значений
SELECT DISTINCT city FROM users;

GROUP BY - группировка строк для агрегатных функций
SELECT department, COUNT(* ), AVG(salary) FROM eployees GROUP BY department;

HAVING - фильтрация по результатам агрегатных функций (как WHERE, но для GROUP BY)

SELECT department, COUNT(* ) FROM employees GROUP BY department HAVING COUNT (* ) > 5;