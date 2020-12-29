---
title: Ввод дополнения к ОС
description: Процедура описывает порядок добавления к существующему ОС.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetAddition
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc1e13863ae13daaa641f52f7a55e01fc1353dc1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447215"
---
# <a name="enter-an-addition-to-a-fixed-asset"></a><span data-ttu-id="2c7cd-103">Ввод дополнения к ОС</span><span class="sxs-lookup"><span data-stu-id="2c7cd-103">Enter an addition to a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2c7cd-104">Процедура описывает порядок добавления к существующему ОС.</span><span class="sxs-lookup"><span data-stu-id="2c7cd-104">This procedure shows how to add an addition to an existing fixed asset.</span></span> <span data-ttu-id="2c7cd-105">Цель дополнения к основному средств — отслеживание дополнений номенклатур, обслуживание или улучшение для актива и только для информации.</span><span class="sxs-lookup"><span data-stu-id="2c7cd-105">The purpose of Fixed asset additions is to track item additions, maintenance, or improvements for an asset, and is informational only.</span></span> <span data-ttu-id="2c7cd-106">Любые изменения стоимости основных средств или срока службы необходимо вносить отдельно.</span><span class="sxs-lookup"><span data-stu-id="2c7cd-106">Any changes to the fixed asset value or service life must be made separately.</span></span>   

<span data-ttu-id="2c7cd-107">В процедуре используется роль бухгалтера и демонстрационные данные для юридического лица USMF.</span><span class="sxs-lookup"><span data-stu-id="2c7cd-107">The procedure uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="2c7cd-108">В области перехода, перейдите к **Модули > Фиксированные активы > Фиксированные активы > Фиксированные активы**.</span><span class="sxs-lookup"><span data-stu-id="2c7cd-108">In the Navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="2c7cd-109">Найдите в списке основное средство для дополнения и выберите его.</span><span class="sxs-lookup"><span data-stu-id="2c7cd-109">In the list, find and select the fixed asset for the addition.</span></span>
3. <span data-ttu-id="2c7cd-110">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="2c7cd-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="2c7cd-111">На панели операций щелкните **Основное средство**.</span><span class="sxs-lookup"><span data-stu-id="2c7cd-111">On the Action Pane, click **Fixed asset**.</span></span>
5. <span data-ttu-id="2c7cd-112">Щелкните **Дополнения к основному средству**.</span><span class="sxs-lookup"><span data-stu-id="2c7cd-112">Click **Fixed asset additions**.</span></span>
6. <span data-ttu-id="2c7cd-113">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="2c7cd-113">Click **New**.</span></span>
7. <span data-ttu-id="2c7cd-114">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="2c7cd-114">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="2c7cd-115">В поле **Дата приобретения** установите дату дополнительной покупки или услуги.</span><span class="sxs-lookup"><span data-stu-id="2c7cd-115">In the **Acquisition date** field, set the date of the addition purchase or service.</span></span>
9. <span data-ttu-id="2c7cd-116">В поле **Стоимость единицы** введите стоимость номенклатуры, обслуживания или иного улучшения основного средства.</span><span class="sxs-lookup"><span data-stu-id="2c7cd-116">In the **Unit cost** field, enter the cost of the item, maintenance, or other improvement for the asset.</span></span>
10. <span data-ttu-id="2c7cd-117">В поле **Количество** введите число.</span><span class="sxs-lookup"><span data-stu-id="2c7cd-117">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="2c7cd-118">Общая стоимость не повлияет на стоимость основного средства и используется только в целях отслеживания и информации.</span><span class="sxs-lookup"><span data-stu-id="2c7cd-118">The total cost will have no impact on the value of the fixed asset and is for tracking and informational purposes only.</span></span> <span data-ttu-id="2c7cd-119">Если стоимость будут капитализирована, проводку корректировки списания необходимо разнести отдельно.</span><span class="sxs-lookup"><span data-stu-id="2c7cd-119">If the cost will be capitalized, then a write-up adjustment transaction must be posted separately.</span></span>  
11. <span data-ttu-id="2c7cd-120">Перейдите на вкладку **Общие**.</span><span class="sxs-lookup"><span data-stu-id="2c7cd-120">Click the **General** tab.</span></span>

    * <span data-ttu-id="2c7cd-121">Задайте для параметра **Увеличивает срок службы** значение **Да**, если дополнение увеличивает срок службы основного средства.</span><span class="sxs-lookup"><span data-stu-id="2c7cd-121">Set **Increases service life** to **Yes** if the addition increases the service life of the asset.</span></span>  
    * <span data-ttu-id="2c7cd-122">Это поле используется только для информации.</span><span class="sxs-lookup"><span data-stu-id="2c7cd-122">This field is informational only.</span></span> <span data-ttu-id="2c7cd-123">Чтобы увеличить срок службы, измените срок службы в моделях стоимости и журналах амортизации для основного средства.</span><span class="sxs-lookup"><span data-stu-id="2c7cd-123">To increase the service life, modify the Service life on the Value models and/or Depreciation books for the asset.</span></span>  

