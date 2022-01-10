---
title: Разделенный пакет оркестрации приложений с двойной записью
description: Пакет оркестрации приложений с двойной записью больше не является единственным пакетом, но разделяется на более мелкие пакеты. В этой теме описываются решения и сопоставления, которые содержит каждый пакет, и его зависимости от других пакетов.
author: RamaKrishnamoorthy
ms.date: 11/29/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.custom: separate-solution
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-11-29
ms.openlocfilehash: 3fe1b7707df72927fba78ee9659502cc62471799
ms.sourcegitcommit: 70ac76be31bab7ed5e93f92f4683e65031fbdf85
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/16/2021
ms.locfileid: "7924874"
---
# <a name="separated-dual-write-application-orchestration-package"></a>Разделенный пакет оркестрации приложений с двойной записью

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Ранее в составе единого пакета оркестрации приложений с двойной записью был один пакет, содержащий следующие решения:

- Заметки Dynamics 365
- Общая привязка Dynamics 365 Finance and Operations
- Сопоставления сущностей двойной записи Dynamics 365 Finance and Operations
- Приложение управления активами Dynamics 365
- Управление активами Dynamics 365
- Общие HCM
- Dynamics 365 Supply Chain Extended
- Dynamics 365 Finance Extended
- Dynamics 365 Finance and Operations Common
- Компания Dynamics 365
- Валютные курсы
- Field Service Common

Поскольку это был единый пакет, этот пакет создал ситуацию "все или ничего" для клиентов. Однако корпорация Microsoft теперь разделила его на более мелкие пакеты. Таким образом, клиент может выбрать только пакеты для необходимых решений. Например, если вы клиенты Microsoft Dynamics 365 Supply Chain Management, а не требуется интеграция с Dynamics 365 Human Resources, заметками и управлением активами, вы можете исключить эти решения из установленных решений. Так как лежащие в основе имена решений, издатели и версии сопоставлений остаются одинаковыми, это изменение не является критическим. Существующие установки будут обновлены.

![Разделенный пакет.](media/separated-package-1.png)

В этой теме описываются решения и сопоставления, которые содержит каждый пакет, и его зависимости от других пакетов.

## <a name="dual-write-application-core"></a>Базовые приложения с двойной записью

Пакет базовых приложений с двойной записью позволяет пользователям устанавливать и настраивать двойную запись без участия каких-либо приложений для взаимодействия с клиентами. В нем содержится следующие пять решений.

| Уникальное имя                           | Отображаемое имя                               |
|---------------------------------------|--------------------------------------------|
| Dynamics365Company                    | Компания Dynamics 365                       |
| Dynamics365FinanceAndOperationsCommon | Dynamics 365 Finance and Operations Common |
| CurrencyExchangeRates                 | Валютные курсы                    |
| msdyn_DualWriteAppCoreMaps            | Сопоставления сущностей базовых приложений с двойной записью   |
| msdyn_DualWriteAppCoreAnchor          | Привязка базовых приложений с двойной записью        |

Следующие сопоставления доступны в этом пакете.

| Приложения Finance and Operations     | Приложения для взаимодействия с клиентами                    |
|---------------------------------|---------------------------------------------|
| Операционная единица                  | msdyn_internalorganizations                 |
| Организационная иерархия          | msdyn_internalorganizationhierarchies       |
| Юридические лица                  | msdyn_internalorganizations                 |
| Юридические лица                  | cdm_companies                               |
| Цели организационной иерархии | msdyn_internalorganizationhierarchypurposes |
| Пара валют валютного курса     | msdyn_currencyexchangeratepairs             |
| Аффиксы имен                    | msdyn_nameaffixes                           |
| Тип валютного курса              | msdyn_exchangeratetypes                     |
| Валютные курсы CDS              | msdyn_currencyexchangerates                 |
| Тип организационной иерархии     | msdyn_internalorganizationhierarchytypes    |
| Валюты                      | transactioncurrencies                       |
| Объект руководства по смешанной реальности     | msmrw_guides                                |

**Сведения о зависимостях**

Пакет базовых приложений с двойной записью не имеет зависимостей от других пакетов.

## <a name="dual-write-human-resources"></a>Human Resources с двойной записью

Пакет Human Resources с двойной записью содержит решения и сопоставления, необходимые для синхронизации данных Human Resources. В нем содержится следующие три решения.

| Уникальное имя                | Отображаемое имя                             |
|----------------------------|------------------------------------------|
| HCMCommon                  | Общие HCM                               |
| msdyn_Dynamics365HCMMaps   | Сопоставления сущностей Dynamics 365 Human Resources |
| msdyn_Dynamics365HCMAnchor | Привязка Dynamics 365 Human Resources      |

Следующие сопоставления доступны в этом пакете.

| Приложения Finance and Operations | Приложения для взаимодействия с клиентами         |
|-----------------------------|----------------------------------|
| Этническое происхождение              | cdm_ethnicorigins                |
| Функция задания компенсации   | cdm_jobfunctions                 |
| Должности V2                | cdm_jobpositions                 |
| Должности                        | cdm_jobs                         |
| Тип задания по компенсации       | cdm_jobtypes                     |
| Коды языков              | cdm_languages                    |
| Тип должности               | cdm_positiontypes                |
| Назначения работника должностям | cdm_positionworkerassignmentmaps |
| Статус ветерана              | cdm_veteranstatuses              |
| Рабочий                      | cdm_workers                      |
| Занятость по компании      | cdm_employments                  |

**Сведения о зависимостях**

Пакет Human Resources с двойной записью зависит от пакета базовых приложений с двойной записью. Поэтому необходимо установить пакет базовых приложений с двойной записью до установки пакета Human Resources с двойной записью.

## <a name="dual-write-supply-chain"></a>Supply Chain с двойной записью

Пакет Supply Chain с двойной записью содержит решения и сопоставления, необходимые для синхронизации данных Supply Chain Management. В нем содержится следующие три решения.

| Уникальное имя                                | Отображаемое имя                                              |
|--------------------------------------------|-----------------------------------------------------------|
| Dynamics365SupplyChainExtended             | Dynamics 365 Supply Chain Extended                        |
| msdyn_Dynamics365SupplyChainExtendedMaps   | Сопоставления расширенных сущностей Dynamics 365 Supply Chain Management |
| msdyn_Dynamics365SupplyChainExtendedAnchor | Расширенная привязка Dynamics 365 Supply Chain Management      |

Следующие сопоставления доступны в этом пакете.

| Приложения Finance and Operations                 | Приложения для взаимодействия с клиентами                      |
|---------------------------------------------|-----------------------------------------------|
| Единицы измерения                                       | uoms                                          |
| Заголовки заказов на продажу CDS                     | salesorders                                   |
| Строки заказа на продажу CDS                       | salesorderdetails                             |
| Заголовок предложения по продаже CDS                  | предложения                                        |
| Строки предложения по продаже CDS                   | quotedetails                                  |
| Уникально идентифицируемые продукты, выпущенные CDS              | продукты                                      |
| Зоны склада                             | msdyn_warehousezones                          |
| Группы зон склада                       | msdyn_warehousezonegroups                     |
| Строки работы склада                        | msdyn_warehouseworklines                      |
| Заголовки работы склада                      | msdyn_warehouseworkheaders                    |
| Склады                                  | msdyn_warehouses                              |
| Складской проход                             | msdyn_warehouseaisles                         |
| Пересчеты единиц измерения                            | msdyn_unitofmeasureconversions                |
| Условия поставки                           | msdyn_termsofdeliveries                       |
| Способы поставки                           | msdyn_shipvias                                |
| Стили шаблонов продуктов                       | msdyn_sharedproductstyles                     |
| Строки накладной заказа на продажу V2                      | invoicedetails                                |
| Заголовки накладной заказа на продажу V2                    | накладные                                      |
| Размеры шаблонов продуктов                        | msdyn_sharedproductsizes                      |
| Выпущенные продукты V2                        | msdyn_sharedproductdetails                    |
| Конфигурации шаблонов продуктов               | msdyn_sharedproductconfigurations             |
| Цвета шаблонов продуктов                       | msdyn_sharedproductcolors                     |
| Коды происхождения заказов на продажу                    | msdyn_salesorderorigins                       |
| Заголовок поступления продуктов                      | msdyn_purchaseorderreceipts                   |
| Строка поступления продуктов                        | msdyn_purchaseorderreceiptproducts            |
| Заголовки заказов на покупку V2                   | msdyn_purchaseorders                          |
| Предварительно удаленный объект строки заказа на покупку CDS | msdyn_purchaseorderproducts                   |
| Объект строки заказа на покупку CDS              | msdyn_purchaseorderproducts                   |
| Группы аналитик отслеживания                   | msdyn_producttrackingdimensiongroups          |
| Стили                                      | msdyn_productstyles                           |
| Группы аналитик хранения                    | msdyn_productstoragedimensiongroups           |
| Преобразования единиц измерения для определенного продукта           | msdyn_productspecificunitofmeasureconversions |
| Параметры заказа продуктов по умолчанию V2           | msdyn_productspecificdefaultordersettings     |
| Размеры                                       | msdyn_productsizes                            |
| Группы аналитик продукта                    | msdyn_productdimensiongroups                  |
| Параметры заказа по умолчанию                      | msdyn_productdefaultordersettings             |
| Конфигурации                              | msdyn_productconfigurations                   |
| Все продукты                                | msdyn_globalproducts                          |
| Цвета                                      | msdyn_productcolors                           |
| Роли иерархии категорий продуктов            | msdyn_productcategoryhierarchyroles           |
| Иерархии категорий продуктов                | msdyn_productcategoryhierarchies              |
| Назначения категорий продуктов                | msdyn_productcategoryassignments              |
| Категории продуктов                          | msdyn_productcategories                       |
| Местонахождения складов                         | msdyn_inventorylocations                      |
| Запасы CDS в                            | msdyn_inventoryonhandentries                  |
| Категории продуктов                          | msdyn_productcategories                       |
| Запасы CDS в                            | msdyn_inventoryonhandrequests                 |
| Штрихкод, связанный с номером продукта           | msdyn_productbarcodes                         |
| Карта лояльности                                | msdyn_loyaltycards                            |
| Баллы поощрения по программе лояльности                       | msdyn_loyaltyrewardpoints                     |
| Ценовые группы клиентов                       | msdyn_pricecustomergroups                     |
| Сайты                                       | msdyn_operationalsites                        |
| Строки предложения по продаже CDS                   | quotedetails                                  |
| Строки заказа на продажу CDS                       | salesorderdetails                             |

**Сведения о зависимостях**

Пакет Supply Chain с двойной записью зависит от следующих трех пакетов. Поэтому перед установкой пакета Supply Chain с двойной записью следует установить эти пакеты.

- Пакет базовых приложений с двойной записью
- Пакет Finance с двойной записью
- Пакет Human Resources с двойной записью

## <a name="dual-write-finance"></a>Finance с двойной записью

Пакет Finance с двойной записью содержит решения и сопоставления, необходимые для синхронизации данных Dynamics 365 Finance. В нем содержится следующие четыре решения.

| Уникальное имя                            | Отображаемое имя                               |
|----------------------------------------|-------------------------------------------|
| Dynamics365FinanceExtended             | Dynamics 365 Finance Extended             |
| msdyn_Dynamics365FinanceExtendedMaps   | Сопоставления сущностей Dynamics 365 Finance Extended |
| FieldServiceCommon                     | Field Service Common                      |
| msdyn_Dynamics365FinanceExtendedAnchor | Привязка Dynamics 365 Finance Extended      |

Следующие сопоставления доступны в этом пакете.

| Приложения Finance and Operations             | Приложения для взаимодействия с клиентами        |
|-----------------------------------------|---------------------------------|
| Группы подоходного налога                  | msdyn_withholdingtaxgroups      |
| Контакты CDS V2 (Клиент)              | контакты                        |
| Контакты CDS V2 (поставщик)                | контакты                        |
| Клиенты V3                            | контакты                        |
| Коды подоходного налога                   | msdyn_withholdingtaxcodes       |
| Поставщики V2                              | msdyn_vendors                   |
| Метод платежа поставщикам                   | msdyn_vendorpaymentmethods      |
| Группы поставщиков                           | msdyn_vendorgroups              |
| План счетов                       | msdyn_chartofaccountses         |
| Группы разноски ГК для налога V2      | msdyn_taxpostinggroups          |
| Налоговая группа номенклатур                    | msdyn_taxitemgroups             |
| Налоговые группы                        | msdyn_taxgroups                 |
| CDS объекта кода налогового освобождения        | msdyn_taxexemptcodes            |
| Группы клиентов                         | msdyn_customergroups            |
| Способ оплаты клиента                 | msdyn_customerpaymentmethods    |
| Финансовые аналитики                    | msdyn_dimensionattributes       |
| Налоговые органы                   | msdyn_taxauthorities            |
| Формат финансовой аналитики              | msdyn_financialdimensionformats |
| Период финансового календаря                  | msdyn_fiscalcalendarperiods     |
| Объект интеграции финансового календаря      | msdyn_fiscalcalendars           |
| Объект интеграции года финансового календаря | msdyn_fiscalcalendaryears       |
| Условия оплаты                        | msdyn_paymentterms              |
| График оплаты                        | msdyn_paymentschedules          |
| Строки графика платежей                  | msdyn_paymentschedulelines      |
| Платежные дни CDS                        | msdyn_paymentdays               |
| Строки платежных дней CDS V2                | msdyn_paymentdaylines           |
| Счет ГК                            | msdyn_mainaccounts              |
| Категории счета ГК                 | msdyn_mainaccountcategories     |
| Ledger                                  | msdyn_ledgers                   |
| Клиенты V3                            | счета                        |

**Сведения о зависимостях**

Пакет Finance с двойной записью зависит от пакета базовых приложений с двойной записью. Поэтому необходимо установить пакет базовых приложений с двойной записью до установки пакета Finance с двойной записью.

## <a name="dual-write-notes"></a>Заметки с двойной записью

Пакет заметок с двойной записью содержит решения и сопоставления, необходимые для синхронизации данных заметок или аннотаций. В нем содержится следующие четыре решения.

| Уникальное имя                  | Отображаемое имя                   |
|------------------------------|--------------------------------|
| Dynamics365Notes             | Заметки Dynamics 365             |
| Dynamics365NotesExtended     | Расширенные заметки Dynamics 365    |
| msdyn_Dynamics365NotesMaps   | Сопоставления сущностей заметок Dynamics 365 |
| msdyn_Dynamics365NotesAnchor | Привязка заметок Dynamics 365      |

Следующие сопоставления доступны в этом пакете.

| Finance and Operations                     | Customer Engagement |
|--------------------------------------------|---------------------|
| Вложения документа заголовка заказа на продажу    | аннотации         |
| Вложения клиента                       | аннотации         |
| Вложения документов поставщика                | аннотации         |
| Вложения документа заголовка заказа на покупку | аннотации         |

**Сведения о зависимостях**

Пакет заметок с двойной записью зависит от следующих двух пакетов. Поэтому перед установкой пакета заметок с двойной записью следует установить эти пакеты.

- Пакет базовых приложений с двойной записью
- Пакет Finance с двойной записью

## <a name="dual-write-asset-management"></a>Управления активами с двойной записью

Пакет управления активами с двойной записью содержит решения и сопоставления, необходимые для синхронизации данных активов из Supply Chain Management или Dynamics 365 Field Service. В нем содержится следующие четыре решения.

| Уникальное имя                          | Отображаемое имя                              |
|--------------------------------------|-------------------------------------------|
| Dynamics365AssetManagement           | Управление активами Dynamics 365             |
| Dynamics365AssetManagementApp        | Приложение управления активами Dynamics 365          |
| msdyn_DualWriteAssetManagementMaps   | Сопоставления сущностей управления активами Dynamics 365 |
| msdyn_DualWriteAssetManagementAnchor | Привязка управления активами Dynamics 365      |

Следующие сопоставления доступны в этом пакете.

| Приложения Finance and Operations                           | Приложения для взаимодействия с клиентами                |
|-------------------------------------------------------|-----------------------------------------|
| Гарантия управления активами                             | msdyn_warranties                        |
| Модели управление активами                               | msdyn_models                            |
| Производители управления активами                        | msdyn_manufacturers                     |
| Типы функциональных местоположений управления активами            | msdyn_functionallocationtypes           |
| Функциональные местоположения управления активами                 | msdyn_functionallocations               |
| Состояния жизненного цикла функционального местоположения управления активами | msdyn_functionallocationlifecyclestates |
| Модели жизненного цикла функционального местоположения управления активами | msdyn_functionallocationlifecyclemodels |
| Активы управления активами                               | msdyn_customerassets                    |
| Типы активов управления активами                          | msdyn_customerassetcategories           |
| Состояния жизненного цикла актива в управлении активами               | msdyn_assetlifecyclestates              |
| Модели жизненного цикла актива в управлении активами               | msdyn_assetlifecyclemodels              |

**Сведения о зависимостях**

Пакет управления активами с двойной записью зависит от пакета базовых приложений с двойной записью. Поэтому необходимо установить пакет базовых приложений с двойной записью до установки пакета управления активами с двойной записью.

## <a name="packages-required-for-project-operations"></a>Пакеты, необходимые для Project Operations
Project Operations зависит от следующих пакетов. Поэтому перед установкой Project Operations следует установить эти пакеты.

- Пакет базовых приложений с двойной записью
- Пакет Finance с двойной записью
- Пакет Supply Chain с двойной записью
- Пакет управления активами с двойной записью
- Пакет Human Resources с двойной записью
