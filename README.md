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

#### 1. **initial_migration**
Запускается при инициализации.
Создает таблицы в PSQL и MySQL
