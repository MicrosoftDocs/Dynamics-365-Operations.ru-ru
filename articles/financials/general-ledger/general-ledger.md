---
title: "Домашняя страница главной книги и финансовой отчетности"
description: "Используйте главную книгу для определения финансовых записей юридического лица и управления ими."
author: twheeloc
manager: AnnBe
ms.date: 08/31/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: GeneralJournalEntryWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 2177110dc16528de7eddedb0667faae553a36b12
ms.contentlocale: ru-ru
ms.lasthandoff: 02/07/2018

---

# <a name="general-ledger"></a><span data-ttu-id="3dce3-103">Главная книга</span><span class="sxs-lookup"><span data-stu-id="3dce3-103">General ledger</span></span> 

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3dce3-104">Используйте главную книгу для определения финансовых записей юридического лица и управления ими.</span><span class="sxs-lookup"><span data-stu-id="3dce3-104">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="3dce3-105">Главная книга — это реестр дебетовых и кредитовых записей.</span><span class="sxs-lookup"><span data-stu-id="3dce3-105">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="3dce3-106">Эти записи классифицируются с помощью счетов, перечисленных в плане счетов.</span><span class="sxs-lookup"><span data-stu-id="3dce3-106">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

 - [<span data-ttu-id="3dce3-107">Планирование плана счетов</span><span class="sxs-lookup"><span data-stu-id="3dce3-107">Plan your chart of accounts</span></span>](plan-chart-of-accounts.md)
 - [<span data-ttu-id="3dce3-108">Типы счетов ГК</span><span class="sxs-lookup"><span data-stu-id="3dce3-108">Main account types</span></span>](main-account-types.md)

<span data-ttu-id="3dce3-109">Денежная сумма можно распределить по одному или нескольким счетам либо комбинациям счетов и аналитик на основе правил распределения.</span><span class="sxs-lookup"><span data-stu-id="3dce3-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="3dce3-110">Существует два типа распределений: фиксированные и переменные.</span><span class="sxs-lookup"><span data-stu-id="3dce3-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="3dce3-111">Можно также сопоставить проводки между счетами ГК и переоценить валютные суммы.</span><span class="sxs-lookup"><span data-stu-id="3dce3-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="3dce3-112">В конце финансового года необходимо создать закрывающие проводки и подготовить счета для следующего финансового года.</span><span class="sxs-lookup"><span data-stu-id="3dce3-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="3dce3-113">Можно использовать функции консолидации, чтобы объединить финансовые результаты для нескольких дочерних юридических лиц в результаты для отдельной консолидированной организации.</span><span class="sxs-lookup"><span data-stu-id="3dce3-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="3dce3-114">Дочерние компании могут входить в одну базу данных Microsoft Dynamics 365 for Finance and Operations или в разные базы данных.</span><span class="sxs-lookup"><span data-stu-id="3dce3-114">The subsidiaries can be in the same Microsoft Dynamics 365 for Finance and Operations database or in separate databases.</span></span>

- [<span data-ttu-id="3dce3-115">Обзор консолидации и закрытия</span><span class="sxs-lookup"><span data-stu-id="3dce3-115">Consolidation and elimination overview</span></span>](../budgeting/consolidation-elimination-overview.md)
- [<span data-ttu-id="3dce3-116">Сальдо счета главной книги</span><span class="sxs-lookup"><span data-stu-id="3dce3-116">General ledger account balances</span></span>](general-ledger-account-balances.md)
- [<span data-ttu-id="3dce3-117">Финансовые аналитики</span><span class="sxs-lookup"><span data-stu-id="3dce3-117">Financial dimensions</span></span>](financial-dimensions.md)

<span data-ttu-id="3dce3-118">[![Бизнес-процесс](./media/GL-process.PNG)](./media/GL-process.PNG)</span><span class="sxs-lookup"><span data-stu-id="3dce3-118">[![Business process](./media/GL-process.PNG)](./media/GL-process.PNG)</span></span>

## <a name="sales-tax"></a><span data-ttu-id="3dce3-119">Налог (НСП)</span><span class="sxs-lookup"><span data-stu-id="3dce3-119">Sales tax</span></span>
<span data-ttu-id="3dce3-120">Каждая компания собирает и платит налоги различным налоговым органам.</span><span class="sxs-lookup"><span data-stu-id="3dce3-120">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="3dce3-121">Правила и ставки различаются по странам, регионам, штатам, областям и городам.</span><span class="sxs-lookup"><span data-stu-id="3dce3-121">The rules and rates vary by country/region, state, county, and city.</span></span>
<span data-ttu-id="3dce3-122">Кроме того, правила необходимо периодически обновлять в связи с изменением требований налоговых органов.</span><span class="sxs-lookup"><span data-stu-id="3dce3-122">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="3dce3-123">Налоговые коды содержат основные сведения о том, сколько нужно собирать и платить налоговым органам.</span><span class="sxs-lookup"><span data-stu-id="3dce3-123">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="3dce3-124">При настройке налоговых кодов определяются суммы или проценты сборов.</span><span class="sxs-lookup"><span data-stu-id="3dce3-124">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="3dce3-125">Можно также определить разные способы применения этих сумм или процентов к суммам транзакций.</span><span class="sxs-lookup"><span data-stu-id="3dce3-125">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="3dce3-126">В разделах этой главы содержится информация о настройке налоговых кодов для способов уплаты и ставок, с которыми работают соответствующие налоговые органы.</span><span class="sxs-lookup"><span data-stu-id="3dce3-126">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>

 - [<span data-ttu-id="3dce3-127">Обзор налога</span><span class="sxs-lookup"><span data-stu-id="3dce3-127">Sales tax overview</span></span>](indirect-taxes-overview.md)
 - [<span data-ttu-id="3dce3-128">Ставки налога на основе базы маржинальной прибыли и методов расчета</span><span class="sxs-lookup"><span data-stu-id="3dce3-128">Sales tax rates based on the Marginal base and Calculation methods</span></span>](marginal-base-field.md)
 - [<span data-ttu-id="3dce3-129">Налоговые платежи и правила округления</span><span class="sxs-lookup"><span data-stu-id="3dce3-129">Sales tax payments and rounding rules</span></span>](round-sales-tax-payments.md)


## <a name="additional-resources"></a><span data-ttu-id="3dce3-130">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3dce3-130">Additional resources</span></span>

### <a name="whats-new-and-in-development"></a><span data-ttu-id="3dce3-131">Новые возможности и текущие разработки</span><span class="sxs-lookup"><span data-stu-id="3dce3-131">What's new and in development</span></span>

<span data-ttu-id="3dce3-132">Перейдите в раздел [Дорожная карта Microsoft Dynamics 365](https://roadmap.dynamics.com/), чтобы просмотреть новые функции, которые уже выпущены и которые все еще находятся в разработке.</span><span class="sxs-lookup"><span data-stu-id="3dce3-132">Go to the [Microsoft Dynamics 365 Roadmap](https://roadmap.dynamics.com/) to see what new features have been released and what new features are in development.</span></span> 

### <a name="blogs"></a><span data-ttu-id="3dce3-133">Блоги</span><span class="sxs-lookup"><span data-stu-id="3dce3-133">Blogs</span></span>

<span data-ttu-id="3dce3-134">Мнения, новости и другие сведения о расчетах с поставщиками и других решениях см. в [блоге по Microsoft Dynamics 365](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise).</span><span class="sxs-lookup"><span data-stu-id="3dce3-134">You can find opinions, news, and other information about Accounts payable and other solutions on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise).</span></span>

<span data-ttu-id="3dce3-135">В [блоге группы разработчиков Microsoft Dynamics AX](https://blogs.msdn.microsoft.com/dax/) есть множество публикаций о модуле "Главная книга".</span><span class="sxs-lookup"><span data-stu-id="3dce3-135">There are many posts about General ledger on the [Microsoft Dynamics AX product team blog](https://blogs.msdn.microsoft.com/dax/).</span></span> <span data-ttu-id="3dce3-136">Хотя некоторые из этих записей посвящены предыдущей версии модуля "Главная книга", обсуждаемые в них понятия по-прежнему актуальны, а процедуры аналогичны процедурам в текущей версии.</span><span class="sxs-lookup"><span data-stu-id="3dce3-136">Although some of these posts were written for the previous version of General ledger, the same concepts still apply, and the procedures are also similar in the current version.</span></span>

<span data-ttu-id="3dce3-137">[Блог сообщества партнеров Microsoft Dynamics Operations](https://community.dynamics.com/partner/b/operationspartnercommunityblog) предоставляет партнерам Microsoft Dynamics единый источник информации о новых возможностях и тенденциях в MBS Operations.</span><span class="sxs-lookup"><span data-stu-id="3dce3-137">The [Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) gives Microsoft Dynamics Partners a single resource where they can learn what is new and trending in MBS Operations.</span></span>

### <a name="task-guides"></a><span data-ttu-id="3dce3-138">Проводники по задачам</span><span class="sxs-lookup"><span data-stu-id="3dce3-138">Task guides</span></span>
<span data-ttu-id="3dce3-139">Руководства по задачам в Finance and Operations — это еще один источник справочной информации.</span><span class="sxs-lookup"><span data-stu-id="3dce3-139">Additional help is available as task guides inside Finance and Operations.</span></span> <span data-ttu-id="3dce3-140">Чтобы перейти к руководствам по задачам, нажмите кнопку "Справка" на любой странице.</span><span class="sxs-lookup"><span data-stu-id="3dce3-140">To access task guides, click the Help button on any page.</span></span>

### <a name="videos"></a><span data-ttu-id="3dce3-141">Видео</span><span class="sxs-lookup"><span data-stu-id="3dce3-141">Videos</span></span>

<span data-ttu-id="3dce3-142">Смотрите видео с инструкциями на канале [Microsoft Dynamics 365 в YouTube](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span><span class="sxs-lookup"><span data-stu-id="3dce3-142">Check out the how-to videos that are now available on the [Microsoft Dynamics 365 YouTube Channel](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span></span>


