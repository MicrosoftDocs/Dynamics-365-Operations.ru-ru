---
title: Текст перезаписывается при настройке номенклатуры в строке заказа на продажу
description: При настройке продукта в строке заказа на продажу измененный текст перезаписывается стандартным текстом. Измените текст после настройки строки, но не перед этим.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 20239b9b0eecb355274e909a8b8b39450e468c7e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477370"
---
# <a name="item-text-is-overwritten-when-a-product-is-configured-on-a-sales-order-line"></a>Текст номенклатуры перезаписывается при настройке продукта в строке заказа на продажу

## <a name="symptoms"></a>Симптомы

Эта проблема возникает при создании строки заказа на продажу для настраиваемой номенклатуры и последующем изменении текста номенклатуры. При настройке номенклатуры и последующем выборе **ОК** текст переписывается стандартным текстом.

## <a name="resolution"></a>Решение

Это поведение является ожидаемым. Текстовое поле включает имя варианта, которое заполняется только после настройки строки. Поэтому необходимо изменить текст после того, как вы настроили строку, но не ранее.
