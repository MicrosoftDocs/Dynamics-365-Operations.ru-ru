---
title: Сопоставление проводок между счетами ГК
description: Ниже описан порядок сопоставления проводок между счетами ГК и отмена сопоставления ГК.
author: aprilolson
manager: AnnBe
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4aff64fa1c017f295752e913de7fb320f0662ef8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568128"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="4994f-103">Сопоставление проводок между счетами ГК</span><span class="sxs-lookup"><span data-stu-id="4994f-103">Settle transactions between ledger accounts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4994f-104">Ниже описан порядок сопоставления проводок между счетами ГК и отмена сопоставления ГК.</span><span class="sxs-lookup"><span data-stu-id="4994f-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="4994f-105">В этой процедуре используется компания с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="4994f-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="4994f-106">Сопоставление проводки между счетами ГК</span><span class="sxs-lookup"><span data-stu-id="4994f-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="4994f-107">Перейдите в раздел "Главная книга" > "Периодические задачи" > "Сопоставления ГК".</span><span class="sxs-lookup"><span data-stu-id="4994f-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="4994f-108">В списке найдите проводку, которую требуется сопоставить.</span><span class="sxs-lookup"><span data-stu-id="4994f-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="4994f-109">Сальдо должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="4994f-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="4994f-110">Щелкните "Включить".</span><span class="sxs-lookup"><span data-stu-id="4994f-110">Click Include.</span></span>
4. <span data-ttu-id="4994f-111">Щелкните "Принять".</span><span class="sxs-lookup"><span data-stu-id="4994f-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="4994f-112">Отмена сопоставления операций</span><span class="sxs-lookup"><span data-stu-id="4994f-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="4994f-113">Перейдите в раздел "Главная книга" > "Запросы и отчеты" > "Пробный баланс".</span><span class="sxs-lookup"><span data-stu-id="4994f-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="4994f-114">Щелкните "Параметры", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="4994f-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="4994f-115">Щелкните Обновить.</span><span class="sxs-lookup"><span data-stu-id="4994f-115">Click Update.</span></span>
4. <span data-ttu-id="4994f-116">В списке найдите счет, в котором есть сопоставленные проводки.</span><span class="sxs-lookup"><span data-stu-id="4994f-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="4994f-117">Щелкните "Все проводки".</span><span class="sxs-lookup"><span data-stu-id="4994f-117">Click All transactions.</span></span>
6. <span data-ttu-id="4994f-118">Используйте фильтр для упрощения поиска проводки в списке.</span><span class="sxs-lookup"><span data-stu-id="4994f-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="4994f-119">Щелкните "Сопоставления ГК".</span><span class="sxs-lookup"><span data-stu-id="4994f-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="4994f-120">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="4994f-120">In the list, mark the selected row.</span></span>

