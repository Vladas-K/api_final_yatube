# Проект «API для Yatube»

## Описание
API для социальной сети, в которой реализованы следующие возможности: публиковать записи, комментировать записи, а так же подписываться или отписываться от авторов. Для аутентификации используется JWT-токен.

## Технологии
Python 3.9
Django==3.2.16
djangorestframework==3.12.4
djangorestframework-simplejwt==4.7.2

## Как запустить проект:
Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/Vladas-K/api_final_yatube.git
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv env
```

```
source env/bin/activate
```

Установить зависимости из файла requirements.txt:

```
python3 -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python3 manage.py migrate
```

Запустить проект:

```
python3 manage.py runserver
```

## Примеры запросов

/api/v1/posts/ (GET, POST, PUT, PATCH, DELETE)

/api/v1/posts/{post_id}/comments/ (GET, POST, PUT, PATCH, DELETE)

/api/v1/groups/ (GET)

/api/v1/follow/ (GET, POST)

## Примеры ответов

- /api/v1/posts/ (POST)

    {
        "text": "string",
        "image": "string",
        "group": 0
    }

- /api/v1/posts/{post_id}/comments{id}/ (GET)

    {
        "id": 0,
        "author": "string",
        "text": "string",
        "created": "2019-08-24T14:15:22Z",
        "post": 0
    }

## Авторы
- Владас 
- Яндекс Практикум
