---
title: Округленная сумма для расчетов амортизации
description: В этой статье рассматривается поле округление поле округления при амортизации, имеющееся на страницах настройки книг.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7721e46a72e0f8133ed67c597a066a97ffd61669
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "308422"
---
# <a name="round-off-amount-for-depreciation-calculations"></a><span data-ttu-id="53d6e-103">Округленная сумма для расчетов амортизации</span><span class="sxs-lookup"><span data-stu-id="53d6e-103">Round-off amount for depreciation calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53d6e-104">В этой статье рассматривается поле округление поле округления при амортизации, имеющееся на страницах настройки книг.</span><span class="sxs-lookup"><span data-stu-id="53d6e-104">This article discusses the Round-off depreciation field that is found on the Book setup pages.</span></span>

<span data-ttu-id="53d6e-105">Округленные суммы амортизации задаются для каждой книги.</span><span class="sxs-lookup"><span data-stu-id="53d6e-105">Round-off depreciation amounts are set for each book.</span></span> <span data-ttu-id="53d6e-106">Округленные суммы амортизации используются в профиле амортизации основных средств, который показывает будущую амортизацию и стоимость основного средства, а также в предложениях по амортизации.</span><span class="sxs-lookup"><span data-stu-id="53d6e-106">Round-off depreciation amounts are used in the fixed asset depreciation profile that shows the future depreciation and value of the fixed asset, and also in depreciation proposals.</span></span> <span data-ttu-id="53d6e-107">Введите наименьшую сумму амортизации, разрешенную для этой книги.</span><span class="sxs-lookup"><span data-stu-id="53d6e-107">Enter the lowest depreciation amount that is allowed for the book.</span></span> 

<span data-ttu-id="53d6e-108">Независимо от того, как настроена точность округления, сумма амортизации в последнем периоде амортизации не округляется.</span><span class="sxs-lookup"><span data-stu-id="53d6e-108">Regardless of the rounding that is set up, the depreciation amount in the last depreciation period isn't rounded.</span></span> <span data-ttu-id="53d6e-109">В конце последнего периода амортизации стоимость основного средства должна быть равна 0 (нулю) или ликвидационной стоимости, если используется ликвидационная стоимость.</span><span class="sxs-lookup"><span data-stu-id="53d6e-109">At the end of the last depreciation period, the value of the fixed asset must be 0 (zero) or the scrap value, if scrap value is used.</span></span>

### <a name="example"></a><span data-ttu-id="53d6e-110">Пример</span><span class="sxs-lookup"><span data-stu-id="53d6e-110">Example</span></span>

<span data-ttu-id="53d6e-111">Амортизация без округления рассчитывается как 2 444,44.</span><span class="sxs-lookup"><span data-stu-id="53d6e-111">Depreciation without rounding is calculated as 2,444.44.</span></span> <span data-ttu-id="53d6e-112">Как показано в следующей таблице, предлагаемые суммы изменяются в зависимости от настройки точности округления.</span><span class="sxs-lookup"><span data-stu-id="53d6e-112">As the following table shows, the amounts that are suggested vary, depending on how rounding is set up.</span></span>

| <span data-ttu-id="53d6e-113">Метод округления</span><span class="sxs-lookup"><span data-stu-id="53d6e-113">Rounding method</span></span> | <span data-ttu-id="53d6e-114">Сумма начисленной амортизации</span><span class="sxs-lookup"><span data-stu-id="53d6e-114">Depreciation amount</span></span> |
|-----------------|---------------------|
| <span data-ttu-id="53d6e-115">Округление 0,1</span><span class="sxs-lookup"><span data-stu-id="53d6e-115">Rounding 0.1</span></span>    | <span data-ttu-id="53d6e-116">2 444,40</span><span class="sxs-lookup"><span data-stu-id="53d6e-116">2,444.40</span></span>            |
| <span data-ttu-id="53d6e-117">Округление 1,00</span><span class="sxs-lookup"><span data-stu-id="53d6e-117">Rounding 1.00</span></span>   | <span data-ttu-id="53d6e-118">2,444.00</span><span class="sxs-lookup"><span data-stu-id="53d6e-118">2,444.00</span></span>            |
| <span data-ttu-id="53d6e-119">Округление 10,00</span><span class="sxs-lookup"><span data-stu-id="53d6e-119">Rounding 10.00</span></span>  | <span data-ttu-id="53d6e-120">2,440.00</span><span class="sxs-lookup"><span data-stu-id="53d6e-120">2,440.00</span></span>            |
| <span data-ttu-id="53d6e-121">Округление 100,00</span><span class="sxs-lookup"><span data-stu-id="53d6e-121">Rounding 100.00</span></span> | <span data-ttu-id="53d6e-122">2,400.00</span><span class="sxs-lookup"><span data-stu-id="53d6e-122">2,400.00</span></span>            |





