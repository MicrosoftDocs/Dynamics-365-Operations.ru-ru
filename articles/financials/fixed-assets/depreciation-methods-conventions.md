---
title: Методы амортизации и соглашения по амортизации
description: В этой статье представлен обзор соглашений по амортизации и методы амортизации, которые поддерживаются Microsoft Dynamics 365 for Finance and Operations.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be8e05a386178b9172a906109e015269dc72b32e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569663"
---
# <a name="depreciation-methods-and-conventions"></a><span data-ttu-id="d5aba-103">Методы амортизации и соглашения по амортизации</span><span class="sxs-lookup"><span data-stu-id="d5aba-103">Depreciation methods and conventions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d5aba-104">В этой статье представлен обзор соглашений по амортизации и методы амортизации, которые поддерживаются Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d5aba-104">This article provides an overview of the depreciation conventions and depreciation methods that are supported by Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="d5aba-105">Можно выбрать различные методы амортизации и соглашения.</span><span class="sxs-lookup"><span data-stu-id="d5aba-105">You can select various depreciation methods and conventions.</span></span> <span data-ttu-id="d5aba-106">Назначение методов отнести амортизируемую стоимость основных средств к финансовым периодам.</span><span class="sxs-lookup"><span data-stu-id="d5aba-106">The purpose of the methods is to allocate the depreciable value of the fixed asset into fiscal periods.</span></span> <span data-ttu-id="d5aba-107">Общая цена приобретения основных средств, за вычетом ликвидационной стоимости, если она имеется.</span><span class="sxs-lookup"><span data-stu-id="d5aba-107">The depreciable value of the fixed asset is the acquisition price, reduced by a scrap value, if any.</span></span> 

<span data-ttu-id="d5aba-108">Если при использовании соглашений по амортизации будет изменена последняя дата начала амортизации для активов, который затем вызывает пропуск некоторых амортизаций, амортизации за последний год могут быть больше или меньше ожидаемых.</span><span class="sxs-lookup"><span data-stu-id="d5aba-108">If you are using depreciation conventions and you modify the last depreciation run date for an asset, which then causes some depreciations to be skipped, the depreciation for the last year might be more than or less than is expected.</span></span> <span data-ttu-id="d5aba-109">Амортизация регулируется числом периодов амортизации, затронутых модификацией последней даты начала амортизации.</span><span class="sxs-lookup"><span data-stu-id="d5aba-109">The depreciation is adjusted by the number of depreciation periods affected by the modification of the last depreciation run date.</span></span>

<span data-ttu-id="d5aba-110">Например, если используется полугодовое соглашение по амортизации на три года, срок амортизации обычно составляет около 3,5 лет.</span><span class="sxs-lookup"><span data-stu-id="d5aba-110">For example, if you are using the Half year depreciation convention over three years, depreciation ordinarily occurs over 3 1/2 years.</span></span> <span data-ttu-id="d5aba-111">При изменении последней даты начала амортизации в течение 3,5 лет в последнем году амортизации сдвигается число затронутых периодов.</span><span class="sxs-lookup"><span data-stu-id="d5aba-111">If you change the last depreciation run date during the 3 1/2 years, the last year of depreciation moves out the number of periods affected.</span></span> <span data-ttu-id="d5aba-112">Если дата сдвигается на 3 месяцев, в последнем году сумма затрат составит 9 месяцев амортизации, когда обычно была бы стоимость 6 месяцев амортизации.</span><span class="sxs-lookup"><span data-stu-id="d5aba-112">If you move the date by three months, the last year will have nine months’ worth of depreciation, when ordinarily there would be six months’ worth of depreciation.</span></span>

<span data-ttu-id="d5aba-113">Можно выбрать из следующих соглашений по амортизации.</span><span class="sxs-lookup"><span data-stu-id="d5aba-113">You can select from the following depreciation conventions.</span></span>


-   <span data-ttu-id="d5aba-114">Полугодие</span><span class="sxs-lookup"><span data-stu-id="d5aba-114">Half year</span></span>
-   <span data-ttu-id="d5aba-115">Полный месяц</span><span class="sxs-lookup"><span data-stu-id="d5aba-115">Full month</span></span>
-   <span data-ttu-id="d5aba-116">Середина квартала</span><span class="sxs-lookup"><span data-stu-id="d5aba-116">Mid quarter</span></span>
-   <span data-ttu-id="d5aba-117">Середина месяца (1 число месяца)</span><span class="sxs-lookup"><span data-stu-id="d5aba-117">Mid month (1st of month)</span></span>
-   <span data-ttu-id="d5aba-118">Середина месяца (15 число месяца)</span><span class="sxs-lookup"><span data-stu-id="d5aba-118">Mid month (15th of month)</span></span>
-   <span data-ttu-id="d5aba-119">Полгода (начало года)</span><span class="sxs-lookup"><span data-stu-id="d5aba-119">Half year (start of year)</span></span>
-   <span data-ttu-id="d5aba-120">Половина года (следующий год)</span><span class="sxs-lookup"><span data-stu-id="d5aba-120">Half year (next year)</span></span>

<span data-ttu-id="d5aba-121">Можно выбрать один из следующих методов амортизации:</span><span class="sxs-lookup"><span data-stu-id="d5aba-121">You can select from the following depreciation methods.</span></span>
-   <span data-ttu-id="d5aba-122">Срок службы (прямолинейный метод)</span><span class="sxs-lookup"><span data-stu-id="d5aba-122">Straight line service life</span></span>
-   <span data-ttu-id="d5aba-123">Уменьшаемое сальдо</span><span class="sxs-lookup"><span data-stu-id="d5aba-123">Reducing balance</span></span>
-   <span data-ttu-id="d5aba-124">Ручная</span><span class="sxs-lookup"><span data-stu-id="d5aba-124">Manual</span></span>
-   <span data-ttu-id="d5aba-125">Множитель</span><span class="sxs-lookup"><span data-stu-id="d5aba-125">Factor</span></span>
-   <span data-ttu-id="d5aba-126">Себестоимость</span><span class="sxs-lookup"><span data-stu-id="d5aba-126">Consumption</span></span>
-   <span data-ttu-id="d5aba-127">Оставшийся срок службы прямолинейный метод)</span><span class="sxs-lookup"><span data-stu-id="d5aba-127">Straight line life remaining</span></span>
-   <span data-ttu-id="d5aba-128">Уменьшаемое сальдо в 200%</span><span class="sxs-lookup"><span data-stu-id="d5aba-128">200% reducing balance</span></span>
-   <span data-ttu-id="d5aba-129">Уменьшаемое сальдо в 175%</span><span class="sxs-lookup"><span data-stu-id="d5aba-129">175% reducing balance</span></span>
-   <span data-ttu-id="d5aba-130">Уменьшаемый остаток в 150%</span><span class="sxs-lookup"><span data-stu-id="d5aba-130">150% reducing balance</span></span>
-   <span data-ttu-id="d5aba-131">Уменьшаемое сальдо в 125%</span><span class="sxs-lookup"><span data-stu-id="d5aba-131">125% reducing balance</span></span>





<a name="additional-resources"></a><span data-ttu-id="d5aba-132">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d5aba-132">Additional resources</span></span>
--------

[<span data-ttu-id="d5aba-133">Амортизация ОС</span><span class="sxs-lookup"><span data-stu-id="d5aba-133">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)

[<span data-ttu-id="d5aba-134">Линейная амортизация срока службы</span><span class="sxs-lookup"><span data-stu-id="d5aba-134">Straight line service life depreciation</span></span>](Straight-line-service-life-depreciation.md)

[<span data-ttu-id="d5aba-135">Уменьшение амортизации баланса</span><span class="sxs-lookup"><span data-stu-id="d5aba-135">Reducing balance depreciation</span></span>](reduce-balance-depreciation.md)

[<span data-ttu-id="d5aba-136">Ручная амортизация</span><span class="sxs-lookup"><span data-stu-id="d5aba-136">Manual depreciation</span></span>](manual-depreciation.md)

[<span data-ttu-id="d5aba-137">Коэффициент амортизации</span><span class="sxs-lookup"><span data-stu-id="d5aba-137">Factor depreciation</span></span>](factor-depreciation.md)

[<span data-ttu-id="d5aba-138">Амортизация потребления</span><span class="sxs-lookup"><span data-stu-id="d5aba-138">Consumption depreciation</span></span>](consumption-depreciation.md)

[<span data-ttu-id="d5aba-139">Линейная амортизация с уменьшаемым остатком</span><span class="sxs-lookup"><span data-stu-id="d5aba-139">Straight line life remaining depreciation</span></span>](straight-line-life-remaining-depreciation.md)

[<span data-ttu-id="d5aba-140">Амортизация с уменьшаемым остатком в 125%</span><span class="sxs-lookup"><span data-stu-id="d5aba-140">125 percent reducing balance depreciation</span></span>](125-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="d5aba-141">Амортизация с уменьшаемым остатком в 150%</span><span class="sxs-lookup"><span data-stu-id="d5aba-141">150 percent reducing balance depreciation</span></span>](150-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="d5aba-142">Амортизация с уменьшаемым остатком в 175%</span><span class="sxs-lookup"><span data-stu-id="d5aba-142">175 percent reducing balance depreciation</span></span>](175-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="d5aba-143">Амортизация с уменьшаемым остатком в 200%</span><span class="sxs-lookup"><span data-stu-id="d5aba-143">200 percent reducing balance depreciation</span></span>](200-percent-reducing-balance-depreciation.md)



