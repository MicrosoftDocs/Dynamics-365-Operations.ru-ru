---
title: "Выверка фрахта в модуле \"Управление транспортировкой\""
description: "В этой статье описывается процесс выверки фрахта."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 0e9dd669ff08c02a8bbb1f83e19dfa62298f317b
ms.contentlocale: ru-ru
ms.lasthandoff: 07/18/2017

---

# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="c21e3-103">Выверка фрахта в модуле "Управление транспортировкой"</span><span class="sxs-lookup"><span data-stu-id="c21e3-103">Reconcile freight in transportation management</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c21e3-104">В этой статье описывается процесс выверки фрахта.</span><span class="sxs-lookup"><span data-stu-id="c21e3-104">This article describes the freight reconciliation process.</span></span>

<span data-ttu-id="c21e3-105">Выверку фрахта можно выполнить вручную или настроить для автоматического выполнения.</span><span class="sxs-lookup"><span data-stu-id="c21e3-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="c21e3-106">Чтобы использовать автоматическую выверку фрахта, необходимо настроить шаблон аудита, в котором можно определить критерии, определяющие, какие векселя фрахта будут сопоставляться автоматически.</span><span class="sxs-lookup"><span data-stu-id="c21e3-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="c21e3-107">Процесс выверки фрахта</span><span class="sxs-lookup"><span data-stu-id="c21e3-107">The freight reconciliation process</span></span>
<span data-ttu-id="c21e3-108">Фрахтовые ставки рассчитываются механизмом ставок, связанным с соответствующим перевозчиком.</span><span class="sxs-lookup"><span data-stu-id="c21e3-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="c21e3-109">При подтверждении загрузки создается вексель фрахта и в него передаются фрахтовые ставки.</span><span class="sxs-lookup"><span data-stu-id="c21e3-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="c21e3-110">Фрахтовые ставки распределяются как накладные расходы для соответствующего документа-источника (заказ на покупку, заказ на продажу или заказ на перемещение) в зависимости от настройки, используемой для стандартного процесса выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="c21e3-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="c21e3-111">Процесс выверки фрахта (который также называется процессом сопоставления) можно запустить сразу после поступления накладной фрахта от перевозчика.</span><span class="sxs-lookup"><span data-stu-id="c21e3-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="c21e3-112">Накладную можно получить в электронном или бумажном формате.</span><span class="sxs-lookup"><span data-stu-id="c21e3-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="c21e3-113">Если накладная поступает в бумажном формате, можно создать электронную накладную с помощью векселя фрахта в качестве шаблона.</span><span class="sxs-lookup"><span data-stu-id="c21e3-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span> 

<span data-ttu-id="c21e3-114">[![Процесс выверки фрахта](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="c21e3-114">[![Freight reconcilation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="c21e3-115">Выверка вручную</span><span class="sxs-lookup"><span data-stu-id="c21e3-115">Manual reconciliation</span></span>
<span data-ttu-id="c21e3-116">Если фрахт выверяется вручную, необходимо сопоставить каждую строку накладной со строкой или строками векселя фрахта для загрузки, по которой выставляется накладная.</span><span class="sxs-lookup"><span data-stu-id="c21e3-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="c21e3-117">Это сопоставление выполняется на странице **Сопоставление векселя фрахта с накладной**.</span><span class="sxs-lookup"><span data-stu-id="c21e3-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="c21e3-118">Если сумма в строке накладной не соответствует сумме векселя фрахта, необходимо выбрать причину для разницы выверки.</span><span class="sxs-lookup"><span data-stu-id="c21e3-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="c21e3-119">Если существует несколько причин для выверки, можно разделить несоответствующую сумму между ними.</span><span class="sxs-lookup"><span data-stu-id="c21e3-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="c21e3-120">Причина выверки определяет способ разноски сумм разницы в главной книге.</span><span class="sxs-lookup"><span data-stu-id="c21e3-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="c21e3-121">При учитывается выверка всей суммы накладной, она направляется на утверждение, после чего выполняется разноска журнала.</span><span class="sxs-lookup"><span data-stu-id="c21e3-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="c21e3-122">На следующем рисунке показано, как создать накладную фрахта и выполнить выверку фрахта в Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c21e3-122">The following illustration shows how to generate a freight invoice and do freight reconciliation in Microsoft Dynamics 365 for Finance and Operations.</span></span> 
<span data-ttu-id="c21e3-123">[![Задачи выверки фрахта в Dynamics AX](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="c21e3-123">[![Freight reconcilation tasks in Dynamics AX](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>
## <a name="automatic-reconciliation"></a><span data-ttu-id="c21e3-124">Автоматическая выверка</span><span class="sxs-lookup"><span data-stu-id="c21e3-124">Automatic reconciliation</span></span>
<span data-ttu-id="c21e3-125">Чтобы использовать автоматическую выверку, необходимо указать расписание для выверки, а также накладные и перевозчиков для использования.</span><span class="sxs-lookup"><span data-stu-id="c21e3-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="c21e3-126">Сопоставление строк накладной и векселей фрахта осуществляется в соответствии с настройкой шаблона аудита и типом векселя фрахта.</span><span class="sxs-lookup"><span data-stu-id="c21e3-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="c21e3-127">После выполнения автоматической выверки необходимо обработать все накладные, которые система не может сопоставить.</span><span class="sxs-lookup"><span data-stu-id="c21e3-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="c21e3-128">Затем необходимо обработать эти накладные вручную, перед разноской всех накладных для платежа.</span><span class="sxs-lookup"><span data-stu-id="c21e3-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>




