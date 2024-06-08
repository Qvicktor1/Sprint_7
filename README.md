﻿## Финальный проект 7 спринта

В этом проекте тестируем некоторые ручки API сервиса [ЯндексСамокат](https://qa-scooter.praktikum-services.ru/)

### Список файлов и описание проверок:

#### 1. test_courier_creation.py 
Проверяет ручку  POST /api/v1/courier

Cодержит тесты:
- test_successful_courier_creation

   Проверяет, что курьера можно создать

- test_creation_repeating_courier_failed

   Проверяет, что нельзя создать двух одинаковых курьеров
   
- test_creation_with_any_missing_field_failed

   Проверяет, что если одного из полей нет, запрос возвращает ошибку и курьера нельзя создать

- test_creation_courier_with_repeating_login_failed

   Проверяет, что если создать пользователя с логином, который уже есть, возвращается ошибка


#### 2. test_courier_login.py
Проверяет ручку  POST /api/v1/courier/login

Cодержит тесты:
- test_successful_courier_login

   Проверяет, что курьер может авторизоваться и что успешный запрос возвращает id (так как id находится в теле ответа).

- test_login_with_any_missing_field_failed

   Проверяет, что если какого-то поля нет, запрос возвращает ошибку.

- test_login_with_any_wrong_field_failed

   Проверяет, что система вернёт ошибку, если неправильно указать логин или пароль и что если авторизоваться под несуществующим пользователем, запрос возвращает ошибку
  


#### 3. test_get_orders_list.py
Проверяет ручку  GET /api/v1/orders

Cодержит тест:
- test_get_orders_list

   Проверяет, что в тело ответа возвращается список заказов

#### 4. test_order_creation.py
Проверяет ручку POST /api/v1/orders

Cодержит тесты:
- test_order_creation_variate_colors
  
   
   Проверяет, что при создании заказа 
   можно указать один из цветов — BLACK или GREY;
   можно указать оба цвета;
   можно совсем не указывать цвет;
   и что тело ответа содержит track.


