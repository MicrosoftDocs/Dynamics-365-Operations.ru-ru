---
title: Цепочка зависимостей объектов (порядок синхронизации)
description: Эта тема определяет порядок синхронизации, который необходимо соблюдать для создания исходных данных.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
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
ms.openlocfilehash: 4adb2c8d57ad8f67346b8d34212b7a4b0bd052ab
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173139"
---
# <a name="entity-dependency-chain-synchronization-order"></a>Цепочка зависимостей объектов (порядок синхронизации)

[!include [banner](../../includes/banner.md)]



В следующих таблицах объекты указаны в том в порядке, в каком их следует включать. При включении сопоставления для первоначальной синхронизации система с двойной записью автоматически определяет другие сопоставления, которые должны быть включены. Страницу **Двойная запись** в приложениях Finance and Operations можно использовать для выбора или отмены выбора объектов во время первоначальной синхронизации.

В последней версии двойной записи можно включить только некоторые объекты, и эти зависимости будут обработаны.

## <a name="dynamics-365-supply-chain-management-entities"></a>Объекты Dynamics 365 Supply Chain Management

Следующие объекты для Supply Chain Management указаны в том в порядке, в каком их следует включать.

| Имя сопоставления на странице двойной записи | Имя метаданных объекта в Supply Chain Management | Имя метаданных объекта в Common Data Service | Основание |
|---|---|---|---|
| Единицы измерения ... uoms                                                                      | UnitOfMeasureEntity                                    | uom                                          | |
| Преобразования единиц измерения ... msdyn_unitofmeasureconversions                                 | UnitOfMeasureConversionEntity                          | msdyn_unitofmeasureconversion                | |
| Все продукты ... msdyn_globalproducts                                               | EcoResEveryProductEntity                               | msdyn_globalproduct                          | |
| Группы аналитик продуктов ... msdyn_productdimensiongroups                           | EcoResProductDimensionGroupEntity                      | msdyn_productdimensiongroup                  | |
| Группы аналитик хранения ... msdyn_productstoragedimensiongroups                    | EcoResStorageDimensionGroupEntity                      | msdyn_productstoragedimensiongroup           | |
| Группы аналитик отслеживания ... msdyn_producttrackingdimensiongroups                  | EcoResTrackingDimensionGroupEntity                     | msdyn_producttrackingdimensiongroup          | |
| Цвета ... msdyn_productcolors                                                      | EcoResProductColorEntity                               | msdyn_productcolor                           | |
| Размеры ... msdyn_productsizes                                                        | EcoResProductSizeEntity                                | msdyn_productsize                            | |
| Стили ... msdyn_productstyles                                                      | EcoResProductStyleEntity                               | msdyn_productstyle                           | |
| Конфигурации ... msdyn_productconfigurations                                      | EcoResProductConfigurationEntity                       | msdyn_productconfiguration                   | |
| Выпущенные продукты V2 ... msdyn_sharedproductdetails                                 | EcoResReleasedProductV2Entity                          | msdyn_sharedproductdetail                    | |
| Выпущенные в Common Data Service уникально идентифицируемые продукты ... продукты                         | EcoResReleasedDistinctProductCommon Data ServiceEntity | продукт                                      | |
| Штрих-код, определяющий номер продукта ... msdyn_productbarcodes                         | EcoResProductNumberIdentifiedBarcodeEntity             | msdyn_productbarcode                         | |
| Параметры заказа по умолчанию ... msdyn_productdefaultordersettings                        | InventProductDefaultOrderSettingsEntity                | msdyn_productdefaultordersetting             | |
| Параметры заказа продуктов по умолчанию V2 ... msdyn_productspecificdefaultordersettings     | InventProductSpecificOrderSettingsV2Entity             | msdyn_productspecificdefaultordersetting     | |
| Пересчеты единиц измерения конкретных продуктов ... msdyn_productspecificunitofmeasureconversions | EcoResProductSpecificUnitConversionEntity              | msdyn_productspecificunitofmeasureconversion | |
| Сайты ... msdyn_operationalsites                                                    | InventOperationalSiteEntity                            | msdyn_operationalsite                        | |
| Склады ... msdyn_warehouses                                                     | InventWarehouseEntity                                  | msdyn_warehouse                              | См. [примечание 1](#scm-notes). |
| Цвета шаблонов продуктов ... msdyn_sharedproductcolors                                 | EcoResProductMasterColorEntity                         | msdyn_sharedproductcolor                     | |
| Размеры шаблонов продуктов ... msdyn_sharedproductsizes                                   | EcoResProductMasterSizeEntity                          | msdyn_sharedproductsize                      | |
| Стили шаблонов продуктов ... msdyn_sharedproductstyles                                 | EcoResProductMasterStyleEntity                         | msdyn_sharedproductstyle                     | |
| Конфигурации шаблонов продуктов ... msdyn_sharedproductconfigurations                 | EcoResProductMasterConfigurationEntity                 | msdyn_sharedproductconfiguration             | |
| Категории продуктов ... msdyn_productcategories                                      | EcoResProductCategoryEntity                            | msdyn_productcategory                        | См. [примечание 2](#scm-notes). |
| Назначения категорий продуктов ... msdyn_productcategoryassignments                   | EcoResProductCategoryAssignmentEntity                  | msdyn_productcategoryassignment              | |
| Иерархии категорий продуктов ... msdyn_productcategoryhierarchies                   | EcoResProductCategoryHierarchyEntity                   | msdyn_productcategoryhierarchy               | |
| Роли иерархии категорий продуктов ... msdyn_productcategoryhierarchyroles            | EcoResProductCategoryHierarchyRoleEntity               | msdyn_productcategoryhierarchyrole           | |
| Складской проход ... msdyn_warehouseaisles                                           | WMSWarehouseAisleEntity                                | msdyn_warehouseaisle                         | |
| Зоны склада ... msdyn_warehousezones                                            | WHSWarehouseZoneEntity                                 | msdyn_warehousezone                          | |
| Группы зон склада ... msdyn_warehousezonegroups                                 | WHSWarehouseZoneGroupEntity                            | msdyn_warehousezonegroup                     | |
| Местонахождение складов ... msdyn_inventorylocations                                    | WMSWarehouseLocationEntity                             | msdyn_inventorylocation                      | См. [примечание 3](#scm-notes). |
| Заголовки работ склада ... msdyn_warehouseworkheaders                               | WHSWarehouseWorkHeaderEntity                           | msdyn_warehouseworkheader                    | |
| Строки работ склада ... msdyn_warehouseworklines                                    | WHSWarehouseWorkLineEntity                             | msdyn_warehouseworklines                     | См. [примечание 4](#scm-notes). |
| Режимы доставки ... msdyn_shipvias                                                | DlvDeliveryModeEntity                                  | msdyn_shipvias                               | |
| Условия поставки ... msdyn_termsofdeliveries                                       | DeliveryTermsEntity                                    | msdyn_termsofdelivery                        | |
| Коды происхождения заказов на продажу ... msdyn_salesorderorigins                                | SalesOrderOriginEntity                                 | msdyn_salesorderorigin                       | |
| Заголовки заказов на продажу Common Data Service ... salesorders                             | SalesOrderHeaderCommon Data ServiceEntity              | salesorder                                   | |
| Строки заказа на продажу Common Data Service ... salesorderdetails                         | SalesOrderLineCommon Data ServiceEntity                | salesorderdetails                            | |
| Заголовок предложения по продаже Common Data Service ... quotes                               | SalesQuotationHeaderCommon Data ServiceEntity          | предложение                                        | |
| Строки предложения по продаже Common Data Service ... quotedetails                          | SalesQuotationLineCommon Data ServiceEntity            | QuoteDetails                                 | |
| Заголовки накладной заказа на продажу V2 ... invoices                                               | SalesInvoiceHeaderV2Entity                             | накладная                                      | |
| Строки накладной заказа на продажу V2 ... invoicedetails                                           | SalesInvoiceLineV2Entity                               | invoicedetail                                | |

### <a name="mapping-specific-notes"></a><a id='scm-notes'></a>Примечания, связанные с сопоставлениями

1. Из-за наличия самозависимости может потребоваться выполнить начальную синхронизацию два раза.
2. По умолчанию начальная синхронизация отключена из-за отношения "родители-потомки" ("интеллектуальное" упорядочивание не обрабатывается платформой). Поэтому существующие категории продуктов должны быть синхронизированы вручную (например, путем обновления описания категории) в правильном порядке (сначала корневая категория, затем потомки, затем потомки потомков). Перейдите в раздел **Управление сведениями о продукте \> Настройка \> Категории и атрибуты \> Иерархии категорий**. На странице **Иерархии категорий** можно выбрать каждую иерархию и просмотреть в ней категории продуктов.
3. Сопоставление пустых полей подстановки **ItemNumberInLocation** и первой, второй и третьей дополнительных складских зон приведут к сбою первоначальной синхронизации. Поэтому эти сопоставления удалены в данное время.
4. Сопоставление пустого поля **CaptureWeight** приведет к сбою первоначальной синхронизации. Поэтому это сопоставление удалено в данное время.

### <a name="setup-related-information"></a>Информация, связанная с настройкой

+ Когда записи первоначально создаются в объекте **Продукты** в приложениях на основе моделей в Dynamics 365, они имеют статус **Черновик**. Чтобы изменить статус на **Активный**, перейдите в раздел **Параметры \> Администрирование \> Параметры системы \> Sales** в приложении на основе модели и установите для параметра **Создавать продукты в активном состоянии** значение **Да**.
+ При создании записей в объекте **Продукты** в приложениях на основе модели в Dynamics 365 или в Common Data Service до включения двойной записи эти записи будут обновляться только в том случае, если весь ключ, включая часть **Компания**, соответствует данным п приложении Finance and Operations.
+ Синхронизация объекта **Продукты** является односторонней, из приложений Finance and Operations в Common Data Service. Если сопоставленное поле в объекте **Продукты** в приложениях на основе модели в Dynamics 365 обновлено, обновление будет перезаписано во время следующей синхронизации из приложения Finance and Operations.

### <a name="known-issues"></a>Известные проблемы

- Ошибка возникает, когда в приложении Finance and Operations удаляется единица измерения. Когда единицы измерения синхронизируются из приложения Finance and Operations в Common Data Service, первая единица измерения определенного класса будет создана в качестве первичного блока и будет предотвращать удаление.

    **Решение:** сначала удалите единицу измерения в Common Data Service. Затем ее можно удалить в приложении Finance and Operations.

- Ошибка возникает, когда в приложении Common Data Service удаляется операционный сайт. Выводится сообщение об ошибке "Infolog: Предупреждение: удаление основного адреса не допускается.; Предупреждение: невозможно удалить запись объекта из-за сбоя проверки для следующего источника данных: InventSiteLogisticsLocation (InventSiteLogisticsLocation)". Эта ошибка вызвана проблемой в объекте данных в приложении Finance and Operations.

    **Решение:** можно удалить сайт в приложении Finance and Operations. После этого сайт будет удален в Common Data Service, если выполняется соответствующее сопоставление двойной записи.

## <a name="dynamics-365-finance-entities"></a>Объекты Dynamics 365 Finance

Следующие объекты для Dynamics 365 Finance указаны в том в порядке, в каком их следует включать.

| Имя сопоставления на странице двойной записи | Имя метаданных объекта в Finance | Имя метаданных объекта в Common Data Service | Основание |
|---|---|---|---|
| Валюты ... transactioncurrencies                                            | CurrencyEntity                              | Денежный                                   | |
| Тип валютного курса ... msdyn_exchangeratetypes                                  | ExchangeRateTypeEntity                      | msdyn_exchangeratetype                     | |
| Пара валют валютного курса ... msdyn_currencyexchangeratepairs                 | ExchangeRateCurrencyPairEntity              | msdyn_currencyexchangeratepair             | |
| Валютные курсы Common Data Service ... msdyn_currencyexchangerates              | ExchangeRateCommon Data ServiceEntity       | msdyn_currencyexchangerate                 | См. [примечание 1](#fin-notes). |
| Объект интеграции финансового календаря ... msdyn_fiscalcalendars                    | FiscalCalendarEntity                        | msdyn_fiscalcalendar                       | |
| Объект интеграции года финансового календаря ... msdyn_fiscalcalendaryears           | FiscalCalendarYearEntity                    | msdyn_fiscalcalendaryear                   | |
| Период финансового календаря ... msdyn_fiscalcalendarperiods                          | FiscalPeriodEntity                          | msdyn_fiscalcalendarperiod                 | |
| Тип организационной иерархии ... msdyn_internalorganizationhierarchytypes        | OMOrganizationHierarchyTypeEntity           | msdyn_internalorganizationhierarchytype    | См. [примечание 1](#fin-notes). |
| Цели организационной иерархии ... msdyn_internalorganizationhierarchypurposes | OMOrganizationHierarchyPurposeEntity        | msdyn_internalorganizationhierarchypurpose | См. [примечание 1](#fin-notes). |
| Юридические лица ... msdyn_internalorganizations                                  | OMLegalEntity                               | msdyn_internalorganization                 | См. [примечание 1](#fin-notes). |
| Юридические лица ... cdm_companies                                                | OMLegalEntity                               | cdm_company                                | |
| Операционная единица ... msdyn_internalorganizations                                  | OMOperatingUnitEntity                       | msdyn_internalorganization                 | См. [примечание 1](#fin-notes). |
| Опубликованная организационная иерархия ... msdyn_internalorganizationhierarchypurposes    | OMOrganizationHierarchyPublishedEntity      | msdyn_internalorganizationhierarchy        | См. [примечание 1](#fin-notes). |
| Аффиксы имен ... msdyn_nameaffixes                                              | DirNameAffixEntity                          | msdyn_nameaffix                            | |
| Платежные дни Common Data Service ... msdyn_paymentdays                          | PaymentDayCommon Data ServiceEntity         | msdyn_paymentday                           | |
| Строки платежных дней Common Data Service V2 ... msdyn_paymentdaylines              | PaymentDayLineCommon Data ServiceV2Entity   | msdyn_paymentdayline                       | |
| График оплаты ... msdyn_paymentschedules                                     | PaymentScheduleEntity                       | msdyn_paymentschedule                      | |
| Строки графика оплаты ... msdyn_paymentschedulelines                           | PaymentScheduleLineEntity                   | msdyn_paymentscheduleline                  | |
| Условия оплаты ... msdyn_paymentterms                                         | PaymentTermEntity                           | msdyn_paymentterm                          | |
| Способ оплаты клиента ... msdyn_customerpaymentmethods                        | CustomerPaymentMethodEntity                 | msdyn_customerpaymentmethod                | |
| Способ оплаты поставщика ... msdyn_vendorpaymentmethods                            | VendorPaymentMethodEntity                   | msdyn_vendorpaymentmethod                  | |
| Группы клиентов ... msdyn_customergroups                                        | CustCustomerGroupEntity                     | msdyn_customergroup                        | |
| Группы поставщиков ... msdyn_vendorgroups                                            | VendVendorGroupEntity                       | msdyn_vendorgroup                          | |
| Налоговые группы ... msdyn_taxgroups                                            | TaxGroupEntity                              | msdyn_taxgroup                             | |
| Налоговая группа номенклатур ... msdyn_taxitemgroups                                   | TaxItemGroupEntity                          | msdyn_taxitemgroup                         | |
| Группы разноски ГК для налога V2 ... msdyn_taxpostinggroups                   | TaxPostingGroupEntityV2                     | msdyn_taxpostinggroup                      | |
| Объект кода налогового освобождения Common Data Service ... msdyn_taxexemptcodes       | TaxExemptCodeCommon Data ServiceEntity      | msdyn_taxexemptcode                        | |
| Налоговые органы ... msdyn_taxauthorities                                  | TaxAuthorityEntity                          | msdyn_taxauthority                         | |
| Налоговый код ... msdyn_taxcodes                                               | TaxCodeEntity                               | msdyn_taxcode                              | См. [примечание 1](#fin-notes). |
| Формат финансовой аналитики ... msdyn_financialdimensionformats                  | DimensionIntegrationFormatEntity            | msdyn_financialdimensionformat             | |
| Финансовые аналитики ... msdyn_dimensionattributes                              | DimensionAttributeEntity                    | msdyn_dimensionattribute                   | |
| Группы подоходного налога ... msdyn_withholdingtaxgroups                           | TaxWithholdingGroupEntity                   | msdyn_withholdingtaxgroup                  | |
| Коды подоходного налога ... msdyn_withholdingtaxcodes                             | TaxWithholdingTaxCodes                      | msdyn_withholdingtaxcode                   | |
| План счетов ... msdyn_chartofaccountses                                   | LedgerChartOfAccountsEntity                 | msdyn_chartofaccounts                      | |
| Книга учета ... msdyn_ledgers                                                        | LedgerEntity                                | msdyn_ledger                               | См. [примечание 1](#fin-notes). |
| Категории счетов ГК ... msdyn_mainaccountcategories                         | MainAccountCategoryEntity                   | msdyn_mainaccountcategory                  | |
| Счет ГК ... msdyn_mainaccounts                                             | MainAccountEntity                           | msdyn_mainaccount                          | |
| Клиенты V3 ... организации                                                       | CustCustomerV3Entity                        | счет                                    | См. [примечание 2](#fin-notes). |
| Клиенты V3 ... контакты                                                       | CustCustomerV3Entity                        | контакт                                    | См. [примечание 3](#fin-notes). |
| Поставщики V2 ... msdyn_vendors                                                    | VendVendorV2Entity                          | msdyn_vendor                               | См. [примечание 2](#fin-notes). |
| Контакты Common Data Service V2 ... контакты                                    | smmContactPersonCommon Data ServiceV2Entity | контакт                                    | См. [примечание 4](#fin-notes). |
| Контакты Common Data Service V2 ... контакты                                    | smmContactPersonCommon Data ServiceV2Entity | контакт                                    | См. [примечание 5](#fin-notes). |

### <a name="mapping-specific-notes"></a><a id='fin-notes'></a>Примечания, связанные с сопоставлениями

1. Однонаправленная синхронизация выполняется из приложений Finance and Operations в Common Data Service.
2. Из-за наличия самозависимости может потребоваться выполнить начальную синхронизацию несколько раз. Обязательно выберите **Клиент** в качестве типа отношения при создании организации с использованием страницы **Организации** в Common Data Service. При возникновении проблем с полем **Основной контакт** во время первоначальной синхронизации удалите это поле из сопоставления, затем снова запустите исходную синхронизацию. После успешного завершения первоначальной синхронизации следует остановить сопоставление и снова добавить к нему поле **Основной контакт**. Затем запустите сопоставление, но пропустите начальную синхронизацию. Значение поля **Основной контакт** не будет включено в начальную синхронизацию, и необходимо будет переносить значения вручную.
3. Обязательно установите для параметра **Для продажи** значение **Да** на странице **Контакты** в Common Data Service при попытке создать клиента типа **Физическое лицо**.
4. Это сопоставление имеет фильтр по обеим сторонам, чтобы связать контакты клиента. Откройте сведения о сопоставлении, нажмите кнопку фильтра (символ воронки) рядом с именем объекта **Sales.Contact** и убедитесь, что критерий файла содержит **msdyn_contactforvendor eq true and msdyn_sellable eq false**.
5. Это сопоставление имеет фильтр по обеим сторонам, чтобы связать контакты поставщика. Откройте сведения о сопоставлении, нажмите кнопку фильтра (символ воронки) рядом с именем объекта **Sales.Contact** и убедитесь, что критерий фильтра содержит **msdyn_contactforvendor eq true and msdyn_sellable eq false**. 

## <a name="dynamics-365-human-resources-entities"></a>Объекты Dynamics 365 Human Resources

Следующие объекты для Dynamics 365 Human Resources указаны в том в порядке, в каком их следует включать.

| Имя сопоставления на странице двойной записи | Имя метаданных объекта в модуле Human Resources | Имя метаданных объекта в Common Data Service | Основание |
|---|---|---|---|
| cdm_jobfunction - Функциональные обязанности                                |                                   | cdm_jobfunction                  | |
| cdm_jobtypes - Типы должностей                                      |                                   | cdm_jobtypes                     | |
| cdm_jobs - Должности                                               |                                   | cdm_jobs                         | |
| cdm_jobs - Сведения о должности                                        |                                   | cdm_jobs                         | |
| cdm_positiontype - PositionType                               | HcmPositionTypeEntity             | cdm_positiontype                 | |
| cdm_jobpositions - Базовая должность                              | HcmPositionBaseEntity             | cdm_jobposition                  | См. [примечание 1](#hr-notes). |
| cdm_jobposition - Сведения о должности                            | HcmPositionDetailEntity           | cdm_jobposition                  | См. [примечание 1](#hr-notes). |
| cdm_jobposition - Период должности                           | HcmPositionDurationEntity         | cdm_jobposition                  | См. [примечание 1](#hr-notes). |
| cdm_jobposition - Иерархии должностей                        | HcmPositionHierarchyEntity        | cdm_jobposition                  | См. [примечание 1](#hr-notes). |
| cdm_veteranstatus - Статус ветерана                            |                                   | cdm_veteranstatus                | |
| cdm_ethnicorigin - Этническое происхождение                              |                                   | cdm_ethnicorigin                 | |
| cdm_languagecode - Код языка                              |                                   | cdm_languagecode                 | |
| cdm_worker - Работник                                           | HcmWorkerEntity                   | cdm_worker                       | |
| cdm_employments - Трудовая деятельность                                 |                                   | cdm_employments                  | |
| cdm_employments - Сведения о трудоустройстве                           |                                   | cdm_employments                  | |
| cdm_positionworkerassignmentmaps - Назначение работника на должность | HcmPositionWorkerAssignmentEntity | cdm_positionworkerassignmentmaps | См. [примечание 2](#hr-notes).|

### <a name="mapping-specific-notes"></a><a id='hr-notes'></a>Примечания, связанные с сопоставлениями

1. Один объект Common Data Service сопоставляется нескольким объектам приложения Finance and Operations.
2. У этого сопоставления имеется ссылка на себя.

## <a name="asset-management-entities"></a>Объекты управления активами

Следующие объекты для управления активами для Dynamics 365 Supply Chain Management указаны в том в порядке, в каком их следует включать.

| Имя сопоставления на странице двойной записи | Имя метаданных объекта в управлении активами | Имя метаданных объекта в Common Data Service | Основание |
|---|---|---|---|
| FO.AssetManagementAssetLifecycleStates--Common Data Service.msdyn_assetlifecyclestates                           | Состояния жизненного цикла актива в управлении активами               | msdyn_assetlifecyclestates               | |
| FO.AssetManagementAssetLifecycleModels--Common Data Service.msdyn_assetlifecyclemodels                           | Модели жизненного цикла актива в управлении активами               | msdyn_assetlifecyclemodels               | |
| FO.AssetManagementFunctionalLocationLifecycleModels--Common Data Service.msdyn_functionallocationlifecyclemodels | Модели жизненного цикла функционального местоположения управления активами | msdyn_functionallocationlifecyclemodels  | |
| FO.AssetManagementFunctionalLocationLifecycleStates--Common Data Service.msdyn_functionallocationlifecyclestates | Состояния жизненного цикла функционального местоположения управления активами | msdyn_functionallocationlifecyclestates  | |
| FO.AssetManagementAssetTypes--Common Data Service.msdyn_customerassetcategories                                  | Типы активов управления активами                          | msdyn_customerassetcategories            | |
| FO.AssetManagementFunctionalLocationTypes--Common Data Service.msdyn_functionallocationtypes                     | Типы функциональных местоположений управления активами            | msdyn_functionallocationtypes            | |
| FO.AssetManagementFunctionalLocations--Common Data Service.msdyn_functionallocations                             | Функциональные местоположения управления активами                 | msdyn_functionallocations                | См. [примечание](#am-notes). |
| FO.AssetManagementAssets--Common Data Service.msdyn_customerassets                                               | Активы управления активами                               | msdyn_customerassets                     | См. [примечание](#am-notes). |
| FO.AssetManagementManufacturers--Common Data Service.msdyn_manufacturers                                         | Производители управления активами                        | msdyn_manufacturers                      | |
| FO.AssetManagementModels--Common Data Service.msdyn_models                                                       | Модели управление активами                               | msdyn_models                             | |
| FO.AssetManagementWarranty--Common Data Service.msdyn_warranties                                                 | Гарантия управления активами                             | msdyn_warranties                         | |

### <a name="mapping-specific-notes"></a><a id='am-notes'></a>Примечания, связанные с сопоставлениями

- Из-за наличия самозависимости может потребоваться выполнить начальную синхронизацию несколько раз.
