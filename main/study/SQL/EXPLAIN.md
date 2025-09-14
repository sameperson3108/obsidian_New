EXPLAIN - показывает план выполнения запроса, помогает найти "узкие места".

EXPLAIN ANALYZE - не только показывает план, но и выполняет запрос, показывая реально время
EXPLAIN ANALYZE SELECT * FROM large_table WHERE category_id = 5;