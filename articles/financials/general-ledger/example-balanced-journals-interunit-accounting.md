---
title: Сбалансированные журналы для внутрихолдингового учета
description: В этой статье показано, как журнал автоматически балансируется, когда на странице "Книга учета" выбрана финансовая аналитика балансировки.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e84d96b5467b38e07a9ed31f142c27b638289284
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839361"
---
# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="fc064-103">Сбалансированные журналы для внутрихолдингового учета</span><span class="sxs-lookup"><span data-stu-id="fc064-103">Balanced journals for interunit accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc064-104">В этой статье показано, как журнал автоматически балансируется, когда на странице "Книга учета" выбрана финансовая аналитика балансировки.</span><span class="sxs-lookup"><span data-stu-id="fc064-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="fc064-105">Если записи счета не сбалансированы на уровне значений финансовых аналитик, дополнительные учетные записи создаются автоматически, чтобы сбалансировать этот журнал.</span><span class="sxs-lookup"><span data-stu-id="fc064-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="fc064-106">Эти записи счета используют типы разноски **Внутрихолдинговый дебет** и **Внутрихолдинговый кредит** на странице **Счета для автоматических проводок**, чтобы определить счет ГК.</span><span class="sxs-lookup"><span data-stu-id="fc064-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="fc064-107">Например, "Бизнес-единица", который является вторым сегментом счета ГК, выбирается в качестве финансовой аналитики балансировки, и подготавливаются к созданию следующие записи учета.</span><span class="sxs-lookup"><span data-stu-id="fc064-107">For example, Business Unit, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="fc064-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="fc064-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="fc064-109">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="fc064-109">100.00 DR</span></span> |
| <span data-ttu-id="fc064-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="fc064-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="fc064-111">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="fc064-111">100.00 DR</span></span> |
| <span data-ttu-id="fc064-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="fc064-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="fc064-113">200,00 CR</span><span class="sxs-lookup"><span data-stu-id="fc064-113">200.00 CR</span></span> |

<span data-ttu-id="fc064-114">В этом случае определяются следующие сальдо:</span><span class="sxs-lookup"><span data-stu-id="fc064-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="fc064-115">Для бизнес-единицы MSP = 100,00 CR</span><span class="sxs-lookup"><span data-stu-id="fc064-115">For Business Unit MSP = 100.00 CR</span></span>
-   <span data-ttu-id="fc064-116">Для бизнес-единицы NY = 100,00 DR</span><span class="sxs-lookup"><span data-stu-id="fc064-116">For Business Unit NY = 100.00 DR</span></span>

<span data-ttu-id="fc064-117">Таким образом, следующие учетные записи создаются автоматически для балансировки журнала на уровне значений финансовых аналитик.</span><span class="sxs-lookup"><span data-stu-id="fc064-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="fc064-118">(Внутрихолдинговый дебет) – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="fc064-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="fc064-119">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="fc064-119">100.00 DR</span></span> |
| <span data-ttu-id="fc064-120">(Внутрихолдинговый кредит) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="fc064-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="fc064-121">100,00 CR</span><span class="sxs-lookup"><span data-stu-id="fc064-121">100.00 CR</span></span> |





