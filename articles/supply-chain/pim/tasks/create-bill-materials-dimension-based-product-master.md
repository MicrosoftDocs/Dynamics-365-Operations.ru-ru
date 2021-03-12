---
title: Создание спецификации для шаблона продукта на основе аналитик
description: Для данной процедуры необходимо завершить предыдущие 4 руководства в этой последовательности из восьми записей.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ffe30f1b5aae3e954b527e84648f4dbb4b181513
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986912"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="bd335-103">Создание спецификации для шаблона продукта на основе аналитик</span><span class="sxs-lookup"><span data-stu-id="bd335-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bd335-104">Для данной процедуры необходимо завершить предыдущие 4 руководства в этой последовательности из восьми записей.</span><span class="sxs-lookup"><span data-stu-id="bd335-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="bd335-105">В первых 4 записях настраиваются данные, необходимые для завершения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="bd335-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="bd335-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="bd335-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="bd335-107">Обычно эта задача выполняется конструктором продуктов.</span><span class="sxs-lookup"><span data-stu-id="bd335-107">This task is typically handled by the product designer.</span></span>


## <a name="select-the-product"></a><span data-ttu-id="bd335-108">Выбор продукта</span><span class="sxs-lookup"><span data-stu-id="bd335-108">Select the product</span></span>
1. <span data-ttu-id="bd335-109">Щелкните "Обслуживание выпущенного продукта".</span><span class="sxs-lookup"><span data-stu-id="bd335-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="bd335-110">Щелкните "Выпущенные продукты".</span><span class="sxs-lookup"><span data-stu-id="bd335-110">Click Released products.</span></span>
3. <span data-ttu-id="bd335-111">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="bd335-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="bd335-112">Найдите выпущенный шаблон продукта с помощью технологии конфигурации на основе аналитик, созданной в первом руководстве по задаче в этой последовательности.</span><span class="sxs-lookup"><span data-stu-id="bd335-112">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
4. <span data-ttu-id="bd335-113">В области действий щелкните "Инжиниринг".</span><span class="sxs-lookup"><span data-stu-id="bd335-113">On the Action Pane, click Engineer.</span></span>
5. <span data-ttu-id="bd335-114">Щелкните "Версии спецификации".</span><span class="sxs-lookup"><span data-stu-id="bd335-114">Click BOM versions.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="bd335-115">Создание новой спецификации и версии спецификации</span><span class="sxs-lookup"><span data-stu-id="bd335-115">Create new BOM and BOM version</span></span>
1. <span data-ttu-id="bd335-116">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="bd335-116">Click New.</span></span>
2. <span data-ttu-id="bd335-117">Щелкните спецификацию и версию спецификации.</span><span class="sxs-lookup"><span data-stu-id="bd335-117">Click BOM and BOM version.</span></span>
3. <span data-ttu-id="bd335-118">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="bd335-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="bd335-119">Настройка сайта</span><span class="sxs-lookup"><span data-stu-id="bd335-119">Setting a site</span></span>  
    * <span data-ttu-id="bd335-120">В этой процедуре мы не настраиваем определенный сайт для спецификации.</span><span class="sxs-lookup"><span data-stu-id="bd335-120">In this procedure we don't set a specific site for the BOM.</span></span>  
4. <span data-ttu-id="bd335-121">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="bd335-121">Click OK.</span></span>
5. <span data-ttu-id="bd335-122">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="bd335-122">Click New.</span></span>
    * <span data-ttu-id="bd335-123">В этой процедуре мы добавим четыре строки в спецификацию.</span><span class="sxs-lookup"><span data-stu-id="bd335-123">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="bd335-124">Две строки представляют параметры кабеля и две строки представляют параметры шкафа.</span><span class="sxs-lookup"><span data-stu-id="bd335-124">Two lines represent cable options and two lines represent cabinet options.</span></span>  
6. <span data-ttu-id="bd335-125">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="bd335-125">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="bd335-126">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bd335-126">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="bd335-127">Выберите код номенклатуры A0001, кабели 6' HDMI.</span><span class="sxs-lookup"><span data-stu-id="bd335-127">Select item number A0001, HDMI 6' Cables.</span></span>  
8. <span data-ttu-id="bd335-128">В поле "Конфигурационная группа" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bd335-128">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="bd335-129">Выберите конфигурационную группу кабеля, созданную в руководстве 4 в этой последовательности.</span><span class="sxs-lookup"><span data-stu-id="bd335-129">Select the Cable configuration group created in guide 4 in this sequence.</span></span>  
9. <span data-ttu-id="bd335-130">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="bd335-130">Click New.</span></span>
    * <span data-ttu-id="bd335-131">Выберите код номенклатуры A0002, кабели 12' HDMI.</span><span class="sxs-lookup"><span data-stu-id="bd335-131">Select item number A0002, HDMI 12' Cables.</span></span>  
10. <span data-ttu-id="bd335-132">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="bd335-132">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="bd335-133">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bd335-133">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="bd335-134">В поле "Конфигурационная группа" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bd335-134">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="bd335-135">Выберите конфигурационную группу кабеля еще раз.</span><span class="sxs-lookup"><span data-stu-id="bd335-135">Select the Cable configuration group again.</span></span>  
13. <span data-ttu-id="bd335-136">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="bd335-136">Click New.</span></span>
14. <span data-ttu-id="bd335-137">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="bd335-137">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="bd335-138">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bd335-138">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="bd335-139">Выберите код номенклатуры D0002, шкаф.</span><span class="sxs-lookup"><span data-stu-id="bd335-139">Select item number D0002 Cabinet.</span></span>  
16. <span data-ttu-id="bd335-140">В поле "Конфигурационная группа" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bd335-140">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="bd335-141">Выберите конфигурационную группу шкафа для данной строки спецификации.</span><span class="sxs-lookup"><span data-stu-id="bd335-141">Select the Cabinet configuration group for this BOM line.</span></span>  
17. <span data-ttu-id="bd335-142">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="bd335-142">Click New.</span></span>
18. <span data-ttu-id="bd335-143">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="bd335-143">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="bd335-144">В поле "Код номенклатуры" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bd335-144">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="bd335-145">Выберите код номенклатуры M0007 StandardCabinet в качестве последней строки спецификации.</span><span class="sxs-lookup"><span data-stu-id="bd335-145">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
20. <span data-ttu-id="bd335-146">В поле "Конфигурационная группа" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bd335-146">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="bd335-147">Выберите конфигурационную группу шкафа для последней строки спецификации.</span><span class="sxs-lookup"><span data-stu-id="bd335-147">Select the Cabinet configuration group for the laste BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="bd335-148">Утвердить и активировать</span><span class="sxs-lookup"><span data-stu-id="bd335-148">Approve and activate</span></span>
1. <span data-ttu-id="bd335-149">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bd335-149">Close the page.</span></span>
2. <span data-ttu-id="bd335-150">Нажмите кнопку Одобрить.</span><span class="sxs-lookup"><span data-stu-id="bd335-150">Click Approve.</span></span>
3. <span data-ttu-id="bd335-151">В поле "Кем утверждено" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bd335-151">In the Approved by field, enter or select a value.</span></span>
4. <span data-ttu-id="bd335-152">Выберите значение "Да" в поле "Также утвердить спецификацию?" .</span><span class="sxs-lookup"><span data-stu-id="bd335-152">Select Yes in the Do you also want to approve the bill of materials? field.</span></span>
5. <span data-ttu-id="bd335-153">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="bd335-153">Click OK.</span></span>
6. <span data-ttu-id="bd335-154">Нажмите кнопку Активировать.</span><span class="sxs-lookup"><span data-stu-id="bd335-154">Click Activate.</span></span>

