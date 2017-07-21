# kakadu

Модуль для локальных-тестовых изменений удалённого сайта (отладка скриптов, адаптация и т.п.)

## ВНИМАНИЕ!
kakadu переехал в организацию [tazau](https://github.com/tazau)
необходимо изменить ссылки на репозиторий
```
git remote set-url origin https://github.com/tazau/kakadu.git
```

### Содержание
- [Установка](#Установка)
- [Начало работы](#Начало-работы)
- [Параметры CLI](#Параметры-cli)

## Установка
* ```git clone https://github.com/yunusga/kakadu.git && cd kakadu && npm i . -g && npm link```
- возможны ошибки при установке ```gulp-sass``` на Windows OS, скорее всего потребуется установить ```python 2```
- Да, в случае отстутствия установленного в системе python, gulp-sass не устанавливается. Не забудьте во время установки отметить пункт установки переменной окружения или добавить позже, вручную

## Начало работы

- создаем папку (желательно одноименную с сайтом)
- переходим в нее
- открываем в терминале или командной строке (shift + ПКМ для Windows)
- вводим ```kakadu```
- конфигурируем скопированную заготовку проекта
- вводим ```kakadu``` в терминале

После запуска целевой сайт запустится через локальный прокси-сервер и в его ```HTML``` внедряются стили ```app.css``` которые компилируются из файла, выбранного CSS пре-процессора на старте проекта

## Параметры CLI

### Инициализация
- `--proxy [url]` - УРЛ проксируемого сайта
- `--port <n>` - порт для прокси-сервера
- `--tech [tech]` - CSS пре-процессор (доступны: styl, less, scss)

CSS пре-процессор можно всегда сменить, установив значение конфига (**config.js**) ```tech``` в ```styl, less или scss```, дополнительно придется создать файл с расширением выбранного CSS пре-процессора ```app.styl,less или scss```

### Запуск
- `-a, --auth [user@password]` - установка логина для включения авторизации (по умолчанию kakadu@случайный_пароль)
![Авторизация с параметрами по умолчанию](https://1.downloader.disk.yandex.ru/disk/1ce5bf3021add193b99ca15a4673e93f34adaa3ca51b036b531437e4ae499c2f/5971d6ba/_B0aXmp4RJTYYcc2mgnKlhvOzGyFr0KHGWEEtj1g8US-Bl9MJ8jDnVYmreOu0sNin2A8FUuQRBqxdqUHdjNSyQ%3D%3D?uid=0&filename=2017-07-21_11-22-15.png&disposition=inline&hash=&limit=0&content_type=image%2Fpng&fsize=1802&hid=bbd59749690ab2a33589ab135e681db4&media_type=image&tknv=v2&etag=72f0d89eb995b785be0fcc1a49d32779)
- `--nano` - включение cssnano при сборке стилей
