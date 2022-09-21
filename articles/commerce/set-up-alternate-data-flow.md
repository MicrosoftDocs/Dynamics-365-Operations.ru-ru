---
title: Настройка альтернативного потока данных для рекомендаций
description: В этой статье описывается, как настроить среду, используя альтернативный поток данных, чтобы предоставить данные службе рекомендаций.
author: bebeale
ms.date: 09/08/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: b507b9bb57c68aca9424b53f8ccc009efea733bc
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460168"
---
# <a name="set-up-an-alternate-dataflow-for-recommendations"></a>Настройка альтернативного потока данных для рекомендаций

[!include [banner](includes/banner.md)]

В этой статье описывается, как настроить среду, используя альтернативный поток данных, чтобы предоставить данные службе рекомендаций.

## <a name="comparison-of-out-of-the-box-dataflow-with-alternate-dataflow"></a>Сравнение изначального потока данных с альтернативным потоком данных

На следующем рисунке показан изначальный поток данных в среде.

![Изначальный поток данных в среде](media/reco-out-of-the-box-dataflow-2.png)

На рисунке ниже показан альтернативный поток данных, в котором пакетное задание синхронизации хранилищ сущностей заменяется шагами альтернативного потока данных.

![Альтернативный поток данных в среде](media/reco-alternate-dataflow-2.png)

## <a name="assumptions"></a>Предпосылки

- В этой статье предполагается, что вы уже включили службу рекомендаций для своей среды. Для получения дополнительных сведений см. раздел [Включение рекомендаций по продуктам](enable-product-recommendations.md).
- При работе с файлами и папками в учетной записи Microsoft Azure Data Lake Storage:

    - Можно воспользоваться интерфейсом веб-портала Azure или приложением Обозреватель службы хранилища Azure.
    - Начальными точками для работы с файлами и папками являются контейнер **dynamics365-financeandoperations**, расположенный в папке, названной в соответствии с URL-адресом среды.
    - Если имя среды песочницы — **MyUAT**, базовый URL-адрес среды будет `myuat.sandbox.operations.dynamics.com`.
    - Если к одной учетной записи хранения подключено несколько сред, каждая среда будет иметь собственную корневую папку.

## <a name="prerequisites"></a>Необходимые условия

Чтобы можно применить подход с альтернативным потоком данных, необходимо выполнить следующие предварительные требования.

### <a name="set-up-microsoft-power-platform"></a>Настройка Microsoft Power Platform

Для настройки Microsoft Power Platform следуйте инструкциям в разделе [Включение интеграции Microsoft Power Platform](../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md).

### <a name="install-the-export-to-data-lake-add-in"></a>Установка надстройки экспорта в Data Lake

Чтобы установить надстройку экспорт в Data Lake, следуйте указаниям в разделе [Установка надстройки экспорта в Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

> [!NOTE]
> Обратите внимание на значения конфигурации, так как они понадобятся для выполнения некоторых шагов, описанных ниже.

### <a name="configure-tables-to-export-in-dynamics-365"></a>Настройка таблиц для экспорта в Dynamics 365

Настройки синхронизации таблиц из Dynamics 365 в Azure Data Lake Storage выполняется на странице **Экспорт в Data Lake**. Так как страница в данный момент не имеет пункта меню, ее могут открыть только пользователи, имеющие роль безопасности **системного администратора**.

Чтобы настроить таблицы для экспорта в Dynamics 365, выполните следующие действия.

1. Чтобы открыть страницу **Экспорт в Data Lake**, добавьте строку `?mi=DataFeedsDefinitionWorkspace` к основному URL-адресу среды, как показано в следующем примере:

    `https://<environment-URL>/?mi=DataFeedsDefinitionWorkspace`

1. На странице **Экспорт в Data Lake** скопируйте таблицы, перечисленные в разделе [Список таблиц куба RetailSales](#list-of-retailsales-cube-tables) данной статьи.
1. В столбце **Имя системы** разверните список параметров фильтра.
1. Выберите тип фильтра **один из**. Затем поместите курсор в текстовое поле и вставьте список таблиц, скопированный со страницы **Экспорт в Data Lake**.
1. В нижней части списка параметров фильтра выберите **Применить**.
1. Выберите все строки в сетке, а затем выберите **Активировать**.

> [!NOTE]
> Прежде чем перейти к следующему шагу, все строки должны быть обновлены до статуса **Выполнение**. При необходимости выполните устранение неполадок и устраните необходимые ошибки.

### <a name="create-a-synapse-workspace"></a>Создание рабочей области Synapse

Чтобы создать рабочую область Synapse, если она еще не создана, следуйте указаниям в разделе [Быстрое начало: создание рабочей области Synapse](/azure/synapse-analytics/quickstart-create-workspace).

Чтобы упорядочить ресурсы Azure, рекомендуется поместить учетную запись Data Lake Storage и рабочую область Synapse вместе в группу ресурсов в Azure. Можно повторно использовать учетную запись хранения, созданную при установке надстройки Экспорт в Data Lake.

## <a name="create-a-database-in-synapse-for-recommendation-data-processing"></a>Создание базы данных в Synapse для обработки данных рекомендаций

Используйте консольное приложение Common Data Model (CDMUtil_ConsoleApp) для создания базы данных в рабочей области Synapse и заполнения ее данными из таблиц Common Data Model в Data Lake Storage. Рекомендуется использовать служебную программу Common Data Model с базой данных в среде разработки, если имеются какие-либо расширения.

> [!NOTE]
> В шагах ниже предполагается, что данные расширения не добавляются в куб RetailSales.

Выполните следующие действия для создания базы данных в Synapse.

1. Перейдите на страницу [Dynamics-365-FastTrack-Implementation-Assets GitHub](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Analytics/CDMUtilSolution#2-cdmutil-console-app) и выполните необходимые действия, чтобы скачать файл **CDMUtilConsoleApp.zip**.
1. Распакуйте ZIP-файл в локальную папку.
1. Откройте файл **CDMUtil_ConsoleApp.dll.config** в текстовом редакторе и измените следующие значения:

    1. Задайте значение **Tenant ID** (идентификатор клиента Azure).
    1. Задайте значение **Access key** (ключ доступа для учетной записи хранения Data Lake).

        1. На портале Azure откройте свою учетную запись хранения.
        1. В меню в левой части страницы выберите **Ключи доступа**.
        1. В верхней части страницы выберите **Показать ключи**.
        1. Нажмите кнопку копирования для одного из двух полей с ключами, а затем вставьте значение между двойными кавычками в файле конфигурации.

    1. Задайте значение **ManifestURL** согласно URL-адресу вашего файла **Tables.manifest.cdm.json** в Azure Data Lake Storage. Чтобы получить URL-адрес, перейдите к файлу на портале Azure, выберите многоточие (**...**) в правой части представления, а затем выберите **Свойства**. URL-адрес является первым свойством, которое отображается на вкладке **Обзор**.
    1. Установите значение **TargetDbConnectionString**, равное строке подключения для встроенного бессерверного пула SQL вашей рабочей области Synapse.

        1. В рабочей области Synapse выберите вкладку **Управление**.
        1. В подменю выберите **Пулы SQL**.
        1. Выберите имя **Встроенный** , чтобы просмотреть свойства пула.
        1. В диалоговом окне свойств выберите тип подключения к ADO.NET, который необходимо использовать. Затем скопируйте значение строки подключения и вставьте его между двойными кавычками в файле конфигурации.

        > [!NOTE]
        > Необходимо иметь разрешение на создание баз данных. Для простоты использования вы можете использовать встроенную учетную запись администратора **sqladminuser**.

    1. Удалите метки комментария с узла **ProcessEntities** и задайте для него значение **true** (например, `<add key="ProcessEntities" value ="true"/>`).

1. Сохраните и закройте файл **CDMUtil_ConsoleApp.dll.config**.
1. Скопируйте файл **EntityList.json** в каталог **/Manifest**.
1. В окне командной строки выполните **cdmutil_consoleapp.exe**.

> [!NOTE]
> При просмотре выходных данных должно быть 35 объектов/представлений, по меньшей мере 75 таблиц и не должно быть ошибок.

## <a name="prepare-the-data-lake-retailsales-aggregate-measurements-directory"></a>Подготовка каталога агрегированных измерений Data Lake RetailSales

### <a name="back-up-your-current-retailsales-cube-data-from-data-lake-storage"></a>Резервное копирование текущих данных куба RetailSales из Data Lake Storage

Самым простым способом резервного копирования текущих данных куба RetailSales является переименование каталога **RetailSales** в Data Lake Storage **RetailSales-backup** или что-то подобное. Этот метод сохраняет существующие данные в случае дальнейшего устранения неполадок.

Папку куба **/RetailSales** можно найти в следующем местоположении:

`<storage-account>/dynamics365-financeandoperations/<environment-url (for example, myuat.sandbox.operations.dynamics.com)>/AggregateMeasurements/RetailSales`

### <a name="create-a-new-retailsales-folder-and-upload-the-model-file"></a>Создание новой папки RetailSales и отправка файла модели

Чтобы создать новый каталог **RetailSales** и отправить файл **model.json** в Data Lake Storage, выполните следующие действия.

1. Создайте новый пустой каталог на том же уровне, что и предыдущий каталог, и назовите его **RetailSales**.
1. Отправьте файл **model.json** в этот новый каталог.

## <a name="create-a-pipeline-to-copy-the-retailsales-cube-data"></a>Создание конвейера для копирования данных куба RetailSales

Конвейер будет считывать представления куба RetailSales и экспортировать данные в файлы CSV в Data Lake Storage.

Для создания конвейера для копирования данных куба RetailSales выполните следующие действия.

1. В рабочей области Synapse выберите вкладку **Интеграция**.
1. Выберите знак плюса (**+**), а затем выберите **Импорт из шаблона конвейера**.
1. Скачайте и затем выберите файл [ExportRetailSalesCubeViews.zip](https://aka.ms/reco-alternate-dataflow-files).
1. Выберите свою связанную службу базы данных SQL.
1. Выберите свою связанную службу учетной записи хранения.
1. Откройте инструмент **Копирование данных** и измените свойство **Путь к папке** на **\<environment_name\>/...**.

### <a name="test-execution-of-the-pipeline"></a>Тестовый запуск конвейера

Рекомендуется тестировать конвейер, используя только одно представление. Представление **RetailSales_RetailMediaTemplateView** хорошо подходит, так как обычно содержит менее 10 строк.

## <a name="schedule-the-pipeline-to-run-on-a-recurring-schedule"></a>Планирование запуска конвейера по регулярному расписанию

При каждом запуске конвейера происходит потребление ресурсов Azure. Рекомендуется планировать запуск с интервалом в 48 часов или дольше. Вы всегда можете запустить конвейер вручную, если необходимо немедленно синхронизировать данные. 
 
## <a name="table-list-for-synchronization-from-dynamics-365-to-data-lake-storage"></a>Список таблиц для синхронизации из Dynamics 365 с Data Lake Storage

Следующий список таблиц является подмножеством всех таблиц, которые необходимы для всего куба RetailSales. Служба рекомендаций использует только 15 представлений в кубе RetailSales, и список требуемых таблиц был отфильтрован соответствующим образом.

### <a name="list-of-retailsales-cube-tables"></a>Список таблиц куба RetailSales

- BICalendarOffsets
- BIDateDimension
- BIDateDimensionValue
- Каталог
- CatalogProduct
- CatalogProductCategory
- CustInvoiceJour
- CustInvoiceTrans
- CustTable
- DataArea
- DimensionAttributeValueCombination
- DimensionAttributeValueSet
- DirPartyTable
- EcoResCategory
- EcoResCategoryHierarchy
- EcoResCategoryHierarchyRole
- EcoResColor
- EcoResConfiguration
- EcoResProduct
- EcoResProductCategory
- EcoResProductTranslation
- EcoResSize
- EcoResStyle
- HcmWorker
- InventDim
- InventDimCombination
- InventItemGroup
- InventItemGroupItem
- InventItemSetupSupplyType
- InventTable
- InventTrans
- LogisticsAddressCountryRegion
- LogisticsAddressCountryRegionTranslation
- LogisticsLocation
- LogisticsPostalAddress
- OMHIERARCHYPURPOSE
- RetailAssortmentLookup
- RetailAssortmentLookupChannelGroup
- RetailChannelProfile
- RetailChannelProfileProperty
- RetailChannelTable
- RetailChannelTableExt
- RetailConnDatabaseProfile
- RetailCustInvoiceJourTable
- RetailCustTable
- RetailMediaTemplate
- RetailOfflineProfile
- RetailPeriodicDiscount
- RetailRecoListConfigurationParameters
- RetailSalesTaxOverrideGroup
- RetailSharedParameters
- RetailSpecialCategoryMember
- RetailTenderTypeCardTable
- RetailTenderTypeTable
- RetailTerminalTable
- RetailTmpProductMedia
- RetailTransactionDiscountTrans
- RetailTransactionPaymentTrans
- RetailTransactionPaymentTransExt
- RetailTransactionSalesTrans
- RetailTransactionSalesTransExt
- RetailTransactionTable
- SalesLine
- SalesTable
- SystemParameters
- RETAILCATALOGINTERNALORG
- RETAILGROUPMEMBERLINE
- RETAILINTERNALORGANIZATION
- RETAILSPECIALCATEGORYPRODUCT
- RETAILPRODUCTCATEGORY
- ECORESCONFIGURATION
- DIMENSIONATTRIBUTE
- DIMENSIONATTRIBUTEVALUESET
- DIMENSIONHIERARCHY
- DIMENSIONHIERARCHYINTEGRATION
- DIMENSIONHIERARCHYLEVEL
- DIMENSIONPARAMETER
- OMExplodedOrganizationSecurityGraph

### <a name="view-list-for-the-parameter-to-pass-to-the-synapse-pipeline"></a>Список представлений для параметра, передаваемого в конвейере Synapse

Следующий список с разделителями-запятыми содержит представления куба RetailSales, над которыми конвейер выполнит операцию "select". Затем результаты будут скопированы в Data Lake Storage.

RetailSales_RetailAssortmentRulesView,RetailSales_RetailChannelNavigationHierarchiesView,RetailSales_RetailChannelNavigationHierarchyCatalogProductsView,RetailSales_RetailChannelNavigationHierarchyCategoryNodesView,RetailSales_RetailChannelNavigationHierarchyCategoryProductsView,RetailSales_RetailMediaBaseUrlChannelView,RetailSales_RetailMediaRelativeUrlProductView,RetailSales_RetailMediaTemplateView,RetailSales_RetailOptOutCustomersView,RetailSales_RetailProductCategory,RetailSales_RetailProductTransaction,RetailSales_RetailProductVariantDimensionsView,RetailSales_RetailRecoListConfigurationParametersView,RetailSales_RetailRecoListsSharedParametersView,RetailSales_RetailEcoResProductTranslation

> [!IMPORTANT]
> Параметром конвейера должен быть список имен представлений, разделенных одной запятой. Не должно быть пробелов или символов перевода строки.

## <a name="environment-specific-fixes"></a>Исправления для определенной среды

### <a name="retailchannelview-fix"></a>Исправление RETAILCHANNELVIEW

Представление **RETAILCHANNELVIEW** содержит жестко закодированное целое число, представляющее организацию типа "канал розничной торговли". Фактическое значение типа может изменяться от среды к среде или от клиента к клиенту.

```SQL
CREATE OR ALTER   VIEW [dbo].[RETAILCHANNELVIEW]
AS
SELECT T1.RECID AS RECID1,
       T1.STOREAREA AS STOREAREA,
       T1.OMOPERATINGUNITID AS OMOPERATINGUNITID,
       T1.DEFAULTCUSTACCOUNT AS DEFAULTCUSTOMER,
       T1.RETAILCHANNELID AS RETAILCHANNELID,
       T1.CHANNELTYPE AS CHANNELTYPE,
       T1.PARTITION AS PARTITION,
       T1.RECID AS RECID,
       T2.OMOPERATINGUNITNUMBER AS OMOPERATINGUNITNUMBER,
       T3.NAME AS NAME
FROM   dbo.RETAILCHANNELTABLE AS T1 CROSS JOIN dbo.DIRPARTYTABLE AS T2 CROSS JOIN dbo.DIRPARTYTABLE AS T3
WHERE  ((((T1.OMOPERATINGUNITID = T2.RECID)
          )
         AND ((T2.RECID = T3.RECID)
              ))
        AND T2.INSTANCERELATIONTYPE IN (8363));
```

Чтобы изменить жестко закодированное целое число, выполните следующие действия.

1. В Dynamics 365 проверьте значение **ChannelID** для своего интернет-канала.
1. В экземпляре SQL Server Management Studio (SSMS), прикрепленном к базе данных Synapse, выполните следующий запрос:

    ```SQL
    select INSTANCERELATIONTYPE, NAME, NAMEALIAS, * from dbo.DIRPARTYTABLE where RECID IN (select OMOPERATINGUNITID from dbo.RETAILCHANNELTABLE where RETAILCHANNELID =     <channelID>)
    ```

1. Скопируйте значение из первого столбца (**INSTANCERELATIONTYPE**) и вставьте его в определение представления.

## <a name="troubleshooting"></a>Устранение неполадок

### <a name="pipeline-task-fails"></a>Задача конвейера не выполняется

Для задачи **CopyData** должно быть 15 запусков задачи конвейера. Если какой-либо запуск завершается со сбоем, необходимо убедиться, что все зависимые объекты SQL существуют и что запросы выполняются. Самым простым способом перехода ко всем зависимостям является использование среды SSMS для подключения к базе данных. Затем можно выбрать и удерживать (или щелкнуть правой кнопкой мыши) представление и выбрать **Создать CREATE as в новом окне**.

Сообщение об ошибке может содержать следующий текст:

- Ошибка: сбой произошел на стороне "Источник"
- Ошибка обработки внешнего файла: "максимальное число ошибок".
- /RetailSales/RetailSales_xxxxxx

#### <a name="example-scenario"></a>Пример сценария

В этом примере задача **RetailSales_RetailProductCategory** завершается сбоем, и выводится сообщение об ошибке "максимальное число ошибок".

Для устранения этой ошибки выполните следующие действия.

1. Откройте файл **EntityList.json** в текстовом редакторе (например, Visual Studio Code).
1. Найдите в определении представления **RetailSales_RetailProductCategory**.

    ```SQL
    CREATE  VIEW [dbo].[RetailSales_RetailProductCategory] AS SELECT 0 AS ROW_UNIQUEKEY ,CATEGORY AS CATEGORYID ,PRODUCT AS PRODUCTID ,PRODUCTNAME ,CATEGORYNAME     ,PARENTCATEGORY AS PARENTCATEGORYID ,PARTITION ,RECID FROM RetailProductCategoryView
    ```

1. Это представление зависит только от одного другого представления: **RetailProductCategoryView** _. Найдите определение представления для _*RetailProductCategoryView**.

    ```SQL
    CREATE VIEW [DBO].[RETAILPRODUCTCATEGORYVIEW] AS SELECT T1.CATEGORY AS CATEGORY, T1.PRODUCT AS PRODUCT, T1.PARTITION AS PARTITION, T1.RECID AS RECID, T2.PRODUCTNAME AS PRODUCTNAME, T2.PARTITION AS PARTITION#2, T3.NAME AS CATEGORYNAME, T3.PARENTCATEGORY AS PARENTCATEGORY, T3.PARTITION AS PARTITION#3 FROM RETAILPRODUCTCATEGORY T1 CROSS JOIN ECORESPRODUCTTRANSLATIONS T2 CROSS JOIN RETAILCATEGORYEXPANDED T3 WHERE((( T1.PRODUCT = T2.PRODUCT) AND ( T1.PARTITION = T2.PARTITION)) AND (( T1.CATEGORY = T3.RECID) AND ( T1.PARTITION = T3.PARTITION)))
    ```

1. Это представление зависит от трех других представлений: **RETAILPRODUCTCATEGORY**, **ECORESPRODUCTTRANSLATIONS** и **RETAILCATEGORYEXPANDED**. Найдите определение для каждого из этих представлений и выведите список их зависимостей. Продолжайте, пока не будут обнаружены все зависимые представления.

    Здесь представлен весь список в виде дерева зависимостей. Необходимо проверить тринадцать представлений.

    - RetailSales_RetailProductCategory

        - RetailProductCategoryView

            - RETAILPRODUCTCATEGORY

                - ECORESPRODUCTCATEGORY
                - ECORESCATEGORYHIERARCHYROLE
                - RETAILSPECIALCATEGORYPRODUCT

                    - ECORESPRODUCT
                    - RETAILGROUPMEMBERLINE
                    - RETAILSPECIALCATEGORYMEMBER

            - ECORESPRODUCTTRANSLATIONS

                - ECORESPRODUCT
                - ECORESPRODUCTTRANSLATION
                - SYSTEMPARAMETERS

            - RETAILCATEGORYEXPANDED

                - ECORESCATEGORY
                - ECORESCATEGORYHIERARCHYROLE

1. В Excel создайте следующие 13 инструкций: **select count(\*) from \<view_name\>**. Выполните эти инструкции в SSMS и отправьте результаты в текстовый редактор. Затем просмотрите результаты, чтобы убедиться, что ни в одном представлении нет сбоев. Исходная ошибка предполагает, что по крайней мере в одном из представлений будет сбой.

    ```SQL
    select count(*) from RetailProductCategoryView
    select count(*) from RETAILPRODUCTCATEGORY
    select count(*) from ECORESPRODUCTCATEGORY
    select count(*) from ECORESCATEGORYHIERARCHYROLE
    select count(*) from RETAILSPECIALCATEGORYPRODUCT
    select count(*) from ECORESPRODUCT
    select count(*) from RETAILGROUPMEMBERLINE
    select count(*) from RETAILSPECIALCATEGORYMEMBER
    select count(*) from ECORESPRODUCTTRANSLATIONS
    select count(*) from ECORESPRODUCTTRANSLATION
    select count(*) from SYSTEMPARAMETERS
    select count(*) from RETAILCATEGORYEXPANDED
    select count(*) from ECORESCATEGORY
    ```

1. Одним из способов подтверждения того, что вы просматриваете, является создание представления, зависящего от корня, для создания определения представления в SSMS. Затем убедитесь, что имеется столбец файлов Azure Data Lake с именем **r.filepath**. Наличие этого столбца указывает на то, что просматриваемое представление считывает данные из Data Lake Storage.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор рекомендаций по продуктам](product-recommendations.md)

[Включение Azure Data Lake Storage в среде Dynamics 365 Commerce](enable-adls-environment.md)

[Включение персонализированных рекомендаций](personalized-recommendations.md)

[Включение рекомендаций "покупать похожие образы"](shop-similar-looks.md)

[Отказ от персонализированных рекомендаций](personalization-gdpr.md)

[Добавление рекомендаций по продуктам в POS](product.md)

[Добавление рекомендаций на экран проводки](add-recommendations-control-pos-screen.md)

[Корректировка результатов рекомендаций на основе искусственного интеллекта и машинного обучения](modify-product-recommendation-results.md)

[Создание контролируемых рекомендаций вручную](create-editorial-recommendation-lists.md)

[Создание рекомендаций с помощью демонстрационных данных](product-recommendations-demo-data.md)

[Вопросы и ответы по рекомендациям по продуктам](faq-recommendations.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
