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
ms.openlocfilehash: 185365ced5c4516d8fcdbdca88794d0078615888
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026856"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a>При разбиении количества с учетом в двух единицах измерения вместо номинального количества используется минимальное количество

Номер статьи базы знаний: 4612073

## <a name="symptoms"></a>Симптомы

Если количество с учетом в двух единицах измерения разделяется на партии, поле **Скомплектовать количество** использует минимальное количество, заданное для номенклатуры, а не номинальное количество.

## <a name="resolution"></a>Приказ

Система работает в соответствии с разработанным поведением. Система использует настройку минимального количества для каждой номенклатуры для комплектации.
