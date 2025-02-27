# Домашнее задание к занятию "`Работа с данными (DDL/DML)`" - `Бакулев Евгений`

### Задание 1
### Что нужно сделать:

1. Поднимите чистый инстанс MySQL версии 8.0+. Можно использовать локальный сервер или контейнер Docker.
2. Создайте учётную запись sys_temp.
3. Выполните запрос на получение списка пользователей в базе данных. (скриншот)
4. Дайте все права для пользователя sys_temp.
5. Выполните запрос на получение списка прав для пользователя sys_temp. (скриншот)
6. Переподключитесь к базе данных от имени sys_temp.
Для смены типа аутентификации с sha2 используйте запрос:
ALTER USER 'sys_test'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
7. По ссылке https://downloads.mysql.com/docs/sakila-db.zip скачайте дамп базы данных.
8. Восстановите дамп в базу данных.
9. При работе в IDE сформируйте ER-диаграмму получившейся базы данных. При работе в командной строке используйте команду для получения всех таблиц базы данных. (скриншот)
Результатом работы должны быть скриншоты обозначенных заданий, а также простыня со всеми запросами.

### Решение 1

```
CREATE USER sys_temp IDENTIFIED BY '571802gg';
GRANT ALL PRIVILEGES ON  * . *  TO sys_temp;
```

![Скрин](https://github.com/garrkiss/ddl_mdl/blob/main/img/%D0%B7%D0%B0%D0%BF%D1%80%D0%BE%D1%81%20%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D0%BE%D0%B2%D0%B0%D1%82%D0%B5%D0%BB%D1%8F.png)
![Скрин](https://github.com/garrkiss/ddl_mdl/blob/main/img/%D0%BF%D1%80%D0%B8%D0%B2%D0%B8%D0%BB%D0%B5%D0%B3%D0%B8%D0%B8.png)
![Скрин](https://github.com/garrkiss/ddl_mdl/blob/main/img/%D1%81%D1%85%D0%B5%D0%BC%D0%B0.png)

### Задание 2
### Что нужно сделать:

Составьте таблицу, используя любой текстовый редактор или Excel, в которой должно быть два столбца: в первом должны быть названия таблиц восстановленной базы, во втором названия первичных ключей этих таблиц. Пример: (скриншот/текст)

```
Название таблицы | Название первичного ключа
customer         | customer_id
```

### Решение 2

```
Название таблицы | Название первичного ключа
actor	         | actor_id   
address	         | address_id
category	 | category_id
city	         | city_id
country	         | country_id
customer         | customer_id
film	         | film_id
film_actor	 | actor_id film_id
film_category	 | film_id category_id
film_text	 | film_id
inventory   	 | inventory_id
language	 | language_id
payment	         | payment_id
rental	         | rental_id
staff	         | staff_id
store	         | store_id
```