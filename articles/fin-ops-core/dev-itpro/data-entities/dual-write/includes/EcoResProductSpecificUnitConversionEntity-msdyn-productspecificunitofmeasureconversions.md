## <a name="product-specific-unit-conversions-to-msdyn_productspecificunitofmeasureconversions"></a>Пересчеты единиц измерения конкретных продуктов -> msdyn_productspecificunitofmeasureconversions

Этот шаблон синхронизирует данные между приложениями Finance and Operations и Common Data Service.

Поле Finance and Operations | Тип сопоставления | Другое поле Dynamics 365 | Значение по умолчанию
---|---|---|---
DENOMINATOR | = | msdyn_denominator | 
NUMERATOR | = | msdyn_numerator | 
FACTOR | = | msdyn_factor | 
FROMUNITSYMBOL | = | msdyn_fromunit.msdyn_symbol | 
TOUNITSYMBOL | = | msdyn_tounit.msdyn_symbol | 
PRODUCTNUMBER | = | msdyn_globalproduct.msdyn_productnumber | 
INNEROFFSET | = | msdyn_inneroffset | 
OUTEROFFSET | = | msdyn_outeroffset | 
ROUNDING | >< | msdyn_rounding | 
