---
title: Закрытие финансового года
description: В этой процедуре описывается процесс закрытия на конец конца, который переносит сальдо в новый финансовый год.
author: aprilolson
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6299325bb8d77cad3977ae3c20790122574b47f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235821"
---
# <a name="close-the-fiscal-year"></a><span data-ttu-id="d0e90-103">Закрытие финансового года</span><span class="sxs-lookup"><span data-stu-id="d0e90-103">Close the fiscal year</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d0e90-104">В этой процедуре описывается процесс закрытия на конец конца, который переносит сальдо в новый финансовый год.</span><span class="sxs-lookup"><span data-stu-id="d0e90-104">This procedure steps through the year end close process that transfers balances to a new fiscal year.</span></span>


## <a name="validate-year-end-close-parameters"></a><span data-ttu-id="d0e90-105">Проверьте параметры закрытия на конец года</span><span class="sxs-lookup"><span data-stu-id="d0e90-105">Validate year-end close parameters</span></span>
1. <span data-ttu-id="d0e90-106">Выберите **Область переходов > Модули > Главная книга > Настройка главной книги > Параметры главной книги**.</span><span class="sxs-lookup"><span data-stu-id="d0e90-106">Go to **Navigation pane > Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="d0e90-107">Разверните раздел **Закрытие финансового года**.</span><span class="sxs-lookup"><span data-stu-id="d0e90-107">Expand the **Fiscal year close** section.</span></span>
3. <span data-ttu-id="d0e90-108">Выберите "Да" или "Нет" для параметра **Удаление закрывающих проводок при переносе**.</span><span class="sxs-lookup"><span data-stu-id="d0e90-108">Select 'Yes' or 'No' for the **Delete close-of-year transactions during transfer** option.</span></span>
    
    <span data-ttu-id="d0e90-109">Если финансового года уже был закрыт и закрытие на конец года выполняется повторно, эта настройка важна.</span><span class="sxs-lookup"><span data-stu-id="d0e90-109">If the fiscal year has already been closed and the year-end close is being run again, this setting is important.</span></span> <span data-ttu-id="d0e90-110">Если задано значение "Да", ваучер для предыдущего закрытия конца года будет удален, и новый ваучер будет создан для всех начальных сальдо счетов.</span><span class="sxs-lookup"><span data-stu-id="d0e90-110">If set to Yes, the voucher for the previous year-end close will be deleted, and a new voucher will be created for all accounts beginning balances.</span></span> <span data-ttu-id="d0e90-111">Если задано значение "Нет", предыдущий ваучер сохраняется, и новый ваучер создается только для корректирующих записей, которые были разнесены после последнего закрытия на конец года.</span><span class="sxs-lookup"><span data-stu-id="d0e90-111">If set to No, the previous voucher will remain and a new voucher will only be created for adjusting entries that were posted after the last year-end close.</span></span>

4. <span data-ttu-id="d0e90-112">Выберите "Да" или "Нет" для параметра **Создать закрывающие проводки при переносе**.</span><span class="sxs-lookup"><span data-stu-id="d0e90-112">Select 'Yes' or 'No' for the **Create closing transactions during transfer** option.</span></span>

    <span data-ttu-id="d0e90-113">Если задано значение "Да", создаются две проводки.</span><span class="sxs-lookup"><span data-stu-id="d0e90-113">If set to Yes, two transactions are created.</span></span> <span data-ttu-id="d0e90-114">Один ваучер создается в закрываемом финансовом году, чтобы привести сальдо доходов и убытков в счетах ГК к нулевому значению, а другой ваучер создается в следующем финансовом году для начальных сальдо.</span><span class="sxs-lookup"><span data-stu-id="d0e90-114">One voucher is created in the fiscal year being closed to bring the balances of the P&L ledger accounts down to zero and a second voucher is created in the next fiscal year for the beginning balances.</span></span> <span data-ttu-id="d0e90-115">Если задано значение "Нет", создается один ваучер в следующем финансовом году для начальных сальдо.</span><span class="sxs-lookup"><span data-stu-id="d0e90-115">If set to No, a single voucher is created in the next fiscal year for the beginning balances.</span></span>  

5. <span data-ttu-id="d0e90-116">Выберите "Да" или "Нет" для параметра **Задать для финансового года статус закрытого на постоянной основе**.</span><span class="sxs-lookup"><span data-stu-id="d0e90-116">Select 'Yes' or 'No' for the **Set fiscal year status to permanently closed** option.</span></span>

    <span data-ttu-id="d0e90-117">Если задано значение "Да", статус финансового года будет установлен на "Закрытый на постоянной основе".</span><span class="sxs-lookup"><span data-stu-id="d0e90-117">If set to Yes, the fiscal year status will be set to Permanently closed.</span></span>  <span data-ttu-id="d0e90-118">Поскольку постоянно закрытый год не может быть повторно открыт, рекомендуется установить для этого параметра значение "Нет".</span><span class="sxs-lookup"><span data-stu-id="d0e90-118">Because a permanently closed year cannot be reopened, it would be a best practice to set this option to No.</span></span>  

6. <span data-ttu-id="d0e90-119">Выберите "Да" или "Нет" для параметра **Код ваучера должен быть заполнен во время закрытия на конец года**.</span><span class="sxs-lookup"><span data-stu-id="d0e90-119">Select 'Yes' or 'No' for the **Voucher number must be filled in during the year end close** option.</span></span>

    <span data-ttu-id="d0e90-120">Если задано значение "Да", код ваучера необходимо вручную ввести во время процесса закрытия на конец года.</span><span class="sxs-lookup"><span data-stu-id="d0e90-120">If set to Yes, a voucher number must be manually entered during the year end close process.</span></span> <span data-ttu-id="d0e90-121">Номерная серия не используется для создания этого кода ваучера.</span><span class="sxs-lookup"><span data-stu-id="d0e90-121">A number sequence is not used to generate this voucher number.</span></span> <span data-ttu-id="d0e90-122">Рекомендуется установить для этого параметра значение "Да".</span><span class="sxs-lookup"><span data-stu-id="d0e90-122">It's a best practice to set this to Yes.</span></span>  

7. <span data-ttu-id="d0e90-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d0e90-123">Close the page.</span></span>
8. <span data-ttu-id="d0e90-124">Перейдите в раздел **Главная книга > Закрытие периода > Закрытие на конец года**.</span><span class="sxs-lookup"><span data-stu-id="d0e90-124">Go to **General ledger > Period close > Year end close**.</span></span>
9. <span data-ttu-id="d0e90-125">Нажмите **Создать** для создания шаблона закрытия на конец года.</span><span class="sxs-lookup"><span data-stu-id="d0e90-125">Click **New** to create a year-end close template.</span></span>

    <span data-ttu-id="d0e90-126">Шаблон может быть создан для группы юридических лиц, для которых требуется выполнить закрытие на конец года.</span><span class="sxs-lookup"><span data-stu-id="d0e90-126">A template can be created for a group of legal entities for which to run the year-end close.</span></span> <span data-ttu-id="d0e90-127">Этот шаблон можно повторно использовать каждый год.</span><span class="sxs-lookup"><span data-stu-id="d0e90-127">This template can be reused year after year.</span></span>  

10. <span data-ttu-id="d0e90-128">В поле **Имя группы** введите имя шаблона закрытия на конец года.</span><span class="sxs-lookup"><span data-stu-id="d0e90-128">In the **Group name** field, enter a year-end close template name..</span></span>
11. <span data-ttu-id="d0e90-129">В поле **Финансовый календарь** выберите финансовый год, для которого будет создан шаблон.</span><span class="sxs-lookup"><span data-stu-id="d0e90-129">In the **Fiscal calendar** field, select the fiscal year for which the template will be created.</span></span>

    <span data-ttu-id="d0e90-130">Только юридические лица, использующие один и тот же финансовый год, можно сгруппировать вместе в шаблоне закрытия на конец года.</span><span class="sxs-lookup"><span data-stu-id="d0e90-130">Only legal entities which use the same fiscal year can be grouped together in the year-end close template.</span></span> <span data-ttu-id="d0e90-131">Это необходимо, поскольку закрытие на конец года производится путем выбора финансового года, а не даты.</span><span class="sxs-lookup"><span data-stu-id="d0e90-131">This is because the year end close is done by selecting a fiscal year, not a date.</span></span>  

12. <span data-ttu-id="d0e90-132">В области **Панель операций** щелкните **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d0e90-132">On the **Action pane**, click **Save**.</span></span>
13. <span data-ttu-id="d0e90-133">В разделе **Юридические лица** щелкните **Добавить**, чтобы выбрать юридические лица для этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="d0e90-133">In the **Legal entities** section, click **Add** to select the legal entities for this template.</span></span>
    
    <span data-ttu-id="d0e90-134">Юридические лица можно добавлять, выбирая юридические лица или выбирая организационную иерархию.</span><span class="sxs-lookup"><span data-stu-id="d0e90-134">Legal entities can be added by either selecting the legal entities or by selecting an organizational hierarchy.</span></span>  <span data-ttu-id="d0e90-135">Будут добавлены только юридические лица с организационной иерархией с одинаковым выбранным финансовым календарем.</span><span class="sxs-lookup"><span data-stu-id="d0e90-135">Only legal entities with the organizational hierarchy with the same fiscal calendar selected will be added.</span></span>  

14. <span data-ttu-id="d0e90-136">Выберите юридические лица или организационную иерархию.</span><span class="sxs-lookup"><span data-stu-id="d0e90-136">Select either the legal entities or the organizational hierarchy.</span></span>
15. <span data-ttu-id="d0e90-137">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e90-137">Click **OK**.</span></span>
16. <span data-ttu-id="d0e90-138">Выберите "Да" или "Нет" в параметре **Переместить аналитики балансового отчета**.</span><span class="sxs-lookup"><span data-stu-id="d0e90-138">Select 'Yes' or 'No' in the **Transfer balance sheet dimension**.</span></span>

    <span data-ttu-id="d0e90-139">Рекомендуется задать для этого параметра значение "Да" для балансовых счетов.</span><span class="sxs-lookup"><span data-stu-id="d0e90-139">It's best practice to set this option to Yes for Balance sheet accounts.</span></span> <span data-ttu-id="d0e90-140">Это позволит сохранить финансовые аналитики в разнесенных проводках при создании начальных сальдо для балансовых счетов.</span><span class="sxs-lookup"><span data-stu-id="d0e90-140">This will maintain the financial dimensions on posted transactions when creating the beginning balances for the balance sheet accounts.</span></span> <span data-ttu-id="d0e90-141">Для счетов прибылей и убытков можно выбрать сохранение финансовых аналитик (Закрыть все), когда сальдо переносятся в нераспределенную прибыль, или можно выбрать, чтобы заменить финансовые аналитики на другое значение аналитики (Закрыть один).</span><span class="sxs-lookup"><span data-stu-id="d0e90-141">For profit and loss accounts, you can select to maintain the financial dimensions (Close all) when the balances are moved to Retained earnings or you can select to have the financial dimensions replaced with a different dimension value (Close single).</span></span> <span data-ttu-id="d0e90-142">При выборе значения "Закрыть один" можно указать конкретное значение аналитики для каждой аналитики или даже оставить его пустым.</span><span class="sxs-lookup"><span data-stu-id="d0e90-142">If you choose Close single, you can define a specific dimension value for each dimension or even choose to leave it blank.</span></span>  

17. <span data-ttu-id="d0e90-143">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d0e90-143">Click **Save**.</span></span>
18. <span data-ttu-id="d0e90-144">Запустите закрытие на конец года, выбрав **Выполнить финансовое закрытие** в области **Панель операций**.</span><span class="sxs-lookup"><span data-stu-id="d0e90-144">Start the year-end close by choosing **Run fiscal close** on the **Action Pane**.</span></span> <span data-ttu-id="d0e90-145">Закрытие на конец года выполняется для выбранного шаблона.</span><span class="sxs-lookup"><span data-stu-id="d0e90-145">The year-end close will be run for the selected template.</span></span>  
19. <span data-ttu-id="d0e90-146">Выберите все или подмножество юридических лиц из шаблона, для которых требуется выполнить закрытие на конец года.</span><span class="sxs-lookup"><span data-stu-id="d0e90-146">Select all or a subset of legal entities from the template for which to run the year-end close.</span></span>

    <span data-ttu-id="d0e90-147">При первом выполнении закрытия на конец года для получения начальных сальдо большинство организаций могут выбрать выполнение закрытия на конец года для всех юридических лиц в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="d0e90-147">When first running the year-end close, to get beginning balance,s most organizations may choose to run the year-end close for all legal entities within the template.</span></span> <span data-ttu-id="d0e90-148">Если записи корректировки выполняются после этого, можно выбрать выполнение закрытия на конец года только для юридических лиц, для которых имеются корректировки.</span><span class="sxs-lookup"><span data-stu-id="d0e90-148">If adjusting entries are made after that, you may choose to run the year-end close for only the legal entities that have adjustments.</span></span>  

20. <span data-ttu-id="d0e90-149">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e90-149">Click **OK**.</span></span>
21. <span data-ttu-id="d0e90-150">Выберите финансовый год, для которого требуется выполнить закрытие на конец года.</span><span class="sxs-lookup"><span data-stu-id="d0e90-150">Select the fiscal year for which to run the year-end close.</span></span>
22. <span data-ttu-id="d0e90-151">В поле **Ваучер** введите значение.</span><span class="sxs-lookup"><span data-stu-id="d0e90-151">In the **Voucher field**, type a value.</span></span> <span data-ttu-id="d0e90-152">Рекомендуется включать финансовый год в код ваучера, чтобы упростить поиск созданного ваучера закрытия на конец года.</span><span class="sxs-lookup"><span data-stu-id="d0e90-152">It's best practice to include the fiscal year in the voucher number, to make it easier to find the year-end close voucher that is created.</span></span>  
23. <span data-ttu-id="d0e90-153">Закрытие на конец года по умолчанию выполняется в пакетном режиме.</span><span class="sxs-lookup"><span data-stu-id="d0e90-153">The year-end close defaults to run in batch.</span></span> <span data-ttu-id="d0e90-154">Рекомендуется выполнять длительные процессы в пакетном режиме.</span><span class="sxs-lookup"><span data-stu-id="d0e90-154">It's best practice for long-running processes to run in batch mode.</span></span> <span data-ttu-id="d0e90-155">Обычно это один из таких процессов, поэтому по умолчанию задано использование пакетного режима.</span><span class="sxs-lookup"><span data-stu-id="d0e90-155">This is typically one of those processes, which is why the default is to use batch mode.</span></span>  
24. <span data-ttu-id="d0e90-156">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0e90-156">Click **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]