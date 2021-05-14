---
title: Налог не рассчитан или сумма налога равна нулю
description: В этой теме содержатся сведения об устранении неполадок, которые могут помочь, когда сумма налога равна 0 (нулю) или налог не рассчитан.
author: shtao
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: ead979081692d4dcee9812c89f5f10c7879d3f7e
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947698"
---
# <a name="tax-isnt-calculated-or-the-tax-amount-is-zero"></a><span data-ttu-id="7d033-103">Налог не рассчитан или сумма налога равна нулю</span><span class="sxs-lookup"><span data-stu-id="7d033-103">Tax isn't calculated or the tax amount is zero</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d033-104">У проводки может быть сумма по строке, которая не равна 0 (нулю), но либо налог не рассчитан, либо рассчитанная сумма налога равна 0.</span><span class="sxs-lookup"><span data-stu-id="7d033-104">A transaction might have a line amount that isn't 0 (zero), but either tax isn't calculated or the calculated tax amount is 0.</span></span> <span data-ttu-id="7d033-105">Для решения проблемы выполните действия, указанные в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="7d033-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="verify-that-tax-codes-are-correctly-selected-by-the-transaction"></a><span data-ttu-id="7d033-106">Убедитесь, что коды налога правильно выбраны проводкой</span><span class="sxs-lookup"><span data-stu-id="7d033-106">Verify that tax codes are correctly selected by the transaction</span></span>

<span data-ttu-id="7d033-107">Если проводка не выбирает правильные налоговые коды или если не выбран ни один налоговый код, то налоги для нее рассчитываться не будут.</span><span class="sxs-lookup"><span data-stu-id="7d033-107">If the transaction doesn't select the correct tax codes, or if it doesn't select any tax codes, taxes won't be calculated on it.</span></span> <span data-ttu-id="7d033-108">Выполните следующие действия, чтобы убедиться, что коды налога правильно выбраны проводкой.</span><span class="sxs-lookup"><span data-stu-id="7d033-108">Follow these steps to verify that tax codes are correctly selected by the transaction.</span></span> 

1. <span data-ttu-id="7d033-109">В строке проводки на экспресс-вкладке **Сведения строки** на вкладке **Настройка** в разделе **Налог** убедитесь, что выбраны правильные налоговые группы в полях **Налоговая группа номенклатур** и **Налоговая группа**.</span><span class="sxs-lookup"><span data-stu-id="7d033-109">On the transaction line, on the **Line details** FastTab, on the **Setup** tab, in the **Sales tax** section, verify that the correct tax groups are selected in the **Item sales tax group** and **Sales tax group** fields.</span></span> <span data-ttu-id="7d033-110">Если правильные налоговые группы не выбраны, выберите их.</span><span class="sxs-lookup"><span data-stu-id="7d033-110">If the correct tax groups aren't selected, select them.</span></span>

    <span data-ttu-id="7d033-111">[![поля "Налоговая группа номенклатур" и "Налоговая группа"](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="7d033-111">[![Item sales tax group and Sales tax group fields](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span></span>

2. <span data-ttu-id="7d033-112">Перейдите в раздел **Налог** \> **Косвенные налоги** \> **Налог** \> **Налоговые группы**.</span><span class="sxs-lookup"><span data-stu-id="7d033-112">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
3. <span data-ttu-id="7d033-113">Выберите подходящую налоговую группу, а затем на экспресс-вкладке **Настройка** запишите налоговый код в поле **Налоговый код**.</span><span class="sxs-lookup"><span data-stu-id="7d033-113">Select the appropriate sales tax group, and then, on the **Setup** FastTab, make a note of the tax code in the **Sales tax code** field.</span></span>

    <span data-ttu-id="7d033-114">[![Страница налоговых групп](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="7d033-114">[![Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span></span>

4. <span data-ttu-id="7d033-115">Перейдите в раздел **Налог** \> **Косвенные налоги** \> **Налог** \> **Налоговые группы номенклатур**.</span><span class="sxs-lookup"><span data-stu-id="7d033-115">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Item sales tax groups**.</span></span>
5. <span data-ttu-id="7d033-116">Выберите подходящую налоговую группу номенклатур, а затем на экспресс-вкладке **Настройка** убедитесь, что налоговый код в поле **Налоговый код** совпадает с налоговым кодом налоговой группы.</span><span class="sxs-lookup"><span data-stu-id="7d033-116">Select the appropriate item sales tax group, and then, on the **Setup** FastTab, verify that the tax code in the **Sales tax code** field matches the tax code of the sales tax group.</span></span>

    <span data-ttu-id="7d033-117">[![Страница налоговых групп номенклатур](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="7d033-117">[![Item sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span></span>

6. <span data-ttu-id="7d033-118">Если налоговые коды не совпадают, обновите налоговый код для одной из групп.</span><span class="sxs-lookup"><span data-stu-id="7d033-118">If the tax codes don't match, update the sales tax code for one of the groups.</span></span>

## <a name="verify-that-the-selected-tax-codes-arent-exempt-and-that-they-have-the-correct-tax-rate-value"></a><span data-ttu-id="7d033-119">Убедитесь, что выбранные налоговые коды не исключаются и что у них правильное значение ставки налога</span><span class="sxs-lookup"><span data-stu-id="7d033-119">Verify that the selected tax codes aren't exempt and that they have the correct tax rate value</span></span>

<span data-ttu-id="7d033-120">Если налоговые коды освобождены или если налоговая ставка равна 0 (нулю), результат расчета налога будет равен 0.</span><span class="sxs-lookup"><span data-stu-id="7d033-120">If the tax codes are exempt, or if the tax rate is 0 (zero), the tax calculation result will be 0.</span></span> <span data-ttu-id="7d033-121">Выполните следующие действия, чтобы определить, освобождаются ли выбранные налоговые коды, и убедитесь, что к ним применяется правильная налоговая ставка.</span><span class="sxs-lookup"><span data-stu-id="7d033-121">Follow these steps to determine whether the selected tax codes are exempt and to verify that the correct tax rate is applied to them.</span></span>

1. <span data-ttu-id="7d033-122">Перейдите в раздел **Налог** \> **Косвенные налоги** \> **Налог** \> **Налоговые группы**.</span><span class="sxs-lookup"><span data-stu-id="7d033-122">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
2. <span data-ttu-id="7d033-123">Выберите подходящую налоговую группу, а затем на экспресс-вкладке **Настройка** убедитесь, что флажок **Освобождается** снят.</span><span class="sxs-lookup"><span data-stu-id="7d033-123">Select the appropriate sales tax group, and then, on the **Setup** FastTab, verify that the **Exempt** check box is cleared.</span></span> <span data-ttu-id="7d033-124">Если этот флажок установлен, снимите его.</span><span class="sxs-lookup"><span data-stu-id="7d033-124">If it's selected, clear it.</span></span>

    <span data-ttu-id="7d033-125">[![Флажок "Освобождается" на странице налоговых групп](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="7d033-125">[![Exempt check box on the Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span></span>

3. <span data-ttu-id="7d033-126">Перейдите в раздел **Налог** \> **Косвенные налоги** \> **Налог** \> **Налоговые коды**.</span><span class="sxs-lookup"><span data-stu-id="7d033-126">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="7d033-127">Выберите соответствующий налоговый код, а затем убедитесь, что значение ставки налога в поле **Значение** не равно 0 (нулю).</span><span class="sxs-lookup"><span data-stu-id="7d033-127">Select the appropriate sales tax code, and then verify that the tax rate value in the **Value** field isn't 0 (zero).</span></span> <span data-ttu-id="7d033-128">Если равно 0, обновите поле так, чтобы оно было настроено на правильную налоговую ставку.</span><span class="sxs-lookup"><span data-stu-id="7d033-128">If it's 0, update the field so that it's set to the correct tax rate.</span></span>

    <span data-ttu-id="7d033-129">[![Поле значения на странице значений налогового кода](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="7d033-129">[![Value field on the Sales tax code values page](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span></span>

## <a name="determine-whether-zero-is-the-correct-tax-amount"></a><span data-ttu-id="7d033-130">Определите, является ли ноль правильной суммой налога</span><span class="sxs-lookup"><span data-stu-id="7d033-130">Determine whether zero is the correct tax amount</span></span>

<span data-ttu-id="7d033-131">В некоторых сценариях сумма налога 0 (ноль) верна.</span><span class="sxs-lookup"><span data-stu-id="7d033-131">In some scenarios, a tax amount of 0 (zero) is correct.</span></span> <span data-ttu-id="7d033-132">Выполните следующие действия, чтобы определить, является ли сумма налога как 0 для проводки правильным значением.</span><span class="sxs-lookup"><span data-stu-id="7d033-132">Follow these steps to determine whether 0 is the correct tax amount for your transaction.</span></span>

1. <span data-ttu-id="7d033-133">Перейдите в раздел **Главная книга** \> **Настройка главной книги** \> **Параметры главной книги**.</span><span class="sxs-lookup"><span data-stu-id="7d033-133">Go to **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span>
2. <span data-ttu-id="7d033-134">На вкладке **Налог** в поле **Метод расчета** убедитесь, что выбрано **Итого**.</span><span class="sxs-lookup"><span data-stu-id="7d033-134">On the **Sales tax** tab, in the **Calculation method** field, verify that **Total** is selected.</span></span>

    <span data-ttu-id="7d033-135">[![Поле метода расчета на странице параметров главной книги](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="7d033-135">[![Calculation method field on the General ledger parameters page](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span></span>

3. <span data-ttu-id="7d033-136">Перейдите в раздел **Налог** \> **Косвенные налоги** \> **Налог** \> **Налоговые коды**.</span><span class="sxs-lookup"><span data-stu-id="7d033-136">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="7d033-137">Выберите соответствующий налоговый код, выберите **Расчет** \> **База маржинальной прибыли** и убедитесь, что база маржинальной прибыли задана как **Чистая сумма сальдо по накладной** или **Общая сумма накладной, включая все прочие налоги**.</span><span class="sxs-lookup"><span data-stu-id="7d033-137">Select the appropriate sales tax code, select **Calculation** \> **Marginal base**, and verify that the marginal base is set to **Net amount of invoice balance** or **Invoice total incl. other sales tax amounts**.</span></span> <span data-ttu-id="7d033-138">Дополнительные сведения см. в разделе [Общая сумма накладной, включая все прочие налоги](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).</span><span class="sxs-lookup"><span data-stu-id="7d033-138">For more information, see the [Invoice total incl. other sales tax amounts](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).</span></span>
5. <span data-ttu-id="7d033-139">Если правильные значения заданы на шагах 2 и 4, определите, является ли общая сумма проводки нулевой (0).</span><span class="sxs-lookup"><span data-stu-id="7d033-139">If the correct values are set in steps 2 and 4, determine whether the total amount of the transaction is 0 (zero).</span></span> <span data-ttu-id="7d033-140">Если итоговая сумма равна 0, то ожидаемым результатом будет сумма налога 0.</span><span class="sxs-lookup"><span data-stu-id="7d033-140">If the total amount is 0, a tax amount of 0 is the expected result.</span></span> <span data-ttu-id="7d033-141">Поскольку расчет налога основан на итоговой сумме сальдо по накладной и эта сумма не находится "строка за строкой", сумма налога, равная 0, будет распределяться по каждой строке после расчета налога.</span><span class="sxs-lookup"><span data-stu-id="7d033-141">Because the tax calculation is based on the total amount of the invoice balance, and that amount isn't line by line, the tax amount of 0 will be allocated to each line after the tax calculation.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="7d033-142">Определение существования настройки</span><span class="sxs-lookup"><span data-stu-id="7d033-142">Determine whether customization exists</span></span>

<span data-ttu-id="7d033-143">Если вы выполнили шаги в предыдущих разделах, но не смогли решить проблему, определите, существует ли настройка.</span><span class="sxs-lookup"><span data-stu-id="7d033-143">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="7d033-144">Если настройки не существует, создайте запрос в службу поддержки Майкрософт для получения дополнительной поддержки.</span><span class="sxs-lookup"><span data-stu-id="7d033-144">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
