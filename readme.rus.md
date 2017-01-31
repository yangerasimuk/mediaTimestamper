# photoTimestamper
Консольная программа для macOS для массового переименования фотографий и зависимых файлов.

## Немного истории
Я очень люблю фотографировать, и не только я один - моя семья фотает всё показавшиеся интересным или достойным сохранения в нашей семейной истории. Всего у нас есть одна любительская зеркалка, три телефона и два планшета. Фотографии я храню на дисках в самолично созданных папках, сторонние программы каталогизации и хранения избегаю.

Всё было прекрасно, до того момента когда сохраняя фотографии в одной папке у меня пересеклись наименования разных файлов, и я чуть не потерял свои бесценные снимки.

Почему я сливал фотки в одну папку? Мне нравится смотреть на событие со всех сторон, в смысле через все доступные стекла. Предположим, у вас случился день езды и вы снимали несколькими фотиками, вполне логично, что все фотки окажутся в одной папке.

Вы счастливый пользователь iPhoto, Aperture, Adobe Lightweight или иных программ с возможностью ведения каталогов? Тогда моя программа не для вас.

## Решение
Итак, есть проблема - неуникальные называния для фото-файлов. Оптимальным решением данной проблемы мне видится добавление к исходному имени файла, уникального значения - времени создания фотографии. Большинство современных камер сохраняет информацию о создании фото в метаданных EXIF.

DSC_2987.JPG -> 2017-01-20_21-40-15_DSC_2987.JPG

У подобного решения есть приятный бонус - при сортировке фотографий по имени, вы получите файлы выстроенные во временную линию, что упростит последующий просмотр сначала до конца фотосессии.

Посмотрите на эти 2 списка, какой из них будет более рабочим:
* DSC_2987.JPG
* DSC_2988.JPG
* DSC_2989.JPG
* DSC_2990.JPG
* IMG_0182.JPG
* IMG_0183.JPG
* IMG_0184.JPG

и

* 2017-01-20_18-33-30_IMG_0182.JPG
* 2017-01-20_21-40-15_DSC_2987.JPG
* 2017-01-20_21-45-25_DSC_2988.JPG
* 2017-01-20_21-46-55_DSC_2989.JPG
* 2017-01-20_22-05-13_IMG_0183.JPG
* 2017-01-20_22-06-47_IMG_0184.JPG

## Установка
photoTimestamper - консольная программа для macOS, обрабатывающая файлы в текущей папке. Чтобы она работала в произвольной папке, необходимо либо поместить в неё саму программу, либо разместить её в одну из общедоступных папок, например, /usr/local/bin.


## Работа
Для запуска программы откройте консоль (Terminal), перейдите в папку с фотографиями и введите photoTimestamper или (phototimestamper).

### Командная строка
phototimestamper - программа запустится с настройками по-умолчанию (вывод только ошибок, переименование только файлов с EXIF),

phototimestamper -i или --info - вывод дополнительной информации,

phototimestamper -n или --noexif - переименование фото с недоступным EXIF, по аттрибутам файла,

phototimestamper -in или --info --noexif - вывод подробной информации и переименование всех фотографий (как с EXIF, так и без). В работе.

## Производительность
На моем компьютере - MacBook Pro (Retina, 15-inch, Late 2013, 2GHz i7, 8GB 1600 MHz DDR3, macOS Sierra), 1000 фотографий и зависимых файлов обрабатывается за 1 минуту.

Ян Герасимук

30 января 2017 г.