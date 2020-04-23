---
title: Уровень обслуживания и описание
description: В этом разделе описываются уровень обслуживания и описание в модуле "Управление активами".
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0aa23e7fe10e684e110126bd58bd761348e44700
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215501"
---
# <a name="service-level-and-description"></a><span data-ttu-id="95800-103">Уровень обслуживания и описание</span><span class="sxs-lookup"><span data-stu-id="95800-103">Service level and description</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="95800-104">При создании заказа на работу может быть необходимо определить уровни обслуживания для него и добавить к нему общее описание.</span><span class="sxs-lookup"><span data-stu-id="95800-104">When you create a work order, you might want to define the service levels for it and add a general description to it.</span></span> <span data-ttu-id="95800-105">Можно создать уровни обслуживания для заказов на работу на странице **Уровни обслуживания для заказа на работу** и описания на странице **Описание заказа на работу**.</span><span class="sxs-lookup"><span data-stu-id="95800-105">You can create work order service levels on the **Work order service levels** page and descriptions on the **Work order description** page.</span></span>

## <a name="create-a-service-level"></a><span data-ttu-id="95800-106">Создание уровня обслуживания</span><span class="sxs-lookup"><span data-stu-id="95800-106">Create a service level</span></span>

1. <span data-ttu-id="95800-107">Выберите **Управление активами** \> **Настройка** \> **Заказы на работу** \> **Уровень обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="95800-107">Select **Asset management** \> **Setup** \> **Work orders** \> **Service level**.</span></span>
2. <span data-ttu-id="95800-108">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="95800-108">Select **New**.</span></span>
3. <span data-ttu-id="95800-109">В поле **Уровень обслуживания** введите уровень обслуживания (например, номер).</span><span class="sxs-lookup"><span data-stu-id="95800-109">In the **Service level** field, enter the service level (for example, a number).</span></span>
4. <span data-ttu-id="95800-110">В поле **Имя** введите имя.</span><span class="sxs-lookup"><span data-stu-id="95800-110">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="95800-111">На экспресс-вкладке **Заказы на работу** можно определить ожидаемые даты и время начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="95800-111">On the **Work orders** FastTab, you can define expected start and end dates and times.</span></span> <span data-ttu-id="95800-112">Поля на этой экспресс-вкладке определяют период, в течение которого заказы на работу должны быть начаты и завершены.</span><span class="sxs-lookup"><span data-stu-id="95800-112">The fields on this FastTab define the period that work orders should be started and ended during.</span></span> <span data-ttu-id="95800-113">Они используются для заказов на работу, созданных вручную, и заказов на работу, созданных на основе запросов обслуживания.</span><span class="sxs-lookup"><span data-stu-id="95800-113">They are used for work orders that are manually created and work orders that are created based on maintenance requests.</span></span> 

5. <span data-ttu-id="95800-114">В поле **День начала** введите количество дней, чтобы определить период, в течение которого должен начаться заказ на работу.</span><span class="sxs-lookup"><span data-stu-id="95800-114">In the **Start day** field, enter a number of days to define the period that the work order should start during.</span></span> <span data-ttu-id="95800-115">Количество дней рассчитывается с даты создания заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="95800-115">The number of days is calculated from the creation date of the work order.</span></span> <span data-ttu-id="95800-116">Например, если заказ на работу должен начаться сразу после его создания, введите **0**.</span><span class="sxs-lookup"><span data-stu-id="95800-116">For example, if the work order should start when it's created, enter **0**.</span></span> <span data-ttu-id="95800-117">Если заказ на работу должен начаться в течение недели после его создания, введите **7**.</span><span class="sxs-lookup"><span data-stu-id="95800-117">If the work order should start within one week after it's created, enter **7**.</span></span>
6. <span data-ttu-id="95800-118">Чтобы задать время начала для заказа на работу в дополнение к дате начала, установите для параметра **Задать время начала** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="95800-118">To set a start time for the work order, in addition to a start date, set the **Set start time** option to **Yes**.</span></span> <span data-ttu-id="95800-119">Затем введите время начала в поле **Время начала**.</span><span class="sxs-lookup"><span data-stu-id="95800-119">Then enter the start time in the **Start time** field.</span></span> <span data-ttu-id="95800-120">Если для параметра выбрано значение **Нет**, используется текущее время дня.</span><span class="sxs-lookup"><span data-stu-id="95800-120">If you set the option to **No**, the current time of day is used.</span></span>
7. <span data-ttu-id="95800-121">В поле **День завершения** введите количество дней, чтобы определить период, в течение которого заказ на работу должен быть завершен.</span><span class="sxs-lookup"><span data-stu-id="95800-121">In the **End day** field, enter a number of days to define the period that the work order should end during.</span></span> <span data-ttu-id="95800-122">Количество дней рассчитывается с даты начала заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="95800-122">The number of days is calculated from the start date of the work order.</span></span> <span data-ttu-id="95800-123">Например, если заказ на работу должен завершиться в течение одной недели с даты начала, введите **7**.</span><span class="sxs-lookup"><span data-stu-id="95800-123">For example, if the work order should end within one week of its start date, enter **7**.</span></span>
8. <span data-ttu-id="95800-124">Чтобы задать время завершения для заказа на работу в дополнение к дате завершения, установите для параметра **Задать время завершения** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="95800-124">To set an end time for the work order, in addition to an end date, set the **Set end time** option to **Yes**.</span></span> <span data-ttu-id="95800-125">Затем введите время завершения в поле **Время завершения**.</span><span class="sxs-lookup"><span data-stu-id="95800-125">Then enter the end time in the **End time** field.</span></span> <span data-ttu-id="95800-126">Если для параметра выбрано значение **Нет**, используется текущее время дня.</span><span class="sxs-lookup"><span data-stu-id="95800-126">If you set the option to **No**, the current time of day is used.</span></span>
9. <span data-ttu-id="95800-127">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="95800-127">Select **Save**.</span></span>

![Страница уровня обслуживания по заказу на работу](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a><span data-ttu-id="95800-129">Создание описания</span><span class="sxs-lookup"><span data-stu-id="95800-129">Create a description</span></span>

1. <span data-ttu-id="95800-130">Выберите **Управление активами** \> **Настройка** \> **Заказы на работу** \> **Описания**.</span><span class="sxs-lookup"><span data-stu-id="95800-130">Select **Asset management** \> **Setup** \> **Work orders** \> **Descriptions**.</span></span>
2. <span data-ttu-id="95800-131">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="95800-131">Select **New**.</span></span>
3. <span data-ttu-id="95800-132">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="95800-132">In the **Description** field, enter the description.</span></span>
4. <span data-ttu-id="95800-133">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="95800-133">Select **Save**.</span></span>
