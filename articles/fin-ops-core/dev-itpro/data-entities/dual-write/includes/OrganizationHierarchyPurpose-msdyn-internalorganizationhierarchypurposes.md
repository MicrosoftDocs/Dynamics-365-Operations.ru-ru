## <a name="organization-hierarchy-purposes-to-msdyn_internalorganizationhierarchypurposes"></a>Цели организационной иерархии -> msdyn_internalorganizationhierarchypurposes

Этот шаблон синхронизирует данные между приложениями Finance and Operations и Common Data Service.

Поле Finance and Operations | Тип сопоставления | Другое поле Dynamics 365 | Значение по умолчанию
---|---|---|---
HIERARCHYTYPE | > | msdyn_hierarchypurposetypename | 
HIERARCHYTYPE | > | msdyn_hierarchytype.msdyn_name | 
HIERARCHYPURPOSE | >> | msdyn_hierarchypurpose | 
IMMUTABLE | >> | msdyn_immutable | 
SETASDEFAULT | >> | msdyn_setasdefault | 
