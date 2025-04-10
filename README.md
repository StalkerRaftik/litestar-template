# Litestar Demo Project

Это демонстрационный проект, созданный с использованием фреймворка Litestar. Проект представляет собой современное веб-приложение, построенное с учетом лучших практик разработки.

## Особенности проекта

- 🚀 **Полная типизация** - проект полностью типизирован с использованием Python type hints
- 🔄 **Асинхронная архитектура** - построен на асинхронном подходе для максимальной производительности
- 🧅 **Луковая архитектура** - структура проекта следует принципам чистой архитектуры
- 🛠 **Инструменты разработки**:
  - Ruff для линтинга и форматирования кода
  - mypy для статической типизации
  - pytest для тестирования
  - pre-commit для автоматизации проверок
- 🐳 **Docker** - контейнеризация приложения для простого развертывания

## Структура проекта

```
.
├── src/       # Исходный код приложения
│   ├── apps/             # Модули приложения
│   │   └── users/        # Модуль пользователей
│   │       ├── api/      # API слой
│   │       │   ├── controllers/  # Контроллеры API
│   │       │   └── router.py     # Маршрутизация API
│   │       ├── core/     # Бизнес-логика
│   │       │   ├── models/       # Бизнес-модели
│   │       │   ├── repositories/ # Интерфейсы репозиториев
│   │       │   └── services/     # Бизнес-сервисы
│   │       └── db/       # Работа с базой данных
│   │           ├── models.py     # Модели БД
│   │           └── repository.py # Реализация репозиториев
│   ├── db/               # Конфиг базы данных
│   │   ├── base_model.py # Базовый класс моделей
│   │   ├── models.py     # Общие модели БД
│   │   └── setup.py      # Настройка подключения к БД
│   ├── app.py            # Основной файл приложения
│   ├── settings.py       # Конфиг приложения
│   ├── requirements.txt  # Зависимости проекта
│   ├── pyproject.toml    # Конфиг проекта
│   ├── ruff.toml         # Конфиг Ruff
│   └── mypy.ini          # Конфиг mypy
└── dev/                  # Файлы для разработки
    ├── .env             # Переменные окружения
    ├── .env.example     # Пример переменных окружения
    ├── Dockerfile       # Конфигурация Docker
    └── docker-compose.yml # Конфигурация Docker Compose
```

## Установка и запуск

### С использованием Docker (рекомендуется)

1. Скопируйте файл с переменными окружения:
```bash
cp dev/env.example .env
```

2. Запустите приложение:
```bash
docker compose up --build
```

### Локальная установка

1. Создайте виртуальное окружение:
```bash
python -m venv .venv
source .venv/bin/activate  # для Linux/Mac
.venv\Scripts\activate     # для Windows
```

2. Установите зависимости:
```bash
pip install -r requirements.txt
```

3. Запустите приложение:
```bash
uvicorn src.app:app --reload
```

## Лицензия

MIT
