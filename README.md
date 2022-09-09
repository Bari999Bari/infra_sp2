# YAMDB
YAMDB

### Описание:

Проект YaMDb собирает отзывы пользователей на произведения. Произведения делятся на категории: «Книги», «Фильмы», «Музыка». Список категорий со временем может быть расширен.
Сами произведения в YaMDb не хранятся, здесь нельзя посмотреть фильм или послушать музыку.
В каждой категории есть произведения: книги, фильмы или музыка. Например, в категории «Книги» могут быть произведения «Винни-Пух и все-все-все» и «Марсианские хроники», а в категории «Музыка» — песня «Давеча» группы «Насекомые» и вторая сюита Баха.
Произведению может быть присвоен жанр из списка предустановленных (например, «Сказка», «Рок» или «Артхаус»). Новые жанры могут быть созданы по жеданию пользователей, но создавать их могут только администраторы.
Благодарные или возмущённые пользователи оставляют к произведениям текстовые отзывы и ставят произведению оценку в диапазоне от одного до десяти; из пользовательских оценок формируется усреднённая оценка произведения — рейтинг. На одно произведение пользователь может оставить только один отзыв

### Как запустить проект:

Клонировать репозиторий и перейти в папку с файлом
docker-compose.yaml(перед этим у вас должен быть установлен Docker)
в командной строке:

```
git clone ...
```

```
cd infra_sp2/infra
```
Запустить сборку контейнера 
```
docker-compose up
```
Выполните по очереди команды:
```
docker-compose exec web python manage.py migrate
docker-compose exec web python manage.py createsuperuser
docker-compose exec web python manage.py collectstatic --no-input 
```

### Примеры:

Примеры и инструкцию можмо посмотреть тут:
http://127.0.0.1:8000/redoc/
