# SBozhko

_23 августа 2015_

## Понедельник <small>39 твитов</small>

Доброе утро понедельника! По просьбе <a href="https://twitter.com/dcromster" title="Roman Milovskiy">@dcromster</a> на этой неделе с вами <a href="https://twitter.com/SBozhko" title="Svetλana">@SBozhko</a> из славного города Минска.

Занимаюсь нагруженным сервер-сайдом на Scala, что-то около обработки больших данных.А по пятницам превращаюсь в подкастера (привет, <a href="https://twitter.com/search?q=%23devzen">#devzen</a>)

На этой неделе поговорим про Scala: чем она хороша, для кого, а кому ее лучше избегать.

Джавистам перейти на Scala очень легко. Просто начните новый проект либо модуль существующего на этом языке.

Примерно таким же образом год назад моя команда перешла на него. До сих пор не пожалели.

А для сомневающихся вот вам быстрое 5-часовое введение от <a href="https://twitter.com/mr_mig_by" title="Alexey Migutsky">@mr_mig_by</a> <a href="http://t.co/WRNFie3t6m">m.habrahabr.ru/post/209532/</a>

RT <a href="https://twitter.com/RusAlexander" title="Alex Pletnev">@RusAlexander</a>: <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> какие основные плюсы ?

Во-первых, Scala – это красиво :)

А вообще, значительно меньше boilerplate-кода. Работа с коллекциями в разы приятнее. Уже не могу жить без map, filter, zip

Наличие фреймворка легковесных потоков в виде akka. И, конечно же, Option, Either и case-классы. Отвыкать от этого совсем не хочется.

И, наконец, посмотрите на Scala-вакансии. Как правило, это не типичный для Java кровавый enterprise, а куда более интересный мир high-load

Что касается книг, то я рекомендую Programming in Scala <a href="http://t.co/hDKxBdXgsG">amazon.com/Programming-Sc…</a>. Да, большая, но зато очень доскональная и понятная

Есть в этом толика сарказма ;) <a href="https://t.co/cDZ67v12Zq">twitter.com/Timrael/status…</a>

В основом это возможность сделать одно и то же разными способами. Так что будьте готовы к долгим спорам из-за стиля <a href="https://t.co/GAk4KThs9M">twitter.com/vmakhaev/statu…</a>

Кроме этого в той же akka есть много подводных камней, если работаете с каким-либо ресурсом синхронно.

В этом случае лучше для таких "блокирующих" акторов делать отдельный диспетчер (по сути это пул потоков).

А здесь можно подробнее почитать, как с этим жить: <a href="http://t.co/AtHEVMk70r">doc.akka.io/docs/akka/snap…</a> (Blocking Needs Careful Management)

Кроме этого, в Scala dsl считается чуть ли не высшей формой развития разных библиотек. Не могу сказать, что я разделяю эту страсть к dsl-ям.

Ну и будьте готовы сами допиливать существующие либы. А из-за того, что они написаны на более сложной Scala, это может быть довольно трудно

Но здесь я вспомню слова Баруха <a href="https://twitter.com/jbaruch" title="jbaruch">@jbaruch</a>: "Технологии идеальны, а люди мудаки". Так что Scala хороша ;) А вся проблема в людях, как и везде.

Да, такое порой имеет место при сильной упоротости разработчиков. Скатиться в write-only код можно довольно легко. <a href="https://t.co/UclPLF0P6R">twitter.com/Foxcool_ru/sta…</a>

RT <a href="https://twitter.com/Bugagazavr" title="Bugagazavr">@Bugagazavr</a>: <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> недавно в Scala, почему в akka задепрекейтели redis как broker? Как сереализует данные, если речь о remote а…

Задепрекейтили Redis не как брокер, а реализацию мейлбокса, который хранит сообщения в Redis.Впрочем, такая же история с ZooKeeper и MongoDB

Потому что механизм durable мейлбоксов разрабатывается в модуле akka-persistent. А иначе получалось ненужное дублирование.

В remote акторах сериализация проиходит с ичпользование протобафа. Для этого есть поддержка из коробки. Но можно и свое взять, если надо.

RT <a href="https://twitter.com/Foxcool_ru" title="Foxcool">@Foxcool_ru</a>: <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> перл - не синоним write-only кода. Ужасно можно писать и на питоне.  Я имел ввиду схожесть философских отпра…

Мне,конечно, сложно судить о философии и инструментах Perl. Но из того, что я знаю, со Scala мало пересечений. А кто-либо может из сравнить?

RT <a href="https://twitter.com/IldarTwitt" title="Ildar Fatikhov">@IldarTwitt</a>: <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> А что можно почитать по akka? Что-нибудь ближе к архитектуре, проектированию. Книги, блоги и.т.п.

Документация у akka на официальном сайте отличная. Что очень здорово, что есть pdf, как для Scala, так и для Java API <a href="http://t.co/uqdNIlxY1K">akka.io/docs/</a>

Есть книга Effective Akka. Она совсем небольшая, но в ней вы найдете best practices для akka с толковыми примерами <a href="http://t.co/9XTCb2XLH1">shop.oreilly.com/product/063692…</a>

Из блогов по akka рекомендую <a href="http://t.co/NGnrnIG3l9">letitcrash.com</a> и <a href="https://t.co/MFu0aCPatU">typesafe.com/blog</a>
А если хочется паттернов с акторами — <a href="http://t.co/WYwmhYIDu3">letitcrash.com/post/591902669…</a>

Ну и конечно же рекомендую курс Principles of Reactive Programming <a href="https://t.co/JHt2ZqWnAg">coursera.org/course/reactive</a>

И это только первый день :) надеюсь,вы сегодня более продуктивны? А какую фичу вы сегодня запилили на вашем бэкенде? <a href="https://t.co/I98woKGVI9">twitter.com/sbozhko/status…</a>

RT <a href="https://twitter.com/mr_mig_by" title="Alexey Migutsky">@mr_mig_by</a>: <a href="https://twitter.com/Timrael" title="Timur Kozmenko">@Timrael</a> <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> ящитаю  это быстро: за 5 часов можно полностью покрыть весь A2 уровень и посмотреть вблизи на основн…

RT <a href="https://twitter.com/5minphp" title="Пятиминутка PHP">@5minphp</a>: <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> не возникало ли ощущения, что <a href="https://twitter.com/search?q=%23scala">#scala</a> слишком сложна и хочется взять что-то более простое для текущей задачи... …

Чувствую подвох в этом вопросе.

Нет, такого желания не было. Scala тем и хороша: язык эволюционирует вместе с вами. Чем глубже изучаете его, тем интереснее становится.

Не зря же это SCAlable LAnguage.

Да, есть такой сайд-эффект. Code review сильно помогает, если в команде инженеры разного уровня и стиля <a href="https://t.co/UpTx1s4KHR">twitter.com/crashkin/statu…</a>

## Вторник <small>33 твита</small>

Доброе утро, друзья! Ну что, вы отстендапились уже? Как вы, кстати, относитесь к ежедневным скрам-ритуалам?

И про какой аспект бэкнед разработки на Scala вы хотите узнать сегодня?

RT <a href="https://twitter.com/_bugov" title="Georgy Bazhukov">@_bugov</a>: <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> Утренний - пошёл он на ... Вечерний - хороший повод подвести итоги.

RT <a href="https://twitter.com/melnikov_p" title="Злой человек">@melnikov_p</a>: <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> утренние ситдауны объединяют!

RT <a href="https://twitter.com/agoosev" title="Andrew">@agoosev</a>: <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> утром стендап полезен, чтобы понять кто и что будет делать. Важно чтобы стендап не занимал много времени и был …

RT <a href="https://twitter.com/vladimore" title="Waldemar">@vladimore</a>: <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> стараюсь опоздать на работу, чтобы не попасть на это дело

RT <a href="https://twitter.com/kmmbvnr" title="kmmbvnr">@kmmbvnr</a>: <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> клево, но не все умеют спокойно к ним относится. На самом же деле, че такого? Затерли по работе и разбежались!

Попросить у автора кода отсыпать того замечательного порошка, который был использован при написании! <a href="https://t.co/b9C2hJejCk">twitter.com/pdrobushevich/…</a>

Веду твиттер бэкенд разработчика! <a href="https://t.co/FVmrMQAfcv">twitter.com/avevlad/status…</a>

Но обычно помогает только долгое, внимательное, кропотливое изучение исходника: переход по функциям, прогон тестов.

А вы какие еще способы знаете, ежели нужно вникнуть в чужой код, весьма сложный и запутанный?

Отличный ответ! Ритуалы как средство формирования команды. Между прочим, человечество давно пользуется этим методом. <a href="https://t.co/gLY5sPIBqB">twitter.com/chorna_kiwka/s…</a>

Нет на вас сертифицированного скрам-мастера! <a href="https://t.co/cZnZISiIVn">twitter.com/lowl4tency/sta…</a>

1-2 таска за среднестатистический стендап! Мне бы такую продуктивность. <a href="https://t.co/wd68P8ohgW">twitter.com/vladimore/stat…</a>

RT <a href="https://twitter.com/pdrobushevich" title="Pavel Drobushevich">@pdrobushevich</a>: <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> все верно и поэтому хорошо бы, чтобы эту сложность хотя бы язык не превносил и так есть с чем разбираться

Утром отлично поговорили за стендапы и скрам. Спасибо за живой отклик. А теперь поведаю свое мнение касательно этого добра.

Собственно, к стендапам я отношусь положительно. Полезно быть в курсе того, что делает команда. Но agile-команда не должна быть большой.

Есть даже такое понятие: "two-pizza team". В бОльшей команде стендап сильно разбухает и становится бесполезным. Скучно слушать нерелевантное

Но я категорически против бездумного следования ритуалам. Хотите стойте, хотите — сидите. Как вам удобно.

Да, есть мнение, что стоя люди будут меньше говорить. Но не в этом же суть. Цель — рассказать, что сделал, что будешь делать, какие блокеры.

*голосом Нерзула*
Нужно больше митингов! <a href="https://t.co/5vI2ihq9Du">twitter.com/a_lithium/stat…</a>

RT <a href="https://twitter.com/pdrobushevich" title="Pavel Drobushevich">@pdrobushevich</a>: <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> ок, у нас вообще их два :) один общий где один человек за всю команду рассказывает коротенько и можно дру…

RT <a href="https://twitter.com/pdrobushevich" title="Pavel Drobushevich">@pdrobushevich</a>: <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> второй внутри команды, с техническим мясом, какие у кого интересные штуки/проблемы/затыки и т.п.

Очень дельный совет. К сожалению, работает только если есть автор. А санитары быстро приезжают за такими авторами. <a href="https://t.co/LT5ATiMv62">twitter.com/listochkin/sta…</a>

Вот, к слову, парное программирование отлично подходит, если нужно ввести нового человека в проект. Это куда быстрее, нежели копаться самому

А что вы можете порекомендовать для ввода нового инженера в проект?

RT <a href="https://twitter.com/vladimore" title="Waldemar">@vladimore</a>: <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> удачи.. - сказал мне мой предшественник и ушел оставив наедине с полугодовалым легаси 😃<a href="https://twitter.com/search?q=%23adventureTime">#adventureTime</a>e

RT <a href="https://twitter.com/ivanenok" title="Maxim S. Ivanov">@ivanenok</a>: <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> кстате, у меня вопрос. а кто в бэкендах юзает XSL+XML и какова мотивация для сего действа?

RT <a href="https://twitter.com/agoosev" title="Andrew">@agoosev</a>: <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> а мы всякие лекции записываем для внутреннего пользования, чтобы по десять раз одно и то же не рассказывать.

RT <a href="https://twitter.com/agoosev" title="Andrew">@agoosev</a>: <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> и предварительный code-review с выделенным наставником. Перед общим code-review.

Рубрика "Знаете ли вы". Знаете ли вы, откуда взялся логотип Scala? А теперь посмотрите на лестницу в EPFL: <a href="http://t.co/u5puPNb7R5">deliveryimages.acm.org/10.1145/260000…</a>

Как Scala-разработчик я должна пиарить Scala, но сейчас сижу и изучаю Go. И вам скажу, что Go весьма неплох, но мне видится чересчур простым

И некоторые моменты в нем вызывают недоумение. Я уже завела себе файлик, который так и называется "wtf golang". Зря не вела такой для Scala.

## Среда <small>22 твита</small>

RT <a href="https://twitter.com/afiskon" title="Eax Melanhovich">@afiskon</a>: Мои впечатления от языка Scala после года работы с ним <a href="http://t.co/ELY931p7Qr">eax.me/scala-one-year/</a> <a href="https://twitter.com/search?q=%23fprog">#fprog</a> <a href="https://twitter.com/search?q=%23scala">#scala</a> <a href="https://twitter.com/search?q=%23java">#java</a>

RT <a href="https://twitter.com/NilzBor" title="Nils">@NilzBor</a>: <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> как долго компилится и собирается средний проект и как можно это ускорить (давай - выкладывай секреты :)

Средний проект (хотя что считать таковым?) собирается у меня на макбуке мавеном за 01:34 минут.

Можно разбивать проект на модули (сервисы) и собирать каждый по необходимости. Также есть инкрементальная сборка, есть еще проме мавена sbt

01:34 минут - это сборка с нуля с прогоном юнит-тестов. Так что не скажу, что собирается все очень медленно.

RT <a href="https://twitter.com/anton_davydov" title="Davy Dovanton">@anton_davydov</a>: <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> мне кажется, что для любого языка можно составить такой файлик. Например, вот для ruby и js :)
https://t.<a href="https://t.co/GUGOToW34E">destroyallsoftware.com/talks/wat</a>

RT <a href="https://twitter.com/adriancolyer" title="Adrian Colyer">@adriancolyer</a>: "Asynchronous Distributed Snapshots for Distributed Dataflows" - Carbone et al. 2015 <a href="http://t.co/QTpfkHseN3">blog.acolyer.org/?p=1052</a> <a href="https://twitter.com/search?q=%23themorningpaper">#themorningpaper</a>

RT <a href="https://twitter.com/SBozhko" title="Svetλana">@SBozhko</a>: Список русскоязычных подкастов на тему информационных технологий <a href="https://t.co/iDnpkgA6gX">github.com/AveVlad/russia…</a> 
<a href="https://twitter.com/search?q=%23DevZen">#DevZen</a> первый в списке :)

Тоже так делаю при разборе нового проекта.   <a href="https://t.co/tnH3aiI60b">twitter.com/borovikov/stat…</a>

Наверняка вы наслышаны про коллекции в Scala. Это и правда очень гибкий инструмент, с которым действительно удобно и приятно работать.

Но настоящие бэкенд разработчики знают, что ничего не дается просто так. А когда речь идет о высоких нагрузках, миллисекунды решают.

Если хотите узнать, чего стоит это удобство в Scala, и вас не испугают байт-код и ассемблер, то этот доклад для вас: <a href="https://t.co/Au0L1J6Ju1">youtube.com/watch?v=M7ptT_…</a>

Здесь должен быть дисклеймер про ваш страх и риск. <a href="https://t.co/KxE51oqrSn">twitter.com/kmmbvnr/status…</a>

Всего год пишу продакшен код на Scala, а меня уже передергивает, когда вижу неоправданные мутабельные переменные в коде на других языках.

RT <a href="https://twitter.com/Borovikov" title="Денис Боровиков">@Borovikov</a>: <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> а зачем? Все эти wtf будут просто первым впечатлением с непривычки

Позвольте не согласиться. Wtf-ки, возникающие при изучении нового языка, библиотеки, инструмента, очень важны.

Они указывают на сомнительные моменты для стороннего наблюдателя с незашоренным взглядом.

По сему я считаю, что такие вещи нужно обязательно фиксировать. Это очень ценный фитбек. Вспомните хотя бы "коридорное тестирование".

RT <a href="https://twitter.com/chubik" title="Valentyn Chub">@chubik</a>: <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> быстрое объяснение почему <a href="https://twitter.com/search?q=%23golang">#golang</a> такой <a href="http://t.co/1L7gtegTqv">learnxinyminutes.com/docs/ru-ru/go-…</a>

Внимание. Вброс. После почти недели с Go у меня в голове крутится только одно слово: "убогонький". Нет в нем мощи Scala. Продолжаю изучение.

Полагаю, внимательный читатель заметил каламбур? УбоGoнький там должно быть.

RT <a href="https://twitter.com/pdrobushevich" title="Pavel Drobushevich">@pdrobushevich</a>: <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> да ему даже до жавки, особенно восьмой долеко

## Четверг <small>13 твитов</small>

RT <a href="https://twitter.com/crashkin" title="crashkin">@crashkin</a>: <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> очень тяжело пересаживаться со scala+akka на java+spring. Ощущение связанных рук

Да это же замечательно! <a href="https://t.co/MwMdvthZIy">twitter.com/xeningem/statu…</a>

Спасибо! Мы стараемся для вас :) <a href="https://t.co/fROgD5vfAL">twitter.com/fliptheweb/sta…</a>

К слову, доклад про внутренности Scala сделал <a href="https://twitter.com/public_void_grv" title="Roman Grebennikov">@public_void_grv</a>. Так что можете ему задавать каверзные вопросы :) <a href="https://t.co/P8cQbnGKbK">twitter.com/public_void_gr…</a>

Да, это тоже весьма интересный доклад про внутренности Scala и jvm <a href="https://t.co/VwJvjVLG2d">twitter.com/ivanenok/statu…</a>

Итак, кому же надо избегать Scala. <a href="https://t.co/yY9NFMA9LW">twitter.com/NilzBor/status…</a>

На мой взгляд, первая причина — это если jvm вам не подходит в принципе.

Вторая—если в команде уровень инженеров сильно разнится. Каждый будет писать в своем стиле, что приведет к совершенно неподдерживаемому коду

Либо же люди будут много и часто спорить, что тоже не есть хорошо.

RT <a href="https://twitter.com/imdefined" title="Denis Fedoseev">@imdefined</a>: <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> а бить граблями по рукам за несоблюдение код-стайла уже не модно?

Здесь даже речь идет не только и не сколько о стиле наименования переменных, отступов и пр. Это скорее об уровне функциональщины в коде.

Если в языке есть множество способов сделать одно и то же, то такая свобода может сыграть против вас.

Мне в свое время книга Spring in Action очень понравилась. Там был хороший пример с web <a href="http://t.co/4zcmywHVnT">manning.com/walls4</a> <a href="https://t.co/EPu57SAH9Y">twitter.com/pl__nk/status/…</a>

## Пятница <small>15 твитов</small>

Как решать сложные задачи в программировании:
1. Попытайтесь понять проблему.
2. Бросьте, начните писать код.
3. Бросьте, вернитесь к шагу 1

В этом репозитории ребята пилят тул для визуализации akka-cluster на D3 <a href="https://t.co/lmlOh5od8P">github.com/dsugden/cluste…</a>

Замечательно! <a href="https://t.co/gUIz41ahH0">twitter.com/ptico/status/6…</a>

RT <a href="https://twitter.com/Haghard" title="Haghard">@Haghard</a>: <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> 
Klang's Conjecture:
If you cannot solve a problem without programming you cannot solve a problem with programm…

А сейчас минутка "А знаете ли вы". В Scala есть интересный класс AnyRef. Он явлется базовым для всех пользовательских классов.

На самом деле это всего лишь алиас для java.lang.Object. Но какова причина существования AnyRef, учитывая, что уже есть java.lang.Object?

Дело в том, что изначально Scala была задизайнена для работы как на Jvm, так и на .NET. Для .NET AnyRef — это алиас для System.Object.

Если вы всегда хотели заниматься Data Science, но не знаете, с чего начать, у меня для вас есть план развития. <a href="http://t.co/j9M1fqEmlB">pic.twitter.com/j9M1fqEmlB</a>

Не мое, но жизненно :)

ПМ сказал: 
"Опять дедлайны 
И куча неотложных дел". 
И отпуск мой он на релизе вертел.

А вы ходили в отпуск этим летом? Я вот нет.

Гоняю тесты, фикшу тесты.
Для пятницы сойдет вполне.
Ищите наш релиз продукта 
На дне.

Ну это такое время, когда можно спокойно пилить свои проекты. <a href="https://t.co/1K4IQkBJVj">twitter.com/ivanenok/statu…</a>

RT <a href="https://twitter.com/public_void_grv" title="Roman Grebennikov">@public_void_grv</a>: <a href="https://twitter.com/ivanenok" title="Maxim S. Ivanov">@ivanenok</a> <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> отпуск это такое мифическое время, когда ты не программируешь несколько дней подряд.

Сегодня вечер пятницы, а значит, пора приниматься за подготовку к выпуску подкаста #55. Создаю интригу: скоро у нас ожидается раздача слонов

А чем вы обычно заниматесь по вечерам пятницы? Неужели пишете код?!

## Суббота <small>5 твитов</small>

RT <a href="https://twitter.com/levwalkin" title="Lev Walkin">@levwalkin</a>: — Какой тупая защита на сайтах, «введите имя своего питомца»...
— У меня на это есть случайно нумерованные жабы.

Да вы сложные вопросы задаете :) <a href="https://t.co/buopKD4Wem">twitter.com/anton_davydov/…</a>

Уже больше года каждая пятница — это подкаст + подготовка к нему. Есть исключения, когда я в разъездах. Но это крайне редко.

RT <a href="https://twitter.com/afiskon" title="Eax Melanhovich">@afiskon</a>: RT за <a href="https://twitter.com/search?q=%23fpconf">#fpconf</a>, <a href="https://twitter.com/search?q=%23opengl">#opengl</a> и <a href="https://twitter.com/search?q=%23vulkan">#vulkan</a>! ::: FPConf и Vulkan с гостем <a href="https://twitter.com/zeuxcg" title="Arseny Kapoulkine">@zeuxcg</a> — Episode 0055 <a href="http://t.co/aPDEUYhOCT">devzen.ru/episode-0055/</a> via <a href="https://twitter.com/gliush" title="Ivan Glushkov">@gliush</a> <a href="https://twitter.com/search?q=%23devzen">#devzen</a>

RT <a href="https://twitter.com/Bugagazavr" title="Bugagazavr">@Bugagazavr</a>: <a href="https://twitter.com/afiskon" title="Eax Melanhovich">@afiskon</a> <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> <a href="https://twitter.com/zeuxcg" title="Arseny Kapoulkine">@zeuxcg</a> <a href="https://twitter.com/gliush" title="Ivan Glushkov">@gliush</a> отличный выпуск

## Воскресенье <small>17 твитов</small>

Неделю изучаю Go и пишу на нем небольшой проект для себя. Нужно признать, что у меня предвзятое мнение. Но тем не менее отмечу следующее:

Когда пишешь код на Scala, чувствуешь себя умным, а когда пишешь на Go, ощущаешь себя кодером.

Это лишь мое впечатление. Возможно, ошибочное. Но как-то не заходит этот язык для меня пока что. Очень жаль, конечно.

RT <a href="https://twitter.com/remm_roman" title="Remm">@remm_roman</a>: Идея переходящего акка <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> интересная.

RT <a href="https://twitter.com/extempore2" title="Paul Phillips">@extempore2</a>: go is a terrible, terrible language, yet still a major productivity boost. Amdahl's law in another context.

RT <a href="https://twitter.com/extempore2" title="Paul Phillips">@extempore2</a>: reduce: what you will do with your expectations after you start with Go

RT <a href="https://twitter.com/extempore2" title="Paul Phillips">@extempore2</a>: Rust and Scala drown you in complexity. Go drowns you in simplicity.

RT <a href="https://twitter.com/extempore2" title="Paul Phillips">@extempore2</a>: You often see languages which are fighting the last war. Go is fighting the War of 1812.

Боль и унижение? <a href="https://t.co/MGtG1fjWId">twitter.com/lopinopulos/st…</a>

RT <a href="https://twitter.com/_toydestroyer" title="Sergey Toy">@_toydestroyer</a>: <a href="https://twitter.com/backendsecret" title="Разработчик Бэкенда">@backendsecret</a> чувствуют, что через неделю в школу (простите).

Давайте еще откровений PHP-разработчиков! <a href="https://t.co/GkKSNGWKyK">twitter.com/lopinopulos/st…</a>

Ну что, ребята, через час мне перекроют доступ к этому аккаунту. У вас осталось мало времени, чтобы успеть задать мне свои вопросы :)

Согласна. Изначально хотела стать ученым-геологом, а потом математиком. <a href="https://t.co/4W5pV5JbB5">twitter.com/rubyunderhood/…</a>

Превосходно! <a href="https://t.co/gStPeGL3qq">twitter.com/webholt/status…</a>

Перегруженный, имхо. Я вообще за либы больше. Если нужно быстро сделать что-то типичное, то фреймворк вполне ок.  <a href="https://t.co/OqWQjQaVRy">twitter.com/NilzBor/status…</a>

Только для небольшого проекта, который вычитывает из зукипера оффсеты очередей кафки и выводит это в виде таблицы. <a href="https://t.co/7onbfyTA4l">twitter.com/NilzBor/status…</a>

За сим прощаюсь. С вами на этой неделе была <a href="https://twitter.com/SBozhko" title="Svetλana">@SBozhko</a>. Это был замечательный опыт. Спасибо вам за это!