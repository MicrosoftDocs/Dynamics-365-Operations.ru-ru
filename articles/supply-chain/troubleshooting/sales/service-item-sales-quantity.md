---
title: Невозможно задать количество номенклатуры Услуги в строке предложения по продажам
description: При работе с предложениями по продажам нельзя задавать количество продаж для продуктов, которые являются номенклатурами Услуга, так как отсутствуют физические номенклатуры для подсчета.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea0f8f246e95f90b6ac5e78ee63950c9ca836a0e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477457"
---
# <a name="cant-change-the-sales-quantity-of-a-service-item-on-a-sales-quotation-line"></a>Невозможно изменить количество продажи для номенклатуры Услуги в строке предложения по продажам

## <a name="symptoms"></a>Симптомы

При попытке задать количество для продажи (поле **SalesQty**) для номенклатуры типа *Сервис* в строке предложения по продажам будет выведено следующее сообщение:

> Обновление не разрешено для поля количества.

## <a name="cause"></a>Причина

Это предусмотрено разработчиками. Невозможно задать количество для продажи для продуктов, которые являются номенклатурами обслуживания. Например, если вы предлагаете услугу по установке номенклатуры, нет смысла записывать количество, поскольку отсутствует физическая номенклатура для подсчета. Имеется только услуга.
