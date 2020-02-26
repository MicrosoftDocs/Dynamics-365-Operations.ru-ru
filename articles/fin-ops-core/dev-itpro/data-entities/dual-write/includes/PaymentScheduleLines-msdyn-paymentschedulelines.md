## <a name="payment-schedule-lines-to-msdyn_paymentschedulelines"></a>Строки графика оплаты -> msdyn_paymentschedulelines

Этот шаблон синхронизирует данные между приложениями Finance and Operations и Common Data Service.

Поле Finance and Operations | Тип сопоставления | Другое поле Dynamics 365 | Значение по умолчанию
---|---|---|---
PAYMENTSCHEDULENAME | = | msdyn_paymentschedule.msdyn_name | 
LINENUMBER | = | msdyn_linenumber | 
PERIODSAFTERDUEDATE | = | msdyn_periodsafterduedate | 
PERCENTORAMOUNT | >< | msdyn_percentoramount | 
PERCENTORAMOUNTVALUE | = | msdyn_percentoramountvalue | 
