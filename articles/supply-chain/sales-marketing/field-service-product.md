---
title: "Синхронизация продуктов в Finance and Operations с продуктами в Field Service"
description: "В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации продуктов из Microsoft Dynamics 365 for Finance and Operations с Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: ace66c037953f4b1b2e8b93a315faefdb090b1eb
ms.openlocfilehash: bf5de13fee6db1b467c1cf4d5cc65b46c67b29fe
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a>Синхронизация продуктов в Finance and Operations с продуктами в Field Service

[!include[banner](../includes/banner.md)]

В этой теме обсуждаются шаблоны и базовая задача, которые используются для синхронизации продуктов из Microsoft Dynamics 365 for Finance and Operations с Microsoft Dynamics 365 for Field Service.

Используемый шаблон **Продукты Field Service (из Fin and Ops в Field Service)** основан на шаблоне **Продукты (из Fin and Ops в Sales) — напрямую** из решения "Перспективный клиент в наличные деньги". Дополнительные сведения см. в разделе [Продукты (из Fin and Ops в Sales) — напрямую](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

В этом разделе описываются только различия между шаблонами **Продукты Field Service (из Fin and Ops в Field Service)** и **Продукты (из Fin and Ops в Sales) — напрямую**.

## <a name="templates-and-tasks"></a>Шаблоны и задачи

**Имя шаблона в интеграции данных:**

- Продукты Field Service (из Fin and Ops в Field Service)

**Имя задачи в проекте интеграции данных:**

- Продукты — Продукты

Шаблон **Продукты Field Service (из Fin and Ops в Field Service)** содержит одно сопоставление, которое отсутствует в шаблоне **Продукты (из Fin and Ops в Sales) — напрямую**. Это сопоставление гарантирует, что обязательное специфичное для Field Service поле **Тип продукта Field Service** установлено правильно.

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

Используется следующее сопоставление значений.

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

В Finance and Operations значение **Тип продукта Field Service** в информационном объекте **Запущенные в производство продукты продажи** вычисляется следующим образом:

- **Запасы:** Тип продукта = Продукт и Группа номенклатурных моделей, Учитываемый в запасах продукт = True
- **Запасы не для продажи:** Тип продукта = Продукт и Группа номенклатурных моделей, Учитываемый в запасах продукт = False
- **Услуга:** Тип продукта = Услуга

## <a name="template-mapping-in-data-integration"></a>Сопоставление шаблона в интеграции данных

На следующем рисунке показано сопоставление шаблона в интеграции данных.

### <a name="field-service-products-fin-and-ops-to-field-service-products---products"></a>Продукты Field Service (из Fin and Ops в Field Service): Продукты — Продукты

[![Сопоставление шаблона в интеграции данных](./media/FSProduct.png)](./media/FSProduct.png)

