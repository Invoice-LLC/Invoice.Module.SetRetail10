## Инструкция по установке плагина Invoice для SetRetail10
### Настройка на сервере 
1. Скачайте [плагин](https://github.com/Invoice-LLC/Invoice.Module.SetRetail10/releases/download/1.5/invoicePluginSetRetail.jar)
2. Скопируйте файл плагина на сервер
  * **ОС Linux**: /var/lib/jboss/plugins/Invoice.Modules.SetRetail10-1.5.jar
  * **ОС Windows**: …\SetRetail10\plugins\Invoice.Modules.SetRetail10-1.5.jar
*Если папка plugins отсутствует, тогда создайте её вручную. 
Для топологии Centrum-Retail-касса плагин необходимо копировать на все узлы топологии - на Centrum, на все Ритейлы, и на все кассы*
3. Настройте плагин
  1. Нажмите Зайдите в Интеграции->Внешние процессинги<br>
  ![image](https://i.imgur.com/5N87Emz.png)
  2. Нажмите на добавление процессинга<br>
  ![image](https://i.imgur.com/JlxzE1O.png)
  3. Выберите Платёжные системы->Invoice и сохраните<br>
  ![image](https://i.imgur.com/Fjj3eDd.png)
  4. Настройте плагин. Введите Login (id компании) и api ключ (можно посмотреть в [личном кабинете Invoice](https://lk.invoice.su/settings?tab=general))<br>
  ![image](https://i.imgur.com/NKOx33J.png)
  5. Добавьте тип оплаты для ваших шаблонов касс. Кассовый модуль -> Шаблоны касс -> Редактировать -> Процесс торговли -> Типы оплаты. Добавьте тип оплаты Invoice (QR). Так же добавьте тип оплаты для юр.лиц и сохраните<br>
  
### Касса 
1. Скопируйте плагин на кассу:
\storage\crystal-cash\plugins\Invoice.Modules.SetRetail10-1.5.jar
2. Перезагрузите кассовый модуль.
3. Зайдите в [личный кабинет Invoice](https://lk.invoice.su/) для настройки нового терминала. 
  1. Настройте новый терминал в [настройках](https://lk.invoice.su/terminals)<br>
  ![Imgur](https://i.imgur.com/9hjr6l5.png)
  ![Imgur](https://i.imgur.com/9vCOqYJ.png) 
  2. Скачайте и распечатайте QR-код, нажав на иконку скачать. <br>
  ![Imgur](https://i.imgur.com/1ZPntdG.png)<br>
*Дальше необходимо прикрепить QR-код к кассе. По этому QR-коду ваши клиенты будут производить оплату.*
*Для каждой кассы будет создаваться свой, уникальный, терминал после первого запуска плагина на кассе.*
