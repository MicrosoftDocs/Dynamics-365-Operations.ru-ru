---
title: Синхронизация заказов на выполнение работ с проектом из Field Service с Finance and Operations
description: В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации заказов на выполнение работ с номером проекта из Microsoft Dynamics 365 for Field Service в Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 77358513ffdf791ab10d6efe1b84f598ffb5ec26
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843417"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a>Синхронизация заказов на выполнение работ с проектом из Field Service с Finance and Operations

[!include[banner](../includes/banner.md)]

В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации заказов на выполнение работ с номером проекта из Microsoft Dynamics 365 for Field Service в Microsoft Dynamics 365 for Finance and Operations.

[![Синхронизация бизнес-процессов между Finance and Operations и Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Используемый шаблон **Заказы на выполнение работ с проектом (из Field Service в Fin and Ops)** основан на шаблоне **Заказы на выполнение работ (из Field Service в Fin and Ops)**. Дополнительные сведения см. в разделе [Синхронизация заказов на выполнение работ в Field Service с заказами на продажу в Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

В этом разделе описываются только различия между двумя шаблонами:
- **Заказы на выполнение работ с проектом (из Field Service в Fin and Ops)**
- **Заказы на выполнение работ (из Field Service в Fin and Ops)**

Основное различие заключается в том, что этот шаблон включает сопоставление номера проекта, назначенного заказу на выполнение работ в Field Service, гарантируя, что заказ на продажу, созданный в Finance and Operations, содержит этот номер проекта, а также что выставление накладных будет возможно для связанного проекта. Помимо этого, шаблон использует расширенные запросы и фильтрацию.

## <a name="templates-and-tasks"></a>Шаблоны и задачи

**Имя шаблона в интеграции данных:**

- Заказы на выполнение работ с проектом (из Field Service в Fin and Ops)

**Имя задачи в проекте интеграции данных:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>Решение Field Service CRM
Поле **Внешний проект** было добавлено в объект "Заказ на выполнение работ". Это поле является полем подстановки, и за счет отметки проекта в вашем задании на выполнение работ заказ на покупку будет затем связан с проектом в Finance and Operations. После изменения значения **Состояние системы** из "Открыто — В работе(690,970,000)" на более высокий статус, поле **Внешний проект** будет заблокировано и вы не сможете добавить, удалить или изменить значение.

## <a name="template-mapping-in-data-integration"></a>Сопоставление шаблона в интеграции данных

На следующем рисунке показано сопоставление шаблона в интеграции данных.

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a>Заказы на выполнение работ с проектом (из Field Service в Fin and Ops): WorkOrderHeader

[![Сопоставление шаблона в интеграции данных](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a>Заказы на выполнение работ с проектом (из Field Service в Fin and Ops): WorkOrderHeaderProject

[![Сопоставление шаблона в интеграции данных](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a>Заказы на выполнение работ с проектом (из Field Service в Fin and Ops): WorkOrderProduct

[![Сопоставление шаблона в интеграции данных](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a>Заказы на выполнение работ с проектом (из Field Service в Fin and Ops): WorkOrderService

[![Сопоставление шаблона в интеграции данных](./media/FSWOP4.png)](./media/FSWOP4.png)
