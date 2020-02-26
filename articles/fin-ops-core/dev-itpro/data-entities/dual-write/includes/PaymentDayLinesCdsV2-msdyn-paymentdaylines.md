## <a name="payment-day-lines-cds-v2-to-msdyn_paymentdaylines"></a>Строки платежных дней CDS V2 -> msdyn_paymentdaylines

Этот шаблон синхронизирует данные между приложениями Finance and Operations и Common Data Service.

Поле Finance and Operations | Тип сопоставления | Другое поле Dynamics 365 | Значение по умолчанию
---|---|---|---
NAME | = | msdyn_paymentday.msdyn_name | 
LINENUMBER | = | msdyn_linenumber | 
FREQUENCY | >< | msdyn_frequency | 
DAYOFWEEK | >< | msdyn_dayofweek | 
DAYOFMONTH | = | msdyn_dayofmonth | 
