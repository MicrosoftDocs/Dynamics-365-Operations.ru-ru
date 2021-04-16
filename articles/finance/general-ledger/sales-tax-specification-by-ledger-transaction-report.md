---
title: Отчет с налоговой информацией по проводке ГК
description: В этой теме объясняется, как использовать отчет по налоговой информации по проводке ГК для просмотра и печати сведений о проводках ГК, для которых рассчитан налог.
author: ericwang
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 75913edcbac0151d5d27d866ff5430b194c62738
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815268"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a><span data-ttu-id="216d2-103">Отчет с налоговой информацией по проводке ГК</span><span class="sxs-lookup"><span data-stu-id="216d2-103">Sales tax specification by ledger transaction report</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="216d2-104">В этой теме объясняется, как использовать отчет **Налоговая информация по проводке ГК** для просмотра и печати сведений о проводках ГК, для которых рассчитан налог.</span><span class="sxs-lookup"><span data-stu-id="216d2-104">This topic explains how to use the **Sales tax specification by ledger transaction** report to view and print information about ledger transactions that sales tax is calculated for.</span></span>

## <a name="tax-accounts-vs-non-tax-accounts"></a><span data-ttu-id="216d2-105">Налоговые счета и счета, не являющиеся налоговыми</span><span class="sxs-lookup"><span data-stu-id="216d2-105">Tax accounts vs. non-tax accounts</span></span>

<span data-ttu-id="216d2-106">В отчете **Налоговая информация по проводке ГК** отображаются налоговые проводки для налоговых и не налоговых счетов.</span><span class="sxs-lookup"><span data-stu-id="216d2-106">The **Sales tax specification by ledger transaction** report shows tax transactions for both tax accounts and non-tax accounts.</span></span> <span data-ttu-id="216d2-107">Эти счета классифицируются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="216d2-107">These accounts are categorized in the following way:</span></span>

- <span data-ttu-id="216d2-108">**Налоговый счет** — счет считается налоговым счетом при разноске налоговой проводки, а счет ГК в строке журнала **Налог** является налоговым счетом, таким как счет уплаты налога или счет получения налога.</span><span class="sxs-lookup"><span data-stu-id="216d2-108">**Tax account** – An account is considered a tax account when a tax transaction is posted, and the main account on the **Sales Tax** journal line is a tax account, such as a sales tax payable account or a sales tax receivable account.</span></span>
- <span data-ttu-id="216d2-109">**Неналоговый счет** — счет считается неналоговым счетом при разноске налоговой проводки, а счет ГК в исходной проводе является неналоговым счетом, таким как счет выручки или расходный счет.</span><span class="sxs-lookup"><span data-stu-id="216d2-109">**Non-tax account** – An account is considered a non-tax account when a tax transaction is posted, and the main account on the original transaction is a non-tax account, such as a revenue account or an expense account.</span></span>

<span data-ttu-id="216d2-110">Для налоговых счетов в столбцах **Источник**, **Входящий налог** и **Исходящий налог** в отчете отображается **0** (ноль).</span><span class="sxs-lookup"><span data-stu-id="216d2-110">For tax accounts, the **Origin**, **Sales tax receivable**, and **Sales tax payable** columns on the report show **0** (zero).</span></span> <span data-ttu-id="216d2-111">Для неналоговых счетов в этих столбцах отображаются суммы.</span><span class="sxs-lookup"><span data-stu-id="216d2-111">For non-tax accounts, those columns show amounts.</span></span>

## <a name="filtering-the-data-on-the-report"></a><span data-ttu-id="216d2-112">Фильтрация данных в отчете</span><span class="sxs-lookup"><span data-stu-id="216d2-112">Filtering the data on the report</span></span>

<span data-ttu-id="216d2-113">При создании этого отчета доступны следующие поля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="216d2-113">When you generate the report, the following default fields are available.</span></span> <span data-ttu-id="216d2-114">Эти поля можно использовать для фильтрации данных, отображаемых в отчете.</span><span class="sxs-lookup"><span data-stu-id="216d2-114">You can use these fields to filter the data that is shown on the report.</span></span>

| <span data-ttu-id="216d2-115">Поле</span><span class="sxs-lookup"><span data-stu-id="216d2-115">Field</span></span>                      | <span data-ttu-id="216d2-116">Описание</span><span class="sxs-lookup"><span data-stu-id="216d2-116">Description</span></span> |
|----------------------------|-------------|
| <span data-ttu-id="216d2-117">Дата</span><span class="sxs-lookup"><span data-stu-id="216d2-117">Date</span></span>                       | <span data-ttu-id="216d2-118">Используйте поля в разделах **От** и **До** для определения диапазона дат для налоговых проводок.</span><span class="sxs-lookup"><span data-stu-id="216d2-118">Use the fields in the **From** and **To** sections to define a date range for the tax transactions.</span></span> |
| <span data-ttu-id="216d2-119">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="216d2-119">Main account</span></span>               | <span data-ttu-id="216d2-120">Используйте поля в разделах **От** и **До** для определения диапазона счетов главной книги.</span><span class="sxs-lookup"><span data-stu-id="216d2-120">Use the fields in the **From** and **To** sections to define a range of main accounts.</span></span> |
| <span data-ttu-id="216d2-121">Код налога</span><span class="sxs-lookup"><span data-stu-id="216d2-121">Sales tax code</span></span>             | <span data-ttu-id="216d2-122">Используйте поля в разделах **От** и **До** для определения диапазона кодов налога.</span><span class="sxs-lookup"><span data-stu-id="216d2-122">Use the fields in the **From** and **To** sections to define a range of sales tax codes.</span></span> |
| <span data-ttu-id="216d2-123">Группировка</span><span class="sxs-lookup"><span data-stu-id="216d2-123">Grouping</span></span>                   | <span data-ttu-id="216d2-124">Выберите, должен ли отчет быть сгруппирован по счету книги учета или по налоговому коду.</span><span class="sxs-lookup"><span data-stu-id="216d2-124">Select whether the report should be grouped by ledger account or sales tax code.</span></span> |
| <span data-ttu-id="216d2-125">Промежуточный итог по налоговому коду</span><span class="sxs-lookup"><span data-stu-id="216d2-125">Subtotal by sales tax code</span></span> | <span data-ttu-id="216d2-126">Установите для этого параметра значение **Да**, чтобы отображать промежуточные итоги по налоговому коду.</span><span class="sxs-lookup"><span data-stu-id="216d2-126">Set this option to **Yes** to show subtotals by sales tax code.</span></span> |
| <span data-ttu-id="216d2-127">Только итоги</span><span class="sxs-lookup"><span data-stu-id="216d2-127">Totals only</span></span>                | <span data-ttu-id="216d2-128">Установите для этого параметра значение **Да**, чтобы отображались только итоги.</span><span class="sxs-lookup"><span data-stu-id="216d2-128">Set this option to **Yes** to show only totals.</span></span> |
| <span data-ttu-id="216d2-129">Только счета ГК</span><span class="sxs-lookup"><span data-stu-id="216d2-129">Main accounts only</span></span>         | <span data-ttu-id="216d2-130">Установите для этого параметра значение **Да**, чтобы включить в отчет только счета ГК.</span><span class="sxs-lookup"><span data-stu-id="216d2-130">Set this option to **Yes** to include only main accounts on the report.</span></span> |

## <a name="showing-only-non-tax-accounts-on-the-report"></a><span data-ttu-id="216d2-131">Отображение в отчете только счетов, не являющихся налоговыми</span><span class="sxs-lookup"><span data-stu-id="216d2-131">Showing only non-tax accounts on the report</span></span>

<span data-ttu-id="216d2-132">Чтобы отобразить в отчете только неналоговые счета, настройте условия фильтрации, такие как звездочка (\*), как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="216d2-132">To show only non-tax accounts on the report, set up a filter condition, such as an asterisk (\*), as shown in the following illustration.</span></span>

![Отчет, отображающий неналоговые счета](media/taxspecperledgertrans.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]