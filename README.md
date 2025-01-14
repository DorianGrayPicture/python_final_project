# Итоговый проект по Python для инженерии данных

## Запуск проекта (для UNIX-like систем)

1. Склонировать проект:
```bash
git clone git@github.com:DorianGrayPicture/python_final_project.git
```

2. Внутри корневой директории запустить проект:
```bash
docker-compose up -d
```

3. После сборки проекта (может занять около минуты!) перейти по ссылке:
```URL
http://localhost:8080
```

4. Ввести данные для входа:
- **login:** `admin`
- **password** `admin`

## Airflow DAGs

### 1. **initial_migration**
- Запускается при инициализации
- Создает таблицы в PostgreSQL и MySQL

### 2. **transfer_postgres_mysql**
- Репликация данных из PostgreSQL в MySQL

### 3. **data_marts**
- Построение аналитических витрин


## Аналитическая витрина `sales_analysis`

### Описание
Витрина с данными о пользователях, заказах, продуктах и категориях, собранных в единую таблицу.

## Структура витрины

| Поле                   | Описание                                                   |
|-------------------------|-----------------------------------------------------------|
| `user_id`              | Уникальный идентификатор пользователя.                     |
| `full_name`            | Полное имя клиента.                                        |
| `email`                | Email клиента.                                             |
| `phone`                | Телефон клиента.                                           |
| `loyalty_status`       | Статус лояльности клиента (`Gold`, `Silver`, `Bronze`).     |
| `order_id`             | Уникальный идентификатор заказа.                           |
| `order_date`           | Дата размещения заказа.                                    |
| `order_total`          | Общая сумма заказа.                                        |
| `product_id`           | Уникальный идентификатор продукта.                         |
| `product_name`         | Название продукта.                                         |
| `category_name`        | Название категории продукта.                               |
| `quantity`             | Количество купленного продукта.                           |
| `price_per_unit`       | Цена за единицу продукта.                                  |
| `total_price_per_product` | Общая стоимость продукта в рамках одного заказа.         |
| `order_status`         | Статус заказа (`Pending`, `Completed`, `Canceled`).        |
