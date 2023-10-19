# Описание:
Портал "Yatube" - это удобный инструмент для людей, желающих высказать накопившиеся у них мысли в письменной форме на любую тематику! Портал предлагает размещение публикаций, в том числе в тематических группах, а также комментирование публикаций и возможность подписки на интересных Вам авторов для удобной навигации. Присоединяйтесь! Портал работает через собственный API, примеры запросов и ответов ниже.

# Установка:
Чтобы развернуть у себя проект, необходимо клонировать репозиторий из GitHub:

```
git clone https://github.com/yandex-praktikum/api_final_yatube.git
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv env
```

Для Linux и Mac OS:

```
. env/bin/activate
```

Для OS Windows:

```
env\Scripts\activate.bat
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

# Примеры запросов:

1. Запрос на получение публикаций:

```
http://127.0.0.1:8000/api/v1/posts/
```

Ответ:
```
{
  "count": 123,
  "next": "http://api.example.org/accounts/?offset=400&limit=100",
  "previous": "http://api.example.org/accounts/?offset=200&limit=100",
  "results": [
    {
      "id": 0,
      "author": "string",
      "text": "string",
      "pub_date": "2021-10-14T20:41:29.648Z",
      "image": "string",
      "group": 0
    }
  ]
}
```

2. Запрос на получение списка сообществ:

```
http://127.0.0.1:8000/api/v1/groups/
```

Ответ:
```
[
  {
    "id": 0,
    "title": "string",
    "slug": "string",
    "description": "string"
  }
]
```

3. Запрос на частичное обновление комментария (вместо {post_id} поставьте порядковый номер поста, вместо {id} порядковый номер комментария):

```
http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/{id}/
```

Ответ:
```
{
  "id": 0,
  "author": "string",
  "text": "string",
  "created": "2019-08-24T14:15:22Z",
  "post": 0
}
```

# Об авторе:

Автор проекта - Зайковский Всеволод.

Email для связи - 4lk4st@gmail.com

