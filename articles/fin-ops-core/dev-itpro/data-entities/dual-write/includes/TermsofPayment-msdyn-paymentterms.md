## <a name="terms-of-payment-to-msdyn_paymentterms"></a>Условия оплаты -> msdyn_paymentterms

Этот шаблон синхронизирует данные между приложениями Finance and Operations и Common Data Service.

Поле Finance and Operations | Тип сопоставления | Другое поле Dynamics 365 | Значение по умолчанию
---|---|---|---
DESCRIPTION | = | msdyn_description | 
NAME | = | msdyn_name | 
NUMBEROFMONTHS | = | msdyn_numberofmonth | 
CUTOFFDAYOFMONTH | = | msdyn_cutoffdayofmonth | 
ISCASHPAYMENT | >< | msdyn_iscashpayment | 
NUMBEROFDAYS | = | msdyn_days | 
ISCERTIFIEDCOMPANYCHECK | >< | msdyn_iscertifiedcompanycheck | 
ISDEFAULTPAYMENTTERM | >< | msdyn_isdefaultpaymentterm | 
CREDITCARDPAYMENTTYPE | >< | msdyn_creditcardpaymenttype | 
CREDITCARDCREDITCHECKTYPE | >< | msdyn_creditcardcreditchecktype | 
PAYMENTDAYNAME | = | msdyn_paymentdayname.msdyn_name | 
PAYMENTMETHODTYPE | >< | msdyn_paymentmethodtype | 
PAYMENTSCHEDULENAME | = | msdyn_paymentschedulename.msdyn_name | 
