## <a name="ledger-to-msdyn_ledgers"></a>Книга учета -> msdyn_ledgers

Этот шаблон синхронизирует данные между приложениями Finance and Operations и Common Data Service.

Поле Finance and Operations | Тип сопоставления | Другое поле Dynamics 365 | Значение по умолчанию
---|---|---|---
LEGALENTITYID | >> | msdyn_company.cdm_companycode | 
DESCRIPTION | >> | msdyn_description | 
ACCOUNTINGCURRENCY | >> | msdyn_accountingcurrency.isocurrencycode | 
ISBUDGETCONTROLENABLED | >> | msdyn_isbudgetcontrolenabled | 
NAME | >> | msdyn_name | 
REPORTINGCURRENCY | >> | msdyn_reportingcurrency.isocurrencycode | 
BUDGETEXCHANGERATETYPE | >> | msdyn_budgetexchangeratetype.msdyn_name | 
CHARTOFACCOUNTS | >> | msdyn_chartofaccounts.msdyn_name | 
EXCHANGERATETYPE | >> | msdyn_exchangeratetype.msdyn_name | 
FISCALCALENDAR | >> | msdyn_fiscalcalendar.msdyn_calendar | 
REPORTINGCURRENCYEXCHANGERATETYPE | >> | msdyn_reportingcurrencyexchangeratetype.msdyn_name | 
