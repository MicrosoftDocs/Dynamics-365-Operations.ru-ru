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
ms.openlocfilehash: 6f1a1c7329f0936147fb8f7a8e0e9fea14f7dd4b
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173023"
---
# <a name="integrated-ledger"></a><span data-ttu-id="615d3-103">Интегрированная книга учета</span><span class="sxs-lookup"><span data-stu-id="615d3-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="615d3-104">В бизнес-приложении данные главной книги определяют основные настройки для ведения бизнеса компании.</span><span class="sxs-lookup"><span data-stu-id="615d3-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="615d3-105">Например, данные ГК описывают финансовый год, который используется в компании, валюты, которые она использует, и счета, используемые в ней.</span><span class="sxs-lookup"><span data-stu-id="615d3-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="615d3-106">В этом разделе описывается интеграция этих основных финансовых данных.</span><span class="sxs-lookup"><span data-stu-id="615d3-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="615d3-107">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="615d3-107">Templates</span></span>

<span data-ttu-id="615d3-108">Данные ГК включают коллекцию сопоставлений основных финансовых объектов, которые работают совместно во время взаимодействия данных клиентов, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="615d3-108">Ledger data includes a collection of core financial entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="615d3-109">Приложения Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="615d3-109">Finance and Operations apps</span></span>      | <span data-ttu-id="615d3-110">Приложение на основе модели в Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="615d3-110">Model-driven app in Dynamics 365</span></span> | <span data-ttu-id="615d3-111">описание</span><span class="sxs-lookup"><span data-stu-id="615d3-111">Description</span></span>
---------------------------------|----------------------------------|------------
<span data-ttu-id="615d3-112">Валюты</span><span class="sxs-lookup"><span data-stu-id="615d3-112">Currencies</span></span>                       | <span data-ttu-id="615d3-113">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="615d3-113">transactioncurrencies</span></span>            |
<span data-ttu-id="615d3-114">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="615d3-114">FiscalCalendar</span></span>                   | <span data-ttu-id="615d3-115">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="615d3-115">msdyn\_fiscalcalendars</span></span>        |
<span data-ttu-id="615d3-116">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="615d3-116">FiscalCalendarYear</span></span>               | <span data-ttu-id="615d3-117">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="615d3-117">msdyn\_fiscalcalendaryears</span></span>        |
<span data-ttu-id="615d3-118">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="615d3-118">ExchRateType</span></span>                     | <span data-ttu-id="615d3-119">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="615d3-119">msdyn\_exchangeratetypes</span></span>        |
<span data-ttu-id="615d3-120">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="615d3-120">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="615d3-121">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="615d3-121">msdyn\_currencyexchangeratepairs</span></span>        |
<span data-ttu-id="615d3-122">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="615d3-122">FiscalPeriodEntity</span></span>               | <span data-ttu-id="615d3-123">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="615d3-123">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="615d3-124">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="615d3-124">MainAccountCategory</span></span>              | <span data-ttu-id="615d3-125">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="615d3-125">msdyn\_mainaccountcategory</span></span>        |
<span data-ttu-id="615d3-126">MainAccount</span><span class="sxs-lookup"><span data-stu-id="615d3-126">MainAccount</span></span>                      | <span data-ttu-id="615d3-127">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="615d3-127">msdyn\_mainaccounts</span></span>        |
<span data-ttu-id="615d3-128">Главная книга</span><span class="sxs-lookup"><span data-stu-id="615d3-128">Ledger</span></span>                           | <span data-ttu-id="615d3-129">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="615d3-129">msdyn\_ledgers</span></span>        |
<span data-ttu-id="615d3-130">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="615d3-130">ExchangeRates</span></span>                    | <span data-ttu-id="615d3-131">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="615d3-131">msdyn\_currencyexchangerates</span></span>        |
<span data-ttu-id="615d3-132">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="615d3-132">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="615d3-133">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="615d3-133">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="615d3-134">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="615d3-134">DimensionAttributeEntity</span></span>         | <span data-ttu-id="615d3-135">msdyn\_dimensionattributes</span><span class="sxs-lookup"><span data-stu-id="615d3-135">msdyn\_dimensionattributes</span></span>        |
<span data-ttu-id="615d3-136">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="615d3-136">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="615d3-137">msdyn\_financialdimensionformats</span><span class="sxs-lookup"><span data-stu-id="615d3-137">msdyn\_financialdimensionformats</span></span>        |
<span data-ttu-id="615d3-138">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="615d3-138">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="615d3-139">msdyn\_chartofaccounts</span><span class="sxs-lookup"><span data-stu-id="615d3-139">msdyn\_chartofaccounts</span></span>        |


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Currency](includes/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](includes/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](includes/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](includes/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](includes/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Ledger fiscal periods](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Main account category](includes/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](includes/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](includes/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](includes/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](includes/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](includes/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](includes/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]




