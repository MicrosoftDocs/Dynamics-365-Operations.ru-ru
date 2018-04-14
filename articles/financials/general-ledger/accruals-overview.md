---
title: "Обзор начислений"
description: "Эта статья описывает начисления и представляет информация о том, как настроить их и создать проводки."
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 0b4d8e7eb268857ce753415a24e600b8006eb5e3
ms.contentlocale: ru-ru
ms.lasthandoff: 04/13/2018

---

# <a name="accruals-overview"></a><span data-ttu-id="de7e2-103">Обзор начислений</span><span class="sxs-lookup"><span data-stu-id="de7e2-103">Accruals overview</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="de7e2-104">Эта статья описывает начисления и представляет информация о том, как настроить их и создать проводки.</span><span class="sxs-lookup"><span data-stu-id="de7e2-104">This article describes accruals, and provides information about how to set them up and create transactions.</span></span>

<span data-ttu-id="de7e2-105">Начисления используются в учете методом начисления для отслеживания выручки, утвержденной за период, в котором она была получена, а не в момент получения платежа, и для отслеживания расходов (затрат), которые были утверждены в момент возникновения, а не в момент осуществления платежа.</span><span class="sxs-lookup"><span data-stu-id="de7e2-105">Accruals are used in accrual accounting to track revenue that is recognized in the period that it's earned in, not when payment is received, and to track expenses (costs) that are recognized when they occur, not when payment is made.</span></span>

## <a name="accrual-schemes"></a><span data-ttu-id="de7e2-106">Схемы начисления</span><span class="sxs-lookup"><span data-stu-id="de7e2-106">Accrual schemes</span></span>
<span data-ttu-id="de7e2-107">Схемы начисления используются для настройки отложенной выручки и затрат. Одну и ту же схему начисления можно использовать как для выручки, так и для затрат.</span><span class="sxs-lookup"><span data-stu-id="de7e2-107">Accrual schemes are used to set up the deferred revenue and costs, and the same accrual scheme can be used for both revenue and costs.</span></span> <span data-ttu-id="de7e2-108">Начисления ГК позволяют перераспределять затраты или выручку из строки журнала, чтобы затраты и выручки распознавались в соответствующих периодах.</span><span class="sxs-lookup"><span data-stu-id="de7e2-108">Ledger accruals redistribute the costs or revenue of a journal line so that the costs and revenues are recognized in the appropriate periods.</span></span> <span data-ttu-id="de7e2-109">На странице **Схема начисления** укажите дебетовый и кредитный счета, которые будут использоваться при применении схемы начисления.</span><span class="sxs-lookup"><span data-stu-id="de7e2-109">On the **Accrual scheme** page, you specify the debit and the credit accounts that will be used when the accrual scheme is applied.</span></span>

-   <span data-ttu-id="de7e2-110">**Дебет** — определяемый счет ГК, который заменит дебетовый счет ГК в строке ваучера журнала.</span><span class="sxs-lookup"><span data-stu-id="de7e2-110">**Debit** – The main account that you define will replace the debit main account on the journal voucher line.</span></span> <span data-ttu-id="de7e2-111">Этот счет также будет использоваться для реверсирования расхода будущего периода на основании проводок начисления ГК.</span><span class="sxs-lookup"><span data-stu-id="de7e2-111">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>
-   <span data-ttu-id="de7e2-112">**Кредит** — определяемый счет ГК, который заменит кредитный счет ГК в строке ваучера журнала.</span><span class="sxs-lookup"><span data-stu-id="de7e2-112">**Credit** – the main account that you define will replace the credit main account on the journal voucher line.</span></span> <span data-ttu-id="de7e2-113">Этот счет также будет использоваться для реверсирования расхода будущего периода на основании проводок начисления ГК.</span><span class="sxs-lookup"><span data-stu-id="de7e2-113">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>

<span data-ttu-id="de7e2-114">После определения счета для использования можно указать способ создания кода ваучера при создании проводок по начислениям.</span><span class="sxs-lookup"><span data-stu-id="de7e2-114">After you determine which accounts to use, you can specify how the voucher number is created when accrual transactions are created.</span></span> <span data-ttu-id="de7e2-115">Также можно указать, как часто должны выполняться проводки, число раз, которое должны создаваться проводки, и время разноски проводок.</span><span class="sxs-lookup"><span data-stu-id="de7e2-115">You can also specify how often the transactions occur, the number of times that the transactions are created, and when the transactions are posted.</span></span> <span data-ttu-id="de7e2-116">После создания схемы начисления ее можно использовать в некоторых журналах с помощью функции "Начисления ГК".</span><span class="sxs-lookup"><span data-stu-id="de7e2-116">After the accrual scheme has been created, you can use it in some of the journals by using the Ledger accruals function.</span></span>

## <a name="ledger-accruals"></a><span data-ttu-id="de7e2-117">Начисления ГК</span><span class="sxs-lookup"><span data-stu-id="de7e2-117">Ledger accruals</span></span>
<span data-ttu-id="de7e2-118">При создании журнала можно щелкнуть **Начисления ГК** в меню **Функции**.</span><span class="sxs-lookup"><span data-stu-id="de7e2-118">When you enter a journal, you can click **Ledger accruals** on the **Functions** menu.</span></span> <span data-ttu-id="de7e2-119">Затем при выборе схемы начисления будет отображаться базовая сумма из журнала, которая будет распределена по периоду, как определено схемой начисления.</span><span class="sxs-lookup"><span data-stu-id="de7e2-119">Then, when you select the accrual scheme, you will see the base amount from the journal that will be spread over the period, as determined by the accrual scheme.</span></span> <span data-ttu-id="de7e2-120">Например, если вы оплачиваете страховку сотрудника за весь год в январе и сумма равна 12 000, вы должны утверждать этот расход каждый месяц.</span><span class="sxs-lookup"><span data-stu-id="de7e2-120">For example, if you pay an employee's insurance for the whole year in January, and the amount is 12,000, you must recognize that expense each month.</span></span> <span data-ttu-id="de7e2-121">Вы можете выбрать дату начала.</span><span class="sxs-lookup"><span data-stu-id="de7e2-121">You can select the start date.</span></span> <span data-ttu-id="de7e2-122">Вы также можете указать, будет ли начисляемая сумма основываться на счете или корр. счете.</span><span class="sxs-lookup"><span data-stu-id="de7e2-122">You can also specify whether the amount that is accrued is based on the account or the offset account.</span></span> <span data-ttu-id="de7e2-123">После выбора значений щелкните **Проводки**, чтобы просмотреть все проводки, которые были созданы на основании схемы начисления.</span><span class="sxs-lookup"><span data-stu-id="de7e2-123">After you make your selections, click **Transactions** to view all the transactions that have been created based on the accrual scheme.</span></span> <span data-ttu-id="de7e2-124">Например, если распределить 12 000 расходов на страхование за год, отобразится 1000 в каждом месяце.</span><span class="sxs-lookup"><span data-stu-id="de7e2-124">For example, if you spread the 12,000 in insurance expenses over the year, you will see 1,000 for each month.</span></span> <span data-ttu-id="de7e2-125">После разноски журнала можно просмотреть проводки с помощью страницы запроса **Проводки по ваучеру**.</span><span class="sxs-lookup"><span data-stu-id="de7e2-125">After you post the journal, you can view the transactions by using the **Voucher transactions** inquiry page.</span></span> <span data-ttu-id="de7e2-126">Если схему начисления невозможно применить (например, если используется накладная по заказу на продажу или накладная по заказу на покупку), то можно кредитовать предоплаченную сумму и дебетовать сумму расходов.</span><span class="sxs-lookup"><span data-stu-id="de7e2-126">If an accrual scheme can't be applied (for example, when a sales order invoice or purchase order invoice is involved), you can credit the prepaid amount and debit the expense amount.</span></span> <span data-ttu-id="de7e2-127">Затем можно выбрать **Корр. счет** при применении схемы начисления.</span><span class="sxs-lookup"><span data-stu-id="de7e2-127">You can then select **Offset** when you apply the accrual scheme.</span></span>


<span data-ttu-id="de7e2-128">Дополнительные сведения см. в разделах [Создание схем начисления](tasks/create-accrual-schemes.md) и [Создание проводок начисления ГК](tasks/create-ledger-accrual-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="de7e2-128">For more information, see [Create accrual schemes](tasks/create-accrual-schemes.md) and [Create ledger accrual transactions](tasks/create-ledger-accrual-transactions.md).</span></span>

