--- 
title: "Создание заранее определенных вариантов продукта"
description: "В этой процедуре показано, как создать варианты продукта для шаблона продукта с использованием комбинаций аналитик продукта."
author: BibiSp
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: fa23f1449e750b4ed1c0f631a98c42b18b7dbb40
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="create-predefined-product-variants"></a><span data-ttu-id="eeaa4-103">Создание заранее определенных вариантов продукта</span><span class="sxs-lookup"><span data-stu-id="eeaa4-103">Create predefined product variants</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eeaa4-104">В этой процедуре показано, как создать варианты продукта для шаблона продукта с использованием комбинаций аналитик продукта.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-104">This procedure walks through creating product variants for a product master using the combinations of product dimensions.</span></span> <span data-ttu-id="eeaa4-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-105">The demo company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-master"></a><span data-ttu-id="eeaa4-106">Создание шаблона продукта</span><span class="sxs-lookup"><span data-stu-id="eeaa4-106">Create a product master</span></span>
1. <span data-ttu-id="eeaa4-107">Перейдите в раздел "Управление сведениями о продукте" > "Продукты" > "Шаблоны продукта".</span><span class="sxs-lookup"><span data-stu-id="eeaa4-107">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="eeaa4-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="eeaa4-108">Click New.</span></span>
3. <span data-ttu-id="eeaa4-109">В поле "Номер продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="eeaa4-110">Вводить номер продукта вручную обязательно, только если для поля "Номер продукта" не настроена номерная серия.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-110">Entering a product number manually is only required if no number sequence has been set for the product number field.</span></span> <span data-ttu-id="eeaa4-111">Другими словами, пропустите этот шаг, если для поля настроена номерная серия.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-111">In other words, skip the step if number sequence has been set for the field.</span></span>  
4. <span data-ttu-id="eeaa4-112">В поле "Имя продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-112">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="eeaa4-113">В поле "Группа аналитик продуктов" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-113">In the Product dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="eeaa4-114">Выберите группу аналитик продуктов SizeCol (размер и цвет).</span><span class="sxs-lookup"><span data-stu-id="eeaa4-114">Select the product dimension group SizeCol (Size and Color).</span></span>  
6. <span data-ttu-id="eeaa4-115">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="eeaa4-115">Click OK.</span></span>

## <a name="add-product-dimensions"></a><span data-ttu-id="eeaa4-116">Добавление аналитик продукта</span><span class="sxs-lookup"><span data-stu-id="eeaa4-116">Add product dimensions</span></span>
1. <span data-ttu-id="eeaa4-117">Щелкните "Аналитики продуктов".</span><span class="sxs-lookup"><span data-stu-id="eeaa4-117">Click Product dimensions.</span></span>
    * <span data-ttu-id="eeaa4-118">В этом примере показано, как ввести аналитики продукта вручную.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="eeaa4-119">Можно также выбрать размер, цвет или группу стилей, включающую значения аналитик продукта, которые необходимо использовать.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-119">You can also choose to select a size, color or style group that includes the product dimension values you want to use.</span></span>  
2. <span data-ttu-id="eeaa4-120">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="eeaa4-120">Click New.</span></span>
3. <span data-ttu-id="eeaa4-121">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="eeaa4-122">В поле "Размер" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-122">In the Size field, enter or select a value.</span></span>
5. <span data-ttu-id="eeaa4-123">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-123">In the Name field, type a value.</span></span>
6. <span data-ttu-id="eeaa4-124">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-124">Click New.</span></span>
7. <span data-ttu-id="eeaa4-125">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-125">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="eeaa4-126">В поле "Размер" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-126">In the Size field, enter or select a value.</span></span>
9. <span data-ttu-id="eeaa4-127">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-127">In the Name field, type a value.</span></span>
10. <span data-ttu-id="eeaa4-128">Перейдите на вкладку "Цвета".</span><span class="sxs-lookup"><span data-stu-id="eeaa4-128">Click the Colors tab.</span></span>
11. <span data-ttu-id="eeaa4-129">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="eeaa4-129">Click New.</span></span>
12. <span data-ttu-id="eeaa4-130">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-130">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="eeaa4-131">В поле "Цвет" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-131">In the Color field, enter or select a value.</span></span>
14. <span data-ttu-id="eeaa4-132">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-132">In the Name field, type a value.</span></span>
15. <span data-ttu-id="eeaa4-133">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-133">Click New.</span></span>
16. <span data-ttu-id="eeaa4-134">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-134">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="eeaa4-135">В поле "Цвет" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-135">In the Color field, enter or select a value.</span></span>
18. <span data-ttu-id="eeaa4-136">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-136">In the Name field, type a value.</span></span>
19. <span data-ttu-id="eeaa4-137">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="eeaa4-137">Click Save.</span></span>
20. <span data-ttu-id="eeaa4-138">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-138">Close the page.</span></span>

## <a name="generate-product-variants"></a><span data-ttu-id="eeaa4-139">Создание вариантов продукта</span><span class="sxs-lookup"><span data-stu-id="eeaa4-139">Generate product variants</span></span>
1. <span data-ttu-id="eeaa4-140">Щелкните "Варианты продуктов".</span><span class="sxs-lookup"><span data-stu-id="eeaa4-140">Click Product variants.</span></span>
2. <span data-ttu-id="eeaa4-141">Щелкните "Предложения вариантов".</span><span class="sxs-lookup"><span data-stu-id="eeaa4-141">Click Variant suggestions.</span></span>
3. <span data-ttu-id="eeaa4-142">Щелкните "Выбрать все".</span><span class="sxs-lookup"><span data-stu-id="eeaa4-142">Click Select all.</span></span>
    * <span data-ttu-id="eeaa4-143">В этом примере выбраны все возможные варианты.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-143">In this example, all possible variants are selected.</span></span> <span data-ttu-id="eeaa4-144">Если для создания вариантов будет использоваться только подмножество возможных комбинаций аналитик продукта, можно выбрать отдельные записи.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-144">If only a subset of the possible product dimension combinations will be used to create variants, you can select the individual entries.</span></span>  
4. <span data-ttu-id="eeaa4-145">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="eeaa4-145">Click Create.</span></span>
    * <span data-ttu-id="eeaa4-146">Можно создавать описания для всех имеющихся вариантов на основе комбинаций значений аналитик продукта.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-146">You can generate descriptions for all your variants based on the combination of product dimension values.</span></span> <span data-ttu-id="eeaa4-147">Описания являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="eeaa4-147">The descriptions are optional.</span></span>  
5. <span data-ttu-id="eeaa4-148">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="eeaa4-148">Click Save.</span></span>


