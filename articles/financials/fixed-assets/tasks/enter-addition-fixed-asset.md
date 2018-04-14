--- 
title: "Ввод дополнения к ОС"
description: "Процедура описывает порядок добавления к существующему ОС."
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 4b8277073810e678fd7d4c76371eeb4709ece020
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---
# <a name="enter-an-addition-to-a-fixed-asset"></a><span data-ttu-id="ee139-103">Ввод дополнения к ОС</span><span class="sxs-lookup"><span data-stu-id="ee139-103">Enter an addition to a fixed asset</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ee139-104">Процедура описывает порядок добавления к существующему ОС.</span><span class="sxs-lookup"><span data-stu-id="ee139-104">This procedure shows how to add an addition to an existing fixed asset.</span></span> <span data-ttu-id="ee139-105">Цель дополнения к основному средств — отслеживание дополнений номенклатур, обслуживание или улучшение для актива и только для информации.</span><span class="sxs-lookup"><span data-stu-id="ee139-105">The purpose of Fixed asset additions is to track item additions, maintenance, or improvements for an asset, and is informational only.</span></span> <span data-ttu-id="ee139-106">Любые изменения стоимости основных средств или срока службы необходимо вносить отдельно.</span><span class="sxs-lookup"><span data-stu-id="ee139-106">Any changes to the fixed asset value or service life must be made separately.</span></span>   



<span data-ttu-id="ee139-107">В процедуре используется роль бухгалтера и демонстрационные данные для юридического лица USMF.</span><span class="sxs-lookup"><span data-stu-id="ee139-107">The procedure uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="ee139-108">Перейдите в раздел "Основные средства" > "Основные средства" > "Основные средства".</span><span class="sxs-lookup"><span data-stu-id="ee139-108">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="ee139-109">Найдите в списке основное средство для дополнения и выберите его.</span><span class="sxs-lookup"><span data-stu-id="ee139-109">In the list, find and select the fixed asset for the addition.</span></span>
3. <span data-ttu-id="ee139-110">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="ee139-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ee139-111">В области действий щелкните "Основное средство".</span><span class="sxs-lookup"><span data-stu-id="ee139-111">On the Action Pane, click Fixed asset.</span></span>
5. <span data-ttu-id="ee139-112">Щелкните "Дополнения к основному средству".</span><span class="sxs-lookup"><span data-stu-id="ee139-112">Click Fixed asset additions.</span></span>
6. <span data-ttu-id="ee139-113">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="ee139-113">Click New.</span></span>
7. <span data-ttu-id="ee139-114">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="ee139-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="ee139-115">Установите дату дополнительной покупки или услуги.</span><span class="sxs-lookup"><span data-stu-id="ee139-115">Set the date of the addition purchase or service.</span></span>
9. <span data-ttu-id="ee139-116">Введите стоимость номенклатуры, обслуживания или иного улучшения основного средства.</span><span class="sxs-lookup"><span data-stu-id="ee139-116">Enter the cost of the item, maintenance, or other improvement for the asset.</span></span>
10. <span data-ttu-id="ee139-117">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="ee139-117">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="ee139-118">Общая стоимость не повлияет на стоимость основного средства и используется только в целях отслеживания и информации.</span><span class="sxs-lookup"><span data-stu-id="ee139-118">The total cost will have no impact on the value of the fixed asset and is for tracking and informational purposes only.</span></span> <span data-ttu-id="ee139-119">Если стоимость будут капитализирована, проводку корректировки списания необходимо разнести отдельно.</span><span class="sxs-lookup"><span data-stu-id="ee139-119">If the cost will be capitalized, then a write-up adjustment transaction must be posted separately.</span></span>  
11. <span data-ttu-id="ee139-120">Перейдите на вкладку "Общие".</span><span class="sxs-lookup"><span data-stu-id="ee139-120">Click the General tab.</span></span>
    * <span data-ttu-id="ee139-121">Установите флажок "Увеличивает срок службы", если дополнение увеличивает срок службы основного средства.</span><span class="sxs-lookup"><span data-stu-id="ee139-121">Set Increases service life if the addition increases the service life of the asset.</span></span>  
    * <span data-ttu-id="ee139-122">Это поле используется только для информации.</span><span class="sxs-lookup"><span data-stu-id="ee139-122">This field is informational only.</span></span> <span data-ttu-id="ee139-123">Чтобы увеличить срок службы, измените срок службы в моделях стоимости и журналах амортизации для основного средства.</span><span class="sxs-lookup"><span data-stu-id="ee139-123">To increase the service life, modify the Service life on the Value models and/or Depreciation books for the asset.</span></span>  


