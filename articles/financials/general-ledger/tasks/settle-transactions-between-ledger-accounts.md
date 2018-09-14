--- 
title: "Сопоставление проводок между счетами ГК"
description: "Ниже описан порядок сопоставления проводок между счетами ГК и отмена сопоставления ГК."
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
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
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 27064331191f3de35bd3c77dc0c8aeca6d4b9edb
ms.contentlocale: ru-ru
ms.lasthandoff: 09/14/2018

---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="1d74f-103">Сопоставление проводок между счетами ГК</span><span class="sxs-lookup"><span data-stu-id="1d74f-103">Settle transactions between ledger accounts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1d74f-104">Ниже описан порядок сопоставления проводок между счетами ГК и отмена сопоставления ГК.</span><span class="sxs-lookup"><span data-stu-id="1d74f-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="1d74f-105">В этой процедуре используется компания с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="1d74f-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="1d74f-106">Сопоставление проводки между счетами ГК</span><span class="sxs-lookup"><span data-stu-id="1d74f-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="1d74f-107">Перейдите в раздел "Главная книга" > "Периодические задачи" > "Сопоставления ГК".</span><span class="sxs-lookup"><span data-stu-id="1d74f-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="1d74f-108">В списке найдите проводку, которую требуется сопоставить.</span><span class="sxs-lookup"><span data-stu-id="1d74f-108">In the list, find the transaction that you want to settle.</span></span>
    * <span data-ttu-id="1d74f-109">Сальдо должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="1d74f-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="1d74f-110">Щелкните "Включить".</span><span class="sxs-lookup"><span data-stu-id="1d74f-110">Click Include.</span></span>
4. <span data-ttu-id="1d74f-111">Щелкните "Принять".</span><span class="sxs-lookup"><span data-stu-id="1d74f-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="1d74f-112">Отмена сопоставления операций</span><span class="sxs-lookup"><span data-stu-id="1d74f-112">Cancel a ledger settlement</span></span>
1. <span data-ttu-id="1d74f-113">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1d74f-113">Close the page.</span></span>
2. <span data-ttu-id="1d74f-114">Перейдите в раздел "Главная книга" > "Запросы и отчеты" > "Пробный баланс".</span><span class="sxs-lookup"><span data-stu-id="1d74f-114">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
3. <span data-ttu-id="1d74f-115">Щелкните "Параметры", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="1d74f-115">Click Parameters to open the drop dialog.</span></span>
4. <span data-ttu-id="1d74f-116">Щелкните Обновить.</span><span class="sxs-lookup"><span data-stu-id="1d74f-116">Click Update.</span></span>
5. <span data-ttu-id="1d74f-117">В списке найдите счет, в котором есть сопоставленные проводки.</span><span class="sxs-lookup"><span data-stu-id="1d74f-117">In the list, find the account that has the settled transaction.</span></span>
6. <span data-ttu-id="1d74f-118">Щелкните "Все проводки".</span><span class="sxs-lookup"><span data-stu-id="1d74f-118">Click All transactions.</span></span>
7. <span data-ttu-id="1d74f-119">Используйте фильтр для упрощения поиска проводки в списке.</span><span class="sxs-lookup"><span data-stu-id="1d74f-119">Use a filter to easily find the transaction in the list.</span></span>
8. <span data-ttu-id="1d74f-120">Щелкните "Сопоставления ГК".</span><span class="sxs-lookup"><span data-stu-id="1d74f-120">Click Ledger settlements.</span></span>
9. <span data-ttu-id="1d74f-121">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="1d74f-121">In the list, mark the selected row.</span></span>


