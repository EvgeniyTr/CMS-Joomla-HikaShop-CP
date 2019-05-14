# CloudPayments модуль для Joomla - Hikashop
Модуль позволит с легкостью добавить на ваш сайт оплату банковскими картами через платежный сервис CloudPayments. 
Для корректной работы модуля необходима регистрация в сервисе.

Порядок регистрации описан в [документации CloudPayments](https://cloudpayments.ru/Docs/Connect)

### Совместимость:
- Hikashop >= 3.4.0
- Joomla >= 3.8.2


Модуль тестировался на Hikashop = 3.4.0 (Joomla = 3.8.2)

### Возможности:
- Одностадийная схема оплаты;
- Двухстадийная схема оплаты;
- Выбор дизайна виджета;
- Поддержка онлайн-касс (ФЗ-54);
- Отправка чеков по email;
- Отправка чеков по SMS;



### Установка через панель управления
В панели адмниистратора зайти в раздел "Расширения/Менеджер расширений/Установка"
![0](pics/0.png)

После чего загрузите zip архив
 Зайдите в управление плагинами. Убедитесь, что плагин включен.
![0](pics/9.png)

### Настройка плагина
- Перейдите в настройки Hikashop  
![0](pics/1.png)
- Далее необходимо выбрать способы оплаты   
![0](pics/2.png)
- Нажать кнопку "Создать"  
![0](pics/3.png)
- Выбрать  платежный плагин  
![0](pics/4.png)
- В качестве имени новой платежной системы указать: "CloudPayments" - **это обязательный пункт!!!**  
![0](pics/5.png)
- Также выбрать "Опубликовать" - "да"
- Далее ввести "Public ID" - из личного кабинета мерчанта CloudPaymentsloudpayments и пароль API, указываем нужные статусы для реагирования плагина на изменения заказа. Для двухстадийки также надо добавить новый статус "авторизации".

После настройки плагина - сохраните изменения и перейдите к настройки вебхуков в ЛК мерчанта Cloudpayments
Все подсказки по настройки есть в шапке плагина. 

### Настройка вебхуков
Перейдите в ЛК мерчанта cloudpayments. Сайты -> Добавить сайт
![0](pics/6.png)
Далее в списке сайтов выбрать  сайт и зайти в настройки
![0](pics/7.png)
Далее активируйте нужный пункт и добавьте адрес вебхука
![0](pics/8.png)
Список нужных вебхуков:

Настройки Сheck уведомлений: http://ваш_домен/index.php?option=com_hikashop&ctrl=checkout&task=notify&if_payment=cloudpayments&tmpl=component&lang=ru&action=check  
Настройки Pay уведомлений: http://ваш_домен/index.php?option=com_hikashop&ctrl=checkout&task=notify&if_payment=cloudpayments&tmpl=component&lang=ru&action=pay  
Настройки Fail уведомлений: http://ваш_домен/index.php?option=com_hikashop&ctrl=checkout&task=notify&if_payment=cloudpayments&tmpl=component&lang=ru&action=fail  
Настройки Cancel уведомлений: http://ваш_домен/index.php?option=com_hikashop&ctrl=checkout&task=notify&if_payment=cloudpayments&tmpl=component&lang=ru&action=cancel  
Настройки Confirm уведомлений: http://ваш_домен/index.php?option=com_hikashop&ctrl=checkout&task=notify&if_payment=cloudpayments&tmpl=component&lang=ru&action=confirm  
Настройки Refund уведомлений: http://ваш_домен/index.php?option=com_hikashop&ctrl=checkout&task=notify&if_payment=cloudpayments&tmpl=component&lang=ru&action=refund  
 где **ваш_домен** нужно заменить на домен вашего сайта.








