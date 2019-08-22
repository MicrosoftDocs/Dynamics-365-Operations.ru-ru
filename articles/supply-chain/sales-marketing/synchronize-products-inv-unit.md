---
title: Синхронизация продуктов с единицами измерения складского учета Finance and Operations с Field Service
description: В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации продуктов с единицей измерения складского учета из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
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
ms.openlocfilehash: 78e8d8fa609b015cf2fceaf498279fe091325dbb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835702"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a>Синхронизация продуктов с единицами измерения складского учета Finance and Operations с Field Service

[!include[banner](../includes/banner.md)]

В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации продуктов с единицей измерения складского учета из Microsoft Dynamics 365 for Finance and Operations в Microsoft Dynamics 365 for Field Service.

[![Синхронизация бизнес-процессов между Finance and Operations и Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Использованный шаблон **Продукты Field Service Products с единицей измерения складского учета (из Fin and Ops в Field Service)** основан на шаблоне **Продукты Field Service (из Fin and Ops в Field Service)**. Дополнительные сведения см. в разделе [Продукты Field Service (из Finance and Operations в Field Service)](field-service-product.md).

В этом разделе описываются только различия между двумя шаблонами: 
- **Продукты Field Service с единицей измерения складских запасов (из Fin and Ops в Sales)**
- **Продукты Field Service (из Fin and Ops в Field Service)** 

## <a name="templates-and-tasks"></a>Шаблоны и задачи

**Имя шаблона в интеграции данных:**

- Продукты Field Service с единицей измерения складских запасов (из Fin and Ops в Sales)

**Имя задачи в проекте интеграции данных:**

- Товары

Шаблон **Продукты Field Service Products с единицей измерения складского учета (из Fin and Ops в Field Service)** включает одно сопоставление, которое не включено в шаблон **Продукты Field Service (из Fin and Ops в Field Service)**. Это сопоставление обеспечивает включение единицы измерения складского учета, необходимой для синхронизации уровня запасов.

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Сопоставление шаблона в интеграции данных

На следующем рисунке показано сопоставление шаблона в интеграции данных.

### <a name="field-service-products-with-inventory-unit-fin-and-ops-to-field-service-products"></a>Продукты Field Service с единицей измерения складского учета (из Fin and Ops в Field Service): Продукты

[![Сопоставление шаблона в интеграции данных](./media/FSProduct1.png)](./media/FSProduct1.png)
