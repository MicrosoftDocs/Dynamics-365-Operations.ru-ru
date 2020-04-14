---
title: Унифицированный опыт работы с продуктами
description: Эта тема описывает интеграцию данных продуктов между приложениями Finance and Operations и Common Data Service.
author: t-benebo
manager: AnnBe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 7de7af1084b62a7248eeda54df215e56f2541286
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173208"
---
# <a name="unified-product-experience"></a>Унифицированный подход к работе с продуктами

[!include [banner](../../includes/banner.md)]



Если бизнес-экосистема состоит из приложений Dynamics 365, таких как Finance, Supply Chain Management и Sales, бизнес часто использует эти приложения для исходных данных о продуктах. Это обусловлено тем, что эти приложения предоставляют надежную инфраструктуру продуктов, дополненную сложными концепциями ценообразования и точными данными запасов в наличии. Бизнесы, использующие внешнюю систему управления жизненным циклом продукции (PLM) в качестве источников данных продуктов, могут канализировать продукты из приложений Finance and Operations в другие приложения Dynamics 365. Унифицированный опыт работы с продуктом привносит интегрированную модель данных продуктов в Common Data Service, чтобы все пользователи приложений, включая пользователей Power Platform, могли воспользоваться богатыми данными о продуктах, поступающим из приложений Finance and Operations.

Ниже приведена модель данных о продукции из Sales.

![Модель данных для продуктов в CE](media/dual-write-product-4.jpg)

Ниже приведена модель данных о продукции из приложений Finance and Operations.

![Модель данных для продуктов в Finance and Operations](media/dual-write-products-5.jpg)

Эти две модели данных продукции были интегрированы в Common Data Service, как показано ниже.

![Модель данных для продуктов в приложениях Dynamics 365](media/dual-write-products-6.jpg)

Объекты с двойной записью для продуктов были спроектированы так, чтобы передавать данные только в одном направлении, и это происходит почти в режиме реального времени из приложений Finance and Operations в Common Data Service. Однако инфраструктура продуктов была сделана открытой, чтобы сделать ее двунаправленной, если это необходимо. Хотя клиенты могут настроить ее, это ваша ответственность, корпорация Майкрософт не рекомендует использовать этот подход.

## <a name="templates"></a>Шаблоны

Информация о продукте содержит все сведения, имеющие отношение к продукту и его определению, такие как аналитики продукта или аналитики отслеживания и хранения. Как показано в следующей таблице, для синхронизации продуктов и связанных сведений создается коллекция сопоставлений объектов.

Приложения Finance and Operations | Другие приложения Dynamics 365 | описание
-----------------------|--------------------------------|---
Выпущенные продукты V2 | msdyn\_sharedproductdetails | Объект **msdyn\_sharedproductdetails** содержит поля из приложений Finance and Operations, определяющие продукт, которые содержат финансовые сведения и сведения об управлении данным продуктом. 
Уникально идентифицируемые продукты, выпущенные Common Data Service | Продукт | Объект **Продукт** содержит поля, определяющие продукт. Он включает в себя отдельные продукты (продукты с подтипом продукта) и варианты продукта. Сопоставления представлены в таблице ниже.
Штрихкод, связанный с номером продукта | msdyn\_productbarcodes | Штрих-коды продукта используются для уникальной идентификации продуктов.
Параметры заказа по умолчанию | msdyn\_productdefaultordersettings
Специфические для продукта параметры заказа по умолчанию | msdyn_productdefaultordersettings
Группы аналитик продукта | msdyn\_productdimensiongroups | Группа аналитик продукта, определяющая, какие аналитики продукта определяют продукт. 
Группы аналитик хранения | msdyn\_productstoragedimensiongroups | Группа аналитик хранения продукта представляет метод, используемый для определения местоположения продукта на складе.
Группы аналитик отслеживания | msdyn\_producttrackingdimensiongroups | Группа аналитик отслеживания продукта представляет метод, используемый для отслеживания продукта на складе.
Цвета | msdyn\_productcolors
Размеры | msdyn\_productsizes
Стили | msdyn\_productsytles
Конфигурации | msdyn\_productconfigurations
Цвета шаблонов продуктов | msdyn_sharedproductcolors | Объект **Общий цвет продуктов** указывает цвета, которые может иметь конкретный шаблон продукта. Эта концепция переносится в Common Data Service для обеспечения согласованности данных.
Размеры шаблонов продуктов | msdyn_sharedproductsizes | Объект **Общий размер продуктов** указывает размеры, которые может иметь конкретный шаблон продукта. Эта концепция переносится в Common Data Service для обеспечения согласованности данных.
Стили шаблонов продуктов | msdyn_sharedproductstyles | Объект **Общий стиль продуктов** указывает стили, которые может иметь конкретный шаблон продукта. Эта концепция переносится в Common Data Service для обеспечения согласованности данных.
Конфигурации шаблонов продуктов | msdyn_sharedproductconfigurations | Объект **Общая конфигурация продуктов** указывает конфигурации, которые может иметь конкретный шаблон продукта. Эта концепция переносится в Common Data Service для обеспечения согласованности данных.
Все продукты | msdyn_globalproducts | Объект всех продуктов содержит все продукты, доступные в приложениях Finance and Operations, как выпущенные, так и невыпущенные продукты.
Ед. изм. | uoms
Пересчеты единиц измерения | msdyn_ unitofmeasureconversions
Специфичное для продукта преобразование единиц измерения | msdyn_productspecificunitofmeasureconversion
Категории продуктов | msdyn_productcategories | Каждая из категорий продуктов и информации о ее структуре и характеристиках содержится в объекте категории продукта. 
Иерархии категорий продуктов | msdyn_productcategoryhierarhies | Иерархия продуктов используется для классификации или группировки продуктов. Иерархии категорий доступны в Common Data Service при использовании объекта иерархии категорий продуктов. 
Роли иерархии категорий продуктов | msdyn_productcategoryhierarchies | Иерархии продуктов могут использоваться для разных ролей в D365 Finance and Operations. Они указывают, какая категория используется в каждой роли, используется объект роли категории продукта. 
Назначения категорий продуктов | msdyn_productcategoryassignments | Чтобы назначить продукт для категории, можно использовать объект назначений категорий продуктов.

## <a name="integration-of-products"></a>Интеграция продуктов

В этой модели продукт представлен комбинацией двух объектов в Common Data Service: **Продукт** и **msdyn\_sharedproductdetails**. В то время как первый объект содержит определение продукта (уникальный идентификатор продукта, название продукта и описание), второй объект содержит поля, которые хранятся на уровне продукта. Сочетание этих двух объектов используется для определения продукта в соответствии с понятием единицы складского хранения (SKU). Каждый выпущенный продукт будет иметь свою информацию в упомянутых объектах (продукт и общие сведения о продукте). Для отслеживания всех продуктов (выпущенных и не выпущенных) используется объект **Глобальные продукты**. 

Поскольку продукт представлен в виде SKU, концепция отдельных продуктов, шаблонов продуктов и вариантов продуктов может быть реализована в Common Data Service следующим образом:

- **Продукты с подтипом продукта** — это продукты, которые определены сами по себе. Не были определены никакие аналитики. Примером является конкретная книга. Для этих продуктов одна запись создается в объекте **Продукт** и одна запись создается в объекте **msdyn\_sharedproductdetails**. Запись семейства продуктов не создается.
- **Шаблоны продукта** используются как универсальные продукты, содержащие определение и правила, определяющие поведение в бизнес-процессах. На основе этих определений могут быть созданы уникально идентифицируемые продукты, известные как варианты продукта. Например, футболка — это шаблон продукта, который может иметь цвет и размер в качестве аналитик. Варианты могут быть выпущены с различной комбинацией этих аналитик, такие как маленькая синяя футболка или средняя зеленая футболка. В интеграции в таблице продуктов создается одна запись для каждого варианта. Эта запись содержит сведения, специфичные для варианта, такие как различные аналитики. Общая информация о продукте хранится в объекте **msdyn\_sharedproductdetails**. (Эта общая информация хранится в шаблоне продукта.) Кроме того, для шаблона продукта создается одна запись семейства продуктов. Информация шаблона продукта синхронизируется с Common Data Service в момент создания шаблона выпущенного продукта (но до выпуска вариантов).
- **Уникально идентифицируемые продукты** обозначают все продукты подтипа продуктов и на все варианты продукта. 

![Модель данных для продуктов](media/dual-write-product.png)

При включенной функции двойной записи приложения из Finance and Operations будут синхронизироваться в других приложениях Dynamics 365 в состоянии **Черновик**. Они добавляются к первому прайс-листу с такой же валютой. Другими словами, они добавляются к первому прайс-листу в приложении Dynamics 365, который соответствует валюте юридического лица, в котором продукт выпущен в приложении Finance and Operations. 

По умолчанию продукты из Finance and Operations синхронизируются с другими приложениями Dynamics 365 в состоянии **Черновик**. Для синхронизации продукта с состоянием **Активный**, чтобы его можно было напрямую использовать в предложениях с расценками по заказам на продажу, например, следует выбрать следующую настройку: на вкладке **Система > Администрирование > Администрирование системы > Параметры системы > Sales** выберите **Создавать продукты в активном состоянии = да**. 

Обратите внимание, что синхронизация продуктов происходит из приложений Finance and Operations для Common Data Service. Это означает, что значения полей объекта продукта можно изменить в Common Data Service, но если синхронизация активирована (при изменении поля продукта в приложении Finance and Operations), это приведет к перезаписи значений в Common Data Service. 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [products](includes/EcoResReleasedDistinctProductCDSEntity-products.md)]

[!include [product details](includes/EcoResReleasedProductV2-msdyn-sharedproductdetails.md)]

[!include [global products](includes/EcoResEveryProductEntity-msdyn-globalproducts.md)]

## <a name="product-dimensions"></a>Аналитики продуктов 

Аналитики продукта — это характеристики, которые определяют вариант продукта. Четыре аналитики продукта (цвет, размер, стиль и конфигурация) также сопоставляются с Common Data Service для определения вариантов продукта. На следующем рисунке показана модель данных для аналитики продукта "Цвет". Эта же модель применяется к размерам, стилям и конфигурациям. 

![Модель данных для продуктов](media/dual-write-product-two.png)

[!include [product colors](includes/EcoResProductColorEntity-msdyn-productcolor.md)]

[!include [product sizes](includes/EcoResProductSizeEntity-msdyn-productsizes.md)]

[!include [product sizes](includes/EcoResProductStyleEntity-msdyn-productstyles.md)]

[!include [product sizes](includes/EcoResProductConfigurationsEntity-msdyn-productconfigurations.md)]

Если у продукта имеются различные аналитики продукта (например, шаблон продукта имеет размеры и цвет как аналитики продукта), каждый уникально идентифицируемый продукт (то есть, каждый вариант продукта) определяется как сочетание этих аналитик продукта. Например, продукт с номером B0001 является очень маленькой черной футболкой, а продукт номер B0002 — маленькой черной футболкой. В этом случае определяются существующие комбинации аналитик продукта. Например, футболка из предыдущего примера может быть очень маленькой и черной, маленькой и черной, средней и черной или большой и черной, но не может быть очень большой и черной. Иными словами, задаются аналитики продукта, которые может принимать шаблон продукта, и варианты могут быть выпущены на основе этих значений.

Для отслеживания аналитик продукта, которые может принимать шаблон продукта, создаются и сопоставляются следующие объекты в Common Data Service для каждой аналитики продукта. Для получения дополнительных сведений см. раздел [Обзор сведений о продуктах](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/pim/product-information).

[!include [product colors](includes/EcoResProductMasterColorEntity-msdyn-sharedproductcolors.md)]

[!include [product sizes](includes/EcoResProductMasterSize-msdyn-sharedproductsizes.md)]

[!include [product styles](includes/EcoResProductMasterStyleEntity-msdyn-sharedproductstyles.md)]

[!include [product configurations](includes/EcoResProductMasterConfigurationEntity-msdyn-sharedproductconfigurations.md)]

[!include [product bar codes](includes/EcoResProductNumberIdentifiedBarcode-msdyn-productbarcodes.md)]

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Настройки заказа по умолчанию и настройки заказа по умолчанию для определенных продуктов

Параметры заказа по умолчанию определяет сайт и склад, с которого будут забираться или на которых будут складироваться продукты, минимальное, максимальное, кратное и стандартное количества, который будут использоваться для торговли или управление запасами, значения времени упреждения, флаг остановки и метод обещанного заказа. Эти сведения будут доступны в Common Data Service с использованием используемых по умолчанию настроек заказов и объекта специфичных для продукта настроек заказа по умолчанию. Дополнительные сведения об этой функции см. в [теме настроек заказа по умолчанию](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/default-order-settings).

[!include [product sizes](includes/InventProductDefaultOrderSettingsEntity-msdyn-productdefaultordersetting.md)]

[!include [product sizes](includes/InventProductSpecificOrderSettingsV2Entity-msdyn-productspecificdefaultordersetting.md)]

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Единицы измерения и преобразования единиц измерения

Единицы измерения и соответствующее им преобразование будут доступны в Common Data Service в соответствии с моделью данных, показанной на диаграмме.

![Модель данных для продуктов](media/dual-write-product-three.png)

Концепция единицы измерения интегрирована между приложениями Finance and Operations и другими приложениями Dynamics 365. Для каждого класса единиц измерения в приложении Finance and Operations группа единиц измерения создается в приложении Dynamics 365, которая содержит единицы измерения, принадлежащие к классу единиц измерения. Базовая единица измерения по умолчанию также создается для каждой группы единиц измерения. 

[!include [unit of measure](includes/UnitOfMeasureEntity-uom.md)]

[!include [unit of measure conversions](includes/UnitOfMeasureConversionEntity-msdyn-unitofmeasureconversions.md)]

[!include [product-specific unit of measure conversions](includes/EcoResProductSpecificUnitConversionEntity-msdyn-productspecificunitofmeasureconversions.md)]

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-common-data-service"></a>Начальная синхронизация данных единиц измерения между Finance and Operations и Common Data Service

### <a name="initial-synchronization-of-units"></a>Начальная синхронизация единиц

Если включена двойная запись единицы из приложений Finance and Operations синхронизируются с другими приложениями Dynamics 365. Группы единиц измерения, синхронизируемые из приложений Finance and Operations в Common Data Service, имеют флаг, который указывает на то, что они "управляются извне".

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Сопоставление единиц измерения и данных классов единиц измерения или групп из Finance and Operations и других приложений Dynamics 365

Во-первых, важно отметить, что ключ интеграции для единицы — msdyn_symbol. Таким образом, это значение должно быть уникальным в Common Data Service или в других приложениях Dynamics 365. Так как в других приложениях Dynamics 365 используется пара "Код группы единиц" и "Имя", определяющие уникальность единицы измерения, необходимо учитывать другие ситуации при сопоставлении данных единиц между приложениями Finance and Operations и Common Data Service.

Для сопоставления или перекрывания единиц в приложениях Finance and Operations и других приложениях Dynamics 365:

+ **Единица измерения принадлежит к группе единиц измерения в других приложениях Dynamics 365, которая соответствует связанному классу единиц измерения в приложениях Finance and Operations**. В этом случае поле msdyn_symbol в других приложениях Dynamics 365 должно быть заполнено символом единицы из приложений Finance and Operations. Следовательно, когда данные будут сопоставлены, группа единиц измерения будет установлена как "Управляется извне" в других приложениях Dynamics 365.
+ **Единица измерения принадлежит к группе единиц измерения в других приложениях Dynamics 365, которая не соответствует связанному классу единиц в приложениях Finance and Operations (нет ни одного класса единиц измерения в приложениях Finance and Operations для класса единиц измерения в других приложениях Dynamics 365).** В этом случае поле msdyn_symbol должно быть заполнено случайной строкой. Обратите внимание, что это значение должно быть уникальным в других приложениях Dynamics 365.

Для единиц и классов единиц в Finance and Operations, не существующих в других приложениях Dynamics 365:

В процессе двойной записи группы единиц измерения из приложений Finance and Operations и соответствующие единицы создаются и синхронизируются в других приложениях Dynamics 365 и Common Data Service, группа единиц задается как "Управляется извне". Дополнительные действия по начальной загрузке не требуются.

Для единиц в других приложениях Dynamics 365, которые не существуют в приложениях Finance and Operations:

Поле msdyn_symbol должно быть заполнено для всех единиц измерения. Единицы измерения могут быть созданы в приложениях Finance and Operations в соответствующем классе единиц измерения (если он существует). Если класс единиц измерения не существует, необходимо создать класс единиц измерения (обратите внимание, что вы не можете создать класс единиц в приложениях Finance and Operations, кроме как с помощью расширения, если выполняется расширение перечислений), соответствующий группе единиц измерения для других приложений Dynamics 365. После этого можно создать единицу. Обратите внимание, что символ единицы в приложениях Finance and Operations должен быть msdyn_symbol, указанным ранее в приложениях Dynamics 365 для единицы.

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>Политики продуктов: группы аналитик, отслеживания и хранения

Политики продуктов — это наборы политик, используемых для определения продуктов и их характеристик на складе. Группа аналитик продукта, группа аналитик отслеживания продукта и группа аналитик хранения могут быть представлены в качестве политик продукта. 

[!include [product dimension group](includes/EcoResProductDimensionGroup-msdyn-productdimensiongroups.md)]

[!include [product tracking dimension group](includes/EcoResTrackingDimensionGroup-msdyn-producttrackingdimensiongroups.md)]

[!include [product storage dimension group](includes/EcoResStorageDimensionGroup-msdyn-productstoragedimensiongroups.md)]

## <a name="product-hierarchies"></a>Иерархии продуктов

[!include [product category hierarchy](includes/EcoResProductCategoryHierarchyEntity-msdyn-productcategoryhierarchy.md)]

[!include [product category](includes/EcoResProductCategoryEntity-msdyn-productcategory.md)]

[!include [product category assignments](includes/EcoResProductCategoryAssignmentEntity-msdyn-productcategoryassignment.md)]

[!include [product category role](includes/EcoResProductCategoryHierarchyRoleEntity-msdyn-productcategoryhierarchyrole.md)]


## <a name="integration-key-for-products"></a>Ключ интеграции для продуктов 

Для уникальной идентификации продуктов между Dynamics 365 for Finance and Operations и продуктов в Common Data Service используются ключи интеграции. Для продуктов **(productnumber)** — это уникальный ключ, идентифицирующий продукт в Common Data Service. Он состоит из объединения: **(company, msdyn_productnumber)**. **company** означает юридическое лицо в Finance and Operations **msdyn_productnumber** означает номер продукта для конкретного продукта в Finance and Operations. 

Для пользователей других приложений Dynamics 365 продукт определяется в интерфейсе пользователя с помощью **msdyn_productnumber** (обратите внимание, что метка поля — **Номер продукта**). В форме продукта отображаются и company, и msydn_productnumber. Однако поле (productnumber), уникальный ключ продукта, не отображается. 

Если вы создаете приложения на основе Common Data Service, вам следует уделять внимание использованию **productnumber** (уникальный код продукта) в качестве ключа интеграции. Не следует использовать **msdyn_productnumber**, поскольку он не является уникальным. 

## <a name="initial-synchronization-of-products-and-migration-of-data-from-common-data-service-to-finance-and-operations"></a>Начальная синхронизация продуктов и перенос данных из Common Data Service в Finance and Operations

### <a name="initial-synchronization-of-products"></a>Начальная синхронизация продуктов 

Если включена двойная запись, продукты из приложений Finance and Operations синхронизируются с Common Data Service и другими приложениями на основе модели в Dynamics 365. Продукты, созданные в Common Data Service и других приложениях Dynamics 365 до выпуска двойной записи, не будут обновлены и сопоставлены с данными о продуктах из приложений Finance and Operations.

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Сопоставление данных о продуктах из Finance and Operations и других приложений Dynamics 365

Если одни и те же продукты хранятся (перекрываются или совпадают) в Finance and Operations и в Common Data Service, а также в других приложениях Dynamics 365, то при разрешении двойной записи синхронизация продуктов из Finance and Operations будет выполняться и дублирующиеся записи появятся в Common Data Service для одного и того же продукта.
Чтобы избежать возникновения такой ситуации, если в других приложениях Dynamics 365 имеются продукты, которые перекрываются или сопоставляются с Finance and Operations, администратор, включающий возможность двойной записи, должен выполнить начальную загрузку полей **Компания** (например: "USMF") и **msdyn_productnumber** (например: "1234:Black:S") перед синхронизацией продуктов. Другими словами, эти два поля в продукте в Common Data Service должны быть заполнены соответствующей компанией в Finance and Operations, с указанием продукта сопоставления и номера продукта. 

Затем, когда синхронизация включена и выполняется, продукты из Finance and Operations будут синхронизированы с продуктами, сопоставленными в Common Data Service и других приложениях Dynamics 365. Это применимо как для уникально идентифицируемых продуктов, так и для вариантов продуктов. 


### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>Миграция данных о продуктах из других приложений Dynamics 365 в Finance and Operations

Если в других приложениях Dynamics 365 есть продукты, отсутствующие в Finance and Operations, администратор может сначала использовать **EcoResReleasedProductCreationV2Entity** для импорта этих продуктов в Finance and Operations. Во-вторых, сопоставьте данные о продуктах в Finance and Operations и других приложениях Dynamics 365, как описано выше. 
