---
title: "Домашняя страница главной книги и финансовой отчетности"
description: "Используйте главную книгу для определения финансовых записей юридического лица и управления ими. Главная книга — это реестр дебетовых и кредитовых записей. Эти записи классифицируются с помощью счетов, перечисленных в плане счетов."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 78f3d9c27767c089ac686f333cae3cb50c03ee18
ms.contentlocale: ru-ru
ms.lasthandoff: 07/18/2017

---

# <a name="general-ledger"></a><span data-ttu-id="484c8-105">Главная книга</span><span class="sxs-lookup"><span data-stu-id="484c8-105">General ledger</span></span> 

[!include[banner](../includes/banner.md)]


<span data-ttu-id="484c8-106">Используйте главную книгу для определения финансовых записей юридического лица и управления ими.</span><span class="sxs-lookup"><span data-stu-id="484c8-106">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="484c8-107">Главная книга — это реестр дебетовых и кредитовых записей.</span><span class="sxs-lookup"><span data-stu-id="484c8-107">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="484c8-108">Эти записи классифицируются с помощью счетов, перечисленных в плане счетов.</span><span class="sxs-lookup"><span data-stu-id="484c8-108">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

<span data-ttu-id="484c8-109">Денежная сумма можно распределить по одному или нескольким счетам либо комбинациям счетов и аналитик на основе правил распределения.</span><span class="sxs-lookup"><span data-stu-id="484c8-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="484c8-110">Существует два типа распределений: фиксированные и переменные.</span><span class="sxs-lookup"><span data-stu-id="484c8-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="484c8-111">Можно также сопоставить проводки между счетами ГК и переоценить валютные суммы.</span><span class="sxs-lookup"><span data-stu-id="484c8-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="484c8-112">В конце финансового года необходимо создать закрывающие проводки и подготовить счета для следующего финансового года.</span><span class="sxs-lookup"><span data-stu-id="484c8-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="484c8-113">Можно использовать функции консолидации, чтобы объединить финансовые результаты для нескольких дочерних юридических лиц в результаты для отдельной консолидированной организации.</span><span class="sxs-lookup"><span data-stu-id="484c8-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="484c8-114">Дочерние компании могут входить в одну базу данных Microsoft Dynamics 365 for Finance and Operations или в разные базы данных.</span><span class="sxs-lookup"><span data-stu-id="484c8-114">The subsidiaries can be in the same Microsoft Dynamics 365 for Finance and Operations database or in separate databases.</span></span>

# <a name="sales-tax"></a><span data-ttu-id="484c8-115">Налог (НСП)</span><span class="sxs-lookup"><span data-stu-id="484c8-115">Sales tax</span></span>
<span data-ttu-id="484c8-116">Каждая компания собирает и платит налоги различным налоговым органам.</span><span class="sxs-lookup"><span data-stu-id="484c8-116">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="484c8-117">Правила и ставки различаются по странам, регионам, штатам, областям и городам.</span><span class="sxs-lookup"><span data-stu-id="484c8-117">The rules and rates vary by country/region, state, county, and city.</span></span> <span data-ttu-id="484c8-118">Кроме того, правила необходимо периодически обновлять в связи с изменением требований налоговых органов.</span><span class="sxs-lookup"><span data-stu-id="484c8-118">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="484c8-119">Налоговые коды содержат основные сведения о том, сколько нужно собирать и платить налоговым органам.</span><span class="sxs-lookup"><span data-stu-id="484c8-119">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="484c8-120">При настройке налоговых кодов определяются суммы или проценты сборов.</span><span class="sxs-lookup"><span data-stu-id="484c8-120">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="484c8-121">Можно также определить разные способы применения этих сумм или процентов к суммам транзакций.</span><span class="sxs-lookup"><span data-stu-id="484c8-121">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="484c8-122">В разделах этой главы содержится информация о настройке налоговых кодов для способов уплаты и ставок, с которыми работают соответствующие налоговые органы.</span><span class="sxs-lookup"><span data-stu-id="484c8-122">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>







