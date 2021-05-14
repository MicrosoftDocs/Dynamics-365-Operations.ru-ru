---
title: Создание спецификации для шаблона продукта на основе аналитик
description: Для данной процедуры необходимо завершить предыдущие 4 руководства в этой последовательности из восьми записей.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13053dd87242963586678b46c64493feb3383c4c
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920713"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="bdc97-103">Создание спецификации для шаблона продукта на основе аналитик</span><span class="sxs-lookup"><span data-stu-id="bdc97-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bdc97-104">Для данной процедуры необходимо завершить предыдущие 4 руководства в этой последовательности из восьми записей.</span><span class="sxs-lookup"><span data-stu-id="bdc97-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="bdc97-105">В первых 4 записях настраиваются данные, необходимые для завершения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="bdc97-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="bdc97-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="bdc97-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="bdc97-107">Обычно эта задача выполняется конструктором продуктов.</span><span class="sxs-lookup"><span data-stu-id="bdc97-107">This task is typically handled by the product designer.</span></span>

## <a name="select-the-product"></a><span data-ttu-id="bdc97-108">Выбор продукта</span><span class="sxs-lookup"><span data-stu-id="bdc97-108">Select the product</span></span>

1. <span data-ttu-id="bdc97-109">Выберите **Управление сведениями о продукте \> Продукты \> Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="bdc97-109">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="bdc97-110">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="bdc97-110">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="bdc97-111">Найдите выпущенный шаблон продукта с помощью технологии конфигурации на основе аналитик, созданной в первом руководстве по задаче в этой последовательности.</span><span class="sxs-lookup"><span data-stu-id="bdc97-111">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
1. <span data-ttu-id="bdc97-112">В области действий выберите **Инженер**.</span><span class="sxs-lookup"><span data-stu-id="bdc97-112">On the Action Pane, select **Engineer**.</span></span>
1. <span data-ttu-id="bdc97-113">Выберите **Версии спецификаций**.</span><span class="sxs-lookup"><span data-stu-id="bdc97-113">Select **BOM versions**.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="bdc97-114">Создание новой спецификации и версии спецификации</span><span class="sxs-lookup"><span data-stu-id="bdc97-114">Create new BOM and BOM version</span></span>

1. <span data-ttu-id="bdc97-115">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="bdc97-115">Select **New**.</span></span>
1. <span data-ttu-id="bdc97-116">Выберите **Спецификация и версия спецификации**.</span><span class="sxs-lookup"><span data-stu-id="bdc97-116">Select **BOM and BOM version**.</span></span>
1. <span data-ttu-id="bdc97-117">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="bdc97-117">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="bdc97-118">Настройка сайта</span><span class="sxs-lookup"><span data-stu-id="bdc97-118">Setting a site</span></span>  
    * <span data-ttu-id="bdc97-119">В этой процедуре мы не настраиваем определенный сайт для спецификации.</span><span class="sxs-lookup"><span data-stu-id="bdc97-119">In this procedure we don't set a specific site for the BOM.</span></span>  
1. <span data-ttu-id="bdc97-120">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="bdc97-120">Select **OK**.</span></span>
1. <span data-ttu-id="bdc97-121">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="bdc97-121">Select **New**.</span></span>
    * <span data-ttu-id="bdc97-122">В этой процедуре мы добавим четыре строки в спецификацию.</span><span class="sxs-lookup"><span data-stu-id="bdc97-122">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="bdc97-123">Две строки представляют параметры кабеля и две строки представляют параметры шкафа.</span><span class="sxs-lookup"><span data-stu-id="bdc97-123">Two lines represent cable options and two lines represent cabinet options.</span></span>  
1. <span data-ttu-id="bdc97-124">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="bdc97-124">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="bdc97-125">В поле **Код номенклатуры** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bdc97-125">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="bdc97-126">Выберите код номенклатуры A0001, кабели 6' HDMI.</span><span class="sxs-lookup"><span data-stu-id="bdc97-126">Select item number A0001, HDMI 6' Cables.</span></span>  
1. <span data-ttu-id="bdc97-127">В поле **Конфигурационная группа** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bdc97-127">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="bdc97-128">Выберите конфигурационную группу кабеля, созданную в руководстве 4 в этой последовательности.</span><span class="sxs-lookup"><span data-stu-id="bdc97-128">Select the cable configuration group created in guide 4 in this sequence.</span></span>  
1. <span data-ttu-id="bdc97-129">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="bdc97-129">Select **New**.</span></span>
    * <span data-ttu-id="bdc97-130">Выберите код номенклатуры A0002, кабели 12' HDMI.</span><span class="sxs-lookup"><span data-stu-id="bdc97-130">Select item number A0002, HDMI 12' Cables.</span></span>  
1. <span data-ttu-id="bdc97-131">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="bdc97-131">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="bdc97-132">В поле **Код номенклатуры** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bdc97-132">In the **Item number** field, enter or select a value.</span></span>
1. <span data-ttu-id="bdc97-133">В поле **Конфигурационная группа** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bdc97-133">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="bdc97-134">Выберите конфигурационную группу кабеля еще раз.</span><span class="sxs-lookup"><span data-stu-id="bdc97-134">Select the cable configuration group again.</span></span>  
1. <span data-ttu-id="bdc97-135">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="bdc97-135">Select **New**.</span></span>
1. <span data-ttu-id="bdc97-136">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="bdc97-136">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="bdc97-137">В поле **Код номенклатуры** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bdc97-137">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="bdc97-138">Выберите код номенклатуры D0002, шкаф.</span><span class="sxs-lookup"><span data-stu-id="bdc97-138">Select item number D0002 Cabinet.</span></span>  
1. <span data-ttu-id="bdc97-139">В поле **Конфигурационная группа** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bdc97-139">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="bdc97-140">Выберите конфигурационную группу шкафа для данной строки спецификации.</span><span class="sxs-lookup"><span data-stu-id="bdc97-140">Select the cabinet configuration group for this BOM line.</span></span>  
1. <span data-ttu-id="bdc97-141">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="bdc97-141">Select **New**.</span></span>
1. <span data-ttu-id="bdc97-142">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="bdc97-142">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="bdc97-143">В поле **Код номенклатуры** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bdc97-143">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="bdc97-144">Выберите код номенклатуры M0007 StandardCabinet в качестве последней строки спецификации.</span><span class="sxs-lookup"><span data-stu-id="bdc97-144">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
1. <span data-ttu-id="bdc97-145">В поле **Конфигурационная группа** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bdc97-145">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="bdc97-146">Выберите конфигурационную группу шкафа для последней строки спецификации.</span><span class="sxs-lookup"><span data-stu-id="bdc97-146">Select the Cabinet configuration group for the last BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="bdc97-147">Утвердить и активировать</span><span class="sxs-lookup"><span data-stu-id="bdc97-147">Approve and activate</span></span>

1. <span data-ttu-id="bdc97-148">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bdc97-148">Close the page.</span></span>
1. <span data-ttu-id="bdc97-149">Выберите **Утвердить**.</span><span class="sxs-lookup"><span data-stu-id="bdc97-149">Select **Approve**.</span></span>
1. <span data-ttu-id="bdc97-150">В поле **Кем утверждено** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bdc97-150">In the **Approved by** field, enter or select a value.</span></span>
1. <span data-ttu-id="bdc97-151">Выберите значение *Да* в поле **Также утвердить спецификацию?**.</span><span class="sxs-lookup"><span data-stu-id="bdc97-151">Select *Yes* in the **Do you also want to approve the bill of materials?** field.</span></span>
1. <span data-ttu-id="bdc97-152">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="bdc97-152">Select **OK**.</span></span>
1. <span data-ttu-id="bdc97-153">Выберите **Активировать**.</span><span class="sxs-lookup"><span data-stu-id="bdc97-153">Select **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]