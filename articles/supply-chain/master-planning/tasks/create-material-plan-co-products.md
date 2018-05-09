--- 
title: "Создание плана материалов для сопутствующих продуктов"
description: "Планировщик производства планирует материальные потребности в номенклатурах, представляющих собой сопутствующие продукты формулы."
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f3a411e8fc773957b5ce3f24749242d9d0c6ffd0
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="462e1-103">Создание плана материалов для сопутствующих продуктов</span><span class="sxs-lookup"><span data-stu-id="462e1-103">Create a material plan for co-products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="462e1-104">Планировщик производства планирует материальные потребности в номенклатурах, представляющих собой сопутствующие продукты формулы.</span><span class="sxs-lookup"><span data-stu-id="462e1-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="462e1-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USP2.</span><span class="sxs-lookup"><span data-stu-id="462e1-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="462e1-106">Создание потребности для сопутствующего продукта</span><span class="sxs-lookup"><span data-stu-id="462e1-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="462e1-107">Перейдите на панель мониторинга по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="462e1-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="462e1-108">Щелкните "Обработка и запрос заказов на продажу".</span><span class="sxs-lookup"><span data-stu-id="462e1-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="462e1-109">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="462e1-109">Click New.</span></span>
4. <span data-ttu-id="462e1-110">Щелкните "Заказ на продажу".</span><span class="sxs-lookup"><span data-stu-id="462e1-110">Click Sales order.</span></span>
5. <span data-ttu-id="462e1-111">В поле "Счет клиента" введите значение.</span><span class="sxs-lookup"><span data-stu-id="462e1-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="462e1-112">Пример: US-001</span><span class="sxs-lookup"><span data-stu-id="462e1-112">Example: US-001</span></span>  
6. <span data-ttu-id="462e1-113">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="462e1-113">Click OK.</span></span>
7. <span data-ttu-id="462e1-114">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="462e1-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="462e1-115">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="462e1-115">Example: P6003</span></span>  
8. <span data-ttu-id="462e1-116">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="462e1-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="462e1-117">Пример: 50000</span><span class="sxs-lookup"><span data-stu-id="462e1-117">Example: 50000</span></span>  
9. <span data-ttu-id="462e1-118">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="462e1-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="462e1-119">Создание плана материалов для сопутствующих продуктов</span><span class="sxs-lookup"><span data-stu-id="462e1-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="462e1-120">Щелкните "Сводное планирование".</span><span class="sxs-lookup"><span data-stu-id="462e1-120">Click Master planning.</span></span>
2. <span data-ttu-id="462e1-121">В поле "План" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="462e1-121">In the Plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="462e1-122">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="462e1-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="462e1-123">Пример: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="462e1-123">Example: MasterPlan</span></span>  
4. <span data-ttu-id="462e1-124">Щелкните "Выполнить".</span><span class="sxs-lookup"><span data-stu-id="462e1-124">Click Run.</span></span>
5. <span data-ttu-id="462e1-125">Разверните или сверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="462e1-125">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="462e1-126">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="462e1-126">Click Filter.</span></span>
7. <span data-ttu-id="462e1-127">Выберите в списке строку, где Поле = Номер номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="462e1-127">In the list, select the row for Field = Item number.</span></span>
8. <span data-ttu-id="462e1-128">В поле "Критерии" введите значение.</span><span class="sxs-lookup"><span data-stu-id="462e1-128">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="462e1-129">Пример: P6003</span><span class="sxs-lookup"><span data-stu-id="462e1-129">Example: P6003</span></span>  
9. <span data-ttu-id="462e1-130">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="462e1-130">Click OK.</span></span>
10. <span data-ttu-id="462e1-131">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="462e1-131">Click OK.</span></span>
11. <span data-ttu-id="462e1-132">Щелкните "Спланированные заказы".</span><span class="sxs-lookup"><span data-stu-id="462e1-132">Click Planned orders.</span></span>
12. <span data-ttu-id="462e1-133">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="462e1-133">Use the Quick Filter to find records.</span></span> <span data-ttu-id="462e1-134">Например, отфильтруйте поле "Номер номенклатуры" по значению "P6000".</span><span class="sxs-lookup"><span data-stu-id="462e1-134">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="462e1-135">Установите фильтр по номенклатуре-формуле, в которой присутствует сопутствующий продукт номенклатуры, для которой вы создали заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="462e1-135">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
13. <span data-ttu-id="462e1-136">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="462e1-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="462e1-137">Выберите любую из строк, возращенных фильтром.</span><span class="sxs-lookup"><span data-stu-id="462e1-137">Select any of the rows returned by the filter.</span></span>  
14. <span data-ttu-id="462e1-138">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="462e1-138">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="462e1-139">Разверните или сверните раздел "Фиксация".</span><span class="sxs-lookup"><span data-stu-id="462e1-139">Expand or collapse the Pegging section.</span></span>
16. <span data-ttu-id="462e1-140">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="462e1-140">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="462e1-141">Спланированный заказ прикрепляется к заказу на продажу сопутствующего продукта.</span><span class="sxs-lookup"><span data-stu-id="462e1-141">The planned order is pegged to the sales order for the co-product.</span></span>  
17. <span data-ttu-id="462e1-142">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="462e1-142">Close the page.</span></span>


