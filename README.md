**protocol** - Протокол по которому пользователи заходят на ваш сайт(http или https)

**domain** - Домен вашего сайта

**port** - Порт вашего сайта, если ваш сайт находится на 80 порте, т.е. в адрессной строке после домена через двоеточие не указано число, то данный параметры указывать не прийдётся!

**protocol://domain:port/** - Может быть как `https://example.com/` так и `https://example.com:80/`

## Перед установкой плагина

1. Создадим главную страницу(если не создана)
- Переходим в `Site`
- Заполняем Page name - `index`
- Нажимаем `Save`
2. Добавим хотя бы один товар в магазин(если нет товаров)
- Переходим в `Store` > `Products` > `New product`
- Заполняем Product name, Price
- Нажимаем `Save`

## Установка

1. Распаковываем содержимое репозитория в корень сайта
2. Переходим в `Store` > `Settings` > `Payment` > `Add payment option` > `Mandarin Bank`
3. Заполняем ID Мерчанта, Secret Мерчанта
4. Нажимаем `Save`
5. Cоздаём страницу, которая будет служить страницей, на которую будет ссылаться пользователь после проплаты(если не создана)
- Переходим в `Site`
- Заполняем Page name - `result`, Page URL - **protocol://domain:port/result**
- Нажимаем `Save`
6. В системе MandarinPay указываем
- callbackURL **protocol://domain:port/payment-mandarin.php**
- returnURL **protocol://domain:port/result**
