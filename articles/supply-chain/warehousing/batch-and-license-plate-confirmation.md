---
title: "Подтверждение партии и грузоместа"
description: "В этом разделе описывается, как настроить и применить подтверждение партии и грузоместа на мобильном устройстве."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: efab5b11782fd2344fb5f532272007d187c1465b
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---

# <a name="batch-and-license-plate-confirmation"></a><span data-ttu-id="dc6b0-103">Подтверждение партии и грузоместа</span><span class="sxs-lookup"><span data-stu-id="dc6b0-103">Batch and license plate confirmation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc6b0-104">Подтверждение партии позволяет подтвердить, что правильная партия комплектуется, на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="dc6b0-104">Batch confirmation allows you to confirm that the correct batch is being picked from the mobile device.</span></span> <span data-ttu-id="dc6b0-105">Только при первоначальной комплектации работы для указанных выше номенклатур, где партия выше означает, что партия выше чем расположение в иерархии поиска, необходимо убедиться, что скомплектованная партия соответствует партии в строке работы.</span><span class="sxs-lookup"><span data-stu-id="dc6b0-105">On the initial pick of work for batch above-items only, where batch above indicates that batch ranges higher than location in the search hierarchy, you must verify that the batch that is picked matches the batch on the work line.</span></span> 

<span data-ttu-id="dc6b0-106">Подтверждение грузоместа позволяет подтвердить, что правильное грузоместо комплектуется, на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="dc6b0-106">License plate confirmation allows you to confirm that the correct license plate is being picked from the mobile device.</span></span> <span data-ttu-id="dc6b0-107">При работе комплектации из местоположения стадии необходимо проверить, что комплектуемое грузоместо соответствует грузоместу, связанному с работой.</span><span class="sxs-lookup"><span data-stu-id="dc6b0-107">When picking work from a stage location, you must verify that the license plate that is picked matches the license plate that is associated with the work.</span></span> <span data-ttu-id="dc6b0-108">Если работа начинается путем сканирования грузоместа, этот шаг подтверждения будет пропущен.</span><span class="sxs-lookup"><span data-stu-id="dc6b0-108">If the work is started by scanning a license plate, this confirmation step will be skipped.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="dc6b0-109">Где он применяется.</span><span class="sxs-lookup"><span data-stu-id="dc6b0-109">Where it applies</span></span>
<span data-ttu-id="dc6b0-110">Подтверждение применяется в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="dc6b0-110">Confirmation applies in the following scenarios:</span></span>

- <span data-ttu-id="dc6b0-111">Подтверждение партии применяется к первоначальной комплектации работы для номенклатур "партия выше".</span><span class="sxs-lookup"><span data-stu-id="dc6b0-111">Batch confirmation applies to the initial picks of work for batch above-items.</span></span>
- <span data-ttu-id="dc6b0-112">Подтверждение грузоместа применяется к комплектации из расположения стадии.</span><span class="sxs-lookup"><span data-stu-id="dc6b0-112">License plate confirmation applies to picks from stage locations.</span></span>

## <a name="set-up-batch-and-license-plate-confirmation"></a><span data-ttu-id="dc6b0-113">Настройка подтверждения партии и грузоместа</span><span class="sxs-lookup"><span data-stu-id="dc6b0-113">Set up batch and license plate confirmation</span></span>
<span data-ttu-id="dc6b0-114">Можно настроить подтверждение партии и грузоместа в меню на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="dc6b0-114">You can configure batch and license plate confirmation from the mobile device menu items.</span></span>  
1.  <span data-ttu-id="dc6b0-115">В пунктах меню мобильного устройства введите настройки подтверждения работы.</span><span class="sxs-lookup"><span data-stu-id="dc6b0-115">From the mobile device menu items, enter the work confirmation setup.</span></span>  
2.  <span data-ttu-id="dc6b0-116">Выберите параметр для подтверждения партии или грузоместа.</span><span class="sxs-lookup"><span data-stu-id="dc6b0-116">Select the option for either batch or license plate confirmation.</span></span> <span data-ttu-id="dc6b0-117">Оба параметра доступны для комплектаций типа работы, у которых не включено автоматическое подтверждение.</span><span class="sxs-lookup"><span data-stu-id="dc6b0-117">Both options are available for work type picks that do not have automatic confirmation enabled.</span></span>  

