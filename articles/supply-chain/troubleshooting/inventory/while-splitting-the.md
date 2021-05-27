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
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a><span data-ttu-id="1cdce-103">При разбиении количества с учетом в двух единицах измерения вместо номинального количества используется минимальное количество</span><span class="sxs-lookup"><span data-stu-id="1cdce-103">When a catch-weight quantity is split, minimum quantity is used instead of nominal quantity</span></span>

<span data-ttu-id="1cdce-104">Номер статьи базы знаний: 4612073</span><span class="sxs-lookup"><span data-stu-id="1cdce-104">KB number: 4612073</span></span>

## <a name="symptoms"></a><span data-ttu-id="1cdce-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="1cdce-105">Symptoms</span></span>

<span data-ttu-id="1cdce-106">Если количество с учетом в двух единицах измерения разделяется на партии, поле **Скомплектовать количество** использует минимальное количество, заданное для номенклатуры, а не номинальное количество.</span><span class="sxs-lookup"><span data-stu-id="1cdce-106">When a catch-weight quantity is being split into batches, the **Pick qty** field uses the minimum quantity that is set for the item, not the nominal quantity.</span></span>

## <a name="resolution"></a><span data-ttu-id="1cdce-107">Приказ</span><span class="sxs-lookup"><span data-stu-id="1cdce-107">Resolution</span></span>

<span data-ttu-id="1cdce-108">Система работает в соответствии с разработанным поведением.</span><span class="sxs-lookup"><span data-stu-id="1cdce-108">The system is behaving as designed.</span></span> <span data-ttu-id="1cdce-109">Система использует настройку минимального количества для каждой номенклатуры для комплектации.</span><span class="sxs-lookup"><span data-stu-id="1cdce-109">The system uses each item's minimum quantity setup for picking.</span></span>
