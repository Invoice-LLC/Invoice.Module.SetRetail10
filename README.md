## Инструкция по установке плагина Invoice для SetRetail10
### Сервер 
1. Скачайте [плагин](https://github.com/Invoice-LLC/Invoice.Modules.SetRetail10/releases/download/1.4/Invoice.Modules.SetRetail10-1.4.jar)
2. Скопируйте файл плагина на сервер
  * **ОС Linux**: /var/lib/jboss/plugins/Invoice.Modules.SetRetail10-1.4.jar
  * **ОС Windows**: …\SetRetail10\plugins\Invoice.Modules.SetRetail10-1.4.jar
*Если папка plugins отсутствует, тогда создайте её вручную. 
Для топологии Centrum-Retail-касса плагин необходимо копировать на все узлы топологии - на Centrum, на все Ритейлы, и на все кассы*
3. Настройте плагин
  1. Нажмите Управление продажами на главной странице<br>
  ![Imgur](https://i.imgur.com/RDgOdLl.png)
  2. Нажмите Внешние системы<br>
  ![Imgur](https://i.imgur.com/HcvWfJD.png)
  3. Откройте вкладку Внешние процессинги<br>
  ![Imgur](https://i.imgur.com/1NJ9XUJ.png)
  4. Нажмите на Добавить оператора, кнопка снизу<br>
  ![Imgur](https://i.imgur.com/d9ky6iW.png)
  5. Выберите Платежные системы -> Invoice. Нажмите Зарегистрировать нового оператора<br>
  ![Imgur](https://i.imgur.com/303art9.png)
  6. Нажмите двойным щелчком по строчке Invoice, для открытия настроек<br>
  ![Imgur](https://i.imgur.com/ZBdnqlT.png)
  7. Введите Login(Номер телефона/Email для входа в личный кабинет) и API-ключ (в настройках личного кабинета) 
    * Номер телефона вводить в формате 79991234567.
    * Будьте внимательны к регистру, не оставляйте лишних пробелов.<br>
    ![Imgur](https://i.imgur.com/UXLym6X.png)
  8. Шаблоны касс-> Выберите ваш шаблон кассы, на которой будет доступна оплата через Invoice.<br>
  ![Imgur](https://i.imgur.com/xG5sPIz.png)
  9. Настройте, если требуется, тип оплаты для функциональных клавиш клавиатуры, привязав тип оплаты Invoice (QR).<br>
  ![Imgur](https://i.imgur.com/hJg5cFd.png)
  
### Касса 
1. Скопируйте плагин на кассу:
\storage\crystal-cash\plugins\Invoice.Modules.SetRetail10-1.4.jar
2. Перезагрузите кассовый модуль.
3. Зайдите в [личный кабинет Invoice](https://lk.invoice.su/) для настройки нового терминала. 
  1. Настройте новый терминал в [настройках](https://lk.invoice.su/terminals)<br>
  ![Imgur](https://i.imgur.com/9hjr6l5.png)
  ![Imgur](https://i.imgur.com/9vCOqYJ.png) 
  2. Скачайте и распечатайте QR-код, нажав на иконку скачать. <br>
  ![Imgur](https://i.imgur.com/1ZPntdG.png)<br>
*Дальше необходимо прикрепить QR-код к кассе. По этому QR-коду ваши клиенты будут производить оплату.*
*Для каждой кассы будет создаваться свой, уникальный, терминал после первого запуска плагина на кассе.*
