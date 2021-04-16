---
title: Выверка фрахта вручную
description: Эта процедура показывает, как выверять фрахт вручную.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily, TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a0a5450697a09e5e54e74b35b2576eb6bbd4cdf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838522"
---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="349d2-103">Выверка фрахта вручную</span><span class="sxs-lookup"><span data-stu-id="349d2-103">Reconcile freight manually</span></span>

<span data-ttu-id="349d2-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="349d2-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="349d2-105">Эта процедура показывает, как выверять фрахт вручную.</span><span class="sxs-lookup"><span data-stu-id="349d2-105">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="349d2-106">Обычно это делает координатор транспортировки.</span><span class="sxs-lookup"><span data-stu-id="349d2-106">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="349d2-107">Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="349d2-107">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="349d2-108">Выберите груз для выверки</span><span class="sxs-lookup"><span data-stu-id="349d2-108">Select a load to reconcile</span></span>
1. <span data-ttu-id="349d2-109">Перейдите в раздел "Управление транспортировкой" > "Планирование" > "Рабочее место планирования загрузки".</span><span class="sxs-lookup"><span data-stu-id="349d2-109">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="349d2-110">Снимите флажок "Скрыть отгруженные и полученные".</span><span class="sxs-lookup"><span data-stu-id="349d2-110">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="349d2-111">В списке выберите груз с кодом груза 00006.</span><span class="sxs-lookup"><span data-stu-id="349d2-111">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="349d2-112">Создайте накладную перевозчика</span><span class="sxs-lookup"><span data-stu-id="349d2-112">Create a carrier invoice</span></span>
<span data-ttu-id="349d2-113">Если выполняется сверка фрахт вручную, и вы не получаете накладные перевозчика автоматически, можно создать накладную на основе счета за фрахт.</span><span class="sxs-lookup"><span data-stu-id="349d2-113">If you reconcile freight manually and don't receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="349d2-114">Щелкните "Связанные сведения".</span><span class="sxs-lookup"><span data-stu-id="349d2-114">Click Related information.</span></span>
2. <span data-ttu-id="349d2-115">Щелкните "Сведения векселя фрахта".</span><span class="sxs-lookup"><span data-stu-id="349d2-115">Click Freight bill details.</span></span>
3. <span data-ttu-id="349d2-116">Щелкните "Создать накладную по векселю фрахта".</span><span class="sxs-lookup"><span data-stu-id="349d2-116">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="349d2-117">В поле "Накладная" введите значение.</span><span class="sxs-lookup"><span data-stu-id="349d2-117">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="349d2-118">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="349d2-118">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="349d2-119">Выверка накладной</span><span class="sxs-lookup"><span data-stu-id="349d2-119">Reconcile the invoice</span></span>
<span data-ttu-id="349d2-120">Сверка накладной перевозчика и счета за фрахт выполняется построчно.</span><span class="sxs-lookup"><span data-stu-id="349d2-120">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="349d2-121">Щелкните "Сопоставить вексели фрахта с накладными".</span><span class="sxs-lookup"><span data-stu-id="349d2-121">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="349d2-122">Разверните раздел "Сведения о накладной".</span><span class="sxs-lookup"><span data-stu-id="349d2-122">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="349d2-123">Разверните раздел "Несовпадающие сведения векселя фрахта".</span><span class="sxs-lookup"><span data-stu-id="349d2-123">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="349d2-124">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="349d2-124">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="349d2-125">Щелкните "Сопоставить".</span><span class="sxs-lookup"><span data-stu-id="349d2-125">Click Match.</span></span>
6. <span data-ttu-id="349d2-126">Разверните раздел "Совпадающие сведения векселя фрахта".</span><span class="sxs-lookup"><span data-stu-id="349d2-126">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="349d2-127">Отправить накладную на утверждение</span><span class="sxs-lookup"><span data-stu-id="349d2-127">Submit the invoice for approval</span></span>
1. <span data-ttu-id="349d2-128">Щелкните "Отправить для утверждения".</span><span class="sxs-lookup"><span data-stu-id="349d2-128">Click Submit for approval.</span></span>
2. <span data-ttu-id="349d2-129">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="349d2-129">Close the page.</span></span>
3. <span data-ttu-id="349d2-130">Снимите флажок "Скрыть утвержденные".</span><span class="sxs-lookup"><span data-stu-id="349d2-130">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="349d2-131">Щелкните "Журналы накладных поставщиков".</span><span class="sxs-lookup"><span data-stu-id="349d2-131">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="349d2-132">Щелкните для перехода по ссылке в поле "Номер ссылочного журнала".</span><span class="sxs-lookup"><span data-stu-id="349d2-132">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="349d2-133">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="349d2-133">Click Lines.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]