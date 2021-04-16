---
title: Просмотр проводок по задолженности, активам и расходам
description: В этой теме объясняется, как просмотреть проводки для арендованного актива. Эти проводки включают проводки по обязательству по аренде и проводки по затратам по осуществлению аренды, которые были разнесены.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 6dbb5de75780091d3392e413e3a2415067ac6dda
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827490"
---
# <a name="view-liability-asset-and-expense-transactions"></a><span data-ttu-id="185d9-104">Просмотр проводок по задолженности, активам и расходам</span><span class="sxs-lookup"><span data-stu-id="185d9-104">View liability, asset, and expense transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="185d9-105">В этой теме объясняется, как просмотреть проводки для арендованного актива.</span><span class="sxs-lookup"><span data-stu-id="185d9-105">This topic explains how to view transactions for a leased asset.</span></span> <span data-ttu-id="185d9-106">Эти проводки включают проводки по обязательству по аренде и проводки по затратам по осуществлению аренды, которые были разнесены.</span><span class="sxs-lookup"><span data-stu-id="185d9-106">These transactions include lease liability transactions and executory expense transactions that have been posted.</span></span> <span data-ttu-id="185d9-107">Учетные стоимости обязательств и актива в форме права пользования (ФПП) используются в нескольких отчетах.</span><span class="sxs-lookup"><span data-stu-id="185d9-107">The carrying values of the liability and right-of-use (ROU) asset are used on several reports.</span></span> <span data-ttu-id="185d9-108">Они также используются для расчета значений коррекции.</span><span class="sxs-lookup"><span data-stu-id="185d9-108">They are also used to calculate adjustment values.</span></span>

## <a name="liability-transactions"></a><span data-ttu-id="185d9-109">Транзакции по обязательствам</span><span class="sxs-lookup"><span data-stu-id="185d9-109">Liability transactions</span></span>

<span data-ttu-id="185d9-110">Чтобы просмотреть проводки по обязательствам по аренде, выберите аренду на странице **Сводка по аренде**, а затем выберите **Книги**, чтобы открыть книги, связанные с записью аренды.</span><span class="sxs-lookup"><span data-stu-id="185d9-110">To view the lease liability transactions, select a lease on the **Lease summary** page, and then select **Books** to open the books that are attached to the lease record.</span></span> <span data-ttu-id="185d9-111">После разноски первоначального признания, накладной или журнала процентов выберите **Проводки по обязательствам**.</span><span class="sxs-lookup"><span data-stu-id="185d9-111">After an initial recognition, an invoice, or an interest journal has been posted, select **Liability transactions**.</span></span>

<span data-ttu-id="185d9-112">На странице **Проводки по обязательствам** отображаются проводки, которые либо увеличивают, либо уменьшают арендное обязательство.</span><span class="sxs-lookup"><span data-stu-id="185d9-112">The **Liability transactions** page shows the transactions that either increase or decrease the lease liability.</span></span> <span data-ttu-id="185d9-113">Отрицательные суммы на этой странице представляют собой кредитные проводки в стандартном приложении.</span><span class="sxs-lookup"><span data-stu-id="185d9-113">Negative amounts on this page represent credit transactions in the standard application.</span></span> <span data-ttu-id="185d9-114">Все начисления процентов отображаются как отрицательные значения и увеличивают общую сумму арендного обязательства.</span><span class="sxs-lookup"><span data-stu-id="185d9-114">Any interest accruals are shown as negative values and increase the total lease liability.</span></span> <span data-ttu-id="185d9-115">Любые корректировки аренды отображаются как положительные или отрицательные значения, в зависимости от природы и воздействия книги по аренде.</span><span class="sxs-lookup"><span data-stu-id="185d9-115">Any lease adjustments are shown as positive or negative values, depending on the nature and impact of the lease book.</span></span> <span data-ttu-id="185d9-116">Текущее чистое общее сальдо арендного обязательства для выбранной аренды отображается в левом нижнем углу страницы.</span><span class="sxs-lookup"><span data-stu-id="185d9-116">The current net total balance of the lease liability for the selected lease is shown at the bottom left of the page.</span></span>

## <a name="asset-transactions"></a><span data-ttu-id="185d9-117">Транзакции по активу</span><span class="sxs-lookup"><span data-stu-id="185d9-117">Asset transactions</span></span>

<span data-ttu-id="185d9-118">Чтобы просмотреть проводки по активам по аренде, выберите аренду на странице **Сводка по аренде**, а затем выберите **Книги**, чтобы открыть книги аренды, связанные с записью аренды.</span><span class="sxs-lookup"><span data-stu-id="185d9-118">To view the lease asset transactions, select a lease on the **Lease summary** page, and then select **Books** to open the lease books that are attached to the lease record.</span></span> <span data-ttu-id="185d9-119">Затем выберите **Проводки по активам**.</span><span class="sxs-lookup"><span data-stu-id="185d9-119">Then select **Asset transactions**.</span></span>

<span data-ttu-id="185d9-120">На странице **Проводка по активу** отображаются проводки, которые либо увеличивают, либо уменьшают счета аренды актива и накопленной амортизации.</span><span class="sxs-lookup"><span data-stu-id="185d9-120">The **Asset transaction** page shows the transactions that either increase or decrease the lease asset and accumulated depreciation accounts.</span></span> <span data-ttu-id="185d9-121">Дебеты отображаются как положительные значения, а кредиты отображаются как отрицательные значения, как на странице **Проводки по обязательствам**.</span><span class="sxs-lookup"><span data-stu-id="185d9-121">Debits are shown as positive values, and credits are shown as negative values, as on the **Liability transactions** page.</span></span> <span data-ttu-id="185d9-122">Учтенное первоначальное признание и следующая накопленная амортизация показаны в нижней левой части страницы в качестве сальдо актива.</span><span class="sxs-lookup"><span data-stu-id="185d9-122">The posted initial recognition and the next of accumulated depreciation are shown at the bottom left of the page as the asset balance.</span></span> 

## <a name="expenses-transactions"></a><span data-ttu-id="185d9-123">Проводки по расходам</span><span class="sxs-lookup"><span data-stu-id="185d9-123">Expenses transactions</span></span>

<span data-ttu-id="185d9-124">Чтобы просмотреть проводки по расходам по аренде, выберите аренду на странице **Сводка по аренде**, а затем выберите **Книги**, чтобы открыть книги аренды, связанные с записью аренды.</span><span class="sxs-lookup"><span data-stu-id="185d9-124">To view the lease expense transactions, select a lease on the **Lease summary** page, and then select **Books** to open the lease books that are attached to the lease record.</span></span> <span data-ttu-id="185d9-125">Затем выберите **Проводки по расходам**.</span><span class="sxs-lookup"><span data-stu-id="185d9-125">Then select **Expense transactions**.</span></span>

<span data-ttu-id="185d9-126">На странице **Проводки по расходам** отображаются все расходы, которые были разнесены по аренде, такие как расходы на уплату процентов, расходы на амортизацию и любые затраты по осуществлению аренды.</span><span class="sxs-lookup"><span data-stu-id="185d9-126">The **Expense transactions** page shows all the expenses that have been posted against the lease, such as interest expenses, depreciation expenses, and any executory costs.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]