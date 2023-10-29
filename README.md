# Домашнее задание к занятию «Резервное копирование» - `Костюк Денис`

## Задание 1. Кеширование

Приведите примеры проблем, которые может решить кеширование.

Приведите ответ в свободной форме.

## Ответ 1:

Как было озвучено на лекции и отражено в презентации:

#### •	Повышение производительности (достигается за счет складывания в кэш данных, к которым чаще всего происходит обращение);
#### •	Увеличение скорости ответа;
#### •	Экономия ресурсов (например, применяя кэширование тяжелых запросов к БД);
#### •	Сглаживание бустов трафика. (Например, во время черной пятницы онлайн-магазины используют кэш, чтобы переживать резкое увеличение трафика).









#### •	Составьте команду rsync, которая позволяет создавать зеркальную копию домашней директории пользователя в директорию /tmp/backup
#### •	Необходимо исключить из синхронизации все директории, начинающиеся с точки (скрытые)
#### •	Необходимо сделать так, чтобы rsync подсчитывал хэш-суммы для всех файлов, даже если их время модификации и размер идентичны в источнике и приемнике.
#### •	На проверку направить скриншот с командой и результатом ее выполнения

##### Исходное состояние домашней директории:
![Скрин1](https://github.com/denniskostyuk/rsync/blob/main/task_11.png)

##### Делаем копирование:
![Скрин2](https://github.com/denniskostyuk/rsync/blob/main/task_12.png)
   
##### Состояние целевой директории (с бэкапом):
![Скрин3](https://github.com/denniskostyuk/rsync/blob/main/task_13.png)


### Задание 2
#### •	Написать скрипт и настроить задачу на регулярное резервное копирование домашней директории пользователя с помощью rsync и cron.
#### •	Резервная копия должна быть полностью зеркальной
#### •	Резервная копия должна создаваться раз в день, в системном логе должна появляться запись об успешном или неуспешном выполнении операции
#### •	Резервная копия размещается локально, в директории /tmp/backup
#### •	На проверку направить файл crontab и скриншот с результатом работы утилиты.

##### Bash-скрипт:
![Скрин4](https://github.com/denniskostyuk/rsync/blob/main/task_21.png)

##### crontab (запуск скрипта каждые сутки в 0 часов 0 минут):
![Скрин5](https://github.com/denniskostyuk/rsync/blob/main/task_22.png)

##### Результат - записи в syslog:
![Скрин6](https://github.com/denniskostyuk/rsync/blob/main/task_23.png)

##### Исходное состояние домашней директории:
![Скрин7](https://github.com/denniskostyuk/rsync/blob/main/task_24.png)

##### Результат - cостояние целевой директории:
