Домашнее задание к занятию 10.5 «Балансировка нагрузки. HAProxy/Nginx» Полянинов Максим 

Инструкция по выполнению домашнего задания

Сделайте fork репозитория c Шаблоном решения к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/gitlab-hw или https://github.com/имя-вашего-репозитория/8-03-hw).

Выполните клонирование данного репозитория к себе на ПК с помощью команды git clone.

Выполните домашнее задание и заполните у себя локально этот файл README.md:
впишите вверху название занятия и вашу фамилию и имя
в каждом задании добавьте решение в требуемом виде (текст/код/скриншоты/ссылка)
для корректного добавления скриншотов воспользуйтесь инструкцией "Как вставить скриншот в шаблон с решением
при оформлении используйте возможности языка разметки md (коротко об этом можно посмотреть в инструкции по MarkDown)

После завершения работы над домашним заданием сделайте коммит (git commit -m "comment") и отправьте его на Github (git push origin);

Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.

Любые вопросы по выполнению заданий спрашивайте в чате учебной группы и/или в разделе “Вопросы по заданию” в личном кабинете.

Желаем успехов в выполнении домашнего задания!

Задание 1

Что такое балансировка нагрузки и зачем она нужна?

Приведите ответ в свободной форме.

Ответ:

Термин балансировка нагрузки относится к распределению рабочих нагрузок между несколькими вычислительными ресурсами. Балансировка нагрузки нацелена на оптимизацию использования ресурсов, увеличение пропускной способности, уменьшение времени отклика и предотвращение перегрузки одного ресурса. Кроме того, она может повысить доступность за счет совместного использования рабочей нагрузки в пределах избыточных вычислительных ресурсов.


Задание 2

Чем отличаются алгоритмы балансировки Round Robin и Weighted Round Robin? В каких случаях каждый из них лучше применять?

Приведите ответ в свободной форме.

Ответ:

Round Robin
Самый простой алгоритм. Балансировщик держит обычную очередь из серверов. Первый сервер в очереди обрабатывает запрос и помещается в конец очереди и так по кругу. Таким образом сервера равномерно нагружены.

Алгоритм отлично походит когда сервера в пуле имеют одинаковую мощность и время обработки запросов.


Weighted Round Robin
Тот же round robin, но имеет дополнительное свойство — вес сервера. С его помощью мы можем указать балансировщику сколько трафика отправлять на тот или иной сервер. Так сервера помощнее будут иметь больший вес и соответственно обрабатывать больше запросов чем другие сервера.



Задание 3

Установите и запустите Haproxy.

Приведите скриншот systemctl status haproxy, где будет видно, что Haproxy запущен.



Ответ:

![haproxy](https://user-images.githubusercontent.com/75700701/230154187-abe19fd2-88e6-447b-9ca4-46bcf5349b03.png)




Задание 4
Установите и запустите Nginx.

Приведите скриншот systemctl status nginx, где будет видно, что Nginx запущен.


Ответ:

![nginx](https://user-images.githubusercontent.com/75700701/230153628-2c13f26c-a494-494b-876b-9b0924d66dce.png)


