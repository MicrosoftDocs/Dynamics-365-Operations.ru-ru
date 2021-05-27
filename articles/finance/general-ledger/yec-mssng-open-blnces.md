---
title: В закрытии года отсутствуют входящие сальдо
description: В этом разделе описывается, почему входящие сальдо могут отсутствовать при закрытии года и как восстановить эти сальдо, если они отсутствуют.
author: kweekley
ms.date: 05/12/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 045d0bf11b11c9a353858ce3ca82c698dbceea7c
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028583"
---
# <a name="year-end-close-missing-opening-balances"></a><span data-ttu-id="e61ec-103">В закрытии года отсутствуют входящие сальдо</span><span class="sxs-lookup"><span data-stu-id="e61ec-103">Year-end close missing opening balances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e61ec-104">В этом разделе описывается, почему входящие сальдо могут отсутствовать при закрытии года и как восстановить эти сальдо, если они отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="e61ec-104">This topic explains why opening balances might be missing when you close a year, and how to rebuild those balances if they are missing.</span></span>

### <a name="symptom"></a><span data-ttu-id="e61ec-105">Симптом</span><span class="sxs-lookup"><span data-stu-id="e61ec-105">Symptom</span></span>

<span data-ttu-id="e61ec-106">Почему отсутствуют входящие сальдо после выполнения закрытия года в главной книге?</span><span class="sxs-lookup"><span data-stu-id="e61ec-106">Why are there no beginning balances after running the General ledger year-end close?</span></span> 

### <a name="resolution"></a><span data-ttu-id="e61ec-107">Решение</span><span class="sxs-lookup"><span data-stu-id="e61ec-107">Resolution</span></span>

<span data-ttu-id="e61ec-108">Вот что следует проверить, если вы закрыли год в главной книге, а затем создали пробный баланс, в котором не отображаются входящие сальдо на следующий финансовый год.</span><span class="sxs-lookup"><span data-stu-id="e61ec-108">Here are things to check if you've closed a year in General ledger, and then generated a trial balance that doesn't display opening balances for the next fiscal year.</span></span>

<span data-ttu-id="e61ec-109">Если для поля **Отменить предыдущее закрытие** задано значение **Да**, предыдущее закрытие того же финансового года реверсируется.</span><span class="sxs-lookup"><span data-stu-id="e61ec-109">If the **Undo previous close** field is set to **Yes**, the previous year-end close for the same fiscal year is being reversed.</span></span> <span data-ttu-id="e61ec-110">При выполнении процесса реверсирования закрытия года все записи для исходящих и входящих сальдо будут удалены, как если бы год никогда не закрывался.</span><span class="sxs-lookup"><span data-stu-id="e61ec-110">When running a process to reverse the year-end close, all entries for both closing and opening balances will be deleted, as if the year had never been closed.</span></span> <span data-ttu-id="e61ec-111">Также будут удалены ваучеры.</span><span class="sxs-lookup"><span data-stu-id="e61ec-111">The vouchers are also deleted.</span></span> <span data-ttu-id="e61ec-112">Процесс закрытия года не будет выполнен повторно автоматически.</span><span class="sxs-lookup"><span data-stu-id="e61ec-112">The year-end close process will not run again automatically.</span></span> <span data-ttu-id="e61ec-113">Необходимо запустить процесс еще раз, на этот раз изменив значение параметра **Отменить предыдущее закрытие** на **Нет**.</span><span class="sxs-lookup"><span data-stu-id="e61ec-113">You must start the process again, this time updating the **Undo previous close** option to **No**.</span></span>

<span data-ttu-id="e61ec-114">Этот сценарий описывается в разделе вопросов и ответов по закрытию года.</span><span class="sxs-lookup"><span data-stu-id="e61ec-114">This scenario is covered in the year-end close FAQ topic.</span></span> <span data-ttu-id="e61ec-115">Дополнительные сведения см. в разделе [Вопросы и ответы по мероприятиям на конец года](faq-year-end-activities.md).</span><span class="sxs-lookup"><span data-stu-id="e61ec-115">For more information, see [Year-end activities FAQ](faq-year-end-activities.md).</span></span>

### <a name="symptom"></a><span data-ttu-id="e61ec-116">Симптом</span><span class="sxs-lookup"><span data-stu-id="e61ec-116">Symptom</span></span>

<span data-ttu-id="e61ec-117">При выполнении закрытия года для параметра **Отменить предыдущее закрытие** было задано значение **Нет**, но входящие сальдо для моего финансового года по-прежнему не отображаются.</span><span class="sxs-lookup"><span data-stu-id="e61ec-117">I ran year-end close with the **Undo previous close** option set to **No**, and I still do not have opening balances for my fiscal year.</span></span>

### <a name="resolution"></a><span data-ttu-id="e61ec-118">Решение</span><span class="sxs-lookup"><span data-stu-id="e61ec-118">Resolution</span></span>

<span data-ttu-id="e61ec-119">Сначала проверьте статус пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="e61ec-119">First check the status of the batch job.</span></span> <span data-ttu-id="e61ec-120">Закрытие года включает ряд отдельных задач, но наиболее важным шагом является пакетная задача с описанием задачи **Шаг 5.0.0**.</span><span class="sxs-lookup"><span data-stu-id="e61ec-120">Closing a year includes a number of separate tasks, but the most critical step is the batch task with the task description **Step 5.0.0**.</span></span> <span data-ttu-id="e61ec-121">На этом шаге выполняется разноска открывающих проводок и при необходимости закрывающих проводок в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="e61ec-121">Posting the opening transactions, and optionally the closing transactions, to General ledger takes place during this step.</span></span> 

<span data-ttu-id="e61ec-122">[![Список журналов пакетов](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span><span class="sxs-lookup"><span data-stu-id="e61ec-122">[![Batch history list](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span></span>

<span data-ttu-id="e61ec-123">Если этот шаг завершился успешно, но вы не видите входящих сальдо на странице **Запрос пробного баланса** (**Главная книга > Запросы и отчеты > Пробный баланс**), просмотрите результаты пакетного задания закрытия года, чтобы проверить, успешно ли завершен шаг повторного создания сальдо.</span><span class="sxs-lookup"><span data-stu-id="e61ec-123">If this step ended successfully but you don’t see opening balances on the **Trial balance inquiry** page (**General ledger > Inquires and reports > Trial balance**), review the results of the year-end close batch job to see if the Rebuild balances step completed successfully.</span></span>

<span data-ttu-id="e61ec-124">[![Результаты пакетного задания закрытия года](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span><span class="sxs-lookup"><span data-stu-id="e61ec-124">[![Results of year-end close batch job](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span></span>

<span data-ttu-id="e61ec-125">Если по какой-либо причине этот шаг завершился с ошибкой, открывающие (и при необходимости закрывающие) проводки, скорее всего, были успешно разнесены.</span><span class="sxs-lookup"><span data-stu-id="e61ec-125">If this step has failed for any reason, the opening (and optionally closing) transactions were likely posted successfully.</span></span> <span data-ttu-id="e61ec-126">Вы можете проверить, что проводки главной книги были успешно разнесены, с помощью страницы **Запрос проводок по ваучеру**, указав код ваучера и дату, предоставленную в диалоговом окне закрытия года для закрываемого года (**Главная книга > Запросы и отчеты > Проводки по ваучеру**).</span><span class="sxs-lookup"><span data-stu-id="e61ec-126">You can verify that the General ledger transactions were posted successfully using the **Voucher transactions inquiry** page by specifying the voucher number and date provided on the year-end close dialog for the year that you closed, (**General Ledger > Inquiries and reports > Voucher transactions**).</span></span>

<span data-ttu-id="e61ec-127">[![Запрос проводок по ваучеру](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span><span class="sxs-lookup"><span data-stu-id="e61ec-127">[![Voucher transactions inquiry](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span></span>

<span data-ttu-id="e61ec-128">Если имеются открывающие (и при необходимости закрывающие) ваучеры, выполнять закрытие года повторно не требуется.</span><span class="sxs-lookup"><span data-stu-id="e61ec-128">If the opening (and optionally closing) vouchers are present, you don’t need to run the year-end close again.</span></span> <span data-ttu-id="e61ec-129">Вместо этого см. следующий раздел для получения информации о дальнейших действиях.</span><span class="sxs-lookup"><span data-stu-id="e61ec-129">Instead refer to the next section for information about how to move forward.</span></span>

### <a name="symptom"></a><span data-ttu-id="e61ec-130">Симптом</span><span class="sxs-lookup"><span data-stu-id="e61ec-130">Symptom</span></span>

<span data-ttu-id="e61ec-131">Шаг "Повторное создание сальдо" при закрытии года завершился с ошибкой. Мне нужно повторно выполнить весь процесс закрытия года?</span><span class="sxs-lookup"><span data-stu-id="e61ec-131">The “Rebuild balances” step in the year-end close failed, do I need to re-run the entire year-end close process?</span></span>

### <a name="resolution"></a><span data-ttu-id="e61ec-132">Решение</span><span class="sxs-lookup"><span data-stu-id="e61ec-132">Resolution</span></span>

<span data-ttu-id="e61ec-133">Шаг "Повторное создание сальдо" обновляет сальдо главной книги, которые используются при создании запроса пробного баланса.</span><span class="sxs-lookup"><span data-stu-id="e61ec-133">The Rebuild balances step updates the General ledger balances that are used when the Trial balance inquiry is generated.</span></span>  <span data-ttu-id="e61ec-134">Это последний шаг в процессе закрытия года.</span><span class="sxs-lookup"><span data-stu-id="e61ec-134">It is the final step in the year-end close process.</span></span>  <span data-ttu-id="e61ec-135">Если этот шаг является единственным шагом, который завершился с ошибкой, проводки главной книги успешно разнесены.</span><span class="sxs-lookup"><span data-stu-id="e61ec-135">If this step is the only step that failed, the General ledger transactions have posted successfully.</span></span>  <span data-ttu-id="e61ec-136">Вам не требуется выполнять закрытие года повторно.</span><span class="sxs-lookup"><span data-stu-id="e61ec-136">You do not need to run the year-end close again.</span></span> <span data-ttu-id="e61ec-137">Вы можете запустить процесс повторного создания сальдо вручную с помощью страницы **Наборы финансовых аналитик** (**Главная книга > План счетов > Аналитики > Наборы финансовых аналитик**).</span><span class="sxs-lookup"><span data-stu-id="e61ec-137">You can run the process to rebuild the balances manually using the **Financial dimension sets** page (**General ledger > Chart of accounts > Dimensions > Financial dimension sets**).</span></span>

<span data-ttu-id="e61ec-138">[![Кнопка повторного создания сальдо на странице "Наборы финансовых аналитик"](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span><span class="sxs-lookup"><span data-stu-id="e61ec-138">[![Rebuild balances button on Financial dimension sets page](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span></span>

<span data-ttu-id="e61ec-139">Если обработка этого шага занимает много времени, рекомендуется просмотреть рекомендации по наборам финансовых аналитик в разделе [Рекомендации по обновлению наборов финансовых аналитик](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets).</span><span class="sxs-lookup"><span data-stu-id="e61ec-139">If this step takes a long time to process, we recommend reviewing the best practices for financial dimension sets as described in [Best practices for updating Financial dimension sets](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets).</span></span> 

