## <a name="fiscal-calendar-year-integration-entity-to-msdyn_fiscalcalendaryears"></a>Объект интеграции года финансового календаря -> msdyn_fiscalcalendaryears

Этот шаблон синхронизирует данные между приложениями Finance and Operations и Common Data Service.

Поле Finance and Operations | Тип сопоставления | Другое поле Dynamics 365 | Значение по умолчанию
---|---|---|---
FISCALCALENDAR_CALENDARID | = | msdyn_fiscalcalendarname | 
NAME | = | msdyn_name | 
STARTDATE | = | msdyn_startdate | 
ENDDATE | = | msdyn_enddate | 
FISCALCALENDAR_CALENDARID | = | msdyn_calendar.msdyn_calendar | 
