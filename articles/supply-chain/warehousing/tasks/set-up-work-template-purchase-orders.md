--- 
title: "Настройка рабочего шаблона для заказов на покупку"
description: "Эта процедура описывает настройку простого шаблона работы, который следует использовать при размещении полученных номенклатур."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 4c388a8ed6a852a92caa3a1eff2d0e8017694bcd
ms.contentlocale: ru-ru
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="7f864-103">Настройка рабочего шаблона для заказов на покупку</span><span class="sxs-lookup"><span data-stu-id="7f864-103">Set up a work template for purchase orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7f864-104">Эта процедура описывает настройку простого шаблона работы, который следует использовать при размещении полученных номенклатур.</span><span class="sxs-lookup"><span data-stu-id="7f864-104">This procedure focuses on the set up of a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="7f864-105">Шаблоны работы определяют набор инструкций, представленных работнику склада на мобильном устройстве при перемещении номенклатур из зоны получения.</span><span class="sxs-lookup"><span data-stu-id="7f864-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="7f864-106">Эту процедуру можно использовать с данными в компании с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="7f864-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="7f864-107">Перед началом этого руководства создайте код пула работы.</span><span class="sxs-lookup"><span data-stu-id="7f864-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="7f864-108">В этом примере используется код пула работы с названием "Входящие".</span><span class="sxs-lookup"><span data-stu-id="7f864-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="7f864-109">Эта процедура предназначена для менеджера склада.</span><span class="sxs-lookup"><span data-stu-id="7f864-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="7f864-110">Перейдите в раздел "Управление складом" > "Настройка" > "Работа" > "Шаблоны работ".</span><span class="sxs-lookup"><span data-stu-id="7f864-110">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="7f864-111">В поле "Тип заказа на выполнение работ" выберите "Заказ на покупку".</span><span class="sxs-lookup"><span data-stu-id="7f864-111">In the Work order type field, select 'Purchase orders'.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="7f864-112">Создание заголовка шаблона работы</span><span class="sxs-lookup"><span data-stu-id="7f864-112">Create a work template header</span></span>
1. <span data-ttu-id="7f864-113">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="7f864-113">Click New.</span></span>
2. <span data-ttu-id="7f864-114">В поле "Порядковый номер" введите число.</span><span class="sxs-lookup"><span data-stu-id="7f864-114">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="7f864-115">Это последовательность, в которой оцениваются шаблоны работы.</span><span class="sxs-lookup"><span data-stu-id="7f864-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="7f864-116">При необходимости последовательность можно изменить.</span><span class="sxs-lookup"><span data-stu-id="7f864-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="7f864-117">В поле "Шаблон работы" введите значение.</span><span class="sxs-lookup"><span data-stu-id="7f864-117">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="7f864-118">Это уникальный идентификатор для этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="7f864-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="7f864-119">В поле "Описание шаблона работы" введите значение.</span><span class="sxs-lookup"><span data-stu-id="7f864-119">In the Work template description field, type a value.</span></span>
    * <span data-ttu-id="7f864-120">Параметр "Допустимо" не должен быть установлен, пока не завершены все сведения, требуемые для шаблона и затем не нажато "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="7f864-120">The Valid option will not be checked until you’ve completed all the information that's needed by the template and have then clicked Save.</span></span>  
    * <span data-ttu-id="7f864-121">Заказ на выполнение работ типа "заказ на покупку" не может быть автоматически обработан, поэтому оставьте значение параметра "Автоматическая обработка" как "Нет".</span><span class="sxs-lookup"><span data-stu-id="7f864-121">A work order of type Purchase order cannot be automatically processed, so leave the  Automatically process option set to No.</span></span>  
5. <span data-ttu-id="7f864-122">В поле "Код пула работы" введите значение.</span><span class="sxs-lookup"><span data-stu-id="7f864-122">In the Work pool ID field, type a value.</span></span>
    * <span data-ttu-id="7f864-123">Коды пулов работ можно использовать для организации работы в группы.</span><span class="sxs-lookup"><span data-stu-id="7f864-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="7f864-124">Значение, которые задано здесь, будет значением по умолчанию для любой работы, созданной с использованием этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="7f864-124">The value that you set here will be the default value for any work that’s created using this template.</span></span>  
6. <span data-ttu-id="7f864-125">В поле "Приоритет работы" введите "1".</span><span class="sxs-lookup"><span data-stu-id="7f864-125">In the Work priority field, enter '1'.</span></span>
    * <span data-ttu-id="7f864-126">Это означает важность работы и значение, которое задано здесь, будет использоваться по умолчанию для любой работы, созданной с использованием этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="7f864-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="7f864-127">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="7f864-127">Click Save.</span></span>
    * <span data-ttu-id="7f864-128">Необходимо сохранить заголовок шаблона работы, прежде чем кнопка "Изменить запрос" становится доступной.</span><span class="sxs-lookup"><span data-stu-id="7f864-128">You must save the work template header before the Edit Query button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="7f864-129">Настройка запроса для шаблона работы</span><span class="sxs-lookup"><span data-stu-id="7f864-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="7f864-130">Щелкните "Изменить запрос".</span><span class="sxs-lookup"><span data-stu-id="7f864-130">Click Edit query.</span></span>
    * <span data-ttu-id="7f864-131">Мы зададим ограничение, чтобы шаблон можно было использовать только в рамках конкретного склада.</span><span class="sxs-lookup"><span data-stu-id="7f864-131">We’ll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="7f864-132">Нажмите кнопку Добавить.</span><span class="sxs-lookup"><span data-stu-id="7f864-132">Click Add.</span></span>
3. <span data-ttu-id="7f864-133">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="7f864-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="7f864-134">В поле "Поле" введите "склад".</span><span class="sxs-lookup"><span data-stu-id="7f864-134">In the Field field, type 'warehouse'.</span></span>
5. <span data-ttu-id="7f864-135">В поле "Критерии" введите значение.</span><span class="sxs-lookup"><span data-stu-id="7f864-135">In the Criteria field, type a value.</span></span>
6. <span data-ttu-id="7f864-136">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="7f864-136">Click OK.</span></span>
7. <span data-ttu-id="7f864-137">Щелкните Да.</span><span class="sxs-lookup"><span data-stu-id="7f864-137">Click Yes.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="7f864-138">Задание сведений шаблона работы</span><span class="sxs-lookup"><span data-stu-id="7f864-138">Set work template details</span></span>
1. <span data-ttu-id="7f864-139">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="7f864-139">Click New.</span></span>
2. <span data-ttu-id="7f864-140">В поле "Тип работы" выберите "Комплектация".</span><span class="sxs-lookup"><span data-stu-id="7f864-140">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="7f864-141">В поле "Код класса работы" введите "покупка".</span><span class="sxs-lookup"><span data-stu-id="7f864-141">In the Work class ID field, type 'purchase'.</span></span>
    * <span data-ttu-id="7f864-142">Класс работы, заданный здесь, будет использоваться по умолчанию во всех строках работы типа "комплектация", созданных с использованием этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="7f864-142">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="7f864-143">Класс работы нельзя переопределить из строк заказа на выполнение работ.</span><span class="sxs-lookup"><span data-stu-id="7f864-143">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="7f864-144">Классы работ используются для направления и/или ограничения типа строк заказа на выполнение работ, которые работник склада может обрабатывать на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="7f864-144">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="7f864-145">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="7f864-145">Click New.</span></span>
5. <span data-ttu-id="7f864-146">В поле "Тип работы" выберите "Поместить".</span><span class="sxs-lookup"><span data-stu-id="7f864-146">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="7f864-147">В поле "Код класса работы" введите значение.</span><span class="sxs-lookup"><span data-stu-id="7f864-147">In the Work class ID field, type a value.</span></span>
    * <span data-ttu-id="7f864-148">Инструкции по комплектации и размещению являются набором.</span><span class="sxs-lookup"><span data-stu-id="7f864-148">The pick and put instructions are a set.</span></span> <span data-ttu-id="7f864-149">Пары "комплектация/размещение" должны иметь один и тот же класс работ.</span><span class="sxs-lookup"><span data-stu-id="7f864-149">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="7f864-150">Используйте один и тот же класс работ, предоставленный для инструкции комплектации.</span><span class="sxs-lookup"><span data-stu-id="7f864-150">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="7f864-151">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="7f864-151">Click Save.</span></span>
    * <span data-ttu-id="7f864-152">Обратите внимание, что теперь флажок "Допустимо" установлен.</span><span class="sxs-lookup"><span data-stu-id="7f864-152">Note that the Valid checkbox is now checked.</span></span>  


