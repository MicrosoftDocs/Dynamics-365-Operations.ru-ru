---
title: Преобразование единиц измерения для вариантов продукта
description: В этом разделе объясняется, как преобразования единиц измерения можно настроить для вариантов продукта.
author: johanhoffmann
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: c8181f0bda9b781a6c2b0feb0aba1beb51bfea65
ms.sourcegitcommit: af36eb17b36092a3101bbfc96486b25036676558
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2020
ms.locfileid: "2935107"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="e0b66-103">Преобразование единиц измерения для вариантов продукта</span><span class="sxs-lookup"><span data-stu-id="e0b66-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0b66-104">В этом разделе объясняется, как преобразования единиц измерения можно настроить для вариантов продукта.</span><span class="sxs-lookup"><span data-stu-id="e0b66-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="e0b66-105">Он включает пример настройки.</span><span class="sxs-lookup"><span data-stu-id="e0b66-105">It includes an example of the setup.</span></span>

<span data-ttu-id="e0b66-106">Эта функция позволяет компаниям определять различные преобразования единиц измерения между вариантами одного продукта.</span><span class="sxs-lookup"><span data-stu-id="e0b66-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="e0b66-107">В этом разделе используется следующий пример.</span><span class="sxs-lookup"><span data-stu-id="e0b66-107">The following example is used in this topic.</span></span> <span data-ttu-id="e0b66-108">Компания продает футболки размеров: маленький, средний, большой и очень большой.</span><span class="sxs-lookup"><span data-stu-id="e0b66-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="e0b66-109">Футболка определяется как продукт, и различные размеры определяются как варианты продукта.</span><span class="sxs-lookup"><span data-stu-id="e0b66-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="e0b66-110">Футболки упакованы в коробки, и может быть пять футболок в коробке, за исключением очень большого размера, для которого в коробку помещается только четыре футболки.</span><span class="sxs-lookup"><span data-stu-id="e0b66-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="e0b66-111">Компании необходимо отслеживать различные варианты футболок в единицах **Штуки**, но она продает футболки в единицах **Коробки**.</span><span class="sxs-lookup"><span data-stu-id="e0b66-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="e0b66-112">Преобразование между единицами измерения складского учета и единицами измерения продаж производится по формуле 1 коробка = 5 штук, за исключением варианта очень большого размера, для которого формула 1 коробка = 4 штуки.</span><span class="sxs-lookup"><span data-stu-id="e0b66-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="e0b66-113">Настройка продукта для пересчета единиц измерения для вариантов продукта</span><span class="sxs-lookup"><span data-stu-id="e0b66-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="e0b66-114">Варианты продукта могут создаваться только для продуктов **Подтип продукта**: **Шаблон продукта**.</span><span class="sxs-lookup"><span data-stu-id="e0b66-114">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="e0b66-115">Дополнительные сведения см. в разделе [Создание шаблона продукта](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="e0b66-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="e0b66-116">Функция не активирована для продуктов, которые были настроены для процессов учета в двух единицах измерения.</span><span class="sxs-lookup"><span data-stu-id="e0b66-116">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="e0b66-117">При создании шаблона продукта с вариантами запущенных в производство продуктов, можно настроить пересчет единиц измерения в зависимости от варианты.</span><span class="sxs-lookup"><span data-stu-id="e0b66-117">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="e0b66-118">Пункт меню для открытия страницы преобразования единиц измерения в контексте продукта или варианта продукта можно найти на следующих страницах.</span><span class="sxs-lookup"><span data-stu-id="e0b66-118">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="e0b66-119">Страница **Сведения о продукте**</span><span class="sxs-lookup"><span data-stu-id="e0b66-119">**Product details** page</span></span>
-   <span data-ttu-id="e0b66-120">Страница **Сведения об используемых продуктах**</span><span class="sxs-lookup"><span data-stu-id="e0b66-120">**Released products details** page</span></span>
-   <span data-ttu-id="e0b66-121">Страница **Варианты используемого продукта**</span><span class="sxs-lookup"><span data-stu-id="e0b66-121">**Released product variants** page</span></span>

<span data-ttu-id="e0b66-122">При открытии страницы **Пересчет единиц измерения** в контексте шаблона продукта или варианта выпущенного продукта можно выбрать, требуется ли настроить преобразование единиц измерения для продукта или варианта продукта.</span><span class="sxs-lookup"><span data-stu-id="e0b66-122">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="e0b66-123">Это делается путем выбора значения **Вариант продукта** или **Продукт** в поле **Создать преобразование для**.</span><span class="sxs-lookup"><span data-stu-id="e0b66-123">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="e0b66-124">Вариант продукта</span><span class="sxs-lookup"><span data-stu-id="e0b66-124">Product variant</span></span>

<span data-ttu-id="e0b66-125">Если выбрано значение **Вариант продукта**, можно выбрать, для какого варианта требуется настроить преобразование единиц измерения, в поле **Вариант продукта**.</span><span class="sxs-lookup"><span data-stu-id="e0b66-125">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="e0b66-126">Продукт</span><span class="sxs-lookup"><span data-stu-id="e0b66-126">Product</span></span>

<span data-ttu-id="e0b66-127">Если выбрано значение **Продукт**, можно настроить преобразование единиц измерения для шаблона продукта.</span><span class="sxs-lookup"><span data-stu-id="e0b66-127">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="e0b66-128">Этот пересчет единиц измерения будет применяться для всех вариантов продукта, для которых не определено преобразование единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="e0b66-128">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="e0b66-129">Пример</span><span class="sxs-lookup"><span data-stu-id="e0b66-129">Example</span></span>

<span data-ttu-id="e0b66-130">Шаблон продукта **Футболка** имеет четыре выпущенных варианта продукта: маленький, средний, большой и очень большой.</span><span class="sxs-lookup"><span data-stu-id="e0b66-130">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="e0b66-131">Футболки упакованы в коробки, и может быть пять футболок в коробке, за исключением очень большого размера, для которого в коробку помещается только четыре футболки.</span><span class="sxs-lookup"><span data-stu-id="e0b66-131">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="e0b66-132">Во-первых, откройте страницу **Пересчет ед. изм** на странице сведений о выпущенном продукте для продукта **Футболка**.</span><span class="sxs-lookup"><span data-stu-id="e0b66-132">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="e0b66-133">На странице **Пересчет ед. изм.** настройте преобразование единиц измерения для выпущенного варианта продукта "Очень большой".</span><span class="sxs-lookup"><span data-stu-id="e0b66-133">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="e0b66-134">**Поле**</span><span class="sxs-lookup"><span data-stu-id="e0b66-134">**Field**</span></span>             | <span data-ttu-id="e0b66-135">**Настройка**</span><span class="sxs-lookup"><span data-stu-id="e0b66-135">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="e0b66-136">Создать преобразование для</span><span class="sxs-lookup"><span data-stu-id="e0b66-136">Create conversion for</span></span> | <span data-ttu-id="e0b66-137">Вариант продукта</span><span class="sxs-lookup"><span data-stu-id="e0b66-137">Product variant</span></span>         |
| <span data-ttu-id="e0b66-138">Вариант продукта</span><span class="sxs-lookup"><span data-stu-id="e0b66-138">Product variant</span></span>       | <span data-ttu-id="e0b66-139">Футболка : : Очень большой : :</span><span class="sxs-lookup"><span data-stu-id="e0b66-139">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="e0b66-140">Из единицы</span><span class="sxs-lookup"><span data-stu-id="e0b66-140">From unit</span></span>             | <span data-ttu-id="e0b66-141">Коробки</span><span class="sxs-lookup"><span data-stu-id="e0b66-141">Boxes</span></span>                   |
| <span data-ttu-id="e0b66-142">Множитель</span><span class="sxs-lookup"><span data-stu-id="e0b66-142">Factor</span></span>                | <span data-ttu-id="e0b66-143">4</span><span class="sxs-lookup"><span data-stu-id="e0b66-143">4</span></span>                       |
| <span data-ttu-id="e0b66-144">В ед. изм.</span><span class="sxs-lookup"><span data-stu-id="e0b66-144">To Unit</span></span>               | <span data-ttu-id="e0b66-145">Штуки</span><span class="sxs-lookup"><span data-stu-id="e0b66-145">Pieces</span></span>                  |

<span data-ttu-id="e0b66-146">Выпущенные варианты продукта "маленький", "средний" и "большой" имеют одинаковые преобразования единиц измерения между единицами измерения "Коробка" и "Штуки"; это означает, что можно определить преобразование единиц измерения для этих вариантов продукта в шаблоне продукта.</span><span class="sxs-lookup"><span data-stu-id="e0b66-146">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="e0b66-147">**Поле**</span><span class="sxs-lookup"><span data-stu-id="e0b66-147">**Field**</span></span>             | <span data-ttu-id="e0b66-148">**Настройка**</span><span class="sxs-lookup"><span data-stu-id="e0b66-148">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="e0b66-149">Создать преобразование для</span><span class="sxs-lookup"><span data-stu-id="e0b66-149">Create conversion for</span></span> | <span data-ttu-id="e0b66-150">Продукт</span><span class="sxs-lookup"><span data-stu-id="e0b66-150">Product</span></span>     |
| <span data-ttu-id="e0b66-151">Продукт</span><span class="sxs-lookup"><span data-stu-id="e0b66-151">Product</span></span>               | <span data-ttu-id="e0b66-152">Футболка</span><span class="sxs-lookup"><span data-stu-id="e0b66-152">T-Shirt</span></span>     |
| <span data-ttu-id="e0b66-153">Из единицы</span><span class="sxs-lookup"><span data-stu-id="e0b66-153">From unit</span></span>             | <span data-ttu-id="e0b66-154">Коробки</span><span class="sxs-lookup"><span data-stu-id="e0b66-154">Boxes</span></span>       |
| <span data-ttu-id="e0b66-155">Множитель</span><span class="sxs-lookup"><span data-stu-id="e0b66-155">Factor</span></span>                | <span data-ttu-id="e0b66-156">5</span><span class="sxs-lookup"><span data-stu-id="e0b66-156">5</span></span>           |
| <span data-ttu-id="e0b66-157">В ед. изм.</span><span class="sxs-lookup"><span data-stu-id="e0b66-157">To Unit</span></span>               | <span data-ttu-id="e0b66-158">Штуки</span><span class="sxs-lookup"><span data-stu-id="e0b66-158">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="e0b66-159">Использование Excel для обновления преобразований единиц измерения</span><span class="sxs-lookup"><span data-stu-id="e0b66-159">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="e0b66-160">Если для продукта существует много вариантов продукта с различными преобразованиями единиц измерения, рекомендуется экспортировать преобразования единиц измерения со страницы **Пересчет ед. изм** в электронную таблицу Excel, обновить преобразования, затем снова опубликовать их в приложении Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e0b66-160">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Supply Chain Mangement.</span></span>

<span data-ttu-id="e0b66-161">Возможность экспорта в Excel и публикации изменений обратно в приложении Supply Chain Management включается в пункте меню **Open in Microsoft Office** на панели операций на странице **Пересчет ед. изм.**.</span><span class="sxs-lookup"><span data-stu-id="e0b66-161">The option to export to Excel and publish the edits back to Supply Chain Mangement is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>
