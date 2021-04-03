---
title: Преобразование единиц измерения для вариантов продукта
description: В этом разделе объясняется, как настроить пересчеты единиц измерения для вариантов продукта. Он включает пример настройки.
author: johanhoffmann
manager: tfehr
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: ddb6c614ede98e46e46ff284a1a16669bbaaaf66
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258055"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="6488c-104">Преобразование единиц измерения для вариантов продукта</span><span class="sxs-lookup"><span data-stu-id="6488c-104">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6488c-105">В этом разделе объясняется, как настроить пересчеты единиц измерения для различных вариантов продукта.</span><span class="sxs-lookup"><span data-stu-id="6488c-105">This topic explains how to set up unit of measure conversions for various product variants.</span></span>

<span data-ttu-id="6488c-106">Вместо создания нескольких отдельных продуктов, которые необходимо обслуживать, вы можете использовать варианты продукта для создания вариантов одного продукта.</span><span class="sxs-lookup"><span data-stu-id="6488c-106">Instead of creating multiple individual products that must be maintained, you can use product variants to create variations of a single product.</span></span> <span data-ttu-id="6488c-107">Например, вариант продукта может быть футболкой заданного размера и цвета.</span><span class="sxs-lookup"><span data-stu-id="6488c-107">For example, a product variant might be a T-shirt of a given size and color.</span></span>

<span data-ttu-id="6488c-108">Ранее пересчет единиц измерения может быть настроен только для шаблона продукта.</span><span class="sxs-lookup"><span data-stu-id="6488c-108">Previously, unit conversions could be set up only on the product master.</span></span> <span data-ttu-id="6488c-109">Таким образом, все варианты продукта имеют одинаковые правила пересчета единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="6488c-109">Therefore, all product variants had the same unit conversion rules.</span></span> <span data-ttu-id="6488c-110">Однако при включении функции *Пересчеты единиц измерения для вариантов продукта*, если футболки продаются в коробках, а число футболок, которые могут быть упакованы в коробку, зависит от размера футболок, теперь можно настроить пересчет единиц измерения между различными размерами футболки и коробками, используемыми для упаковки.</span><span class="sxs-lookup"><span data-stu-id="6488c-110">However, when the *Unit of measure conversions for product variants* feature is turned on, if your T-shirts are sold in boxes, and the number of T-shirts that can be packed in a box depends on the size of the T-shirts, you can now set up unit conversions between the different shirt sizes and the boxes that are used for packaging.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="6488c-111">Включите функцию в системе</span><span class="sxs-lookup"><span data-stu-id="6488c-111">Turn on the feature in your system</span></span>

<span data-ttu-id="6488c-112">Если эта функция не отображается в системе, перейдите в [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) и включите *Пересчеты единиц измерения для вариантов продукта*.</span><span class="sxs-lookup"><span data-stu-id="6488c-112">If you don't already see this feature in your system, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Unit of measure conversions for product variants* feature.</span></span>

## <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="6488c-113">Настройка продукта для пересчета единиц измерения для вариантов продукта</span><span class="sxs-lookup"><span data-stu-id="6488c-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="6488c-114">Варианты продукта могут создаваться только для продуктов, которые являются шаблоном продукта.</span><span class="sxs-lookup"><span data-stu-id="6488c-114">Product variants can be created only for products that are product masters.</span></span> <span data-ttu-id="6488c-115">Дополнительные сведения см. в разделе [Создание шаблона продукта](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="6488c-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span> <span data-ttu-id="6488c-116">Функция *Пересчеты единиц измерения для вариантов продукта* недоступна для продуктов, которые настроены для процессов "учета в двух единицах измерения".</span><span class="sxs-lookup"><span data-stu-id="6488c-116">The *Unit of measure conversions for product variants* feature isn't available for products that are set up for catch-weight processes.</span></span>

<span data-ttu-id="6488c-117">Чтобы настроить шаблон продукта для поддержки пересчеты единиц измерения по вариантам, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="6488c-117">To configure a product master to support unit conversion per variant, follow these steps.</span></span>

1. <span data-ttu-id="6488c-118">Перейдите в раздел **Управление сведениями о продукте \> Продукты \> Шаблоны продукта**.</span><span class="sxs-lookup"><span data-stu-id="6488c-118">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="6488c-119">Создайте или откройте шаблон продукта, чтобы перейти на страницу **сведений о продукте**.</span><span class="sxs-lookup"><span data-stu-id="6488c-119">Create or open a product master to go to its **Product details** page.</span></span>
1. <span data-ttu-id="6488c-120">Установите для параметра **Включить пересчеты единиц измерения** значение *Да*.</span><span class="sxs-lookup"><span data-stu-id="6488c-120">Set the **Enable unit of measure conversions** option to *Yes*.</span></span>
1. <span data-ttu-id="6488c-121">На панели операций на вкладке **Продукт** в группе **Настройка** выберите **Пересчеты единиц измерения**.</span><span class="sxs-lookup"><span data-stu-id="6488c-121">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Unit conversions**.</span></span>
1. <span data-ttu-id="6488c-122">Откроется страница **Пересчеты единиц измерения**.</span><span class="sxs-lookup"><span data-stu-id="6488c-122">The **Unit conversions** page opens.</span></span> <span data-ttu-id="6488c-123">Выберите один из следующих вкладок:</span><span class="sxs-lookup"><span data-stu-id="6488c-123">Select one of the following tabs:</span></span>

    - <span data-ttu-id="6488c-124">**Пересчеты внутри класса** — выберите эту вкладку для преобразования между единицами измерения, которые относятся к одному и тому же классу единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="6488c-124">**Intra-class conversions** – Select this tab to convert between units that belong to the same unit class.</span></span>
    - <span data-ttu-id="6488c-125">**Пересчеты между классами** — выберите эту вкладку для преобразования между единицами измерения, которые относятся к разным классам единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="6488c-125">**Inter-class conversions** – Select this tab to convert between units that belong to different unit classes.</span></span>

1. <span data-ttu-id="6488c-126">Чтобы добавить новый пересчет единиц измерения, нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="6488c-126">Select **New** to add a new unit conversion.</span></span>
1. <span data-ttu-id="6488c-127">Установите в поле **создать преобразование для** на одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="6488c-127">Set the **Create conversion for** field to one of the following values:</span></span>

    - <span data-ttu-id="6488c-128">**Продукт** — Если выбрано это значение, можно настроить преобразование единиц измерения для шаблона продукта.</span><span class="sxs-lookup"><span data-stu-id="6488c-128">**Product** – If you select this value, you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="6488c-129">Это преобразование единиц будет использоваться как откат для всех вариантов продукта, для которых не определено преобразование единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="6488c-129">That unit conversion will be used as a fallback for all product variants that no unit conversion is defined for.</span></span>
    - <span data-ttu-id="6488c-130">**Вариант продукта** — Если выбрано это значение, можно настроить преобразование единиц измерения для конкретного варианта продукта.</span><span class="sxs-lookup"><span data-stu-id="6488c-130">**Product variant** – If you select this value, you can set up a unit conversion for a specific product variant.</span></span> <span data-ttu-id="6488c-131">Поле **вариант продукта** используется для выбора варианта.</span><span class="sxs-lookup"><span data-stu-id="6488c-131">Use the **Product variant** field to select the variant.</span></span>

    <span data-ttu-id="6488c-132">![Добавление нового пересчеты единиц измерения](media/uom-new-conversion.png "Добавление нового пересчеты единиц измерения")</span><span class="sxs-lookup"><span data-stu-id="6488c-132">![Adding a new unit conversion](media/uom-new-conversion.png "Adding a new unit conversion")</span></span>

1. <span data-ttu-id="6488c-133">Для настройки пересчета единиц измерения используются другие поля, указанные в форме.</span><span class="sxs-lookup"><span data-stu-id="6488c-133">Use the other fields that are provided to set up your unit conversion.</span></span>
1. <span data-ttu-id="6488c-134">Нажмите кнопку **ОК**, чтобы сохранить новое преобразование единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="6488c-134">Select **OK** to save the new unit conversion.</span></span>

> [!TIP]
> <span data-ttu-id="6488c-135">Можно открыть страницу **Пересчеты единиц измерения** для продукта или варианта продукта с одной из следующих страниц:</span><span class="sxs-lookup"><span data-stu-id="6488c-135">You can open the **Unit conversions** page for a product or a product variant from any of the following pages:</span></span>
> 
> - <span data-ttu-id="6488c-136">Сведения о продукте</span><span class="sxs-lookup"><span data-stu-id="6488c-136">Product details</span></span>
> - <span data-ttu-id="6488c-137">Сведения о выпущенных продуктах</span><span class="sxs-lookup"><span data-stu-id="6488c-137">Released products details</span></span>
> - <span data-ttu-id="6488c-138">Используемые варианты продукта</span><span class="sxs-lookup"><span data-stu-id="6488c-138">Released product variants</span></span>

## <a name="example-scenario"></a><span data-ttu-id="6488c-139">Пример сценария</span><span class="sxs-lookup"><span data-stu-id="6488c-139">Example scenario</span></span>

<span data-ttu-id="6488c-140">В этом сценарии компания продает футболки размеров: маленький, средний, большой и очень большой.</span><span class="sxs-lookup"><span data-stu-id="6488c-140">In this scenario, a company sells T-shirts in sizes small, medium, large, and extra-large.</span></span> <span data-ttu-id="6488c-141">Футболка определяется как продукт, и различные размеры определяются как варианты этого продукта.</span><span class="sxs-lookup"><span data-stu-id="6488c-141">The T-shirt is defined as a product, and the different sizes are defined as variants of that product.</span></span> <span data-ttu-id="6488c-142">Эти футболки упакованы в коробки.</span><span class="sxs-lookup"><span data-stu-id="6488c-142">The shirts are packed in boxes.</span></span> <span data-ttu-id="6488c-143">Для маленьких, средних и больших размеров в каждой коробке может быть пять футболок.</span><span class="sxs-lookup"><span data-stu-id="6488c-143">For sizes small, medium, and large, there can be five shirts in each box.</span></span> <span data-ttu-id="6488c-144">Однако для размера "очень большой" в каждой коробке имеется место только для четырех футболок.</span><span class="sxs-lookup"><span data-stu-id="6488c-144">However, for size extra-large, there is space for only four shirts in each box.</span></span>

<span data-ttu-id="6488c-145">Компании необходимо отслеживать различные варианты в единицах *Штуки*, но она продает их в единицах *Коробки*.</span><span class="sxs-lookup"><span data-stu-id="6488c-145">The company wants to track the different variants in the *Pieces* unit, but it's selling them in the *Boxes* unit.</span></span> <span data-ttu-id="6488c-146">Для малых, средних и больших размеров пересчет между единицей измерения запасов и единицей измерения продажи составляет 1 ящик = 5 штук.</span><span class="sxs-lookup"><span data-stu-id="6488c-146">For sizes small, medium, and large, the conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces.</span></span> <span data-ttu-id="6488c-147">Для размера очень крупный преобразование составляет 1 ящик = 4 штуки.</span><span class="sxs-lookup"><span data-stu-id="6488c-147">For size extra-large, the conversion is 1 Box = 4 Pieces.</span></span>

1. <span data-ttu-id="6488c-148">На странице **Сведения о выпущенном продукте** для продукта **Футболка** откройте страницу **Пересчеты единиц измерения**.</span><span class="sxs-lookup"><span data-stu-id="6488c-148">From the **Released product details** page for the **T-Shirt** product, open the **Unit conversions** page.</span></span>
1. <span data-ttu-id="6488c-149">На странице **Пересчеты единиц измерения** настройте следующие пересчеты единиц измерения для варианта выпущенного продукта **Очень большой**.</span><span class="sxs-lookup"><span data-stu-id="6488c-149">On the **Unit conversions** page, set up the following unit conversion for the **X-Large** released product variant.</span></span>

    | <span data-ttu-id="6488c-150">Поле</span><span class="sxs-lookup"><span data-stu-id="6488c-150">Field</span></span>                 | <span data-ttu-id="6488c-151">Настройка</span><span class="sxs-lookup"><span data-stu-id="6488c-151">Setting</span></span>                 |
    |-----------------------|-------------------------|
    | <span data-ttu-id="6488c-152">Создать преобразование для</span><span class="sxs-lookup"><span data-stu-id="6488c-152">Create conversion for</span></span> | <span data-ttu-id="6488c-153">Вариант продукта</span><span class="sxs-lookup"><span data-stu-id="6488c-153">Product variant</span></span>         |
    | <span data-ttu-id="6488c-154">Вариант продукта</span><span class="sxs-lookup"><span data-stu-id="6488c-154">Product variant</span></span>       | <span data-ttu-id="6488c-155">Футболка : : Очень большой : :</span><span class="sxs-lookup"><span data-stu-id="6488c-155">T-Shirt : : X-Large : :</span></span> |
    | <span data-ttu-id="6488c-156">Из единицы</span><span class="sxs-lookup"><span data-stu-id="6488c-156">From unit</span></span>             | <span data-ttu-id="6488c-157">Коробки</span><span class="sxs-lookup"><span data-stu-id="6488c-157">Boxes</span></span>                   |
    | <span data-ttu-id="6488c-158">Множитель</span><span class="sxs-lookup"><span data-stu-id="6488c-158">Factor</span></span>                | <span data-ttu-id="6488c-159">4</span><span class="sxs-lookup"><span data-stu-id="6488c-159">4</span></span>                       |
    | <span data-ttu-id="6488c-160">В ед. изм.</span><span class="sxs-lookup"><span data-stu-id="6488c-160">To Unit</span></span>               | <span data-ttu-id="6488c-161">Штуки</span><span class="sxs-lookup"><span data-stu-id="6488c-161">Pieces</span></span>                  |

1. <span data-ttu-id="6488c-162">Поскольку варианты продуктов **малый**, **средний** и **большой** имеют одинаковые пересчеты единиц измерения между единицами измерения *Коробка* и *Штуки*; это означает, что можно определить следующие пересчеты единиц измерения для них в шаблоне продукта.</span><span class="sxs-lookup"><span data-stu-id="6488c-162">Because the **Small**, **Medium**, and **Large** product variants all have the same unit conversion between the *Box* and *Pieces* units, you can define the following unit conversion for them on the product master.</span></span>

    | <span data-ttu-id="6488c-163">Поле</span><span class="sxs-lookup"><span data-stu-id="6488c-163">Field</span></span>                 | <span data-ttu-id="6488c-164">Настройка</span><span class="sxs-lookup"><span data-stu-id="6488c-164">Setting</span></span> |
    |-----------------------|---------|
    | <span data-ttu-id="6488c-165">Создать преобразование для</span><span class="sxs-lookup"><span data-stu-id="6488c-165">Create conversion for</span></span> | <span data-ttu-id="6488c-166">Продукт</span><span class="sxs-lookup"><span data-stu-id="6488c-166">Product</span></span> |
    | <span data-ttu-id="6488c-167">Продукт</span><span class="sxs-lookup"><span data-stu-id="6488c-167">Product</span></span>               | <span data-ttu-id="6488c-168">Футболка</span><span class="sxs-lookup"><span data-stu-id="6488c-168">T-Shirt</span></span> |
    | <span data-ttu-id="6488c-169">Из единицы</span><span class="sxs-lookup"><span data-stu-id="6488c-169">From unit</span></span>             | <span data-ttu-id="6488c-170">Коробки</span><span class="sxs-lookup"><span data-stu-id="6488c-170">Boxes</span></span>   |
    | <span data-ttu-id="6488c-171">Множитель</span><span class="sxs-lookup"><span data-stu-id="6488c-171">Factor</span></span>                | <span data-ttu-id="6488c-172">5</span><span class="sxs-lookup"><span data-stu-id="6488c-172">5</span></span>       |
    | <span data-ttu-id="6488c-173">В ед. изм.</span><span class="sxs-lookup"><span data-stu-id="6488c-173">To Unit</span></span>               | <span data-ttu-id="6488c-174">Штуки</span><span class="sxs-lookup"><span data-stu-id="6488c-174">Pieces</span></span>  |

## <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="6488c-175">Использование Excel для обновления преобразований единиц измерения</span><span class="sxs-lookup"><span data-stu-id="6488c-175">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="6488c-176">Если у продукта много вариантов с различными пересчетами единиц измерения, рекомендуется экспортировать пересчеты единиц измерения в книгу Microsoft Excel, обновить их, а затем опубликовать снова в Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6488c-176">If a product has many product variants that have different unit conversions, it's a good idea to export the unit conversions to a Microsoft Excel workbook, update them, and then publish them back to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="6488c-177">Для экспорта пересчета единиц измерения в Excel на странице **пересчеты единиц измерения** на панели операций выберите **Открыть в Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="6488c-177">To export unit conversions to Excel, on the **Unit conversions** page, on the Action Pane, select **Open in Microsoft Office**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6488c-178">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6488c-178">Additional resources</span></span>

[<span data-ttu-id="6488c-179">Управление единицей измерения</span><span class="sxs-lookup"><span data-stu-id="6488c-179">Manage unit of measure</span></span>](tasks/manage-unit-measure.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]