## <a name="product-categories-to-msdyn_productcategories"></a>Категории продуктов -> msdyn_productcategories

Этот шаблон синхронизирует данные между приложениями Finance and Operations и Common Data Service.

Поле Finance and Operations | Тип сопоставления | Другое поле Dynamics 365 | Значение по умолчанию
---|---|---|---
PRODUCTCATEGORYHIERARCHYNAME | = | msdyn_hierarchy.msdyn_name | 
ISCATEGORYINHERITINGPARENTPRODUCTATTRIBUTES | >< | msdyn_isinheritingparentproductattributes | 
PROJECTCATEGORYNAME | = | msdyn_projectcategoryname | 
ISTANGIBLEPRODUCT | >< | msdyn_istangibleproduct | 
ISCATEGORYINHERITINGPARENTCATEGORYATTRIBUTES | >< | msdyn_isinheritingparentcategoryattributes | 
CATEGORYCODE | = | msdyn_code | 
CATEGORYDESCRIPTION | = | msdyn_description | 
CATEGORYKEYWORDS | = | msdyn_keywords | 
CATEGORYNAME | = | msdyn_name | 
FRIENDLYCATEGORYNAME | = | msdyn_friendlycategoryname | 
PARENTPRODUCTCATEGORYNAME | = | msdyn_parentproductcategory.msdyn_name | 
PRODUCTCATEGORYHIERARCHYNAME | >> | msdyn_parentproductcategory.msdyn_hierarchy.msdyn_name | 
