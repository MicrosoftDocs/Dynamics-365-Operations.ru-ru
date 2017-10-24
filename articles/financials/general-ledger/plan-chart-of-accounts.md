---
title: "Планирование плана счетов"
description: "Эта статья представляет информацию, которая поможет запланировать плана счетов для вашей организации."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 848da7ec8f4a7915f3b78945b808b564f4510434
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="plan-your-chart-of-accounts"></a><span data-ttu-id="20585-103">Планирование плана счетов</span><span class="sxs-lookup"><span data-stu-id="20585-103">Plan your chart of accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="20585-104">Эта статья представляет информацию, которая поможет запланировать плана счетов для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="20585-104">This article provides information that will help you plan the chart of accounts for your organization.</span></span>

<span data-ttu-id="20585-105">Для того, чтобы отслеживать и вести финансовые сведения в организации, вы можете настроить план счетов.</span><span class="sxs-lookup"><span data-stu-id="20585-105">To track and maintain financial information in an organization, you can set up a chart of accounts.</span></span> <span data-ttu-id="20585-106">План счетов — это собрание счетов, которые определяют финансовые структуры.</span><span class="sxs-lookup"><span data-stu-id="20585-106">A chart of accounts is a collection of accounts that define a financial framework.</span></span> <span data-ttu-id="20585-107">Для дополнительного отслеживания проводок по этим счетам добавляются сегменты, которые называются финансовыми аналитиками.</span><span class="sxs-lookup"><span data-stu-id="20585-107">To further track the transactions in these accounts, you can add segments, which are known as financial dimensions.</span></span> <span data-ttu-id="20585-108">Например, счет расходов может включать финансовые аналитики с названиями "Подразделение", "Центр затрат" и "Назначение".</span><span class="sxs-lookup"><span data-stu-id="20585-108">For example, an expense account might include financial dimensions that are named Department, Cost center, and Purpose.</span></span> <span data-ttu-id="20585-109">Определяемые пользователем правила, которые называются структурами счетов и расширенными правилами, указывают, как эти финансовые аналитики связываются со счетами ГК и другими финансовыми аналитиками, и как проводки можно вводить.</span><span class="sxs-lookup"><span data-stu-id="20585-109">User-defined rules, which are known as account structures and advanced rules, determine how financial dimensions are attached to the main accounts and other financial dimensions, and also how transactions are entered.</span></span> 

<span data-ttu-id="20585-110">План счетов представляет собой структурированный список счетов ГК юридического лица.</span><span class="sxs-lookup"><span data-stu-id="20585-110">The chart of accounts is a structured list of a legal entity’s general ledger accounts.</span></span> <span data-ttu-id="20585-111">Список используется для подготовки отчетов ГК для органов власти и для собственников.</span><span class="sxs-lookup"><span data-stu-id="20585-111">The list is used to prepare financial reports for authorities and owners.</span></span> <span data-ttu-id="20585-112">Счета группируются по типам счетов, а затем агрегируются по более широким категориям.</span><span class="sxs-lookup"><span data-stu-id="20585-112">The accounts are grouped into types of accounts and then further aggregated into larger categories.</span></span> <span data-ttu-id="20585-113">Самым общим видом группировки является группировка по выручке и затратам (текущие счета), а также активам и пассивам (балансовые счета).</span><span class="sxs-lookup"><span data-stu-id="20585-113">At the most general level, the accounts are grouped as revenues and costs (operating accounts), and assets and liabilities (balance accounts).</span></span> 

<span data-ttu-id="20585-114">План счетов может быть предоставлен для совместного доступа и использован любым юридическим лицом в организации.</span><span class="sxs-lookup"><span data-stu-id="20585-114">A chart of accounts can be shared and used by any legal entity in an organization.</span></span> <span data-ttu-id="20585-115">План счетов, используемый юридическим лицом, определяется на странице **Книга учета**.</span><span class="sxs-lookup"><span data-stu-id="20585-115">The chart of accounts that is used by a legal entity is defined on the **Ledger** page.</span></span> 

<span data-ttu-id="20585-116">Здесь указаны некоторые факторы, которые следует учесть при планировании структуры плана счетов для своей организации:</span><span class="sxs-lookup"><span data-stu-id="20585-116">Here are some of the factors that you must consider when you plan the structure of the chart of accounts for your organization:</span></span>

-   <span data-ttu-id="20585-117">Требования к отчетности, существующие в стране/регионе, где базируется организация</span><span class="sxs-lookup"><span data-stu-id="20585-117">The reporting requirements of the country/region where your organization is based</span></span>
-   <span data-ttu-id="20585-118">Требования к отчетности вашего юридического лица</span><span class="sxs-lookup"><span data-stu-id="20585-118">The reporting requirements of your legal entity</span></span>
-   <span data-ttu-id="20585-119">Уровень детализации, необходимый как для внешних организаций, так и для вашей организации</span><span class="sxs-lookup"><span data-stu-id="20585-119">The degree of specification that is required, both for both external organizations and for your organization</span></span>

<span data-ttu-id="20585-120">Создайте план счетов на странице **План счетов**.</span><span class="sxs-lookup"><span data-stu-id="20585-120">Create the chart of accounts on the **Chart of accounts** page.</span></span> <span data-ttu-id="20585-121">Счета ГК можно создать на странице **План счетов** или на странице **Счета ГК**.</span><span class="sxs-lookup"><span data-stu-id="20585-121">Main accounts can be created from the **Chart of accounts** page or the **Main accounts** page.</span></span> <span data-ttu-id="20585-122">Для счетов ГК не должны использоваться специальные символы, которые используются как разделители в плане счетов.</span><span class="sxs-lookup"><span data-stu-id="20585-122">Your main accounts shouldn't use any special characters that are used as chart of accounts delimiters.</span></span> <span data-ttu-id="20585-123">Если у вас есть специальный символ, который аналогичен разделителю в плане счетов, возможна нестабильная работа системы или потребуется всегда использовать поиск или всплывающий элемент при вводе счета или комбинаций аналитик.</span><span class="sxs-lookup"><span data-stu-id="20585-123">If you do have a special character that is the same as your chart of accounts delimiter, you may experience instability, or the need to always use lookups or the flyout when entering account and dimension combinations.</span></span> <span data-ttu-id="20585-124">Дополнительные сведения см. в разделе [Создание счета ГК](tasks/create-account-structures.md).</span><span class="sxs-lookup"><span data-stu-id="20585-124">For more information, see [Create a main account](tasks/create-account-structures.md).</span></span>


<span data-ttu-id="20585-125">Рекомендуется связать счета ГК с категориями счета ГК, чтобы можно было воспользоваться преимуществами финансовых отчетов по умолчанию без внесения изменений.</span><span class="sxs-lookup"><span data-stu-id="20585-125">It's a good idea to link the main accounts to main account categories, so that you can take advantage of the default financial reports without having to make any modifications.</span></span> <span data-ttu-id="20585-126">Поэтому, вы сможете быстро и легко создавать и вести отчеты.</span><span class="sxs-lookup"><span data-stu-id="20585-126">Therefore, you can more quickly and easily design and maintain reports.</span></span> 

<span data-ttu-id="20585-127">Используйте страницу **Настройка структур счета** для создания структур счетов.</span><span class="sxs-lookup"><span data-stu-id="20585-127">Use the **Configure account structures** page to create account structures.</span></span> <span data-ttu-id="20585-128">Структуры счетов определяют допустимые комбинации.</span><span class="sxs-lookup"><span data-stu-id="20585-128">Account structures define valid combinations.</span></span> <span data-ttu-id="20585-129">Сочетания со счетами ГК формируют план счетов.</span><span class="sxs-lookup"><span data-stu-id="20585-129">The combinations, together with main accounts, form a chart of accounts.</span></span>  <span data-ttu-id="20585-130">Дополнительные сведения см. в разделе [Создание структур счетов](tasks/create-main-account.md).</span><span class="sxs-lookup"><span data-stu-id="20585-130">For more information, see [Create account structures](tasks/create-main-account.md).</span></span>

<span data-ttu-id="20585-131">**Переопределения юридического лица**</span><span class="sxs-lookup"><span data-stu-id="20585-131">**Legal entity overrides**</span></span> 

<span data-ttu-id="20585-132">Не все счета ГК действительны для всех юридических лиц, и некоторые могут действовать только в определенный период времени.</span><span class="sxs-lookup"><span data-stu-id="20585-132">Not all main accounts are valid for all legal entities and some may only be relevant for a specific time period.</span></span> <span data-ttu-id="20585-133">В этом сценарии раздел "Переопределения юридического лица" можно использовать для идентификации компаний, для которых счет КГ должен быть приостановлен, для идентификации владельца и для указания периода времени, в течение которого активна аналитика.</span><span class="sxs-lookup"><span data-stu-id="20585-133">In this scenario the Legal entity overrides section can be used to identify which companies the main account should be suspended for, who the owner is and the time period the dimension is active.</span></span> <span data-ttu-id="20585-134">Переопределения на общем уровне не могут быть в большей степени ограничивающими, чем переопределения на уровне юридического лица.</span><span class="sxs-lookup"><span data-stu-id="20585-134">The overrides at the shared level cannot be more restrictive than the overrides at the legal entity level.</span></span>

<span data-ttu-id="20585-135">Дополнительные сведения см. в следующих темах: [Финансовые аналитики](financial-dimensions.md)
[Создание и назначение структур дополнительных правил](tasks/create-assign-advanced-rule-structures.md)</span><span class="sxs-lookup"><span data-stu-id="20585-135">For more information, see the following topics: [Financial dimensions](financial-dimensions.md)
[Create and assign advanced rule structures](tasks/create-assign-advanced-rule-structures.md)</span></span>




