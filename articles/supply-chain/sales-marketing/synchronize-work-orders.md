---
title: "Синхронизация заказов на выполнение работ Finance and Operations с Field Service"
description: "В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации заказов на выполнение работ с номером проекта из Microsoft Dynamics 365 for Field Service с Microsoft Dynamics 365 for Finance and Operations."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: f5bd6b8c554688d0d1b2bfd93a34a60a95412bf3
ms.contentlocale: ru-ru
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a>Синхронизация заказов на выполнение работ с проектом из Field Service с Finance and Operations

[!include[banner](../includes/banner.md)]

В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации заказов на выполнение работ с номером проекта из Microsoft Dynamics 365 for Field Service с Microsoft Dynamics 365 for Finance and Operations.

[![Синхронизация бизнес-процессов между Finance and Operations и Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Используемый шаблон **Продукты Field Service (из Finance and Operations в Field Service)** основан на шаблоне **Продукты (из Finance and Operations в Sales) — напрямую** из решения "Перспективный клиент в наличные деньги". Дополнительные сведения см. в разделе [Продукты (из Finance and Operations в Sales) — напрямую](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

В этом разделе описываются только различия между шаблонами **Продукты Field Service (из Finance and Operations в Field Service)** и **Продукты (из Finance and Operations в Field Service) — напрямую**.

Основное различие заключается в том, что этот шаблон включает сопоставление номера проекта, назначенного заказу на выполнение работ в Field Service, гарантируя, что заказ на продажу, созданный в Finance and Operations, содержит этот номер проекта, а также что выставление накладных будет возможно для связанного проекта. Помимо этого, шаблон использует расширенные запросы и фильтрацию.

## <a name="templates-and-tasks"></a>Шаблоны и задачи

**Имя шаблона в интеграции данных:**

- Заказы на выполнение работ с проектом (из Field Service в Finance and Operations)

**Имя задачи в проекте интеграции данных:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>Решение Field Service CRM
Поле **Внешний проект** было добавлено в объект "Заказ на выполнение работ". Это поле является полем подстановки, и за счет отметки проекта в вашем задании на выполнение работ заказ на покупку будет затем связан с проектом в Finance and Operations. После изменения значения **Состояние системы** из "Открыто — В работе(690,970,000)" на более высокий статус, поле **Внешний проект** будет заблокировано и вы не сможете добавить, удалить или изменить значение.

## <a name="template-mapping-in-data-integration"></a>Сопоставление шаблона в интеграции данных

На следующем рисунке показано сопоставление шаблона в интеграции данных.

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a>Заказы на выполнение работ с проектом (из Field Service в Finance and Operations): WorkOrderHeader

[![Сопоставление шаблона в интеграции данных](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a>Заказы на выполнение работ с проектом (из Field Service в Finance and Operations): WorkOrderHeaderProject

[![Сопоставление шаблона в интеграции данных](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a>Заказы на выполнение работ с проектом (из Field Service в Finance and Operations): WorkOrderProduct

[![Сопоставление шаблона в интеграции данных](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a>Заказы на выполнение работ с проектом (из Field Service в Finance and Operations): WorkOrderService

[![Сопоставление шаблона в интеграции данных](./media/FSWOP4.png)](./media/FSWOP4.png)

