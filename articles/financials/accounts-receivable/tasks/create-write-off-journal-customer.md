---
title: Создание журнала списания для клиента
description: В этом руководстве по задаче показано, как настроить параметры для списания, а затем списать проводки на странице "Сборы", странице "Открытые накладные клиента" и странице "Клиент".
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 44f36a12195a57e1b4cea524d2e4881f1fa7d0e9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842937"
---
# <a name="create-a-write-off-journal-for-a-customer"></a><span data-ttu-id="8119b-103">Создание журнала списания для клиента</span><span class="sxs-lookup"><span data-stu-id="8119b-103">Create a write-off journal for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8119b-104">В этом руководстве по задаче показано, как настроить параметры для списания, а затем списать проводки на странице "Сборы", странице "Открытые накладные клиента" и странице "Клиент".</span><span class="sxs-lookup"><span data-stu-id="8119b-104">This task guide will show you how to set up the parameters for write-offs and then write off transactions from the Collections page, the Open customer invoices page, and the Customer page.</span></span> <span data-ttu-id="8119b-105">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="8119b-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-the-write-off-parameters"></a><span data-ttu-id="8119b-106">Настройка параметров списания</span><span class="sxs-lookup"><span data-stu-id="8119b-106">Set up the write off parameters</span></span>
1. <span data-ttu-id="8119b-107">Перейдите в раздел "Кредит и сборы" > "Настройка" > "Параметры расчетов с клиентами".</span><span class="sxs-lookup"><span data-stu-id="8119b-107">Go to Credit and collections > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="8119b-108">Перейдите на вкладку "Сборы".</span><span class="sxs-lookup"><span data-stu-id="8119b-108">Click the Collections tab.</span></span>
3. <span data-ttu-id="8119b-109">Разверните или сверните раздел "Списание".</span><span class="sxs-lookup"><span data-stu-id="8119b-109">Expand or collapse the Write-off section.</span></span>
    * <span data-ttu-id="8119b-110">Журнал списания — это общий журнал, в котором будут указаны созданные проводки списания.</span><span class="sxs-lookup"><span data-stu-id="8119b-110">The Write-off journal is the general journal that will hold the write-off transactions that you create.</span></span>  
    * <span data-ttu-id="8119b-111">Можно добавить код причины к каждому списанию.</span><span class="sxs-lookup"><span data-stu-id="8119b-111">You can attach a reason code to every write-off.</span></span> <span data-ttu-id="8119b-112">Можно переопределить это параметр по умолчанию во время списания.</span><span class="sxs-lookup"><span data-stu-id="8119b-112">You can override this default at the time of the write-off.</span></span>  
    * <span data-ttu-id="8119b-113">Задайте значение "Да", если необходимо разделить налог и исходную проводку в списании.</span><span class="sxs-lookup"><span data-stu-id="8119b-113">Set this to Yes if you want to separate the sales tax from the original transaction in the write-off.</span></span>  
4. <span data-ttu-id="8119b-114">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8119b-114">Close the page.</span></span>
5. <span data-ttu-id="8119b-115">Перейдите в раздел "Кредит и сборы" > "Настройка" > "Профили разноски по клиенту".</span><span class="sxs-lookup"><span data-stu-id="8119b-115">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
    * <span data-ttu-id="8119b-116">Счет списания будет использоваться как счет расходов или корректировка резервирование в общем журнале</span><span class="sxs-lookup"><span data-stu-id="8119b-116">The write-off account will be used as the expense account or reserve adjustment in the general journal</span></span>   
6. <span data-ttu-id="8119b-117">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8119b-117">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a><span data-ttu-id="8119b-118">Списание сальдо клиента на странице сальдо с распределением по срокам</span><span class="sxs-lookup"><span data-stu-id="8119b-118">Write off a customer balance from the aged balances page</span></span>
1. <span data-ttu-id="8119b-119">Перейдите в раздел "Кредит и сборы" > "Сборы" > "Сальдо по срокам".</span><span class="sxs-lookup"><span data-stu-id="8119b-119">Go to Credit and collections > Collections > Aged balances.</span></span>
2. <span data-ttu-id="8119b-120">Пометьте строку клиента, которого требуется списать.</span><span class="sxs-lookup"><span data-stu-id="8119b-120">Mark the row for the customer that you want to write off.</span></span> <span data-ttu-id="8119b-121">Например, пометьте строку, в которой указана компания Birch.</span><span class="sxs-lookup"><span data-stu-id="8119b-121">For example, mark the line with Birch Company on it.</span></span>
3. <span data-ttu-id="8119b-122">В области действий щелкните "Сбор".</span><span class="sxs-lookup"><span data-stu-id="8119b-122">On the Action Pane, click Collect.</span></span>
4. <span data-ttu-id="8119b-123">Щелкните "Списание".</span><span class="sxs-lookup"><span data-stu-id="8119b-123">Click Write off.</span></span>
5. <span data-ttu-id="8119b-124">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8119b-124">Click OK.</span></span>
6. <span data-ttu-id="8119b-125">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8119b-125">Close the page.</span></span>
7. <span data-ttu-id="8119b-126">Перейдите в раздел "Главная книга" > "Записи в журнале" > "Общие журналы".</span><span class="sxs-lookup"><span data-stu-id="8119b-126">Go to General ledger > Journal entries > General journals.</span></span>
8. <span data-ttu-id="8119b-127">Выберите номер партии журнала, который содержит списание.</span><span class="sxs-lookup"><span data-stu-id="8119b-127">Select the journal batch number for the journal that contains your write-off.</span></span>
    * <span data-ttu-id="8119b-128">Одна строка создается для реверсирования сальдо клиента.</span><span class="sxs-lookup"><span data-stu-id="8119b-128">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="8119b-129">Одна или несколько строк создаются для разноски списания на счет списания.</span><span class="sxs-lookup"><span data-stu-id="8119b-129">One or more lines are created to post the write-off to the write-off account.</span></span>  
9. <span data-ttu-id="8119b-130">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8119b-130">Close the page.</span></span>
10. <span data-ttu-id="8119b-131">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8119b-131">Close the page.</span></span>

## <a name="write-off-transactions-from-the-collections-form"></a><span data-ttu-id="8119b-132">Спишите проводки в форме сборов.</span><span class="sxs-lookup"><span data-stu-id="8119b-132">Write off transactions from the collections form.</span></span>
1. <span data-ttu-id="8119b-133">Перейдите в раздел "Кредит и сборы" > "Сборы" > "Сальдо по срокам".</span><span class="sxs-lookup"><span data-stu-id="8119b-133">Go to Credit and collections > Collections > Aged balances.</span></span>
2. <span data-ttu-id="8119b-134">Выберите имя клиента, имеющего проводки, которые необходимо списать.</span><span class="sxs-lookup"><span data-stu-id="8119b-134">Select the name of the customer that has the transactions that you want to write off.</span></span> <span data-ttu-id="8119b-135">Например, выберите Cave Wholesales (US-004).</span><span class="sxs-lookup"><span data-stu-id="8119b-135">For example, select Cave Wholesales (US-004).</span></span>
3. <span data-ttu-id="8119b-136">Пометьте строку для первой проводки.</span><span class="sxs-lookup"><span data-stu-id="8119b-136">Mark the row for the first transaction.</span></span>
4. <span data-ttu-id="8119b-137">Пометьте строку для второй проводки.</span><span class="sxs-lookup"><span data-stu-id="8119b-137">Mark the row for the second transaction.</span></span>
5. <span data-ttu-id="8119b-138">Щелкните "Списание".</span><span class="sxs-lookup"><span data-stu-id="8119b-138">Click Write off.</span></span>
6. <span data-ttu-id="8119b-139">В поле код "Комментарий к причине" введите "Безнадежные задолженности".</span><span class="sxs-lookup"><span data-stu-id="8119b-139">In the Reason comment field, type 'Bad debts'.</span></span>
7. <span data-ttu-id="8119b-140">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8119b-140">Click OK.</span></span>
8. <span data-ttu-id="8119b-141">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8119b-141">Close the page.</span></span>
9. <span data-ttu-id="8119b-142">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8119b-142">Close the page.</span></span>
10. <span data-ttu-id="8119b-143">Перейдите в раздел "Главная книга" > "Записи в журнале" > "Общие журналы".</span><span class="sxs-lookup"><span data-stu-id="8119b-143">Go to General ledger > Journal entries > General journals.</span></span>
11. <span data-ttu-id="8119b-144">Выберите номер партии журнала, который содержит списание.</span><span class="sxs-lookup"><span data-stu-id="8119b-144">Select the journal batch number for the journal that contains your write-off.</span></span>
    * <span data-ttu-id="8119b-145">Одна строка создается для реверсирования сальдо клиента.</span><span class="sxs-lookup"><span data-stu-id="8119b-145">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="8119b-146">Одна или несколько строк создаются для разноски списания на счет списания.</span><span class="sxs-lookup"><span data-stu-id="8119b-146">One or more lines are created to post the write-off to the write-off account.</span></span>  
12. <span data-ttu-id="8119b-147">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8119b-147">Close the page.</span></span>
13. <span data-ttu-id="8119b-148">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8119b-148">Close the page.</span></span>

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a><span data-ttu-id="8119b-149">Списание накладной на странице "Открытые накладные клиентов"</span><span class="sxs-lookup"><span data-stu-id="8119b-149">Write off an invoice from the Open customers invoices page</span></span>
1. <span data-ttu-id="8119b-150">Перейдите в раздел "Расчеты с клиентами" > "Накладные" > "Открытые накладные клиента".</span><span class="sxs-lookup"><span data-stu-id="8119b-150">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="8119b-151">Пометьте строку для накладной.</span><span class="sxs-lookup"><span data-stu-id="8119b-151">Mark the line for an invoice.</span></span> <span data-ttu-id="8119b-152">Например, пометьте строку для CIV-000667.</span><span class="sxs-lookup"><span data-stu-id="8119b-152">For example, mark the line for CIV-000667.</span></span>
3. <span data-ttu-id="8119b-153">В области действий щелкните "Накладная".</span><span class="sxs-lookup"><span data-stu-id="8119b-153">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="8119b-154">Щелкните "Списание".</span><span class="sxs-lookup"><span data-stu-id="8119b-154">Click Write off.</span></span>
5. <span data-ttu-id="8119b-155">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8119b-155">Click OK.</span></span>
6. <span data-ttu-id="8119b-156">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8119b-156">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-customer-page"></a><span data-ttu-id="8119b-157">Списание сальдо клиента на странице клиента</span><span class="sxs-lookup"><span data-stu-id="8119b-157">Write off a customer balance from the customer page</span></span>
1. <span data-ttu-id="8119b-158">Перейдите в раздел "Расчеты с клиентами" > "Клиенты" > "Все клиенты".</span><span class="sxs-lookup"><span data-stu-id="8119b-158">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="8119b-159">Выберите счет клиента.</span><span class="sxs-lookup"><span data-stu-id="8119b-159">Select a customer account.</span></span> <span data-ttu-id="8119b-160">Например, выберите US-001 (Contoso Retail San Diego).</span><span class="sxs-lookup"><span data-stu-id="8119b-160">For example, select US-001 (Contoso Retail San Diego).</span></span>
3. <span data-ttu-id="8119b-161">В области действий щелкните "Сбор".</span><span class="sxs-lookup"><span data-stu-id="8119b-161">On the Action Pane, click Collect.</span></span>
4. <span data-ttu-id="8119b-162">Щелкните "Списание".</span><span class="sxs-lookup"><span data-stu-id="8119b-162">Click Write off.</span></span>
5. <span data-ttu-id="8119b-163">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8119b-163">Click OK.</span></span>
6. <span data-ttu-id="8119b-164">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8119b-164">Close the page.</span></span>

