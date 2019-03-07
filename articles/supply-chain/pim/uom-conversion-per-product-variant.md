---
title: Преобразование единиц измерения для вариантов продукта
description: В этом разделе объясняется, как преобразования единиц измерения можно настроить для вариантов продукта.
author: johanhoffmann
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 9d5d6fd65717cd886f1c6576aabf2bc59ca4fcaf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "345935"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="c53ea-103">Преобразование единиц измерения для вариантов продукта</span><span class="sxs-lookup"><span data-stu-id="c53ea-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

[!include [pivate-preview](../includes/pivate-preview-banner.md)]

<span data-ttu-id="c53ea-104">В этом разделе объясняется, как преобразования единиц измерения можно настроить для вариантов продукта.</span><span class="sxs-lookup"><span data-stu-id="c53ea-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="c53ea-105">Он включает пример настройки.</span><span class="sxs-lookup"><span data-stu-id="c53ea-105">It includes an example of the setup.</span></span>

<span data-ttu-id="c53ea-106">Эта функция позволяет компаниям определять различные преобразования единиц измерения между вариантами одного продукта.</span><span class="sxs-lookup"><span data-stu-id="c53ea-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="c53ea-107">В этом разделе используется следующий пример.</span><span class="sxs-lookup"><span data-stu-id="c53ea-107">The following example is used in this topic.</span></span> <span data-ttu-id="c53ea-108">Компания продает футболки размеров: маленький, средний, большой и очень большой.</span><span class="sxs-lookup"><span data-stu-id="c53ea-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="c53ea-109">Футболка определяется как продукт, и различные размеры определяются как варианты продукта.</span><span class="sxs-lookup"><span data-stu-id="c53ea-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="c53ea-110">Футболки упакованы в коробки, и может быть пять футболок в коробке, за исключением очень большого размера, для которого в коробку помещается только четыре футболки.</span><span class="sxs-lookup"><span data-stu-id="c53ea-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="c53ea-111">Компании необходимо отслеживать различные варианты футболок в единицах **Штуки**, но она продает футболки в единицах **Коробки**.</span><span class="sxs-lookup"><span data-stu-id="c53ea-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="c53ea-112">Преобразование между единицами измерения складского учета и единицами измерения продаж производится по формуле 1 коробка = 5 штук, за исключением варианта очень большого размера, для которого формула 1 коробка = 4 штуки.</span><span class="sxs-lookup"><span data-stu-id="c53ea-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

## <a name="setup"></a><span data-ttu-id="c53ea-113">Настройка</span><span class="sxs-lookup"><span data-stu-id="c53ea-113">Setup</span></span>

<span data-ttu-id="c53ea-114">Можно настроить параметры для использования этой функции для продуктов, для которых разрешены **Все процессы**, или только для продуктов, для которых разрешены **Складские процессы**, с помощью параметра **Включить преобразования единиц измерения** на странице **Параметры сведений о продукте**.</span><span class="sxs-lookup"><span data-stu-id="c53ea-114">You can configure the parameters for using the feature for products enabled for **All processes** or only for product enabled for the **Warehouse processes** by using the **Enable unit of measure conversations** option on the **Product information parameters** page.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="c53ea-115">Настройка продукта для пересчета единиц измерения для вариантов продукта</span><span class="sxs-lookup"><span data-stu-id="c53ea-115">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="c53ea-116">Варианты продукта могут создаваться только для продуктов **Подтип продукта**: **Шаблон продукта**.</span><span class="sxs-lookup"><span data-stu-id="c53ea-116">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="c53ea-117">Дополнительные сведения см. в разделе [Создание шаблона продукта](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="c53ea-117">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="c53ea-118">Функция не активирована для продуктов, которые были настроены для процессов учета в двух единицах измерения.</span><span class="sxs-lookup"><span data-stu-id="c53ea-118">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="c53ea-119">Во время создания шаблона продукта включите преобразование единиц измерения с помощью параметра **Включить преобразования единиц измерения** на странице **Сведения о продукте**.</span><span class="sxs-lookup"><span data-stu-id="c53ea-119">During the creation of a product master enable unit of measure conversion by using the **Enable unit of measure conversions** option on the **Product details** page.</span></span>

<span data-ttu-id="c53ea-120">При создании шаблона продукта с вариантами запущенных в производство продуктов, можно настроить пересчет единиц измерения в зависимости от варианты.</span><span class="sxs-lookup"><span data-stu-id="c53ea-120">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="c53ea-121">Пункт меню для открытия страницы преобразования единиц измерения в контексте продукта или варианта продукта можно найти на следующих страницах.</span><span class="sxs-lookup"><span data-stu-id="c53ea-121">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="c53ea-122">Страница **Сведения о продукте**</span><span class="sxs-lookup"><span data-stu-id="c53ea-122">**Product details** page</span></span>
-   <span data-ttu-id="c53ea-123">Страница **Сведения об используемых продуктах**</span><span class="sxs-lookup"><span data-stu-id="c53ea-123">**Released products details** page</span></span>
-   <span data-ttu-id="c53ea-124">Страница **Варианты используемого продукта**</span><span class="sxs-lookup"><span data-stu-id="c53ea-124">**Released product variants** page</span></span>

<span data-ttu-id="c53ea-125">При открытии страницы **Пересчет единиц измерения** в контексте шаблона продукта или варианта выпущенного продукта можно выбрать, требуется ли настроить преобразование единиц измерения для продукта или варианта продукта.</span><span class="sxs-lookup"><span data-stu-id="c53ea-125">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="c53ea-126">Это делается путем выбора значения **Вариант продукта** или **Продукт** в поле **Создать преобразование для**.</span><span class="sxs-lookup"><span data-stu-id="c53ea-126">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="c53ea-127">Вариант продукта</span><span class="sxs-lookup"><span data-stu-id="c53ea-127">Product variant</span></span>

<span data-ttu-id="c53ea-128">Если выбрано значение **Вариант продукта**, можно выбрать, для какого варианта требуется настроить преобразование единиц измерения, в поле **Вариант продукта**.</span><span class="sxs-lookup"><span data-stu-id="c53ea-128">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="c53ea-129">Продукт</span><span class="sxs-lookup"><span data-stu-id="c53ea-129">Product</span></span>

<span data-ttu-id="c53ea-130">Если выбрано значение **Продукт**, можно настроить преобразование единиц измерения для шаблона продукта.</span><span class="sxs-lookup"><span data-stu-id="c53ea-130">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="c53ea-131">Этот пересчет единиц измерения будет применяться для всех вариантов продукта, для которых не определено преобразование единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="c53ea-131">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="c53ea-132">Пример</span><span class="sxs-lookup"><span data-stu-id="c53ea-132">Example</span></span>

<span data-ttu-id="c53ea-133">Шаблон продукта **Футболка** имеет четыре выпущенных варианта продукта: маленький, средний, большой и очень большой.</span><span class="sxs-lookup"><span data-stu-id="c53ea-133">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="c53ea-134">Футболки упакованы в коробки, и может быть пять футболок в коробке, за исключением очень большого размера, для которого в коробку помещается только четыре футболки.</span><span class="sxs-lookup"><span data-stu-id="c53ea-134">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="c53ea-135">Во-первых, откройте страницу **Пересчет ед. изм** на странице сведений о выпущенном продукте для продукта **Футболка**.</span><span class="sxs-lookup"><span data-stu-id="c53ea-135">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="c53ea-136">На странице **Пересчет ед. изм.** настройте преобразование единиц измерения для выпущенного варианта продукта "Очень большой".</span><span class="sxs-lookup"><span data-stu-id="c53ea-136">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="c53ea-137">**Поле**</span><span class="sxs-lookup"><span data-stu-id="c53ea-137">**Field**</span></span>             | <span data-ttu-id="c53ea-138">**Настройка**</span><span class="sxs-lookup"><span data-stu-id="c53ea-138">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="c53ea-139">Создать преобразование для</span><span class="sxs-lookup"><span data-stu-id="c53ea-139">Create conversion for</span></span> | <span data-ttu-id="c53ea-140">Вариант продукта</span><span class="sxs-lookup"><span data-stu-id="c53ea-140">Product variant</span></span>         |
| <span data-ttu-id="c53ea-141">Вариант продукта</span><span class="sxs-lookup"><span data-stu-id="c53ea-141">Product variant</span></span>       | <span data-ttu-id="c53ea-142">Футболка : : Очень большой : :</span><span class="sxs-lookup"><span data-stu-id="c53ea-142">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="c53ea-143">Из единицы</span><span class="sxs-lookup"><span data-stu-id="c53ea-143">From unit</span></span>             | <span data-ttu-id="c53ea-144">Коробки</span><span class="sxs-lookup"><span data-stu-id="c53ea-144">Boxes</span></span>                   |
| <span data-ttu-id="c53ea-145">Множитель</span><span class="sxs-lookup"><span data-stu-id="c53ea-145">Factor</span></span>                | <span data-ttu-id="c53ea-146">4</span><span class="sxs-lookup"><span data-stu-id="c53ea-146">4</span></span>                       |
| <span data-ttu-id="c53ea-147">В ед. изм.</span><span class="sxs-lookup"><span data-stu-id="c53ea-147">To Unit</span></span>               | <span data-ttu-id="c53ea-148">Штуки</span><span class="sxs-lookup"><span data-stu-id="c53ea-148">Pieces</span></span>                  |

<span data-ttu-id="c53ea-149">Выпущенные варианты продукта "маленький", "средний" и "большой" имеют одинаковые преобразования единиц измерения между единицами измерения "Коробка" и "Штуки"; это означает, что можно определить преобразование единиц измерения для этих вариантов продукта в шаблоне продукта.</span><span class="sxs-lookup"><span data-stu-id="c53ea-149">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="c53ea-150">**Поле**</span><span class="sxs-lookup"><span data-stu-id="c53ea-150">**Field**</span></span>             | <span data-ttu-id="c53ea-151">**Настройка**</span><span class="sxs-lookup"><span data-stu-id="c53ea-151">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="c53ea-152">Создать преобразование для</span><span class="sxs-lookup"><span data-stu-id="c53ea-152">Create conversion for</span></span> | <span data-ttu-id="c53ea-153">Продукт</span><span class="sxs-lookup"><span data-stu-id="c53ea-153">Product</span></span>     |
| <span data-ttu-id="c53ea-154">Продукт</span><span class="sxs-lookup"><span data-stu-id="c53ea-154">Product</span></span>               | <span data-ttu-id="c53ea-155">Футболка</span><span class="sxs-lookup"><span data-stu-id="c53ea-155">T-Shirt</span></span>     |
| <span data-ttu-id="c53ea-156">Из единицы</span><span class="sxs-lookup"><span data-stu-id="c53ea-156">From unit</span></span>             | <span data-ttu-id="c53ea-157">Коробки</span><span class="sxs-lookup"><span data-stu-id="c53ea-157">Boxes</span></span>       |
| <span data-ttu-id="c53ea-158">Множитель</span><span class="sxs-lookup"><span data-stu-id="c53ea-158">Factor</span></span>                | <span data-ttu-id="c53ea-159">5</span><span class="sxs-lookup"><span data-stu-id="c53ea-159">5</span></span>           |
| <span data-ttu-id="c53ea-160">В ед. изм.</span><span class="sxs-lookup"><span data-stu-id="c53ea-160">To Unit</span></span>               | <span data-ttu-id="c53ea-161">Штуки</span><span class="sxs-lookup"><span data-stu-id="c53ea-161">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="c53ea-162">Использование Excel для обновления преобразований единиц измерения</span><span class="sxs-lookup"><span data-stu-id="c53ea-162">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="c53ea-163">Если для продукта существует много вариантов продукта с различными преобразованиями единиц измерения, рекомендуется экспортировать преобразования единиц измерения со страницы **Пересчет ед. изм** в электронную таблицу Excel, обновить преобразования, затем снова опубликовать их в приложении Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c53ea-163">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Finance and Operations.</span></span>

<span data-ttu-id="c53ea-164">Возможность экспорта в Excel и публикации изменений обратно в приложении Finance and Operations включается в пункте меню **Открыть в Microsoft Office** на панели операций на странице **Пересчет ед. изм.**.</span><span class="sxs-lookup"><span data-stu-id="c53ea-164">The option to export to Excel and publish the edits back to Finance and Operations is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>
