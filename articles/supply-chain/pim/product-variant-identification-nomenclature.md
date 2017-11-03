---
title: "Номенклатура номеров и названий вариантов продуктов"
description: "В этом разделе описывается, как можно настроить номенклатуру номеров продукции для замены фиксированного формата [Номер шаблона продукта - Конфигурация – Размер - Цвет - Стиль]. Новая номенклатура имеет целевой формат, включающий номер шаблона продукта, активные аналитики продукта и разделители текста по вашему выбору. Также можно создать номенклатуру для названий продуктов. Наконец, можно создать номенклатуру для идентификации конфигураций, созданных с помощью конфигуратора продукта на основе ограничений. Эти номенклатуры могут содержать атрибуты по вашему выбору."
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: db01d26376ec3ca6997b1ad2cb62e7b3ecc4b330
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="afb63-107">Номенклатура номеров и названий вариантов продуктов</span><span class="sxs-lookup"><span data-stu-id="afb63-107">Nomenclature of product variant numbers and names</span></span>

<span data-ttu-id="afb63-108">В этом разделе описывается, как можно настроить номенклатуру номеров продукции для замены фиксированного формата [Номер шаблона продукта - Конфигурация – Размер - Цвет - Стиль].</span><span class="sxs-lookup"><span data-stu-id="afb63-108">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="afb63-109">Новая номенклатура имеет целевой формат, включающий номер шаблона продукта, активные аналитики продукта и разделители текста по вашему выбору.</span><span class="sxs-lookup"><span data-stu-id="afb63-109">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="afb63-110">Также можно создать номенклатуру для названий продуктов.</span><span class="sxs-lookup"><span data-stu-id="afb63-110">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="afb63-111">Наконец, можно создать номенклатуру для идентификации конфигураций, созданных с помощью конфигуратора продукта на основе ограничений.</span><span class="sxs-lookup"><span data-stu-id="afb63-111">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="afb63-112">Эти номенклатуры могут содержать атрибуты по вашему выбору.</span><span class="sxs-lookup"><span data-stu-id="afb63-112">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="afb63-113">Новые номенклатуры для номеров вариантов продуктов и имен вариантов продуктов позволяют включать сегменты в идентификаторы для вариантов продуктов.</span><span class="sxs-lookup"><span data-stu-id="afb63-113">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="afb63-114">Эти сегменты могут включать номер и названием шаблона продукта, коды и названия аналитик продукта, номерные серии, текстовые константы и атрибуты.</span><span class="sxs-lookup"><span data-stu-id="afb63-114">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="afb63-115">Эта функция позволяет быстро найти определенный вариант продукта при создании заказа на продажу или заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="afb63-115">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="afb63-116">Номенклатуры для номеров вариантов продуктов и названий вариантов продуктов создаются с помощью страницы **Номенклатура продуктов**.</span><span class="sxs-lookup"><span data-stu-id="afb63-116">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="afb63-117">Чтобы открыть эту страницу, щелкните **Управление сведениями о продукте** &gt; **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="afb63-117">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="afb63-118">Номенклатура предопределенных вариантов продуктов</span><span class="sxs-lookup"><span data-stu-id="afb63-118">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="afb63-119">Варианты продукта создаются для шаблонов продуктов в соответствии с одной из трех технологий конфигурации:</span><span class="sxs-lookup"><span data-stu-id="afb63-119">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="afb63-120">Предопределенные варианты</span><span class="sxs-lookup"><span data-stu-id="afb63-120">Predefined variants</span></span>
-   <span data-ttu-id="afb63-121">На основе ограничений</span><span class="sxs-lookup"><span data-stu-id="afb63-121">Constraint-based</span></span>
-   <span data-ttu-id="afb63-122">На основе аналитик</span><span class="sxs-lookup"><span data-stu-id="afb63-122">Dimension-based</span></span>

<span data-ttu-id="afb63-123">Каждый вариант продукта имеет номер и название, и номенклатуры идентификации варианта продукта позволяют выбрать сегменты, которые будут включены в каждый номер или название варианта продукта.</span><span class="sxs-lookup"><span data-stu-id="afb63-123">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="afb63-124">Можно выбрать следующие сегменты на странице **Номенклатура продуктов**:</span><span class="sxs-lookup"><span data-stu-id="afb63-124">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="afb63-125">Номер шаблона продукта</span><span class="sxs-lookup"><span data-stu-id="afb63-125">Product master number</span></span>
-   <span data-ttu-id="afb63-126">Имя шаблона продукта</span><span class="sxs-lookup"><span data-stu-id="afb63-126">Product master name</span></span>
-   <span data-ttu-id="afb63-127">Значение номерной серии</span><span class="sxs-lookup"><span data-stu-id="afb63-127">Number sequence value</span></span>
-   <span data-ttu-id="afb63-128">Текстовая константа</span><span class="sxs-lookup"><span data-stu-id="afb63-128">Text constant</span></span>
-   <span data-ttu-id="afb63-129">Аналитики продуктов</span><span class="sxs-lookup"><span data-stu-id="afb63-129">Product dimensions</span></span>
    -   <span data-ttu-id="afb63-130">Код или наименование конфигурации</span><span class="sxs-lookup"><span data-stu-id="afb63-130">Configuration ID or name</span></span>
    -   <span data-ttu-id="afb63-131">Код или название цвета</span><span class="sxs-lookup"><span data-stu-id="afb63-131">Color ID or name</span></span>
    -   <span data-ttu-id="afb63-132">Код или название размера</span><span class="sxs-lookup"><span data-stu-id="afb63-132">Size ID or name</span></span>
    -   <span data-ttu-id="afb63-133">Код или название стиля</span><span class="sxs-lookup"><span data-stu-id="afb63-133">Style ID or name</span></span>

<span data-ttu-id="afb63-134">После определения номенклатуры номеров идентификации вариантов продуктов ее можно связать с группой аналитик продуктов.</span><span class="sxs-lookup"><span data-stu-id="afb63-134">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="afb63-135">Всем шаблонам продуктов, ссылающимся на эту группу аналитик продуктов, будут назначены номера вариантов продуктов в соответствии с номенклатурой.</span><span class="sxs-lookup"><span data-stu-id="afb63-135">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="afb63-136">Однако номенклатуры название вариантов продукта нельзя связать с группами аналитик продуктов.</span><span class="sxs-lookup"><span data-stu-id="afb63-136">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="afb63-137">Можно также назначить номенклатуру идентификации варианта продукта непосредственно шаблону продукта.</span><span class="sxs-lookup"><span data-stu-id="afb63-137">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="afb63-138">В этом случае вариантам продукта, которые относятся к шаблону продукта, будут назначаться номера и названия вариантов продуктов в соответствии с номенклатурами.</span><span class="sxs-lookup"><span data-stu-id="afb63-138">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="afb63-139">Пример</span><span class="sxs-lookup"><span data-stu-id="afb63-139">Example</span></span>

<span data-ttu-id="afb63-140">Футболка (TS1234) выпускается в трех размерах (S, M, L), четырех цветах (красный, зеленый, голубой, желтый) и двух стилях (Поло, V).</span><span class="sxs-lookup"><span data-stu-id="afb63-140">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="afb63-141">Таким образом, возможны 24 варианта продукта (= 3 × 4 × 2).</span><span class="sxs-lookup"><span data-stu-id="afb63-141">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="afb63-142">Вы создаете номенклатуру номеров вариантов продукта, имеющую следующие сегменты:</span><span class="sxs-lookup"><span data-stu-id="afb63-142">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="afb63-143">Номер шаблона продукта</span><span class="sxs-lookup"><span data-stu-id="afb63-143">Product master number</span></span>
2.  <span data-ttu-id="afb63-144">Текстовая константа: "-"</span><span class="sxs-lookup"><span data-stu-id="afb63-144">Text constant: "-"</span></span>
3.  <span data-ttu-id="afb63-145">Цвет</span><span class="sxs-lookup"><span data-stu-id="afb63-145">Color</span></span>
4.  <span data-ttu-id="afb63-146">Текстовая константа: "-"</span><span class="sxs-lookup"><span data-stu-id="afb63-146">Text constant: "-"</span></span>
5.  <span data-ttu-id="afb63-147">Размер</span><span class="sxs-lookup"><span data-stu-id="afb63-147">Size</span></span>
6.  <span data-ttu-id="afb63-148">Текстовая константа: "-"</span><span class="sxs-lookup"><span data-stu-id="afb63-148">Text constant: "-"</span></span>
7.  <span data-ttu-id="afb63-149">Стиль</span><span class="sxs-lookup"><span data-stu-id="afb63-149">Style</span></span>

<span data-ttu-id="afb63-150">В этом случае номер варианта продукта для красной футболки поло маленького размера будет: TS1234-Red-Small-Polo.</span><span class="sxs-lookup"><span data-stu-id="afb63-150">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraintbased-configurations"></a><span data-ttu-id="afb63-151">Номенклатура конфигураций на основе ограничений</span><span class="sxs-lookup"><span data-stu-id="afb63-151">Nomenclature of constraintbased configurations</span></span>
<span data-ttu-id="afb63-152">Для конфигураций, основанных на ограничениях, можно создать специальную номенклатуру для аналитики продукта конфигурации.</span><span class="sxs-lookup"><span data-stu-id="afb63-152">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="afb63-153">Можно выбрать следующие сегменты на странице **Номенклатура продуктов**:</span><span class="sxs-lookup"><span data-stu-id="afb63-153">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="afb63-154">Значение номерной серии</span><span class="sxs-lookup"><span data-stu-id="afb63-154">Number sequence value</span></span>
-   <span data-ttu-id="afb63-155">Текстовая константа</span><span class="sxs-lookup"><span data-stu-id="afb63-155">Text constant</span></span>
-   <span data-ttu-id="afb63-156">Значение атрибута</span><span class="sxs-lookup"><span data-stu-id="afb63-156">Attribute value</span></span>

<span data-ttu-id="afb63-157">Каждый из компонентов в модели конфигурации продукта может иметь собственную номенклатуру конфигурации.</span><span class="sxs-lookup"><span data-stu-id="afb63-157">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="afb63-158">Только атрибуты, принадлежащие компоненту, могут быть использованы.</span><span class="sxs-lookup"><span data-stu-id="afb63-158">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="afb63-159">Атрибуты из субкомпонентов или из требований пользователя использовать невозможно.</span><span class="sxs-lookup"><span data-stu-id="afb63-159">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="afb63-160">Пример</span><span class="sxs-lookup"><span data-stu-id="afb63-160">Example</span></span>

<span data-ttu-id="afb63-161">Модель конфигурации продукта имеет корневой компонент с двумя атрибутами:</span><span class="sxs-lookup"><span data-stu-id="afb63-161">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="afb63-162">Материал (пластик, древесина, сталь)</span><span class="sxs-lookup"><span data-stu-id="afb63-162">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="afb63-163">Длина (10...100)</span><span class="sxs-lookup"><span data-stu-id="afb63-163">Length (10...100)</span></span>

<span data-ttu-id="afb63-164">Вы создаете номенклатуру конфигурации, имеющую следующие сегменты:</span><span class="sxs-lookup"><span data-stu-id="afb63-164">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="afb63-165">Значение атрибута: Материал</span><span class="sxs-lookup"><span data-stu-id="afb63-165">Attribute value: Material</span></span>
2.  <span data-ttu-id="afb63-166">Текстовая константа: "AAA"</span><span class="sxs-lookup"><span data-stu-id="afb63-166">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="afb63-167">Значение атрибута: Длина</span><span class="sxs-lookup"><span data-stu-id="afb63-167">Attribute value: Length</span></span>

<span data-ttu-id="afb63-168">В этом случае код конфигурации для деревянного материала с длиной 78 будет WoodAAA78.</span><span class="sxs-lookup"><span data-stu-id="afb63-168">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimensionbased-configurations"></a><span data-ttu-id="afb63-169">Номенклатура конфигураций на основе аналитик</span><span class="sxs-lookup"><span data-stu-id="afb63-169">Nomenclature of dimensionbased configurations</span></span>
<span data-ttu-id="afb63-170">Для конфигураций, основанных на аналитиках, можно создать специальную номенклатуру для аналитики продукта конфигурации.</span><span class="sxs-lookup"><span data-stu-id="afb63-170">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="afb63-171">Можно выбрать следующие сегменты на странице **Номенклатура продуктов**:</span><span class="sxs-lookup"><span data-stu-id="afb63-171">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="afb63-172">Значение номерной серии</span><span class="sxs-lookup"><span data-stu-id="afb63-172">Number sequence value</span></span>
-   <span data-ttu-id="afb63-173">Текстовая константа</span><span class="sxs-lookup"><span data-stu-id="afb63-173">Text constant</span></span>
-   <span data-ttu-id="afb63-174">Номенклатура конфигурационной группы</span><span class="sxs-lookup"><span data-stu-id="afb63-174">Configuration group item</span></span>

<span data-ttu-id="afb63-175">Номенклатуру конфигурации можно определить для спецификации (BOM).</span><span class="sxs-lookup"><span data-stu-id="afb63-175">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="afb63-176">Пример</span><span class="sxs-lookup"><span data-stu-id="afb63-176">Example</span></span>

<span data-ttu-id="afb63-177">Спецификация имеет четыре строки спецификации, которые делятся на две конфигурационные группы:</span><span class="sxs-lookup"><span data-stu-id="afb63-177">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="afb63-178">Строка спецификации: M0007, стандартный шкаф</span><span class="sxs-lookup"><span data-stu-id="afb63-178">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="afb63-179">Конфигурационная группа: Шкаф</span><span class="sxs-lookup"><span data-stu-id="afb63-179">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="afb63-180">Строка спецификации: M0008, Шкаф верхнего сегмента</span><span class="sxs-lookup"><span data-stu-id="afb63-180">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="afb63-181">Конфигурационная группа: Шкаф</span><span class="sxs-lookup"><span data-stu-id="afb63-181">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="afb63-182">Строка спецификации: M0021, Передняя решетка ткань</span><span class="sxs-lookup"><span data-stu-id="afb63-182">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="afb63-183">Конфигурационная группа: Передняя решетка</span><span class="sxs-lookup"><span data-stu-id="afb63-183">Configuration group: Front grill</span></span>
-   <span data-ttu-id="afb63-184">Строка спецификации: M0022, Передняя решетка металл</span><span class="sxs-lookup"><span data-stu-id="afb63-184">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="afb63-185">Конфигурационная группа: Передняя решетка</span><span class="sxs-lookup"><span data-stu-id="afb63-185">Configuration group: Front grill</span></span>

<span data-ttu-id="afb63-186">Вы создаете номенклатуру конфигурации, имеющую следующие сегменты:</span><span class="sxs-lookup"><span data-stu-id="afb63-186">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="afb63-187">Конфигурационная группа: Шкаф</span><span class="sxs-lookup"><span data-stu-id="afb63-187">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="afb63-188">Текстовая константа: "&"</span><span class="sxs-lookup"><span data-stu-id="afb63-188">Text constant: "&"</span></span>
3.  <span data-ttu-id="afb63-189">Конфигурационная группа: Передняя решетка</span><span class="sxs-lookup"><span data-stu-id="afb63-189">Configuration group: Front grill</span></span>

<span data-ttu-id="afb63-190">В этом случае код конфигурации для стандартного корпуса с тканевой передней решеткой будет M0007&M0021.</span><span class="sxs-lookup"><span data-stu-id="afb63-190">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="afb63-191">Номенклатура для комбинации вариантов продукта и конфигураций</span><span class="sxs-lookup"><span data-stu-id="afb63-191">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="afb63-192">При использовании технологии конфигурации на основе ограничений или на основе аналитик для конфигурации вариантов продукта для шаблона продукта варианты продукта могут получить номера вариантов продукта, которые включают номенклатуру из аналитики конфигурации.</span><span class="sxs-lookup"><span data-stu-id="afb63-192">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="afb63-193">Чтобы настроить варианты, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="afb63-193">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="afb63-194">На странице **Номенклатура продукта** определите номенклатуру номеров вариантов продукта, которые включают аналитику конфигурации.</span><span class="sxs-lookup"><span data-stu-id="afb63-194">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="afb63-195">Назначьте эту номенклатуру группе аналитики продукта, которая имеет аналитику конфигурации.</span><span class="sxs-lookup"><span data-stu-id="afb63-195">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="afb63-196">Определите номенклатуру конфигурации для компонентов или спецификаций, которые будут использоваться для настройки вариантов продукта.</span><span class="sxs-lookup"><span data-stu-id="afb63-196">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="afb63-197">Также можно создать номенклатуры для названий вариантов продукта.</span><span class="sxs-lookup"><span data-stu-id="afb63-197">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="afb63-198">Названия вариантов продуктов можно настроить таким образом, чтобы они содержали код или название конфигурации.</span><span class="sxs-lookup"><span data-stu-id="afb63-198">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="afb63-199">Пример конфигураций на основе ограничений</span><span class="sxs-lookup"><span data-stu-id="afb63-199">Example for constraint-based configurations</span></span>

<span data-ttu-id="afb63-200">Для этого примера используется номенклатура номеров вариантов продукта, которая состоит из следующих сегментов:</span><span class="sxs-lookup"><span data-stu-id="afb63-200">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="afb63-201">Номер шаблона продукта</span><span class="sxs-lookup"><span data-stu-id="afb63-201">Product master number</span></span>
2.  <span data-ttu-id="afb63-202">Текстовая константа: "\_"</span><span class="sxs-lookup"><span data-stu-id="afb63-202">Text constant "\_"</span></span>
3.  <span data-ttu-id="afb63-203">Конфигурация</span><span class="sxs-lookup"><span data-stu-id="afb63-203">Configuration</span></span>

<span data-ttu-id="afb63-204">Номенклатура конфигурации состоит из следующих сегментов:</span><span class="sxs-lookup"><span data-stu-id="afb63-204">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="afb63-205">Значение атрибута: Материал</span><span class="sxs-lookup"><span data-stu-id="afb63-205">Attribute value: Material</span></span>
2.  <span data-ttu-id="afb63-206">Текстовая константа: "AAA"</span><span class="sxs-lookup"><span data-stu-id="afb63-206">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="afb63-207">Значение атрибута: Длина</span><span class="sxs-lookup"><span data-stu-id="afb63-207">Attribute value: Length</span></span>

<span data-ttu-id="afb63-208">Вы вводите следующие значения для сегментов:</span><span class="sxs-lookup"><span data-stu-id="afb63-208">You enter the following values for segments:</span></span>

-   <span data-ttu-id="afb63-209">Номер шаблона продукта = **M0099**</span><span class="sxs-lookup"><span data-stu-id="afb63-209">Product master number = **M0099**</span></span>
-   <span data-ttu-id="afb63-210">Материал = **Пластик**</span><span class="sxs-lookup"><span data-stu-id="afb63-210">Material = **Plastic**</span></span>
-   <span data-ttu-id="afb63-211">Длина = **12**</span><span class="sxs-lookup"><span data-stu-id="afb63-211">Length = **12**</span></span>

<span data-ttu-id="afb63-212">В этом случае номер варианта продукта будет M0099\_ПластикAAA12.</span><span class="sxs-lookup"><span data-stu-id="afb63-212">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="afb63-213">Пример конфигураций на основе аналитик</span><span class="sxs-lookup"><span data-stu-id="afb63-213">Example for dimension-based configurations</span></span>

<span data-ttu-id="afb63-214">Для этого примера используется номенклатура номеров вариантов продукта, которая состоит из следующих сегментов:</span><span class="sxs-lookup"><span data-stu-id="afb63-214">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="afb63-215">Номер шаблона продукта</span><span class="sxs-lookup"><span data-stu-id="afb63-215">Product master number</span></span>
2.  <span data-ttu-id="afb63-216">Текстовая константа "//"</span><span class="sxs-lookup"><span data-stu-id="afb63-216">Text constant "//"</span></span>
3.  <span data-ttu-id="afb63-217">Конфигурация</span><span class="sxs-lookup"><span data-stu-id="afb63-217">Configuration</span></span>

<span data-ttu-id="afb63-218">Номенклатура конфигурации состоит из следующих сегментов:</span><span class="sxs-lookup"><span data-stu-id="afb63-218">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="afb63-219">Конфигурационная группа: Шкаф</span><span class="sxs-lookup"><span data-stu-id="afb63-219">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="afb63-220">Текстовая константа: "&"</span><span class="sxs-lookup"><span data-stu-id="afb63-220">Text constant: "&"</span></span>
3.  <span data-ttu-id="afb63-221">Конфигурационная группа: Передняя решетка</span><span class="sxs-lookup"><span data-stu-id="afb63-221">Configuration group: Front grill</span></span>

<span data-ttu-id="afb63-222">Вы вводите следующие значения для сегментов:</span><span class="sxs-lookup"><span data-stu-id="afb63-222">You enter the following values for segments:</span></span>

-   <span data-ttu-id="afb63-223">Номер шаблона продукта = **D0123**</span><span class="sxs-lookup"><span data-stu-id="afb63-223">Product master number = **D0123**</span></span>
-   <span data-ttu-id="afb63-224">Корпус = **M0008**</span><span class="sxs-lookup"><span data-stu-id="afb63-224">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="afb63-225">Передняя решетка = **M0022**</span><span class="sxs-lookup"><span data-stu-id="afb63-225">Front grill = **M0022**</span></span>

<span data-ttu-id="afb63-226">В этом случае номер варианта продукта будет D0123//M0008&M0022.</span><span class="sxs-lookup"><span data-stu-id="afb63-226">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="afb63-227">Конфликты нумерации</span><span class="sxs-lookup"><span data-stu-id="afb63-227">Numbering conflicts</span></span>
<span data-ttu-id="afb63-228">В некоторых случаях настроенная номенклатура номеров вариантов продукта может не обеспечивать уникальность номеров вариантов продукта.</span><span class="sxs-lookup"><span data-stu-id="afb63-228">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="afb63-229">Например, номера вариантов продукта могут не быть уникальными, если одна из активный аналитик продукта не включена в номенклатуру для шаблона продукта, который использует технологию конфигурации предопределенных вариантов.</span><span class="sxs-lookup"><span data-stu-id="afb63-229">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="afb63-230">Способ обработки конфликтов зависит от технологии конфигурации.</span><span class="sxs-lookup"><span data-stu-id="afb63-230">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="afb63-231">Предопределенные варианты</span><span class="sxs-lookup"><span data-stu-id="afb63-231">Predefined variants</span></span>

<span data-ttu-id="afb63-232">Ошибка возникает, если попытаться создать вручную или автоматически создать варианты продукта, когда нескольким вариантам продукта соответствует одинаковый номер варианта продукта.</span><span class="sxs-lookup"><span data-stu-id="afb63-232">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="afb63-233">Чтобы избежать такого сценария, следует использовать все активные аналитики продукта в группе аналитик продукта.</span><span class="sxs-lookup"><span data-stu-id="afb63-233">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="afb63-234">Можно также включить номерную серию, которая поможет гарантировать уникальность номеров вариантов продукта.</span><span class="sxs-lookup"><span data-stu-id="afb63-234">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="afb63-235">Конфигурации на основе ограничений</span><span class="sxs-lookup"><span data-stu-id="afb63-235">Constraint-based configurations</span></span>

<span data-ttu-id="afb63-236">В зависимости от номенклатуры система может попытаться назначить неуникальный номер варианта продукта для конфигурации.</span><span class="sxs-lookup"><span data-stu-id="afb63-236">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="afb63-237">В этом случае система использует номерную серию для аналитики конфигурации как номер варианта продукта и вы получаете предупреждение.</span><span class="sxs-lookup"><span data-stu-id="afb63-237">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="afb63-238">Чтобы избежать такого сценария, следует включить достаточно атрибутов в номенклатуру для обеспечения уникальности номеров вариантов продукта.</span><span class="sxs-lookup"><span data-stu-id="afb63-238">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="afb63-239">Следует также убедиться в том, что параметр **Повторное использование** включен для компонента.</span><span class="sxs-lookup"><span data-stu-id="afb63-239">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="afb63-240">Конфигурации на основе аналитик</span><span class="sxs-lookup"><span data-stu-id="afb63-240">Dimension-based configurations</span></span>

<span data-ttu-id="afb63-241">Во время одного этапа процесса конфигурации система предлагает значение конфигурация в соответствии с номенклатурой.</span><span class="sxs-lookup"><span data-stu-id="afb63-241">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="afb63-242">На этом этапе можно вручную изменить значение конфигурации.</span><span class="sxs-lookup"><span data-stu-id="afb63-242">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="afb63-243">При сохранении конфигурации система проверяет, является ли значение конфигурации уникальным.</span><span class="sxs-lookup"><span data-stu-id="afb63-243">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="afb63-244">Если введенное значение не является уникальным, вы получите сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="afb63-244">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="afb63-245">Чтобы сохранить конфигурацию, необходимо ввести уникальное значение конфигурации.</span><span class="sxs-lookup"><span data-stu-id="afb63-245">To save the configuration, you must enter a unique configuration value.</span></span>

<a name="see-also"></a><span data-ttu-id="afb63-246">См. также</span><span class="sxs-lookup"><span data-stu-id="afb63-246">See also</span></span>
--------

[<span data-ttu-id="afb63-247">Создание номенклатуры номера продукта для предопределенных вариантов продуктов</span><span class="sxs-lookup"><span data-stu-id="afb63-247">Create a product number nomenclature for predefined product variants</span></span>](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[<span data-ttu-id="afb63-248">Создание номенклатуры номера продукта для сконфигурированных вариантов продуктов</span><span class="sxs-lookup"><span data-stu-id="afb63-248">Create a product number nomenclature for configured product variants</span></span>](tasks/create-product-number-nomenclature-product-variants_2016_11.md)


