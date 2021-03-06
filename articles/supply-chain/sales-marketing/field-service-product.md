---
title: Синхронизация продуктов непосредственно из Supply Chain Management с продуктами в Field Service
description: В этом разделе описываются шаблоны и базовая задача, которые используются для синхронизации продуктов из Dynamics 365 Supply Chain Management в Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 04/09/2018
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
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 45a989604d829db715756b6cd206a5675a18acf2
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909999"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a>Синхронизация продуктов непосредственно из Supply Chain Management с продуктами в Field Service

[!include[banner](../includes/banner.md)]

В этой теме рассматриваются шаблоны и базовая задача, которые используются для синхронизации продуктов из Dynamics 365 Supply Chain Management в Dynamics 365 Field Service.

Используемый шаблон **Продукты Field Service (из Supply Chain Management в Field Service)** основан на шаблоне **Продукты (из Supply Chain Management в Sales) — напрямую** из решения "Перспективный клиент в наличные деньги". Дополнительные сведения см. в разделе [Продукты (из Supply Chain Management в Sales) — напрямую](/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

В этом разделе описываются только различия между шаблонами **Продукты Field Service (из Supply Chain Management в Field Service)** и **Продукты (из Supply Chain Management в Sales) — напрямую**.

## <a name="templates-and-tasks"></a>Шаблоны и задачи

**Имя шаблона в интеграции данных**

- Продукты Field Service (из Supply Chain Management в Field Service)

**Имя задачи в проекте интеграции данных**

- Продукты — Продукты

Шаблон **Продукты Field Service (из Supply Chain Management в Field Service)** содержит одно сопоставление, которое отсутствует в шаблоне **Продукты (из Supply Chain Management в Sales) — напрямую**. Это сопоставление гарантирует, что обязательное специфичное для Field Service поле **Тип продукта Field Service** установлено правильно.

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

Используется следующее сопоставление значений.

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

В Supply Chain Management значение **Тип продукта Field Service** в информационном объекте **Запущенные в производство продукты продажи** вычисляется следующим образом:

- **Запасы:** Тип продукта = Продукт и Группа номенклатурных моделей, Учитываемый в запасах продукт = True
- **Запасы не для продажи:** Тип продукта = Продукт и Группа номенклатурных моделей, Учитываемый в запасах продукт = False
- **Услуга:** Тип продукта = Услуга

## <a name="template-mapping-in-data-integration"></a>Сопоставление шаблона в интеграции данных

На следующем рисунке показано сопоставление шаблона в интеграции данных.

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a>Продукты Field Service (из Supply Chain Management в Field Service): Продукты — Продукты

[![Сопоставление шаблона в интеграции данных](./media/FSProduct.png)](./media/FSProduct.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]