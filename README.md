# mfc63.watchdog
Программа предназначена для мониторинга предварительной записи на сайте mfc63.ru и дублирования сообщений, если такая имеется, на произвольную электронную почту.

# Установка
1. Скачайте со страницы релиза самый последний архив и распакуйте содержимое в произвольную папку.
2. Отредактируйте mfc63.watchdog.ini по инструкции ниже.
3. Запустите mfc63.watchdog.exe. При первом запуске программа проверит наличие предварительной записи на сайте и, если такая имеется, отправит на почту уведомление.

# Сборка
Для сборки необходим компилятор AutoIt. Никаких сторонних библиотек подгружать не нужно.

# Настройка
Для настройки необходимо отредактировать mfc63.watchdog.ini
[General]
;ID вашей площадки (см пункт RaisID ниже)
RaisID=35


SmtpServer=smtp.mail.ru ;Параметры smtp сервера с которого будут отправляться письма (здесь рабочие для mai.ru)
Port=465

FromName=noreply.2bite ;Имя отправителя
FromAddress=noreply@mail.ru ;Адрес отправителя

;Логин/пароль отправителя
Login=noreply@mail.ru
Password=password

;Куда отправлять отчет
ToAddress=mfc020712@yandex.ru

;Техподдержка
AdminMail=sergey.2bite@gmail.com

[Timers]
;Частота проверок в минутах
Delay=60
;Начало проверки 8:00
DayStart=8
;Конец проверки 18:00
DayEnd=18

# RaisID

# Лицензия
MIT

# Стороннее ПО:
Утилита для отправки почты с использованием SSL
https://github.com/muquit/mailsend

WinHTTP для Autoit
https://github.com/dragana-r/autoit-winhttp
