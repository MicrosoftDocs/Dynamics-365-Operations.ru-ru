---
title: Ввод дополнения к ОС
description: Процедура описывает порядок добавления к существующему ОС.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetAddition
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c9733f07f995dd37669f3c33fd0f082daa34dd2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "324430"
---
# <a name="enter-an-addition-to-a-fixed-asset"></a><span data-ttu-id="c5239-103">Ввод дополнения к ОС</span><span class="sxs-lookup"><span data-stu-id="c5239-103">Enter an addition to a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c5239-104">Процедура описывает порядок добавления к существующему ОС.</span><span class="sxs-lookup"><span data-stu-id="c5239-104">This procedure shows how to add an addition to an existing fixed asset.</span></span> <span data-ttu-id="c5239-105">Цель дополнения к основному средств — отслеживание дополнений номенклатур, обслуживание или улучшение для актива и только для информации.</span><span class="sxs-lookup"><span data-stu-id="c5239-105">The purpose of Fixed asset additions is to track item additions, maintenance, or improvements for an asset, and is informational only.</span></span> <span data-ttu-id="c5239-106">Любые изменения стоимости основных средств или срока службы необходимо вносить отдельно.</span><span class="sxs-lookup"><span data-stu-id="c5239-106">Any changes to the fixed asset value or service life must be made separately.</span></span>   



<span data-ttu-id="c5239-107">В процедуре используется роль бухгалтера и демонстрационные данные для юридического лица USMF.</span><span class="sxs-lookup"><span data-stu-id="c5239-107">The procedure uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="c5239-108">Перейдите в раздел "Основные средства" > "Основные средства" > "Основные средства".</span><span class="sxs-lookup"><span data-stu-id="c5239-108">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="c5239-109">Найдите в списке основное средство для дополнения и выберите его.</span><span class="sxs-lookup"><span data-stu-id="c5239-109">In the list, find and select the fixed asset for the addition.</span></span>
3. <span data-ttu-id="c5239-110">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="c5239-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c5239-111">В области действий щелкните "Основное средство".</span><span class="sxs-lookup"><span data-stu-id="c5239-111">On the Action Pane, click Fixed asset.</span></span>
5. <span data-ttu-id="c5239-112">Щелкните "Дополнения к основному средству".</span><span class="sxs-lookup"><span data-stu-id="c5239-112">Click Fixed asset additions.</span></span>
6. <span data-ttu-id="c5239-113">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="c5239-113">Click New.</span></span>
7. <span data-ttu-id="c5239-114">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="c5239-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="c5239-115">Установите дату дополнительной покупки или услуги.</span><span class="sxs-lookup"><span data-stu-id="c5239-115">Set the date of the addition purchase or service.</span></span>
9. <span data-ttu-id="c5239-116">Введите стоимость номенклатуры, обслуживания или иного улучшения основного средства.</span><span class="sxs-lookup"><span data-stu-id="c5239-116">Enter the cost of the item, maintenance, or other improvement for the asset.</span></span>
10. <span data-ttu-id="c5239-117">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="c5239-117">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="c5239-118">Общая стоимость не повлияет на стоимость основного средства и используется только в целях отслеживания и информации.</span><span class="sxs-lookup"><span data-stu-id="c5239-118">The total cost will have no impact on the value of the fixed asset and is for tracking and informational purposes only.</span></span> <span data-ttu-id="c5239-119">Если стоимость будут капитализирована, проводку корректировки списания необходимо разнести отдельно.</span><span class="sxs-lookup"><span data-stu-id="c5239-119">If the cost will be capitalized, then a write-up adjustment transaction must be posted separately.</span></span>  
11. <span data-ttu-id="c5239-120">Перейдите на вкладку "Общие".</span><span class="sxs-lookup"><span data-stu-id="c5239-120">Click the General tab.</span></span>
    * <span data-ttu-id="c5239-121">Установите флажок "Увеличивает срок службы", если дополнение увеличивает срок службы основного средства.</span><span class="sxs-lookup"><span data-stu-id="c5239-121">Set Increases service life if the addition increases the service life of the asset.</span></span>  
    * <span data-ttu-id="c5239-122">Это поле используется только для информации.</span><span class="sxs-lookup"><span data-stu-id="c5239-122">This field is informational only.</span></span> <span data-ttu-id="c5239-123">Чтобы увеличить срок службы, измените срок службы в моделях стоимости и журналах амортизации для основного средства.</span><span class="sxs-lookup"><span data-stu-id="c5239-123">To increase the service life, modify the Service life on the Value models and/or Depreciation books for the asset.</span></span>  

