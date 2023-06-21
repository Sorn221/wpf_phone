# wpf_phone
Приложение с использованием технологии wpf и подключенной бд, для магазина по продаже телефонов
# Как сделать так, что бы все заработало? 

1) Создаем базу данных в PgAdmin, называем ее как нибудь, скрипт для создания сущностей:
 ```sql
|   CREATE TABLE "Company"
|(
|   "Id" SERIAL PRIMARY KEY,
|   "Title" character varying(150),
|   "CEO" character varying(150),
|   "Capital" double precision
|);
|CREATE TABLE "Phone"
|(
|   "Id" SERIAL PRIMARY KEY,
|   "Title" character varying(150),
|   "CompanyId" integer,
|   "Price" numeric(15, 2),
|   "Definition" text,
|   "Image" text,
|   FOREIGN KEY ("CompanyId") REFERENCES "Company"("Id")
|);
```
2) Распаковываем архив
3) Открываем папку "wpf_phone"
4) Находим файл "Lr4.sln", запускаем
5) Находим класс "DbAppContext", открываем
6) Ищем 19 строку, Password = "Ваш пароль от PgAdmin", Database = "Ваше название базы"
7) F5, наслаждаемся 
