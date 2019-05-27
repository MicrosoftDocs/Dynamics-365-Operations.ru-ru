---
title: Выверка фрахта вручную
description: Эта процедура показывает, как выверять фрахт вручную.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee2d114b0a725b947add3e155cc6445021fee998
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556742"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="bdff7-103">Выверка фрахта вручную</span><span class="sxs-lookup"><span data-stu-id="bdff7-103">Reconcile freight manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bdff7-104">Эта процедура показывает, как выверять фрахт вручную.</span><span class="sxs-lookup"><span data-stu-id="bdff7-104">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="bdff7-105">Обычно это делает координатор транспортировки.</span><span class="sxs-lookup"><span data-stu-id="bdff7-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="bdff7-106">Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="bdff7-106">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="bdff7-107">Выберите груз для выверки</span><span class="sxs-lookup"><span data-stu-id="bdff7-107">Select a load to reconcile</span></span>
1. <span data-ttu-id="bdff7-108">Перейдите в раздел "Управление транспортировкой" > "Планирование" > "Рабочее место планирования загрузки".</span><span class="sxs-lookup"><span data-stu-id="bdff7-108">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="bdff7-109">Снимите флажок "Скрыть отгруженные и полученные".</span><span class="sxs-lookup"><span data-stu-id="bdff7-109">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="bdff7-110">В списке выберите груз с кодом груза 00006.</span><span class="sxs-lookup"><span data-stu-id="bdff7-110">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="bdff7-111">Создайте накладную перевозчика</span><span class="sxs-lookup"><span data-stu-id="bdff7-111">Create a carrier invoice</span></span>
    * <span data-ttu-id="bdff7-112">Если выполняется сверка фрахт вручную, и вы не получаете накладные перевозчика автоматически, можно создать накладную на основе счета за фрахт.</span><span class="sxs-lookup"><span data-stu-id="bdff7-112">If you reconcile freight manually and don’t receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="bdff7-113">Щелкните "Связанные сведения".</span><span class="sxs-lookup"><span data-stu-id="bdff7-113">Click Related information.</span></span>
2. <span data-ttu-id="bdff7-114">Щелкните "Сведения векселя фрахта".</span><span class="sxs-lookup"><span data-stu-id="bdff7-114">Click Freight bill details.</span></span>
3. <span data-ttu-id="bdff7-115">Щелкните "Создать накладную по векселю фрахта".</span><span class="sxs-lookup"><span data-stu-id="bdff7-115">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="bdff7-116">В поле "Накладная" введите значение.</span><span class="sxs-lookup"><span data-stu-id="bdff7-116">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="bdff7-117">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="bdff7-117">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="bdff7-118">Выверка накладной</span><span class="sxs-lookup"><span data-stu-id="bdff7-118">Reconcile the invoice</span></span>
    * <span data-ttu-id="bdff7-119">Сверка накладной перевозчика и счета за фрахт выполняется построчно.</span><span class="sxs-lookup"><span data-stu-id="bdff7-119">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="bdff7-120">Щелкните "Сопоставить вексели фрахта с накладными".</span><span class="sxs-lookup"><span data-stu-id="bdff7-120">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="bdff7-121">Разверните раздел "Сведения о накладной".</span><span class="sxs-lookup"><span data-stu-id="bdff7-121">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="bdff7-122">Разверните раздел "Несовпадающие сведения векселя фрахта".</span><span class="sxs-lookup"><span data-stu-id="bdff7-122">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="bdff7-123">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="bdff7-123">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="bdff7-124">Щелкните "Сопоставить".</span><span class="sxs-lookup"><span data-stu-id="bdff7-124">Click Match.</span></span>
6. <span data-ttu-id="bdff7-125">Разверните раздел "Совпадающие сведения векселя фрахта".</span><span class="sxs-lookup"><span data-stu-id="bdff7-125">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="bdff7-126">Отправить накладную на утверждение</span><span class="sxs-lookup"><span data-stu-id="bdff7-126">Submit the invoice for approval</span></span>
1. <span data-ttu-id="bdff7-127">Щелкните "Отправить для утверждения".</span><span class="sxs-lookup"><span data-stu-id="bdff7-127">Click Submit for approval.</span></span>
2. <span data-ttu-id="bdff7-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bdff7-128">Close the page.</span></span>
3. <span data-ttu-id="bdff7-129">Снимите флажок "Скрыть утвержденные".</span><span class="sxs-lookup"><span data-stu-id="bdff7-129">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="bdff7-130">Щелкните "Журналы накладных поставщиков".</span><span class="sxs-lookup"><span data-stu-id="bdff7-130">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="bdff7-131">Щелкните для перехода по ссылке в поле "Номер ссылочного журнала".</span><span class="sxs-lookup"><span data-stu-id="bdff7-131">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="bdff7-132">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="bdff7-132">Click Lines.</span></span>

