--- 
title: "Выверка фрахта вручную"
description: "Эта процедура показывает, как выверять фрахт вручную."
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 48623e53633d00e4c3871d3a0266981b78a2f380
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---
# <a name="reconcile-freight-manually"></a><span data-ttu-id="d4ff5-103">Выверка фрахта вручную</span><span class="sxs-lookup"><span data-stu-id="d4ff5-103">Reconcile freight manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d4ff5-104">Эта процедура показывает, как выверять фрахт вручную.</span><span class="sxs-lookup"><span data-stu-id="d4ff5-104">This procedure shows how to reconcile freight manually.</span></span> <span data-ttu-id="d4ff5-105">Обычно это делает координатор транспортировки.</span><span class="sxs-lookup"><span data-stu-id="d4ff5-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="d4ff5-106">Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="d4ff5-106">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-load-to-reconcile"></a><span data-ttu-id="d4ff5-107">Выберите груз для выверки</span><span class="sxs-lookup"><span data-stu-id="d4ff5-107">Select a load to reconcile</span></span>
1. <span data-ttu-id="d4ff5-108">Перейдите в раздел "Управление транспортировкой" > "Планирование" > "Рабочее место планирования загрузки".</span><span class="sxs-lookup"><span data-stu-id="d4ff5-108">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="d4ff5-109">Снимите флажок "Скрыть отгруженные и полученные".</span><span class="sxs-lookup"><span data-stu-id="d4ff5-109">Clear the Hide shipped and received check box.</span></span> 
3. <span data-ttu-id="d4ff5-110">В списке выберите груз с кодом груза 00006.</span><span class="sxs-lookup"><span data-stu-id="d4ff5-110">In the list, select the load that has load ID 00006.</span></span>

## <a name="create-a-carrier-invoice"></a><span data-ttu-id="d4ff5-111">Создайте накладную перевозчика</span><span class="sxs-lookup"><span data-stu-id="d4ff5-111">Create a carrier invoice</span></span>
    * <span data-ttu-id="d4ff5-112">Если выполняется сверка фрахт вручную, и вы не получаете накладные перевозчика автоматически, можно создать накладную на основе счета за фрахт.</span><span class="sxs-lookup"><span data-stu-id="d4ff5-112">If you reconcile freight manually and don’t receive carrier invoices automatically, you can create an invoice based on the freight bill.</span></span>  
1. <span data-ttu-id="d4ff5-113">Щелкните "Связанные сведения".</span><span class="sxs-lookup"><span data-stu-id="d4ff5-113">Click Related information.</span></span>
2. <span data-ttu-id="d4ff5-114">Щелкните "Сведения векселя фрахта".</span><span class="sxs-lookup"><span data-stu-id="d4ff5-114">Click Freight bill details.</span></span>
3. <span data-ttu-id="d4ff5-115">Щелкните "Создать накладную по векселю фрахта".</span><span class="sxs-lookup"><span data-stu-id="d4ff5-115">Click Generate freight bill invoice.</span></span>
4. <span data-ttu-id="d4ff5-116">В поле "Накладная" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d4ff5-116">In the Invoice field, type a value.</span></span>
5. <span data-ttu-id="d4ff5-117">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="d4ff5-117">Click OK.</span></span>

## <a name="reconcile-the-invoice"></a><span data-ttu-id="d4ff5-118">Выверка накладной</span><span class="sxs-lookup"><span data-stu-id="d4ff5-118">Reconcile the invoice</span></span>
    * <span data-ttu-id="d4ff5-119">Сверка накладной перевозчика и счета за фрахт выполняется построчно.</span><span class="sxs-lookup"><span data-stu-id="d4ff5-119">When you reconcile a carrier invoice and a freight bill, this is done line by line.</span></span>  
1. <span data-ttu-id="d4ff5-120">Щелкните "Сопоставить вексели фрахта с накладными".</span><span class="sxs-lookup"><span data-stu-id="d4ff5-120">Click Match freight bills and invoices.</span></span>
2. <span data-ttu-id="d4ff5-121">Разверните раздел "Сведения о накладной".</span><span class="sxs-lookup"><span data-stu-id="d4ff5-121">Expand the Invoice details section.</span></span>
3. <span data-ttu-id="d4ff5-122">Разверните раздел "Несовпадающие сведения векселя фрахта".</span><span class="sxs-lookup"><span data-stu-id="d4ff5-122">Expand the Unmatched freight bill details section.</span></span>
4. <span data-ttu-id="d4ff5-123">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="d4ff5-123">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="d4ff5-124">Щелкните "Сопоставить".</span><span class="sxs-lookup"><span data-stu-id="d4ff5-124">Click Match.</span></span>
6. <span data-ttu-id="d4ff5-125">Разверните раздел "Совпадающие сведения векселя фрахта".</span><span class="sxs-lookup"><span data-stu-id="d4ff5-125">Expand the Matched freight bill details section.</span></span>

## <a name="submit-the-invoice-for-approval"></a><span data-ttu-id="d4ff5-126">Отправить накладную на утверждение</span><span class="sxs-lookup"><span data-stu-id="d4ff5-126">Submit the invoice for approval</span></span>
1. <span data-ttu-id="d4ff5-127">Щелкните "Отправить для утверждения".</span><span class="sxs-lookup"><span data-stu-id="d4ff5-127">Click Submit for approval.</span></span>
2. <span data-ttu-id="d4ff5-128">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d4ff5-128">Close the page.</span></span>
3. <span data-ttu-id="d4ff5-129">Снимите флажок "Скрыть утвержденные".</span><span class="sxs-lookup"><span data-stu-id="d4ff5-129">Clear the Hide approved check box.</span></span> 
4. <span data-ttu-id="d4ff5-130">Щелкните "Журналы накладных поставщиков".</span><span class="sxs-lookup"><span data-stu-id="d4ff5-130">Click Vendor invoice journals.</span></span>
5. <span data-ttu-id="d4ff5-131">Щелкните для перехода по ссылке в поле "Номер ссылочного журнала".</span><span class="sxs-lookup"><span data-stu-id="d4ff5-131">Click to follow the link in the Reference journal number field.</span></span>
6. <span data-ttu-id="d4ff5-132">Щелкните "Строки".</span><span class="sxs-lookup"><span data-stu-id="d4ff5-132">Click Lines.</span></span>


