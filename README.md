# ЗооДруг

Сайт доступен по адресу: http://kristimo.beget.tech/.

## Информация о проекте
Сайт представляет собой информационную базу для поиска животных.

Целью проекта является создание базы по подбору семей для животных (из приютов города Кирова) и их консультация в области зоопсихологии и ветеринарии с дальнейшим ненавязчививым отслеживанием жизни пристроенных животных.

[Видео о проекте](https://vk.com/video134054390_456240002)

## Роль в проекте
Разработчик сайта.

## Запуск на локальном утройстве
### Подготовка
Для запуска сайта создате вирутальное окружение:
```
python -m venv venv
```

И установите необходимые зависимости:
```
pip install -r requirements.txt
```

После необходимо в корне проекта создать .env файл, в котором указать следующие переменные:
```
# Настройка работы сайта
DEBUG = True

# Настройка почты
EMAIL_BACKEND ='django.core.mail.backends.smtp.EmailBackend'
EMAIL_HOST = 'smtp.yandex.ru'
EMAIL_PORT = 465
EMAIL_USE_TLS = False
EMAIL_USE_SSL = True
EMAIL_HOST_USER = 'your_yandex_mail@yandex.ru'
EMAIL_HOST_PASSWORD = 'your_password'
```

Если в качестве почты используется другой сервер (mail.ru, gmail.ru), то соответсвующую конфигурацию можно найти [здесь](https://pocoz.gitbooks.io/django-v-primerah/content/glava-2-uluchshenie-bloga-s-pomoshyu-rasshirennyh-vozmozhnostej/otpravka-postov-na-e-mail/otpravka-e-mail-v-django.html).

### Запуск
Для запуска сайта перейдите в директорию _zoofriends_ командой:
```
cd zoofriends
```

И введите в консоль:
```
python manage.py runserver
```