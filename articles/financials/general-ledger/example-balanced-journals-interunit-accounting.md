---
title: "Сбалансированные журналы для внутрихолдингового учета"
description: "В этой статье показано, как журнал автоматически балансируется, когда на странице \"Книга учета\" выбрана финансовая аналитика балансировки."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f45d180dc8dcafb0579e76b890dd5d516df5b8c0
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="1d018-103">Сбалансированные журналы для внутрихолдингового учета</span><span class="sxs-lookup"><span data-stu-id="1d018-103">Balanced journals for interunit accounting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1d018-104">В этой статье показано, как журнал автоматически балансируется, когда на странице "Книга учета" выбрана финансовая аналитика балансировки.</span><span class="sxs-lookup"><span data-stu-id="1d018-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="1d018-105">Если записи счета не сбалансированы на уровне значений финансовых аналитик, дополнительные учетные записи создаются автоматически, чтобы сбалансировать этот журнал.</span><span class="sxs-lookup"><span data-stu-id="1d018-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="1d018-106">Эти записи счета используют типы разноски **Внутрихолдинговый дебет** и **Внутрихолдинговый кредит** на странице **Счета для автоматических проводок**, чтобы определить счет ГК.</span><span class="sxs-lookup"><span data-stu-id="1d018-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="1d018-107">Например, "Филиал", который является вторым сегментом счета ГК, выбирается в качестве финансовой аналитики балансировки, и подготавливаются к созданию следующие записи учета.</span><span class="sxs-lookup"><span data-stu-id="1d018-107">For example, Branch, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="1d018-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="1d018-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="1d018-109">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="1d018-109">100.00 DR</span></span> |
| <span data-ttu-id="1d018-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="1d018-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="1d018-111">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="1d018-111">100.00 DR</span></span> |
| <span data-ttu-id="1d018-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="1d018-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="1d018-113">200,00 CR</span><span class="sxs-lookup"><span data-stu-id="1d018-113">200.00 CR</span></span> |

<span data-ttu-id="1d018-114">В этом случае определяются следующие сальдо:</span><span class="sxs-lookup"><span data-stu-id="1d018-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="1d018-115">Для филиала MSP = 100,00 CR</span><span class="sxs-lookup"><span data-stu-id="1d018-115">For Branch MSP = 100.00 CR</span></span>
-   <span data-ttu-id="1d018-116">Для филиала NY = 100,00 DR</span><span class="sxs-lookup"><span data-stu-id="1d018-116">For Branch NY = 100.00 DR</span></span>

<span data-ttu-id="1d018-117">Таким образом, следующие учетные записи создаются автоматически для балансировки журнала на уровне значений финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="1d018-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="1d018-118">(Внутрихолдинговый дебет) – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="1d018-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="1d018-119">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="1d018-119">100.00 DR</span></span> |
| <span data-ttu-id="1d018-120">(Внутрихолдинговый кредит) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="1d018-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="1d018-121">100,00 CR</span><span class="sxs-lookup"><span data-stu-id="1d018-121">100.00 CR</span></span> |






