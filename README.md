# Простое веб-приложение на Flask (flask_web_application)
Данный проект реализован для демонстрации своих навыков по тестовому заданию.
В рамках данного веб-приложения реализован следующий функционал:
* регистрация, аутентификация и авторизация пользователей;
* создание, просмотр, изменение и удаление заметок пользователя (для демонстрации выполнения CRUD операций);
* отображение погодных условий по городу, введенным пользователем (интеграция с внешним api). 

Для хранения данных используется база данных PostgreSQL.

## Устновка и локальный запуск
1. Клонируйте репозиторий;
2. Создайте виртуальное окружение;
3. Установите зависимости:
```
pip install -r requirments.txt
```
4. Создайте базу данных PostgreSQL
5. В папке 'webapp' создайте файл config.py и опишите в нем переменные:
```
DB_NAME = 'Наименование вашей базы данных'

# Ваше путь/URI к базе данных
SQLALCHEMY_DATABASE_URI = f'postgresql://login:password@localhost:port/{DB_NAME}'
# Статус отслеживания измененных объектов и их вывода
SQLALCHEMY_TRACK_MODIFICATIONS = False

SECRET_KEY = 'Ваш секретный ключ для защиты от CSRF-атак'

# API ключ доступа к погодным условиям (https://weatherstack.com)
WEATHER_KEY = '236a15e449e790249595c79f1d5984a8'
```

### Создание пользователя - администратор
Из корня проекта запустите файл:
```
python create_admin.py
```
Заполните запрашиваемые данные в консоли.

### Запуск
Чтобы запустить веб-приложение, выполните в консоли:
```
run.bat
```
