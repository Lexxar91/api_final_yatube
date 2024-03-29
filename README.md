**Задача учебного проекта**

Задачей учебного проекта являлось создание API для упрощенной версии блога "Yatube".

### Стэк технологий:

[![Python](https://img.shields.io/badge/-Python-464646?style=flat-square&logo=Python)](https://www.python.org/)
[![Django](https://img.shields.io/badge/-Django-464646?style=flat-square&logo=Django)](https://www.djangoproject.com/)
[![Django REST Framework](https://img.shields.io/badge/-Django%20REST%20Framework-464646?style=flat-square&logo=Django%20REST%20Framework)](https://www.django-rest-framework.org/)
[![Simple-JWT](https://img.shields.io/badge/-JWT-464646?style=flat-square&logo=JWT)](https://jwt.io/)

**Описание проекта**

Социальная сеть Yatube это блог предназначенный для публикации личных записей. По желанию посты могут быть опубликованы в группах. Проект предоставляет возможность подписываться на авторов и оставлять комментарии к записям. Аутентификация пользователей осуществляется по JWT-токену.

**Доступные эндпоинты:**

/api/v1/jwt/create/ - POST: получение JWT-токена;

/api/v1/jwt/refresh/ - POST: обновление JWT-токена;

/api/v1/jwt/verify/ - POST: Проверка JWT-токена;

/api/v1/posts/ - GET: получение всех записей, POST: добавление новой записи;
/api/v1/posts/{id}/ - GET: получение записи, PUT: обновление записи, PATCH: частичное обновление записи, DELETE: удаление записи;

/api/v1/posts/{post_id}/comments/ - GET: получение всех комментов к записи, POST: добавление нового коммента к записи;

/api/v1/posts/{post_id}/comments/{comment_id}/ - GET: получение коммента, PUT: обновление коммента, PATCH: частичное обновление коммента, DELETE: удаление коммента;

/api/v1/follow/ - GET: получение списка всех своих подписок, POST: создание новой подписки;

/api/v1/group/ - GET: получение списка всех групп. /api/v1/group/{group_id} - GET: получение информации о группе.

Спецификация API по всем доступным эндпоинтам, структурам данных и параметром запросов будет доступна после запуска проекта по адресу http://localhost:8000/redoc/.


**Как развернуть**

Склонируйте репозиторий: https://github.com/Lexxar91/api_final_yatube.git.

С помощью инструкции создайте и активируйте виртуальное окружение.

Установите зависимости: pip install -r requirements.txt.

Примените миграции: python manage.py migrate.

Запустите сервер: python manage.py runserver, и приступайте к работе с API!

Как работать с API

Для работы с API подходят CURL или Postman. Спецификация API по всем доступным эндпоинтам, структурам данных и параметром запросов будет доступна после запуска проекта по адресу http://localhost:8000/redoc/.
