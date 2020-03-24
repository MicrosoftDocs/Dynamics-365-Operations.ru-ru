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
ms.openlocfilehash: d9bcec1d4bb0207a2c3e0d46f7661b666fea3736
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112222"
---
# <a name="integrated-ledger"></a><span data-ttu-id="a88f6-103">Интегрированная книга учета</span><span class="sxs-lookup"><span data-stu-id="a88f6-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="a88f6-104">В бизнес-приложении данные главной книги определяют основные настройки для ведения бизнеса компании.</span><span class="sxs-lookup"><span data-stu-id="a88f6-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="a88f6-105">Например, данные ГК описывают финансовый год, который используется в компании, валюты, которые она использует, и счета, используемые в ней.</span><span class="sxs-lookup"><span data-stu-id="a88f6-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="a88f6-106">В этом разделе описывается интеграция этих основных финансовых данных.</span><span class="sxs-lookup"><span data-stu-id="a88f6-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="a88f6-107">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="a88f6-107">Templates</span></span>

<span data-ttu-id="a88f6-108">Данные ГК включают коллекцию сопоставлений основных финансовых объектов, которые работают совместно во время взаимодействия данных клиентов, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a88f6-108">Ledger data includes a collection of core financial entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="a88f6-109">Приложения Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a88f6-109">Finance and Operations apps</span></span>      | <span data-ttu-id="a88f6-110">Приложение на основе модели в Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a88f6-110">Model-driven app in Dynamics 365</span></span> | <span data-ttu-id="a88f6-111">описание</span><span class="sxs-lookup"><span data-stu-id="a88f6-111">Description</span></span>
---------------------------------|----------------------------------|------------
<span data-ttu-id="a88f6-112">Валюты</span><span class="sxs-lookup"><span data-stu-id="a88f6-112">Currencies</span></span>                       | <span data-ttu-id="a88f6-113">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="a88f6-113">transactioncurrencies</span></span>            |
<span data-ttu-id="a88f6-114">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="a88f6-114">FiscalCalendar</span></span>                   | <span data-ttu-id="a88f6-115">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="a88f6-115">msdyn\_fiscalcalendars</span></span>        |
<span data-ttu-id="a88f6-116">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="a88f6-116">FiscalCalendarYear</span></span>               | <span data-ttu-id="a88f6-117">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="a88f6-117">msdyn\_fiscalcalendaryears</span></span>        |
<span data-ttu-id="a88f6-118">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="a88f6-118">ExchRateType</span></span>                     | <span data-ttu-id="a88f6-119">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="a88f6-119">msdyn\_exchangeratetypes</span></span>        |
<span data-ttu-id="a88f6-120">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="a88f6-120">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="a88f6-121">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="a88f6-121">msdyn\_currencyexchangeratepairs</span></span>        |
<span data-ttu-id="a88f6-122">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="a88f6-122">FiscalPeriodEntity</span></span>               | <span data-ttu-id="a88f6-123">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="a88f6-123">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="a88f6-124">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="a88f6-124">MainAccountCategory</span></span>              | <span data-ttu-id="a88f6-125">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="a88f6-125">msdyn\_mainaccountcategory</span></span>        |
<span data-ttu-id="a88f6-126">MainAccount</span><span class="sxs-lookup"><span data-stu-id="a88f6-126">MainAccount</span></span>                      | <span data-ttu-id="a88f6-127">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="a88f6-127">msdyn\_mainaccounts</span></span>        |
<span data-ttu-id="a88f6-128">Главная книга</span><span class="sxs-lookup"><span data-stu-id="a88f6-128">Ledger</span></span>                           | <span data-ttu-id="a88f6-129">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="a88f6-129">msdyn\_ledgers</span></span>        |
<span data-ttu-id="a88f6-130">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="a88f6-130">ExchangeRates</span></span>                    | <span data-ttu-id="a88f6-131">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="a88f6-131">msdyn\_currencyexchangerates</span></span>        |
<span data-ttu-id="a88f6-132">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="a88f6-132">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="a88f6-133">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="a88f6-133">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="a88f6-134">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="a88f6-134">DimensionAttributeEntity</span></span>         | <span data-ttu-id="a88f6-135">msdyn\_dimensionattributes</span><span class="sxs-lookup"><span data-stu-id="a88f6-135">msdyn\_dimensionattributes</span></span>        |
<span data-ttu-id="a88f6-136">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="a88f6-136">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="a88f6-137">msdyn\_financialdimensionformats</span><span class="sxs-lookup"><span data-stu-id="a88f6-137">msdyn\_financialdimensionformats</span></span>        |
<span data-ttu-id="a88f6-138">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="a88f6-138">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="a88f6-139">msdyn\_chartofaccounts</span><span class="sxs-lookup"><span data-stu-id="a88f6-139">msdyn\_chartofaccounts</span></span>        |


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




