# TaskFlow

Веб-приложение для управления личными задачами на Django.

## Возможности
- регистрация и авторизация пользователей;
- создание, редактирование, удаление задач;
- изменение статуса и отметка выполнения;
- поиск, фильтрация и сортировка задач;
- категории задач;
- административная панель.

## Стек
- Django 5
- SQLite
- Bootstrap 5

## Локальный запуск
```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

## Тесты
```bash
python manage.py test
```
