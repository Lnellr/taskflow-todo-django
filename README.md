TaskFlow — веб-приложение для управления личными задачами, разработанное на Django.

Проект создан в рамках производственной практики на базе open-source проекта  
**Build a Todo List with Django and Test-Driven Development** из каталога:

https://github.com/practical-tutorials/project-based-learning

---

## Возможности

- регистрация и авторизация пользователей
- создание задач
- редактирование задач
- удаление задач
- изменение статуса задачи
- установка срока выполнения (deadline)
- поиск задач
- фильтрация по статусу, приоритету и категории
- сортировка задач
- управление категориями
- административная панель

---

## Технологии

- Python
- Django
- SQLite
- Bootstrap 5
- HTML / CSS

---

## Архитектура

Приложение построено по архитектуре Django (MVT):
Browser (Client)
        │
        ▼
Django Templates (View)
        │
        ▼
Django Views (Controller logic)
        │
        ▼
Django Models (ORM)
        │
        ▼
SQLite Database

MVT (Model-View-Template) — архитектурный шаблон Django.

Model — описание структуры данных и бизнес-логики приложения.  
View — обработка HTTP-запросов и взаимодействие с моделями.  
Template — отображение пользовательского интерфейса.

---

## ERD (Модель базы данных)

В приложении используются следующие основные сущности:

User
- id
- username
- password
- email
- role

Role
- id
- name

Task
- id
- title
- description
- status
- priority
- due_date
- created_at
- updated_at
- user_id
- category_id

TaskCategory
- id
- name
- description

Связи между сущностями:

Role 1 ─── N User  
User 1 ─── N Task  
TaskCategory 1 ─── N Task

---

## Основные сценарии использования (Use Case)

1. Пользователь регистрируется в системе.
2. Пользователь выполняет вход в систему.
3. Пользователь создаёт новую задачу.
4. Пользователь редактирует задачу.
5. Пользователь изменяет статус задачи.
6. Пользователь ищет и фильтрует задачи.
7. Администратор управляет категориями задач.