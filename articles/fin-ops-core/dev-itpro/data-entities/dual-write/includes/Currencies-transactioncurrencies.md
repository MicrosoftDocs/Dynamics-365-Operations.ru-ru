## <a name="currencies-to-transactioncurrencies"></a>Валюты -> transactioncurrencies

Этот шаблон синхронизирует данные между приложениями Finance and Operations и Common Data Service.

Фильтр источника: ((CURRENCYCODE != "999"))

Поле Finance and Operations | Тип сопоставления | Другое поле Dynamics 365 | Значение по умолчанию
---|---|---|---
CURRENCYCODE | = | isocurrencycode | 
NAME | = | currencyname | 
SYMBOL | = | currencysymbol | 
Нет | >> | exchangerate | 1
