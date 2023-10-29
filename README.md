# Домашнее задание к занятию «Кеширование Redis/memcached» - `Костюк Денис`

## Задание 1. Кеширование

Приведите примеры проблем, которые может решить кеширование.

Приведите ответ в свободной форме.

## Ответ 1:

Как было озвучено на лекции и отражено в презентации:

•	Повышение производительности (достигается за счет складывания в кэш данных, к которым чаще всего происходит обращение);

•	Увеличение скорости ответа;

•	Экономия ресурсов (например, применяя кэширование тяжелых запросов к БД);

•	Сглаживание бустов трафика. (Например, во время черной пятницы онлайн-магазины используют кэш, чтобы переживать резкое увеличение трафика).


## Задание 2. Memcached

Установите и запустите memcached.

Приведите скриншот systemctl status memcached, где будет видно, что memcached запущен.

## Ответ 2:

![Скрин1](https://github.com/denniskostyuk/cash/blob/main/task_2.png)

## Задание 3. Удаление по TTL в Memcached

Запишите в memcached несколько ключей с любыми именами и значениями, для которых выставлен TTL 5.

Приведите скриншот, на котором видно, что спустя 5 секунд ключи удалились из базы.

## Ответ 3:

![Скрин2](https://github.com/denniskostyuk/cash/blob/main/task_3.png)

## Задание 4. Запись данных в Redis

Запишите в Redis несколько ключей с любыми именами и значениями.

Через redis-cli достаньте все записанные ключи и значения из базы, приведите скриншот этой операции.

## Ответ 4:

Устанавливаем и проверяем активность Redis:
![Скрин3](https://github.com/denniskostyuk/cash/blob/main/task_41.png)

Записываем ключи со значениями и достаем данные:
![Скрин4](https://github.com/denniskostyuk/cash/blob/main/task_42.png)

## Задание 5*. Работа с числами

Запишите в Redis ключ key5 со значением типа "int" равным числу 5. Увеличьте его на 5, чтобы в итоге в значении лежало число 10.

Приведите скриншот, где будут проделаны все операции и будет видно, что значение key5 стало равно 10.

## Ответ 5:

![Скрин2](https://github.com/denniskostyuk/cash/blob/main/task_3.png)
