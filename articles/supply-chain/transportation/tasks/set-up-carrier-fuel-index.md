---
title: Настройка индекса топлива перевозчика
description: В этом руководстве демонстрируется, как создать регион индекса топлива, индекс топлива и индекс топлива перевозчика.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSFuelIndexRegion, TMSCarrierFuelIndexTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33441de148b7edc8c564465d94ccf5602acbbe67
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016755"
---
# <a name="set-up-a-carrier-fuel-index"></a><span data-ttu-id="609c8-103">Настройка индекса топлива перевозчика</span><span class="sxs-lookup"><span data-stu-id="609c8-103">Set up a carrier fuel index</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="609c8-104">В этом руководстве демонстрируется, как создать регион индекса топлива, индекс топлива и индекс топлива перевозчика.</span><span class="sxs-lookup"><span data-stu-id="609c8-104">This guide shows how to create a fuel index region, a fuel index and a carrier fuel index.</span></span> <span data-ttu-id="609c8-105">Регион индекса топлива определяет, к какому региону должен применяться индекс топлива, а индекс топлива определяет цену на топливо в течение определенного периода времени.</span><span class="sxs-lookup"><span data-stu-id="609c8-105">The fuel index region specifies which region the fuel index should apply to, and the fuel index specifies a fuel price for a particular period of time.</span></span> <span data-ttu-id="609c8-106">Чтобы отразить изменение в ценах на топливо с течением времени, можно связать перевозчика с несколькими индексами топлива.</span><span class="sxs-lookup"><span data-stu-id="609c8-106">To reflect the change in fuel prices over time, you can associate multiple fuel indexes with a carrier.</span></span>  <span data-ttu-id="609c8-107">Обычно эти задачи выполняются координатором транспортировки.</span><span class="sxs-lookup"><span data-stu-id="609c8-107">These tasks are normally done by a transportation coordinator.</span></span> <span data-ttu-id="609c8-108">Эту процедуру можно использовать применительно к компании с демонстрационными данными USMF или применительно к собственным данным.</span><span class="sxs-lookup"><span data-stu-id="609c8-108">You can use this procedure in demo data company USMF or using your own data.</span></span>


## <a name="create-a-fuel-index-region"></a><span data-ttu-id="609c8-109">Создание региона индекса топлива</span><span class="sxs-lookup"><span data-stu-id="609c8-109">Create a fuel index region</span></span>
1. <span data-ttu-id="609c8-110">Перейдите в раздел "Управление транспортировкой" > "Настройка" > "Индексы топлива" > "Регионы индекса топлива".</span><span class="sxs-lookup"><span data-stu-id="609c8-110">Go to Transportation management > Setup > Fuel indexes > Fuel index regions.</span></span>
    * <span data-ttu-id="609c8-111">Сначала необходимо создать различные регионы, в которых вы работаете, и рассчитать различные доплаты за топливо.</span><span class="sxs-lookup"><span data-stu-id="609c8-111">First you have to create the different regions, where you operate and calculate different fuel surcharges.</span></span>  
2. <span data-ttu-id="609c8-112">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="609c8-112">Click New.</span></span>
3. <span data-ttu-id="609c8-113">В поле "Регион" введите значение.</span><span class="sxs-lookup"><span data-stu-id="609c8-113">In the Region field, type a value.</span></span>
4. <span data-ttu-id="609c8-114">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="609c8-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="609c8-115">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="609c8-115">Click Save.</span></span>

## <a name="create-a-fuel-index"></a><span data-ttu-id="609c8-116">Создание индекса топлива</span><span class="sxs-lookup"><span data-stu-id="609c8-116">Create a fuel index</span></span>
1. <span data-ttu-id="609c8-117">Перейдите в раздел "Управление транспортировкой" > "Настройка" > "Индексы топлива" > "Индексы топлива".</span><span class="sxs-lookup"><span data-stu-id="609c8-117">Go to Transportation management > Setup > Fuel indexes > Fuel indexes.</span></span>
    * <span data-ttu-id="609c8-118">Для настроенных регионов необходимо ввести текущие цены на топливо.</span><span class="sxs-lookup"><span data-stu-id="609c8-118">For the regions you have set up you need to enter the current prices for the fuel.</span></span>  
2. <span data-ttu-id="609c8-119">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="609c8-119">Click New.</span></span>
3. <span data-ttu-id="609c8-120">В поле "Регион" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="609c8-120">In the Region field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="609c8-121">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="609c8-121">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="609c8-122">В поле "Цена за галлон" введите число.</span><span class="sxs-lookup"><span data-stu-id="609c8-122">In the Price per gallon field, enter a number.</span></span>
6. <span data-ttu-id="609c8-123">В поле "Фактические дата и время начала" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="609c8-123">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="609c8-124">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="609c8-124">Click Save.</span></span>

## <a name="create-a-carrier-fuel-index"></a><span data-ttu-id="609c8-125">Создание индекса топлива перевозчика</span><span class="sxs-lookup"><span data-stu-id="609c8-125">Create a Carrier fuel index</span></span>
1. <span data-ttu-id="609c8-126">Перейдите в раздел "Управление транспортировкой" > "Настройка" > "Индексы топлива" > "Индексы топлива перевозчика".</span><span class="sxs-lookup"><span data-stu-id="609c8-126">Go to Transportation management > Setup > Fuel indexes > Carrier fuel indexes.</span></span>
2. <span data-ttu-id="609c8-127">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="609c8-127">Click New.</span></span>
3. <span data-ttu-id="609c8-128">В поле "Индекс топлива перевозчика" введите значение.</span><span class="sxs-lookup"><span data-stu-id="609c8-128">In the Carrier fuel index field, type a value.</span></span>
4. <span data-ttu-id="609c8-129">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="609c8-129">In the Description field, type a value.</span></span>
5. <span data-ttu-id="609c8-130">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="609c8-130">Click New.</span></span>
6. <span data-ttu-id="609c8-131">В поле "Фактические дата и время начала" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="609c8-131">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="609c8-132">В поле "Цена за галлон от" введите число.</span><span class="sxs-lookup"><span data-stu-id="609c8-132">In the PPG From field, enter a number.</span></span>
    * <span data-ttu-id="609c8-133">В этом примере можно установить значение в поле "Цена за галлон от" равным 1,95.</span><span class="sxs-lookup"><span data-stu-id="609c8-133">In this example, you can set PPG From field to 1.95.</span></span>  
8. <span data-ttu-id="609c8-134">В поле "Цена за галлон до" введите число.</span><span class="sxs-lookup"><span data-stu-id="609c8-134">In the PPG To field, enter a number.</span></span>
    * <span data-ttu-id="609c8-135">В этом примере можно установить значение в поле "Цена за галлон до" равным 2.</span><span class="sxs-lookup"><span data-stu-id="609c8-135">In this example you can set the PPG To field to 2.</span></span>  
9. <span data-ttu-id="609c8-136">В поле "Процент" введите число.</span><span class="sxs-lookup"><span data-stu-id="609c8-136">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="609c8-137">В этом примере можно установить процент равным 3.</span><span class="sxs-lookup"><span data-stu-id="609c8-137">In this example you can set the percentage to 3.</span></span>  
10. <span data-ttu-id="609c8-138">В поле "Валюта" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="609c8-138">In the Currency field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="609c8-139">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="609c8-139">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="609c8-140">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="609c8-140">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="609c8-141">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="609c8-141">Click Save.</span></span>

