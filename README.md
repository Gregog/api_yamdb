# Реализация API для сервиса Ya|MDb на базе Django REST
## Данный проект выполнен в рамках обучения на курсах Яндекс.Практикум
### Установка и запуск
#### Выполните следующие команды в терминале:
##### 1. Установка pip
```
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
python get-pip.py
```
##### 2. Подготовьте виртуальное окружение
```
pip install virtualenv
mkdir home/Yatube_api
cd home/Yatube_api
virtualenv env
source env/bin/activate
```
##### 3. Загрузите проект с Github
```
git clone https://github.com/gregog/api_yamdb
cd api_final_yatube
```
##### 4. Установите необходимые зависимости
```
pip install -r requirements.txt
```
##### 5. Запустите проект
```
python3 manage.py migrate
python3 manage.py runserver
```
### Доступные методы
```
api/v1/titles (GET, POST)
api/v1/titles/<title_id>/ (GET, POST, PUT, PATCH, DELETE)
api/v1/titles/<title_id>/comments/ (GET, POST)
api/v1/titles/<title_id>/comments/<comment_id> (GET, POST, PUT, PATCH, DELETE)
api/v1/genre/ (GET, POST)
api/v1/category/ (GET, POST)
```
### Пример возможного запроса
```
import requests

URL = '127.0.0.1/api/v1/titles/'
data = {'text' = 'Мой тестовый пост'}
headers = {'Authorization':'Bearer *ваш токен, (для получения перейдите по /api/token/)*'}
re = requests.post(URL, data=data, headers=headers)
```
*Более подрбную информацию вы можете получить после запуска проекта (примеры запросов, их описание) зайдя  на 127.0.0.1/redoc/*

### Почта для обратной связи idzaoshang@gmail.com
