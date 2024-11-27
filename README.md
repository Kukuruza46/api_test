# API Test Project

Пример работы с FastAPI: от простых хардкод-ответов до интеграции с базой данных.

## Описание

Проект демонстрирует использование **FastAPI** для создания API, а также работу с базой данных через библиотеку SQLAlchemy. 

### Основные файлы:

1. **`main.py`**:
   - Возвращает JSON-ответ `"Hello, World!"` на запрос по маршруту `/`.
   - Пример минимального API с FastAPI.
   - Документация API доступна по адресу: [http://127.0.0.1:8000/docs#/](http://127.0.0.1:8000/docs#/).

2. **`main_1.py`**:
   - Пример API с использованием библиотеки **SQLAlchemy**.
   - Создан класс `Item`, представляющий таблицу `items` с полями `id` и `name`.
   - Реализован маршрут `/items/{item_id}`:
     - Выполняет запрос к базе данных.
     - Возвращает данные о записи с указанным `item_id` в формате JSON.
     - Если запись не найдена, возвращает сообщение об ошибке.
   - Включает автоматическое создание таблицы базы данных на основе модели `Item`.

### Сравнение примеров

- **`main.py`**: демонстрирует статичный JSON-ответ.
- **`main_1.py`**: включает взаимодействие с базой данных для получения динамических данных.

## Установка и запуск

### 1. Клонирование репозитория

```bash
git clone https://github.com/Kukuruza46/api_test.git
cd api_test
