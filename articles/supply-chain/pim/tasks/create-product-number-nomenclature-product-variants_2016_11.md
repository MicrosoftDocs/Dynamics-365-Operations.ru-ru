---
title: Создание номенклатуры номера продукта для настроенных вариантов продукта
description: На этой процедуры показано, как настроить номенклатуру номера продукта для сконфигурированных вариантов продукта, и как ее можно добавить в конфигурируемый шаблон продукта.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ea30dc107213b1a2c6b2a109188066a6ea82159
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921019"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="5069b-103">Создание номенклатуры номера продукта для настроенных вариантов продукта</span><span class="sxs-lookup"><span data-stu-id="5069b-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5069b-104">На этой процедуры показано, как настроить номенклатуру номера продукта для сконфигурированных вариантов продукта, и как ее можно добавить в конфигурируемый шаблон продукта.</span><span class="sxs-lookup"><span data-stu-id="5069b-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="5069b-105">Эта процедура также демонстрирует, как можно создать конфигурацию номенклатуры для компонента модели конфигурации продукта.</span><span class="sxs-lookup"><span data-stu-id="5069b-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="5069b-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="5069b-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="5069b-107">Новая номенклатура номера продукта назначена шаблону продукта D0004.</span><span class="sxs-lookup"><span data-stu-id="5069b-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="5069b-108">Эта задача обычно выполняется конструктором продуктов.</span><span class="sxs-lookup"><span data-stu-id="5069b-108">This task would typically be done by a product designer.</span></span>

## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="5069b-109">Создание номенклатуры номеров продуктов</span><span class="sxs-lookup"><span data-stu-id="5069b-109">Create a product number nomenclature</span></span>

1. <span data-ttu-id="5069b-110">Перейдите в раздел **Управление сведениями о продукте \> Настройка \> Номенклатура продукта**.</span><span class="sxs-lookup"><span data-stu-id="5069b-110">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="5069b-111">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="5069b-111">Select **New**.</span></span>
1. <span data-ttu-id="5069b-112">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="5069b-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="5069b-113">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="5069b-113">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="5069b-114">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="5069b-114">Select **Add**.</span></span>
1. <span data-ttu-id="5069b-115">Выберите **Номер шаблона продукта**.</span><span class="sxs-lookup"><span data-stu-id="5069b-115">Select **Product master number**.</span></span>
1. <span data-ttu-id="5069b-116">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="5069b-116">Select **Add**.</span></span>
1. <span data-ttu-id="5069b-117">Выберите **Текстовая константа**.</span><span class="sxs-lookup"><span data-stu-id="5069b-117">Select **Text constant**.</span></span>
1. <span data-ttu-id="5069b-118">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="5069b-118">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5069b-119">В поле **Текст** введите значение.</span><span class="sxs-lookup"><span data-stu-id="5069b-119">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="5069b-120">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="5069b-120">Select **Add**.</span></span>
1. <span data-ttu-id="5069b-121">Выберите **Конфигурация**.</span><span class="sxs-lookup"><span data-stu-id="5069b-121">Select **Configuration**.</span></span>
1. <span data-ttu-id="5069b-122">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="5069b-122">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="5069b-123">Назначение номенклатуры номеров продуктов шаблону продукта</span><span class="sxs-lookup"><span data-stu-id="5069b-123">Assign the product number nomenclature to a product master</span></span>

1. <span data-ttu-id="5069b-124">Перейдите в раздел **Управление сведениями о продукте \> Продукты \> Шаблоны продукта**.</span><span class="sxs-lookup"><span data-stu-id="5069b-124">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="5069b-125">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="5069b-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="5069b-126">Например, отфильтруйте поле **Номер продукта** по значению "D".</span><span class="sxs-lookup"><span data-stu-id="5069b-126">For example, filter on the **Product number** field with a value of 'D'.</span></span>
1. <span data-ttu-id="5069b-127">В списке выберите ссылку в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="5069b-127">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="5069b-128">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="5069b-128">Select **Edit**.</span></span>
1. <span data-ttu-id="5069b-129">Выберите *Да* в поле **Использовать номенклатуру**.</span><span class="sxs-lookup"><span data-stu-id="5069b-129">Select *Yes* in the **Use nomenclature** field.</span></span>
1. <span data-ttu-id="5069b-130">В поле **Номенклатура номеров вариантов продуктов** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="5069b-130">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
1. <span data-ttu-id="5069b-131">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="5069b-131">Close the page.</span></span>
1. <span data-ttu-id="5069b-132">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="5069b-132">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="5069b-133">Создание номенклатуры для компонента модели конфигурации продукта</span><span class="sxs-lookup"><span data-stu-id="5069b-133">Create nomenclature for a product configuration model component</span></span>

1. <span data-ttu-id="5069b-134">Перейдите в раздел **Управление сведениями о продукте \> Продукты \> Модели конфигурации продукта**.</span><span class="sxs-lookup"><span data-stu-id="5069b-134">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="5069b-135">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="5069b-135">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="5069b-136">В списке выберите ссылку в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="5069b-136">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="5069b-137">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="5069b-137">Select **Edit**.</span></span>
1. <span data-ttu-id="5069b-138">Выберите *Да* в поле **Использовать номенклатуру конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="5069b-138">Select *Yes* in the **Use configuration nomenclature** field.</span></span>
1. <span data-ttu-id="5069b-139">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="5069b-139">Select **Add**.</span></span>
1. <span data-ttu-id="5069b-140">Выберите **Значение атрибута**.</span><span class="sxs-lookup"><span data-stu-id="5069b-140">Select **Attribute value**.</span></span>
1. <span data-ttu-id="5069b-141">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="5069b-141">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5069b-142">В поле **Атрибут** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="5069b-142">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="5069b-143">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="5069b-143">Select **Add**.</span></span>
1. <span data-ttu-id="5069b-144">Выберите **Текстовая константа**.</span><span class="sxs-lookup"><span data-stu-id="5069b-144">Select **Text constant**.</span></span>
1. <span data-ttu-id="5069b-145">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="5069b-145">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5069b-146">В поле **Текст** введите значение.</span><span class="sxs-lookup"><span data-stu-id="5069b-146">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="5069b-147">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="5069b-147">Select **Add**.</span></span>
1. <span data-ttu-id="5069b-148">Выберите **Значение атрибута**.</span><span class="sxs-lookup"><span data-stu-id="5069b-148">Select **Attribute value**.</span></span>
1. <span data-ttu-id="5069b-149">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="5069b-149">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5069b-150">В поле **Атрибут** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="5069b-150">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="5069b-151">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="5069b-151">Select **Add**.</span></span>
1. <span data-ttu-id="5069b-152">Выберите **Текстовая константа**.</span><span class="sxs-lookup"><span data-stu-id="5069b-152">Select **Text constant**.</span></span>
1. <span data-ttu-id="5069b-153">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="5069b-153">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5069b-154">В поле **Текст** введите значение.</span><span class="sxs-lookup"><span data-stu-id="5069b-154">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="5069b-155">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="5069b-155">Select **Add**.</span></span>
1. <span data-ttu-id="5069b-156">Выберите **Значение атрибута**.</span><span class="sxs-lookup"><span data-stu-id="5069b-156">Select **Attribute value**.</span></span>
1. <span data-ttu-id="5069b-157">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="5069b-157">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5069b-158">В поле **Атрибут** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="5069b-158">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="5069b-159">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="5069b-159">Select **Add**.</span></span>
1. <span data-ttu-id="5069b-160">Выберите **Текстовая константа**.</span><span class="sxs-lookup"><span data-stu-id="5069b-160">Select **Text constant**.</span></span>
1. <span data-ttu-id="5069b-161">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="5069b-161">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5069b-162">В поле **Текст** введите значение.</span><span class="sxs-lookup"><span data-stu-id="5069b-162">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="5069b-163">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="5069b-163">Select **Add**.</span></span>
1. <span data-ttu-id="5069b-164">Выберите **Значение атрибута**.</span><span class="sxs-lookup"><span data-stu-id="5069b-164">Select **Attribute value**.</span></span>
1. <span data-ttu-id="5069b-165">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="5069b-165">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5069b-166">В поле **Атрибут** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="5069b-166">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="5069b-167">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="5069b-167">Select **Add**.</span></span>
1. <span data-ttu-id="5069b-168">Выберите **Текстовая константа**.</span><span class="sxs-lookup"><span data-stu-id="5069b-168">Select **Text constant**.</span></span>
1. <span data-ttu-id="5069b-169">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="5069b-169">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5069b-170">В поле **Текст** введите значение.</span><span class="sxs-lookup"><span data-stu-id="5069b-170">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="5069b-171">Выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="5069b-171">Select **Add**.</span></span>
1. <span data-ttu-id="5069b-172">Выберите **Значение номерной серии**.</span><span class="sxs-lookup"><span data-stu-id="5069b-172">Select **Number sequence value**.</span></span>
1. <span data-ttu-id="5069b-173">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="5069b-173">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="5069b-174">В поле **Номерная серия** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="5069b-174">In the **Number sequence** field, enter or select a value.</span></span>
1. <span data-ttu-id="5069b-175">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="5069b-175">Close the page.</span></span>
1. <span data-ttu-id="5069b-176">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="5069b-176">Close the page.</span></span>
1. <span data-ttu-id="5069b-177">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="5069b-177">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]