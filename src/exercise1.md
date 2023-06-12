## Алгоритмы балансировки нагрузки


#### Балансировка нагрузки:

***Балансировка потребления*** — это метод быстрого распределения трафика по пулу ресурсов, поддерживающих приложение. Современные приложения должны использовать несколько пользователей одновременно, а также быстро и надежно использовать правильный текст, видео, изображения и другие данные. Для обработки значительного объема трафика в большинстве приложений используется множество серверов ресурсов с дублированием данных между ними.

***Баланс нагрузки*** — это устройство, которое находится между пользователями и группами серверов и действует как невидимый посредник, повсеместное использование всех серверов ресурсов.

***Аппаратный балансировщик нагрузки*** — это аппаратное устройство, которое может обеспечить безопасность и перенаправить гигабайты трафика на сотни различных серверов.
***Программные балансировщики нагрузок*** — это приложения, выполняющие все функции балансировки нагрузок. Вы можете установить их на старшего или получить доступ к ним как к полностью управляемому стороннему сервису.

***Алгоритм балансировки нагрузки*** – это набор правил, которым следует балансировщик нагрузки для определения наилучшего сервера для каждого из различных клиентских запросов. Алгоритмы балансировки нагрузки делятся на две основные категории.

***Round Robin*** - 
 алгоритм кругового обслуживания, представляет собой перебор по круговому циклу: первый запрос передаётся одному серверу, затем следующий запрос передаётся другому и так до достижения последнего сервера, а затем всё начинается сначала.
 В числе несомненных плюсов этого алгоритма следует назвать, во-первых, независимость от протокола высокого уровня. Для работы по алгоритму Round Robin используется любой протокол, в котором обращение к серверу идёт по имени.
Балансировка на основе алгоритма Round Robin никак не зависит от нагрузки на сервер: кэширующие DNS-серверы помогут справиться с любым наплывом клиентов.

Использование алгоритма Round Robin не требует связи между серверами, поэтому он может использоваться как для локальной, так и для глобальной балансировки,.
Наконец, решения на базе алгоритма Round Robin отличаются низкой стоимостью: чтобы они начали работать, достаточно просто добавить несколько записей в DNS.

Алгоритм Round Robin имеет и целый ряд существенных **недостатков** . Чтобы распределение нагрузки по этому алгоритму отвечало упомянутым выше критериями справедливости и эффективности, нужно, чтобы у каждого сервера был в наличии одинаковый набор ресурсов. При выполнении всех операций также должно быть задействовано одинаковое количество ресурсов. В реальной практике эти условия в большинстве случаев оказываются невыполнимыми.

Также при балансировке по алгоритму Round Robin совершенно не учитывается загруженность того или иного сервера в составе кластера. Представим себе следующую гипотетическую ситуацию: один из узлов загружен на 100%, в то время как другие — всего на 10 — 15%. Алгоритм Round Robin возможности возникновения такой ситуации не учитывает в принципе, поэтому перегруженный узел все равно будет получать запросы. Ни о какой справедливости, эффективности и предсказуемости в таком случае не может быть и речи.

В силу описанных выше обстоятельств сфера применения алгоритма Round Robin весьма ограничена.

***Weighted Round Robin***
Это — усовершенствованная версия алгоритма Round Robin. Суть усовершенствований заключается в следующем: каждому серверу присваивается весовой коэффициент в соответствии с его производительностью и мощностью. Это помогает распределять нагрузку более гибко: серверы с большим весом обрабатывают больше запросов. Однако всех проблем с отказоустойчивостью это отнюдь не решает. Более эффективную балансировку обеспечивают другие методы, в которых при планировании и распределении нагрузки учитывается большее количество параметров.

***Least Connections***
Он учитывает количество подключений, поддерживаемых серверами в текущий момент времени. Каждый следующий вопрос передаётся серверу с наименьшим количеством активных подключений.
Существует усовершенствованный вариант этого алгоритма, предназначенный в первую очередь для использования в кластерах, состоящих из серверов с разными техническими характеристиками и разной производительностью. Он называется Weighted Least Connections и учитывает при распределении нагрузки не только количество активных подключений, но и весовой коэффициент серверов.

В числе других усовершенствованных вариантов алгоритма Least Connections следует прежде всего выделить Locality-Based Least Connection Scheduling и Locality-Based Least Connection Scheduling with Replication Scheduling.

Первый метод был создан специально для кэширующих прокси-серверов. Его суть заключается в следующем: наибольшее количество запросов передаётся серверам с наименьшим количеством активных подключений. За каждым из клиентских серверов закрепляется группа клиентских IP. Запросы с этих IP направляются на «родной» сервер, если он не загружен полностью. В противном случае запрос будет перенаправлен на другой сервер (он должен быть загружен менее чем наполовину).

В алгоритме Locality-Based Least Connection Scheduling with Replication Scheduling каждый IP-адрес или группа IP-адресов закрепляется не за отдельным сервером, а за целой группой серверов. Запрос передаётся наименее загруженному серверу из группы. Если же все серверы из «родной» группы перегружены, то будет зарезервирован новый сервер. Этот новый сервер будет добавлен к группе, обслуживающей IP, с которого был отправлен запрос. В свою очередь наиболее загруженный сервер из этой группы будет удалён — это позволяет избежать избыточной репликации.


***Destination Hash Scheduling и Source Hash Scheduling***

Алгоритм Destination Hash Scheduling был создан для работы с кластером кэширующих прокси-серверов, но он часто используется и в других случаях. В этом алгоритме сервер, обрабатывающий запрос, выбирается из статической таблицы по IP-адресу получателя.

Алгоритм Source Hash Scheduling основывается на тех же самых принципах, что и предыдущий, только сервер, который будет обрабатывать запрос, выбирается из таблицы по IP-адресу отправителя.


***Sticky Sessions***
Sticky Sessions — алгоритм распределения входящих запросов, при котором соединения передаются на один и тот же сервер группы. Он используется, например, в веб-сервере Nginx. Сессии пользователя могут быть закреплены за конкретным сервером с помощью метода IP hash. С помощью этого метода запросы распределяются по серверам на основе IP-aдреса клиента, «метод гарантирует, что запросы одного и того же клиента будет передаваться на один и тот же сервер». Если закреплённый за конкретным адресом сервер недоступен, запрос будет перенаправлен на другой сервер.
Применение этого метода сопряжено с некоторыми проблемами. Проблемы с привязкой сессий могут возникнуть, если клиент использует динамический IP. В ситуации, когда большое количество запросов проходит через один прокси-сервер, балансировку вряд ли можно назвать эффективной и справедливой. Описанные проблемы, однако, можно решить, используя cookies. В коммерческой версии Nginx имеется специальный модуль sticky, который как раз использует cookies для балансировки. Есть у него и бесплатные аналоги — например, nginx-sticky-module.
Можно использовать метод sticky-sessions и в HAProxy.