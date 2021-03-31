---
title: Нарушения политики аудита и соответствующие случаи
description: Статья описывает, как обращения аудита создаются из нарушений правил политики аудита. Она также включает информацию о различных способах, которые политики аудита используют для диапазон дат выбора документа.
author: panolte
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 170a27c55f808e11fba047186209a2b126b6a87a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228847"
---
# <a name="audit-policy-violations-and-cases"></a><span data-ttu-id="20c11-104">Нарушения политики аудита и соответствующие случаи</span><span class="sxs-lookup"><span data-stu-id="20c11-104">Audit policy violations and cases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20c11-105">Статья описывает, как обращения аудита создаются из нарушений правил политики аудита.</span><span class="sxs-lookup"><span data-stu-id="20c11-105">The article explains how audit cases are generated from violations of audit policy rules.</span></span> <span data-ttu-id="20c11-106">Она также включает информацию о различных способах, которые политики аудита используют для диапазон дат выбора документа.</span><span class="sxs-lookup"><span data-stu-id="20c11-106">It also includes information about the various ways that audit policies use the document selection date range.</span></span>

<a name="how-audit-cases-are-generated"></a><span data-ttu-id="20c11-107">Как создаются обращения аудита</span><span class="sxs-lookup"><span data-stu-id="20c11-107">How audit cases are generated</span></span>
-----------------------------

<span data-ttu-id="20c11-108">Политики аудита используются для определения отчетов по расходам, заказов на покупку и накладных поставщика, которые не соответствуют бизнес-правилам, определенным и настроенным в качестве правил политики аудита.</span><span class="sxs-lookup"><span data-stu-id="20c11-108">Audit policies are used to identify expense reports, purchase orders, and vendor invoices that don't comply with business rules that you define and configure as audit policy rules.</span></span> 

<span data-ttu-id="20c11-109">Политики аудита выполняются в пакетном режиме.</span><span class="sxs-lookup"><span data-stu-id="20c11-109">Audit policies are run in batch mode.</span></span> <span data-ttu-id="20c11-110">При выполнении политики аудита все правил политики, которые являются частью этой политики, выполняются одновременно.</span><span class="sxs-lookup"><span data-stu-id="20c11-110">When you run an audit policy, all the policy rules that are part of that policy are run at the same time.</span></span>

<span data-ttu-id="20c11-111">Каждое правило политики оценивает комплект документов.</span><span class="sxs-lookup"><span data-stu-id="20c11-111">Each policy rule evaluates a set of documents.</span></span> <span data-ttu-id="20c11-112">Правило политики выбирает документы, которые находятся в требуемом диапазоне дат и соответствуют указанным критериям.</span><span class="sxs-lookup"><span data-stu-id="20c11-112">The policy rule selects documents that are in the document selection date range and that match the specified criteria.</span></span> <span data-ttu-id="20c11-113">Например, одно из правил политик может отбирать отчеты по расходам, в которых упоминаются обеды стоимостью более 50 долларов.</span><span class="sxs-lookup"><span data-stu-id="20c11-113">For example, one policy rule might select expense reports that have meals that exceed 50.00.</span></span> <span data-ttu-id="20c11-114">В другом правиле политики могут отбираться накладные поставщика, подлежащие оплате в пользу определенного поставщика.</span><span class="sxs-lookup"><span data-stu-id="20c11-114">Another policy rule might select vendor invoices that are payable to a specific vendor.</span></span> <span data-ttu-id="20c11-115">Для каждого документа в выбранном наборе создается нарушение.</span><span class="sxs-lookup"><span data-stu-id="20c11-115">For each document that is selected in the set, a violation is generated.</span></span> <span data-ttu-id="20c11-116">Такое нарушение – это запись о том, что определенный документ, например, накладная 12345, не соответствует правилу политики.</span><span class="sxs-lookup"><span data-stu-id="20c11-116">That violation is a record that a particular document, such as invoice 12345, doesn't comply with the policy rule.</span></span> 

<span data-ttu-id="20c11-117">Несколько записей о нарушениях аудита группируются и связываются с обращениями аудита.</span><span class="sxs-lookup"><span data-stu-id="20c11-117">Multiple audit violation records are grouped together and associated with audit cases.</span></span> <span data-ttu-id="20c11-118">По умолчанию обращения для каждой политики аудита группируются по правилу политики аудита.</span><span class="sxs-lookup"><span data-stu-id="20c11-118">By default, cases for each audit policy are grouped by audit policy rule.</span></span> <span data-ttu-id="20c11-119">Если вы предпочитаете, то вы можете выбрать другие критерии группировки путем использования страница **Критерии группировки обращений**.</span><span class="sxs-lookup"><span data-stu-id="20c11-119">If you prefer, you can select other grouping criteria by using the **Case grouping criteria** page.</span></span> <span data-ttu-id="20c11-120">Например, можно сгруппировать заголовки расходов по коду проекта, а накладные поставщика — по счету поставщика.</span><span class="sxs-lookup"><span data-stu-id="20c11-120">For example, you can group expense headers by project ID and vendor invoices by vendor account.</span></span> <span data-ttu-id="20c11-121">В этом случае все нарушения заголовков расходов с одинаковым кодом проекта группируются в одно обращение, и все накладные поставщика с одинаковым счетом поставщика группируются в одно обращение.</span><span class="sxs-lookup"><span data-stu-id="20c11-121">In this case, all expense header violations that have the same project ID will be grouped in the same case, and all vendor invoices that have the same vendor account will be grouped in the same case.</span></span> 

> [!NOTE]
> <span data-ttu-id="20c11-122">Для правил политики аудита, которые основаны на типе запроса **Дубликат**, нарушения не группируются по правилу политики или по критериям, заданным на странице **Критерии группировки обращений**.</span><span class="sxs-lookup"><span data-stu-id="20c11-122">For audit policy rules that are based on a **Duplicate** query type, violations aren't grouped by policy rule or by the criteria that are specified on the **Case grouping criteria** page.</span></span> <span data-ttu-id="20c11-123">Вместо этого они группируются по критериям, которые встроены в правило политики аудита.</span><span class="sxs-lookup"><span data-stu-id="20c11-123">Instead, they are grouped by the criteria that are built into the audit policy rule.</span></span> <span data-ttu-id="20c11-124">Например, если правило политики оценивает отчеты по расходам на наличие двойных расходов с одинаковым кодом получателя платежа и датой, все расходы с одинаковыми значениями в этих полях будут представлять одно обращение.</span><span class="sxs-lookup"><span data-stu-id="20c11-124">For example, if a policy rule evaluates expense reports for duplicate expenses of the same amount, merchant ID, and date, all expenses that have the same values in those fields will be one case.</span></span> <span data-ttu-id="20c11-125">Все расходы которые имеют различные значения, будут отдельным случаем.</span><span class="sxs-lookup"><span data-stu-id="20c11-125">Any expenses that have different values will be a separate case.</span></span>

<span data-ttu-id="20c11-126">После создания обращений аудита они обрабатываются посредством типовых процессов управления обращениями.</span><span class="sxs-lookup"><span data-stu-id="20c11-126">After the audit cases have been generated, they are handled by using the typical processes for case management.</span></span>

## <a name="document-selection-date-ranges"></a><span data-ttu-id="20c11-127">Диапазоны дат выбора документов</span><span class="sxs-lookup"><span data-stu-id="20c11-127">Document selection date ranges</span></span>
<span data-ttu-id="20c11-128">Если политика аудита запущена, все правила политики выбирают документы указанного типа, дата которых находится в диапазоне дат выбора документа.</span><span class="sxs-lookup"><span data-stu-id="20c11-128">When an audit policy is run, each policy rule selects documents of the specified type that have a date that is in the document selection date range.</span></span> <span data-ttu-id="20c11-129">Диапазон дат выбора документа определяется на странице **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="20c11-129">The document selection date range is specified on the **Additional options** page.</span></span> <span data-ttu-id="20c11-130">Многие документы имеют несколько дат, связанных с ними.</span><span class="sxs-lookup"><span data-stu-id="20c11-130">Many documents have more than one date associated with them.</span></span> <span data-ttu-id="20c11-131">Поле даты, которое использует правило политики аудита, указано на странице **Тип правила политики**.</span><span class="sxs-lookup"><span data-stu-id="20c11-131">The date field that the audit policy rule uses is specified on the **Policy rule type** page.</span></span>

<span data-ttu-id="20c11-132">Вот некоторые другие способы, которыми политика аудита использует диапазон дат выбора документа:</span><span class="sxs-lookup"><span data-stu-id="20c11-132">Here are some other ways that an audit policy uses the document selection date range:</span></span>

-   <span data-ttu-id="20c11-133">Политика использует версию каждого правила политики, которое является действующим в последний день диапазона дат выбора документа.</span><span class="sxs-lookup"><span data-stu-id="20c11-133">The policy uses the version of each policy rule that is effective on the last day of the document selection date range.</span></span> <span data-ttu-id="20c11-134">Вы можете осмотреть даты действия для каждого правила политики на странице списка **Политики аудита**.</span><span class="sxs-lookup"><span data-stu-id="20c11-134">You can view the effective dates for each policy rule on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="20c11-135">Политика использует узлы организации, связанные с политикой на последний день диапазона дат выбора документа.</span><span class="sxs-lookup"><span data-stu-id="20c11-135">The policy uses the organization nodes that are associated with the policy on the last day of the document selection date range.</span></span> <span data-ttu-id="20c11-136">Только узлы организации, которые в настоящее время связаны с политикой, отображаются на странице списка **Политики аудита**.</span><span class="sxs-lookup"><span data-stu-id="20c11-136">Only the organization nodes that are currently associated with the policy appear on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="20c11-137">Для правил политики, основанных на типе запроса **Поиск по списку**, политика оценивает документы для отслеживаемых объектов, действующих в последний день диапазона дат выбора документа.</span><span class="sxs-lookup"><span data-stu-id="20c11-137">For policy rules that are based on a **List search** query type, the policy evaluates documents for monitored entities that are effective on the last day of the document selection date range.</span></span>


<span data-ttu-id="20c11-138">Дополнительные сведения см. в разделе [Правила политики аудита](audit-policy-rules.md)</span><span class="sxs-lookup"><span data-stu-id="20c11-138">For more information, see [Audit policy rules](audit-policy-rules.md)</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]