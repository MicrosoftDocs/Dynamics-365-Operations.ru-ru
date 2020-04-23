---
title: Настройка рабочего шаблона для заказов на покупку
description: В этой теме описывается настройка простого шаблона работы, который следует использовать при размещении полученных номенклатур.
author: ShylaThompson
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a3e91fe67ed97b37bfb89f5f487e2bc59c3f7bb8
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216766"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="f1fe4-103">Настройка рабочего шаблона для заказов на покупку</span><span class="sxs-lookup"><span data-stu-id="f1fe4-103">Set up a work template for purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f1fe4-104">В этой теме описывается настройка простого шаблона работы, который следует использовать при размещении полученных номенклатур.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-104">This topic describes how to set up a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="f1fe4-105">Шаблоны работы определяют набор инструкций, представленных работнику склада на мобильном устройстве при перемещении номенклатур из зоны получения.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="f1fe4-106">Эту процедуру можно использовать с данными в компании с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="f1fe4-107">Перед началом этого руководства создайте код пула работы.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="f1fe4-108">В этом примере используется код пула работы с названием "Входящие".</span><span class="sxs-lookup"><span data-stu-id="f1fe4-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="f1fe4-109">Эта процедура предназначена для менеджера склада.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="f1fe4-110">В области перехода выберите **Модули > Управление складом > Настройка > Работа > Шаблоны работы**.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-110">In the navigation pane, go to **Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="f1fe4-111">В поле **Тип заказа на работу** выберите **Заказ на покупку**.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-111">In the **Work order type** field, select **Purchase orders**.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="f1fe4-112">Создание заголовка шаблона работы</span><span class="sxs-lookup"><span data-stu-id="f1fe4-112">Create a work template header</span></span>
1. <span data-ttu-id="f1fe4-113">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-113">Select **New**.</span></span>
2. <span data-ttu-id="f1fe4-114">В поле **Порядковый номер** введите число.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-114">In the **Sequence number** field, enter a number.</span></span> <span data-ttu-id="f1fe4-115">Это последовательность, в которой оцениваются шаблоны работы.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="f1fe4-116">При необходимости последовательность можно изменить.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="f1fe4-117">В поле **Шаблон работы** введите значение.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-117">In the **Work template** field, type a value.</span></span> <span data-ttu-id="f1fe4-118">Это уникальный идентификатор для этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="f1fe4-119">В поле **Описание шаблона работы** введите значение.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-119">In the **Work template description** field, type a value.</span></span>
    - <span data-ttu-id="f1fe4-120">Параметр **Допустимо** не должен быть установлен, пока не завершены все сведения, требуемые для шаблона и затем не выбрано **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-120">The **Valid** option will not be checked until you've completed all the information that's needed by the template and have then selected **Save**.</span></span>  
    - <span data-ttu-id="f1fe4-121">Заказ на выполнение работ типа **Заказ на покупку** не может быть автоматически обработан, поэтому оставьте значение параметра **Автоматическая обработка** как **Нет**.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-121">A work order of type **Purchase order** cannot be automatically processed, so leave the **Automatically process** option set to **No**.</span></span>  
5. <span data-ttu-id="f1fe4-122">В поле **Код пула работы** введите значение.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-122">In the **Work pool ID** field, type a value.</span></span> <span data-ttu-id="f1fe4-123">Коды пулов работ можно использовать для организации работы в группы.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="f1fe4-124">Значение, которые задано здесь, будет значением по умолчанию для любой работы, созданной с использованием этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-124">The value that you set here will be the default value for any work that's created using this template.</span></span>  
6. <span data-ttu-id="f1fe4-125">В поле **Приоритет работы** введите `1`.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-125">In the **Work priority** field, enter `1`.</span></span> <span data-ttu-id="f1fe4-126">Это означает важность работы и значение, которое задано здесь, будет использоваться по умолчанию для любой работы, созданной с использованием этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="f1fe4-127">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-127">Select **Save**.</span></span> <span data-ttu-id="f1fe4-128">Необходимо сохранить заголовок шаблона работы, прежде чем кнопка **Изменить запрос** становится доступной.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-128">You must save the work template header before the **Edit Query** button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="f1fe4-129">Настройка запроса для шаблона работы</span><span class="sxs-lookup"><span data-stu-id="f1fe4-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="f1fe4-130">Выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-130">Select **Edit query**.</span></span> <span data-ttu-id="f1fe4-131">Мы зададим ограничение, чтобы шаблон можно было использовать только в рамках конкретного склада.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-131">We'll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="f1fe4-132">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-132">Select **Add**.</span></span>
3. <span data-ttu-id="f1fe4-133">В поле **Поля** новой строки введите `warehouse`.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-133">In the **Field** field of the new row, type `warehouse`.</span></span>
4. <span data-ttu-id="f1fe4-134">В поле **Критерии** введите значение.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-134">In the **Criteria** field, type a value.</span></span>
5. <span data-ttu-id="f1fe4-135">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-135">Select **OK**.</span></span>
6. <span data-ttu-id="f1fe4-136">Выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-136">Select **Yes**.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="f1fe4-137">Задание сведений шаблона работы</span><span class="sxs-lookup"><span data-stu-id="f1fe4-137">Set work template details</span></span>
1. <span data-ttu-id="f1fe4-138">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-138">Select **New**.</span></span>
2. <span data-ttu-id="f1fe4-139">В поле **Тип работы** выберите **Комплектация**.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-139">In the **Work type** field, select **Pick**.</span></span>
3. <span data-ttu-id="f1fe4-140">В поле **Код класса работы** введите `purchase`.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-140">In the **Work class ID** field, type `purchase`.</span></span> <span data-ttu-id="f1fe4-141">Класс работы, заданный здесь, будет использоваться по умолчанию во всех строках работы типа "комплектация", созданных с использованием этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-141">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="f1fe4-142">Класс работы нельзя переопределить из строк заказа на выполнение работ.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-142">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="f1fe4-143">Классы работ используются для направления и/или ограничения типа строк заказа на выполнение работ, которые работник склада может обрабатывать на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-143">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="f1fe4-144">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-144">Select **New**.</span></span>
5. <span data-ttu-id="f1fe4-145">В поле **Тип работы** выберите **Поместить**.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-145">In the **Work type** field, select **Put**.</span></span>
6. <span data-ttu-id="f1fe4-146">В поле **Код класса работы** введите значение.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-146">In the **Work class ID** field, type a value.</span></span> <span data-ttu-id="f1fe4-147">Инструкции по комплектации и размещению являются набором.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-147">The pick and put instructions are a set.</span></span> <span data-ttu-id="f1fe4-148">Пары "комплектация/размещение" должны иметь один и тот же класс работ.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-148">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="f1fe4-149">Используйте один и тот же класс работ, предоставленный для инструкции комплектации.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-149">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="f1fe4-150">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-150">Select **Save**.</span></span> <span data-ttu-id="f1fe4-151">Обратите внимание, что теперь флажок **Допустимо** установлен.</span><span class="sxs-lookup"><span data-stu-id="f1fe4-151">Note that the **Valid** checkbox is now checked.</span></span>  

