---
title: Синхронизация заказов на выполнение работ с проектом из Field Service в Supply Chain Management
description: В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации заказов на выполнение работ с номером проекта из Dynamics 365 Field Service в Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 3ee512c2814b45a0bf35d1bee718b1ce37867bbb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010823"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a>Синхронизация заказов на выполнение работ с проектом из Field Service в Supply Chain Management

[!include[banner](../includes/banner.md)]

В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации заказов на выполнение работ с номером проекта из Dynamics 365 Field Service в Dynamics 365 Supply Chain Management.

[![Синхронизация бизнес-процессов между Supply Chain Management и Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Используемый шаблон **Заказы на выполнение работ с проектом (из Field Service в Supply Chain Management)** основан на шаблоне **Заказы на выполнение работ (из Field Service в Supply Chain Management)**. Дополнительные сведения см. в разделе [Синхронизация заказов на выполнение работ в Field Service с заказами на продажу в Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

В этом разделе описываются только различия между двумя шаблонами:
- **Заказы на выполнение работ с проектом (из Field Service в Supply Chain Management)**
- **Заказы на выполнение работ (из Field Service в Supply Chain Management)**

Основное различие заключается в том, что этот шаблон включает сопоставление номера проекта, назначенного заказу на выполнение работ в Field Service, гарантируя, что заказ на продажу, созданный в Supply Chain Management, содержит этот номер проекта, а также что выставление накладных будет возможно для связанного проекта. Помимо этого, шаблон использует расширенные запросы и фильтрацию.

## <a name="templates-and-tasks"></a>Шаблоны и задачи

**Имя шаблона в интеграции данных:**

- Заказы на выполнение работ с проектом (из Field Service в Supply Chain Management)

**Имя задачи в проекте интеграции данных:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>Решение Field Service CRM
Поле **Внешний проект** было добавлено в объект "Заказ на выполнение работ". Это поле является полем подстановки, и за счет отметки проекта в вашем задании на выполнение работ заказ на покупку будет затем связан с проектом в Supply Chain Management. Когда значение **Состояние системы** изменяется из "Открыто — В работе(690 970 000)" на более высокий статус, поле **Внешний проект** будет заблокировано и вы не сможете добавить, удалить или изменить значение.

## <a name="template-mapping-in-data-integration"></a>Сопоставление шаблона в интеграции данных

На следующем рисунке показано сопоставление шаблона в интеграции данных.

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a>Заказы на выполнение работ с проектом (из Field Service в Supply Chain Management): WorkOrderHeader

[![Сопоставление шаблона в интеграции данных](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a>Заказы на выполнение работ с проектом (из Field Service в Supply Chain Management): WorkOrderHeaderProject

[![Сопоставление шаблона в интеграции данных](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a>Заказы на выполнение работ с проектом (из Field Service в Supply Chain Management): WorkOrderProduct

[![Сопоставление шаблона в интеграции данных](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a>Заказы на выполнение работ с проектом (из Field Service в Supply Chain Management): WorkOrderService

[![Сопоставление шаблона в интеграции данных](./media/FSWOP4.png)](./media/FSWOP4.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]