# API для Yatube

### Описание

Проект реализует возможность публикации и редактирования записей, комментирования, использования системы подписок в социальной сети Yatube

### Технологии

Python 3.7, Django 3.2, DRF, JWT + Djoser

### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/yandex-praktikum/kittygram2plus.git
```

```
cd kittygram2plus
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv venv
```

```
source venv/bin/activate
```

```
python3 -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:

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

### Примеры запросов к API:
Для неавторизованных пользователей работа с API доступна в режиме чтения:

```
GET api/v1/posts/ - получить список всех публикаций
```
```
GET api/v1/posts/{id}/ - получение публикации по id
```
```
GET api/v1/groups/ - получение списка доступных сообществ
```
```
GET api/v1/groups/{id}/ - получение информации о сообществе по id
```
```
GET api/v1/{post_id}/comments/ - получение всех комментариев к публикации
```
```
GET api/v1/{post_id}/comments/{id}/ - получение комментария к публикации по id
```
Для авторизованныx пользователей доступен расширенный функционал.

Полная документация к API доступна по адресу `http://localhost:8000/redoc/`