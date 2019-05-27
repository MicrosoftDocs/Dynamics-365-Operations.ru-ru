---
title: Амортизация ОС
description: В этом разделе приводится обзор амортизации для основных средств.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a82e14e12cbde29e5619518481d0c22f6fa1a37a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569617"
---
# <a name="fixed-asset-depreciation"></a><span data-ttu-id="d750a-103">Амортизация ОС</span><span class="sxs-lookup"><span data-stu-id="d750a-103">Fixed asset depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d750a-104">В этом разделе приводится обзор амортизации для основных средств.</span><span class="sxs-lookup"><span data-stu-id="d750a-104">This topic provides an overview of depreciation for fixed assets.</span></span>

<span data-ttu-id="d750a-105">Амортизация — это периодическая проводка, которая обычно уменьшает значение основных средств в балансовом отчете и учитывается в качестве расхода в счете прибыли и убытков.</span><span class="sxs-lookup"><span data-stu-id="d750a-105">Depreciation is a periodic transaction that typically reduces the value of the fixed asset on the balance sheet, and is charged as an expenditure to a profit and loss account.</span></span> <span data-ttu-id="d750a-106">Поэтому, главный счет обычно используется для кредитования периодической амортизации в балансовом отчете.</span><span class="sxs-lookup"><span data-stu-id="d750a-106">Therefore, a main account is typically used to credit the periodic depreciation on the balance sheet.</span></span> <span data-ttu-id="d750a-107">Корр. счет — это счет в части прибылей и убытков плана счетов.</span><span class="sxs-lookup"><span data-stu-id="d750a-107">An offset account is an account in the profit and loss part of the chart of accounts.</span></span>

## <a name="depreciation-adjustment"></a><span data-ttu-id="d750a-108">Корректировка амортизации</span><span class="sxs-lookup"><span data-stu-id="d750a-108">Depreciation adjustment</span></span>
<span data-ttu-id="d750a-109">Обычно только корректировка в уже разнесенной проводки амортизации разносится в качестве переоценки амортизации.</span><span class="sxs-lookup"><span data-stu-id="d750a-109">Usually, only a correction to a posted depreciation transaction is posted as a depreciation adjustment.</span></span> <span data-ttu-id="d750a-110">Поэтому настраиваются главный и корр. счет аналогично как и счета для амортизации.</span><span class="sxs-lookup"><span data-stu-id="d750a-110">Therefore, both the main account and the offset account are set up just like the accounts for depreciation.</span></span> <span data-ttu-id="d750a-111">Корректировка амортизации может быть положительной или отрицательной суммой, но функциональность главного счета (в качестве счета балансового отчета) и функциональность корр. счета (обычно в качестве счета прибыли и убытков) остается той же самой.</span><span class="sxs-lookup"><span data-stu-id="d750a-111">A depreciation adjustment can be either a positive amount or a negative amount, but the functionality of the main account (as a balance sheet account) and the functionality of the offset account (usually as a profit and loss account) remain the same.</span></span>

## <a name="extraordinary-depreciation"></a><span data-ttu-id="d750a-112">Дополнительная амортизация</span><span class="sxs-lookup"><span data-stu-id="d750a-112">Extraordinary depreciation</span></span>
<span data-ttu-id="d750a-113">Дополнительная амортизация работает аналогично базовой амортизации.</span><span class="sxs-lookup"><span data-stu-id="d750a-113">Extraordinary depreciation works like basic depreciation.</span></span> <span data-ttu-id="d750a-114">Поэтому счет ГК используется для кредитования суммы амортизации в балансовом отчете и уменьшает значение основного средства.</span><span class="sxs-lookup"><span data-stu-id="d750a-114">Therefore, a main account is used to credit the depreciation amount to the balance sheet and reduce the value of the fixed asset.</span></span> <span data-ttu-id="d750a-115">Корр. счет — это счет учета прибыли и расходов, где амортизация рассчитывается для финансового периода вычитается как расход.</span><span class="sxs-lookup"><span data-stu-id="d750a-115">An offset account is a profit and loss account, where the depreciation that is calculated for the fiscal period is charged as an expenditure.</span></span> 

<span data-ttu-id="d750a-116">Дополнительная амортизация функционирует независимо от базовой амортизации.</span><span class="sxs-lookup"><span data-stu-id="d750a-116">Extraordinary depreciation works independently of basic depreciation.</span></span> <span data-ttu-id="d750a-117">Применение дополнительной амортизации в качестве отдельного типа проводки позволяет разнести и представить в отчете дополнительную амортизацию отдельно от обычной базовой амортизации.</span><span class="sxs-lookup"><span data-stu-id="d750a-117">By having extraordinary depreciation as a separate transaction type, you can post and report the extraordinary depreciation separately from the basic depreciation.</span></span>

## <a name="special-depreciation-allowance"></a><span data-ttu-id="d750a-118">Особая амортизационная премия</span><span class="sxs-lookup"><span data-stu-id="d750a-118">Special depreciation allowance</span></span>
<span data-ttu-id="d750a-119">Можно использовать специальные амортизационные премии, чтобы взимать суммы дополнительной амортизации в течении первого года, в который актив введен в эксплуатацию и амортизируется.</span><span class="sxs-lookup"><span data-stu-id="d750a-119">You can use special depreciation allowances to take extra depreciation amounts during the first year that an asset is put in service and depreciated.</span></span> <span data-ttu-id="d750a-120">Амортизационные премии необходимо применять до любых других расчетов амортизации.</span><span class="sxs-lookup"><span data-stu-id="d750a-120">Special depreciation allowances must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="d750a-121">Поскольку амортизационные премии часто становятся известны только на более поздних этапах срока службы основного средства, рекомендуется использовать этот тип амортизации с книгой, которая на разносится в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="d750a-121">Because special depreciation allowances are often unknown until later in the service life of the fixed asset, it's best to use this type of depreciation with a book that doesn't post to the general ledger.</span></span> <span data-ttu-id="d750a-122">Можно использовать периодическую функцию "Удалить проводки, не разнесенные в главную книгу" для удаления истории проводок для этих книг.</span><span class="sxs-lookup"><span data-stu-id="d750a-122">You can use the Delete transactions not posted to general ledger periodic function to delete the transaction history for these books.</span></span> <span data-ttu-id="d750a-123">Затем можно удалить историю амортизации для журнала основных средств, разнести амортизационную премия, когда она станет известна, а затем разнести остальные проводки амортизации за год.</span><span class="sxs-lookup"><span data-stu-id="d750a-123">You can then delete the depreciation history for the fixed asset book, post the special depreciation allowance when it's known, and then post the remaining depreciation transactions for the year.</span></span> 

<span data-ttu-id="d750a-124">Можно создать неограниченное количество записей специальных амортизационных премий.</span><span class="sxs-lookup"><span data-stu-id="d750a-124">You can create an unlimited number of special depreciation allowance records.</span></span> <span data-ttu-id="d750a-125">После назначения этих записей журналу группы активов они используются для журнала активов.</span><span class="sxs-lookup"><span data-stu-id="d750a-125">After you assign those records to an asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="d750a-126">Специальная амортизационная премия вводится как процент или фиксированная сумма.</span><span class="sxs-lookup"><span data-stu-id="d750a-126">A special depreciation allowance is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="d750a-127">При разноске предложений по амортизации проводки амортизационной премии разносятся в книгу как проводки, отделенные от проводок амортизации.</span><span class="sxs-lookup"><span data-stu-id="d750a-127">When you post depreciation proposals, special depreciation allowance transactions are posted to the book as transactions that are separate from the depreciation transactions.</span></span>

## <a name="depreciation-calendars"></a><span data-ttu-id="d750a-128">Календари амортизации</span><span class="sxs-lookup"><span data-stu-id="d750a-128">Depreciation calendars</span></span>
<span data-ttu-id="d750a-129">Каждая книга имеет календарь, который используется при амортизации основных средств.</span><span class="sxs-lookup"><span data-stu-id="d750a-129">Each book has a calendar that is used when you depreciate fixed assets.</span></span> <span data-ttu-id="d750a-130">Если не указать календарь в книге, по умолчанию книга использует финансовый календарь книги учета.</span><span class="sxs-lookup"><span data-stu-id="d750a-130">By default, if you don't indicate a calendar on the book, the book uses the ledger fiscal calendar.</span></span> <span data-ttu-id="d750a-131">Необходимо выбрать финансовый календарь для книги, когда связанный с книгой профиль амортизации использует фискальный год амортизации.</span><span class="sxs-lookup"><span data-stu-id="d750a-131">You must select a fiscal calendar for a book when the depreciation profile that is associated with the book uses a fiscal depreciation year.</span></span> 

<span data-ttu-id="d750a-132">Вы можете создать общие календари, используя страницу **Финансовые календари** в главной книге.</span><span class="sxs-lookup"><span data-stu-id="d750a-132">You can create shared calendars by using the **Fiscal calendars** page in General ledger.</span></span>

<span data-ttu-id="d750a-133">Дополнительные сведения см. в разделе [Методы амортизации и соглашения по амортизации](depreciation-methods-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="d750a-133">For more information, see [Depreciation methods and conventions](depreciation-methods-conventions.md).</span></span>



