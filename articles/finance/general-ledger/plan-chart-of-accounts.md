---
title: Планирование плана счетов
description: Эти разделы представляют информацию, которая поможет запланировать плана счетов для вашей организации.
author: aprilolson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 29e5328043a4259b464b272983e11061ade1724c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230378"
---
# <a name="plan-your-chart-of-accounts"></a><span data-ttu-id="946cc-103">Планирование плана счетов</span><span class="sxs-lookup"><span data-stu-id="946cc-103">Plan your chart of accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="946cc-104">Этот раздел представляет информацию, которая поможет запланировать плана счетов для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="946cc-104">This topic provides information that will help you plan the chart of accounts for your organization.</span></span>

<span data-ttu-id="946cc-105">Для того, чтобы отслеживать и вести финансовые сведения в организации, вы можете настроить план счетов.</span><span class="sxs-lookup"><span data-stu-id="946cc-105">To track and maintain financial information in an organization, you can set up a chart of accounts.</span></span> <span data-ttu-id="946cc-106">План счетов — это собрание счетов, которые определяют финансовые структуры.</span><span class="sxs-lookup"><span data-stu-id="946cc-106">A chart of accounts is a collection of accounts that define a financial framework.</span></span> <span data-ttu-id="946cc-107">Для дополнительного отслеживания проводок по этим счетам можно добавить сегменты.</span><span class="sxs-lookup"><span data-stu-id="946cc-107">To further track the transactions in these accounts, you can add segments.</span></span> <span data-ttu-id="946cc-108">Эти сегменты называются финансовыми аналитиками.</span><span class="sxs-lookup"><span data-stu-id="946cc-108">These segments are known as financial dimensions.</span></span> <span data-ttu-id="946cc-109">Например, счет расходов может включать финансовые аналитики с названиями "Подразделение", "Центр затрат" и "Назначение".</span><span class="sxs-lookup"><span data-stu-id="946cc-109">For example, an expense account might include financial dimensions that are named Department, Cost center, and Purpose.</span></span> <span data-ttu-id="946cc-110">Определяемые пользователем правила указывают, как эти финансовые аналитики связываются со счетами ГК и другими финансовыми аналитиками, и как проводки можно вводить.</span><span class="sxs-lookup"><span data-stu-id="946cc-110">User-defined rules determine how financial dimensions are attached to the main accounts and to other financial dimensions, and also how transactions are entered.</span></span> <span data-ttu-id="946cc-111">Эти определяемые пользователем правила известны как структуры счетов и дополнительные правила.</span><span class="sxs-lookup"><span data-stu-id="946cc-111">These user-defined rules are known as account structures and advanced rules.</span></span>

<span data-ttu-id="946cc-112">План счетов представляет собой структурированный список счетов ГК юридического лица.</span><span class="sxs-lookup"><span data-stu-id="946cc-112">The chart of accounts is a structured list of a legal entity's general ledger accounts.</span></span> <span data-ttu-id="946cc-113">Список используется для подготовки отчетов ГК для органов власти и для собственников.</span><span class="sxs-lookup"><span data-stu-id="946cc-113">The list is used to prepare financial reports for authorities and owners.</span></span> <span data-ttu-id="946cc-114">Счета группируются сначала по типам счетов, а затем агрегируются по более широким категориям.</span><span class="sxs-lookup"><span data-stu-id="946cc-114">The accounts are first grouped into types of accounts and then further aggregated into larger categories.</span></span> <span data-ttu-id="946cc-115">Самым общим видом группировки является группировка по выручке и затратам (текущие счета), а также активам и пассивам (балансовые счета).</span><span class="sxs-lookup"><span data-stu-id="946cc-115">At the most general level, the accounts are grouped as revenues and costs (operating accounts), and assets and liabilities (balance accounts).</span></span>

<span data-ttu-id="946cc-116">План счетов может быть предоставлен для совместного доступа и использован любым юридическим лицом в организации.</span><span class="sxs-lookup"><span data-stu-id="946cc-116">A chart of accounts can be shared and used by any legal entity in an organization.</span></span> <span data-ttu-id="946cc-117">План счетов, используемый юридическим лицом, определяется на странице **Книга учета**.</span><span class="sxs-lookup"><span data-stu-id="946cc-117">The chart of accounts that is used by a legal entity is defined on the **Ledger** page.</span></span>

<span data-ttu-id="946cc-118">Здесь указаны некоторые факторы, которые следует учесть при планировании структуры плана счетов для своей организации:</span><span class="sxs-lookup"><span data-stu-id="946cc-118">Here are some of the factors that you must consider when you plan the structure of the chart of accounts for your organization:</span></span>

- <span data-ttu-id="946cc-119">Требования к отчетности, существующие в стране или регионе, где базируется организация</span><span class="sxs-lookup"><span data-stu-id="946cc-119">The reporting requirements of the country or region where your organization is based</span></span>
- <span data-ttu-id="946cc-120">Требования к отчетности вашего юридического лица</span><span class="sxs-lookup"><span data-stu-id="946cc-120">The reporting requirements of your legal entity</span></span>
- <span data-ttu-id="946cc-121">Уровень детализации, необходимый как для внешних организаций, так и для вашей организации</span><span class="sxs-lookup"><span data-stu-id="946cc-121">The degree of specification that is required, both for both external organizations and for your organization</span></span>

<span data-ttu-id="946cc-122">План счетов создается на странице **План счетов**.</span><span class="sxs-lookup"><span data-stu-id="946cc-122">You create the chart of accounts on the **Chart of accounts** page.</span></span> <span data-ttu-id="946cc-123">Счета ГК можно создать на странице **План счетов** или на странице **Счета ГК**.</span><span class="sxs-lookup"><span data-stu-id="946cc-123">You can create main accounts from the **Chart of accounts** page or the **Main accounts** page.</span></span> <span data-ttu-id="946cc-124">Для счетов ГК не должны использоваться специальные символы, которые используются как разделители для плана счетов.</span><span class="sxs-lookup"><span data-stu-id="946cc-124">Your main accounts shouldn't use any special characters that are used as delimiters for chart of accounts.</span></span> <span data-ttu-id="946cc-125">В противном случае может возникнуть неустойчивость, или будет необходимо всегда использовать поиск с подстановкой или диалоговое окно при вводе комбинации счетов и аналитик.</span><span class="sxs-lookup"><span data-stu-id="946cc-125">Otherwise, you might experience instability, or you might always have to use lookups or the dialog box when you enter combinations of accounts and dimensions.</span></span> <span data-ttu-id="946cc-126">Дополнительные сведения см. в разделе [Создание счета ГК](tasks/create-main-account.md).</span><span class="sxs-lookup"><span data-stu-id="946cc-126">For more information, see [Create a main account](tasks/create-main-account.md).</span></span>

> [!NOTE]
> <span data-ttu-id="946cc-127">В Dynamics 365 for Finance and Operations версии 8.0 (апрель 2018) можно изменить разделитель плана счетов на странице **Параметры главной книги**.</span><span class="sxs-lookup"><span data-stu-id="946cc-127">In Dynamics 365 for Finance and Operations version 8.0 (April 2018), you can modify the chart of accounts delimiter from the **General ledger parameters** page.</span></span>

<span data-ttu-id="946cc-128">Рекомендуется связать счета ГК с категориями счета ГК, чтобы можно было воспользоваться преимуществами финансовых отчетов по умолчанию без внесения изменений.</span><span class="sxs-lookup"><span data-stu-id="946cc-128">It's a good idea to link the main accounts to main account categories, so that you can take advantage of the default financial reports without having to make any modifications.</span></span> <span data-ttu-id="946cc-129">Поэтому, вы сможете быстро и легко создавать и вести отчеты.</span><span class="sxs-lookup"><span data-stu-id="946cc-129">Therefore, you can more quickly and easily design and maintain reports.</span></span>

<span data-ttu-id="946cc-130">Структура счетов создается на странице **Настройка структур счета**.</span><span class="sxs-lookup"><span data-stu-id="946cc-130">You create account structures on the **Configure account structures** page.</span></span> <span data-ttu-id="946cc-131">Структуры счетов определяют допустимые комбинации.</span><span class="sxs-lookup"><span data-stu-id="946cc-131">Account structures define valid combinations.</span></span> <span data-ttu-id="946cc-132">Эти сочетания вместе со счетами ГК формируют план счетов.</span><span class="sxs-lookup"><span data-stu-id="946cc-132">These combinations, together with main accounts, form a chart of accounts.</span></span> <span data-ttu-id="946cc-133">Дополнительные сведения см. в разделе [Создание структур счетов](tasks/create-account-structures.md).</span><span class="sxs-lookup"><span data-stu-id="946cc-133">For more information, see [Create account structures](tasks/create-account-structures.md).</span></span>

<span data-ttu-id="946cc-134">**Переопределения юридического лица**</span><span class="sxs-lookup"><span data-stu-id="946cc-134">**Legal entity overrides**</span></span>

<span data-ttu-id="946cc-135">Не все счета ГК действительны для всех юридических лиц, и некоторые счета ГК могут действовать только в определенный период времени.</span><span class="sxs-lookup"><span data-stu-id="946cc-135">Not all main accounts are valid for all legal entities, and some main account might be relevant only for a specific period.</span></span> <span data-ttu-id="946cc-136">В этом сценарии можно использовать раздел **Переопределения юридического лица** для идентификации компаний, для которых счет ГК должен быть приостановлен, для идентификации владельца и для указания периода времени, в течение которого активна аналитика.</span><span class="sxs-lookup"><span data-stu-id="946cc-136">In this scenario, you can use the **Legal entity overrides** section to identify the companies that the main account should be suspended for, the owner, and the period when the dimension is active.</span></span> <span data-ttu-id="946cc-137">Переопределения на общем уровне не могут быть в большей степени ограничивающими, чем переопределения на уровне юридического лица.</span><span class="sxs-lookup"><span data-stu-id="946cc-137">The overrides at the shared level can't be more restrictive than the overrides at the legal entity level.</span></span>

<span data-ttu-id="946cc-138">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="946cc-138">For more information, see the following topics:</span></span>

- [<span data-ttu-id="946cc-139">Финансовые аналитики</span><span class="sxs-lookup"><span data-stu-id="946cc-139">Financial dimensions</span></span>](financial-dimensions.md)
- [<span data-ttu-id="946cc-140">Создание и назначение структур дополнительных правил</span><span class="sxs-lookup"><span data-stu-id="946cc-140">Create and assign advanced rule structures</span></span>](tasks/create-assign-advanced-rule-structures.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]