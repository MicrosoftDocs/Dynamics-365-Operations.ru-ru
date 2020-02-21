## <a name="loyalty-card-to-msdyn_loyaltycards"></a>Карта постоянного клиента -> msdyn_loyaltycards

Этот шаблон синхронизирует данные между приложениями Finance and Operations и Common Data Service.

Поле Finance and Operations | Тип сопоставления | Другое поле Dynamics 365 | Значение по умолчанию
---|---|---|---
CARDNUMBER | = | msdyn_cardnumber | 
CARDTENDERTYPE | >< | msdyn_cardtendertype | 
PARTYNUMBER | = | msdyn_partynumber | 
REPLACEMENTCARDNUMBER | > | msdyn_replacementcardnumber | 
OMOPERATINGUNITNUMBER | = | msdyn_operatingunitnumber | 
LOYALTYENROLLMENTDATE | = | msdyn_enrollmentdate | 
