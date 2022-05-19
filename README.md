# API Yatube

## Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/pozdnysheva/api_final_yatube.git
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
python -m venv env
```

```
source venv/Scripts/activate
```

Установить зависимости из файла requirements.txt:

```
python -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python manage.py migrate
```

Запустить проект:

```
python manage.py runserver
```
## Доступные эндпоинты

`api/v1/posts/` : получаем список всех постов или создаём новый пост;
`api/v1/posts/{post_id}/` : получаем, редактируем или удаляем пост по id;
`api/v1/posts/{post_id}/comments/` : получаем список всех комментариев поста с id=post_id или создаём новый, указав id поста, который хотим прокомментировать;
`api/v1/posts/{post_id}/comments/{comment_id}/` : получаем, редактируем или удаляем комментарий по id у поста с id=post_id;
`api/v1/groups/` : получаем список всех групп;
`api/v1/groups/{group_id}/` : получаем информацию о группе по id;
`api/v1/follow/` : получаем все подписки пользователя, сделавшего запрос, или подписываемся на пользователя, переданного в теле запроса;

http://127.0.0.1:8000/api/v1/jwt/create/
http://127.0.0.1:8000/api/v1/jwt/refresh/
http://127.0.0.1:8000/api/v1/jwt/verify/
