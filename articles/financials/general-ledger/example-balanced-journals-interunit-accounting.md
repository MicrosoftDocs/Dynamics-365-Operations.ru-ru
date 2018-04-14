---
title: "Сбалансированные журналы для внутрихолдингового учета"
description: "В этой статье показано, как журнал автоматически балансируется, когда на странице \"Книга учета\" выбрана финансовая аналитика балансировки."
author: twheeloc
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 74a55b66df63f84c6cb6926b56c4b7395b895740
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---

# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="14ba5-103">Сбалансированные журналы для внутрихолдингового учета</span><span class="sxs-lookup"><span data-stu-id="14ba5-103">Balanced journals for interunit accounting</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="14ba5-104">В этой статье показано, как журнал автоматически балансируется, когда на странице "Книга учета" выбрана финансовая аналитика балансировки.</span><span class="sxs-lookup"><span data-stu-id="14ba5-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="14ba5-105">Если записи счета не сбалансированы на уровне значений финансовых аналитик, дополнительные учетные записи создаются автоматически, чтобы сбалансировать этот журнал.</span><span class="sxs-lookup"><span data-stu-id="14ba5-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="14ba5-106">Эти записи счета используют типы разноски **Внутрихолдинговый дебет** и **Внутрихолдинговый кредит** на странице **Счета для автоматических проводок**, чтобы определить счет ГК.</span><span class="sxs-lookup"><span data-stu-id="14ba5-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="14ba5-107">Например, "Бизнес-единица", который является вторым сегментом счета ГК, выбирается в качестве финансовой аналитики балансировки, и подготавливаются к созданию следующие записи учета.</span><span class="sxs-lookup"><span data-stu-id="14ba5-107">For example, Business Unit, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="14ba5-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="14ba5-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="14ba5-109">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="14ba5-109">100.00 DR</span></span> |
| <span data-ttu-id="14ba5-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="14ba5-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="14ba5-111">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="14ba5-111">100.00 DR</span></span> |
| <span data-ttu-id="14ba5-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="14ba5-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="14ba5-113">200,00 CR</span><span class="sxs-lookup"><span data-stu-id="14ba5-113">200.00 CR</span></span> |

<span data-ttu-id="14ba5-114">В этом случае определяются следующие сальдо:</span><span class="sxs-lookup"><span data-stu-id="14ba5-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="14ba5-115">Для бизнес-единицы MSP = 100,00 CR</span><span class="sxs-lookup"><span data-stu-id="14ba5-115">For Business Unit MSP = 100.00 CR</span></span>
-   <span data-ttu-id="14ba5-116">Для бизнес-единицы NY = 100,00 DR</span><span class="sxs-lookup"><span data-stu-id="14ba5-116">For Business Unit NY = 100.00 DR</span></span>

<span data-ttu-id="14ba5-117">Таким образом, следующие учетные записи создаются автоматически для балансировки журнала на уровне значений финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="14ba5-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="14ba5-118">(Внутрихолдинговый дебет) – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="14ba5-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="14ba5-119">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="14ba5-119">100.00 DR</span></span> |
| <span data-ttu-id="14ba5-120">(Внутрихолдинговый кредит) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="14ba5-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="14ba5-121">100,00 CR</span><span class="sxs-lookup"><span data-stu-id="14ba5-121">100.00 CR</span></span> |






