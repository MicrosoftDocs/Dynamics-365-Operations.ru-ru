---
title: "Синхронизация продуктов с единицами измерения складского учета Finance and Operations с Field Service"
description: "В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации продуктов с единицей измерения складского учета из Microsoft Dynamics 365 for Finance and Operations с Microsoft Dynamics 365 for Field Service."
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
ms.openlocfilehash: 5d3767c1a499f3d888d8fc2ce06c2837442e39f0
ms.contentlocale: ru-ru
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a>Синхронизация продуктов с единицами измерения складского учета Finance and Operations с Field Service

[!include[banner](../includes/banner.md)]

В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации продуктов с единицей измерения складского учета из Microsoft Dynamics 365 for Finance and Operations с Microsoft Dynamics 365 for Field Service.

[![Синхронизация бизнес-процессов между Finance and Operations и Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Используемый шаблон **Продукты Field Service (из Finance and Operations в Field Service)** основан на шаблоне **Продукты (из Finance and Operations в Sales) — напрямую** из решения "Перспективный клиент в наличные деньги". Дополнительные сведения см. в разделе [Продукты (из Finance and Operations в Sales) — напрямую](products-template-mapping-direct.md).

В этом разделе описываются только различия между шаблонами **Продукты Field Service (из Finance and Operations в Field Service)** и **Продукты (из Finance and Operations в Field Service) — напрямую**.

## <a name="templates-and-tasks"></a>Шаблоны и задачи

**Имя шаблона в интеграции данных:**

- Продукты Field Service с единицей измерения складских запасов (из Finance and Operations в Sales)

**Имя задачи в проекте интеграции данных:**

- Товары

Шаблон **Продукты Field Service Products с единицей измерения складского учета (из Finance and Operations в Field Service)** включает одно сопоставление, которое не включено в шаблон **Продукты Field Service (из Finance and Operations в Field Service)**. Это сопоставление обеспечивает включение единицы измерения складского учета, необходимой для синхронизации уровня запасов.

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Сопоставление шаблона в интеграции данных

На следующем рисунке показано сопоставление шаблона в интеграции данных.

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a>Продукты Field Service с единицей измерения складского учета (из Finance and Operations в Field Service): Продукты

[![Сопоставление шаблона в интеграции данных](./media/FSProduct1.png)](./media/FSProduct1.png)

