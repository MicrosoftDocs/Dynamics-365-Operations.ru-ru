---
title: В одном чеке печатается только одна этикетка для нескольких заголовков работы
description: В одном чеке печатается только одна этикетка для нескольких заголовков работы.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8e11dc918eb3c9085018d15b43819522cc8bebe3
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026846"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a><span data-ttu-id="016de-103">В одном чеке печатается только одна этикетка для нескольких заголовков работы</span><span class="sxs-lookup"><span data-stu-id="016de-103">Only one label is printed for multiple work headers on a single receipt</span></span>

<span data-ttu-id="016de-104">Номер статьи базы знаний: 4614667</span><span class="sxs-lookup"><span data-stu-id="016de-104">KB number: 4614667</span></span>

## <a name="symptoms"></a><span data-ttu-id="016de-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="016de-105">Symptoms</span></span>

<span data-ttu-id="016de-106">Несколько заголовков работ создается для одного и того же целевого грузоместа в рамках одного события получения приложения склада.</span><span class="sxs-lookup"><span data-stu-id="016de-106">Multiple work headers are created for the same target license plate as part of a single warehouse app receiving event.</span></span> <span data-ttu-id="016de-107">Однако при получении продукта будет напечатана только одна этикетка для грузоместа.</span><span class="sxs-lookup"><span data-stu-id="016de-107">However, only one license plate label is printed when the product is received.</span></span>

## <a name="resolution"></a><span data-ttu-id="016de-108">Приказ</span><span class="sxs-lookup"><span data-stu-id="016de-108">Resolution</span></span>

<span data-ttu-id="016de-109">Система работает в соответствии с разработанным поведением.</span><span class="sxs-lookup"><span data-stu-id="016de-109">The system is behaving as designed.</span></span>

<span data-ttu-id="016de-110">В текущей системе всегда генерируется отдельная метка для грузоместа, независимо от количества заголовков и существующих сочетаний заголовка и строки работы.</span><span class="sxs-lookup"><span data-stu-id="016de-110">In the current design, a single license plate label is always generated, regardless of the number of work header and work line combinations that exist.</span></span> <span data-ttu-id="016de-111">Созданная метка включает информацию только для одной комбинации.</span><span class="sxs-lookup"><span data-stu-id="016de-111">The generated label includes the information for only one combination.</span></span>

<span data-ttu-id="016de-112">Чтобы обойти эту проблему, убедитесь, что создание заголовка работ всегда сопоставляется только с одним целевым грузоместом.</span><span class="sxs-lookup"><span data-stu-id="016de-112">To work around this issue, make sure that work header creation is always mapped to just one target license plate.</span></span>
