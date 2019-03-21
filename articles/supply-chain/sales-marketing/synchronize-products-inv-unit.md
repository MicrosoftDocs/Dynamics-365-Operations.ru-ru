---
title: Синхронизация продуктов с единицами измерения складского учета Finance and Operations с Field Service
description: В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации продуктов с единицей измерения складского учета из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 8e421be79fde6103be6344040b6ae6cda0626c5a
ms.sourcegitcommit: d9ed934a142b88340d268fd2bd3753475a3712b0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/12/2019
ms.locfileid: "836310"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a>Синхронизация продуктов с единицами измерения складского учета Finance and Operations с Field Service

[!include[banner](../includes/banner.md)]

В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации продуктов с единицей измерения складского учета из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.

[![Синхронизация бизнес-процессов между Finance and Operations и Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Использованный шаблон **Продукты Field Service Products с единицей измерения складского учета (из Finance and Operations в Field Service)** основан на шаблоне **Продукты Field Service (из Finance and Operations в Field Service)**. Дополнительные сведения см. в разделе [Продукты Field Service (из Finance and Operations в Field Service)](field-service-product.md).

В этом разделе описываются только различия между двумя шаблонами: 
- **Продукты Field Service с единицей измерения складских запасов (из Finance and Operations в Sales)**
- **Продукты Field Service (из Finance and Operations в Field Service)**. 

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
