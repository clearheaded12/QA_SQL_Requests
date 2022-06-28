# Запросы к таблицам через СУБД PostgreSQL
Здесь находятся мои запросы к БД. В этом документе примеры запросов к таблицам, которые схожи в компании SkyEng, где я активно обучался и практиковался. Перечислю все таблицы:**group_student, student, subject, teacher, users**.
Чтобы удостовериться в правильности моих запросов вы можете скопировать команду для создание таблиц. Файл для этого выложен в открытом доступе на  [Google Drive](https://drive.google.com/file/d/12pfLbAtuL6X0inZYOK3OHtG1Z0k7YE1U/view?usp=sharing)
## SELECT-запросы: выбор колонок
```sql
SELECT user_id, subject_id FROM users;
```
## SELECT-запросы: выбор строк
```sql
SELECT user_id, subject_id FROM users WHERE user_email=‘igorpetrov@mail.ru’;
```
## SELECT-запросы: несколько условий с логическим опретором AND;
```SQL
SELECT * FROM student WHERE level='Elementary' AND education_form='personal' AND subject_id=1;
```
## Совместное использование OR и AND
```SQL
SELECT * FROM student WHERE (level='Elementary' AND education_form='personal') OR (level='Intermediate' AND education_form='personal');
```
## Запрос с использованием логических операторов NOT и IN;
```sql
SELECT * FROM users WHERE subject_id NOT IN(1,3,5);
```
## Запрос с использованием оператора BETWEEN
```SQL
SELECT * FROM users WHERE subject_id BETWEEN 1 AND 3;
```
## Вставка новых данных через команду INSERT;
```SQL
INSERT INTO subject(subject_id, subject_title) VALUES (4, 'Chemistry');
```
## Обновление данных через команду UPDATE;
```SQL
UPDATE subject SET subject_title='Biology' WHERE subject_id=4;
```
## Удаление данных через команду DELETE;
```SQL
DELETE FROM subject WHERE subject_id=4;
```
