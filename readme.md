# Eventicious API

PHP-класс для работы с api сервиса [eventicious.com](https://eventicious.com/)

## Установка

### Установка через Composer

Запустите

```
php composer.phar require gulik17/eventicious "~1"
```

или добавьте

```
"gulik17/eventicious": "~1"
```

в секцию ```require``` вашего composer.json

## Использование

Простая авторизация (с помощью token):

```php
$host = "https://admin.eventicious.com/";
$code = "Your_Authorization_Key";

$client = new \Gulik17\Eventicious\Eventicious();
$client->setHost($host);
$client->setCode($code);
```

Отправка SMS:

```php

$result = $client->speakersCreate(
    1,
    "Иван",
    "Иванов",
    "Aurus",
    "Повар",
    "Москва",
    "https://vk.com/ivan_ivanov",
    "https://twitter.com/",
    "https://fb.com/",
    "ivan@aurus.ru",
    "79885001133",
    "Звездный повар Ваня",
    true,
    "picture_url",
    1)

print_r($result);
```
return array Массив аналогичен запросу

Ответ:
Аналогичен запросу. Содержит дополнительные поля, например networkingCode — ID-участника (персональный код доступа в приложение).


## Каждый метод в классе содержит подробное описание (PhpDoc)


## Автор

[Владимир Гулеватый](https://github.com/gulik17/), e-mail: [gulik.v@bk.ru](mailto:gulik.v@bk.ru)
