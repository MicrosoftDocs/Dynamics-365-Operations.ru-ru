--- 
title: "Создание журнала списания для клиента"
description: "В этом руководстве по задаче показано, как настроить параметры для списания, а затем списать проводки на странице \"Сборы\", странице \"Открытые накладные клиента\" и странице \"Клиент\"."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 4b7f585502b6734b3e18095a756ab07860fc5de5
ms.contentlocale: ru-ru
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-write-off-journal-for-a-customer"></a><span data-ttu-id="e02f7-103">Создание журнала списания для клиента</span><span class="sxs-lookup"><span data-stu-id="e02f7-103">Create a write-off journal for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e02f7-104">В этом руководстве по задаче показано, как настроить параметры для списания, а затем списать проводки на странице "Сборы", странице "Открытые накладные клиента" и странице "Клиент".</span><span class="sxs-lookup"><span data-stu-id="e02f7-104">This task guide will show you how to set up the parameters for write-offs and then write off transactions from the Collections page, the Open customer invoices page, and the Customer page.</span></span> <span data-ttu-id="e02f7-105">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="e02f7-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-the-write-off-parameters"></a><span data-ttu-id="e02f7-106">Настройка параметров списания</span><span class="sxs-lookup"><span data-stu-id="e02f7-106">Set up the write off parameters</span></span>
1. <span data-ttu-id="e02f7-107">Перейдите в раздел "Кредит и сборы" > "Настройка" > "Параметры расчетов с клиентами".</span><span class="sxs-lookup"><span data-stu-id="e02f7-107">Go to Credit and collections > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="e02f7-108">Перейдите на вкладку "Сборы".</span><span class="sxs-lookup"><span data-stu-id="e02f7-108">Click the Collections tab.</span></span>
3. <span data-ttu-id="e02f7-109">Разверните или сверните раздел "Списание".</span><span class="sxs-lookup"><span data-stu-id="e02f7-109">Expand or collapse the Write-off section.</span></span>
    * <span data-ttu-id="e02f7-110">Журнал списания — это общий журнал, в котором будут указаны созданные проводки списания.</span><span class="sxs-lookup"><span data-stu-id="e02f7-110">The Write-off journal is the general journal that will hold the write-off transactions that you create.</span></span>  
    * <span data-ttu-id="e02f7-111">Можно добавить код причины к каждому списанию.</span><span class="sxs-lookup"><span data-stu-id="e02f7-111">You can attach a reason code to every write-off.</span></span> <span data-ttu-id="e02f7-112">Можно переопределить это параметр по умолчанию во время списания.</span><span class="sxs-lookup"><span data-stu-id="e02f7-112">You can override this default at the time of the write-off.</span></span>  
    * <span data-ttu-id="e02f7-113">Задайте значение "Да", если необходимо разделить налог и исходную проводку в списании.</span><span class="sxs-lookup"><span data-stu-id="e02f7-113">Set this to Yes if you want to separate the sales tax from the original transaction in the write-off.</span></span>  
4. <span data-ttu-id="e02f7-114">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e02f7-114">Close the page.</span></span>
5. <span data-ttu-id="e02f7-115">Перейдите в раздел "Кредит и сборы" > "Настройка" > "Профили разноски по клиенту".</span><span class="sxs-lookup"><span data-stu-id="e02f7-115">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
    * <span data-ttu-id="e02f7-116">Счет списания будет использоваться как счет расходов или корректировка резервирование в общем журнале</span><span class="sxs-lookup"><span data-stu-id="e02f7-116">The write-off account will be used as the expense account or reserve adjustment in the general journal</span></span>   
6. <span data-ttu-id="e02f7-117">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e02f7-117">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a><span data-ttu-id="e02f7-118">Списание сальдо клиента на странице сальдо с распределением по срокам</span><span class="sxs-lookup"><span data-stu-id="e02f7-118">Write off a customer balance from the aged balances page</span></span>
1. <span data-ttu-id="e02f7-119">Перейдите в раздел "Кредит и сборы" > "Сборы" > "Сальдо по срокам".</span><span class="sxs-lookup"><span data-stu-id="e02f7-119">Go to Credit and collections > Collections > Aged balances.</span></span>
2. <span data-ttu-id="e02f7-120">Пометьте строку клиента, которого требуется списать.</span><span class="sxs-lookup"><span data-stu-id="e02f7-120">Mark the row for the customer that you want to write off.</span></span> <span data-ttu-id="e02f7-121">Например, пометьте строку, в которой указана компания Birch.</span><span class="sxs-lookup"><span data-stu-id="e02f7-121">For example, mark the line with Birch Company on it.</span></span>
3. <span data-ttu-id="e02f7-122">В области действий щелкните "Сбор".</span><span class="sxs-lookup"><span data-stu-id="e02f7-122">On the Action Pane, click Collect.</span></span>
4. <span data-ttu-id="e02f7-123">Щелкните "Списание".</span><span class="sxs-lookup"><span data-stu-id="e02f7-123">Click Write off.</span></span>
5. <span data-ttu-id="e02f7-124">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e02f7-124">Click OK.</span></span>
6. <span data-ttu-id="e02f7-125">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e02f7-125">Close the page.</span></span>
7. <span data-ttu-id="e02f7-126">Перейдите в раздел "Главная книга" > "Записи в журнале" > "Общие журналы".</span><span class="sxs-lookup"><span data-stu-id="e02f7-126">Go to General ledger > Journal entries > General journals.</span></span>
8. <span data-ttu-id="e02f7-127">Выберите номер партии журнала, который содержит списание.</span><span class="sxs-lookup"><span data-stu-id="e02f7-127">Select the journal batch number for the journal that contains your write-off.</span></span>
    * <span data-ttu-id="e02f7-128">Одна строка создается для реверсирования сальдо клиента.</span><span class="sxs-lookup"><span data-stu-id="e02f7-128">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="e02f7-129">Одна или несколько строк создаются для разноски списания на счет списания.</span><span class="sxs-lookup"><span data-stu-id="e02f7-129">One or more lines are created to post the write-off to the write-off account.</span></span>  
9. <span data-ttu-id="e02f7-130">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e02f7-130">Close the page.</span></span>
10. <span data-ttu-id="e02f7-131">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e02f7-131">Close the page.</span></span>

## <a name="write-off-transactions-from-the-collections-form"></a><span data-ttu-id="e02f7-132">Спишите проводки в форме сборов.</span><span class="sxs-lookup"><span data-stu-id="e02f7-132">Write off transactions from the collections form.</span></span>
1. <span data-ttu-id="e02f7-133">Перейдите в раздел "Кредит и сборы" > "Сборы" > "Сальдо по срокам".</span><span class="sxs-lookup"><span data-stu-id="e02f7-133">Go to Credit and collections > Collections > Aged balances.</span></span>
2. <span data-ttu-id="e02f7-134">Выберите имя клиента, имеющего проводки, которые необходимо списать.</span><span class="sxs-lookup"><span data-stu-id="e02f7-134">Select the name of the customer that has the transactions that you want to write off.</span></span> <span data-ttu-id="e02f7-135">Например, выберите Cave Wholesales (US-004).</span><span class="sxs-lookup"><span data-stu-id="e02f7-135">For example, select Cave Wholesales (US-004).</span></span>
3. <span data-ttu-id="e02f7-136">Пометьте строку для первой проводки.</span><span class="sxs-lookup"><span data-stu-id="e02f7-136">Mark the row for the first transaction.</span></span>
4. <span data-ttu-id="e02f7-137">Пометьте строку для второй проводки.</span><span class="sxs-lookup"><span data-stu-id="e02f7-137">Mark the row for the second transaction.</span></span>
5. <span data-ttu-id="e02f7-138">Щелкните "Списание".</span><span class="sxs-lookup"><span data-stu-id="e02f7-138">Click Write off.</span></span>
6. <span data-ttu-id="e02f7-139">В поле код "Комментарий к причине" введите "Безнадежные задолженности".</span><span class="sxs-lookup"><span data-stu-id="e02f7-139">In the Reason comment field, type 'Bad debts'.</span></span>
7. <span data-ttu-id="e02f7-140">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e02f7-140">Click OK.</span></span>
8. <span data-ttu-id="e02f7-141">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e02f7-141">Close the page.</span></span>
9. <span data-ttu-id="e02f7-142">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e02f7-142">Close the page.</span></span>
10. <span data-ttu-id="e02f7-143">Перейдите в раздел "Главная книга" > "Записи в журнале" > "Общие журналы".</span><span class="sxs-lookup"><span data-stu-id="e02f7-143">Go to General ledger > Journal entries > General journals.</span></span>
11. <span data-ttu-id="e02f7-144">Выберите номер партии журнала, который содержит списание.</span><span class="sxs-lookup"><span data-stu-id="e02f7-144">Select the journal batch number for the journal that contains your write-off.</span></span>
    * <span data-ttu-id="e02f7-145">Одна строка создается для реверсирования сальдо клиента.</span><span class="sxs-lookup"><span data-stu-id="e02f7-145">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="e02f7-146">Одна или несколько строк создаются для разноски списания на счет списания.</span><span class="sxs-lookup"><span data-stu-id="e02f7-146">One or more lines are created to post the write-off to the write-off account.</span></span>  
12. <span data-ttu-id="e02f7-147">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e02f7-147">Close the page.</span></span>
13. <span data-ttu-id="e02f7-148">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e02f7-148">Close the page.</span></span>

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a><span data-ttu-id="e02f7-149">Списание накладной на странице "Открытые накладные клиентов"</span><span class="sxs-lookup"><span data-stu-id="e02f7-149">Write off an invoice from the Open customers invoices page</span></span>
1. <span data-ttu-id="e02f7-150">Перейдите в раздел "Расчеты с клиентами" > "Накладные" > "Открытые накладные клиента".</span><span class="sxs-lookup"><span data-stu-id="e02f7-150">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="e02f7-151">Пометьте строку для накладной.</span><span class="sxs-lookup"><span data-stu-id="e02f7-151">Mark the line for an invoice.</span></span> <span data-ttu-id="e02f7-152">Например, пометьте строку для CIV-000667.</span><span class="sxs-lookup"><span data-stu-id="e02f7-152">For example, mark the line for CIV-000667.</span></span>
3. <span data-ttu-id="e02f7-153">В области действий щелкните "Накладная".</span><span class="sxs-lookup"><span data-stu-id="e02f7-153">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="e02f7-154">Щелкните "Списание".</span><span class="sxs-lookup"><span data-stu-id="e02f7-154">Click Write off.</span></span>
5. <span data-ttu-id="e02f7-155">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e02f7-155">Click OK.</span></span>
6. <span data-ttu-id="e02f7-156">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e02f7-156">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-customer-page"></a><span data-ttu-id="e02f7-157">Списание сальдо клиента на странице клиента</span><span class="sxs-lookup"><span data-stu-id="e02f7-157">Write off a customer balance from the customer page</span></span>
1. <span data-ttu-id="e02f7-158">Перейдите в раздел "Расчеты с клиентами" > "Клиенты" > "Все клиенты".</span><span class="sxs-lookup"><span data-stu-id="e02f7-158">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="e02f7-159">Выберите счет клиента.</span><span class="sxs-lookup"><span data-stu-id="e02f7-159">Select a customer account.</span></span> <span data-ttu-id="e02f7-160">Например, выберите US-001 (Contoso Retail San Diego).</span><span class="sxs-lookup"><span data-stu-id="e02f7-160">For example, select US-001 (Contoso Retail San Diego).</span></span>
3. <span data-ttu-id="e02f7-161">В области действий щелкните "Сбор".</span><span class="sxs-lookup"><span data-stu-id="e02f7-161">On the Action Pane, click Collect.</span></span>
4. <span data-ttu-id="e02f7-162">Щелкните "Списание".</span><span class="sxs-lookup"><span data-stu-id="e02f7-162">Click Write off.</span></span>
5. <span data-ttu-id="e02f7-163">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="e02f7-163">Click OK.</span></span>
6. <span data-ttu-id="e02f7-164">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="e02f7-164">Close the page.</span></span>


