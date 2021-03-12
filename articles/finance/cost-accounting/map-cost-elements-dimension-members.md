---
title: Сопоставление элементов аналитики элемента затрат с общим набором элементов аналитики
description: Сопоставив различные члены аналитики элемента затрат общему набору членов аналитики элемента затрат, можно объединить данные в общий формат для целей анализа.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMDimensionMember, CAMDimensionMapping
audience: Application User
ms.reviewer: roschlom
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 79b235af60e452b80d99c13a2fc80d322a02fc04
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976174"
---
# <a name="map-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a><span data-ttu-id="af1a5-103">Сопоставление элементов аналитики элемента затрат с общим набором элементов аналитики</span><span class="sxs-lookup"><span data-stu-id="af1a5-103">Map cost element dimension members to a common set of dimension members</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="af1a5-104">Сопоставив различные члены аналитики элемента затрат общему набору членов аналитики элемента затрат, можно объединить данные в общий формат для целей анализа.</span><span class="sxs-lookup"><span data-stu-id="af1a5-104">By mapping different cost element dimension members to a common set of cost element dimension members, you merge data into a common format for analysis purposes.</span></span>

<span data-ttu-id="af1a5-105">Если вы глобальная компания и соответствуете предписанным законом правилам бухгалтерской отчетности, вы можете использовать несколько планов счетов.</span><span class="sxs-lookup"><span data-stu-id="af1a5-105">If you're a global company and comply with statutory accounting requirements, you might use multiple charts of accounts.</span></span> <span data-ttu-id="af1a5-106">Импорт членов аналитики элемента затрат из различных планов счетов может привести к смешиванию счетов.</span><span class="sxs-lookup"><span data-stu-id="af1a5-106">When you import cost element dimension members from different charts of accounts, you can end up with a mix of accounts.</span></span> <span data-ttu-id="af1a5-107">Однако фактически эти счета могут иметь одинаковую природу, и вы можете захотеть проанализировать и распределить затрат для них, используя общий формат.</span><span class="sxs-lookup"><span data-stu-id="af1a5-107">However, these accounts might actually have the same nature, and you might want to analyze and allocate costs for them by using a common format.</span></span>

## <a name="map-cost-element-dimension-members-to-a-common-format"></a><span data-ttu-id="af1a5-108">Сопоставление членов аналитики элемента издержек с общим форматом</span><span class="sxs-lookup"><span data-stu-id="af1a5-108">Map cost element dimension members to a common format</span></span>
<span data-ttu-id="af1a5-109">В следующем примере показано, как контролер затрат может создать новую аналитику элемента затрат в модуле учета затрат, которая сопоставляет члены аналитики элемента издержек из структуры плана счетов для США и структурой плана счетов для Франции общему набору членов аналитики элемента затрат.</span><span class="sxs-lookup"><span data-stu-id="af1a5-109">The following example shows how you, as a cost controller, can create a new cost element dimension in Cost accounting that maps cost element dimension members from the US chart of accounts structure and the French chart of accounts structure to a common set of cost element dimension members.</span></span> <span data-ttu-id="af1a5-110">Затем можно использовать общий набор членов аналитики элемента затрат для анализа данных по затратам из двух юридических лиц в книге учета затрат.</span><span class="sxs-lookup"><span data-stu-id="af1a5-110">You can then use the common set of cost element dimension members to analyze cost data from the two legal entities in a cost accounting ledger.</span></span>

| <span data-ttu-id="af1a5-111">Источник: план счетов для США</span><span class="sxs-lookup"><span data-stu-id="af1a5-111">Source: US chart of accounts</span></span>                                          | <span data-ttu-id="af1a5-112">Источник: план счетов для Франции</span><span class="sxs-lookup"><span data-stu-id="af1a5-112">Source: French chart of accounts</span></span>                                          | <span data-ttu-id="af1a5-113">Новый общий набор членов аналитики элемента затрат</span><span class="sxs-lookup"><span data-stu-id="af1a5-113">New common set of cost element dimension members</span></span>                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="af1a5-114">Импортированные члены аналитики элемента затрат из плана счетов для США</span><span class="sxs-lookup"><span data-stu-id="af1a5-114">Imported cost element dimension members from the US chart of accounts</span></span> | <span data-ttu-id="af1a5-115">Импортированные члены аналитики элемента затрат из плана счетов для Франции</span><span class="sxs-lookup"><span data-stu-id="af1a5-115">Imported cost element dimension members from the French chart of accounts</span></span> | <span data-ttu-id="af1a5-116">Сопоставление членов аналитики элемента затрат для США и Франции с общим набором</span><span class="sxs-lookup"><span data-stu-id="af1a5-116">Mapping of US and French cost element dimension members to a common set</span></span> |
| <span data-ttu-id="af1a5-117">5001: Продажи</span><span class="sxs-lookup"><span data-stu-id="af1a5-117">5001: Sales</span></span>                                                           | <span data-ttu-id="af1a5-118">5001: Продажи и маркетинг</span><span class="sxs-lookup"><span data-stu-id="af1a5-118">5001: Sales and advertising</span></span>                                               | <span data-ttu-id="af1a5-119">5000: Продажи и маркетинг</span><span class="sxs-lookup"><span data-stu-id="af1a5-119">5000: Sales and advertising</span></span>                                             |
| <span data-ttu-id="af1a5-120">5030: Реклама</span><span class="sxs-lookup"><span data-stu-id="af1a5-120">5030: Advertising</span></span>                                                     | <span data-ttu-id="af1a5-121">6390: Покупка запасов\*</span><span class="sxs-lookup"><span data-stu-id="af1a5-121">6390: Stock purchase\*</span></span>                                                    | <span data-ttu-id="af1a5-122">7000: Расходы по уборке</span><span class="sxs-lookup"><span data-stu-id="af1a5-122">7000: Cleaning expenses</span></span>                                                 |
| <span data-ttu-id="af1a5-123">7001: Расходы по уборке</span><span class="sxs-lookup"><span data-stu-id="af1a5-123">7001: Cleaning expenses</span></span>                                               | <span data-ttu-id="af1a5-124">7001: Командировочные расходы</span><span class="sxs-lookup"><span data-stu-id="af1a5-124">7001: Travel expense</span></span>                                                      | <span data-ttu-id="af1a5-125">7001: Командировочные расходы</span><span class="sxs-lookup"><span data-stu-id="af1a5-125">7001: Travel expenses</span></span>                                                   |

<span data-ttu-id="af1a5-126">\*Член аналитики элемента затрат "Покупка запасов" для Франции не сопоставляется.</span><span class="sxs-lookup"><span data-stu-id="af1a5-126">\*The Stock purchase French cost element dimension member isn't mapped.</span></span>

## <a name="currency-conversion"></a><span data-ttu-id="af1a5-127">Конвертация валюты</span><span class="sxs-lookup"><span data-stu-id="af1a5-127">Currency conversion</span></span>
<span data-ttu-id="af1a5-128">Различные планы счетов, которые используются, могут быть настроены для использования различных валют.</span><span class="sxs-lookup"><span data-stu-id="af1a5-128">The various charts of accounts that you use might be set up to use different currencies.</span></span> <span data-ttu-id="af1a5-129">В этом случае обязательно укажите конвертацию валюты, чтобы данные о затратах обрабатывались с помощью правильной валюты, как определено в книге учета затрат, где члены аналитика элемента затрат используются.</span><span class="sxs-lookup"><span data-stu-id="af1a5-129">In this case, be sure to specify a currency conversion, so that cost data is processed by using the correct currency, as defined in the cost accounting ledger where the cost element dimension members are used.</span></span> <span data-ttu-id="af1a5-130">В предыдущем примере, если доллары США (USD) используются в книге учета затрат, необходимо создать конвертацию валюты из USD в евро (EUR) для обработки проводок для сопоставленных членов аналитики элемента затрат.</span><span class="sxs-lookup"><span data-stu-id="af1a5-130">In the preceding example, if US dollars (USD) are used in the cost accounting ledger, you must create a currency conversion from USD to euros (EUR) to process transactions for the mapped cost element dimension members.</span></span>

## <a name="update-mappings-at-any-time"></a><span data-ttu-id="af1a5-131">Обновление сопоставлений в любое время</span><span class="sxs-lookup"><span data-stu-id="af1a5-131">Update mappings at any time</span></span>
<span data-ttu-id="af1a5-132">Можно обновить определения сопоставления для аналитики элемента затрат в любое время.</span><span class="sxs-lookup"><span data-stu-id="af1a5-132">You can update the mapping definitions for a cost element dimension at any time.</span></span> <span data-ttu-id="af1a5-133">Поскольку сопоставления не имеют даты вступления в силу, изменения будут применены в следующий раз, когда будут обрабатываться проводки затрат или выполняться расчеты затрат.</span><span class="sxs-lookup"><span data-stu-id="af1a5-133">Because mappings aren't date-effective, changes are applied the next time that you process cost transactions or run cost calculations.</span></span>



