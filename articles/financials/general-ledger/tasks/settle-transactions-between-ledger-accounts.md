--- 
title: "Сопоставление проводок между счетами ГК"
description: "Ниже описан порядок сопоставления проводок между счетами ГК и отмена сопоставления ГК."
author: aprilolson
manager: AnnBe
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 74522c97716238b62af3d65a1c23ba9e5e60a68b
ms.openlocfilehash: 4aff64fa1c017f295752e913de7fb320f0662ef8
ms.contentlocale: ru-ru
ms.lasthandoff: 10/03/2018

---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="7487b-103">Сопоставление проводок между счетами ГК</span><span class="sxs-lookup"><span data-stu-id="7487b-103">Settle transactions between ledger accounts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7487b-104">Ниже описан порядок сопоставления проводок между счетами ГК и отмена сопоставления ГК.</span><span class="sxs-lookup"><span data-stu-id="7487b-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="7487b-105">В этой процедуре используется компания с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="7487b-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="7487b-106">Сопоставление проводки между счетами ГК</span><span class="sxs-lookup"><span data-stu-id="7487b-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="7487b-107">Перейдите в раздел "Главная книга" > "Периодические задачи" > "Сопоставления ГК".</span><span class="sxs-lookup"><span data-stu-id="7487b-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="7487b-108">В списке найдите проводку, которую требуется сопоставить.</span><span class="sxs-lookup"><span data-stu-id="7487b-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="7487b-109">Сальдо должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="7487b-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="7487b-110">Щелкните "Включить".</span><span class="sxs-lookup"><span data-stu-id="7487b-110">Click Include.</span></span>
4. <span data-ttu-id="7487b-111">Щелкните "Принять".</span><span class="sxs-lookup"><span data-stu-id="7487b-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="7487b-112">Отмена сопоставления операций</span><span class="sxs-lookup"><span data-stu-id="7487b-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="7487b-113">Перейдите в раздел "Главная книга" > "Запросы и отчеты" > "Пробный баланс".</span><span class="sxs-lookup"><span data-stu-id="7487b-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="7487b-114">Щелкните "Параметры", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="7487b-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="7487b-115">Щелкните Обновить.</span><span class="sxs-lookup"><span data-stu-id="7487b-115">Click Update.</span></span>
4. <span data-ttu-id="7487b-116">В списке найдите счет, в котором есть сопоставленные проводки.</span><span class="sxs-lookup"><span data-stu-id="7487b-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="7487b-117">Щелкните "Все проводки".</span><span class="sxs-lookup"><span data-stu-id="7487b-117">Click All transactions.</span></span>
6. <span data-ttu-id="7487b-118">Используйте фильтр для упрощения поиска проводки в списке.</span><span class="sxs-lookup"><span data-stu-id="7487b-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="7487b-119">Щелкните "Сопоставления ГК".</span><span class="sxs-lookup"><span data-stu-id="7487b-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="7487b-120">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="7487b-120">In the list, mark the selected row.</span></span>


