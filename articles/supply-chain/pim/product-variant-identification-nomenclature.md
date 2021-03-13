---
title: Номенклатура номеров и названий вариантов продуктов
description: В этом разделе описывается, как можно настроить номенклатуру номеров продукции для замены фиксированного формата [Номер шаблона продукта - Конфигурация – Размер - Цвет - Стиль].
author: roxanadiaconu
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: f17f9e1401c68c11e23f327d96028663470b3245
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011330"
---
# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="da11b-103">Номенклатура номеров и названий вариантов продуктов</span><span class="sxs-lookup"><span data-stu-id="da11b-103">Nomenclature of product variant numbers and names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="da11b-104">В этом разделе описывается, как можно настроить номенклатуру номеров продукции для замены фиксированного формата [Номер шаблона продукта - Конфигурация – Размер - Цвет - Стиль].</span><span class="sxs-lookup"><span data-stu-id="da11b-104">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="da11b-105">Новая номенклатура имеет целевой формат, включающий номер шаблона продукта, активные аналитики продукта и разделители текста по вашему выбору.</span><span class="sxs-lookup"><span data-stu-id="da11b-105">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="da11b-106">Также можно создать номенклатуру для названий продуктов.</span><span class="sxs-lookup"><span data-stu-id="da11b-106">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="da11b-107">Наконец, можно создать номенклатуру для идентификации конфигураций, созданных с помощью конфигуратора продукта на основе ограничений.</span><span class="sxs-lookup"><span data-stu-id="da11b-107">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="da11b-108">Эти номенклатуры могут содержать атрибуты по вашему выбору.</span><span class="sxs-lookup"><span data-stu-id="da11b-108">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="da11b-109">Новые номенклатуры для номеров вариантов продуктов и имен вариантов продуктов позволяют включать сегменты в идентификаторы для вариантов продуктов.</span><span class="sxs-lookup"><span data-stu-id="da11b-109">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="da11b-110">Эти сегменты могут включать номер и названием шаблона продукта, коды и названия аналитик продукта, номерные серии, текстовые константы и атрибуты.</span><span class="sxs-lookup"><span data-stu-id="da11b-110">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="da11b-111">Эта функция позволяет быстро найти определенный вариант продукта при создании заказа на продажу или заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="da11b-111">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="da11b-112">Номенклатуры для номеров вариантов продуктов и названий вариантов продуктов создаются с помощью страницы **Номенклатура продуктов**.</span><span class="sxs-lookup"><span data-stu-id="da11b-112">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="da11b-113">Чтобы открыть эту страницу, щелкните **Управление сведениями о продукте** &gt; **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="da11b-113">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="da11b-114">Номенклатура предопределенных вариантов продуктов</span><span class="sxs-lookup"><span data-stu-id="da11b-114">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="da11b-115">Варианты продукта создаются для шаблонов продуктов в соответствии с одной из трех технологий конфигурации:</span><span class="sxs-lookup"><span data-stu-id="da11b-115">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="da11b-116">Предопределенные варианты</span><span class="sxs-lookup"><span data-stu-id="da11b-116">Predefined variants</span></span>
-   <span data-ttu-id="da11b-117">На основе ограничений</span><span class="sxs-lookup"><span data-stu-id="da11b-117">Constraint-based</span></span>
-   <span data-ttu-id="da11b-118">На основе аналитик</span><span class="sxs-lookup"><span data-stu-id="da11b-118">Dimension-based</span></span>

<span data-ttu-id="da11b-119">Каждый вариант продукта имеет номер и название, и номенклатуры идентификации варианта продукта позволяют выбрать сегменты, которые будут включены в каждый номер или название варианта продукта.</span><span class="sxs-lookup"><span data-stu-id="da11b-119">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="da11b-120">Можно выбрать следующие сегменты на странице **Номенклатура продуктов**:</span><span class="sxs-lookup"><span data-stu-id="da11b-120">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="da11b-121">Номер шаблона продукта</span><span class="sxs-lookup"><span data-stu-id="da11b-121">Product master number</span></span>
-   <span data-ttu-id="da11b-122">Имя шаблона продукта</span><span class="sxs-lookup"><span data-stu-id="da11b-122">Product master name</span></span>
-   <span data-ttu-id="da11b-123">Значение номерной серии</span><span class="sxs-lookup"><span data-stu-id="da11b-123">Number sequence value</span></span>
-   <span data-ttu-id="da11b-124">Текстовая константа</span><span class="sxs-lookup"><span data-stu-id="da11b-124">Text constant</span></span>
-   <span data-ttu-id="da11b-125">Аналитики продуктов</span><span class="sxs-lookup"><span data-stu-id="da11b-125">Product dimensions</span></span>
    -   <span data-ttu-id="da11b-126">Код или наименование конфигурации</span><span class="sxs-lookup"><span data-stu-id="da11b-126">Configuration ID or name</span></span>
    -   <span data-ttu-id="da11b-127">Код или название цвета</span><span class="sxs-lookup"><span data-stu-id="da11b-127">Color ID or name</span></span>
    -   <span data-ttu-id="da11b-128">Код или название размера</span><span class="sxs-lookup"><span data-stu-id="da11b-128">Size ID or name</span></span>
    -   <span data-ttu-id="da11b-129">Код или название стиля</span><span class="sxs-lookup"><span data-stu-id="da11b-129">Style ID or name</span></span>

<span data-ttu-id="da11b-130">После определения номенклатуры номеров идентификации вариантов продуктов ее можно связать с группой аналитик продуктов.</span><span class="sxs-lookup"><span data-stu-id="da11b-130">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="da11b-131">Всем шаблонам продуктов, ссылающимся на эту группу аналитик продуктов, будут назначены номера вариантов продуктов в соответствии с номенклатурой.</span><span class="sxs-lookup"><span data-stu-id="da11b-131">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="da11b-132">Однако номенклатуры название вариантов продукта нельзя связать с группами аналитик продуктов.</span><span class="sxs-lookup"><span data-stu-id="da11b-132">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="da11b-133">Можно также назначить номенклатуру идентификации варианта продукта непосредственно шаблону продукта.</span><span class="sxs-lookup"><span data-stu-id="da11b-133">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="da11b-134">В этом случае вариантам продукта, которые относятся к шаблону продукта, будут назначаться номера и названия вариантов продуктов в соответствии с номенклатурами.</span><span class="sxs-lookup"><span data-stu-id="da11b-134">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="da11b-135">Пример</span><span class="sxs-lookup"><span data-stu-id="da11b-135">Example</span></span>

<span data-ttu-id="da11b-136">Футболка (TS1234) выпускается в трех размерах (S, M, L), четырех цветах (красный, зеленый, голубой, желтый) и двух стилях (Поло, V).</span><span class="sxs-lookup"><span data-stu-id="da11b-136">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="da11b-137">Таким образом, возможны 24 варианта продукта (= 3 × 4 × 2).</span><span class="sxs-lookup"><span data-stu-id="da11b-137">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="da11b-138">Вы создаете номенклатуру номеров вариантов продукта, имеющую следующие сегменты:</span><span class="sxs-lookup"><span data-stu-id="da11b-138">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="da11b-139">Номер шаблона продукта</span><span class="sxs-lookup"><span data-stu-id="da11b-139">Product master number</span></span>
2.  <span data-ttu-id="da11b-140">Текстовая константа: "-"</span><span class="sxs-lookup"><span data-stu-id="da11b-140">Text constant: "-"</span></span>
3.  <span data-ttu-id="da11b-141">Цвет</span><span class="sxs-lookup"><span data-stu-id="da11b-141">Color</span></span>
4.  <span data-ttu-id="da11b-142">Текстовая константа: "-"</span><span class="sxs-lookup"><span data-stu-id="da11b-142">Text constant: "-"</span></span>
5.  <span data-ttu-id="da11b-143">Размер</span><span class="sxs-lookup"><span data-stu-id="da11b-143">Size</span></span>
6.  <span data-ttu-id="da11b-144">Текстовая константа: "-"</span><span class="sxs-lookup"><span data-stu-id="da11b-144">Text constant: "-"</span></span>
7.  <span data-ttu-id="da11b-145">Стиль</span><span class="sxs-lookup"><span data-stu-id="da11b-145">Style</span></span>

<span data-ttu-id="da11b-146">В этом случае номер варианта продукта для красной футболки поло маленького размера будет: TS1234-Red-Small-Polo.</span><span class="sxs-lookup"><span data-stu-id="da11b-146">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraint-based-configurations"></a><span data-ttu-id="da11b-147">Номенклатура конфигураций на основе ограничений</span><span class="sxs-lookup"><span data-stu-id="da11b-147">Nomenclature of constraint-based configurations</span></span>
<span data-ttu-id="da11b-148">Для конфигураций, основанных на ограничениях, можно создать специальную номенклатуру для аналитики продукта конфигурации.</span><span class="sxs-lookup"><span data-stu-id="da11b-148">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="da11b-149">Можно выбрать следующие сегменты на странице **Номенклатура продуктов**:</span><span class="sxs-lookup"><span data-stu-id="da11b-149">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="da11b-150">Значение номерной серии</span><span class="sxs-lookup"><span data-stu-id="da11b-150">Number sequence value</span></span>
-   <span data-ttu-id="da11b-151">Текстовая константа</span><span class="sxs-lookup"><span data-stu-id="da11b-151">Text constant</span></span>
-   <span data-ttu-id="da11b-152">Значение атрибута</span><span class="sxs-lookup"><span data-stu-id="da11b-152">Attribute value</span></span>

<span data-ttu-id="da11b-153">Каждый из компонентов в модели конфигурации продукта может иметь собственную номенклатуру конфигурации.</span><span class="sxs-lookup"><span data-stu-id="da11b-153">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="da11b-154">Только атрибуты, принадлежащие компоненту, могут быть использованы.</span><span class="sxs-lookup"><span data-stu-id="da11b-154">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="da11b-155">Атрибуты из субкомпонентов или из требований пользователя использовать невозможно.</span><span class="sxs-lookup"><span data-stu-id="da11b-155">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="da11b-156">Пример</span><span class="sxs-lookup"><span data-stu-id="da11b-156">Example</span></span>

<span data-ttu-id="da11b-157">Модель конфигурации продукта имеет корневой компонент с двумя атрибутами:</span><span class="sxs-lookup"><span data-stu-id="da11b-157">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="da11b-158">Материал (пластик, древесина, сталь)</span><span class="sxs-lookup"><span data-stu-id="da11b-158">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="da11b-159">Длина (10...100)</span><span class="sxs-lookup"><span data-stu-id="da11b-159">Length (10...100)</span></span>

<span data-ttu-id="da11b-160">Вы создаете номенклатуру конфигурации, имеющую следующие сегменты:</span><span class="sxs-lookup"><span data-stu-id="da11b-160">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="da11b-161">Значение атрибута: Материал</span><span class="sxs-lookup"><span data-stu-id="da11b-161">Attribute value: Material</span></span>
2.  <span data-ttu-id="da11b-162">Текстовая константа: "AAA"</span><span class="sxs-lookup"><span data-stu-id="da11b-162">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="da11b-163">Значение атрибута: Длина</span><span class="sxs-lookup"><span data-stu-id="da11b-163">Attribute value: Length</span></span>

<span data-ttu-id="da11b-164">В этом случае код конфигурации для деревянного материала с длиной 78 будет WoodAAA78.</span><span class="sxs-lookup"><span data-stu-id="da11b-164">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimension-based-configurations"></a><span data-ttu-id="da11b-165">Номенклатура конфигураций на основе аналитик</span><span class="sxs-lookup"><span data-stu-id="da11b-165">Nomenclature of dimension-based configurations</span></span>
<span data-ttu-id="da11b-166">Для конфигураций, основанных на аналитиках, можно создать специальную номенклатуру для аналитики продукта конфигурации.</span><span class="sxs-lookup"><span data-stu-id="da11b-166">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="da11b-167">Можно выбрать следующие сегменты на странице **Номенклатура продуктов**:</span><span class="sxs-lookup"><span data-stu-id="da11b-167">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="da11b-168">Значение номерной серии</span><span class="sxs-lookup"><span data-stu-id="da11b-168">Number sequence value</span></span>
-   <span data-ttu-id="da11b-169">Текстовая константа</span><span class="sxs-lookup"><span data-stu-id="da11b-169">Text constant</span></span>
-   <span data-ttu-id="da11b-170">Номенклатура конфигурационной группы</span><span class="sxs-lookup"><span data-stu-id="da11b-170">Configuration group item</span></span>

<span data-ttu-id="da11b-171">Номенклатуру конфигурации можно определить для спецификации (BOM).</span><span class="sxs-lookup"><span data-stu-id="da11b-171">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="da11b-172">Пример</span><span class="sxs-lookup"><span data-stu-id="da11b-172">Example</span></span>

<span data-ttu-id="da11b-173">Спецификация имеет четыре строки спецификации, которые делятся на две конфигурационные группы:</span><span class="sxs-lookup"><span data-stu-id="da11b-173">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="da11b-174">Строка спецификации: M0007, стандартный шкаф</span><span class="sxs-lookup"><span data-stu-id="da11b-174">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="da11b-175">Конфигурационная группа: Шкаф</span><span class="sxs-lookup"><span data-stu-id="da11b-175">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="da11b-176">Строка спецификации: M0008, Шкаф верхнего сегмента</span><span class="sxs-lookup"><span data-stu-id="da11b-176">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="da11b-177">Конфигурационная группа: Шкаф</span><span class="sxs-lookup"><span data-stu-id="da11b-177">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="da11b-178">Строка спецификации: M0021, Передняя решетка ткань</span><span class="sxs-lookup"><span data-stu-id="da11b-178">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="da11b-179">Конфигурационная группа: Передняя решетка</span><span class="sxs-lookup"><span data-stu-id="da11b-179">Configuration group: Front grill</span></span>
-   <span data-ttu-id="da11b-180">Строка спецификации: M0022, Передняя решетка металл</span><span class="sxs-lookup"><span data-stu-id="da11b-180">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="da11b-181">Конфигурационная группа: Передняя решетка</span><span class="sxs-lookup"><span data-stu-id="da11b-181">Configuration group: Front grill</span></span>

<span data-ttu-id="da11b-182">Вы создаете номенклатуру конфигурации, имеющую следующие сегменты:</span><span class="sxs-lookup"><span data-stu-id="da11b-182">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="da11b-183">Конфигурационная группа: Шкаф</span><span class="sxs-lookup"><span data-stu-id="da11b-183">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="da11b-184">Текстовая константа: "&"</span><span class="sxs-lookup"><span data-stu-id="da11b-184">Text constant: "&"</span></span>
3.  <span data-ttu-id="da11b-185">Конфигурационная группа: Передняя решетка</span><span class="sxs-lookup"><span data-stu-id="da11b-185">Configuration group: Front grill</span></span>

<span data-ttu-id="da11b-186">В этом случае код конфигурации для стандартного корпуса с тканевой передней решеткой будет M0007&M0021.</span><span class="sxs-lookup"><span data-stu-id="da11b-186">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="da11b-187">Номенклатура для комбинации вариантов продукта и конфигураций</span><span class="sxs-lookup"><span data-stu-id="da11b-187">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="da11b-188">При использовании технологии конфигурации на основе ограничений или на основе аналитик для конфигурации вариантов продукта для шаблона продукта варианты продукта могут получить номера вариантов продукта, которые включают номенклатуру из аналитики конфигурации.</span><span class="sxs-lookup"><span data-stu-id="da11b-188">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="da11b-189">Чтобы настроить варианты, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="da11b-189">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="da11b-190">На странице **Номенклатура продукта** определите номенклатуру номеров вариантов продукта, которые включают аналитику конфигурации.</span><span class="sxs-lookup"><span data-stu-id="da11b-190">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="da11b-191">Назначьте эту номенклатуру группе аналитики продукта, которая имеет аналитику конфигурации.</span><span class="sxs-lookup"><span data-stu-id="da11b-191">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="da11b-192">Определите номенклатуру конфигурации для компонентов или спецификаций, которые будут использоваться для настройки вариантов продукта.</span><span class="sxs-lookup"><span data-stu-id="da11b-192">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="da11b-193">Также можно создать номенклатуры для названий вариантов продукта.</span><span class="sxs-lookup"><span data-stu-id="da11b-193">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="da11b-194">Названия вариантов продуктов можно настроить таким образом, чтобы они содержали код или название конфигурации.</span><span class="sxs-lookup"><span data-stu-id="da11b-194">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="da11b-195">Пример конфигураций на основе ограничений</span><span class="sxs-lookup"><span data-stu-id="da11b-195">Example for constraint-based configurations</span></span>

<span data-ttu-id="da11b-196">Для этого примера используется номенклатура номеров вариантов продукта, которая состоит из следующих сегментов:</span><span class="sxs-lookup"><span data-stu-id="da11b-196">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="da11b-197">Номер шаблона продукта</span><span class="sxs-lookup"><span data-stu-id="da11b-197">Product master number</span></span>
2.  <span data-ttu-id="da11b-198">Текстовая константа: "\_"</span><span class="sxs-lookup"><span data-stu-id="da11b-198">Text constant "\_"</span></span>
3.  <span data-ttu-id="da11b-199">Конфигурация</span><span class="sxs-lookup"><span data-stu-id="da11b-199">Configuration</span></span>

<span data-ttu-id="da11b-200">Номенклатура конфигурации состоит из следующих сегментов:</span><span class="sxs-lookup"><span data-stu-id="da11b-200">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="da11b-201">Значение атрибута: Материал</span><span class="sxs-lookup"><span data-stu-id="da11b-201">Attribute value: Material</span></span>
2.  <span data-ttu-id="da11b-202">Текстовая константа: "AAA"</span><span class="sxs-lookup"><span data-stu-id="da11b-202">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="da11b-203">Значение атрибута: Длина</span><span class="sxs-lookup"><span data-stu-id="da11b-203">Attribute value: Length</span></span>

<span data-ttu-id="da11b-204">Вы вводите следующие значения для сегментов:</span><span class="sxs-lookup"><span data-stu-id="da11b-204">You enter the following values for segments:</span></span>

-   <span data-ttu-id="da11b-205">Номер шаблона продукта = **M0099**</span><span class="sxs-lookup"><span data-stu-id="da11b-205">Product master number = **M0099**</span></span>
-   <span data-ttu-id="da11b-206">Материал = **Пластик**</span><span class="sxs-lookup"><span data-stu-id="da11b-206">Material = **Plastic**</span></span>
-   <span data-ttu-id="da11b-207">Длина = **12**</span><span class="sxs-lookup"><span data-stu-id="da11b-207">Length = **12**</span></span>

<span data-ttu-id="da11b-208">В этом случае номер варианта продукта будет M0099\_ПластикAAA12.</span><span class="sxs-lookup"><span data-stu-id="da11b-208">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="da11b-209">Пример конфигураций на основе аналитик</span><span class="sxs-lookup"><span data-stu-id="da11b-209">Example for dimension-based configurations</span></span>

<span data-ttu-id="da11b-210">Для этого примера используется номенклатура номеров вариантов продукта, которая состоит из следующих сегментов:</span><span class="sxs-lookup"><span data-stu-id="da11b-210">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="da11b-211">Номер шаблона продукта</span><span class="sxs-lookup"><span data-stu-id="da11b-211">Product master number</span></span>
2.  <span data-ttu-id="da11b-212">Текстовая константа "//"</span><span class="sxs-lookup"><span data-stu-id="da11b-212">Text constant "//"</span></span>
3.  <span data-ttu-id="da11b-213">Конфигурация</span><span class="sxs-lookup"><span data-stu-id="da11b-213">Configuration</span></span>

<span data-ttu-id="da11b-214">Номенклатура конфигурации состоит из следующих сегментов:</span><span class="sxs-lookup"><span data-stu-id="da11b-214">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="da11b-215">Конфигурационная группа: Шкаф</span><span class="sxs-lookup"><span data-stu-id="da11b-215">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="da11b-216">Текстовая константа: "&"</span><span class="sxs-lookup"><span data-stu-id="da11b-216">Text constant: "&"</span></span>
3.  <span data-ttu-id="da11b-217">Конфигурационная группа: Передняя решетка</span><span class="sxs-lookup"><span data-stu-id="da11b-217">Configuration group: Front grill</span></span>

<span data-ttu-id="da11b-218">Вы вводите следующие значения для сегментов:</span><span class="sxs-lookup"><span data-stu-id="da11b-218">You enter the following values for segments:</span></span>

-   <span data-ttu-id="da11b-219">Номер шаблона продукта = **D0123**</span><span class="sxs-lookup"><span data-stu-id="da11b-219">Product master number = **D0123**</span></span>
-   <span data-ttu-id="da11b-220">Корпус = **M0008**</span><span class="sxs-lookup"><span data-stu-id="da11b-220">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="da11b-221">Передняя решетка = **M0022**</span><span class="sxs-lookup"><span data-stu-id="da11b-221">Front grill = **M0022**</span></span>

<span data-ttu-id="da11b-222">В этом случае номер варианта продукта будет D0123//M0008&M0022.</span><span class="sxs-lookup"><span data-stu-id="da11b-222">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="da11b-223">Конфликты нумерации</span><span class="sxs-lookup"><span data-stu-id="da11b-223">Numbering conflicts</span></span>
<span data-ttu-id="da11b-224">В некоторых случаях настроенная номенклатура номеров вариантов продукта может не обеспечивать уникальность номеров вариантов продукта.</span><span class="sxs-lookup"><span data-stu-id="da11b-224">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="da11b-225">Например, номера вариантов продукта могут не быть уникальными, если одна из активный аналитик продукта не включена в номенклатуру для шаблона продукта, который использует технологию конфигурации предопределенных вариантов.</span><span class="sxs-lookup"><span data-stu-id="da11b-225">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="da11b-226">Способ обработки конфликтов зависит от технологии конфигурации.</span><span class="sxs-lookup"><span data-stu-id="da11b-226">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="da11b-227">Предопределенные варианты</span><span class="sxs-lookup"><span data-stu-id="da11b-227">Predefined variants</span></span>

<span data-ttu-id="da11b-228">Ошибка возникает, если попытаться создать вручную или автоматически создать варианты продукта, когда нескольким вариантам продукта соответствует одинаковый номер варианта продукта.</span><span class="sxs-lookup"><span data-stu-id="da11b-228">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="da11b-229">Чтобы избежать такого сценария, следует использовать все активные аналитики продукта в группе аналитик продукта.</span><span class="sxs-lookup"><span data-stu-id="da11b-229">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="da11b-230">Можно также включить номерную серию, которая поможет гарантировать уникальность номеров вариантов продукта.</span><span class="sxs-lookup"><span data-stu-id="da11b-230">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="da11b-231">Конфигурации на основе ограничений</span><span class="sxs-lookup"><span data-stu-id="da11b-231">Constraint-based configurations</span></span>

<span data-ttu-id="da11b-232">В зависимости от номенклатуры система может попытаться назначить неуникальный номер варианта продукта для конфигурации.</span><span class="sxs-lookup"><span data-stu-id="da11b-232">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="da11b-233">В этом случае система использует номерную серию для аналитики конфигурации как номер варианта продукта и вы получаете предупреждение.</span><span class="sxs-lookup"><span data-stu-id="da11b-233">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="da11b-234">Чтобы избежать такого сценария, следует включить достаточно атрибутов в номенклатуру для обеспечения уникальности номеров вариантов продукта.</span><span class="sxs-lookup"><span data-stu-id="da11b-234">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="da11b-235">Следует также убедиться в том, что параметр **Повторное использование** включен для компонента.</span><span class="sxs-lookup"><span data-stu-id="da11b-235">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="da11b-236">Конфигурации на основе аналитик</span><span class="sxs-lookup"><span data-stu-id="da11b-236">Dimension-based configurations</span></span>

<span data-ttu-id="da11b-237">Во время одного этапа процесса конфигурации система предлагает значение конфигурация в соответствии с номенклатурой.</span><span class="sxs-lookup"><span data-stu-id="da11b-237">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="da11b-238">На этом этапе можно вручную изменить значение конфигурации.</span><span class="sxs-lookup"><span data-stu-id="da11b-238">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="da11b-239">При сохранении конфигурации система проверяет, является ли значение конфигурации уникальным.</span><span class="sxs-lookup"><span data-stu-id="da11b-239">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="da11b-240">Если введенное значение не является уникальным, вы получите сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="da11b-240">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="da11b-241">Чтобы сохранить конфигурацию, необходимо ввести уникальное значение конфигурации.</span><span class="sxs-lookup"><span data-stu-id="da11b-241">To save the configuration, you must enter a unique configuration value.</span></span>

<a name="additional-resources"></a><span data-ttu-id="da11b-242">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="da11b-242">Additional resources</span></span>
--------

[<span data-ttu-id="da11b-243">Создание номенклатуры номера продукта для заранее определенных вариантов продукта</span><span class="sxs-lookup"><span data-stu-id="da11b-243">Create a product number nomenclature for predefined product variants</span></span>](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[<span data-ttu-id="da11b-244">Создание номенклатуры номера продукта для сконфигурированных вариантов продуктов</span><span class="sxs-lookup"><span data-stu-id="da11b-244">Create a product number nomenclature for configured product variants</span></span>](tasks/create-product-number-nomenclature-product-variants_2016_11.md)

