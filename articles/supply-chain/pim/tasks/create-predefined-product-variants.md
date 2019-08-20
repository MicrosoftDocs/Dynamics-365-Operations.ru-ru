---
title: Создание заранее определенных вариантов продукта
description: В этой процедуре показано, как создать варианты продукта для шаблона продукта с использованием комбинаций аналитик продукта.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: baf1e41d0071a4c78d2a0f43548e44ae9d426580
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844785"
---
# <a name="create-predefined-product-variants"></a><span data-ttu-id="9f1f8-103">Создание заранее определенных вариантов продукта</span><span class="sxs-lookup"><span data-stu-id="9f1f8-103">Create predefined product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9f1f8-104">В этой процедуре показано, как создать варианты продукта для шаблона продукта с использованием комбинаций аналитик продукта.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-104">This procedure walks through creating product variants for a product master using the combinations of product dimensions.</span></span> <span data-ttu-id="9f1f8-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-105">The demo company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-master"></a><span data-ttu-id="9f1f8-106">Создание шаблона продукта</span><span class="sxs-lookup"><span data-stu-id="9f1f8-106">Create a product master</span></span>
1. <span data-ttu-id="9f1f8-107">Перейдите в раздел "Управление сведениями о продукте" > "Продукты" > "Шаблоны продукта".</span><span class="sxs-lookup"><span data-stu-id="9f1f8-107">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="9f1f8-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="9f1f8-108">Click New.</span></span>
3. <span data-ttu-id="9f1f8-109">В поле "Номер продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="9f1f8-110">Вводить номер продукта вручную обязательно, только если для поля "Номер продукта" не настроена номерная серия.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-110">Entering a product number manually is only required if no number sequence has been set for the product number field.</span></span> <span data-ttu-id="9f1f8-111">Другими словами, пропустите этот шаг, если для поля настроена номерная серия.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-111">In other words, skip the step if number sequence has been set for the field.</span></span>  
4. <span data-ttu-id="9f1f8-112">В поле "Имя продукта" введите значение.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-112">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="9f1f8-113">В поле "Группа аналитик продуктов" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-113">In the Product dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="9f1f8-114">Выберите группу аналитик продуктов SizeCol (размер и цвет).</span><span class="sxs-lookup"><span data-stu-id="9f1f8-114">Select the product dimension group SizeCol (Size and Color).</span></span>  
6. <span data-ttu-id="9f1f8-115">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="9f1f8-115">Click OK.</span></span>

## <a name="add-product-dimensions"></a><span data-ttu-id="9f1f8-116">Добавление аналитик продукта</span><span class="sxs-lookup"><span data-stu-id="9f1f8-116">Add product dimensions</span></span>
1. <span data-ttu-id="9f1f8-117">Щелкните "Аналитики продуктов".</span><span class="sxs-lookup"><span data-stu-id="9f1f8-117">Click Product dimensions.</span></span>
    * <span data-ttu-id="9f1f8-118">В этом примере показано, как ввести аналитики продукта вручную.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="9f1f8-119">Можно также выбрать размер, цвет или группу стилей, включающую значения аналитик продукта, которые необходимо использовать.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-119">You can also choose to select a size, color or style group that includes the product dimension values you want to use.</span></span>  
2. <span data-ttu-id="9f1f8-120">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="9f1f8-120">Click New.</span></span>
3. <span data-ttu-id="9f1f8-121">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="9f1f8-122">В поле "Размер" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-122">In the Size field, enter or select a value.</span></span>
5. <span data-ttu-id="9f1f8-123">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-123">In the Name field, type a value.</span></span>
6. <span data-ttu-id="9f1f8-124">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-124">Click New.</span></span>
7. <span data-ttu-id="9f1f8-125">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-125">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="9f1f8-126">В поле "Размер" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-126">In the Size field, enter or select a value.</span></span>
9. <span data-ttu-id="9f1f8-127">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-127">In the Name field, type a value.</span></span>
10. <span data-ttu-id="9f1f8-128">Перейдите на вкладку "Цвета".</span><span class="sxs-lookup"><span data-stu-id="9f1f8-128">Click the Colors tab.</span></span>
11. <span data-ttu-id="9f1f8-129">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="9f1f8-129">Click New.</span></span>
12. <span data-ttu-id="9f1f8-130">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-130">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="9f1f8-131">В поле "Цвет" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-131">In the Color field, enter or select a value.</span></span>
14. <span data-ttu-id="9f1f8-132">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-132">In the Name field, type a value.</span></span>
15. <span data-ttu-id="9f1f8-133">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-133">Click New.</span></span>
16. <span data-ttu-id="9f1f8-134">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-134">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="9f1f8-135">В поле "Цвет" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-135">In the Color field, enter or select a value.</span></span>
18. <span data-ttu-id="9f1f8-136">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-136">In the Name field, type a value.</span></span>
19. <span data-ttu-id="9f1f8-137">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="9f1f8-137">Click Save.</span></span>
20. <span data-ttu-id="9f1f8-138">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-138">Close the page.</span></span>

## <a name="generate-product-variants"></a><span data-ttu-id="9f1f8-139">Создание вариантов продукта</span><span class="sxs-lookup"><span data-stu-id="9f1f8-139">Generate product variants</span></span>
1. <span data-ttu-id="9f1f8-140">Щелкните "Варианты продуктов".</span><span class="sxs-lookup"><span data-stu-id="9f1f8-140">Click Product variants.</span></span>
2. <span data-ttu-id="9f1f8-141">Щелкните "Предложения вариантов".</span><span class="sxs-lookup"><span data-stu-id="9f1f8-141">Click Variant suggestions.</span></span>
3. <span data-ttu-id="9f1f8-142">Щелкните "Выбрать все".</span><span class="sxs-lookup"><span data-stu-id="9f1f8-142">Click Select all.</span></span>
    * <span data-ttu-id="9f1f8-143">В этом примере выбраны все возможные варианты.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-143">In this example, all possible variants are selected.</span></span> <span data-ttu-id="9f1f8-144">Если для создания вариантов будет использоваться только подмножество возможных комбинаций аналитик продукта, можно выбрать отдельные записи.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-144">If only a subset of the possible product dimension combinations will be used to create variants, you can select the individual entries.</span></span>  
4. <span data-ttu-id="9f1f8-145">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="9f1f8-145">Click Create.</span></span>
    * <span data-ttu-id="9f1f8-146">Можно создавать описания для всех имеющихся вариантов на основе комбинаций значений аналитик продукта.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-146">You can generate descriptions for all your variants based on the combination of product dimension values.</span></span> <span data-ttu-id="9f1f8-147">Описания являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="9f1f8-147">The descriptions are optional.</span></span>  
5. <span data-ttu-id="9f1f8-148">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="9f1f8-148">Click Save.</span></span>

