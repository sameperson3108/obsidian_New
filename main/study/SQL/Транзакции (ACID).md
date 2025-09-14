Набор операций, которые либо выполняются все, либо не выполняется ни одна. Ключевые команды: BEGIN, COMMIT, ROLLBACK

BEGIN;
UPDATE accounts SET balance = balance - 100 WHERE user_id = 1;
UPDATE accounts SET balance = balance +100 WHERE user_id = 2;
// Если здесь ошибка, делаем ROLLBACK
COMMIT; //Если всё успешно, подтверждаем