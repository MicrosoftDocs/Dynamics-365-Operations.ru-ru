---
title: Просмотр записей журнала и проводок
description: Эта статья описывает различные методы, которыми можно посмотреть записи и проводки в журнале
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13031
ms.assetid: 281c7ea6-4dfd-4d1f-994f-c361ee299dbe
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 07774e607abc90951c27100e749645d8a476b6a7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846131"
---
# <a name="view-journal-entries-and-transactions"></a><span data-ttu-id="67479-103">Просмотр записей журнала и проводок</span><span class="sxs-lookup"><span data-stu-id="67479-103">View journal entries and transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67479-104">Эта статья описывает различные методы, которыми можно посмотреть записи и проводки в журнале</span><span class="sxs-lookup"><span data-stu-id="67479-104">This article explains the various ways that you can view journal entries and transactions.</span></span> 

<span data-ttu-id="67479-105">Пользователи, которые хотят просмотреть журналы и проводки, имеют несколько способов получить доступ к данным.</span><span class="sxs-lookup"><span data-stu-id="67479-105">Users who want to view journals and transactions have several ways to access the data.</span></span> <span data-ttu-id="67479-106">Они могут использовать страницы запросов, которые предлагают возможность детализации, или различные параметры отчетов в главной книге.</span><span class="sxs-lookup"><span data-stu-id="67479-106">They can take advantage of inquiry pages that provide drill-down ability, or they can use various report options in the general ledger.</span></span>

## <a name="voucher-transactions"></a><span data-ttu-id="67479-107">Проводки по ваучеру</span><span class="sxs-lookup"><span data-stu-id="67479-107">Voucher transactions</span></span>
<span data-ttu-id="67479-108">**Проводки по ваучеру** — это страница запроса, на которой можно выбрать элементы в различных таблицах и полях для того, чтобы определить критерии для искомых сальдо или проводок.</span><span class="sxs-lookup"><span data-stu-id="67479-108">**Voucher transactions** is an inquiry page where you can select from various tables and fields to specify criteria for the balance or transaction that you're searching for.</span></span> <span data-ttu-id="67479-109">Например, можно просмотреть все проводки за определенную дату или для определенного счета либо все проводки типа **Работа**, которые находятся в определенном слое разноски.</span><span class="sxs-lookup"><span data-stu-id="67479-109">For example, you can view all transactions for a specific date or account, or all transactions of the **Operating** type that are in a specific posting layer.</span></span> <span data-ttu-id="67479-110">По умолчанию на странице отображается номер журнала, ваучер, дата и счет ГК, но можно добавить дополнительные таблицы, поля и критерии для того, чтобы сузить поиск.</span><span class="sxs-lookup"><span data-stu-id="67479-110">By default, the page shows the journal number, voucher, date, and main account, but you can add additional tables, fields, and criteria to narrow down your search.</span></span>

## <a name="audit-trail"></a><span data-ttu-id="67479-111">Аудиторский след</span><span class="sxs-lookup"><span data-stu-id="67479-111">Audit trail</span></span>
<span data-ttu-id="67479-112">**Аудиторский след** — это страница запроса, на которой отображаются типы проводок, описания, авторы проводок и дата создания проводок.</span><span class="sxs-lookup"><span data-stu-id="67479-112">**Audit trail** is an inquiry page that shows the types of transactions, descriptions, who the transactions were created by, and when they were created.</span></span> <span data-ttu-id="67479-113">На странице запроса **Аудиторский след** можно просмотреть проводки по ваучеру.</span><span class="sxs-lookup"><span data-stu-id="67479-113">From the **Audit trail** inquiry page, you can view the voucher transactions.</span></span>

## <a name="financial-reports"></a><span data-ttu-id="67479-114">Финансовые отчеты</span><span class="sxs-lookup"><span data-stu-id="67479-114">Financial reports</span></span>
<span data-ttu-id="67479-115">Проводки ГК также можно изучить и проанализировать, выполнив финансовые отчеты.</span><span class="sxs-lookup"><span data-stu-id="67479-115">You can also explore and analyze general ledger transactions by running financial reports.</span></span> <span data-ttu-id="67479-116">Поскольку дизайн финансовых отчетов может основываться на счетах, аналитиках, категориях счетов или сочетании этих трех параметров, проводки можно просмотреть, выполнив различную детализацию.</span><span class="sxs-lookup"><span data-stu-id="67479-116">Because the design of financial reports can be based on accounts, dimensions, account categories, or a combination of the three, you can view the transactions by drilling down in various ways.</span></span> <span data-ttu-id="67479-117">Если вам требуется больше информации о проводках ГК, вы также можете включить несколько свойств проводки как часть дизайна отчета.</span><span class="sxs-lookup"><span data-stu-id="67479-117">If you require more information for general ledger transactions, you can also include multiple transaction properties as part of the report design.</span></span> <span data-ttu-id="67479-118">Кроме того, если требуется просмотреть проводки, которые составляют сальдо ГК, можно выполнить детализацию до проводок по счету, так же как на странице списка **Пробный баланс**.</span><span class="sxs-lookup"><span data-stu-id="67479-118">Additionally, if you want to see the transactions that make up a general ledger balance, you can drill down to account transactions, just as you can from the **Trial balance** list page.</span></span>

## <a name="ledger-reports"></a><span data-ttu-id="67479-119">Отчеты по главной книге</span><span class="sxs-lookup"><span data-stu-id="67479-119">Ledger reports</span></span>
<span data-ttu-id="67479-120">В дополнение к финансовым отчетам можно использовать следующие отчеты по главной книге для просмотра проводок ГК:</span><span class="sxs-lookup"><span data-stu-id="67479-120">In addition to the financial reports, you can use the following ledger reports to view general ledger transactions:</span></span>

-   <span data-ttu-id="67479-121">**Отчет по аналитике** — в этом отчете отображаются проводки по дню и счету. Также можно просмотреть проводки по аналитике и периоду.</span><span class="sxs-lookup"><span data-stu-id="67479-121">**Dimension statement** – This report shows transactions by day and account, and there are also options to show transactions by dimension and period.</span></span>
-   <span data-ttu-id="67479-122">**Список проводок ГК** — в этом отчете отображаются проводки в валютах проводки, учета и отчетности для счета.</span><span class="sxs-lookup"><span data-stu-id="67479-122">**Ledger transaction list** – This report shows transactions in transaction, accounting, and reporting currencies for an account.</span></span>
-   <span data-ttu-id="67479-123">**Журнал печати** — в этом отчете отображается результат разнесенного журнала.</span><span class="sxs-lookup"><span data-stu-id="67479-123">**Print journal** – This report shows the result of a posted journal.</span></span> <span data-ttu-id="67479-124">Вы можете выполнить отчет по номеру партии журнала или типу журнала либо добавить дополнительные поля.</span><span class="sxs-lookup"><span data-stu-id="67479-124">You can run the report by journal batch number or journal type, or add additional fields.</span></span>
-   <span data-ttu-id="67479-125">**Разнесенные проводки по журналу** — в этом отчете отображаются проводки, которые были разнесены в журнал, сгруппированные по ваучеру.</span><span class="sxs-lookup"><span data-stu-id="67479-125">**Posted transactions by journal** – This report shows the transactions that have been posted to a journal, grouped by voucher.</span></span>
-   <span data-ttu-id="67479-126">**Список проводок по датам** — в этом отчете отображаются все проводки по дате вместе с номером журнала, ваучером и счетом ГК.</span><span class="sxs-lookup"><span data-stu-id="67479-126">**Transaction list by date** – This report shows all the transactions by date, together with the journal number, voucher, and ledger account.</span></span> <span data-ttu-id="67479-127">В нем также отображаются проводки в валютах проводки, учета и отчетности.</span><span class="sxs-lookup"><span data-stu-id="67479-127">It also shows the transactions in the transaction, accounting, and reporting currencies.</span></span>
-   <span data-ttu-id="67479-128">**Основание проводки** — в этом отчете по проводкам отображается счет по журналу, а также по валюте проводки, учета и отчетности.</span><span class="sxs-lookup"><span data-stu-id="67479-128">**Transaction origin** – This transaction report shows the account by journal, and by transaction, accounting, and reporting currency.</span></span> <span data-ttu-id="67479-129">В нем также отображается каждая строка журнала, которая использовалась как смещение.</span><span class="sxs-lookup"><span data-stu-id="67479-129">It also shows each line of the journal that was used as an offset.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="67479-130">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="67479-130">Additional resources</span></span>
- [<span data-ttu-id="67479-131">Сальдо счета главной книги</span><span class="sxs-lookup"><span data-stu-id="67479-131">General ledger account balances</span></span>](general-ledger-account-balances.md) 
- [<span data-ttu-id="67479-132">Анализатор источника учета</span><span class="sxs-lookup"><span data-stu-id="67479-132">Accounting source explorer</span></span>](../accounts-payable/accounting-source-explorer.md)
- [<span data-ttu-id="67479-133">Финансовая отчетность</span><span class="sxs-lookup"><span data-stu-id="67479-133">Financial reporting</span></span>](financial-reporting-getting-started.md)
- [<span data-ttu-id="67479-134">Просмотр записей журнала</span><span class="sxs-lookup"><span data-stu-id="67479-134">View journal entries</span></span>](tasks/view-journal-entries-or-transactions.md)



