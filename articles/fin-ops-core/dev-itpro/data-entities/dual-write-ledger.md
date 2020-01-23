---
title: Интегрированная ГК
description: В этом разделе описывается интеграция данных ГК между Finance and Operations и другими приложениями Dynamics 365 с помощью Common Data Service.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 4a0a8f2f52cf9a73efc3557b63793201a7a3f8b8
ms.sourcegitcommit: d0322d1ed6c798301058e44dae76227a0e1f49ac
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853890"
---
# <a name="integrated-ledger"></a><span data-ttu-id="79b80-103">Интегрированная книга учета</span><span class="sxs-lookup"><span data-stu-id="79b80-103">Integrated ledger</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="79b80-104">В бизнес-приложении данные главной книги определяют основные настройки для ведения бизнеса компании.</span><span class="sxs-lookup"><span data-stu-id="79b80-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="79b80-105">Например, данные ГК описывают финансовый год, который используется в компании, валюты, которые она использует, и счета, используемые в ней.</span><span class="sxs-lookup"><span data-stu-id="79b80-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="79b80-106">В этом разделе описывается интеграция этих основных финансовых данных.</span><span class="sxs-lookup"><span data-stu-id="79b80-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="79b80-107">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="79b80-107">Templates</span></span>

<span data-ttu-id="79b80-108">Данные ГК включают коллекцию сопоставлений основных финансовых объектов, которые работают совместно во время взаимодействия данных клиентов, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="79b80-108">Ledger data includes a collection of core financial entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="79b80-109">Приложения Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="79b80-109">Finance and Operations apps</span></span>      | <span data-ttu-id="79b80-110">Другие приложения Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="79b80-110">Other Dynamics 365 apps</span></span>
---------------------------------|---------------------------------
<span data-ttu-id="79b80-111">Валюты</span><span class="sxs-lookup"><span data-stu-id="79b80-111">Currencies</span></span>                       | <span data-ttu-id="79b80-112">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="79b80-112">transactioncurrencies</span></span>
<span data-ttu-id="79b80-113">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="79b80-113">FiscalCalendar</span></span>                   | <span data-ttu-id="79b80-114">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="79b80-114">msdyn\_fiscalcalendars</span></span>
<span data-ttu-id="79b80-115">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="79b80-115">FiscalCalendarYear</span></span>               | <span data-ttu-id="79b80-116">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="79b80-116">msdyn\_fiscalcalendaryears</span></span>
<span data-ttu-id="79b80-117">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="79b80-117">ExchRateType</span></span>                     | <span data-ttu-id="79b80-118">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="79b80-118">msdyn\_exchangeratetypes</span></span>
<span data-ttu-id="79b80-119">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="79b80-119">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="79b80-120">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="79b80-120">msdyn\_currencyexchangeratepairs</span></span>
<span data-ttu-id="79b80-121">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="79b80-121">FiscalPeriodEntity</span></span>               | <span data-ttu-id="79b80-122">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="79b80-122">msdyn\_fiscalcalendarperiods</span></span>
<span data-ttu-id="79b80-123">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="79b80-123">MainAccountCategory</span></span>              | <span data-ttu-id="79b80-124">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="79b80-124">msdyn\_mainaccountcategory</span></span>
<span data-ttu-id="79b80-125">MainAccount</span><span class="sxs-lookup"><span data-stu-id="79b80-125">MainAccount</span></span>                      | <span data-ttu-id="79b80-126">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="79b80-126">msdyn\_mainaccounts</span></span>
<span data-ttu-id="79b80-127">Главная книга</span><span class="sxs-lookup"><span data-stu-id="79b80-127">Ledger</span></span>                           | <span data-ttu-id="79b80-128">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="79b80-128">msdyn\_ledgers</span></span>
<span data-ttu-id="79b80-129">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="79b80-129">ExchangeRates</span></span>                    | <span data-ttu-id="79b80-130">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="79b80-130">msdyn\_currencyexchangerates</span></span>
<span data-ttu-id="79b80-131">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="79b80-131">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="79b80-132">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="79b80-132">msdyn\_fiscalcalendarperiods</span></span>
<span data-ttu-id="79b80-133">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="79b80-133">DimensionAttributeEntity</span></span>         | <span data-ttu-id="79b80-134">msdyn\_dimensionattributes.md</span><span class="sxs-lookup"><span data-stu-id="79b80-134">msdyn\_dimensionattributes.md</span></span>
<span data-ttu-id="79b80-135">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="79b80-135">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="79b80-136">msdyn\_financialdimensionformats.md</span><span class="sxs-lookup"><span data-stu-id="79b80-136">msdyn\_financialdimensionformats.md</span></span>
<span data-ttu-id="79b80-137">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="79b80-137">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="79b80-138">msdyn\_chartofaccounts.md</span><span class="sxs-lookup"><span data-stu-id="79b80-138">msdyn\_chartofaccounts.md</span></span>


[!include [banner](../includes/dual-write-symbols.md)]

[!include [Currency](dual-write/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](dual-write/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](dual-write/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](dual-write/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](dual-write/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Ledger fiscal periods](dual-write/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Main account category](dual-write/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](dual-write/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](dual-write/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](dual-write/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](dual-write/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](dual-write/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](dual-write/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](dual-write/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]




