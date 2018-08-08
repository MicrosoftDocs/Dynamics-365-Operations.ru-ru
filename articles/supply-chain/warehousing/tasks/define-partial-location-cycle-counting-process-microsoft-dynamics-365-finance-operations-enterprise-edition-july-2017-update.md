--- 
title: "Определение процесса частичного подсчета циклов для местонахождения"
description: "При использовании планов подсчета циклов для создания работы подсчета можно руководить фактическими операциями подсчета, запросив, чтобы подсчитывались только конкретные продукты и варианты продуктов, а не все запасы в наличии в местонахождении."
author: ShylaThompson
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 3aafb42cea1664b0629f57fe4492736601902cc1
ms.contentlocale: ru-ru
ms.lasthandoff: 08/07/2018

---
# <a name="define-partial-location-cycle-counting-process"></a><span data-ttu-id="ac35f-103">Определение процесса частичного подсчета циклов для местонахождения</span><span class="sxs-lookup"><span data-stu-id="ac35f-103">Define partial location cycle counting process</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ac35f-104">При использовании планов подсчета циклов для создания работы подсчета можно руководить фактическими операциями подсчета, запросив, чтобы подсчитывались только конкретные продукты и варианты продуктов, а не все запасы в наличии в местонахождении.</span><span class="sxs-lookup"><span data-stu-id="ac35f-104">When you use cycle count plans to create counting work, you can guide the actual counting operations by requesting that only specific products and product variants be counted instead of all on-hand inventory at the location.</span></span> <span data-ttu-id="ac35f-105">С помощью фильтрации по конкретным продуктам менеджер склада может уменьшить накладные расходы для рассмотрения, избежать ошибок консолидации и сэкономить время.</span><span class="sxs-lookup"><span data-stu-id="ac35f-105">By filtering on specific products, the warehouse manager can reduce review overhead, help prevent consolidation mistakes, and save time.</span></span> <span data-ttu-id="ac35f-106">Обычно задачи по настройке выполняет менеджер склада.</span><span class="sxs-lookup"><span data-stu-id="ac35f-106">Typically, a warehouse manager performs the setup tasks.</span></span> <span data-ttu-id="ac35f-107">Выполнить процедуру можно в компании с демонстрационными данными USMF или с вашими собственными данными.</span><span class="sxs-lookup"><span data-stu-id="ac35f-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="create-a-cycle-counting-work-template"></a><span data-ttu-id="ac35f-108">Создание шаблона работы подсчета циклов</span><span class="sxs-lookup"><span data-stu-id="ac35f-108">Create a cycle counting work template</span></span>
1. <span data-ttu-id="ac35f-109">Перейдите в раздел "Управление складом" > "Настройка" > "Работа" > "Шаблоны работ".</span><span class="sxs-lookup"><span data-stu-id="ac35f-109">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="ac35f-110">В поле "Тип заказа на выполнение работ" выберите "Цикличный подсчет".</span><span class="sxs-lookup"><span data-stu-id="ac35f-110">In the Work order type field, select 'Cycle counting'.</span></span>
3. <span data-ttu-id="ac35f-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="ac35f-111">Click New.</span></span>
4. <span data-ttu-id="ac35f-112">В поле "Порядковый номер" введите число.</span><span class="sxs-lookup"><span data-stu-id="ac35f-112">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="ac35f-113">Порядок сортировки — от наименьшего до наибольшего числа.</span><span class="sxs-lookup"><span data-stu-id="ac35f-113">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="ac35f-114">Значение должно быть больше нуля.</span><span class="sxs-lookup"><span data-stu-id="ac35f-114">The value must be more than 0 (zero).</span></span>  
5. <span data-ttu-id="ac35f-115">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="ac35f-115">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="ac35f-116">В поле "Шаблон работы" введите значение.</span><span class="sxs-lookup"><span data-stu-id="ac35f-116">In the Work template field, type a value.</span></span>
7. <span data-ttu-id="ac35f-117">В поле "Описание шаблона работы" введите значение.</span><span class="sxs-lookup"><span data-stu-id="ac35f-117">In the Work template description field, type a value.</span></span>
8. <span data-ttu-id="ac35f-118">В поле "Код пула работ" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="ac35f-118">In the Work pool ID field, enter or select a value.</span></span>
9. <span data-ttu-id="ac35f-119">В поле "Приоритет работы" введите число.</span><span class="sxs-lookup"><span data-stu-id="ac35f-119">In the Work priority field, enter a number.</span></span>
10. <span data-ttu-id="ac35f-120">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="ac35f-120">Click Save.</span></span>
11. <span data-ttu-id="ac35f-121">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="ac35f-121">Click New.</span></span>
12. <span data-ttu-id="ac35f-122">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="ac35f-122">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="ac35f-123">В поле "Тип работы" выберите "Инвентаризация".</span><span class="sxs-lookup"><span data-stu-id="ac35f-123">In the Work type field, select 'Counting'.</span></span>
14. <span data-ttu-id="ac35f-124">В поле "Код класса работы" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="ac35f-124">In the Work class ID field, enter or select a value.</span></span>
15. <span data-ttu-id="ac35f-125">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="ac35f-125">Click Save.</span></span>
16. <span data-ttu-id="ac35f-126">Щелкните "Разрывы строки работы".</span><span class="sxs-lookup"><span data-stu-id="ac35f-126">Click Work line breaks.</span></span>
17. <span data-ttu-id="ac35f-127">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="ac35f-127">Click New.</span></span>
18. <span data-ttu-id="ac35f-128">В поле "Порядковый номер" введите число.</span><span class="sxs-lookup"><span data-stu-id="ac35f-128">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="ac35f-129">Порядок сортировки — от наименьшего до наибольшего числа.</span><span class="sxs-lookup"><span data-stu-id="ac35f-129">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="ac35f-130">Значение должно быть больше нуля.</span><span class="sxs-lookup"><span data-stu-id="ac35f-130">The value must be more than 0 (zero).</span></span>  
19. <span data-ttu-id="ac35f-131">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="ac35f-131">Click Save.</span></span>
20. <span data-ttu-id="ac35f-132">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ac35f-132">Close the page.</span></span>
21. <span data-ttu-id="ac35f-133">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ac35f-133">Close the page.</span></span>

## <a name="create-a-cycle-counting-plan"></a><span data-ttu-id="ac35f-134">Создание плана подсчета циклов</span><span class="sxs-lookup"><span data-stu-id="ac35f-134">Create a cycle counting plan</span></span>
1. <span data-ttu-id="ac35f-135">Перейдите в раздел "Управление складом" > "Настройка" > "Подсчет циклов" > "Планы подсчета циклов".</span><span class="sxs-lookup"><span data-stu-id="ac35f-135">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="ac35f-136">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="ac35f-136">Click New.</span></span>
3. <span data-ttu-id="ac35f-137">В поле "Код плана подсчета циклов" введите значение.</span><span class="sxs-lookup"><span data-stu-id="ac35f-137">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="ac35f-138">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="ac35f-138">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ac35f-139">В поле "Максимальное количество подсчетов циклов" введите число.</span><span class="sxs-lookup"><span data-stu-id="ac35f-139">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="ac35f-140">В поле "Шаблон работы" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="ac35f-140">In the Work template field, enter or select a value.</span></span>
7. <span data-ttu-id="ac35f-141">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="ac35f-141">Click New.</span></span>
8. <span data-ttu-id="ac35f-142">В поле "Порядковый номер" введите число.</span><span class="sxs-lookup"><span data-stu-id="ac35f-142">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="ac35f-143">Порядок сортировки — от наименьшего до наибольшего числа.</span><span class="sxs-lookup"><span data-stu-id="ac35f-143">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="ac35f-144">Значение должно быть больше нуля.</span><span class="sxs-lookup"><span data-stu-id="ac35f-144">The value must be more than 0 (zero).</span></span>  
9. <span data-ttu-id="ac35f-145">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="ac35f-145">In the Description field, type a value.</span></span>
10. <span data-ttu-id="ac35f-146">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="ac35f-146">Click Save.</span></span>
11. <span data-ttu-id="ac35f-147">Щелкните "Определить запрос продукта".</span><span class="sxs-lookup"><span data-stu-id="ac35f-147">Click Define product query.</span></span>
12. <span data-ttu-id="ac35f-148">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="ac35f-148">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="ac35f-149">В поле "Критерии" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="ac35f-149">In the Criteria field, enter or select a value.</span></span>
14. <span data-ttu-id="ac35f-150">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="ac35f-150">Click OK.</span></span>
15. <span data-ttu-id="ac35f-151">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="ac35f-151">Close the page.</span></span>


