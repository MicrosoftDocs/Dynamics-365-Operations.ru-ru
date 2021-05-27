---
title: Производительность при расчете налога влияет на проводки
description: В этой теме содержатся сведения об устранении неполадок, связанных с производительностью расчета налогов и его влиянием на проводки.
author: shtao
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 6fce4e2cb8c5507769533a875e23ccc4531abf51
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020147"
---
# <a name="tax-calculation-performance-affects-transactions"></a><span data-ttu-id="62659-103">Производительность при расчете налога влияет на проводки</span><span class="sxs-lookup"><span data-stu-id="62659-103">Tax calculation performance affects transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62659-104">Иногда на проводку влияют вопросы производительности, связанные с расчетом налога.</span><span class="sxs-lookup"><span data-stu-id="62659-104">Sometimes, a transaction is affected by performance issues that tax calculation is having.</span></span> <span data-ttu-id="62659-105">Для решения проблемы выполните действия, указанные в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="62659-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="review-the-transaction-line-count"></a><span data-ttu-id="62659-106">Просмотр количества строк проводок</span><span class="sxs-lookup"><span data-stu-id="62659-106">Review the transaction line count</span></span>

<span data-ttu-id="62659-107">Определите, есть ли у проводки большое количество строк (например, более нескольких сотен).</span><span class="sxs-lookup"><span data-stu-id="62659-107">Determine whether the transaction has a large number of lines (for example, more than several hundred).</span></span> <span data-ttu-id="62659-108">Если нет, перейдите к следующему разделу.</span><span class="sxs-lookup"><span data-stu-id="62659-108">If it doesn't, move on to the next section.</span></span> <span data-ttu-id="62659-109">Если проводка содержит несколько сотен строк, следует отложить расчет налога.</span><span class="sxs-lookup"><span data-stu-id="62659-109">If the transaction does have several hundred lines, delay the tax calculation.</span></span> <span data-ttu-id="62659-110">Дополнительные сведения см. в разделе [Включение отсроченного расчета налога для журналов](enable-delayed-tax-calculation.md).</span><span class="sxs-lookup"><span data-stu-id="62659-110">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span> 

<span data-ttu-id="62659-111">Затем можно определить, удовлетворяются ли какие-либо из следующих условий:</span><span class="sxs-lookup"><span data-stu-id="62659-111">Next, you can determine whether any of the following conditions are met:</span></span>

- <span data-ttu-id="62659-112">Имеются проводки импорта из больших файлов.</span><span class="sxs-lookup"><span data-stu-id="62659-112">There are import transactions from large files.</span></span>
- <span data-ttu-id="62659-113">Несколько сеансов обрабатывают один и тот же расчет налога на проводку одновременно.</span><span class="sxs-lookup"><span data-stu-id="62659-113">Multiple sessions process the same transaction tax calculation at the same time.</span></span>
- <span data-ttu-id="62659-114">Проводка имеет несколько строк, и представления обновляются в реальном времени.</span><span class="sxs-lookup"><span data-stu-id="62659-114">The transaction has multiple lines, and the views are updated in real time.</span></span> <span data-ttu-id="62659-115">Например, поле **Рассчитанная сумма налога** на странице **Общий журнал** обновляется в реальном времени при изменении полей строки.</span><span class="sxs-lookup"><span data-stu-id="62659-115">For example, the **Calculated sales tax amount** field on the **General journal** page is updated in real time when a line's fields are changed.</span></span>

   <span data-ttu-id="62659-116">[![Поле рассчитанной суммы налога на странице ваучера журнала](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="62659-116">[![Calculated sales tax amount field on the Jounal voucher page](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span></span>

<span data-ttu-id="62659-117">Если какое-либо из этих условий выполнено, отложите расчет налога.</span><span class="sxs-lookup"><span data-stu-id="62659-117">If any of these conditions are met, delay the tax calculation.</span></span>

## <a name="review-the-call-stack"></a><span data-ttu-id="62659-118">Проверка стека вызова</span><span class="sxs-lookup"><span data-stu-id="62659-118">Review the call stack</span></span>

<span data-ttu-id="62659-119">Проверьте стек вызовов, чтобы определить, вызывается ли расчет налога несколько раз.</span><span class="sxs-lookup"><span data-stu-id="62659-119">Review the call stack to determine whether tax calculation is called multiple times.</span></span> <span data-ttu-id="62659-120">Если нет, перейдите к следующему разделу.</span><span class="sxs-lookup"><span data-stu-id="62659-120">If it isn't, move on to the next section.</span></span> <span data-ttu-id="62659-121">Если стек вызова вызван несколько раз, выполните следующие действия, чтобы уменьшить время расчета налога.</span><span class="sxs-lookup"><span data-stu-id="62659-121">If the call stack is called multiple times, follow these steps to help reduce the tax calculation times.</span></span>

1. <span data-ttu-id="62659-122">Если журнал изучал проводку, задержите расчет налога.</span><span class="sxs-lookup"><span data-stu-id="62659-122">If the journal has considered the transaction, delay the tax calculation.</span></span> <span data-ttu-id="62659-123">Дополнительные сведения см. в разделе [Включение отсроченного расчета налога для журналов](enable-delayed-tax-calculation.md).</span><span class="sxs-lookup"><span data-stu-id="62659-123">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span>
2. <span data-ttu-id="62659-124">Если проводка является заказом на покупку, а версия приложения позже 10.0.15, можно отложить расчет налога до окончательного расчета путем включения фокус-тестирования для **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.</span><span class="sxs-lookup"><span data-stu-id="62659-124">If the transaction is a purchase order, and the application version is later than 10.0.15, you can delay the tax calculation until the final calculation by enabling the flighting for **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.</span></span>

## <a name="review-the-call-stack-timeline"></a><span data-ttu-id="62659-125">Проверка временной шкалы стека вызова</span><span class="sxs-lookup"><span data-stu-id="62659-125">Review the call stack timeline</span></span>

<span data-ttu-id="62659-126">Проверьте временную шкалу стека вызова, чтобы определить, имеются ли следующие проблемы.</span><span class="sxs-lookup"><span data-stu-id="62659-126">Review the call stack timeline to determine whether the following issues exist.</span></span> <span data-ttu-id="62659-127">Если они есть, включите фокус-тестирование рейс для **TaxUncommittedDoIsolateScopeFlighting**, чтобы устранить проблему.</span><span class="sxs-lookup"><span data-stu-id="62659-127">If they do, enable the flighting for **TaxUncommittedDoIsolateScopeFlighting** to fix the issue.</span></span>

- <span data-ttu-id="62659-128">Проводка приводит к тому, что система перестает отвечать на запросы до окончания сеанса.</span><span class="sxs-lookup"><span data-stu-id="62659-128">The transaction causes the system to stop responding until the session ends.</span></span> <span data-ttu-id="62659-129">Поэтому проводка не может рассчитать результат налога.</span><span class="sxs-lookup"><span data-stu-id="62659-129">Therefore, the transaction can't calculate the tax result.</span></span> <span data-ttu-id="62659-130">На следующем рисунке показано полученное окно сообщения "Сеанс завершен".</span><span class="sxs-lookup"><span data-stu-id="62659-130">The following illustration shows the "Session ended" message box that you receive.</span></span>

    <span data-ttu-id="62659-131">[![Сообщение о завершении сеанса](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="62659-131">[![Session ended message](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span></span>

- <span data-ttu-id="62659-132">Методы **TaxUncommitted** занимают больше времени, чем другие методы.</span><span class="sxs-lookup"><span data-stu-id="62659-132">The **TaxUncommitted** methods take more time than other methods.</span></span> <span data-ttu-id="62659-133">Например, на следующем рисунке метод **TaxUncommitted::updateTaxUncommitted()** занимает 43 347,42 секунды, но другие методы занимают 0,09 секунды.</span><span class="sxs-lookup"><span data-stu-id="62659-133">For example, in the following illustration, the **TaxUncommitted::updateTaxUncommitted()** method takes 43,347.42 seconds, but other methods take 0.09 seconds.</span></span>

    <span data-ttu-id="62659-134">[![Продолжительность метода](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="62659-134">[![Method durations](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span></span>

## <a name="customizing-and-calling-tax-calculation"></a><span data-ttu-id="62659-135">Настройка и вызов расчета налогов</span><span class="sxs-lookup"><span data-stu-id="62659-135">Customizing and calling tax calculation</span></span>

<span data-ttu-id="62659-136">При настройке не вызывайте расчет налогов метода **insert()** или **update()** для каждой строки.</span><span class="sxs-lookup"><span data-stu-id="62659-136">When you customize, don't call tax calculation at the **insert()** or **update()** method for each line.</span></span> <span data-ttu-id="62659-137">Расчет налога должен вызываться на уровне проводки.</span><span class="sxs-lookup"><span data-stu-id="62659-137">Tax calculation should be called at the transaction level.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="62659-138">Определение существования настройки</span><span class="sxs-lookup"><span data-stu-id="62659-138">Determine whether customization exists</span></span>

<span data-ttu-id="62659-139">Если вы выполнили шаги в предыдущих разделах, но не смогли решить проблему, определите, существует ли настройка.</span><span class="sxs-lookup"><span data-stu-id="62659-139">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="62659-140">Если настройки не существует, создайте запрос в службу поддержки Майкрософт для получения дополнительной поддержки.</span><span class="sxs-lookup"><span data-stu-id="62659-140">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
