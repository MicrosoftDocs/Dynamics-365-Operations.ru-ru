---
title: Обработка писем-напоминаний
description: В этой теме описан порядок создания, печати и разноски писем-напоминаний.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 326d9375670cb4f4990a4f7070bf923a28b2c025
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867663"
---
# <a name="process-collection-letters"></a><span data-ttu-id="04619-103">Обработка писем-напоминаний</span><span class="sxs-lookup"><span data-stu-id="04619-103">Process collection letters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="04619-104">В этой теме описан порядок создания, печати и разноски писем-напоминаний.</span><span class="sxs-lookup"><span data-stu-id="04619-104">This topic shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="04619-105">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="04619-105">This task uses the USMF demo company.</span></span>

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="04619-106">Настройка последовательности писем-напоминаний в профиле разноски</span><span class="sxs-lookup"><span data-stu-id="04619-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="04619-107">Выберите **Область перехода > Модули > Кредит и сборы > Настройка > Профили разноски по клиенту**.</span><span class="sxs-lookup"><span data-stu-id="04619-107">Go to **Navigation pane > Modules > Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="04619-108">Выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="04619-108">Click **Edit**.</span></span>
3. <span data-ttu-id="04619-109">Выберите последовательность писем-напоминаний из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="04619-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="04619-110">Если вы не хотите создавать письма-напоминания для проводок с использованием этого профиля разноски, оставьте поле пустым.</span><span class="sxs-lookup"><span data-stu-id="04619-110">If you do not want to generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
4. <span data-ttu-id="04619-111">Разверните вкладку **Табличные ограничения**, чтобы изменить способ обработки писем-напоминаний.</span><span class="sxs-lookup"><span data-stu-id="04619-111">Expand the **Table restrictions** tab to change the way that collection letters are processed.</span></span> <span data-ttu-id="04619-112">Если это поле установлено на значение **Да**, для данного профиля разноски будут создаваться письма-напоминания.</span><span class="sxs-lookup"><span data-stu-id="04619-112">If this field is set to **Yes**, then collection letters will be created for this posting profile.</span></span>  

## <a name="create-collection-letters"></a><span data-ttu-id="04619-113">Создать письма-напоминания</span><span class="sxs-lookup"><span data-stu-id="04619-113">Create collection letters</span></span>
1. <span data-ttu-id="04619-114">Выберите **Область перехода > Модули > Кредиты и сборы > Письмо-напоминание > Создание писем-напоминаний**.</span><span class="sxs-lookup"><span data-stu-id="04619-114">Go to **Navigation pane > Modules > Credit and collections > Collection letter > Create collection letters**.</span></span>
2. <span data-ttu-id="04619-115">Выберите типы проводки, для которых будут использоваться письма-напоминания.</span><span class="sxs-lookup"><span data-stu-id="04619-115">Select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="04619-116">Все открытые проводки для этих типов будут включены в расчет.</span><span class="sxs-lookup"><span data-stu-id="04619-116">All of the open transactions for these types will be included in the calculation.</span></span>  
3. <span data-ttu-id="04619-117">В поле **Письмо-напоминание** выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="04619-117">In the **Collection letter** field, select an option.</span></span>
4. <span data-ttu-id="04619-118">В поле **Дата письма-напоминания** введите дату письма-напоминания.</span><span class="sxs-lookup"><span data-stu-id="04619-118">In the **Collection letter date** field, enter the date of the collection letter.</span></span>
5. <span data-ttu-id="04619-119">Выберите профиль разноски, если вы изменили значение **Использовать профиль разноски из** на **Выбрать**.</span><span class="sxs-lookup"><span data-stu-id="04619-119">Select a posting profile if you changed **Use posting profile from** to **Select**.</span></span> <span data-ttu-id="04619-120">Имеются два варианта профиля разноски:</span><span class="sxs-lookup"><span data-stu-id="04619-120">There are two posting profile options:</span></span>   

   - <span data-ttu-id="04619-121">**Счет** — используется профиль разноски, назначенный для счета клиента, для каждой процент-ноты.</span><span class="sxs-lookup"><span data-stu-id="04619-121">**Account** – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   
   - <span data-ttu-id="04619-122">**Выбор** — используется профиль разноски, выбранный в поле **Профиль разноски**.</span><span class="sxs-lookup"><span data-stu-id="04619-122">**Select** – Use the posting profile that you select in the **Posting profile** field.</span></span>  

6. <span data-ttu-id="04619-123">Разверните раздел **Записи для добавления**.</span><span class="sxs-lookup"><span data-stu-id="04619-123">Expand the **Records to include** section.</span></span>
7. <span data-ttu-id="04619-124">Выберите **Фильтр**.</span><span class="sxs-lookup"><span data-stu-id="04619-124">Select **Filter**.</span></span>
8. <span data-ttu-id="04619-125">В поле **Критерии** введите код клиента.</span><span class="sxs-lookup"><span data-stu-id="04619-125">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="04619-126">Например, введите "US-001".</span><span class="sxs-lookup"><span data-stu-id="04619-126">For example, enter 'US-001'.</span></span>
9. <span data-ttu-id="04619-127">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="04619-127">Select **OK**.</span></span>
10. <span data-ttu-id="04619-128">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="04619-128">Select **OK**.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="04619-129">Печатать писем-напоминаний</span><span class="sxs-lookup"><span data-stu-id="04619-129">Print collection letters</span></span>
1. <span data-ttu-id="04619-130">Выберите **область перехода > Модули > Кредиты и сборы > Письмо-напоминание > Просмотр и обработка писем-напоминаний**.</span><span class="sxs-lookup"><span data-stu-id="04619-130">Go to **navigation pane > Modules > Credit and collections > Collection letter > Review and process collection letters**.</span></span>
2. <span data-ttu-id="04619-131">В поле **Статус** выберите **Создано**.</span><span class="sxs-lookup"><span data-stu-id="04619-131">In the **Status** field, select **Created**.</span></span>
3. <span data-ttu-id="04619-132">В поле **Напечатано** выберите **Не напечатано**.</span><span class="sxs-lookup"><span data-stu-id="04619-132">In the **Printed** field, select **Not printed**.</span></span>
4. <span data-ttu-id="04619-133">Выберите **Печать**.</span><span class="sxs-lookup"><span data-stu-id="04619-133">Select **Print**.</span></span>
5. <span data-ttu-id="04619-134">Выберите **Примечание к письму-напоминанию**.</span><span class="sxs-lookup"><span data-stu-id="04619-134">Select **Collection letter note**.</span></span>
6. <span data-ttu-id="04619-135">В разделе **Параметры** введите дату прекращения для разноски.</span><span class="sxs-lookup"><span data-stu-id="04619-135">In the **Parameters** section, enter the cutoff date for postings.</span></span>
7. <span data-ttu-id="04619-136">Разверните раздел **Записи для добавления** и введите сведения о примечании к письму-напоминанию.</span><span class="sxs-lookup"><span data-stu-id="04619-136">Expand the **Records to include** section and enter the details of the Collection letter note.</span></span>
8. <span data-ttu-id="04619-137">Выберите **ОК**, чтобы напечатать письмо-напоминание.</span><span class="sxs-lookup"><span data-stu-id="04619-137">Select **OK** to print the collection letter.</span></span>
9. <span data-ttu-id="04619-138">Разноска письма-напоминания.</span><span class="sxs-lookup"><span data-stu-id="04619-138">Post the collection letter.</span></span>

    1. <span data-ttu-id="04619-139">Выберите **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="04619-139">Select **Post**.</span></span>
    1. <span data-ttu-id="04619-140">Введите дату разноски письма-напоминания".</span><span class="sxs-lookup"><span data-stu-id="04619-140">Enter the posting date for the collection letter.</span></span>
    1. <span data-ttu-id="04619-141">Разверните раздел **Записи для добавления**.</span><span class="sxs-lookup"><span data-stu-id="04619-141">Expand the **Records to include** section.</span></span>
    1. <span data-ttu-id="04619-142">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="04619-142">Select **OK**.</span></span>
    1. <span data-ttu-id="04619-143">В поле **Статус** выберите **Разнесено**.</span><span class="sxs-lookup"><span data-stu-id="04619-143">In the **Status** field, select **Posted**.</span></span>
    1. <span data-ttu-id="04619-144">В поле **Распечатано** выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="04619-144">In the **Printed** field, select an option.</span></span>

## <a name="control-collection-letters-at-the-customer-level"></a><span data-ttu-id="04619-145">Управление письмами-напоминаниями на уровне клиента</span><span class="sxs-lookup"><span data-stu-id="04619-145">Control collection letters at the customer level</span></span>
<span data-ttu-id="04619-146">Можно также настроить письма-напоминания на уровне клиентов, чтобы отслеживать код письма-напоминания для каждой проводки, но обработка писем-напоминаний будет основываться на уровне одного письма-напоминания, сохраненного для клиента.</span><span class="sxs-lookup"><span data-stu-id="04619-146">You can also set up collection letters at the customer level so that the collection letter code for each transaction is tracked, but the collection letter processing will be based on a single collection letter level that is stored for the customer.</span></span> <span data-ttu-id="04619-147">Одно письмо-напоминание будет содержать все проводки, просроченные для клиента.</span><span class="sxs-lookup"><span data-stu-id="04619-147">The single collection letter will contain all transactions that are overdue for the customer.</span></span> <span data-ttu-id="04619-148">Так как теперь льготный период отслеживается на уровне клиентов, следующее письмо-напоминание не будет отправлено, пока не пройдет количество дней льготного периода для следующего письма-напоминания в последовательности, даже если проводки станут просроченными после отправки последнего письма-напоминания.</span><span class="sxs-lookup"><span data-stu-id="04619-148">Because the grace days are now tracked on the customer level, the next collection letter will not be sent until the number of grace days has passed for the next collection letter in the sequence, even though transactions become overdue after the last collection letter was sent.</span></span> <span data-ttu-id="04619-149">Этот параметр уменьшает количество писем-напоминаний, которые будут отправлены каждому клиенту.</span><span class="sxs-lookup"><span data-stu-id="04619-149">This option reduces the number of collection letters you will send per customer.</span></span> 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a><span data-ttu-id="04619-150">Настройка клиента для управления письмами-напоминаниями на уровне клиента</span><span class="sxs-lookup"><span data-stu-id="04619-150">Set up the customer to control collection letters at the customer level</span></span>
1.  <span data-ttu-id="04619-151">Выберите **Область переходов > Модули > Кредит и сборы > Настройка > Параметры модуля расчетов с клиентами** и выберите вкладку **Сборы**.</span><span class="sxs-lookup"><span data-stu-id="04619-151">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters** and select the **Collections** tab.</span></span> 
2.  <span data-ttu-id="04619-152">Измените значение **Создать письмо-напоминание для** на **Клиент**.</span><span class="sxs-lookup"><span data-stu-id="04619-152">Change the value of **Create collection letter per** to **Customer**.</span></span> 
3.  <span data-ttu-id="04619-153">Выберите **область перехода > Модули > Кредиты и сборы > Письмо-напоминание > Просмотр и обработка писем-напоминаний**.</span><span class="sxs-lookup"><span data-stu-id="04619-153">Go to **navigation pane > Modules > Credit and collections > Collection letter > Review and process collection letters**.</span></span> <span data-ttu-id="04619-154">Будет создано только одно письмо-напоминание для клиента со всеми просроченными проводками.</span><span class="sxs-lookup"><span data-stu-id="04619-154">Only one collection letter will be generated for a customer with all the overdue transactions.</span></span>

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a><span data-ttu-id="04619-155">Игнорировать платежи и кредит-ноты при расчете кода письма-напоминания</span><span class="sxs-lookup"><span data-stu-id="04619-155">Ignore payments and credit memos when calculating the collection letter code</span></span>
<span data-ttu-id="04619-156">Если включить платежи и кредит-ноты в проводки, которые будут включены в письма-напоминания, можно иметь платежи или кредит-ноты, которые будут запускать письмо-напоминание.</span><span class="sxs-lookup"><span data-stu-id="04619-156">If you include payments and credit memos in the transactions that will be included in the collection letters, you may have payments or credit memos that will trigger a collection letter.</span></span> <span data-ttu-id="04619-157">Можно управлять тем, каким образом платежи и кредит-ноты управляют кодом письма-напоминания, изменив значение параметра **Игнорировать платежи и кредит-ноты при расчете кода письма-напоминания**.</span><span class="sxs-lookup"><span data-stu-id="04619-157">You can control how payments and credit memos control the collection letter code by changing the value of the **Ignore payments and credit memos when calculating the collection letter code** parameter.</span></span> 

<span data-ttu-id="04619-158">Чтобы игнорировать платежи и кредит-ноты при расчете кода письма-напоминания, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="04619-158">To ignore payments and credit memos when calculating the collection letter code, do the following.</span></span>

1. <span data-ttu-id="04619-159">Выберите **Область переходов > Модули > Кредит и сборы > Настройка > Параметры модуля расчетов с клиентами** и щелкните вкладку **Сборы**.</span><span class="sxs-lookup"><span data-stu-id="04619-159">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2. <span data-ttu-id="04619-160">Измените значение параметра **Игнорировать платежи и кредит-ноты при расчете кода письма-напоминания** на **Да**.</span><span class="sxs-lookup"><span data-stu-id="04619-160">Change the value of **Ignore payments and credit memos when calculating the collection letter code** to **Yes**.</span></span>
