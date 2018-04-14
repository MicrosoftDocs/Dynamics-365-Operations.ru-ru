---
title: "Возврат НДС в модуле \"Управление расходами\""
description: "В этом разделе описан порядок получения возврата денежных средств по соответствующим проводкам налога на добавленную стоимость (НДС)."
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: d1c9357f8f51e1a87aebeb8f802dbe3b5fdd5aa0
ms.contentlocale: ru-ru
ms.lasthandoff: 03/13/2018

---

# <a name="vat-recovery-in-expense-management"></a><span data-ttu-id="55845-103">Возврат НДС в модуле "Управление расходами"</span><span class="sxs-lookup"><span data-stu-id="55845-103">VAT recovery in Expense management</span></span>

<span data-ttu-id="55845-104">Для получения возврата денежных средств на подходящих проводках налога на добавленную стоимость (НДС) компании или организации необходимо найти, собрать, проверить и отправить точную информацию.</span><span class="sxs-lookup"><span data-stu-id="55845-104">To receive refunds on eligible value-added tax (VAT) transactions, a company or organization must identify, collect, verify, and submit accurate information.</span></span> <span data-ttu-id="55845-105">Этот процесс включает в себя несколько задач, и, в зависимости от размера компании, может включать несколько ролей или сотрудников.</span><span class="sxs-lookup"><span data-stu-id="55845-105">This process includes multiple tasks and, depending on the size of your company, can include several employees or roles.</span></span>

<span data-ttu-id="55845-106">Для возврата НДС с помощью модуля "Управление расходами", должны быть выполнены следующие предварительные требования:</span><span class="sxs-lookup"><span data-stu-id="55845-106">To recover VAT by using Expense management, the following prerequisites must be completed:</span></span>

- <span data-ttu-id="55845-107">Налоговые коды должны быть созданы для страны/региона, относящейся к категории расходов.</span><span class="sxs-lookup"><span data-stu-id="55845-107">Tax codes must be created for countries/regions that are allocated to expense categories.</span></span>
- <span data-ttu-id="55845-108">Налоговую группа необходимо создать для каждого налогового кода.</span><span class="sxs-lookup"><span data-stu-id="55845-108">A sales tax group must be created for each tax code.</span></span>
- <span data-ttu-id="55845-109">Налоговый код номенклатуры должен быть создан для каждой налоговой группы.</span><span class="sxs-lookup"><span data-stu-id="55845-109">An item sales tax code must be created for each sales tax group.</span></span>

<span data-ttu-id="55845-110">После того как выполнены обязательные предварительные условия, сотрудники могут выполнить эти шаги для запроса возврата денежных средств по проводкам НДС.</span><span class="sxs-lookup"><span data-stu-id="55845-110">After the prerequisites are completed, employees follow these steps to request refunds for VAT transactions.</span></span>

1. <span data-ttu-id="55845-111">В отчете о расходах введите налоговые сведения о проводках кредитной карты для определения подходящие возврат денежных средств НДС.</span><span class="sxs-lookup"><span data-stu-id="55845-111">On an expense report, enter tax information about credit card transactions to identify eligible VAT refunds.</span></span>
2. <span data-ttu-id="55845-112">Убедитесь, что все сведения о налогах заполнены, затем выполните разноску отчета о расходах.</span><span class="sxs-lookup"><span data-stu-id="55845-112">Make sure that all tax information is complete, and then post the expense report.</span></span>
3. <span data-ttu-id="55845-113">Выполните обработку расходов, которые подходят для возмещения международного НДС.</span><span class="sxs-lookup"><span data-stu-id="55845-113">Process expenses that are eligible for international VAT recovery.</span></span>
4. <span data-ttu-id="55845-114">Отправьте данные по возмещения НДС сторонним поставщикам для возврата международного возмещения.</span><span class="sxs-lookup"><span data-stu-id="55845-114">Send VAT recovery data to the third-party vendor to file international recovery returns.</span></span>
5. <span data-ttu-id="55845-115">Обработка расходы для возмещения местного НДС.</span><span class="sxs-lookup"><span data-stu-id="55845-115">Process expenses for domestic VAT recovery.</span></span>

<span data-ttu-id="55845-116">В следующих разделах приведены примеры, показывающие, как сотрудники компании Contoso выполняют каждый шаг.</span><span class="sxs-lookup"><span data-stu-id="55845-116">The following sections provide examples that show how Contoso employees complete each step.</span></span>

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a><span data-ttu-id="55845-117">В отчете о расходах введите налоговые сведения о проводках кредитной карты для определения подходящие возврат денежных средств НДС</span><span class="sxs-lookup"><span data-stu-id="55845-117">On an expense report, enter tax information about credit card transactions to identify eligible VAT refunds</span></span>

<span data-ttu-id="55845-118">Нэнси, торговый представитель компании Contoso, которая располагается на территории США, недавно вернулась из деловой поездки в Великобританию.</span><span class="sxs-lookup"><span data-stu-id="55845-118">Nancy, a Contoso sales representative who is based in the US, recently returned from a sales trip to the United Kingdom.</span></span> <span data-ttu-id="55845-119">Во время ее путешествия, она произвела некоторые Личные расходы по кредитной карте для еды.</span><span class="sxs-lookup"><span data-stu-id="55845-119">During her trip, she incurred some personal credit card expenses for meals.</span></span> <span data-ttu-id="55845-120">Нэнси теперь должна создать отчет о расходах для выверки ее расходов.</span><span class="sxs-lookup"><span data-stu-id="55845-120">Nancy must now create an expense report to reconcile her expenses.</span></span>

<span data-ttu-id="55845-121">Когда Нэнси вводит информацию в свой отчет о расходах, она выбирает **Великобритания** в поле **Страна/регион** на странице **Изменить отчет по расходам**.</span><span class="sxs-lookup"><span data-stu-id="55845-121">When Nancy enters information on her expense report, she selects **United Kingdom** in the **Country/region** field on the **Edit expense report** page.</span></span> <span data-ttu-id="55845-122">Список групп налогов затем фильтруется, чтобы отобразить только те группы, которые имеют отношение к Великобритании.</span><span class="sxs-lookup"><span data-stu-id="55845-122">The list of sales tax groups is then filtered so that it shows only the groups that apply to the United Kingdom.</span></span> <span data-ttu-id="55845-123">Нэнси выбирает налоговую группу **Великобритания 001**, а затем выбирает налоговую группу номенклатур **Питание**.</span><span class="sxs-lookup"><span data-stu-id="55845-123">Nancy selects the **United Kingdom 001** sales tax group and then selects the **Meals** item sales tax group.</span></span> <span data-ttu-id="55845-124">Затем она добавляет новую проводку для своего проживания.</span><span class="sxs-lookup"><span data-stu-id="55845-124">She then adds a new transaction for her lodging.</span></span> <span data-ttu-id="55845-125">Поскольку имеется только одна налоговая группа и налоговая группа номенклатур для проживания в Великобритании, эти сведения автоматически заполняются в отчете о расходах Нэнси.</span><span class="sxs-lookup"><span data-stu-id="55845-125">Because there is only one sales tax group and item sales tax group for lodging in the United Kingdom, this information is automatically filled in on Nancy's expense report.</span></span>

<span data-ttu-id="55845-126">Согласно политике компании Contoso, на все расходы должен иметься соответствующий чек.</span><span class="sxs-lookup"><span data-stu-id="55845-126">Per Contoso policy, all expenses must have a matching receipt.</span></span> <span data-ttu-id="55845-127">Поэтому когда Нэнси сохраняет свой отчет о расходах, она получает сообщение о том, что она должна приложить чек для каждой проводки, которую она указала в своем отчете о расходах.</span><span class="sxs-lookup"><span data-stu-id="55845-127">Therefore, when Nancy saves her expense report, she receives a message that states that she must attach a receipt for each transaction that she listed on her expense report.</span></span> <span data-ttu-id="55845-128">Нэнси проверяет, что она присоединила цифровую фотографию чека для каждой проводки к ее отчету о расходах, и затем направляет свой отчет для утверждения.</span><span class="sxs-lookup"><span data-stu-id="55845-128">Nancy verifies that she has attached a digital image of each transaction receipt to her expense report and then submits her report for approval.</span></span> <span data-ttu-id="55845-129">Затем она отправляет бумажные чеки к группу обработки бэк-офиса.</span><span class="sxs-lookup"><span data-stu-id="55845-129">She then sends the paper receipts to the back-office processing team.</span></span> <span data-ttu-id="55845-130">Эта группа отправит данные по возмещению НДС сторонним поставщикам, которые зарегистрируют заявку на международное возмещение НДС для компании Contoso.</span><span class="sxs-lookup"><span data-stu-id="55845-130">This team will send the VAT recovery data to the third-party vendor that files international VAT recovery returns for Contoso.</span></span>

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a><span data-ttu-id="55845-131">Убедитесь, что все сведения о налогах заполнены, затем выполните разноску отчета о расходах</span><span class="sxs-lookup"><span data-stu-id="55845-131">Make sure that all tax information is complete, and then post the expense report</span></span>

<span data-ttu-id="55845-132">Эйприл, координатор расчетов с поставщиками в компании Contoso, должен ввести любые сведения о налогах, которые отсутствуют в отчете о расходах, прежде чем отчет может быть разнесен.</span><span class="sxs-lookup"><span data-stu-id="55845-132">April, the Accounts payable coordinator for Contoso, must enter any tax information that is missing from an expense report before the report can be posted.</span></span> <span data-ttu-id="55845-133">Она открывает страницу **Отчет о расходах: подробности** и видит утвержденный отчет о расходах Нэнси.</span><span class="sxs-lookup"><span data-stu-id="55845-133">She opens the **Expense report details** page and sees Nancy's approved expense report.</span></span> <span data-ttu-id="55845-134">Затем Эйприл открывает отчет о расходах для просмотра подробностей проводок.</span><span class="sxs-lookup"><span data-stu-id="55845-134">April then opens the expense report to view the details of the transactions.</span></span> <span data-ttu-id="55845-135">Она видит, что Нэнси не ввела налоговую группу номенклатур для одной из проводок.</span><span class="sxs-lookup"><span data-stu-id="55845-135">She sees that Nancy didn't enter an item sales tax group for one of the transactions.</span></span> <span data-ttu-id="55845-136">Поскольку этой информации нет, Эйприл не может разнести отчет о расходах.</span><span class="sxs-lookup"><span data-stu-id="55845-136">Because this information isn't provided, April can't post the expense report.</span></span> <span data-ttu-id="55845-137">Поэтому Эйприл открывает страницу **Конфигурации налогов** модуля управления расходами и находит соответствующую налоговую группу номенклатур для страны/региона и типа проводки.</span><span class="sxs-lookup"><span data-stu-id="55845-137">Therefore, April looks on the **Tax configurations** page in Expense management, and finds the appropriate item sales tax group for the country/region and the transaction type.</span></span> <span data-ttu-id="55845-138">April может теперь разнести отчета о расходах в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="55845-138">April can now post the expense report to the general ledger.</span></span>

<span data-ttu-id="55845-139">Когда Эйприл разносит отчет о расходах, создается рабочий элемент возврата НДС.</span><span class="sxs-lookup"><span data-stu-id="55845-139">When April posts the expense report, a VAT recoverable work item is created.</span></span> <span data-ttu-id="55845-140">Этот рабочий элемент назначается члену группы обработки бэк-офиса.</span><span class="sxs-lookup"><span data-stu-id="55845-140">This work item is assigned to a member of the back-office processing team.</span></span> <span data-ttu-id="55845-141">Эйприл получает сообщение, подтверждающее, что разноска была успешной.</span><span class="sxs-lookup"><span data-stu-id="55845-141">April receives a message that confirms that posting was successful.</span></span> <span data-ttu-id="55845-142">В этом сообщении также указано число проводок НДС, которые были определены для возврата.</span><span class="sxs-lookup"><span data-stu-id="55845-142">This message also lists the number of VAT transactions that were identified for recovery.</span></span>

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a><span data-ttu-id="55845-143">Обработка расходов, которые подходят для возмещения международного НДС</span><span class="sxs-lookup"><span data-stu-id="55845-143">Process expenses that are eligible for international VAT recovery</span></span>

<span data-ttu-id="55845-144">Арни, член группы обработки бэк-офиса компании Contoso, ответственен за подтверждение, что все необходимые данные для возмещения НДС включены в отчеты о расходах.</span><span class="sxs-lookup"><span data-stu-id="55845-144">Arnie, a member of Contoso's back-office processing team, is responsible for confirming that all the required information for VAT recovery is included on expense reports.</span></span> <span data-ttu-id="55845-145">Он открывает страницу **Возврат налоговых расходов** и выбирает отчет о расходах, который отправила Нэнси.</span><span class="sxs-lookup"><span data-stu-id="55845-145">He opens the **Expense tax recovery** page and selects the expense report that Nancy submitted.</span></span> <span data-ttu-id="55845-146">Арни проверяет, что все необходимые чеки приложены и что были введены правильные коды налоговой группы номенклатур и налога.</span><span class="sxs-lookup"><span data-stu-id="55845-146">Arnie verifies that all the required receipts are attached, and that the correct sales tax group and item sales tax codes were entered.</span></span>

<span data-ttu-id="55845-147">Когда Арни получает бумажные чеков от Нэнси, он проверяет бумажные чеки по цифровым чекам и затем изменяет статус отчета о расходах на **Готово для возмещения**.</span><span class="sxs-lookup"><span data-stu-id="55845-147">When Arnie receives the paper receipts from Nancy, he verifies the paper receipts against the digital receipts and then changes the status of the expense report to **Ready for recovery**.</span></span>

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a><span data-ttu-id="55845-148">Отправьте данные по возмещения НДС на исполнение сторонним поставщикам для международного возврата</span><span class="sxs-lookup"><span data-stu-id="55845-148">Send VAT recovery data to the third-party vendor to file international recovery returns</span></span>

<span data-ttu-id="55845-149">Когда Арни готов отправить информацию отчета о расходах на исполнение сторонним поставщикам, которые подадут на возвраты возмещения НДС, он открывает страницу **Возврат налоговых расходов**.</span><span class="sxs-lookup"><span data-stu-id="55845-149">When Arnie is ready to send the expense report data to the third-party vendor that will file the VAT recovery returns, he opens the **Expense tax recovery** page.</span></span> <span data-ttu-id="55845-150">Он фильтрует страницу для отображения на ней только отчетов о расходах, помеченные как **Готово для возмещения**.</span><span class="sxs-lookup"><span data-stu-id="55845-150">He filters the page so that it shows only the expense reports that are marked as **Ready for recovery**.</span></span> <span data-ttu-id="55845-151">Затем Арни выбирает **Файл** &gt; **Экспорт в Excel**.</span><span class="sxs-lookup"><span data-stu-id="55845-151">Arnie then selects **File** &gt; **Export to Excel**.</span></span> <span data-ttu-id="55845-152">Данные по НДС из отчетов о расходах экспортируются в лист Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="55845-152">The VAT information from the expense reports is exported to a Microsoft Excel worksheet.</span></span> <span data-ttu-id="55845-153">Арни отправляет этот лист на исполнение сторонним поставщикам и включает сообщение о том, что бумажные чеки были отправлены курьером.</span><span class="sxs-lookup"><span data-stu-id="55845-153">Arnie submits this worksheet to the third-party vendor and includes a message that states that the paper receipts have been sent by courier.</span></span>

## <a name="process-expenses-for-domestic-vat-recovery"></a><span data-ttu-id="55845-154">Обработка расходы для возмещения местного НДС</span><span class="sxs-lookup"><span data-stu-id="55845-154">Process expenses for domestic VAT recovery</span></span>

<span data-ttu-id="55845-155">Арни должен проверить, что проводки отчета о расходах применимы для возмещения НДС, а цифровые чеки прикреплены к отчетам.</span><span class="sxs-lookup"><span data-stu-id="55845-155">Arnie must verify that the expense report transactions are eligible for VAT recovery, and that the digital receipts are attached to the reports.</span></span> <span data-ttu-id="55845-156">Для запуска обработки подходящие расходов для локального возмещения Арни открывает страницу **Возврат налоговых расходов** и выбирает отчет о расходах, который требует проверки.</span><span class="sxs-lookup"><span data-stu-id="55845-156">To start to process eligible expenses for domestic recovery, Arnie opens the **Expense tax recovery** page and selects the expense report that requires verification.</span></span> <span data-ttu-id="55845-157">Он проверяет, что чеки выданы на имя компании, а не на имя сотрудника.</span><span class="sxs-lookup"><span data-stu-id="55845-157">He verifies that receipts are in the name of the company instead of the employee.</span></span> <span data-ttu-id="55845-158">Для возмещения НДС чеки должны быть на имя компании.</span><span class="sxs-lookup"><span data-stu-id="55845-158">For VAT recovery, receipts must be in the name of the company.</span></span> <span data-ttu-id="55845-159">Arnie затем подтверждает, что правильные налоговую группу и налоговые коды номенклатур применены.</span><span class="sxs-lookup"><span data-stu-id="55845-159">Arnie then confirms that the correct sales tax group and item sales tax codes were applied.</span></span>

<span data-ttu-id="55845-160">Когда Арни получает бумажные чеки, он изменяет статус отчета о расходах на **Готово для возмещения**.</span><span class="sxs-lookup"><span data-stu-id="55845-160">When Arnie receives the paper receipts, he changes the status of the expense report to **Ready for recovery**.</span></span> <span data-ttu-id="55845-161">Затем он может подать документы на возврат в соответствующий налоговый орган.</span><span class="sxs-lookup"><span data-stu-id="55845-161">He can then file the return with the appropriate tax authority.</span></span> <span data-ttu-id="55845-162">В этом случае соответствующий налоговый орган в США — налоговое ведомство (IRS).</span><span class="sxs-lookup"><span data-stu-id="55845-162">In this case, the appropriate tax authority in the US is the Internal Revenue Service (IRS).</span></span>
