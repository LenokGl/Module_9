# Домашнее задание 08

## Кибербезопасность в архитектуре

Проработка  возможных рисков с т.з. кибербезопасности

## Риски
* Отказ в обслуживании
* Разглашение информации (утечка)
* Заражение устройства вредоносным ПО
* Повышение привилегий


# Способы уменьшения рисков
Первое что должно быть реализовано для всех видов угроз - это наличие навыков реагирования на инциденты безопасности и наличие инструментария контроля и анализа системы (SIEM )

Второе - не держать мониторинг в секрете, т.е. сотрудники должны знать что и как отслеживается. 

Третье - реализация концепции Zero Trust при построении системы

## Риск отказа в обслуживании
 В начале надо убедиться что это реально DDoS атака , а не  нехватка ресурсов системы. Т.е. при проектировании приложения надо попытаться оценить реальную нагрузку на приложение. Провести нагрузочное тестирование. Оптимизировать производительность. Оценить перспективы масштабирования.
 ### Для предотвращения атаки на приложение необходимо
 * выявить и проанализировать ресурсоемкие запросы ( например когда идет full scan по всей таблице)
 * настроить мониторинг показателей работы приложения
 * по возможности использовать кэширование
 * установить лимиты на выполнение операций
 * требовать аутентификацию для операций с большой нагрузкой на систему
 * использовать капчи  и т.п. для провверки что обращение идет не от бота
 * блокировать IP
 ### Для предотвращения атаки на сеть необходимо 
 * своевременно обновлять ПО
 * использовать брандмауэры / Firewalls
 * Использовать системы анализа сетевого траффика
 
 
 ## Риск разглашения информации (утечка)
 * создание внутренних политик компании. Подписание документов о неразглашении и нераспространении информации
 * необходимо правильно сконфигурировать вебприложения,веб-сервер и сервер базы данных. Не оставлять  в конфигурации параметры по умолчанию и пароли производителя.
 * использование DLP систем
 * необходимо использовать анализ кода приложений на предмет наличия в них учетных данных для доступа к системе 
 * необходимо использовать защищенный репозиторий для размещения исходных кодов приложений
 * данные не должны храниться в открытом виде, необходимо использовать шифрование
 * везде где это возможно данные должны быть обезличены
 * данные должны быть сегментированы
 * необходимо настроить политики разграничение доступа к данным
 * использование  двухфакторной аутентификации 
 * настроить фильтрацию расширения загружаемых файлов по белому списку(исключить возможность загрузки исполняемых файлов) 
 * настроить политику разграничения доступа к каталогам, где хранятся исполняемые файлы
 * запрет на использование съемных носителей
 
 ## Риск заражения устройства вредоносным ПО
 * обучение персонала
 * номативно-методологическое обеспечение
 * установка и обновление программных и программно-технических средств защиты ( IDS/IPS, SOAR  т.д)
 * установка и обновление антивирусного ПО
 * использование систем защиты разных вендоров
 * использование межсетевых экранов
 * использование Sandbox для проверки загружаемого ПО
 * резервное копирование 
 * контроль подключения внешних устройств
 * безопасные административные интерфейсы
 * применение парольной политики
 * контроль блокировки неиспользуемых учетных записей, а также использования технологических учетных записей
 
 ## Риск повышения привилегий
 * использование Sandbox
 * использование принципа наименьших привилегий
 * анализ каждого привилегированного пользователя или учетной записи
 * минимизация количества и объема привилегированных учетных записей, мониторинг и ведение журнала их деятельности (UEBA)
 * запретить администраторам предоставлять общий доступ к учетным записям и учетным данным
 
 
 ## Краткое резюме
 
 Люди явяются наиболее уязвимой частью системы. Причиной неудачного запуска одной из ракет со спутниками ГЛОНАСС было то что один из датчиков не сработал. Когда попытались докопаться до исполнителей то оказалось что их зарплата примерно как у кассира в Пятерочке.
 
 