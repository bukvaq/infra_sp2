# api_yamdb
Проект YaMDb собирает отзывы пользователей на различные произведения.
***
### Возможности:
* Регистрация (по ник-нейму и электронной почте)
* Получение токена (по ник-нейму и коду подтверждения почты)
* Написание отзыва для произведений 
* Оценка произведений по шкале от 1 до 10
* Комментирование отзыва
* Админ может создавать/удалять жанры, категории, произведения
* Админ может назначать модераторов из пользователей
***
### Шаблон .env файла:
DB_ENGINE=django.db.backends.postgresql
DB_NAME=postgres
POSTGRES_USER=*пользователь*
POSTGRES_PASSWORD=*пароль*
DB_HOST=db 
DB_PORT=5432 
***
### Как запустить проект:

из папки infra:

docker-compose up

Ссылка на проект:
http://51.250.19.35
***
Документация доступна по адресу:
http://51.250.19.35/redoc/
***
### Как запустить автотесты:
после запуска проекта, в папке infra_sp2:

pytest

### Пример работы API:

Запрос для создания поста:
```python
import requests
from pprint import pprint
url = 'http://127.0.0.1:8000/api/v1/categories/'
request = requests.get(url).json()
pprint(request)
```
Ответ от API:
```json
{"count": 3,
 "next": "None",
 "previous": "None",
 "results": [{"name": "Фильм", "slug": "movie"},
             {"name": "Книга", "slug": "book"},
             {"name": "Музыка", "slug": "music"}]}
```
***
## Авторы проекта:
* Дарья Понамарёва
* Евгений Салахутдинов
* Максим Шамшурин
***
