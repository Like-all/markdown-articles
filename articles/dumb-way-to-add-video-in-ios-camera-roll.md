Тупое руководство по добавлению видеоролика в CameraRoll в iOS
==============================================================

CameraRoll в iOS - штука одновременно тупая и сложная. Тупая потому, что в неё валится весь фото и видеохлам: скриншоты, картинки из браузеров, фотографии и прочая чушь складывается в одну директорию. Сложная потому, что записать файл в директорию мало, ибо CameraRoll ничего не знает о существовании этих файлов без добавления их в специальную БД, запись в которую осуществляется через хитромудрую ORM. Но, всё же, способы есть:

+ Создаём видеоролик, который может быть воспроизведён в iOS, желательно дать ему расширение `.MOV`
+ Закидываем его по ssh/скачиваем посредством wget в `/private/var/mobile/Media/DCIM/100APPLE`
+ Удаляем файл `/private/var/mobile/Media/PhotoData/Photos.db`
+ Перезагружаем устройство
+ Заходим в CameraRoll и ждём обновления
