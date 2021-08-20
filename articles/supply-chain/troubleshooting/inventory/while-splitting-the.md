---
title: При разбиении количества с учетом в двух единицах измерения вместо номинального количества используется минимальное количество
description: Если количество с учетом в двух единицах измерения разделяется на партии, поле "Скомплектовать количество" использует минимальное количество, заданное для номенклатуры, а не номинальное количество.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 424ad46281612f6a3e8cb4c90478a39f757d5416c3ce1d77ed6ff6dba7b20dcb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723463"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a>При разбиении количества с учетом в двух единицах измерения вместо номинального количества используется минимальное количество

Номер статьи базы знаний: 4612073

## <a name="symptoms"></a>Симптомы

Если количество с учетом в двух единицах измерения разделяется на партии, поле **Скомплектовать количество** использует минимальное количество, заданное для номенклатуры, а не номинальное количество.

## <a name="resolution"></a>Приказ

Система работает в соответствии с разработанным поведением. Система использует настройку минимального количества для каждой номенклатуры для комплектации.
