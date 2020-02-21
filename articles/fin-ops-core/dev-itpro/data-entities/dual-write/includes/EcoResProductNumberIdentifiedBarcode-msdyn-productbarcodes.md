## <a name="product-number-identified-barcode-to-msdyn_productbarcodes"></a>Штрих-код, определяющий номер продукта -> msdyn_productbarcodes

Этот шаблон синхронизирует данные между приложениями Finance and Operations и Common Data Service.

Поле Finance and Operations | Тип сопоставления | Другое поле Dynamics 365 | Значение по умолчанию
---|---|---|---
PRODUCTNUMBER | > | msdyn_productnumberid.msdyn_productnumber | 
BARCODE | > | msdyn_name | 
BARCODE | > | msdyn_barcode | 
PRODUCTQUANTITY | > | msdyn_productquantity | 
PRODUCTDESCRIPTION | > | msdyn_productdescription | 
BARCODESETUPID | > | msdyn_barcodesetupid | 
PRODUCTQUANTITYUNITSYMBOL | > | msdyn_unitofmeasureid.msdyn_symbol | 
ISDEFAULTSCANNEDBARCODE | >> | msdyn_isdefaultscannedbarcode | 
ISDEFAULTPRINTEDBARCODE | >> | msdyn_isdefaultprintedbarcode | 
ISDEFAULTDISPLAYEDBARCODE | >> | msdyn_isdefaultdisplayedbarcode | 
