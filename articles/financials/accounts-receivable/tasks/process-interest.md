---
title: Обработка процента
description: В этой процедуре показано, как создать, напечатать и разнести процент-ноты.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5652a38684061914f895d7f8b82999c9840fd63
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "359160"
---
# <a name="process-interest"></a><span data-ttu-id="dce10-103">Обработка процента</span><span class="sxs-lookup"><span data-stu-id="dce10-103">Process interest</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dce10-104">В этой процедуре показано, как создать, напечатать и разнести процент-ноты.</span><span class="sxs-lookup"><span data-stu-id="dce10-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="dce10-105">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="dce10-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="dce10-106">Настройка процента в профиле разноски</span><span class="sxs-lookup"><span data-stu-id="dce10-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="dce10-107">Перейдите в раздел "Кредит и сборы" > "Настройка" > "Профили разноски по клиенту".</span><span class="sxs-lookup"><span data-stu-id="dce10-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="dce10-108">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="dce10-108">Click Edit.</span></span>
    * <span data-ttu-id="dce10-109">Выберите код процента из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="dce10-109">Select an interest code from the drop-down list.</span></span> <span data-ttu-id="dce10-110">Если вы не хотите рассчитывать процент для проводок с использованием этого профиля разноски, оставьте поле пустым.</span><span class="sxs-lookup"><span data-stu-id="dce10-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="dce10-111">Вкладка "Табличные ограничения" позволяет изменить способ обработки процента.</span><span class="sxs-lookup"><span data-stu-id="dce10-111">The Table restriction tab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="dce10-112">Если в этом поле установить значение "Да", процент будет рассчитан для данного профиля разноски.</span><span class="sxs-lookup"><span data-stu-id="dce10-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="dce10-113">Рассчитать процент</span><span class="sxs-lookup"><span data-stu-id="dce10-113">Calculate interest</span></span>
1. <span data-ttu-id="dce10-114">Перейдите в раздел "Кредит и сборы" > "Процент" > "Создание процент-нот".</span><span class="sxs-lookup"><span data-stu-id="dce10-114">Go to Credit and collections > Interest > Create interest notes.</span></span>
    * <span data-ttu-id="dce10-115">Необходимо выбрать типы проводки, для которых будет рассчитываться процент.</span><span class="sxs-lookup"><span data-stu-id="dce10-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="dce10-116">Все открытые проводки для этих типов будут включены в расчет.</span><span class="sxs-lookup"><span data-stu-id="dce10-116">All of the open transactions for these types will be included in the calculation.</span></span>  
    * <span data-ttu-id="dce10-117">Если выбран процент, будет рассчитан процент по процентам.</span><span class="sxs-lookup"><span data-stu-id="dce10-117">If you select Interest, you will calculate interest on interest.</span></span> <span data-ttu-id="dce10-118">Возможно, потребуется проверить законодательство по расчету процентов по процентам до их включения в проводку.</span><span class="sxs-lookup"><span data-stu-id="dce10-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
    * <span data-ttu-id="dce10-119">Процент будет рассчитан, начиная с этой даты до даты, указанной в поле "Дата окончания".</span><span class="sxs-lookup"><span data-stu-id="dce10-119">Interest will be calculated from this date to the "To date".</span></span> <span data-ttu-id="dce10-120">Если не указать значение в поле "Дата начала", все неразнесенные процент-ноты будут отменены и процент будет пересчитан от даты проводки.</span><span class="sxs-lookup"><span data-stu-id="dce10-120">If you do not specific a "From date", then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>  
2. <span data-ttu-id="dce10-121">Введите дату процент-ноты.</span><span class="sxs-lookup"><span data-stu-id="dce10-121">Enter the date of the interest note.</span></span>
    * <span data-ttu-id="dce10-122">Существует три параметра профиля разноски:   "Счет" — используется профиль разноски, назначенный счету клиента для каждой процент-ноты.</span><span class="sxs-lookup"><span data-stu-id="dce10-122">There are three posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="dce10-123">"Выбор" — используется профиль разноски, выбранный в поле "Профиль разноски".</span><span class="sxs-lookup"><span data-stu-id="dce10-123">Select – Use the posting profile that you select in the Posting profile field.</span></span>   <span data-ttu-id="dce10-124">"Проводка" — используется отдельный профиль разноски из проводок, по которым рассчитывается процент для каждой процент-ноты.</span><span class="sxs-lookup"><span data-stu-id="dce10-124">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="dce10-125">Проводки без назначенного профиля разноски используют профиль разноски, который указан в области "Главная книга и налог" формы "Параметры расчетов с клиентами".</span><span class="sxs-lookup"><span data-stu-id="dce10-125">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
    * <span data-ttu-id="dce10-126">Выберите профиль разноски здесь, если вы изменили значение "Использовать профиль разноски из" на "Выбор".</span><span class="sxs-lookup"><span data-stu-id="dce10-126">Select a posting profile here if you changed "Use posting profile from" to "Select".</span></span>  
3. <span data-ttu-id="dce10-127">Разверните или сверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="dce10-127">Expand or collapse the Records to include section.</span></span>
4. <span data-ttu-id="dce10-128">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="dce10-128">Click Filter.</span></span>
5. <span data-ttu-id="dce10-129">В поле "Критерии" введите код клиента.</span><span class="sxs-lookup"><span data-stu-id="dce10-129">In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="dce10-130">Например, введите "US-001".</span><span class="sxs-lookup"><span data-stu-id="dce10-130">For example, enter 'US-001'..</span></span>
6. <span data-ttu-id="dce10-131">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="dce10-131">Click OK.</span></span>
7. <span data-ttu-id="dce10-132">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="dce10-132">Click OK.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="dce10-133">Печать процент-нот</span><span class="sxs-lookup"><span data-stu-id="dce10-133">Print interest notes</span></span>
1. <span data-ttu-id="dce10-134">Перейдите в раздел "Кредит и сборы" > "Процент" > "Просмотр и обработка процент-нот".</span><span class="sxs-lookup"><span data-stu-id="dce10-134">Go to Credit and collections > Interest > Review and process interest notes.</span></span>
2. <span data-ttu-id="dce10-135">В поле "Статус" выберите "Создано".</span><span class="sxs-lookup"><span data-stu-id="dce10-135">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="dce10-136">В поле "Напечатано" выберите "Не напечатано".</span><span class="sxs-lookup"><span data-stu-id="dce10-136">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="dce10-137">Нажмите кнопку Печать.</span><span class="sxs-lookup"><span data-stu-id="dce10-137">Click Print.</span></span>
5. <span data-ttu-id="dce10-138">Разверните или сверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="dce10-138">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="dce10-139">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="dce10-139">Click OK.</span></span>
7. <span data-ttu-id="dce10-140">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="dce10-140">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="dce10-141">Разноска процент-ноты</span><span class="sxs-lookup"><span data-stu-id="dce10-141">Post the interest note</span></span>
1. <span data-ttu-id="dce10-142">Выберите процент-ноту, готовую к разноске (статус "Создано").</span><span class="sxs-lookup"><span data-stu-id="dce10-142">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="dce10-143">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="dce10-143">Click Post.</span></span>
3. <span data-ttu-id="dce10-144">Введите дату разноски для процент-ноты.</span><span class="sxs-lookup"><span data-stu-id="dce10-144">Enter the posting date for the interest note.</span></span>
    * <span data-ttu-id="dce10-145">Выберите значение "Да", чтобы создать проводку главной книги для каждой процент-ноты.</span><span class="sxs-lookup"><span data-stu-id="dce10-145">Select Yes to create a general ledger transaction for each interest note.</span></span>     <span data-ttu-id="dce10-146">В противном случае процент во всех процент-нотах для клиента накапливается и разносится в ГК в одной проводке.</span><span class="sxs-lookup"><span data-stu-id="dce10-146">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="dce10-147">Разверните или сверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="dce10-147">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="dce10-148">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="dce10-148">Click OK.</span></span>
6. <span data-ttu-id="dce10-149">В поле "Статус" выберите "Разнесено".</span><span class="sxs-lookup"><span data-stu-id="dce10-149">In the Status field, select 'Posted'.</span></span>

