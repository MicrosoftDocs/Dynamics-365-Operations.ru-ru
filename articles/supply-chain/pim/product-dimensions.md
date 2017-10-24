---
title: "Аналитики продуктов"
description: "Предусмотрено четыре аналитики продукта — цвет, конфигурация, размер и стиль. Аналитики продукта объединяются в группы аналитик, а группы аналитик назначаются шаблонам продуктов. Комбинации аналитик продукта определяют, как определяются варианты продуктов."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 105324f146f28bc61e87dff1089b367958ff9062
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="product-dimensions"></a><span data-ttu-id="2b2b5-105">Аналитики продуктов</span><span class="sxs-lookup"><span data-stu-id="2b2b5-105">Product dimensions</span></span>

[!include[banner](../includes/banner.md)]

[!include[Retail name](../includes/retail-name.md)]


<span data-ttu-id="2b2b5-106">Предусмотрено четыре аналитики продукта — цвет, конфигурация, размер и стиль.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-106">There are four product dimensions -  Color, Configuration, Size and Style.</span></span> <span data-ttu-id="2b2b5-107">Аналитики продукта объединяются в группы аналитик, а группы аналитик назначаются шаблонам продуктов.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-107">You combine product dimensions in dimension groups and assign dimension groups to product masters.</span></span> <span data-ttu-id="2b2b5-108">Комбинации аналитик продукта определяют, как определяются варианты продуктов.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-108">The combinations of product dimensions determine how product variants are defined.</span></span>

<span data-ttu-id="2b2b5-109">Аналитики продукта — это характеристики, которые позволяют определить вариант продукта.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-109">Product dimensions are characteristics that serve to identify a product variant.</span></span> <span data-ttu-id="2b2b5-110">Вы можете использовать комбинации аналитик продукта для определения вариантов продуктов.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-110">You can use combinations of product dimensions to define product variants.</span></span> <span data-ttu-id="2b2b5-111">Необходимо определить хотя бы одну аналитику продукта для шаблона продукта, чтобы создать вариант продукта.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-111">You must define at least one product dimension for a product master in order to create a product variant.</span></span>
<span data-ttu-id="2b2b5-112">Варианты продуктов</span><span class="sxs-lookup"><span data-stu-id="2b2b5-112">Product variants</span></span>
----------------

<span data-ttu-id="2b2b5-113">Варианты продуктов также называются номенклатурой.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-113">Product variants are also referred to as items.</span></span> <span data-ttu-id="2b2b5-114">Номенклатура — это материальный продукт в отличие от услуги.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-114">An item is a tangible product, which is not the same as a service.</span></span> <span data-ttu-id="2b2b5-115">Можно также определить шаблон продукта типа "Услуга".</span><span class="sxs-lookup"><span data-stu-id="2b2b5-115">It is also possible to define a product master with the Service type.</span></span> <span data-ttu-id="2b2b5-116">Используя тип "Услуга", можно указать варианты продукта, включающие услуги.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-116">By using the Service type, you can specify product variants that include services.</span></span> <span data-ttu-id="2b2b5-117">Например, можно указать шаблон продукта для консультаций и варианты продуктов для работы, которая выполняется старшими и младшими консультантами.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-117">For example, you can specify a product master for Consultancy work and product variants for work that is performed by senior consultants and junior consultants.</span></span>

## <a name="product-dimensions"></a><span data-ttu-id="2b2b5-118">Аналитики продуктов</span><span class="sxs-lookup"><span data-stu-id="2b2b5-118">Product dimensions</span></span>
<span data-ttu-id="2b2b5-119">Доступны следующие аналитики продукта: конфигурация, цвет, размер и стиль.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-119">The following product dimensions are available: Configuration, Color, Size, and Style.</span></span> <span data-ttu-id="2b2b5-120">Вариант продукта можно создать на основе значений аналитик продукта.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-120">A product variant can be generated based on the product dimension values.</span></span>

<span data-ttu-id="2b2b5-121">Значения аналитик продукта, такие как размер, цвет и стиль, можно создать на страницах **Размер**, **Цвет** и **Стиль**, которые можно открыть из следующих расположений: **Управление сведениями о продукте** &gt; **Настройка** &gt; **Группы аналитик и вариантов** &gt; **Размеры/Цвета/Стили**.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-121">Product dimensions values such as Size, Color and Style can be created on the **Size**, **Color** and **Style** pages, which can be accessed from the following locations: **Product information management** &gt; **Setup** &gt; **Dimension and variant Groups** &gt; **Sizes/Colors/Styles**.</span></span> <span data-ttu-id="2b2b5-122">Значения аналитик продуктов для аналитики "Конфигурация" обычно создаются с помощью конфигуратора продукции или конфигуратора на основе аналитик.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-122">Product dimension values for the Configuration dimension are typically created using either the Product configurator or the Dimension-based configurator.</span></span> <span data-ttu-id="2b2b5-123">Аналитики продуктов можно также создавать и поддерживать на странице **Аналитики продуктов**, которую можно открыть из следующих местоположений:</span><span class="sxs-lookup"><span data-stu-id="2b2b5-123">Product dimensions can also be created and maintained on the **Product dimensions** page, which can be accessed from the following locations:</span></span>
-   <span data-ttu-id="2b2b5-124">Щелкните **Управление сведениями о продукте** &gt; **Продукты** &gt; **Шаблоны продукта**.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-124">Click **Product information management** &gt; **Products** &gt; **Product masters**.</span></span> <span data-ttu-id="2b2b5-125">В **области действий** щелкните **Аналитики продуктов**.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-125">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="2b2b5-126">Щелкните **Управление сведениями о продукте** &gt; **Продукты** &gt; **Все продукты и шаблоны продукции**.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-126">Click **Product information management** &gt; **Products** &gt; **All products and product masters**.</span></span> <span data-ttu-id="2b2b5-127">Выберите шаблон продукта.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-127">Select a product master.</span></span> <span data-ttu-id="2b2b5-128">В **области действий** щелкните **Аналитики продуктов**.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-128">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="2b2b5-129">Щелкните **Управление сведениями о продукте** &gt; **Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-129">Click **Product information management** &gt; **Released products**.</span></span> <span data-ttu-id="2b2b5-130">Выберите шаблон продукта.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-130">Select a product master.</span></span> <span data-ttu-id="2b2b5-131">В **области действий**, щелкните **Продукт**.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-131">On the **Action Pane**, click **Product**.</span></span> <span data-ttu-id="2b2b5-132">В группе **Шаблон продукта** щелкните **Аналитики продуктов**.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-132">In the **Product master** group, click **Product dimensions**.</span></span>

<span data-ttu-id="2b2b5-133">Число вариантов, которые можно создать для номенклатуры, ограничено числом возможных комбинаций аналитик продукта.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-133">The number of variants that you can create for an item is limited by the number of possible product dimension combinations.</span></span>
| <span data-ttu-id="2b2b5-134">**Совет**</span><span class="sxs-lookup"><span data-stu-id="2b2b5-134">**Tip**</span></span>                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b2b5-135">При использовании продукта, например, в строке заказа, вы выбираете аналитики продукта для указания варианта продукта, с которым требуется работать.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-135">When you use a product on, for example, an order line, you select the product dimensions to identify the product variant that you want to work with.</span></span> |

## <a name="example"></a><span data-ttu-id="2b2b5-136">Пример</span><span class="sxs-lookup"><span data-stu-id="2b2b5-136">Example</span></span>
<span data-ttu-id="2b2b5-137">Компания продает джинсы из денима.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-137">A company sells denim jeans.</span></span> <span data-ttu-id="2b2b5-138">Для номенклатуры "Джинсы" используются аналитики "Цвет" и "Размер".</span><span class="sxs-lookup"><span data-stu-id="2b2b5-138">The item, Jeans, uses the Color and Size product dimensions.</span></span> <span data-ttu-id="2b2b5-139">Джинсы продаются в трех различных цветовых решениях и могут быть шести различных размеров.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-139">The jeans are sold in three different colors and six different sizes.</span></span> <span data-ttu-id="2b2b5-140">Цвета: Голубой, Черный, Коричневый Размеры: XS, S, M, L, XL, XXL Не все размеры доступны во всех трех цветах.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-140">Colors: Blue, Black, Brown Sizes: XS, S, M, L, XL, XXL Not all sizes are available in all the three colors.</span></span> <span data-ttu-id="2b2b5-141">Если бы все комбинации были доступны, будет создано 18 разных типов джинсов.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-141">If all combinations were available, it would create 18 different types of jeans.</span></span> <span data-ttu-id="2b2b5-142">В этом примере создаются только следующие девять комбинаций вариантов продукта.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-142">In this example, only the following nine product variant combinations are produced.</span></span>

| <span data-ttu-id="2b2b5-143">Цвет</span><span class="sxs-lookup"><span data-stu-id="2b2b5-143">Color</span></span> | <span data-ttu-id="2b2b5-144">Размер</span><span class="sxs-lookup"><span data-stu-id="2b2b5-144">Size</span></span> |
|-------|------|
| <span data-ttu-id="2b2b5-145">Голубой</span><span class="sxs-lookup"><span data-stu-id="2b2b5-145">Blue</span></span>  | <span data-ttu-id="2b2b5-146">XS</span><span class="sxs-lookup"><span data-stu-id="2b2b5-146">XS</span></span>   |
| <span data-ttu-id="2b2b5-147">Голубой</span><span class="sxs-lookup"><span data-stu-id="2b2b5-147">Blue</span></span>  | <span data-ttu-id="2b2b5-148">П</span><span class="sxs-lookup"><span data-stu-id="2b2b5-148">S</span></span>    |
| <span data-ttu-id="2b2b5-149">Голубой</span><span class="sxs-lookup"><span data-stu-id="2b2b5-149">Blue</span></span>  | <span data-ttu-id="2b2b5-150">Н</span><span class="sxs-lookup"><span data-stu-id="2b2b5-150">M</span></span>    |
| <span data-ttu-id="2b2b5-151">Черный</span><span class="sxs-lookup"><span data-stu-id="2b2b5-151">Black</span></span> | <span data-ttu-id="2b2b5-152">Н</span><span class="sxs-lookup"><span data-stu-id="2b2b5-152">M</span></span>    |
| <span data-ttu-id="2b2b5-153">Черный</span><span class="sxs-lookup"><span data-stu-id="2b2b5-153">Black</span></span> | <span data-ttu-id="2b2b5-154">М</span><span class="sxs-lookup"><span data-stu-id="2b2b5-154">L</span></span>    |
| <span data-ttu-id="2b2b5-155">Черный</span><span class="sxs-lookup"><span data-stu-id="2b2b5-155">Black</span></span> | <span data-ttu-id="2b2b5-156">XL</span><span class="sxs-lookup"><span data-stu-id="2b2b5-156">XL</span></span>   |
| <span data-ttu-id="2b2b5-157">Коричневый</span><span class="sxs-lookup"><span data-stu-id="2b2b5-157">Brown</span></span> | <span data-ttu-id="2b2b5-158">М</span><span class="sxs-lookup"><span data-stu-id="2b2b5-158">L</span></span>    |
| <span data-ttu-id="2b2b5-159">Коричневый</span><span class="sxs-lookup"><span data-stu-id="2b2b5-159">Brown</span></span> | <span data-ttu-id="2b2b5-160">XL</span><span class="sxs-lookup"><span data-stu-id="2b2b5-160">XL</span></span>   |
| <span data-ttu-id="2b2b5-161">Коричневый</span><span class="sxs-lookup"><span data-stu-id="2b2b5-161">Brown</span></span> | <span data-ttu-id="2b2b5-162">XXL</span><span class="sxs-lookup"><span data-stu-id="2b2b5-162">XXL</span></span>  |






