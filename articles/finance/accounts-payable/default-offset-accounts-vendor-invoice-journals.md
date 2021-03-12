---
title: Корреспондентские счета по умолчанию для журналов накладных поставщиков и утверждения накладных
description: Этот раздел поможет решить, где следует назначать счета по умолчанию для журналов накладных.
author: abruer
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3b2ad808d5008d9a4b2d3ee975d15fa1ee13ed7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003502"
---
# <a name="default-offset-accounts-for-vendor-invoice-and-invoice-approval-journals"></a><span data-ttu-id="ec49b-103">Корреспондентские счета по умолчанию для журналов накладных поставщиков и утверждения накладных</span><span class="sxs-lookup"><span data-stu-id="ec49b-103">Default offset accounts for vendor invoice and invoice approval journals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec49b-104">Корр. счета по умолчанию используются на следующих страницах журналов накладных поставщика:</span><span class="sxs-lookup"><span data-stu-id="ec49b-104">Default offset accounts are used on the following vendor invoice journal pages:</span></span>

-   <span data-ttu-id="ec49b-105">Журнал накладных</span><span class="sxs-lookup"><span data-stu-id="ec49b-105">Invoice journal</span></span>
-   <span data-ttu-id="ec49b-106">Журнал утверждения накладных</span><span class="sxs-lookup"><span data-stu-id="ec49b-106">Invoice approval journal</span></span>

<span data-ttu-id="ec49b-107">Используйте следующую таблицу, чтобы решить, где следует назначать счета по умолчанию для журналов накладных.</span><span class="sxs-lookup"><span data-stu-id="ec49b-107">Use the following table to help decide where you should assign default accounts for invoice journals.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ec49b-108">Настройте счета по умолчанию здесь</span><span class="sxs-lookup"><span data-stu-id="ec49b-108">Set up default accounts here</span></span></th>
<th><span data-ttu-id="ec49b-109">Где предоставляются счета по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ec49b-109">Where default accounts are provided</span></span></th>
<th><span data-ttu-id="ec49b-110">Как этот вариант влияет на обработку</span><span class="sxs-lookup"><span data-stu-id="ec49b-110">How this option affects processing</span></span></th>
<th><span data-ttu-id="ec49b-111">Когда вы должны использовать этот вариант</span><span class="sxs-lookup"><span data-stu-id="ec49b-111">When you should use this option</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ec49b-112"><strong>Группа поставщиков</strong> — настройте корреспондентские счета по умолчанию для групп поставщиков на странице <strong>Настройка счета по умолчанию</strong>, которую можно открыть со страницы <strong>Группы поставщиков</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec49b-112"><strong>Vendor group</strong> – Set up default offset accounts for vendor groups on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendor groups</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="ec49b-113">Счет поставщика</span><span class="sxs-lookup"><span data-stu-id="ec49b-113">Vendor account</span></span></li>
<li><span data-ttu-id="ec49b-114">Записи журнала для счетов поставщика в группе поставщиков, если счета по умолчанию не указаны для счетов поставщика.</span><span class="sxs-lookup"><span data-stu-id="ec49b-114">Journal entries for vendor accounts in the vendor group, if default accounts aren’t specified for vendor accounts</span></span></li>
</ul></td>
<td><span data-ttu-id="ec49b-115">Корреспондентские счета по умолчанию для групп поставщиков отображаются как корреспондентские счета по умолчанию для поставщиков на странице <strong>Настройка счета по умолчанию</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec49b-115">The default offset accounts for vendor groups are shown as default offset accounts for vendors on the <strong>Default account setup</strong> page.</span></span> <span data-ttu-id="ec49b-116">Вы можете открыть эту страницу со страницы списка <strong>Все поставщики</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec49b-116">You can open this page from the <strong>All vendors</strong> list page.</span></span></td>
<td><span data-ttu-id="ec49b-117">Используйте этот вариант, если вы обычно оплачиваете вещи одного типа от этих же групп поставщиков с течением времени.</span><span class="sxs-lookup"><span data-stu-id="ec49b-117">Use this option if you typically pay for the same types of things from the same vendor groups over time.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec49b-118"><strong>Счет поставщика</strong> — настройте счета по умолчанию для счетов поставщиков на странице <strong>Настройка счета по умолчанию</strong>, которую можно открыть со страницы <strong>Поставщики</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec49b-118"><strong>Vendor account</strong> – Set up default accounts for vendor accounts on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendors</strong> page.</span></span></td>
<td><span data-ttu-id="ec49b-119">Записи журнала для счета поставщика</span><span class="sxs-lookup"><span data-stu-id="ec49b-119">Journal entries for the vendor account</span></span></td>
<td><span data-ttu-id="ec49b-120">Корр. счета по умолчанию для счетов поставщика отображаются как корр. счета по умолчанию для записей журнала для счета поставщика.</span><span class="sxs-lookup"><span data-stu-id="ec49b-120">The default offset accounts for vendor accounts are shown as default offset accounts for journal entries for the vendor account.</span></span></td>
<td><span data-ttu-id="ec49b-121">Используйте этот вариант, если вы обычно оплачиваете вещи одного типа от этих же поставщиков с течением времени.</span><span class="sxs-lookup"><span data-stu-id="ec49b-121">Use this option if you typically pay for the same types of things from the same vendors over time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec49b-122"><strong>Имена журналов</strong> — настройте корреспондентские счета по умолчанию для журналов на странице <strong>Имена журналов</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec49b-122"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="ec49b-123">Выбор вариант <strong>Фиксированный корр. счет</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec49b-123">Select the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="ec49b-124">Обратите внимание, что вы не можете указать корреспондентские счета по умолчанию для имен журналов, если тип журнала для имен журналов имеет значение <strong>Реестр накладных</strong> или <strong>Утверждение</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec49b-124">Note that you can&#39;t specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="ec49b-125">Заголовок журнала, в котором используется наименование журнала</span><span class="sxs-lookup"><span data-stu-id="ec49b-125">Journal header that uses the journal name</span></span></li>
<li><span data-ttu-id="ec49b-126">Записи журнала в журналах, в которых используется наименование журнала</span><span class="sxs-lookup"><span data-stu-id="ec49b-126">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="ec49b-127">Если установлен флажок <strong>Фиксированный корр. счет</strong> на странице <strong>Имена журналов</strong>, корр. счет для наименования журнала переопределяет корр. счет для корр.счеты по умолчанию для поставщика или группы поставщиков.</span><span class="sxs-lookup"><span data-stu-id="ec49b-127">If the <strong>Fixed offset account</strong> option on the <strong>Journal names</strong> page is selected, the offset account for the journal name overrides the default offset account for the vendor or vendor group.</span></span></td>
<td><span data-ttu-id="ec49b-128">Используйте этот параметр для настройки журналов для конкретных затрат и расходов, которые отнесены к конкретным счетам, независимо от поставщика или группы поставщиков, к которой принадлежит поставщик.</span><span class="sxs-lookup"><span data-stu-id="ec49b-128">Use this option to set up journals for specific costs and expenses that are charged to specific accounts, regardless of the vendor or the vendor group that the vendor belongs to.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec49b-129"><strong>Имена журналов</strong> — настройте корреспондентские счета по умолчанию для журналов на странице <strong>Имена журналов</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec49b-129"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="ec49b-130">Снимите флажок <strong>Фиксированный корр. счет</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec49b-130">Clear the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="ec49b-131">Обратите внимание, что вы не можете указать корреспондентские счета по умолчанию для имен журналов, если тип журнала для имен журналов имеет значение <strong>Реестр накладных</strong> или <strong>Утверждение</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec49b-131">Note that you can&#39;t specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="ec49b-132">Заголовок журнала</span><span class="sxs-lookup"><span data-stu-id="ec49b-132">Journal header</span></span></li>
<li><span data-ttu-id="ec49b-133">Записи журнала в журналах, в которых используется наименование журнала</span><span class="sxs-lookup"><span data-stu-id="ec49b-133">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="ec49b-134">Эти записи по умолчанию используются на страницах заголовка журнала, а корр. счет на странице заголовка журнала используется как запись по умолчанию на страницах ваучера журнала.</span><span class="sxs-lookup"><span data-stu-id="ec49b-134">These default entries are used on journal header pages, and the offset account on the journal header page is used as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="ec49b-135">Счета по умолчанию со страницы <strong>Имена журналов </strong>используются только в том случае, если не настроены счета по умолчанию для счета поставщика.</span><span class="sxs-lookup"><span data-stu-id="ec49b-135">Default accounts from the <strong>Journal names </strong>page are used only if default accounts aren’t set up for the vendor account.</span></span></td>
<td><span data-ttu-id="ec49b-136">Используйте этот параметр, чтобы настроить счета по умолчанию, которые используются, если не назначен корр. счет поставщика по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ec49b-136">Use this option to set up default accounts that are used when a default vendor offset account isn&#39;t assigned.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec49b-137"><strong>Заголовок журнала</strong> — Настройте использование корр. счета по умолчанию для журнала в качестве записи по умолчанию на страницах ваучера журнала.</span><span class="sxs-lookup"><span data-stu-id="ec49b-137"><strong>Journal header</strong> – Set up a default offset account for a journal as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="ec49b-138">Обратите внимание, что вы не можете указать корреспондентские счета по умолчанию для заголовка журнала, если тип журнала для имен журналов имеет значение <strong>Реестр накладных</strong> или <strong>Утверждение</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec49b-138">Note that you can&#39;t specify default offset accounts on the journal header if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><span data-ttu-id="ec49b-139">Записи журнала</span><span class="sxs-lookup"><span data-stu-id="ec49b-139">Journal entries in the journal</span></span></td>
<td><span data-ttu-id="ec49b-140">Корр. счет по умолчанию для журнала используется а качестве записи по умолчанию на страницах ваучера журнала.</span><span class="sxs-lookup"><span data-stu-id="ec49b-140">The default offset account for a journal is used as the default entry on the journal voucher pages.</span></span></td>
<td><span data-ttu-id="ec49b-141">Используйте этот параметр, чтобы ускорить ввод данных, если большинство записей в журнале имеют один и тот же корр. счет.</span><span class="sxs-lookup"><span data-stu-id="ec49b-141">Use this option to help speed up data entry if most entries in a journal have the same offset account.</span></span></td>
</tr>
</tbody>
</table>





