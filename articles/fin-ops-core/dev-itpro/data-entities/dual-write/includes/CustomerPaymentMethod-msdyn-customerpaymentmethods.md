## <a name="customer-payment-method-to-msdyn_customerpaymentmethods"></a>Способ оплаты клиента -> msdyn_customerpaymentmethods

Этот шаблон синхронизирует данные между приложениями Finance and Operations и Common Data Service.

Поле Finance and Operations | Тип сопоставления | Другое поле Dynamics 365 | Значение по умолчанию
---|---|---|---
NAME | = | msdyn_name | 
ACCOUNTTYPE | >< | msdyn_accounttype | 
DISCOUNTGRACEPERIODDAYS | = | msdyn_discountgraceperioddays | 
BRIDGINGPOSTINGENABLED | >< | msdyn_bridgingpostingenabled | 
ISSEPA | >< | msdyn_issepa | 
LASTFILENUMBER | = | msdyn_lastfilenumber | 
LASTFILENUMBERTODAY | = | msdyn_lastfilenumbertoday | 
DESCRIPTION | = | msdyn_description | 
PAYMENTTYPE | >< | msdyn_paymenttype | 
CREATEANDDRAWBILLOFEXCHANGEDURINGINVOICEPOSTING | >< | msdyn_invoiceupdate | 
PAYMENTSTATUS | >< | msdyn_paymentstatus | 
SUMBYPERIOD | >< | msdyn_sumbyperiod | 
ENABLEPOSTDATEDCHECKCLEARINGPOSTING | >< | msdyn_enablepostdatescheckclearingposting | 
BILLOFEXCHANGEDRAFTTYPE | >< | msdyn_billofexchangedrafttype | 
DIRECTDEBIT | >< | msdyn_directdebit | 
