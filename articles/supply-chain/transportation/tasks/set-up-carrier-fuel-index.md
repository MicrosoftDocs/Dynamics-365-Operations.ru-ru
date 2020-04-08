---
title: Настройка индекса топлива перевозчика
description: В этом руководстве демонстрируется, как создать регион индекса топлива, индекс топлива и индекс топлива перевозчика.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 73336c6803f28239ff8ca78dcff5ea8db0835e32
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146275"
---
# <a name="set-up-a-carrier-fuel-index"></a><span data-ttu-id="fad56-103">Настройка индекса топлива перевозчика</span><span class="sxs-lookup"><span data-stu-id="fad56-103">Set up a carrier fuel index</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fad56-104">В этом руководстве демонстрируется, как создать регион индекса топлива, индекс топлива и индекс топлива перевозчика.</span><span class="sxs-lookup"><span data-stu-id="fad56-104">This guide shows how to create a fuel index region, a fuel index and a carrier fuel index.</span></span> <span data-ttu-id="fad56-105">Регион индекса топлива определяет, к какому региону должен применяться индекс топлива, а индекс топлива определяет цену на топливо в течение определенного периода времени.</span><span class="sxs-lookup"><span data-stu-id="fad56-105">The fuel index region specifies which region the fuel index should apply to, and the fuel index specifies a fuel price for a particular period of time.</span></span> <span data-ttu-id="fad56-106">Чтобы отразить изменение в ценах на топливо с течением времени, можно связать перевозчика с несколькими индексами топлива.</span><span class="sxs-lookup"><span data-stu-id="fad56-106">To reflect the change in fuel prices over time, you can associate multiple fuel indexes with a carrier.</span></span>  <span data-ttu-id="fad56-107">Обычно эти задачи выполняются координатором транспортировки.</span><span class="sxs-lookup"><span data-stu-id="fad56-107">These tasks are normally done by a transportation coordinator.</span></span> <span data-ttu-id="fad56-108">Эту процедуру можно использовать применительно к компании с демонстрационными данными USMF или применительно к собственным данным.</span><span class="sxs-lookup"><span data-stu-id="fad56-108">You can use this procedure in demo data company USMF or using your own data.</span></span>


## <a name="create-a-fuel-index-region"></a><span data-ttu-id="fad56-109">Создание региона индекса топлива</span><span class="sxs-lookup"><span data-stu-id="fad56-109">Create a fuel index region</span></span>
1. <span data-ttu-id="fad56-110">Перейдите в раздел "Управление транспортировкой" > "Настройка" > "Индексы топлива" > "Регионы индекса топлива".</span><span class="sxs-lookup"><span data-stu-id="fad56-110">Go to Transportation management > Setup > Fuel indexes > Fuel index regions.</span></span>
    * <span data-ttu-id="fad56-111">Сначала необходимо создать различные регионы, в которых вы работаете, и рассчитать различные доплаты за топливо.</span><span class="sxs-lookup"><span data-stu-id="fad56-111">First you have to create the different regions, where you operate and calculate different fuel surcharges.</span></span>  
2. <span data-ttu-id="fad56-112">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="fad56-112">Click New.</span></span>
3. <span data-ttu-id="fad56-113">В поле "Регион" введите значение.</span><span class="sxs-lookup"><span data-stu-id="fad56-113">In the Region field, type a value.</span></span>
4. <span data-ttu-id="fad56-114">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="fad56-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="fad56-115">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="fad56-115">Click Save.</span></span>

## <a name="create-a-fuel-index"></a><span data-ttu-id="fad56-116">Создание индекса топлива</span><span class="sxs-lookup"><span data-stu-id="fad56-116">Create a fuel index</span></span>
1. <span data-ttu-id="fad56-117">Перейдите в раздел "Управление транспортировкой" > "Настройка" > "Индексы топлива" > "Индексы топлива".</span><span class="sxs-lookup"><span data-stu-id="fad56-117">Go to Transportation management > Setup > Fuel indexes > Fuel indexes.</span></span>
    * <span data-ttu-id="fad56-118">Для настроенных регионов необходимо ввести текущие цены на топливо.</span><span class="sxs-lookup"><span data-stu-id="fad56-118">For the regions you have set up you need to enter the current prices for the fuel.</span></span>  
2. <span data-ttu-id="fad56-119">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="fad56-119">Click New.</span></span>
3. <span data-ttu-id="fad56-120">В поле "Регион" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="fad56-120">In the Region field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="fad56-121">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="fad56-121">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="fad56-122">В поле "Цена за галлон" введите число.</span><span class="sxs-lookup"><span data-stu-id="fad56-122">In the Price per gallon field, enter a number.</span></span>
6. <span data-ttu-id="fad56-123">В поле "Фактические дата и время начала" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="fad56-123">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="fad56-124">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="fad56-124">Click Save.</span></span>

## <a name="create-a-carrier-fuel-index"></a><span data-ttu-id="fad56-125">Создание индекса топлива перевозчика</span><span class="sxs-lookup"><span data-stu-id="fad56-125">Create a Carrier fuel index</span></span>
1. <span data-ttu-id="fad56-126">Перейдите в раздел "Управление транспортировкой" > "Настройка" > "Индексы топлива" > "Индексы топлива перевозчика".</span><span class="sxs-lookup"><span data-stu-id="fad56-126">Go to Transportation management > Setup > Fuel indexes > Carrier fuel indexes.</span></span>
2. <span data-ttu-id="fad56-127">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="fad56-127">Click New.</span></span>
3. <span data-ttu-id="fad56-128">В поле "Индекс топлива перевозчика" введите значение.</span><span class="sxs-lookup"><span data-stu-id="fad56-128">In the Carrier fuel index field, type a value.</span></span>
4. <span data-ttu-id="fad56-129">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="fad56-129">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fad56-130">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="fad56-130">Click New.</span></span>
6. <span data-ttu-id="fad56-131">В поле "Фактические дата и время начала" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="fad56-131">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="fad56-132">В поле "Цена за галлон от" введите число.</span><span class="sxs-lookup"><span data-stu-id="fad56-132">In the PPG From field, enter a number.</span></span>
    * <span data-ttu-id="fad56-133">В этом примере можно установить значение в поле "Цена за галлон от" равным 1,95.</span><span class="sxs-lookup"><span data-stu-id="fad56-133">In this example, you can set PPG From field to 1.95.</span></span>  
8. <span data-ttu-id="fad56-134">В поле "Цена за галлон до" введите число.</span><span class="sxs-lookup"><span data-stu-id="fad56-134">In the PPG To field, enter a number.</span></span>
    * <span data-ttu-id="fad56-135">В этом примере можно установить значение в поле "Цена за галлон до" равным 2.</span><span class="sxs-lookup"><span data-stu-id="fad56-135">In this example you can set the PPG To field to 2.</span></span>  
9. <span data-ttu-id="fad56-136">В поле "Процент" введите число.</span><span class="sxs-lookup"><span data-stu-id="fad56-136">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="fad56-137">В этом примере можно установить процент равным 3.</span><span class="sxs-lookup"><span data-stu-id="fad56-137">In this example you can set the percentage to 3.</span></span>  
10. <span data-ttu-id="fad56-138">В поле "Валюта" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="fad56-138">In the Currency field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="fad56-139">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="fad56-139">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="fad56-140">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="fad56-140">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="fad56-141">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="fad56-141">Click Save.</span></span>

