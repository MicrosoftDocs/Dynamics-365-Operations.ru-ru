---
title: Выверка фрахта в модуле "Управление транспортировкой"
description: В этой теме описывается процесс выверки фрахта.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e1680572f1ba9816c9ec45ef52498cab1f45247
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206227"
---
# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="95b9c-103">Выверка фрахта в модуле "Управление транспортировкой"</span><span class="sxs-lookup"><span data-stu-id="95b9c-103">Reconcile freight in transportation management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95b9c-104">В этой теме описывается процесс выверки фрахта.</span><span class="sxs-lookup"><span data-stu-id="95b9c-104">This topic describes the freight reconciliation process.</span></span>

<span data-ttu-id="95b9c-105">Выверку фрахта можно выполнить вручную или настроить для автоматического выполнения.</span><span class="sxs-lookup"><span data-stu-id="95b9c-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="95b9c-106">Чтобы использовать автоматическую выверку фрахта, необходимо настроить шаблон аудита, в котором можно определить критерии, определяющие, какие векселя фрахта будут сопоставляться автоматически.</span><span class="sxs-lookup"><span data-stu-id="95b9c-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="95b9c-107">Процесс выверки фрахта</span><span class="sxs-lookup"><span data-stu-id="95b9c-107">The freight reconciliation process</span></span>
<span data-ttu-id="95b9c-108">Фрахтовые ставки рассчитываются механизмом ставок, связанным с соответствующим перевозчиком.</span><span class="sxs-lookup"><span data-stu-id="95b9c-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="95b9c-109">При подтверждении загрузки создается вексель фрахта и в него передаются фрахтовые ставки.</span><span class="sxs-lookup"><span data-stu-id="95b9c-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="95b9c-110">Фрахтовые ставки распределяются как накладные расходы для соответствующего документа-источника (заказ на покупку, заказ на продажу или заказ на перемещение) в зависимости от настройки, используемой для стандартного процесса выставления накладных.</span><span class="sxs-lookup"><span data-stu-id="95b9c-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="95b9c-111">Процесс выверки фрахта (который также называется процессом сопоставления) можно запустить сразу после поступления накладной фрахта от перевозчика.</span><span class="sxs-lookup"><span data-stu-id="95b9c-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="95b9c-112">Накладную можно получить в электронном или бумажном формате.</span><span class="sxs-lookup"><span data-stu-id="95b9c-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="95b9c-113">Если накладная поступает в бумажном формате, можно создать электронную накладную с помощью векселя фрахта в качестве шаблона.</span><span class="sxs-lookup"><span data-stu-id="95b9c-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span> 

<span data-ttu-id="95b9c-114">[![Процесс выверки фрахта](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="95b9c-114">[![Freight reconcilation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="95b9c-115">Выверка вручную</span><span class="sxs-lookup"><span data-stu-id="95b9c-115">Manual reconciliation</span></span>
<span data-ttu-id="95b9c-116">Если фрахт выверяется вручную, необходимо сопоставить каждую строку накладной со строкой или строками векселя фрахта для загрузки, по которой выставляется накладная.</span><span class="sxs-lookup"><span data-stu-id="95b9c-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="95b9c-117">Это сопоставление выполняется на странице **Сопоставление векселя фрахта с накладной**.</span><span class="sxs-lookup"><span data-stu-id="95b9c-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="95b9c-118">Если сумма в строке накладной не соответствует сумме векселя фрахта, необходимо выбрать причину для разницы выверки.</span><span class="sxs-lookup"><span data-stu-id="95b9c-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="95b9c-119">Если существует несколько причин для выверки, можно разделить несоответствующую сумму между ними.</span><span class="sxs-lookup"><span data-stu-id="95b9c-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="95b9c-120">Причина выверки определяет способ разноски сумм разницы в главной книге.</span><span class="sxs-lookup"><span data-stu-id="95b9c-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="95b9c-121">При учитывается выверка всей суммы накладной, она направляется на утверждение, после чего выполняется разноска журнала.</span><span class="sxs-lookup"><span data-stu-id="95b9c-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="95b9c-122">В следующем примере показано, как создать накладную фрахта и выполнить выверку фрахта.</span><span class="sxs-lookup"><span data-stu-id="95b9c-122">The following illustration shows how to generate a freight invoice and do freight reconciliation.</span></span> 
<span data-ttu-id="95b9c-123">[![Задачи выверки фрахта](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="95b9c-123">[![Freight reconcilation tasks](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>
## <a name="automatic-reconciliation"></a><span data-ttu-id="95b9c-124">Автоматическая выверка</span><span class="sxs-lookup"><span data-stu-id="95b9c-124">Automatic reconciliation</span></span>
<span data-ttu-id="95b9c-125">Чтобы использовать автоматическую выверку, необходимо указать расписание для выверки, а также накладные и перевозчиков для использования.</span><span class="sxs-lookup"><span data-stu-id="95b9c-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="95b9c-126">Сопоставление строк накладной и векселей фрахта осуществляется в соответствии с настройкой шаблона аудита и типом векселя фрахта.</span><span class="sxs-lookup"><span data-stu-id="95b9c-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="95b9c-127">После выполнения автоматической выверки необходимо обработать все накладные, которые система не может сопоставить.</span><span class="sxs-lookup"><span data-stu-id="95b9c-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="95b9c-128">Затем необходимо обработать эти накладные вручную, перед разноской всех накладных для платежа.</span><span class="sxs-lookup"><span data-stu-id="95b9c-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>



