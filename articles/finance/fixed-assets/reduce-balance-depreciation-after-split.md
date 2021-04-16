---
title: Амортизация с уменьшаемым остатком после разделения
description: В этой теме описывается метод, используемый в модуле основных средств для расчета амортизации после разделения актива с помощью метода сокращения сальдо.
author: moaamer
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-17
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 056808b7d4d490bc4d60aa058108d159c1d4867c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826259"
---
# <a name="reduce-balance-depreciation-after-a-split"></a><span data-ttu-id="e6585-103">Амортизация с уменьшаемым остатком после разделения</span><span class="sxs-lookup"><span data-stu-id="e6585-103">Reduce balance depreciation after a split</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e6585-104">В этой теме описывается метод, используемый в модуле основных средств для расчета амортизации после разделения актива на другой актив с помощью метода сокращения сальдо.</span><span class="sxs-lookup"><span data-stu-id="e6585-104">This topic describes the method that is used in Fixed assets to calculate depreciation after an asset is split to another asset by using the reduce balance method.</span></span> <span data-ttu-id="e6585-105">Год амортизации, настроенный в книге активов, является финансовым годом.</span><span class="sxs-lookup"><span data-stu-id="e6585-105">The depreciation year that is configured in the asset book is the fiscal year.</span></span> <span data-ttu-id="e6585-106">Дополнительные сведения см. в разделе [Амортизация с уменьшаемым остатком](reduce-balance-depreciation.md) и [Разбиение основного средства](tasks/split-fixed-asset.md).</span><span class="sxs-lookup"><span data-stu-id="e6585-106">For more information, see [Reduce balance depreciation](reduce-balance-depreciation.md) and [Split a fixed asset](tasks/split-fixed-asset.md).</span></span>

<span data-ttu-id="e6585-107">При разбиении основных средств в течение финансового периода, который позже периода, в который был приобретен актив, амортизация с уменьшаемым остатком будет учитывать остаточную стоимость актива за предыдущий год.</span><span class="sxs-lookup"><span data-stu-id="e6585-107">If you split a fixed asset during a fiscal period that is later than the period when the asset was acquired, the reduced balance depreciation will account for the asset's net book value (NBV) for the previous year.</span></span> <span data-ttu-id="e6585-108">Также будут учтены проводки по приобретению и по корректировке амортизации, которые были созданы из проводки, которая разделяет актив.</span><span class="sxs-lookup"><span data-stu-id="e6585-108">It will also account for the acquisition and depreciation adjustment transactions that were generated from the transaction that split the asset.</span></span> <span data-ttu-id="e6585-109">В этом случае предполагается, что актив был приобретен в одном финансовом году и разбит в более позднем финансовом году.</span><span class="sxs-lookup"><span data-stu-id="e6585-109">This behavior assumes that the asset was acquired in one fiscal year and split in a later fiscal year.</span></span> <span data-ttu-id="e6585-110">Сумма, которая должна быть амортизирована для исходного актива после разделения, отражает остаточную стоимость актива до разделения актива и проводку по приобретению и корректировке амортизации, разнесенную для разбиения.</span><span class="sxs-lookup"><span data-stu-id="e6585-110">The amount that must be depreciated for the original asset after the split reflects the asset's NBV before the asset was split, and the acquisition and depreciation adjustment transaction that was posted for the split.</span></span>

<span data-ttu-id="e6585-111">Например, действуют следующие условия:</span><span class="sxs-lookup"><span data-stu-id="e6585-111">For example, the following conditions are in effect:</span></span>

- <span data-ttu-id="e6585-112">Финансовый период берется с 30 июня до 1 июля.</span><span class="sxs-lookup"><span data-stu-id="e6585-112">The fiscal period is from June 30 to July 1.</span></span>
- <span data-ttu-id="e6585-113">Процент уменьшаемого сальдо составляет 18 процентов, а актив приобретается в июне 2019 по цене приобретения 10 000 долларов США.</span><span class="sxs-lookup"><span data-stu-id="e6585-113">The reducing balance percentage is 18 percent, and an asset is acquired in June 2019 at an acquisition price of $10,000.</span></span>
- <span data-ttu-id="e6585-114">Амортизация первого финансового года равна 18 000 долларам США, месячная амортизация равняется 150 долларам США, а актив затем амортизируется до ноября 2019 года в сумме 738,75 долларов США.</span><span class="sxs-lookup"><span data-stu-id="e6585-114">The depreciation of the first fiscal year equals $18,000, the monthly depreciation equals $150, and the asset is then depreciated until November 2019, in the amount of $738.75.</span></span>
- <span data-ttu-id="e6585-115">В ноябре 2019 года 80 процентов актива разделяется на другие основные средства.</span><span class="sxs-lookup"><span data-stu-id="e6585-115">In November 2019, 80 percent of the asset is split to another fixed asset.</span></span>

<span data-ttu-id="e6585-116">[![Амортизация с уменьшаемым остатком после разделения](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span><span class="sxs-lookup"><span data-stu-id="e6585-116">[![Reduce balance depreciation after a split](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span></span>

<span data-ttu-id="e6585-117">Сумма для амортизации для исходного актива равна 1 822,25 долларов США.</span><span class="sxs-lookup"><span data-stu-id="e6585-117">The amount to depreciate for the original asset is $1,822.25.</span></span> <span data-ttu-id="e6585-118">Эта сумма равна остаточной стоимости до разноски проводки разбиения (9 111,25 доллара США) плюс корректировка приобретения, которая создается при разноске проводки разбиения (-8 000 долларов США) плюс корректировка амортизации, созданная в ходе проводки разбиения (711 долларов США).</span><span class="sxs-lookup"><span data-stu-id="e6585-118">This amount equals the NBV before the split transaction is posted ($9,111.25), plus the acquisition adjustment that is generated during posting of the split transaction (-$8,000), plus the depreciation adjustment that is generated during the split transaction ($711).</span></span> <span data-ttu-id="e6585-119">Таким образом, амортизация за второй год равна (1 822,25 × 18 процентов) ÷ 12 = 27,33 доллара США.</span><span class="sxs-lookup"><span data-stu-id="e6585-119">Therefore, the depreciation for the second year is (1,822.25 × 18 percent) ÷ 12 = $27.33.</span></span>

<span data-ttu-id="e6585-120">Сумма для амортизации для нового основного средства в первом году равна (8 000 × 18 процентов) ÷ 12 = 120 долларов США.</span><span class="sxs-lookup"><span data-stu-id="e6585-120">The amount to depreciate for the new fixed asset in the first year is (8,000 × 18 percent) ÷ 12 = $120.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]