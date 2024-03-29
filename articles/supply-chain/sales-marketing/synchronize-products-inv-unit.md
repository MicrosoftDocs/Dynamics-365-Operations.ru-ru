---
title: Синхронизация продуктов с единицей измерения складского учета из Supply Chain Management в Field Service
description: В этой статье обсуждаются шаблоны и базовая задача, которые используются для синхронизации продуктов с единицей измерения складского учета из Dynamics 365 Supply Chain Management в Dynamics 365 Field Service.
author: Henrikan
ms.date: 03/13/2019
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
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5f7658eacd20aa69a64d6288e9d29e53b6ccb002
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887264"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a>Синхронизация продуктов с единицей измерения складского учета из Supply Chain Management в Field Service

[!include[banner](../includes/banner.md)]

В этой статье обсуждаются шаблоны и базовая задача, которые используются для синхронизации продуктов с единицей измерения складского учета из Dynamics 365 Supply Chain Management в Dynamics 365 Field Service.

[![Синхронизация бизнес-процессов между Supply Chain Management и Field Service.](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Использованный шаблон **Продукты Field Service Products с единицей измерения складского учета (из Supply Chain Management в Field Service)** основан на шаблоне **Продукты Field Service (из Supply Chain Management в Field Service)**. Дополнительные сведения см. в разделе [Синхронизация продуктов непосредственно из Supply Chain Management с продуктами в Field Service](field-service-product.md).

В этой статье описываются только различия между двумя шаблонами: 
- **Продукты Field Service с единицей измерения складского учета (из Supply Chain Management в Sales)**
- **Продукты Field Service (из Supply Chain Management в Field Service)** 

## <a name="templates-and-tasks"></a>Шаблоны и задачи

**Имя шаблона в интеграции данных:**

- Продукты Field Service с единицей измерения складского учета (из Supply Chain Management в Sales)

**Имя задачи в проекте интеграции данных:**

- Товары

Шаблон **Продукты Field Service Products с единицей измерения складского учета (из Supply Chain Management в Field Service)** содержит одно сопоставление, которое отсутствует в шаблоне **Продукты Field Service (из Supply Chain Management в Field Service)**. Это сопоставление обеспечивает включение единицы измерения складского учета, необходимой для синхронизации уровня запасов.

```plaintext
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Сопоставление шаблона в интеграции данных

На следующем рисунке показано сопоставление шаблона в интеграции данных.

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a>Продукты Field Service с единицей измерения складского учета (из Supply Chain Management в Field Service): Продукты

[![Сопоставление шаблона в интеграции данных.](./media/FSProduct1.png)](./media/FSProduct1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]