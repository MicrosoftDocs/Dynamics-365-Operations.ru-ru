---
title: Методы расчета налога в поле "Основание"
description: В этой статье описываются параметры в поле "Источник" на странице налоговых кодов, а также порядок расчета налога на основе выбранного параметра для налогового кода.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1473eeb2950296f5ae6250d7a53794af3d9cba81
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "330686"
---
# <a name="sales-tax-calculation-methods-in-the-origin-field"></a><span data-ttu-id="0716b-103">Методы расчета налога в поле "Основание"</span><span class="sxs-lookup"><span data-stu-id="0716b-103">Sales tax calculation methods in the Origin field</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="0716b-104">В этой статье описываются параметры в поле "Источник" на странице налоговых кодов, а также порядок расчета налога на основе выбранного параметра для налогового кода.</span><span class="sxs-lookup"><span data-stu-id="0716b-104">This article explains the options in the Origin field on the sales tax codes page and how sales tax is calculated based on the selected option for a sales tax code.</span></span>

<span data-ttu-id="0716b-105">Для каждого из налоговых кодов, создаваемых на странице "Налоговые коды", необходимо указать метод расчета для базовой суммы налога в поле "Основание".</span><span class="sxs-lookup"><span data-stu-id="0716b-105">For each sales tax code that you create in the Sales tax codes page, you must select the method of calculation to apply to the tax base amount in the Origin field.</span></span>

## <a name="percentage-of-net-amount"></a><span data-ttu-id="0716b-106">Процент от чистой суммы</span><span class="sxs-lookup"><span data-stu-id="0716b-106">Percentage of net amount</span></span>
<span data-ttu-id="0716b-107">Метод расчета процента от чистой суммы — это значение по умолчанию в поле "Основание".</span><span class="sxs-lookup"><span data-stu-id="0716b-107">The Percentage of net amount calculation method is the default value in the Origin field.</span></span> <span data-ttu-id="0716b-108">Этот налог рассчитывается как процент от суммы покупки или суммы продаж за вычетом всех остальных налогов.</span><span class="sxs-lookup"><span data-stu-id="0716b-108">The sales tax is calculated as a percentage of the purchase or sales amount, excluding any other sales taxes.</span></span>
### <a name="example"></a><span data-ttu-id="0716b-109">Пример</span><span class="sxs-lookup"><span data-stu-id="0716b-109">Example</span></span>

<span data-ttu-id="0716b-110">Ставка налога = 25%.</span><span class="sxs-lookup"><span data-stu-id="0716b-110">The tax rate is 25%.</span></span> <span data-ttu-id="0716b-111">В строке накладной количество равно 10 шт. по 1,00 каждая, и клиенту положена скидка 10%.</span><span class="sxs-lookup"><span data-stu-id="0716b-111">The invoice line shows a quantity of 10 items at 1.00 each, and the customer is allowed a 10% line discount.</span></span> <span data-ttu-id="0716b-112">Чистая сумма: (10 x 1,00) -10% = 9,00 Налог: 9,00 x 25% = 2,25 Общая сумма: 9,00 + 2,25 = 11,25</span><span class="sxs-lookup"><span data-stu-id="0716b-112">Net amount: (10 x 1.00) -10% = 9.00 Sales tax: 9.00 x 25% = 2.25 Total amount: 9.00 + 2.25 = 11.25</span></span>

## <a name="percentage-of-gross-amount"></a><span data-ttu-id="0716b-113">Процент от валовой суммы</span><span class="sxs-lookup"><span data-stu-id="0716b-113">Percentage of gross amount</span></span>
<span data-ttu-id="0716b-114">Если вы выбираете метод "Процент от валовой суммы", то налог рассчитывается как процент от валовой суммы продаж.</span><span class="sxs-lookup"><span data-stu-id="0716b-114">If you select the Percentage of gross amount method, the sales tax is calculated as a percentage of the gross sales amount.</span></span> <span data-ttu-id="0716b-115">Валовая суммы равна чистой сумме строки плюс все налоги и сборы для строки за исключением одного налога с "Основание" = "Процент от валовой суммы".</span><span class="sxs-lookup"><span data-stu-id="0716b-115">The gross amount is the line net amount plus all taxes and fees for the line except the one tax with Origin = Percentage of gross amount.</span></span>
### <a name="example"></a><span data-ttu-id="0716b-116">Пример</span><span class="sxs-lookup"><span data-stu-id="0716b-116">Example</span></span>

<span data-ttu-id="0716b-117">Налоговым органом введены особые пошлины по данной номенклатуре.</span><span class="sxs-lookup"><span data-stu-id="0716b-117">The tax authority has imposed special duties on an item.</span></span> <span data-ttu-id="0716b-118">Суммы пошлины добавляются к чистой сумме до расчета налога.</span><span class="sxs-lookup"><span data-stu-id="0716b-118">The duty amounts are added to the net amount before sales tax is calculated.</span></span> <span data-ttu-id="0716b-119">Если имеются следующие налоговые коды:</span><span class="sxs-lookup"><span data-stu-id="0716b-119">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="0716b-120">ПОШЛИНА 1 = 10% с использованием метода расчета процента от чистой суммы</span><span class="sxs-lookup"><span data-stu-id="0716b-120">DUTY 1 = 10%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="0716b-121">ПОШЛИНА 2 = 20% с использованием метода расчета процента от чистой суммы</span><span class="sxs-lookup"><span data-stu-id="0716b-121">DUTY 2 = 20%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="0716b-122">НАЛОГ С ПРОДАЖ = 25% с использованием метода расчета "Процент от валовой суммы"</span><span class="sxs-lookup"><span data-stu-id="0716b-122">SALESTAX = 25%, using the Percentage of gross amount calculation method</span></span>

<span data-ttu-id="0716b-123">Если чистая сумма составляет 10,00, то ПОШЛИНА 1 составляет 1,00 (10,00 x 10%), а ПОШЛИНА 2 составляет 2,00 (10,00 х 20%).</span><span class="sxs-lookup"><span data-stu-id="0716b-123">If the net amount is 10.00, then DUTY 1 is 1.00 (10.00 x 10%) and DUTY 2 = 2.00 (10.00 x 20%).</span></span> <span data-ttu-id="0716b-124">Суммы будут следующие: Валовая сумма: Чистая сумма + сумма ПОШЛИНА 1 + сумма ПОШЛИНА 2 (10,00 + 1,00 + 2,00) = 13,00 НАЛОГ С ПРОДАЖ = 13,00 x 25% = 3,25 Итого ПОШЛИНЫ и НАЛОГ С ПРОДАЖ: 1,00 + 2,00 + 3,25 = 6,25 Общая сумма: 10,00 + 6,25 = 16,25</span><span class="sxs-lookup"><span data-stu-id="0716b-124">The amounts would be as follows: Gross amount: Net amount + DUTY 1 amount + DUTY 2 amount (10.00 + 1.00 + 2.00) = 13.00 SALESTAX = 13.00 x 25% = 3.25 Total DUTIES and SALESTAX: 1.00 + 2.00 + 3.25 = 6.25 Total amount: 10.00 + 6.25 = 16.25</span></span>

| <span data-ttu-id="0716b-125">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="0716b-125">**Note**</span></span>                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0716b-126">Только один код налога с "Основание" = "Процент от валовой суммы" может использоваться для проводки.</span><span class="sxs-lookup"><span data-stu-id="0716b-126">Only one tax code with Origin = Percentage of gross amount can be used for a transaction.</span></span> <span data-ttu-id="0716b-127">Если для проводки определено более одного такого кода налога, отображается ошибка с предупреждением о невозможности расчета налога.</span><span class="sxs-lookup"><span data-stu-id="0716b-127">If more than one such tax code is determined for a transaction an error will be displayed that sales tax cannot be calculated.</span></span> |


<a name="percentage-of-sales-tax"></a><span data-ttu-id="0716b-128">Процент от другого налога</span><span class="sxs-lookup"><span data-stu-id="0716b-128">Percentage of sales tax</span></span>
-----------------------

<span data-ttu-id="0716b-129">При выборе в поле "Основание" значения "Процент от другого налога" налог рассчитывается как процент налога, выбранного в поле "Налог на налог".</span><span class="sxs-lookup"><span data-stu-id="0716b-129">When you select Percentage of sales tax in the Origin field, sales tax is calculated as a percentage of the sales tax that is selected in the Sales tax on sales tax field.</span></span> <span data-ttu-id="0716b-130">Расчет налога, выбранного в поле "Налог на налог", выполняется в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="0716b-130">The sales tax that is selected in the Sales tax on sales tax field is calculated first.</span></span> <span data-ttu-id="0716b-131">Затем на основании суммы первого налога рассчитывается второй налог.</span><span class="sxs-lookup"><span data-stu-id="0716b-131">The second sales tax is then calculated based on the first sales tax amount.</span></span>
### <a name="example"></a><span data-ttu-id="0716b-132">Пример</span><span class="sxs-lookup"><span data-stu-id="0716b-132">Example</span></span>

<span data-ttu-id="0716b-133">Если имеются следующие налоговые коды:</span><span class="sxs-lookup"><span data-stu-id="0716b-133">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="0716b-134">ПОШЛИНА 1 = 10% с использованием метода расчета процента от чистой суммы</span><span class="sxs-lookup"><span data-stu-id="0716b-134">DUTY 1 = 10%, using the Percentage of net amount method</span></span>
-   <span data-ttu-id="0716b-135">ПОШЛИНА 2 = 20% с использованием метода "Процент от другого налога", когда в поле "Налог на налог" указано значение Пошлина 1</span><span class="sxs-lookup"><span data-stu-id="0716b-135">DUTY 2 = 20%, using the Percentage of sales tax method, with Duty 1 in the Sales tax on sales tax field</span></span>
-   <span data-ttu-id="0716b-136">НАЛОГ С ПРОДАЖ = 25% с использованием метода "Процент от валовой суммы"</span><span class="sxs-lookup"><span data-stu-id="0716b-136">SALESTAX = 25%, using the Percentage of gross amount method</span></span>

<span data-ttu-id="0716b-137">Чистая сумма: 10,00 ПОШЛИНА 1: 10,00 x 10% = 1,00 ПОШЛИНА 2: 1,00 x 20% = 0,20 Валовая сумма: 10,00 + 1,00 + 0,20 = 11,20 НАЛОГ С ПРОДАЖ: 11,20 x 25% = 2,80 Итого ПОШЛИНЫ и НАЛОГ С ПРОДАЖ: 1,00 + 0,20 + 2,80 = 4,00 Общая сумма: 10,00 + 4,00 = 14,00</span><span class="sxs-lookup"><span data-stu-id="0716b-137">Net amount: 10.00 DUTY 1: 10.00 x 10% = 1.00 DUTY 2: 1.00 x 20% = 0.20 Gross amount: 10.00 + 1.00 + 0.20 = 11.20 SALESTAX: 11.20 x 25% = 2.80 Total DUTIES and SALESTAX: 1.00 + 0.20 + 2.80 = 4.00 Total amount: 10.00 + 4.00 = 14.00</span></span>

| <span data-ttu-id="0716b-138">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="0716b-138">**Note**</span></span>                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0716b-139">Расчеты многоуровневых налогов на налоги невозможны.</span><span class="sxs-lookup"><span data-stu-id="0716b-139">Multilevel tax on tax calculations are not possible.</span></span> <span data-ttu-id="0716b-140">Налог нельзя рассчитать на основе налога, который уже рассчитан на основе другого налога.</span><span class="sxs-lookup"><span data-stu-id="0716b-140">A tax cannot be calculated based on a tax which already is calculated based on another tax.</span></span> <span data-ttu-id="0716b-141">Несколько одноуровневых кодов налогов на налоги можно рассчитать в одной проводке.</span><span class="sxs-lookup"><span data-stu-id="0716b-141">Multiple single level tax on tax codes can be calculated on a transaction.</span></span> |

## <a name="amount-per-unit"></a><span data-ttu-id="0716b-142">Сумма на единицу</span><span class="sxs-lookup"><span data-stu-id="0716b-142">Amount per unit</span></span>
<span data-ttu-id="0716b-143">Когда вы выбираете метод "Сумма на единицу" в поле "Основание", налог рассчитывается как фиксированная сумма на единицу умноженная на количество, введенное в строку документа.</span><span class="sxs-lookup"><span data-stu-id="0716b-143">When you select Amount per unit in the Origin field, sales tax is calculated as a fixed amount per unit multiplied with the quantity entered on the document line.</span></span> <span data-ttu-id="0716b-144">Единица измерения выбирается в поле "Единица измерения".</span><span class="sxs-lookup"><span data-stu-id="0716b-144">A unit has to be selected in the Unit field.</span></span> <span data-ttu-id="0716b-145">Сумма на единицу указывается на странице "Значения налогового кода".</span><span class="sxs-lookup"><span data-stu-id="0716b-145">The amount per unit is specified in the Sales tax code values page.</span></span>
### <a name="example"></a><span data-ttu-id="0716b-146">Пример</span><span class="sxs-lookup"><span data-stu-id="0716b-146">Example</span></span>

<span data-ttu-id="0716b-147">Код налога настраивается следующим образом: USD 1,20 на единицу = коробка. В строке накладной заказа на продажу продано 25 коробок номенклатуры. Налог рассчитывается как 25 x 1,20 = 30,00</span><span class="sxs-lookup"><span data-stu-id="0716b-147">Sales tax code is set up as: USD 1.20 per unit = box On a sales invoice line 25 boxes of an item are sold Sales tax is calculated as 25 x 1.20 = 30.00</span></span>

| <span data-ttu-id="0716b-148">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="0716b-148">**Note**</span></span>                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0716b-149">Если проводка введена в других единицах, чем единицы, определенные в коде налога на продажу, то они автоматически преобразуются на основе преобразований единиц измерения, настроенных на странице "Пересчеты единиц измерения".</span><span class="sxs-lookup"><span data-stu-id="0716b-149">If the transaction is entered in different unit than the unit specified on the sales tax code, it is converted automatically based on the unit conversions that are set up in the Unit conversions page.</span></span> |

###  <a name="amount-per-unit-additional-option"></a><span data-ttu-id="0716b-150">Метод "Сумма на единицу": дополнительные возможности</span><span class="sxs-lookup"><span data-stu-id="0716b-150">Amount per unit, additional option</span></span>

<span data-ttu-id="0716b-151">На вкладке "Расчет" вы можете выбрать, будет ли налог с расчетом на единицу рассчитываться до других налоговых кодов и добавляться к чистой сумме до расчета других налоговых кодов с "Основание" = "Процент от чистой суммы".</span><span class="sxs-lookup"><span data-stu-id="0716b-151">On the Calculation tab, you can select whether an amount per unit calculated tax is calculated before other tax codes and added to the net amount before other tax codes with Origin = Percentage of net amount are calculated.</span></span>

### <a name="examples"></a><span data-ttu-id="0716b-152">Примеры</span><span class="sxs-lookup"><span data-stu-id="0716b-152">Examples</span></span>

<span data-ttu-id="0716b-153">Предположим, что для проводки рассчитываются 2 налоговых кода:</span><span class="sxs-lookup"><span data-stu-id="0716b-153">Assume we calculate 2 tax codes on a transaction:</span></span>

-   <span data-ttu-id="0716b-154">ПОШЛИНА: "Основание" = "Сумма на единицу" и налог, значение установлено 5,00 на единицу = шт.</span><span class="sxs-lookup"><span data-stu-id="0716b-154">DUTY: Origin = Amount per unit and a sales tax, the value is set to 5.00 per unit = pcs</span></span>
-   <span data-ttu-id="0716b-155">НАЛОГ С ПРОДАЖ: "Основание" = как показано в примерах ниже, значение установлено равным 25%</span><span class="sxs-lookup"><span data-stu-id="0716b-155">SALESTAX: Origin = as shown in the examples below, the value is set to 25%</span></span>

<span data-ttu-id="0716b-156">Мы продаем 1 единицу номенклатуры в ценой единицы 10,00</span><span class="sxs-lookup"><span data-stu-id="0716b-156">We sell 1 piece of an item at a unit price of 10.00</span></span>
#### <a name="example-1"></a><span data-ttu-id="0716b-157">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0716b-157">Example 1</span></span>

<span data-ttu-id="0716b-158">НАЛОГ С ПРОДАЖ: "Основание" = метод "Процент от валовой суммы". Параметр "Расчет сборов до расчета налогов" не действует, так как НАЛОГ С ПРОДАЖ рассчитывается как процент от валовой суммы.</span><span class="sxs-lookup"><span data-stu-id="0716b-158">SALESTAX: Origin = Percentage of gross amount method The Calculate before sales tax option has no effect, because SALESTAX is calculated as a percentage of the gross amount.</span></span> <span data-ttu-id="0716b-159">ПОШЛИНА: 1 x 5,00 = 5,00 Валовая сумма: 10,00 + 5,00 = 15,00 НАЛОГ С ПРОДАЖ: 15,00 x 25% = 3,75 Всего налог: 5,00 + 3,75 = 8,75 Общая сумма: 10,00 + 8,75 = 18,75</span><span class="sxs-lookup"><span data-stu-id="0716b-159">DUTY: 1 x 5.00 = 5.00 Gross amount: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-2"></a><span data-ttu-id="0716b-160">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0716b-160">Example 2</span></span>

<span data-ttu-id="0716b-161">НАЛОГ С ПРОДАЖ: "Основание" = "Процент от чистой суммы" Параметр "Расчет сборов до расчета налогов" не выбран для расчета ПОШЛИНЫ.</span><span class="sxs-lookup"><span data-stu-id="0716b-161">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is not selected for the DUTY calculation.</span></span> <span data-ttu-id="0716b-162">Чистая сумма: 10,00 ПОШЛИНА: 1 x 5,00 = 5,00 НАЛОГ С ПРОДАЖ: 10,00 x 25% = 2,50 Всего налог: 5,00 + 2,50 = 7,50 Общая сумма: 10,00 + 7,50 = 17,50</span><span class="sxs-lookup"><span data-stu-id="0716b-162">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: 10.00 x 25% = 2.50 Total sales tax: 5.00 + 2.50 = 7.50 Total amount: 10.00 + 7.50 = 17.50</span></span>

#### <a name="example-3"></a><span data-ttu-id="0716b-163">Пример 3</span><span class="sxs-lookup"><span data-stu-id="0716b-163">Example 3</span></span>

<span data-ttu-id="0716b-164">НАЛОГ С ПРОДАЖ: "Основание" = "Процент от чистой суммы" Параметр "Расчет сборов до расчета налогов" выбран для расчета ПОШЛИНЫ.</span><span class="sxs-lookup"><span data-stu-id="0716b-164">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is selected for the DUTY calculation.</span></span> <span data-ttu-id="0716b-165">Чистая сумма: 10,00 ПОШЛИНА: 1 x 5,00 = 5,00 НАЛОГ С ПРОДАЖ: (10,00 + 5,00) x 25% = 3,75 Всего налог: 5,00 + 3,75 = 8,75 Общая сумма: 10,00 + 8,75 = 18,75</span><span class="sxs-lookup"><span data-stu-id="0716b-165">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: (10.00 + 5.00) x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-4"></a><span data-ttu-id="0716b-166">Пример 4</span><span class="sxs-lookup"><span data-stu-id="0716b-166">Example 4</span></span>

<span data-ttu-id="0716b-167">Результаты Примеров 3 и 1 одинаковы, так как существует только одна пошлина.</span><span class="sxs-lookup"><span data-stu-id="0716b-167">The result of Example 3 and Example 1 is the same, because there is only one duty.</span></span> <span data-ttu-id="0716b-168">Предположим, что имеются две ПОШЛИНЫ, и только одна из них включена в чистую сумму для расчета налога: ПОШЛИНА 1: 5,00, с использованием метода "Сумма на единицу", и выбран параметр "Расчет сборов до расчета налогов" ПОШЛИНА 2: 2,50, с использованием метода "Сумма на единицу", и параметр "Расчет сборов до расчета налогов" не выбран Налог: 25%, с использованием метода "Процент от чистой суммы" Чистая сумма: 10,00 ПОШЛИНА 1: 1 x 5,00 = 5,00 ПОШЛИНА 2: 1 x 2,50 = 2,50 Чистая сумма для налога с продаж: 10,00 + 5,00 = 15,00 НАЛОГ С ПРОДАЖ: 15,00 x 25% = 3,75 Итого налоги с продаж, включая пошлины: 5,00 + 2,50 + 3,75 = 11,25 Общая сумма: 10,00 + 11,25 = 21,25 НАЛОГ С ПРОДАЖ 25% рассчитывается для суммы чистой суммы (10,00) + ПОШЛИНА 1 (5,00) = 15,00.</span><span class="sxs-lookup"><span data-stu-id="0716b-168">Assume that you have two DUTIES, and only one of them is included in the net amount for the sales tax calculation: DUTY 1: 5.00, using the Amount per unit method, and the Calculate before sales tax option is selected DUTY 2: 2.50, using the Amount per unit method, and the Calculate before sales tax option is not selected Sales tax: 25%, using the Percentage of net amount method Net amount: 10.00 DUTY 1: 1 x 5.00 = 5.00 DUTY 2: 1 x 2.50 = 2.50 Net amount subject to sales tax: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales taxes, including duties: 5.00 + 2.50 + 3.75 = 11.25 Total amount: 10.00 + 11.25 = 21.25 The 25% SALESTAX is calculated for the sum of the net amount (10.00) + DUTY 1 (5.00) = 15.00.</span></span> <span data-ttu-id="0716b-169">ПОШЛИНА 2 будет добавлена к сумме налога после расчета налога с продаж.</span><span class="sxs-lookup"><span data-stu-id="0716b-169">DUTY 2 is added to the tax amount after the sales tax is calculated.</span></span>

## <a name="calculated-percentage-of-net-amount"></a><span data-ttu-id="0716b-170">Рассчитанный процент чистой суммы</span><span class="sxs-lookup"><span data-stu-id="0716b-170">Calculated percentage of net amount</span></span>
<span data-ttu-id="0716b-171">Расчет налога методом "Рассчитанный процент чистой суммы" производится по-разному в зависимости от настройки параметра "Суммы включают налог" для документа или журнала.</span><span class="sxs-lookup"><span data-stu-id="0716b-171">The Calculated percentage of net amount handles tax calculation differently depending on the setting of the Amounts include sales tax parameter for the document or journal.</span></span>
### <a name="example-1"></a><span data-ttu-id="0716b-172">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0716b-172">Example 1</span></span>

<span data-ttu-id="0716b-173">Для документа или журнала задано значение "Суммы включают налог" = "Да" Сумма в строке проводки: 10,00 Ставка налога: 25% Налог с продаж: Сумма в строке проводки x Ставка налога (10,00 x 25%) = 2,50 Сумма налоговой базы (сумма основания): Сумма в строке проводки - Налог с продаж (10,00 - 2,50) = 7,50</span><span class="sxs-lookup"><span data-stu-id="0716b-173">Document / journal is set to Amounts include sales tax = Yes Transaction line amount: 10.00 Tax rate: 25% Sales tax: Transaction line amount x tax rate (10.00 x 25%) = 2.50 Tax base amount (origin amount): Transaction line amount - Sales tax (10.00 - 2.50) = 7.50</span></span>

### <a name="example-2"></a><span data-ttu-id="0716b-174">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0716b-174">Example 2</span></span>

<span data-ttu-id="0716b-175">Для документа или журнала задано значение "Суммы включают налог" = "Нет" Сумма в строке проводки: 10,00 Ставка налога: 25% Налог с продаж: (Сумма в строке проводки x Ставка налога)/(100 - Ставка налога) (10,00 x 25%)/(100% - 25%) = 3,33 Сумма налоговой базы (сумма основания): Сумма в строке проводки = 10,00</span><span class="sxs-lookup"><span data-stu-id="0716b-175">Document / journal is set to Amounts include sales tax = No Transaction line amount: 10.00 Tax rate: 25% Sales tax: (Transaction line amount x tax rate) / (100 - tax rate) (10.00 x 25%) / (100% - 25%) = 3.33 Tax base amount (origin amount): Transaction line amount = 10.00</span></span>



<a name="additional-resources"></a><span data-ttu-id="0716b-176">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0716b-176">Additional resources</span></span>
--------

[<span data-ttu-id="0716b-177">Определение ставок налога на основе полей "База маржинальной прибыли" и "Метода расчета"</span><span class="sxs-lookup"><span data-stu-id="0716b-177">Determining sale tax rates based on the Marginal base and Calculation method fields</span></span>](marginal-base-field.md)

[<span data-ttu-id="0716b-178">Параметры расчета "Полная сумма" и "Интервал" для налоговых кодов</span><span class="sxs-lookup"><span data-stu-id="0716b-178">Whole amount and Interval calculation options for sales tax codes</span></span>](whole-amount-interval-options-sales-tax-codes.md)



