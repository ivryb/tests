Необходимо разработать REST API для веб-приложения на PHP с использованием фреймворка Laravel:
* Создание, удаление и редактирование пользователей (users).
    * Имя.
    * Фамилия.
    * E-mail.
* Создание, удаление и редактирование встреч (meetings).
    * Название встречи.
    * Время начала встречи.
    * Время конца встречи.
    * Статус встречи (запланирована/проходит/завершена, read only).
    * Список участников (связанных пользователей). Один и тот же пользователь не может быть активным участником двух встреч, проходящих в одно и то же время.
    * Роли фасилитатор встречи и секретарь встречи.
        * Каждая роль должна быть занята одним из участников встречи.
        * При этом один и тот же участник не может занимать обе роли.
        * Встреча не может быть создана до тех пор, пока обе роли не заняты.
* При создании встречи всем участникам должно отправляться «на почту» электронное письмо с названием и временем встречи. Можно не настраивать почтовый сервер и отправлять письма в log-файл записью формата «время, e-mail, текст сообщения».