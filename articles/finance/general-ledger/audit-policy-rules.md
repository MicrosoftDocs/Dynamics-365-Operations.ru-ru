---
title: Правила политики аудита
description: Для оценки отчетов по расходам, накладных поставщиков и заказов на покупку в соответствии на предмет соответствия созданным правилам политики можно использовать политики аудита. Все правила, связанные с политиками аудита, применяются в пакетном режиме в соответствии с заданным графиком.  Каждое правило политики представляет собой экземпляр типа правила политики. Для каждого типа правила политики одновременно может быть активно только одно правило политики.
author: ryansandness
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: de6406029aa88424863dd9a47505f5b3ad27f237
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179558"
---
# <a name="audit-policy-rules"></a><span data-ttu-id="92bfd-106">Правила политики аудита</span><span class="sxs-lookup"><span data-stu-id="92bfd-106">Audit policy rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="92bfd-107">Для оценки отчетов по расходам, накладных поставщиков и заказов на покупку в соответствии на предмет соответствия созданным правилам политики можно использовать политики аудита.</span><span class="sxs-lookup"><span data-stu-id="92bfd-107">You can use audit policies to evaluate expense reports, vendor invoices, and purchase orders to make sure that they comply with policy rules that you create.</span></span> <span data-ttu-id="92bfd-108">Все правила, связанные с политиками аудита, применяются в пакетном режиме в соответствии с заданным графиком.</span><span class="sxs-lookup"><span data-stu-id="92bfd-108">All of the rules that are associated with an audit policy are run in batch mode, according to a schedule that you specify.</span></span>  <span data-ttu-id="92bfd-109">Каждое правило политики представляет собой экземпляр типа правила политики.</span><span class="sxs-lookup"><span data-stu-id="92bfd-109">Each policy rule is an instance of a policy rule type.</span></span> <span data-ttu-id="92bfd-110">Для каждого типа правила политики одновременно может быть активно только одно правило политики.</span><span class="sxs-lookup"><span data-stu-id="92bfd-110">For each policy rule type, only one policy rule can be active at a time.</span></span> 

<a name="queries-and-query-types"></a><span data-ttu-id="92bfd-111">Запросы и типы запросов</span><span class="sxs-lookup"><span data-stu-id="92bfd-111">Queries and query types</span></span>
-----------------------

<span data-ttu-id="92bfd-112">При создании правила политики аудита необходимо сначала выбрать тип правила политики.</span><span class="sxs-lookup"><span data-stu-id="92bfd-112">When you create an audit policy rule, you first select a policy rule type.</span></span> <span data-ttu-id="92bfd-113">Тип правила политики определяет запрос репозитория прикладных объектов (AOT), который будет использоваться в качестве отправной точки для создания правила политики.</span><span class="sxs-lookup"><span data-stu-id="92bfd-113">The policy rule type specifies the Application Object Tree (AOT) query to use as the starting point for creating the policy rule.</span></span> <span data-ttu-id="92bfd-114">Он также определяет тип запроса, который будет использоваться для правила политики.</span><span class="sxs-lookup"><span data-stu-id="92bfd-114">It also specifies the query type to use for the policy rule.</span></span> <span data-ttu-id="92bfd-115">Запрос определяет документ-источник, который будет оцениваться с помощью правила политики.</span><span class="sxs-lookup"><span data-stu-id="92bfd-115">The query determines the source document that the policy rule evaluates.</span></span> <span data-ttu-id="92bfd-116">Также он определяет поля в документе-источнике, которые идентифицируют юридическое лицо и дату, используемую при выборе документов для аудита.</span><span class="sxs-lookup"><span data-stu-id="92bfd-116">It also specifies the fields in the source document that identify both the legal entity and the date to use when documents are selected for audit.</span></span> <span data-ttu-id="92bfd-117">От типа запроса зависят поля по умолчанию на странице запроса и на странице правил политики аудита.</span><span class="sxs-lookup"><span data-stu-id="92bfd-117">The query type controls the default fields in the query page and in the Audit policy rule page.</span></span> <span data-ttu-id="92bfd-118">В следующей таблице показаны типы запросов, предусмотренные для правил политики аудита.</span><span class="sxs-lookup"><span data-stu-id="92bfd-118">The following table shows the query types that are available for audit policy rules.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="92bfd-119">Тип запроса</span><span class="sxs-lookup"><span data-stu-id="92bfd-119">Query type</span></span></th>
<th><span data-ttu-id="92bfd-120">Назначение</span><span class="sxs-lookup"><span data-stu-id="92bfd-120">Purpose</span></span></th>
<th><span data-ttu-id="92bfd-121">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="92bfd-121">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="92bfd-122">Условный</span><span class="sxs-lookup"><span data-stu-id="92bfd-122">Conditional</span></span></td>
<td><span data-ttu-id="92bfd-123">Оценка атрибутов документа-источника относительно заданных значений.</span><span class="sxs-lookup"><span data-stu-id="92bfd-123">Evaluate source document attributes against specified values.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92bfd-124">Агрегированное</span><span class="sxs-lookup"><span data-stu-id="92bfd-124">Aggregate</span></span></td>
<td><span data-ttu-id="92bfd-125">Оценка нескольких документов-источников или строк документов-источников относительно правила политики путем агрегирования числовых значений.</span><span class="sxs-lookup"><span data-stu-id="92bfd-125">Evaluate multiple source documents or source document lines against a policy rule by aggregating numeric values.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="92bfd-126">Образец</span><span class="sxs-lookup"><span data-stu-id="92bfd-126">Sampling</span></span></td>
<td><span data-ttu-id="92bfd-127">Случайный выбор заданного процента документов-источников для оценки на предмет нарушений политики.</span><span class="sxs-lookup"><span data-stu-id="92bfd-127">Randomly select a specified percentage of the source documents to evaluate for policy violations.</span></span></td>
<td><span data-ttu-id="92bfd-128">При выборе этого варианта используйте страницу Правило политики аудита для указания процента документов, случайным образом выбираемых для аудита.</span><span class="sxs-lookup"><span data-stu-id="92bfd-128">When you select this option, use the Audit policy rule page to specify the percentage of documents to randomly select for audit.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92bfd-129">Дубликат</span><span class="sxs-lookup"><span data-stu-id="92bfd-129">Duplicate</span></span></td>
<td><span data-ttu-id="92bfd-130">Оценка документов-источников на предмет наличия в них дублирующихся записей в заданных полях.</span><span class="sxs-lookup"><span data-stu-id="92bfd-130">Evaluate source documents to determine whether they contain duplicate entries in specified fields.</span></span></td>
<td><span data-ttu-id="92bfd-131">При выборе этого варианта в используйте страницу Правило политики аудита для указания числа дней, добавляемого в начало диапазона дат для выбора документов при оценке документов на предмет дублирующихся записей.</span><span class="sxs-lookup"><span data-stu-id="92bfd-131">When you select this option, use the Audit policy rule page to specify the number of days to add to the start of the document selection date range when documents are evaluated for duplicate entries.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="92bfd-132">Поиск по списку</span><span class="sxs-lookup"><span data-stu-id="92bfd-132">List search</span></span></td>
<td><span data-ttu-id="92bfd-133">Оценка документов-источников для конкретных объектов.</span><span class="sxs-lookup"><span data-stu-id="92bfd-133">Evaluate source documents for specific entities.</span></span></td>
<td><span data-ttu-id="92bfd-134">Корневой документ запроса определяет документ, аудит которого проводится.</span><span class="sxs-lookup"><span data-stu-id="92bfd-134">The root document of the query defines the document that is being audited.</span></span> <span data-ttu-id="92bfd-135">Запрос должен быть запросом списка, который включает ссылку на таблицу dirpartytable.</span><span class="sxs-lookup"><span data-stu-id="92bfd-135">The query must be a list query that includes a reference to the dirpartytable table.</span></span> <span data-ttu-id="92bfd-136">Этот вариант можно использовать только со следующими запросами AOT:</span><span class="sxs-lookup"><span data-stu-id="92bfd-136">This option can be used only with the following AOT queries:</span></span>
<ul>
<li><span data-ttu-id="92bfd-137"><span class="ui">AuditPolicyExpenseList</span> (Сотрудники, отслеживаемые в отчете о расходах)</span><span class="sxs-lookup"><span data-stu-id="92bfd-137"><span class="ui">AuditPolicyExpenseList</span> (Expense report monitored employees)</span></span></li>
<li><span data-ttu-id="92bfd-138"><span class="ui">AuditPolicyPurchList</span> (Поставщики, отслеживаемые в заказе на покупку)</span><span class="sxs-lookup"><span data-stu-id="92bfd-138"><span class="ui">AuditPolicyPurchList</span> (Purchase order monitored vendors)</span></span></li>
<li><span data-ttu-id="92bfd-139"><span class="ui">AuditPolicyVendInvoiceList</span> (Поставщики, отслеживаемые в накладной поставщика)</span><span class="sxs-lookup"><span data-stu-id="92bfd-139"><span class="ui">AuditPolicyVendInvoiceList</span> (Vendor invoice monitored vendors)</span></span></li>
</ul>
<span data-ttu-id="92bfd-140">При выборе этого варианта необходимо указать контролируемые объекты на странице Правило политики аудита.</span><span class="sxs-lookup"><span data-stu-id="92bfd-140">When you select this option, specify the monitored entities in the Audit policy rule page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="92bfd-141">Поиск по ключевым словам</span><span class="sxs-lookup"><span data-stu-id="92bfd-141">Keyword search</span></span></td>
<td><span data-ttu-id="92bfd-142">Оценка документов-источников на предмет того, содержат ли они определенные слова.</span><span class="sxs-lookup"><span data-stu-id="92bfd-142">Evaluate source documents to determine whether they contain certain words.</span></span></td>
<td><span data-ttu-id="92bfd-143">При выборе этого варианта введите слова, которые искать, на странице Правило политики аудита.</span><span class="sxs-lookup"><span data-stu-id="92bfd-143">When you select this option, enter the words to look for in the Audit policy rule page.</span></span> <span data-ttu-id="92bfd-144">Страница Правило политики аудита также включает параметры, которые позволяют указать таблицы и поля, оцениваемые на предмет вхождения введенных слов.</span><span class="sxs-lookup"><span data-stu-id="92bfd-144">The Audit policy rule page also includes options that let you specify the tables and fields to evaluate for the words you entered.</span></span></td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a><span data-ttu-id="92bfd-145">Общие параметры</span><span class="sxs-lookup"><span data-stu-id="92bfd-145">Common parameters</span></span>
<span data-ttu-id="92bfd-146">Во всех правилах политики для определенной политики аудита используются одни и те же пакетные параметры и один и тот же диапазон дат для выбора документов.</span><span class="sxs-lookup"><span data-stu-id="92bfd-146">All of the policy rules for a particular audit policy share the same batch parameters and the same document selection date range.</span></span> <span data-ttu-id="92bfd-147">Эти параметры задаются для политики в странице Дополнительные параметры.</span><span class="sxs-lookup"><span data-stu-id="92bfd-147">These parameters are specified for the policy in the Additional options page.</span></span>



<a name="additional-resources"></a><span data-ttu-id="92bfd-148">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="92bfd-148">Additional resources</span></span>
--------

<span data-ttu-id="92bfd-149">[Нарушения политики аудита и соответствующие обращения](audit-policy-violations-cases.md)
[пределение политик аудита для документов-источников](tasks/define-audit-policies-source-documents.md)</span><span class="sxs-lookup"><span data-stu-id="92bfd-149">[Audit policy violations and cases](audit-policy-violations-cases.md)
[Define audit policies for source documents](tasks/define-audit-policies-source-documents.md)</span></span>


