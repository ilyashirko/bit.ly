# Обрезка ссылок с помощью bit.ly
Генерирует короткие ссылки bit.ly и считает количество переходов по таким ссылкам

## Как установить
###Для работы вам понадобится токен.  
Получить его можно здесь: 
>https://app.bitly.com/settings/api/  
Регистрируетесь, вводите пароль и нажимаете "Сгенерировать токен"  
Токен выглядит примерно так: >"3ig534hv53uv5ih4gjh34gb5jh3bjhb345b3j5b"  
Его необходимо поместить в файл ".env" после знака "="  
Должно получиться так:  
>BITLINK_TOKEN=3ig534hv53uv5ih4gjh34gb5jh3bjhb345b3j5b  

###Установка зависимостей.
Вам потребуется python3 и pip (pip3).
> pip3 install -r requirement.txt

## Как запустить
вместо ССЫЛКА вводите ссылку в формате "http://www.google.com"
>$python3 main.py ССЫЛКА


# Описание функций main.py
## is_bitlink
Проверяет является ли ссылка сокращенной.
Если это битлинк - возвращает True, в противном случае False

## count_click
Если введеная ссылка сокращенная:
 - запрашивает количество переходов по ней;
 - выводит на экран в случае успешного ответа сервера.
 - выводит ошибку в случае отсутствия ответа.

## shorten_link
Запрашивает у сервера сокращенную ссылку для введенной ссылки.  
Ссылка должна быть указана полностью, с протоколом, иначе отобразится ошибка.
Выводит на экран полученную ссылку