---
title: "Амортизационная премия"
description: "Эта статья содержит обзор функции Амортизационной премии."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBonus
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3621
ms.assetid: 835ec594-744e-461c-a676-1b9abc094173
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 89814bf54f09b91d7c23904c2f1ac31d5b284824
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="bonus-depreciation"></a><span data-ttu-id="674dc-103">Амортизационная премия</span><span class="sxs-lookup"><span data-stu-id="674dc-103">Bonus depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="674dc-104">Эта статья содержит обзор функции Амортизационной премии.</span><span class="sxs-lookup"><span data-stu-id="674dc-104">This article provides an overview of the bonus depreciation functionality.</span></span>

<span data-ttu-id="674dc-105">Для амортизационной премии можно получить дополнительные суммы амортизационной премии за первый год использования и амортизации актива.</span><span class="sxs-lookup"><span data-stu-id="674dc-105">For bonus depreciation, you can take extra or bonus depreciation amounts during the first year that the asset is put in service and depreciated.</span></span> <span data-ttu-id="674dc-106">Амортизационную премию необходимо применять до любых других расчетов амортизации.</span><span class="sxs-lookup"><span data-stu-id="674dc-106">Bonus depreciation must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="674dc-107">Поэтому рекомендуется использовать амортизационную премию с книгами, в которых функция разноски в ГК отключена.</span><span class="sxs-lookup"><span data-stu-id="674dc-107">Therefore, it's best to use bonus depreciation with books where the Post to general ledger functionality is disabled.</span></span> <span data-ttu-id="674dc-108">Можно использовать параметр **Удалить проводки, не разнесенные в главную книгу**, чтобы удалить исторические проводки для книг, которые не разносятся в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="674dc-108">You can use the **Delete transactions not posted to general ledger** option to delete historical transactions for books that don't post to the general ledger.</span></span> <span data-ttu-id="674dc-109">Затем можно учесть амортизационную премию позднее в жизненном цикле средства, удалив проводки амортизации, которые были ранее разнесены.</span><span class="sxs-lookup"><span data-stu-id="674dc-109">You can then accommodate bonus depreciation later in the asset life cycle by deleting depreciation transactions that were previously posted.</span></span> 

<span data-ttu-id="674dc-110">Амортизационную премию можно рассчитать, используя процесс предложений, либо проводки амортизационной премии можно создать вручную.</span><span class="sxs-lookup"><span data-stu-id="674dc-110">You can calculate bonus depreciation by using the proposal process, or you can create manual bonus depreciation transactions.</span></span> <span data-ttu-id="674dc-111">Нельзя создать проводки амортизационной премии, если для этой книги ОС существуют проводки амортизации или проводки корректировки амортизации.</span><span class="sxs-lookup"><span data-stu-id="674dc-111">You can't create bonus depreciation transactions if depreciation transactions or depreciation adjustment transactions exist for that asset book.</span></span>

<span data-ttu-id="674dc-112">При использовании процесса предложения для расчета амортизационной премии, все существующие проводки премии включаются в расчет базы.</span><span class="sxs-lookup"><span data-stu-id="674dc-112">When you use the proposal process to calculate bonus depreciation, all existing bonus transactions are included in the calculation of the basis.</span></span> <span data-ttu-id="674dc-113">Вычисление включает также все предыдущие амортизационные премии, введенные вручную для актива.</span><span class="sxs-lookup"><span data-stu-id="674dc-113">The calculation also includes any previous bonus depreciations that you manually entered for the asset.</span></span> 

<span data-ttu-id="674dc-114">Если для актива существует несколько учитываемых амортизационных премий, учитывается приоритет.</span><span class="sxs-lookup"><span data-stu-id="674dc-114">If more than one bonus depreciation will be taken for an asset, the priority is considered.</span></span> <span data-ttu-id="674dc-115">Каждая премия уменьшает базу актива для следующей премии.</span><span class="sxs-lookup"><span data-stu-id="674dc-115">Each bonus reduces the asset basis for the next bonus.</span></span> <span data-ttu-id="674dc-116">Ликвидационная стоимость не учитывается в базе актива для расчетов амортизационных премий, и соглашение по амортизации неприменимо к амортизационной премии.</span><span class="sxs-lookup"><span data-stu-id="674dc-116">Salvage value isn't considered in the asset basis for bonus depreciation calculations, and the depreciation convention doesn't apply for bonus depreciation.</span></span> 

<span data-ttu-id="674dc-117">В настоящее время некоторое имущество в США классифицируется как имущество Раздела 179.</span><span class="sxs-lookup"><span data-stu-id="674dc-117">Currently, in the United States, some property qualifies as Section 179 property.</span></span> <span data-ttu-id="674dc-118">С помощью вычета раздела 179 можно выполнить восстановление всей или части стоимости некоторой собственности, до определенного предела.</span><span class="sxs-lookup"><span data-stu-id="674dc-118">By using the Section 179 deduction, you can recover all or part of the cost of some property, up to a limit.</span></span> <span data-ttu-id="674dc-119">Можно восстановить стоимость путем вычитания ее в год, когда имущество было введено в эксплуатацию.</span><span class="sxs-lookup"><span data-stu-id="674dc-119">You can recover the cost by deducting it in the year when you put the property in service.</span></span>

## <a name="example"></a><span data-ttu-id="674dc-120">Пример</span><span class="sxs-lookup"><span data-stu-id="674dc-120">Example</span></span>
<span data-ttu-id="674dc-121">С книгой актива связаны следующие амортизационные премии:</span><span class="sxs-lookup"><span data-stu-id="674dc-121">The following bonus depreciations are associated with an asset book:</span></span>

-   <span data-ttu-id="674dc-122">**Раздел 179:** 1 000,00, Приоритет 1</span><span class="sxs-lookup"><span data-stu-id="674dc-122">**Section 179:** 1,000.00, Priority 1</span></span>
-   <span data-ttu-id="674dc-123">**Свободная зона:** 30 процентов, Приоритет 2</span><span class="sxs-lookup"><span data-stu-id="674dc-123">**Liberty Zone:** 30 percent, Priority 2</span></span>

<span data-ttu-id="674dc-124">Стоимость приобретения актива 5 000,00.</span><span class="sxs-lookup"><span data-stu-id="674dc-124">The asset acquisition cost is 5,000.00.</span></span> <span data-ttu-id="674dc-125">При расчете амортизационной премии величина первой амортизационной премии составляет 1000,00 для вычета по разделу 179.</span><span class="sxs-lookup"><span data-stu-id="674dc-125">When bonus depreciation is calculated, the first bonus depreciation amount is 1,000.00 for the Section 179 depreciation.</span></span> 

<span data-ttu-id="674dc-126">Следующее значение амортизационной премии – для вычета в свободной зоне – рассчитывается по следующей формуле:</span><span class="sxs-lookup"><span data-stu-id="674dc-126">The next bonus depreciation amount, for the Liberty Zone depreciation, is calculated as follows:</span></span> 

<span data-ttu-id="674dc-127">Затраты на приобретение – 1000 (вычет в соответствии с разделом 179) x 30% = 1200</span><span class="sxs-lookup"><span data-stu-id="674dc-127">Acquisition cost – 1,000 (Section 179 depreciation) × 30 percent = 1,200</span></span> 

<span data-ttu-id="674dc-128">Если величина амортизационной премии превышает остаток Стоимости приобретения, амортизационная премия будет равна либо рассчитанной амортизационной премии, либо остатку Стоимости приобретения, в зависимости от того, какая сумма меньше.</span><span class="sxs-lookup"><span data-stu-id="674dc-128">If the bonus depreciation amount is more than the remaining acquisition cost, the bonus depreciation amount is either the result of the bonus depreciation calculation or the remaining acquisition cost, whichever amount is less.</span></span> 

<span data-ttu-id="674dc-129">Если остаток затрат на приобретение равен 0 (нулю) или меньше нуля, проводки амортизационной премии не будут созданы.</span><span class="sxs-lookup"><span data-stu-id="674dc-129">If the remaining acquisition cost is 0 (zero) or less, bonus depreciation transactions isn't generated.</span></span> 

<span data-ttu-id="674dc-130">Когда амортизационная премия рассчитывается с помощью процесса предложений, проводка амортизационной премии будет создана для всех соответствующих записей амортизационной премии, связанных с книгой ОС.</span><span class="sxs-lookup"><span data-stu-id="674dc-130">When bonus depreciation is calculated by using the proposal process, a bonus depreciation transaction is created for all applicable bonus depreciation records that are associated with the asset book.</span></span> 

<span data-ttu-id="674dc-131">Можно создать неограниченное количество записей амортизационных премий.</span><span class="sxs-lookup"><span data-stu-id="674dc-131">You can create an unlimited number of bonus depreciation records.</span></span> <span data-ttu-id="674dc-132">После назначения этих записей журналу группы активов они используются для журнала активов.</span><span class="sxs-lookup"><span data-stu-id="674dc-132">After you assign those records to the asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="674dc-133">Амортизационная премия вводится как процент или фиксированная сумма.</span><span class="sxs-lookup"><span data-stu-id="674dc-133">Bonus depreciation is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="674dc-134">При разноске предложений по амортизации проводки амортизационной премии разносятся в книгу как проводки, отделенные от проводок амортизации.</span><span class="sxs-lookup"><span data-stu-id="674dc-134">When you post depreciation proposals, bonus depreciation transactions are posted to the book as separate transactions from the depreciation transactions.</span></span>




