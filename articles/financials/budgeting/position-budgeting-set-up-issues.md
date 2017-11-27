---
title: "Устранение неполадок бюджетирования должностей"
description: "Эта статься содержит ответы на вопросы, которые могут возникнуть при настройке бюджетирования должностей. Он включает часто задаваемые вопросы о создании элементов бюджетных затрат, групп компенсации и сеток компенсации."
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmBudgetPurposeType, HcmPositionForecast
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 88253
ms.assetid: c44df01b-8700-4022-b4c6-c4b1cb84d31d
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f2ef04008a5e6339a2193f9fcc77f2e0e6643557
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="position-budgeting-troubleshooting"></a><span data-ttu-id="d4a95-104">Устранение неполадок бюджетирования должностей</span><span class="sxs-lookup"><span data-stu-id="d4a95-104">Position budgeting troubleshooting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d4a95-105">Эта статься содержит ответы на вопросы, которые могут возникнуть при настройке бюджетирования должностей.</span><span class="sxs-lookup"><span data-stu-id="d4a95-105">This article provides answers to questions that you might have when you configure position budgeting.</span></span> <span data-ttu-id="d4a95-106">Он включает часто задаваемые вопросы о создании элементов бюджетных затрат, групп компенсации и сеток компенсации.</span><span class="sxs-lookup"><span data-stu-id="d4a95-106">It addresses frequently asked questions about how to create budget cost elements, compensation groups, and compensation grids.</span></span> 

<a name="why-cant-i-find-the-forecast-position-page-in-human-resources"></a><span data-ttu-id="d4a95-107">Почему я не могу найти страницу прогнозируемой должности в модуле "Управление персоналом"?</span><span class="sxs-lookup"><span data-stu-id="d4a95-107">Why can’t I find the forecast position page in Human resources?</span></span>
---------------------------------------------------------------

<span data-ttu-id="d4a95-108">Прогнозируемые должности перенесены в модуль "Бюджетирование".</span><span class="sxs-lookup"><span data-stu-id="d4a95-108">Forecast positions have been moved to Budgeting.</span></span>

## <a name="why-cant-i-delete-a-budget-cost-element"></a><span data-ttu-id="d4a95-109">Почему я не могу удалить элемент бюджетных затрат?</span><span class="sxs-lookup"><span data-stu-id="d4a95-109">Why can’t I delete a budget cost element?</span></span>
<span data-ttu-id="d4a95-110">Невозможно удалить элемент бюджетных затрат, который назначен прогнозируемой должности.</span><span class="sxs-lookup"><span data-stu-id="d4a95-110">You can’t delete a budget cost element that is assigned to a forecast position.</span></span> <span data-ttu-id="d4a95-111">Чтобы можно было удалить элемент бюджетных затрат, необходимо сначала удалить его из всех прогнозируемых должностей.</span><span class="sxs-lookup"><span data-stu-id="d4a95-111">Before you can delete a budget cost element, you must remove it from all forecast positions.</span></span> <span data-ttu-id="d4a95-112">**Совет.** Для обнаружения всех должностей, которым назначен этот элемент бюджетных затрат, выберите элемент затрат на странице **Элементы бюджетных затрат**, затем нажмите **Обновить должности**.</span><span class="sxs-lookup"><span data-stu-id="d4a95-112">**Tip:** To find all the positions that a budget cost element is assigned to, select the cost element on the **Budget cost elements** page, and then click **Update positions**.</span></span> <span data-ttu-id="d4a95-113">Должности, которые используют элемент затрат, перечислены в верхней сетке.</span><span class="sxs-lookup"><span data-stu-id="d4a95-113">The positions that use the cost element are listed in the upper grid.</span></span>

## <a name="how-can-i-remove-a-cost-element-from-multiple-forecast-positions-without-opening-each-one"></a><span data-ttu-id="d4a95-114">Как можно удалить элемент затрат из нескольких прогнозируемых должностей, не открывая каждую должность?</span><span class="sxs-lookup"><span data-stu-id="d4a95-114">How can I remove a cost element from multiple forecast positions without opening each one?</span></span>
<span data-ttu-id="d4a95-115">Невозможно удалить элемент затрат.</span><span class="sxs-lookup"><span data-stu-id="d4a95-115">You can’t remove a cost element.</span></span> <span data-ttu-id="d4a95-116">Однако при изменении даты начала и окончания так, чтобы они находились вне диапазона дат цикла планирования бюджета, элемент затрат больше не будет назначен прогнозируемым должностям в этом цикле планирования бюджета.</span><span class="sxs-lookup"><span data-stu-id="d4a95-116">However, if you change the start and end dates so that they are outside the budget planning cycle dates, the cost element will no longer be assigned to the forecast positions in that budget planning cycle.</span></span> <span data-ttu-id="d4a95-117">Чтобы сделать это изменение, откройте элемент бюджетных затрат, затем на экспресс-вкладке **Вычисление затрат** нажмите **Изменить даты** и измените дату вступления в силу и дату окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="d4a95-117">To make this change, open the budget cost element, and then, on the **Cost calculation** FastTab, click **Change dates**, and change the effective date or expiration date.</span></span> <span data-ttu-id="d4a95-118">Затем нажмите **ОК** для автоматического обновления всех прогнозируемых должностей, которым назначен элемент затрат.</span><span class="sxs-lookup"><span data-stu-id="d4a95-118">Then click **OK** to automatically update all forecast positions that the cost element is assigned to.</span></span> <span data-ttu-id="d4a95-119">**Совет.** При использовании этого метода необходимо помнить, что элемент бюджетных затрат будет удален из **всех** прогнозируемых должностей, в которых начальная и конечная даты больше не входят в соответствующий диапазон.</span><span class="sxs-lookup"><span data-stu-id="d4a95-119">**Tip:** If you use this method, be aware that it removes the budget cost element from **all** forecast positions where the start and end dates are no longer within the appropriate range.</span></span> <span data-ttu-id="d4a95-120">Если это не то, что вам требуется, необходимо открыть каждую прогнозируемую должность, из которой следует удалить элемент бюджетных затрат, и внести изменение вручную.</span><span class="sxs-lookup"><span data-stu-id="d4a95-120">If this effect isn't what you intend, you must open each forecast position that you want to remove the budget cost element from and manually make the change.</span></span>

## <a name="why-cant-i-enter-an-annual-amount-on-the-cost-calculation-fasttab-for-the-budget-cost-element"></a><span data-ttu-id="d4a95-121">Почему я не могу ввести годовую сумму на экспресс-вкладке "Вычисление затрат" элемента бюджетных затрат?</span><span class="sxs-lookup"><span data-stu-id="d4a95-121">Why can’t I enter an annual amount on the Cost calculation FastTab for the budget cost element?</span></span>
<span data-ttu-id="d4a95-122">Нельзя ввести годовую сумму, если на экспресс-вкладке **Основа расчета** имеются элементы бюджетных затрат, поскольку системе требуется процент для расчета значения.</span><span class="sxs-lookup"><span data-stu-id="d4a95-122">You can’t enter an annual amount if there are budget cost elements on the **Calculation basis** FastTab, because the system requires a percentage in order to calculate the value.</span></span> <span data-ttu-id="d4a95-123">Чтобы изменить это значение, удалите все элементы бюджетных затрат с экспресс-вкладки **Основа расчета**.</span><span class="sxs-lookup"><span data-stu-id="d4a95-123">To change the value, remove all budget cost elements from the **Calculation basis** FastTab.</span></span>

## <a name="why-cant-i-change-the-budget-cost-type-from-earning-to-another-budget-cost-type"></a><span data-ttu-id="d4a95-124">Почему я не могу изменить тип бюджетных затрат с дохода на другой тип бюджетных затрат?</span><span class="sxs-lookup"><span data-stu-id="d4a95-124">Why can’t I change the budget cost type from earning to another budget cost type?</span></span>
<span data-ttu-id="d4a95-125">Некоторые элементы бюджетных затрат используют элемент затрат "Доход" как основу для расчета.</span><span class="sxs-lookup"><span data-stu-id="d4a95-125">Some budget cost elements use the earning cost element as a calculation basis.</span></span> <span data-ttu-id="d4a95-126">Для изменения поля **Тип бюджетных затрат** удалите элемент затрат "Доход" с экспресс-вкладки **Основа расчета** для всех элементов бюджетных затрат.</span><span class="sxs-lookup"><span data-stu-id="d4a95-126">To change the **Budget cost type** field, remove the earning cost element from the **Calculation basis** FastTab of all budget cost elements.</span></span>

## <a name="why-cant-i-change-the-date-on-budget-cost-element-lines-for-a-budget-cost-element"></a><span data-ttu-id="d4a95-127">Почему я не могу изменить дату в строках элемента бюджетных затрат для элемента бюджетных затрат?</span><span class="sxs-lookup"><span data-stu-id="d4a95-127">Why can’t I change the date on budget cost element lines for a budget cost element?</span></span>
<span data-ttu-id="d4a95-128">Невозможно изменить дату в строке элемента бюджетных затрат, если элемент бюджетных затрат используется прогнозируемой должностью.</span><span class="sxs-lookup"><span data-stu-id="d4a95-128">You can’t change the date on the budget cost element line when a budget cost element is used by a forecast position.</span></span> <span data-ttu-id="d4a95-129">Это ограничение помогает обеспечить, чтобы прогнозируемые должности всегда соответствовали нормативам элемента бюджетных затрат.</span><span class="sxs-lookup"><span data-stu-id="d4a95-129">This limitation helps guarantee that the forecast positions are always within the guidelines of the budget cost element.</span></span> <span data-ttu-id="d4a95-130">Чтобы изменить дату, на экспресс-вкладке **Вычисление затрат** щелкните **Изменить даты** и введите новые даты.</span><span class="sxs-lookup"><span data-stu-id="d4a95-130">To change the date, on the **Cost calculation** FastTab, click **Change dates**, and enter the new dates.</span></span> <span data-ttu-id="d4a95-131">Затем нажмите **ОК** для обновления должностей, которым назначен элемент затрат.</span><span class="sxs-lookup"><span data-stu-id="d4a95-131">Then click **OK** to update the positions that the cost element is assigned to.</span></span>

## <a name="why-cant-i-change-the-costs-for-a-budget-cost-element-on-the-compensation-group-page"></a><span data-ttu-id="d4a95-132">Почему я не могу изменить затраты для элемента бюджетных затрат на странице "Группа компенсации"?</span><span class="sxs-lookup"><span data-stu-id="d4a95-132">Why can’t I change the costs for a budget cost element on the Compensation group page?</span></span>
<span data-ttu-id="d4a95-133">Элементы бюджетных затрат можно создавать и изменять только на странице **Элементы бюджетных затрат**.</span><span class="sxs-lookup"><span data-stu-id="d4a95-133">You can create and change budget cost elements only on the **Budget cost elements** page.</span></span>

## <a name="why-do-i-receive-an-error-message-when-i-change-the-dates-for-a-cost-element-on-a-forecast-position"></a><span data-ttu-id="d4a95-134">Почему я получаю сообщение об ошибке, когда изменяю даты для элемента затрат в прогнозируемой должности?</span><span class="sxs-lookup"><span data-stu-id="d4a95-134">Why do I receive an error message when I change the dates for a cost element on a forecast position?</span></span>
<span data-ttu-id="d4a95-135">Даты в строке элемента затрат прогнозируемой должности должны входить в следующие диапазоны.</span><span class="sxs-lookup"><span data-stu-id="d4a95-135">The dates on the forecast position cost element line must be within the following ranges:</span></span>

-   <span data-ttu-id="d4a95-136">Даты активации и выбытия должности.</span><span class="sxs-lookup"><span data-stu-id="d4a95-136">The activation and retirement dates of the position.</span></span>
-   <span data-ttu-id="d4a95-137">Даты активации и окончания срока действия элемента бюджетных затрат.</span><span class="sxs-lookup"><span data-stu-id="d4a95-137">The activation and expiration dates of the budget cost element.</span></span>
-   <span data-ttu-id="d4a95-138">Даты начала и окончания бюджетного цикла, связанного с процессом бюджетного планирования прогнозируемой должности.</span><span class="sxs-lookup"><span data-stu-id="d4a95-138">The start and end dates of the budget cycle that is associated with the budget planning process of the forecast position.</span></span>





