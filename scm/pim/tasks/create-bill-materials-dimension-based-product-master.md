--- 
title: "Создание спецификации для шаблона продукта на основе аналитик"
description: "Для данной процедуры необходимо завершить предыдущие 4 руководства в этой последовательности из восьми записей."
author: YuyuScheller
manager: AnnBe
ms.date: 06/21/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 4f9f9473d0872d68571b87409b93e0cf5455364c
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="6c788-103">Создание спецификации для шаблона продукта на основе аналитик</span><span class="sxs-lookup"><span data-stu-id="6c788-103">Create a bill of materials for a dimension-based product master</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6c788-104">Для данной процедуры необходимо завершить предыдущие 4 руководства в этой последовательности из восьми записей.</span><span class="sxs-lookup"><span data-stu-id="6c788-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="6c788-105">В первых 4 записях настраиваются данные, необходимые для завершения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="6c788-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="6c788-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="6c788-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6c788-107">Обычно эта задача выполняется конструктором продуктов.</span><span class="sxs-lookup"><span data-stu-id="6c788-107">This task is typically handled by the product designer.</span></span>


## <a name="select-the-product"></a><span data-ttu-id="6c788-108">Выбор продукта</span><span class="sxs-lookup"><span data-stu-id="6c788-108">Select the product</span></span>
1. <span data-ttu-id="6c788-109">Щелкните "Обслуживание выпущенного продукта".</span><span class="sxs-lookup"><span data-stu-id="6c788-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="6c788-110">Щелкните "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="6c788-110">Click Released products.</span></span>
3. <span data-ttu-id="6c788-111">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="6c788-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6c788-112">Найдите выпущенный шаблон продукта с помощью технологии конфигурации на основе аналитик, созданной в первом руководстве по задаче в этой последовательности.</span><span class="sxs-lookup"><span data-stu-id="6c788-112">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
4. <span data-ttu-id="6c788-113">В области действий щелкните "Инжиниринг".</span><span class="sxs-lookup"><span data-stu-id="6c788-113">On the Action Pane, click Engineer.</span></span>
5. <span data-ttu-id="6c788-114">Щелкните "Версии спецификации".</span><span class="sxs-lookup"><span data-stu-id="6c788-114">Click BOM versions.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="6c788-115">Создание новой спецификации и версии спецификации</span><span class="sxs-lookup"><span data-stu-id="6c788-115">Create new BOM and BOM version</span></span>
1. <span data-ttu-id="6c788-116">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="6c788-116">Click New.</span></span>
2. <span data-ttu-id="6c788-117">Щелкните спецификацию и версию спецификации.</span><span class="sxs-lookup"><span data-stu-id="6c788-117">Click BOM and BOM version.</span></span>
3. <span data-ttu-id="6c788-118">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="6c788-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="6c788-119">Настройка сайта</span><span class="sxs-lookup"><span data-stu-id="6c788-119">Setting a site</span></span>  
    * <span data-ttu-id="6c788-120">В этой процедуре мы не настраиваем определенный сайт для спецификации.</span><span class="sxs-lookup"><span data-stu-id="6c788-120">In this procedure we don't set a specific site for the BOM.</span></span>  
4. <span data-ttu-id="6c788-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="6c788-121">Click OK.</span></span>
5. <span data-ttu-id="6c788-122">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="6c788-122">Click New.</span></span>
    * <span data-ttu-id="6c788-123">В этой процедуре мы добавим четыре строки в спецификацию.</span><span class="sxs-lookup"><span data-stu-id="6c788-123">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="6c788-124">Две строки представляют параметры кабеля и две строки представляют параметры шкафа.</span><span class="sxs-lookup"><span data-stu-id="6c788-124">Two lines represent cable options and two lines represent cabinet options.</span></span>  
6. <span data-ttu-id="6c788-125">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="6c788-125">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="6c788-126">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6c788-126">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="6c788-127">Выберите код номенклатуры A0001, кабели 6' HDMI.</span><span class="sxs-lookup"><span data-stu-id="6c788-127">Select item number A0001, HDMI 6' Cables.</span></span>  
8. <span data-ttu-id="6c788-128">В поле "Конфигурационная группа" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6c788-128">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="6c788-129">Выберите конфигурационную группу кабеля, созданную в руководстве 4 в этой последовательности.</span><span class="sxs-lookup"><span data-stu-id="6c788-129">Select the Cable configuration group created in guide 4 in this sequence.</span></span>  
9. <span data-ttu-id="6c788-130">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="6c788-130">Click New.</span></span>
    * <span data-ttu-id="6c788-131">Выберите код номенклатуры A0002, кабели 12' HDMI.</span><span class="sxs-lookup"><span data-stu-id="6c788-131">Select item number A0002, HDMI 12' Cables.</span></span>  
10. <span data-ttu-id="6c788-132">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="6c788-132">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="6c788-133">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6c788-133">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="6c788-134">В поле "Конфигурационная группа" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6c788-134">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="6c788-135">Выберите конфигурационную группу кабеля еще раз.</span><span class="sxs-lookup"><span data-stu-id="6c788-135">Select the Cable configuration group again.</span></span>  
13. <span data-ttu-id="6c788-136">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="6c788-136">Click New.</span></span>
14. <span data-ttu-id="6c788-137">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="6c788-137">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="6c788-138">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6c788-138">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="6c788-139">Выберите код номенклатуры D0002, шкаф.</span><span class="sxs-lookup"><span data-stu-id="6c788-139">Select item number D0002 Cabinet.</span></span>  
16. <span data-ttu-id="6c788-140">В поле "Конфигурационная группа" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6c788-140">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="6c788-141">Выберите конфигурационную группу шкафа для данной строки спецификации.</span><span class="sxs-lookup"><span data-stu-id="6c788-141">Select the Cabinet configuration group for this BOM line.</span></span>  
17. <span data-ttu-id="6c788-142">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="6c788-142">Click New.</span></span>
18. <span data-ttu-id="6c788-143">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="6c788-143">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="6c788-144">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6c788-144">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="6c788-145">Выберите код номенклатуры M0007 StandardCabinet в качестве последней строки спецификации.</span><span class="sxs-lookup"><span data-stu-id="6c788-145">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
20. <span data-ttu-id="6c788-146">В поле "Конфигурационная группа" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6c788-146">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="6c788-147">Выберите конфигурационную группу шкафа для последней строки спецификации.</span><span class="sxs-lookup"><span data-stu-id="6c788-147">Select the Cabinet configuration group for the laste BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="6c788-148">Утвердить и активировать</span><span class="sxs-lookup"><span data-stu-id="6c788-148">Approve and activate</span></span>
1. <span data-ttu-id="6c788-149">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="6c788-149">Close the page.</span></span>
2. <span data-ttu-id="6c788-150">Нажмите кнопку Одобрить.</span><span class="sxs-lookup"><span data-stu-id="6c788-150">Click Approve.</span></span>
3. <span data-ttu-id="6c788-151">В поле "Кем утверждено" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6c788-151">In the Approved by field, enter or select a value.</span></span>
4. <span data-ttu-id="6c788-152">Выберите значение "Да" в поле "Также утвердить спецификацию?" .</span><span class="sxs-lookup"><span data-stu-id="6c788-152">Select Yes in the Do you also want to approve the bill of materials? field.</span></span>
5. <span data-ttu-id="6c788-153">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="6c788-153">Click OK.</span></span>
6. <span data-ttu-id="6c788-154">Нажмите кнопку Активировать.</span><span class="sxs-lookup"><span data-stu-id="6c788-154">Click Activate.</span></span>


