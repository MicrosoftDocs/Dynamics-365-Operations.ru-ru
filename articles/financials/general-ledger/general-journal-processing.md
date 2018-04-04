---
title: "Обработка общего журнала"
description: "Эта статья описывает возможности в Microsoft Dynamics 365 for Finance and Operations, которые могут помочь выполнить обработку общего журнала легче, и которое также может помочь гарантировать, что правильные данные отражаются, и внутренний контроль не скомпрометирован."
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: eb46613f805999753c2ab73ffb91a6fdae04c68e
ms.contentlocale: ru-ru
ms.lasthandoff: 03/26/2018

---

# <a name="general-journal-processing"></a><span data-ttu-id="a18ce-103">Обработка общего журнала</span><span class="sxs-lookup"><span data-stu-id="a18ce-103">General journal processing</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a18ce-104">Эта статья описывает возможности в Microsoft Dynamics 365 for Finance and Operations, которые могут помочь выполнить обработку общего журнала легче, и которое также может помочь гарантировать, что правильные данные отражаются, и внутренний контроль не скомпрометирован.</span><span class="sxs-lookup"><span data-stu-id="a18ce-104">This articles describes capabilities in Microsoft Dynamics 365 for Finance and Operations that can help make general journal processing easier, and that can also help guarantee that correct data is captured and internal control isn't compromised.</span></span>  

<span data-ttu-id="a18ce-105">Наименования журналов</span><span class="sxs-lookup"><span data-stu-id="a18ce-105">Journal names</span></span>

<span data-ttu-id="a18ce-106">Одна из самых важных областей, которую нужно настроить, это имена журнала.</span><span class="sxs-lookup"><span data-stu-id="a18ce-106">One of the most important areas to set up is journal names.</span></span> <span data-ttu-id="a18ce-107">Рекомендуется определить специфические имена журналов для каждой цели, такой как внутрихолдинговый, корректировка начисления и исправление ошибки.</span><span class="sxs-lookup"><span data-stu-id="a18ce-107">It's a good idea to define specific journal names for each purpose, such as intercompany, accrual adjustment, and error correction.</span></span> <span data-ttu-id="a18ce-108">Вы можете подогнать каждое имя журнала для того, чтобы помочь сделать ввод данных для каждой цели легким и безопасным.</span><span class="sxs-lookup"><span data-stu-id="a18ce-108">You can tailor each journal name to help make data entry for each purpose easy and secure.</span></span> 

<span data-ttu-id="a18ce-109">На странице **Имена журналов**, вы можете настроить следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="a18ce-109">On the **Journal names** page, you can set up the following elements:</span></span>

-   <span data-ttu-id="a18ce-110">**Утверждение workflow-процесса** — для того, чтобы увеличить внутренний контроль, определите workflow-процессы журнала, которые устанавливают пределы материальности для шагов обзора и утверждения, основанные на таких критериях, как полная сумма дебета.</span><span class="sxs-lookup"><span data-stu-id="a18ce-110">**Workflow approval** – To increase internal control, define journal workflows that establish materiality limits for review and approval steps, based on criteria such as total debit amount.</span></span> <span data-ttu-id="a18ce-111">Вы настроили workflow-процессы для общих журналов на странице **Workflow-процессы главной книги**.</span><span class="sxs-lookup"><span data-stu-id="a18ce-111">You set up workflows for the general journals on the** General ledger workflows** page.</span></span>
-   <span data-ttu-id="a18ce-112">**Значения по умолчанию** — выберите значения по умолчанию для корр. счетов, валюты, и финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="a18ce-112">**Default values** – Select default values for offset accounts, currency, and financial dimensions.</span></span>
-   <span data-ttu-id="a18ce-113">**Проверка журнала** — вы можете настроить ограничения на тип компании и счета, и также на значения сегмента.</span><span class="sxs-lookup"><span data-stu-id="a18ce-113">**Journal control** – You can set up restrictions on the company and account type, and also the segment values.</span></span> 

<span data-ttu-id="a18ce-114">**Примеры**</span><span class="sxs-lookup"><span data-stu-id="a18ce-114">**Examples**</span></span>

<span data-ttu-id="a18ce-115">Имя журнала может использоваться только для корректировок.</span><span class="sxs-lookup"><span data-stu-id="a18ce-115">A journal name can be used only for adjustments.</span></span> <span data-ttu-id="a18ce-116">В этом случае, вы можете указать, что только тип счета **книга учета** действителен по всем компаниям.</span><span class="sxs-lookup"><span data-stu-id="a18ce-116">In this case, you can specify that only the **Ledger** account type is valid across all companies.</span></span> <span data-ttu-id="a18ce-117">[![Типы счета управления журналом](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span><span class="sxs-lookup"><span data-stu-id="a18ce-117">[![Journal control account types](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span></span>

<span data-ttu-id="a18ce-118">Имя журнала можно использовать только для специфического сегмента или для диапазона для счетов ГК.</span><span class="sxs-lookup"><span data-stu-id="a18ce-118">A journal name can be used only for a specific segment or for a range for main accounts.</span></span> <span data-ttu-id="a18ce-119">[![Сегмент управления журналом](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span><span class="sxs-lookup"><span data-stu-id="a18ce-119">[![Journal control segment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span></span>

<span data-ttu-id="a18ce-120">Параметр **Автоматическое реверсирование** доступен в общих журналах.</span><span class="sxs-lookup"><span data-stu-id="a18ce-120">The **Automatic reversal** option is available in general journals.</span></span> <span data-ttu-id="a18ce-121">Например, вы имеете регулировку начисления, где фактический документ пока не был обработан, как показано в следующей иллюстрации.</span><span class="sxs-lookup"><span data-stu-id="a18ce-121">For example, you have an accrual adjustment where the actual document hasn't yet been processed, as shown in the following illustration.</span></span>
<span data-ttu-id="a18ce-122">[![Реверсирование общего журнала](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span><span class="sxs-lookup"><span data-stu-id="a18ce-122">[![General journal reversing](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span></span> 

<span data-ttu-id="a18ce-123">Надстройка Microsoft Excel для записи в журнале обеспечивает дополнительный уровень автоматизации и делает ввод данных легче.</span><span class="sxs-lookup"><span data-stu-id="a18ce-123">The Microsoft Excel add-in for journal entry provides an additional level of automation and makes data entry easier.</span></span> <span data-ttu-id="a18ce-124">Действие **Открыть строки в Excel** доступно на страницах **Общий журнал** и **Ваучер журнала**.</span><span class="sxs-lookup"><span data-stu-id="a18ce-124">The **Open lines in Excel** action is available on the **General journal** and **Journal voucher** pages.</span></span> 

<span data-ttu-id="a18ce-125">На странице **Периодические журналы** вы можете настроить повторяющиеся журналы для того, чтобы автоматизировать обработку журнала.</span><span class="sxs-lookup"><span data-stu-id="a18ce-125">On the **Periodic journals** page, you can set up recurring journals to automate journal processing.</span></span> 

<span data-ttu-id="a18ce-126">Вы можете использовать шаблоны ваучера в любое время.</span><span class="sxs-lookup"><span data-stu-id="a18ce-126">You can use voucher templates at any time.</span></span> <span data-ttu-id="a18ce-127">На странице **Общие журналы** действия **Сохранить** и **Выбрать шаблон ваучера** находятся на странице **Ваучер журнала** в разделе **Функции** для строк ваучера.</span><span class="sxs-lookup"><span data-stu-id="a18ce-127">On the **General journals** page, the **Save** and **Select voucher template** actions are found on the **Journal voucher** page, under **Functions** for the voucher lines.</span></span>

## <a name="related-setup"></a><span data-ttu-id="a18ce-128">Связанная настройка</span><span class="sxs-lookup"><span data-stu-id="a18ce-128">Related setup</span></span>
<span data-ttu-id="a18ce-129">Следующая установка не специфична по отношению к общим журналам, но поможет гарантировать, что ввод данных — правильные данные и легко.</span><span class="sxs-lookup"><span data-stu-id="a18ce-129">The following setup isn't specific to general journals, but will help guarantee that data entry is correct data and easy.</span></span>

### <a name="main-account"></a><span data-ttu-id="a18ce-130">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="a18ce-130">Main account</span></span>

<span data-ttu-id="a18ce-131">Настройка счета ГК обеспечивает много вариантов для обработки общего журнала:</span><span class="sxs-lookup"><span data-stu-id="a18ce-131">The main account setup provides many options for general journal processing:</span></span>

-   <span data-ttu-id="a18ce-132">**Требование DC/CR** — используйте этот вариант, если счет ГК ограничен проводками дебета или кредита.</span><span class="sxs-lookup"><span data-stu-id="a18ce-132">**DC/CR requirement** – Use this option if a main account is limited to debit or credit transactions.</span></span> <span data-ttu-id="a18ce-133">Настройка подтверждена когда журнал проверен или разнесен.</span><span class="sxs-lookup"><span data-stu-id="a18ce-133">The setup is verified when a journal is validated or posted.</span></span>
-   <span data-ttu-id="a18ce-134">**Корр. счет по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="a18ce-134">**Default offset account**</span></span>
-   <span data-ttu-id="a18ce-135">**Приостановлено** — приостановите счет КГ для ввода данных по всем компаниям или для специфической компании/юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="a18ce-135">**Suspended** – Suspend a main account for data entry across all companies or for a specific company/legal entities.</span></span>
-   <span data-ttu-id="a18ce-136">**Не разрешать ввод вручную** — предотвратите ручной ввод значения пользователями для счета в журналах.</span><span class="sxs-lookup"><span data-stu-id="a18ce-136">**Do not allow manual entry** – Prevent users from manually entering a value for the account in journals.</span></span>
-   <span data-ttu-id="a18ce-137">**По умолчанию/Проверка валют**</span><span class="sxs-lookup"><span data-stu-id="a18ce-137">**Default/Validate currency**</span></span>
-   <span data-ttu-id="a18ce-138">**Переопределение юридического лица** — эта установка специфическая для определенной компании/юридического лица:</span><span class="sxs-lookup"><span data-stu-id="a18ce-138">**Legal entity override** – This setup is specific to the defined company/legal entity:</span></span>
    -   <span data-ttu-id="a18ce-139">**По умолчанию/Проверить налог**</span><span class="sxs-lookup"><span data-stu-id="a18ce-139">**Default/Validate sales tax**</span></span>
    -   <span data-ttu-id="a18ce-140">**Аналитика по умолчанию** – **Не фиксировано** или **Фиксированное значение**.</span><span class="sxs-lookup"><span data-stu-id="a18ce-140">**Default dimension** – **Not fixed** or **Fixed value**.</span></span> <span data-ttu-id="a18ce-141">**Фиксированное значение** поможет гарантировать что все разноски для этого счета ГК всегда используют любое значение аналитики, которое настроено как **Фиксировано**.</span><span class="sxs-lookup"><span data-stu-id="a18ce-141">**Fixed value** will help guarantee that all postings for this main account always use any dimension value that is set up as **Fixed**.</span></span>
-   <span data-ttu-id="a18ce-142">**Проверка разноски**</span><span class="sxs-lookup"><span data-stu-id="a18ce-142">**Posting validation**</span></span>
    -   <span data-ttu-id="a18ce-143">**Проверка пользователя** — этот вариант контролирует, которые пользователи могут разносить в счет ГК.</span><span class="sxs-lookup"><span data-stu-id="a18ce-143">**User validation** – This option controls which users are allowed to post to a main account.</span></span>
    -   <span data-ttu-id="a18ce-144">**Проверка типа разноски** — этот вариант контролирует, которые типы разноски разрешены для счета ГК.</span><span class="sxs-lookup"><span data-stu-id="a18ce-144">**Posting type validation** – This option controls which posting types are allowed for a main account.</span></span>

### <a name="accounting-structures-and-advanced-rules-structures"></a><span data-ttu-id="a18ce-145">Структуры учета и расширенные структуры правил</span><span class="sxs-lookup"><span data-stu-id="a18ce-145">Accounting structures and advanced rules structures</span></span>

<span data-ttu-id="a18ce-146">Структуры учета и расширенные структуры правил очень важны, чтобы гарантировать, что данные, которые необходимо для финансовой отчетности и отслеживания производительности, захвачены во время обработки общего журнала и любой документации.</span><span class="sxs-lookup"><span data-stu-id="a18ce-146">Accounting structures and advanced rules structures are extremely important for guaranteeing that the data that is required for financial reporting and performance tracking is captured during general journal processing and any documentation.</span></span> <span data-ttu-id="a18ce-147">Структуры учета и расширенные структуры правил позволяют настроить впечатления от ввода данных.</span><span class="sxs-lookup"><span data-stu-id="a18ce-147">Accounting structures and advanced rules structures let you tailor the data entry experience.</span></span> <span data-ttu-id="a18ce-148">Вы можете позволить ввод данных только для финансовых аналитик, которые уместны в каждой ситуации, и можете также принудить требование, чтобы обязательные и правильные данные всегда захватывались.</span><span class="sxs-lookup"><span data-stu-id="a18ce-148">You can allow data entry only for financial dimensions that are relevant in each situation, and can also enforce the requirement that mandatory and correct data always be captured.</span></span>

<span data-ttu-id="a18ce-149">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="a18ce-149">For more information, see the following topics:</span></span>
- <span data-ttu-id="a18ce-150">[Планирование: план счетов](plan-chart-of-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="a18ce-150">[Planning: Chart of accounts](plan-chart-of-accounts.md).</span></span> 
- [<span data-ttu-id="a18ce-151">Создание расширенных правил для журналов</span><span class="sxs-lookup"><span data-stu-id="a18ce-151">Create advanced rules for journals</span></span>](tasks/create-advanced-rules-journals.md)
- [<span data-ttu-id="a18ce-152">Создание записи в журнале с помощью шаблона</span><span class="sxs-lookup"><span data-stu-id="a18ce-152">Create a journal entry using a template</span></span>](tasks/create-journal-entry-template.md)
- [<span data-ttu-id="a18ce-153">Создание и проверка журналов</span><span class="sxs-lookup"><span data-stu-id="a18ce-153">Create and validate journals</span></span>](tasks/create-validate-journals.md)
- [<span data-ttu-id="a18ce-154">Учет периодических журналов</span><span class="sxs-lookup"><span data-stu-id="a18ce-154">Post periodic journals</span></span>](tasks/post-periodic-journals.md)
- [<span data-ttu-id="a18ce-155">Обработка журнала распределения ГК</span><span class="sxs-lookup"><span data-stu-id="a18ce-155">Process ledger allocation journal</span></span>](tasks/process-ledger-allocation-journal.md)



