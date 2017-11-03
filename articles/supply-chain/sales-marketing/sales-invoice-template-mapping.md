---
title: "Синхронизация заголовков и строк счетов продажи из Finance and Operations в Sales"
description: "В этой теме рассматриваются шаблоны и базовые задачи, которые используются для синхронизации заголовков и строк накладных по продажам из Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition с Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: fb5ba099911deda5308daf92d82cd6b3489995bf
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a>Синхронизация заголовков и строк счетов продажи из Finance and Operations в Sales

[!include[banner](../includes/banner.md)]

В этой теме рассматриваются шаблоны и базовые задачи, которые используются для синхронизации заголовков и строк накладных по продажам из Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition с Microsoft Dynamics 365 for Sales. 

## <a name="templates-and-tasks"></a>Шаблоны и задачи

Следующие шаблоны и базовые задачи используются для синхронизации заголовков и строк накладных по продажам из Finance and Operations в Sales:

- **Имя шаблона в интеграции данных** 

     - Накладные по продажам (из Fin and Ops в Sales)

- **Имена задач в проекте интеграции данных**

    - SalesInvoiceHeader
    - SalesInvoiceLine

Задачи синхронизации, которые необходимо выполнить перед синхронизацией заголовков и строк накладных по продажам:
-   Продукты (из Fin and Ops в Sales)
-   Счета (из Sales в Fin and Ops) (если используются)
-   Контакты (из Sales в Fin and Ops) (если используются)
-   Заголовки и строки накладных по продажам (из Fin and Ops в Sales)

## <a name="entity-set"></a>Набор объектов

| Finance and Operations                               | Common Data Service (CDS)              | Прод.          |
|------------------------------------------------------|------------------|----------------|
| Заголовки счетов продажи клиентам, управляемых извне | SalesInvoice     | Накладные       |
| Строки счетов продажи клиентам, управляемых извне   | SalesInvoiceLine | InvoiceDetails |

## <a name="entity-flow"></a>Поток объектов

Накладные по продажам создаются в Finance and Operations и синхронизируются в Sales.

> [!NOTE]
> Налоги, связанные с суммами в **заголовке накладной по продаже**, в настоящее время не включаются в синхронизацию из Finance and Operations в Sales. Это связано с тем, что в Sales не поддерживается налоговая информация на уровне заголовка. Налоги, связанные с суммами на уровне строки, включаются.

## <a name="prospect-to-cash-solution-for-sales"></a>Решение "Перспективный клиент в наличные деньги" для Sales

-  **Поле номера накладной** добавляется в объект **Накладная** и отображается на странице.
 
-  Кнопка **Создать накладную** на странице **Заказ на продажу** скрывается, потому что накладные будут создаваться в Finance and Operations и синхронизироваться в Sales. Страница **Накладная** недоступна для редактирования, потому что накладные будут синхронизироваться из Finance and Operations.
 
-  **Статус заказа на продажу** меняется автоматически на **Выставлена накладная** после того как соответствующая накладная из Finance and Operations синхронизируется в Sales. Кроме того владелец заказа на продажу, из которого была создана накладная, назначается в качестве владельца накладной. Это дает владельцу заказа на продажу возможность просматривать накладную.
 
## <a name="preconditions-and-mapping-setup"></a>Предварительные условия и настройка сопоставления

Перед синхронизацией накладных по продажам необходимо задать в системах следующие параметры:

### <a name="setup-in-sales"></a>Настройка в Sales

- Выбрав **Параметры** > **Администрирование** > **Параметры системы** > **Продажи** убедитесь, что для параметра **Использовать системный расчет цен** установлено значение **Да**. 

- Выбрав **Параметры** > **Администрирование** > **Параметры системы** > **Продажи** убедитесь, что для параметра **Способ расчета скидки** установлено значение **Позиция строки**. 

### <a name="setup-in-the-data-integration-project"></a>Настройка в проекте интеграции данных

#### <a name="salesinvoiceheader-task"></a>Задача SalesInvoiceHeader

- Обновите сопоставление для **кода организации CDS** в **Источник** > **CDS**. 

    -  Значение шаблона по умолчанию для **SalesOrder_Organization_OrganizationId** — ORG001.
    -  Значение шаблона по умолчанию для **Account_Organization_OrganizationId** — ORG001.
    -  Значение шаблона по умолчанию для **Organization_OrganizationId** — ORG001.

- Убедитесь, что в **Источник** > **CDS для InvoiceCountryRegionId** существует необходимое сопоставление с **BillingAddress_Country**.

    -  Значение шаблона — **ValueMap** с количеством сопоставленных стран.

- Для создания накладных в Sales требуется **прайс-лист**. Измените **ValueMap** в **CDS** > **Место назначения для pricelevelid.name [имя прайс-листа]** на **прайс-лист**, используемый в Sales для данной валюты. Можно использовать либо **прайс-лист** по умолчанию для одной валюты, либо **ValueMap** если у вас есть **прайс-листы** в нескольких валютах.

    -  Значение шаблона для **pricelevelid.name [имя прайс-листа]** — это **ValueMap** в зависимости от **валюты**.
    -  usd: CRM Service USA (sample). 

#### <a name="salesinvoiceline-task"></a>Задача SalesInvoiceLine

- Убедитесь, что в **Источник** > **CDS** существует необходимое сопоставление для единицы измерения.

- Убедитесь, что в **Источник** > **Сопоставление CDS** существует необходимая **ValueMap** для **SalesUnitSymbol** в Finance and Operations. 
    
    - Значение шаблона с **ValueMap** определено для **SalesUnitSymbol с Quantity_UOM**.
    
-  Обновите сопоставление для кода организации CDS **Источник** > **CDS**. 

    -  Значение шаблона по умолчанию для **SalesInvoicer_Organization_OrganizationId** — ORG001.
    -  Значение шаблона по умолчанию для **Product_Organization_OrganizationId** — ORG001.
 
## <a name="template-mapping-in-data-integrator"></a>Сопоставление шаблона в интеграторе данных

> [!NOTE]
> Поля **Условия оплаты**, **Условия фрахта**, **Условия поставки**, **Способ доставки** и **Режим доставки** не входят в сопоставления по умолчанию. Для сопоставления этих полей необходимо настроить преобразование значений, характерное для данных в организациях, между которыми синхронизируется объект.

На следующем рисунке показан пример сопоставления шаблона в интеграторе данных.

![Сопоставление шаблона в интеграторе данных](./media/sales-invoice-template-mapping-data-integrator-1.png)

![Сопоставление шаблона в интеграторе данных](./media/sales-invoice-template-mapping-data-integrator-2.png)

![Сопоставление шаблона в интеграторе данных](./media/sales-invoice-template-mapping-data-integrator-3.png)

![Сопоставление шаблона в интеграторе данных](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Связанные разделы

[Синхронизация продуктов из Finance and Operations с продуктами в Sales](products-template-mapping.md)

[Синхронизация организаций из Finance and Operations с клиентами в Sales](accounts-template-mapping.md)

[Синхронизация контактов из Finance and Operations с контактами в Sales](contacts-template-mapping.md)

[Синхронизация заголовков и строк предложений по продажам из Sales с Finance and Operations](sales-quotation-template-mapping.md)

[Синхронизация заголовков и строк заказов на продажу из Finance and Operations в Sales](sales-order-template-mapping.md)


