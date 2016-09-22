# kakadu

Модуль для ускорения стилевой адаптации сайта

## Установка
* ```git clone https://github.com/yunusga/kakadu.git && cd kakadu && git pull --all && git checkout develop && npm i . -g && npm link```
* возможны ошибки при установке ```gulp-sass``` на Windows OS, скорее всего потребуется установить ```python 2```

## Как рабоатет?

* создаем папку (желательно одноименную с сайтом)
* переходим в нее
* открываем в терминале или командной строке (shift + ПКМ для Windows)
* вводим ```kakadu```
* отвечаем на вопросы модуля

после запуска целевой сайт запустится через локальный прокси-сервер и в его ```HTML``` внедряются стили ```_app.css``` которые компилируются из файлы выбранного CSS пре-процессора на старте проекта

CSS пре-процессор можно всегда сменить, установив значение ```tech``` в ```styl, less или scss```, дополнительно придется создать файл с расширением выбранного CSS пре-процессора ```_app.styl,less или scss```

### Все!
