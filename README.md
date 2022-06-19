API для сервиса YAMDB

YAMDB собирает отзывы пользователей на произведения в категориях «Книги», «Фильмы», «Музыка». Проект представляет собой web-приложение и базу данных, поднятых в двух docker-контейнерах.

При разработке приложения использованы фреймфорки django и django-rest-framework. В качестве базы выступает postgresql Запуск проекта осуществляется средствами docker

Установка

1. Установка docker и docker-compose

Если у вас уже установлены docker и docker-compose, этот шаг можно пропустить, иначе можно воспользоваться официальной инструкцией.

2. Запуск контейнера

docker-compose up
3. Выключение контейнера

docker-compose down
Использование

Создание суперпользователя Django

docker-compose run web python manage.py createsuperuser
Пример инициализации стартовых данных:

docker-compose run web python manage.py loaddata fixtures.json
Работа с api

Документация ко всем ручкам описана в redoc

Основные использованные технологии

python 3.8
django
drf
posgresql
docker
