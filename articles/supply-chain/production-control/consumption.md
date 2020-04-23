---
title: Расчет потребления материалов
description: В этой статье представлена информация о различных параметрах, связанных с расчетом потребления материалов.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f58365278200344169b93658e9c92dea2bc4f18f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211650"
---
# <a name="calculate-material-consumption"></a><span data-ttu-id="d8855-103">Расчет потребления материалов</span><span class="sxs-lookup"><span data-stu-id="d8855-103">Calculate material consumption</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d8855-104">В этой статье представлена информация о различных параметрах, связанных с расчетом потребления материалов.</span><span class="sxs-lookup"><span data-stu-id="d8855-104">This article provides information about various options that are related to the calculation of material consumption.</span></span> 

<span data-ttu-id="d8855-105">Следующие параметры, которые отнесены к вычислению материального потребления, доступны на вкладках **Настройка** и **Ступенчатое потребление** на экспресс-вкладке **Сведения о строке** страницы **Спецификация**.</span><span class="sxs-lookup"><span data-stu-id="d8855-105">The following options that are related to the calculation of material consumption are available on the **Setup** and **Step consumption** tabs on the **Line details** FastTab of the **Bill of materials** page.</span></span>

## <a name="variable-and-constant-consumption"></a><span data-ttu-id="d8855-106">Переменное и постоянное потребление</span><span class="sxs-lookup"><span data-stu-id="d8855-106">Variable and constant consumption</span></span>
<span data-ttu-id="d8855-107">В поле **Потребление** вы можете выбрать, должно ли потребление рассчитываться как постоянное или переменное количество.</span><span class="sxs-lookup"><span data-stu-id="d8855-107">In the **Consumption is** field, you can select whether consumption should be calculated as a constant quantity or a variable quantity.</span></span> <span data-ttu-id="d8855-108">Выберите **Константа**, если фиксированные количество или объем необходимы для производства, независимо от количества, которое произведено.</span><span class="sxs-lookup"><span data-stu-id="d8855-108">Select **Constant** if a fixed quantity or volume is required for the production, regardless of the quantity that is produced.</span></span> <span data-ttu-id="d8855-109">Выберите **Переменная** (настройка по умолчанию), если необходимое количество материала в готовых товарах пропорционально количеству произведенных готовых товаров.</span><span class="sxs-lookup"><span data-stu-id="d8855-109">Select **Variable**, which is the default setting, if the required amount of material in the finished goods is proportional to the number of finished goods that are produced.</span></span>

## <a name="calculating-consumption-from-a-formula"></a><span data-ttu-id="d8855-110">Расчет потребления по формуле</span><span class="sxs-lookup"><span data-stu-id="d8855-110">Calculating consumption from a formula</span></span>
<span data-ttu-id="d8855-111">В поле **Формула** можно настроить различные формулы для расчета материального потребления.</span><span class="sxs-lookup"><span data-stu-id="d8855-111">In the **Formula** field, you can set up various formulas for calculating material consumption.</span></span> <span data-ttu-id="d8855-112">Если вы используете значение по умолчанию **Стандартное**, потребление не высчитывается по формуле.</span><span class="sxs-lookup"><span data-stu-id="d8855-112">If you use the default value, **Standard**, the consumption isn't calculated from a formula.</span></span> <span data-ttu-id="d8855-113">Следующие формулы работают вместе полями **Высота**, **Ширина**, **Глубина**, **Плотность** и **Константа**:</span><span class="sxs-lookup"><span data-stu-id="d8855-113">The following formulas work together with the **Height**, **Width**, **Depth**, **Density**, and **Constant** fields:</span></span>

-   <span data-ttu-id="d8855-114">Высота \* Константа</span><span class="sxs-lookup"><span data-stu-id="d8855-114">Height \* Constant</span></span>
-   <span data-ttu-id="d8855-115">Высота \* Ширина \* Константа</span><span class="sxs-lookup"><span data-stu-id="d8855-115">Height \* Width \* Constant</span></span>
-   <span data-ttu-id="d8855-116">Высота \* Ширина \* Глубина \* Константа</span><span class="sxs-lookup"><span data-stu-id="d8855-116">Height \* Width \* Depth \* Constant</span></span>
-   <span data-ttu-id="d8855-117">(Высота \* Ширина \* Глубина / Плотность) \* Константа</span><span class="sxs-lookup"><span data-stu-id="d8855-117">(Height \* Width \* Depth / Density) \* Constant</span></span>

## <a name="rounding-up-and-multiples"></a><span data-ttu-id="d8855-118">Округление и кратность</span><span class="sxs-lookup"><span data-stu-id="d8855-118">Rounding up and multiples</span></span>
<span data-ttu-id="d8855-119">Совместно поля **В большую сторону** и **Кратное** позволяют округлять в большую сторону значение материального потребления.</span><span class="sxs-lookup"><span data-stu-id="d8855-119">Together, the **Rounding up** and **Multiples** fields let you round up the material consumption value.</span></span> <span data-ttu-id="d8855-120">Например, вы можете округлить вверх значение согласно единице обработки, в которой сырье выбирается для производства.</span><span class="sxs-lookup"><span data-stu-id="d8855-120">For example, you can round up the value according to the handling unit in which the raw material is picked for production.</span></span> <span data-ttu-id="d8855-121">Следующие параметры доступны в поле **В большую сторону**: **Количество**, **Измерение** и **Потребление**.</span><span class="sxs-lookup"><span data-stu-id="d8855-121">The following options are available in the **Rounding up** field: **Quantity**, **Measurement**, and **Consumption**.</span></span>

### <a name="quantity"></a><span data-ttu-id="d8855-122">Количество</span><span class="sxs-lookup"><span data-stu-id="d8855-122">Quantity</span></span>

<span data-ttu-id="d8855-123">Если вы выбираете **Количество** в качестве механизма округления, то количество должно быть кратно указанному количеству.</span><span class="sxs-lookup"><span data-stu-id="d8855-123">If you select **Quantity** as the rounding-up mechanism, the quantity must be a multiple of the specified quantity.</span></span> <span data-ttu-id="d8855-124">Например, когда требуются целые числа, укажите **1** в поле **Кратное**.</span><span class="sxs-lookup"><span data-stu-id="d8855-124">For example, if whole numbers are required, select **1** in the **Multiples** field.</span></span> <span data-ttu-id="d8855-125">Числа после этого округляются в большую сторону до количества, кратное 1.</span><span class="sxs-lookup"><span data-stu-id="d8855-125">Numbers are then rounded up to a quantity that is divisible by 1.</span></span>

### <a name="measurement"></a><span data-ttu-id="d8855-126">Измерение</span><span class="sxs-lookup"><span data-stu-id="d8855-126">Measurement</span></span>

<span data-ttu-id="d8855-127">Обычно механизм округления **Измерение** выбирается, когда сырье приходит со специфическим размером.</span><span class="sxs-lookup"><span data-stu-id="d8855-127">Typically, you select **Measurement** as the rounding-up mechanism when the raw material comes in specific dimensions.</span></span> <span data-ttu-id="d8855-128">Например, часть металлической трубы длиной 2 метра необходима для законченного изделия, а металлическая труба хранится в сортаменте длиной 4,5 метра.</span><span class="sxs-lookup"><span data-stu-id="d8855-128">For example, a piece of 2-meter metal tube is required for a finished good, and the metal tube is stored in 4.5-meter lengths.</span></span> <span data-ttu-id="d8855-129">В этом случае можно использовать механизм округления **Измерение**, чтобы высчитать, сколько металлических труб необходимо для производства определенного числа готовых изделий.</span><span class="sxs-lookup"><span data-stu-id="d8855-129">In this case, the **Measurement** rounding-up mechanism can be used to calculate how many metal tubes are required to produce a specific number of pieces of the finished good.</span></span> <span data-ttu-id="d8855-130">Для этого примера в поле **Формула** задается значение **Высота \* Константа**.</span><span class="sxs-lookup"><span data-stu-id="d8855-130">For this example, the **Formula** field is set to **Height \* Constant**.</span></span> <span data-ttu-id="d8855-131">В поле **Высота** задается значение **2**, чтобы указать длину трубы, которая необходима для законченного изделия.</span><span class="sxs-lookup"><span data-stu-id="d8855-131">The **Height** field is set to **2** to indicate the length of the tube that is required for the finished good.</span></span> <span data-ttu-id="d8855-132">В поле **Кратное** установлено значение **4,5**, чтобы указать, что труба поступает длиной 4,5 м.</span><span class="sxs-lookup"><span data-stu-id="d8855-132">The **Multiple** field is set to **4.5** to indicate that the tube is picked in lengths of 4.5 meters.</span></span> <span data-ttu-id="d8855-133">Расчет производится следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d8855-133">Here is the calculation:</span></span>

1.  <span data-ttu-id="d8855-134">Кратное количество, необходимое для 10 готовых изделий: 10 ÷ 2 = 5 шт.</span><span class="sxs-lookup"><span data-stu-id="d8855-134">Number of multiples that are required for 10 pieces of the finished good: 10 ÷ 2 = 5 pieces</span></span>
2.  <span data-ttu-id="d8855-135">Полное потребление: 4,5 × 5 = 22,5 м металлической трубы</span><span class="sxs-lookup"><span data-stu-id="d8855-135">Total consumption:  4.5 × 5 = 22.5 meters of metal tube</span></span>

<span data-ttu-id="d8855-136">Предполагается, что 0,5 м трубы сдаются в утиль для каждого из пяти потребленных отрезков трубы.</span><span class="sxs-lookup"><span data-stu-id="d8855-136">It's assumed that 0.5 meter of tube is scrapped for every five pieces of tube that are consumed.</span></span>

### <a name="consumption"></a><span data-ttu-id="d8855-137">Себестоимость</span><span class="sxs-lookup"><span data-stu-id="d8855-137">Consumption</span></span>

<span data-ttu-id="d8855-138">Обычно значение **Потребление** выбирается в качестве метода округления, когда сырье необходимо выбрать в целых количествах определенной единицы обработки продукта.</span><span class="sxs-lookup"><span data-stu-id="d8855-138">Typically, you select **Consumption** as the rounding-up mechanism when raw material must be picked in whole quantities of a specific handling unit of the product.</span></span> <span data-ttu-id="d8855-139">Например, 2 кварты краски используются для производства одной единицы готового изделия, и краска поставляется банками объемом 25 кварт.</span><span class="sxs-lookup"><span data-stu-id="d8855-139">For example, 2 quarts of paint are used to produce one piece of a finished good, and the paint is picked in 25-quart cans.</span></span> <span data-ttu-id="d8855-140">В этом случае механизм округления **Потребление** можно использовать для того, чтобы округлить потребление до целого количества банок емкостью 25 кварт.</span><span class="sxs-lookup"><span data-stu-id="d8855-140">In this case, the **Consumption** rounding-up mechanism can be used to round up consumption to whole numbers of 25-quart cans.</span></span> <span data-ttu-id="d8855-141">Ниже приведен расчет количества краски, которая необходимо, если нужно произвести 180 единиц готовых изделий:</span><span class="sxs-lookup"><span data-stu-id="d8855-141">Here is the calculation for the amount of paint that is required if 180 pieces of the finished good must be produced:</span></span>

1.  <span data-ttu-id="d8855-142">Необходимая краска, без отходов: 180 × 2 = 360 кварт</span><span class="sxs-lookup"><span data-stu-id="d8855-142">Paint that is required, excluding scrap: 180 × 2 = 360 quarts</span></span>
2.  <span data-ttu-id="d8855-143">Количество банок: 360 ÷ 25 = 14,4, что округляется вверх до 15</span><span class="sxs-lookup"><span data-stu-id="d8855-143">Number of cans: 360 ÷ 25 = 14.4, which is rounded up to 15</span></span>
3.  <span data-ttu-id="d8855-144">Необходимая краска, включая отходы: 15 × 25 = 375 кварт</span><span class="sxs-lookup"><span data-stu-id="d8855-144">Paint that is required, including scrap: 15 × 25 = 375 quarts</span></span>

## <a name="step-consumption"></a><span data-ttu-id="d8855-145">Потребление на шаге</span><span class="sxs-lookup"><span data-stu-id="d8855-145">Step consumption</span></span>
<span data-ttu-id="d8855-146">Ступенчатое потребление используется для расчета постоянного потребления с количественными интервалами.</span><span class="sxs-lookup"><span data-stu-id="d8855-146">Step consumption is used to calculate constant consumption in quantity intervals.</span></span> <span data-ttu-id="d8855-147">Выбрав **Потребление не шаге** в поле **Формула** на вкладке **Настройка**, вы можете добавить информацию о шагах на вкладке **Потребление на шаге**. Фиксированное потребляемое количество можно настроить в интервалах произведенного количества.</span><span class="sxs-lookup"><span data-stu-id="d8855-147">If you select **Step consumption** in the **Formula** field on the **Setup** tab, you can add information about the steps on the **Step consumption** tab. The fixed consumed quantity can be set up in intervals of the produced quantity.</span></span> <span data-ttu-id="d8855-148">Например, потребление на шаге настроено, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d8855-148">For example, step consumption is set up as shown in the following table.</span></span>

| <span data-ttu-id="d8855-149">Из серии</span><span class="sxs-lookup"><span data-stu-id="d8855-149">From series</span></span> | <span data-ttu-id="d8855-150">Количество</span><span class="sxs-lookup"><span data-stu-id="d8855-150">Quantity</span></span> |
|-------------|----------|
| <span data-ttu-id="d8855-151">0,00</span><span class="sxs-lookup"><span data-stu-id="d8855-151">0.00</span></span>        | <span data-ttu-id="d8855-152">10,0000</span><span class="sxs-lookup"><span data-stu-id="d8855-152">10.0000</span></span>  |
| <span data-ttu-id="d8855-153">100,00</span><span class="sxs-lookup"><span data-stu-id="d8855-153">100.00</span></span>      | <span data-ttu-id="d8855-154">20,0000</span><span class="sxs-lookup"><span data-stu-id="d8855-154">20.0000</span></span>  |
| <span data-ttu-id="d8855-155">200,00</span><span class="sxs-lookup"><span data-stu-id="d8855-155">200.00</span></span>      | <span data-ttu-id="d8855-156">40,0000</span><span class="sxs-lookup"><span data-stu-id="d8855-156">40.0000</span></span>  |

<span data-ttu-id="d8855-157">Количество в спецификации равно 1, и произведенное количество равно 110.</span><span class="sxs-lookup"><span data-stu-id="d8855-157">The bill of materials (BOM) quantity is 1, and the production quantity is 110.</span></span> <span data-ttu-id="d8855-158">Формула для затрат имеет вид: Из серии (количество) = Потребление.</span><span class="sxs-lookup"><span data-stu-id="d8855-158">The formula for the consumption is From series (Quantity) = Consumption.</span></span> <span data-ttu-id="d8855-159">Поскольку количество продукции равно 110, оно попадает в интервал "Из серии 100".</span><span class="sxs-lookup"><span data-stu-id="d8855-159">Because the production quantity is 110, it falls into the "From 100 series."</span></span> <span data-ttu-id="d8855-160">Поэтому количество равно 20.</span><span class="sxs-lookup"><span data-stu-id="d8855-160">Therefore, the quantity is 20.</span></span>



