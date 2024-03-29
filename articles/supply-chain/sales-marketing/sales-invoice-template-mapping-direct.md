---
title: Синхронизация заголовков и строк накладной по продаже непосредственно из Supply Chain Management с Sales
description: В этой статье рассматриваются шаблоны и базовые задачи, которые используются для синхронизации заголовков и строк накладных по продаже непосредственно из Dynamics 365 Supply Chain Management в Dynamics 365 Sales.
author: Henrikan
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 421d84b739faacbade711b01bfccb9f4efe6de32
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103286"
---
# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Синхронизация заголовков и строк накладных по продаже непосредственно из приложений для управления финансами и операциями с Sales

[!include [banner](../includes/banner.md)]

В этой статье рассматриваются шаблоны и базовые задачи, которые используются для синхронизации заголовков и строк накладных по продаже непосредственно из Dynamics 365 Supply Chain Management в Dynamics 365 Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Поток данных в решение "Перспективный клиент в наличные деньги"

Решение "Перспективный клиент в наличные деньги" использует функцию интеграции данных для синхронизации данных между экземплярами Supply Chain Management и Sales. Шаблоны "Перспективный клиент в наличные деньги", доступные в компоненте интеграции данных, обеспечивают движение данных об организациях, контактах, продуктах, предложениях по продажам, заказах на продажу и накладных по продажам между Supply Chain Management и Sales. На следующем рисунке показано, как данные синхронизируются между Supply Chain Management и Sales.

[![Поток данных в решение "Перспективный клиент в наличные деньги".](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Шаблоны и задачи

Чтобы получить доступ к доступным шаблонам, откройте [Центр администрирования Power Apps](https://preview.admin.powerapps.com/dataintegration). Выберите **Проекты**, затем в правом верхнем углу выберите **Создать проект**, чтобы выбрать общие шаблоны.

Следующий шаблон и базовые задачи используются для синхронизации заголовков и строк накладных по продажам напрямую из Sales с Supply Chain Management в Sales:

- **Имя шаблона в интеграции данных:** "Накладные продаж (из Fin and Ops в Sales) - напрямую"
- **Имена задач в проекте интеграции данных:**

    - SalesInvoiceHeader
    - SalesInvoiceLine

Перед синхронизацией заголовков и строк накладных по продаже требуются следующие задачи синхронизации:

- Продукты (из Supply Chain Management в Sales) — напрямую
- Счета (из Sales в Supply Chain Management) — напрямую (если используется)
- Контакты (из Sales в Supply Chain Management) — напрямую (если используется)
- Заголовки и строки заказов на продажу (из Supply Chain Management в Sales) — напрямую

## <a name="entity-set"></a>Набор объектов

| Управление цепочкой поставок                              | Прод.          |
|------------------------------------------------------|----------------|
| Заголовки счетов продажи клиентам, управляемых извне | Накладные       |
| Строки счетов продажи клиентам, управляемых извне   | InvoiceDetails |

## <a name="entity-flow"></a>Поток объектов

Накладные по продажам создаются в Supply Chain Management и синхронизируются с Sales.

> [!NOTE]
> В настоящее время налоги, связанные с суммами в заголовке накладной по продаже, не включаются в синхронизацию из Supply Chain Management в Sales. Sales не поддерживает налоговую информацию на уровне заголовка. Однако налог, который относится к расходам на уровне строки, включается в синхронизацию.

## <a name="prospect-to-cash-solution-for-sales"></a>Решение "Перспективный клиент в наличные деньги" для Sales

- Поле **Номер накладной** было добавлено в объект **Накладная** и отображается на странице.
- Кнопка **Создать накладную** на странице **Заказ на продажу** скрывается, потому что накладные будут создаваться в Supply Chain Management и синхронизироваться в Sales. Страница **Накладная** недоступна для редактирования, потому что накладные будут синхронизироваться из Supply Chain Management.
- Значение **Статус заказа на продажу** меняется автоматически на **Выставлена накладная** после того как соответствующая накладная из Supply Chain Management синхронизируется в Sales. Кроме того, владелец заказа на продажу, из которого была создана накладная, назначается в качестве владельца накладной. Таким образом, владелец заказа на продажу может просмотреть накладную.

## <a name="preconditions-and-mapping-setup"></a>Предварительные условия и настройка сопоставления

Перед синхронизацией накладных по продажам необходимо обновить следующие параметры в системах.

### <a name="setup-in-sales"></a>Настройка в Sales

Откройте **Параметры** > **Администрирование** > **Параметры системы** > **Продажи** и убедитесь, что используются следующие настройки:

- Для параметра **Использовать системный расчет цен** установлено значение **Да**.
- Для параметра **Способ расчета скидки** установлено значение **Номенклатура строки**.

### <a name="setup-in-the-data-integration-project"></a>Настройка в проекте интеграции данных

#### <a name="salesinvoiceheader-task"></a>Задача SalesInvoiceHeader

- Убедитесь в наличии необходимого сопоставления для **InvoiceCountryRegionId** в **BillingAddress\_Country**.

    Значение шаблона является схемой значений, где сопоставляются нескольких стран или регионов.

- Для создания накладных в Sales требуется прайс-лист. Обновите схему сопоставления для **pricelevelid.name \[имя прайс-листа\]** на прайс-лист, используемый в Sales для данной валюты. Можно использовать прайс-лист по умолчанию для одной валюты. Если имеются прайс-листы в нескольких валютах, можно использовать схему сопоставления.

    Значение шаблона для **pricelevelid.name \[Имя прайс-листа\]** представляет собой схему сопоставления, основанную на валюте с USD = CRM Service USA (образец).  
    
#### <a name="salesinvoiceline-task"></a>Задача SalesInvoiceLine

- Убедитесь в наличии необходимого сопоставления для параметра **Единица измерения**.
- Убедитесь, что существует требуемая схема сопоставления значений для **SalesUnitSymbol** в Supply Chain Management.

    Значение шаблона, которое имеет сопоставление значений, определено для **SalesUnitSymbol** в **Quantity\_UOM**.

## <a name="template-mapping-in-data-integration"></a>Сопоставление шаблона в интеграции данных

> [!NOTE]
> Поля **Условия оплаты**, **Условия фрахта**, **Условия поставки**, **Способ доставки** и **Режим доставки** не включены в сопоставления по умолчанию. Чтобы сопоставить эти поля, необходимо настроить преобразование значений, характерное для данных в организациях, между которыми синхронизируется объект.

На следующем рисунке показан пример сопоставления шаблона в интеграции данных. 

> [!NOTE]
> Сопоставление показывает, какие данные полей будут синхронизированы из Sales в Supply Chain Management.

### <a name="salesinvoiceheader"></a>SalesInvoiceHeader

![Сопоставление шаблонов в интеграции данных для SalesInvoiceHeader.](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a>SalesInvoiceLine

![Сопоставление шаблонов в интеграции данных для SalesInvoiceLine.](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-articles"></a>Связанные статьи

[Продажа перспективному клиенту](prospect-to-cash.md)

[Синхронизация организаций непосредственно из Sales с клиентами в Supply Chain Management](accounts-template-mapping-direct.md)

[Синхронизация продуктов непосредственно из Supply Chain Management с продуктами в Sales](products-template-mapping-direct.md)

[Синхронизация контактов непосредственно из Sales с контактами или клиентами в Supply Chain Management](contacts-template-mapping-direct.md)

[Синхронизация заказов на продажу напрямую между Sales и Supply Chain Management](sales-order-template-mapping-direct-two-ways.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
