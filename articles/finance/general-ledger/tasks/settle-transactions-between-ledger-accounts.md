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
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8220bacc8d683163e97956ec59a5af929b04319c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994423"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="bcf68-103">Сопоставление проводок между счетами ГК</span><span class="sxs-lookup"><span data-stu-id="bcf68-103">Settle transactions between ledger accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bcf68-104">Ниже описан порядок сопоставления проводок между счетами ГК и отмена сопоставления ГК.</span><span class="sxs-lookup"><span data-stu-id="bcf68-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="bcf68-105">В этой процедуре используется компания с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="bcf68-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="bcf68-106">Сопоставление проводки между счетами ГК</span><span class="sxs-lookup"><span data-stu-id="bcf68-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="bcf68-107">Перейдите в раздел "Главная книга" > "Периодические задачи" > "Сопоставления ГК".</span><span class="sxs-lookup"><span data-stu-id="bcf68-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="bcf68-108">В списке найдите проводку, которую требуется сопоставить.</span><span class="sxs-lookup"><span data-stu-id="bcf68-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="bcf68-109">Сальдо должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="bcf68-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="bcf68-110">Щелкните "Включить".</span><span class="sxs-lookup"><span data-stu-id="bcf68-110">Click Include.</span></span>
4. <span data-ttu-id="bcf68-111">Щелкните "Принять".</span><span class="sxs-lookup"><span data-stu-id="bcf68-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="bcf68-112">Отмена сопоставления операций</span><span class="sxs-lookup"><span data-stu-id="bcf68-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="bcf68-113">Перейдите в раздел "Главная книга" > "Запросы и отчеты" > "Пробный баланс".</span><span class="sxs-lookup"><span data-stu-id="bcf68-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="bcf68-114">Щелкните "Параметры", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="bcf68-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="bcf68-115">Щелкните Обновить.</span><span class="sxs-lookup"><span data-stu-id="bcf68-115">Click Update.</span></span>
4. <span data-ttu-id="bcf68-116">В списке найдите счет, в котором есть сопоставленные проводки.</span><span class="sxs-lookup"><span data-stu-id="bcf68-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="bcf68-117">Щелкните "Все проводки".</span><span class="sxs-lookup"><span data-stu-id="bcf68-117">Click All transactions.</span></span>
6. <span data-ttu-id="bcf68-118">Используйте фильтр для упрощения поиска проводки в списке.</span><span class="sxs-lookup"><span data-stu-id="bcf68-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="bcf68-119">Щелкните "Сопоставления ГК".</span><span class="sxs-lookup"><span data-stu-id="bcf68-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="bcf68-120">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="bcf68-120">In the list, mark the selected row.</span></span>

