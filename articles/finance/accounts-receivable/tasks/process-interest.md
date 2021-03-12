---
title: Обработка процента
description: В этой процедуре показано, как создать, напечатать и разнести процент-ноты.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ad30984f55017ee275af15ddb4f1a46c6a50db69
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992947"
---
# <a name="process-interest"></a><span data-ttu-id="7f17c-103">Обработка процента</span><span class="sxs-lookup"><span data-stu-id="7f17c-103">Process interest</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7f17c-104">В этой процедуре показано, как создать, напечатать и разнести процент-ноты.</span><span class="sxs-lookup"><span data-stu-id="7f17c-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="7f17c-105">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="7f17c-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="7f17c-106">Настройка процента в профиле разноски</span><span class="sxs-lookup"><span data-stu-id="7f17c-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="7f17c-107">В области **Область перехода** выберите **Модули > Кредит и сборы > Настройка > Профили разноски по клиенту**.</span><span class="sxs-lookup"><span data-stu-id="7f17c-107">In the **Navigation pane**, go to **Modules > Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="7f17c-108">Выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="7f17c-108">Click **Edit**.</span></span>
3. <span data-ttu-id="7f17c-109">На экспресс-вкладке **Настройка** в поле **Код процента** выберите код процента из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="7f17c-109">In the **Setup fastTab**, in the **Interest code** field, select an interest code from the drop-down list.</span></span> <span data-ttu-id="7f17c-110">Если вы не хотите рассчитывать процент для проводок с использованием этого профиля разноски, оставьте поле пустым.</span><span class="sxs-lookup"><span data-stu-id="7f17c-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span> <span data-ttu-id="7f17c-111">Экспресс-вкладка **Табличные ограничения** позволяет изменить способ обработки процента.</span><span class="sxs-lookup"><span data-stu-id="7f17c-111">The **Table restriction** fastTab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="7f17c-112">Если в этом поле установить значение "Да", процент будет рассчитан для данного профиля разноски.</span><span class="sxs-lookup"><span data-stu-id="7f17c-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="7f17c-113">Рассчитать процент</span><span class="sxs-lookup"><span data-stu-id="7f17c-113">Calculate interest</span></span>
1. <span data-ttu-id="7f17c-114">В области **Область перехода** выберите **Модули > Кредит и сборы > Процент > Создание процент-нот**.</span><span class="sxs-lookup"><span data-stu-id="7f17c-114">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Create interest notes**.</span></span>
2. <span data-ttu-id="7f17c-115">Необходимо выбрать типы проводки, для которых будет рассчитываться процент.</span><span class="sxs-lookup"><span data-stu-id="7f17c-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="7f17c-116">Все открытые проводки для этих типов будут включены в расчет.</span><span class="sxs-lookup"><span data-stu-id="7f17c-116">All of the open transactions for these types will be included in the calculation.</span></span>  
3. <span data-ttu-id="7f17c-117">Если в поле **Процент** задано значение "Да", будет рассчитан процент по процентам.</span><span class="sxs-lookup"><span data-stu-id="7f17c-117">If you set **Interest** to 'Yes', you will calculate interest on interest.</span></span> <span data-ttu-id="7f17c-118">Возможно, потребуется проверить законодательство по расчету процентов по процентам до их включения в проводку.</span><span class="sxs-lookup"><span data-stu-id="7f17c-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
4. <span data-ttu-id="7f17c-119">В поле **Начальная дата** введите дату, с которой будут рассчитываться проценты.</span><span class="sxs-lookup"><span data-stu-id="7f17c-119">In the **From date** field, enter a date from which the interest will be calculated.</span></span> <span data-ttu-id="7f17c-120">Если не указать значение в поле **Дата начала**, все неразнесенные процент-ноты будут отменены и процент будет пересчитан от даты проводки.</span><span class="sxs-lookup"><span data-stu-id="7f17c-120">If you do not specific a **From date**, then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>
5. <span data-ttu-id="7f17c-121">В поле **Конечная дата** введите дату, до которой будут рассчитываться проценты.</span><span class="sxs-lookup"><span data-stu-id="7f17c-121">In the **To date** field, enter a date to which the interest would be calculated.</span></span>
6. <span data-ttu-id="7f17c-122">В поле **Использовать профиль разноски из** выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="7f17c-122">In the **Use posting profile from** field, select an option.</span></span> <span data-ttu-id="7f17c-123">Имеются три варианта профиля разноски:</span><span class="sxs-lookup"><span data-stu-id="7f17c-123">There are three posting profile options:</span></span>
    - <span data-ttu-id="7f17c-124">Счет — используется профиль разноски, назначенный для счета клиента, для каждой процент-ноты.</span><span class="sxs-lookup"><span data-stu-id="7f17c-124">Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span> 
    - <span data-ttu-id="7f17c-125">"Выбор" — используется профиль разноски, выбранный в поле "Профиль разноски".</span><span class="sxs-lookup"><span data-stu-id="7f17c-125">Select – Use the posting profile that you select in the Posting profile field.</span></span>
    - <span data-ttu-id="7f17c-126">"Проводка" — используется отдельный профиль разноски из проводок, по которым рассчитывается процент для каждой процент-ноты.</span><span class="sxs-lookup"><span data-stu-id="7f17c-126">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="7f17c-127">Проводки без назначенного профиля разноски используют профиль разноски, который указан в области "Главная книга и налог" формы "Параметры расчетов с клиентами".</span><span class="sxs-lookup"><span data-stu-id="7f17c-127">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
7. <span data-ttu-id="7f17c-128">Разверните экспресс-вкладку **Записи для добавления**.</span><span class="sxs-lookup"><span data-stu-id="7f17c-128">Expand the **Records to include** fastTab.</span></span>
8. <span data-ttu-id="7f17c-129">Щелкните **Фильтр**.</span><span class="sxs-lookup"><span data-stu-id="7f17c-129">Click **Filter**.</span></span>
9. <span data-ttu-id="7f17c-130">В поле **Критерии** введите код клиента.</span><span class="sxs-lookup"><span data-stu-id="7f17c-130">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="7f17c-131">Например, введите "US-001".</span><span class="sxs-lookup"><span data-stu-id="7f17c-131">For example, enter 'US-001'.</span></span>
6. <span data-ttu-id="7f17c-132">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="7f17c-132">Click **OK**.</span></span>
7. <span data-ttu-id="7f17c-133">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="7f17c-133">Click **OK**.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="7f17c-134">Печать процент-нот</span><span class="sxs-lookup"><span data-stu-id="7f17c-134">Print interest notes</span></span>
1. <span data-ttu-id="7f17c-135">В области **Область перехода** выберите **Модули > Кредит и сборы > Процент > Просмотр и обработка процент-нот**.</span><span class="sxs-lookup"><span data-stu-id="7f17c-135">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Review and process interest notes**.</span></span>
2. <span data-ttu-id="7f17c-136">В поле **Статус** выберите "Создано".</span><span class="sxs-lookup"><span data-stu-id="7f17c-136">In the **Status** field, select 'Created'.</span></span>
3. <span data-ttu-id="7f17c-137">В поле **Напечатано** выберите "Не напечатано".</span><span class="sxs-lookup"><span data-stu-id="7f17c-137">In the **Printed** field, select 'Not printed'.</span></span>
4. <span data-ttu-id="7f17c-138">Нажмите кнопку **Печать**.</span><span class="sxs-lookup"><span data-stu-id="7f17c-138">Click **Print**.</span></span>
5. <span data-ttu-id="7f17c-139">Разверните экспресс-вкладку **Записи для добавления**.</span><span class="sxs-lookup"><span data-stu-id="7f17c-139">Expand the **Records to include** fastTab.</span></span>
6. <span data-ttu-id="7f17c-140">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="7f17c-140">Click **OK**.</span></span>
7. <span data-ttu-id="7f17c-141">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="7f17c-141">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="7f17c-142">Разноска процент-ноты</span><span class="sxs-lookup"><span data-stu-id="7f17c-142">Post the interest note</span></span>
1. <span data-ttu-id="7f17c-143">Выберите процент-ноту, готовую к разноске (статус "Создано").</span><span class="sxs-lookup"><span data-stu-id="7f17c-143">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="7f17c-144">Щелкните **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="7f17c-144">Click **Post**.</span></span>
3. <span data-ttu-id="7f17c-145">Введите дату разноски для процент-ноты.</span><span class="sxs-lookup"><span data-stu-id="7f17c-145">Enter the posting date for the interest note.</span></span> <span data-ttu-id="7f17c-146">Выберите значение "Да", чтобы создать проводку главной книги для каждой процент-ноты.</span><span class="sxs-lookup"><span data-stu-id="7f17c-146">Select Yes to create a general ledger transaction for each interest note.</span></span> <span data-ttu-id="7f17c-147">В противном случае процент во всех процент-нотах для клиента накапливается и разносится в ГК в одной проводке.</span><span class="sxs-lookup"><span data-stu-id="7f17c-147">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="7f17c-148">Разверните экспресс-вкладку **Записи для добавления**.</span><span class="sxs-lookup"><span data-stu-id="7f17c-148">Expand the **Records to include** fastTab.</span></span>
5. <span data-ttu-id="7f17c-149">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="7f17c-149">Click **OK**.</span></span>
6. <span data-ttu-id="7f17c-150">В поле **Статус** выберите "Разнесено".</span><span class="sxs-lookup"><span data-stu-id="7f17c-150">In the **Status** field, select 'Posted'.</span></span>

