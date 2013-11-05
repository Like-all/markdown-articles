Почему я использую mcabber в качестве мессенджера(доходчивое объяснение для тех, кто ещё не понял)
==================================================================================================

Пошёл уже практически пятый год, как я использую [mcabber](http://mcabber.com), а на меня до сих пор смотрят как на юродивого и задают смешные вопросы. Зачастую, это просто праздный интерес, однако и этого достаточно, чтобы начать меня раздражать. Клиент этот обладает множеством достоинств и недостатков, поэтому вопросы получаются из: 

    + того, что кто-то не понимает достоинств этого мессенджера;
    + того, что кто-то не понимает, как жить с недостатками этого мессенджера;
    + всего вышеперечисленного.

Ок, раз пошла такая пьянка, я расскажу обо всём этом. Один раз. Здесь.

Сперва, об очевидных мне достоинствах:

####Малый размер устанавливаемого пакета
Да, именно это и есть первопричина. Пакет с клиентом весит меньше мегабайта. Ну либу ещё придётся доставить. Тогда, в далёком 2008 году, у меня из интернетов кроме GPRS, который развивал фантастические 7Кб/с, ничего не было. Мало того, что GPRS медленный, так ещё и дорогой зараза. 7 рублей за мегабайт - это вам non penis canina. Перепробовано было несколько легковесных клиентов: climm, centerim, finch и mcabber. И только последний покорил меня удобочитаемыми конфигами и приятным интерфейсом. О них в следующих подпунктах.

####Интерфейс
Честно говоря, ничего более аккуратного я ещё не видел. Всё на своих местах: ростер, буфер логов, буфер чата, поле ввода текста и команд. Никакого буллшита вроде картинок, смайликов, свистелок, перделок, вкладок и многооконности. Всё видно как на ладони. При желании ростер и буфер логов можно подвинуть на противоположный край или вообще скрыть. Красота, да и только. Навигация по ростеру проста до безобразия: жмём `PgUP` или `PgDn` и перемещаемся, соответственно, вверх или вниз. Если надо быстро перескочить к какому либо контакту, то можно использовать команду `/roster search`, или, если сделан алиас, прос то `/s`. Детально расписывать все команды я не буду, их много и для этого можно нажать `man mcabber`. Если Вы не любите читать маны - этот клиент не для Вас, дальше можете не читать. Отмечу лишь, что помимо набивания команд в поле ввода руками их можно посылать в клиент через **fifo**. Просто включаем в конфиге соответствующий модуль и записываем команды в файл любым удобным способом. Также, можно настроить реакцию клиента на любые типы сообщений путём написания программы на любом угодном душе пользователя языке программирования. Лишь бы аргументы принимать умел.

####Конфигурационные файлы
Здесь тоже всё предельно прозрачно. Почти все параметры конфигурируются путём `set param = value`. И никаких глазовыжигающих иксемелей или графических приблуд, для которых требуется манипулятор типа "мышь". Также можно определять алиасы, хоткеи, цвета, определять события до и после коннекта, подключать модули, а также, с помощью команды `source`, подключать другие конфиги, вынесенные в отдельные файлы. Детально конфигурирование я рассматривать не буду, для этого есть [example](https://bitbucket.org/McKael/mcabber-crew/raw/tip/mcabber/mcabberrc.example). Всё же, это статья о том, "**почему**", а не о том, "**как**".

####Логи чата
И за это я тоже люблю mcabber. Да, логи можно читать невооружённым глазом. Опять же, никаких [иксемелей](http://ru.wikipedia.org/wiki/Xml), [джысонов](http://ru.wikipedia.org/wiki/JSON), [скулайтов](http://ru.wikipedia.org/wiki/SQLite) и [многодб](http://ru.wikipedia.org/wiki/MongoDB). Соотвественно, можно применять для поиска нужного текста такие средства, как `sed`, `cut`, `grep`, `awk` и многие другие.

####Мобильность
Здесь mcabber, по моему скромному мнению, вообще вне конкуренции. Текстовый интрефейс настолько лёгок и хорошо масштабируем, что пролезет в любой терминал через ssh. А поскольку ssh-клиенты есть практически для любой мало-мальски развитой пользовательской операционной системы, доступ к своему чатику я могу без особого труда получить вообще из любого места, в котором есть интернет. Разве что кейлоггеров на чьей-нибудь операционной системе стоит опасаться, но и для этого можно таскать с собой ридонли-флэшку с клиентом и ключиками. В общей сложности, мне удавалось использовать mcabber с комфортом на следующих операционных системах:

    + Microsoft Windows([PuTTY](http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html), [KiTTY](http://www.9bis.net/kitty/)) 
    + Apple Mac OS X(native, [OpenSSH](http://www.openssh.com/))
    + GNU/Linux(native, [OpenSSH](http://www.openssh.com/), [MOSH](http://mosh.mit.edu))
    + FreeBSD(native, [OpenSSH](http://www.openssh.com/))
    + Symbian([S2PuTTY](http://sourceforge.net/projects/s2putty/))
    + Maemo & MeeGo([OpenSSH](http://www.openssh.com/))
    + Android
        + [ConnectBot](https://play.google.com/store/apps/details?id=org.connectbot)
        + [Irssi ConnectBot](https://play.google.com/store/apps/details?id=org.woltage.irssiconnectbot)
        + [VX ConnectBot](https://play.google.com/store/apps/details?id=sk.vx.connectbot)
        + [ServerAuditor](https://play.google.com/store/apps/details?id=com.crystalnix.gloria)
        + [JuiceSSH](https://play.google.com/store/apps/details?id=com.sonelli.juicessh)
    + Apple iOS(https://itunes.apple.com/ru/app/id549039908?mt=8)

Как видите, вариантов достаточно много. Кстати, при использовании mcabber через ssh отпадает надобность в синхронизации чатлогов: нужно всего лишь зайти на сервер и вызвать `screen` или `tmux`. Удобно, если не хочется терять нить беседы.