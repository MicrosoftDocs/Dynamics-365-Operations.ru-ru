--- 
title: "Обработка писем-напоминаний"
description: "Ниже описан порядок создания, печати и разноски писем-напоминаний."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/04/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.translationtype: HT
ms.sourcegitcommit: 075d0f5dc0c9dc4e46dc92a2da75da9f7a207472
ms.openlocfilehash: 33d9fd62a780ab109474eefa9e322a9c529f9e72
ms.contentlocale: ru-ru
ms.lasthandoff: 12/06/2018

---
# <a name="process-collection-letters"></a><span data-ttu-id="1bd88-103">Обработка писем-напоминаний</span><span class="sxs-lookup"><span data-stu-id="1bd88-103">Process collection letters</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../../includes/preview-banner.md)]

<span data-ttu-id="1bd88-104">Ниже описан порядок создания, печати и разноски писем-напоминаний.</span><span class="sxs-lookup"><span data-stu-id="1bd88-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="1bd88-105">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="1bd88-105">This task uses the USMF demo company.</span></span>

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="1bd88-106">Настройка последовательности писем-напоминаний в профиле разноски</span><span class="sxs-lookup"><span data-stu-id="1bd88-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="1bd88-107">Перейдите в раздел **Кредит и сборы > Настройка > Профили разноски по клиенту**.</span><span class="sxs-lookup"><span data-stu-id="1bd88-107">Go to **Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="1bd88-108">Выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="1bd88-108">Click **Edit**.</span></span>
3. <span data-ttu-id="1bd88-109">Выберите последовательность писем-напоминаний из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="1bd88-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="1bd88-110">Если вы не хотите создавать письма-напоминания для проводок с использованием этого профиля разноски, оставьте поле пустым.</span><span class="sxs-lookup"><span data-stu-id="1bd88-110">If you do not want to generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
4. <span data-ttu-id="1bd88-111">Разверните вкладку табличных ограничений, чтобы изменить способ обработки писем-напоминаний.</span><span class="sxs-lookup"><span data-stu-id="1bd88-111">Expand the table restriction tab to change the way that collection letters are processed.</span></span> <span data-ttu-id="1bd88-112">Если это поле установлено на значение **Да**, для данного профиля разноски будут создаваться письма-напоминания.</span><span class="sxs-lookup"><span data-stu-id="1bd88-112">If this field is set to **Yes**, then collection letters will be created for this posting profile.</span></span>  

## <a name="create-collection-letters"></a><span data-ttu-id="1bd88-113">Создать письма-напоминания</span><span class="sxs-lookup"><span data-stu-id="1bd88-113">Create collection letters</span></span>
1. <span data-ttu-id="1bd88-114">Перейдите в раздел **Кредиты и сборы > Письмо-напоминание > Создание писем-напоминаний**.</span><span class="sxs-lookup"><span data-stu-id="1bd88-114">Go to **Credit and collections > Collection letter > Create collection letters**.</span></span>
2. <span data-ttu-id="1bd88-115">Выберите типы проводки, для которых будут использоваться письма-напоминания.</span><span class="sxs-lookup"><span data-stu-id="1bd88-115">Select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="1bd88-116">Все открытые проводки для этих типов будут включены в расчет.</span><span class="sxs-lookup"><span data-stu-id="1bd88-116">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="1bd88-117">В поле **Письмо-напоминание** выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="1bd88-117">In the **Collection letter** field, select an option.</span></span>
3. <span data-ttu-id="1bd88-118">Введите дату письма-напоминания.</span><span class="sxs-lookup"><span data-stu-id="1bd88-118">Enter the date of the collection letter.</span></span>
4. <span data-ttu-id="1bd88-119">Выберите профиль разноски, если вы изменили значение **Использовать профиль разноски из** на **Выбрать**.</span><span class="sxs-lookup"><span data-stu-id="1bd88-119">Select a posting profile if you changed **Use posting profile from** to **Select**.</span></span> <span data-ttu-id="1bd88-120">Имеются два варианта профиля разноски:</span><span class="sxs-lookup"><span data-stu-id="1bd88-120">There are two posting profile options:</span></span>   
   - <span data-ttu-id="1bd88-121">**Счет** — используется профиль разноски, назначенный для счета клиента, для каждой процент-ноты.</span><span class="sxs-lookup"><span data-stu-id="1bd88-121">**Account** – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   
   - <span data-ttu-id="1bd88-122">**Выбор** — используется профиль разноски, выбранный в поле **Профиль разноски**.</span><span class="sxs-lookup"><span data-stu-id="1bd88-122">**Select** – Use the posting profile that you select in the **Posting profile** field.</span></span>  
5. <span data-ttu-id="1bd88-123">Разверните раздел **Записи для добавления**.</span><span class="sxs-lookup"><span data-stu-id="1bd88-123">Expand the **Records to include** section.</span></span>
6. <span data-ttu-id="1bd88-124">Щелкните **Фильтр**.</span><span class="sxs-lookup"><span data-stu-id="1bd88-124">Click **Filter**.</span></span>
7. <span data-ttu-id="1bd88-125">В поле **Критерии** введите код клиента.</span><span class="sxs-lookup"><span data-stu-id="1bd88-125">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="1bd88-126">Например, введите "US-001".</span><span class="sxs-lookup"><span data-stu-id="1bd88-126">For example, enter 'US-001'.</span></span>
8. <span data-ttu-id="1bd88-127">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1bd88-127">Click **OK**.</span></span>
9. <span data-ttu-id="1bd88-128">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1bd88-128">Click **OK**.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="1bd88-129">Печатать писем-напоминаний</span><span class="sxs-lookup"><span data-stu-id="1bd88-129">Print collection letters</span></span>
1. <span data-ttu-id="1bd88-130">Перейдите в раздел **Кредиты и сборы > Письмо-напоминание > Просмотр и обработка писем-напоминаний**.</span><span class="sxs-lookup"><span data-stu-id="1bd88-130">Go to **Credit and collections > Collection letter > Review and process collection letters**.</span></span>
2. <span data-ttu-id="1bd88-131">В поле **Статус** выберите **Создано**.</span><span class="sxs-lookup"><span data-stu-id="1bd88-131">In the **Status** field, select **Created**.</span></span>
3. <span data-ttu-id="1bd88-132">В поле **Напечатано** выберите **Не напечатано**.</span><span class="sxs-lookup"><span data-stu-id="1bd88-132">In the **Printed** field, select **Not printed**.</span></span>
4. <span data-ttu-id="1bd88-133">Нажмите кнопку **Печать**.</span><span class="sxs-lookup"><span data-stu-id="1bd88-133">Click **Print**.</span></span>
5. <span data-ttu-id="1bd88-134">Щелкните **Примечание к письму-напоминанию**.</span><span class="sxs-lookup"><span data-stu-id="1bd88-134">Click **Collection letter note**.</span></span>
6. <span data-ttu-id="1bd88-135">Разверните раздел **Записи для добавления**.</span><span class="sxs-lookup"><span data-stu-id="1bd88-135">Expand the **Records to include** section.</span></span>
7. <span data-ttu-id="1bd88-136">Введите дату прекращения для разноски.</span><span class="sxs-lookup"><span data-stu-id="1bd88-136">Enter the cutoff date for postings.</span></span>
8. <span data-ttu-id="1bd88-137">Нажмите **ОК**, чтобы напечатать письмо-напоминание.</span><span class="sxs-lookup"><span data-stu-id="1bd88-137">Click **OK** to print the collection letter.</span></span>
9. <span data-ttu-id="1bd88-138">Разноска письма-напоминания.</span><span class="sxs-lookup"><span data-stu-id="1bd88-138">Post the collection letter.</span></span>
   1. <span data-ttu-id="1bd88-139">Щелкните **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="1bd88-139">Click **Post**.</span></span>
   2. <span data-ttu-id="1bd88-140">Введите дату разноски письма-напоминания".</span><span class="sxs-lookup"><span data-stu-id="1bd88-140">Enter the posting date for the collection letter.</span></span>
   3. <span data-ttu-id="1bd88-141">Разверните раздел **Записи для добавления**.</span><span class="sxs-lookup"><span data-stu-id="1bd88-141">Expand the **Records to include** section.</span></span>
   4. <span data-ttu-id="1bd88-142">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="1bd88-142">Click **OK**.</span></span>
   5. <span data-ttu-id="1bd88-143">В поле **Статус** выберите **Разнесено**.</span><span class="sxs-lookup"><span data-stu-id="1bd88-143">In the **Status** field, select **Posted**.</span></span>
   6. <span data-ttu-id="1bd88-144">В поле **Распечатано** выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="1bd88-144">In the **Printed** field, select an option.</span></span>

## <a name="control-collection-letters-at-the-customer-level"></a><span data-ttu-id="1bd88-145">Управление письмами-напоминаниями на уровне клиента</span><span class="sxs-lookup"><span data-stu-id="1bd88-145">Control collection letters at the customer level</span></span>
<span data-ttu-id="1bd88-146">Можно также настроить письма-напоминания на уровне клиентов, чтобы отслеживать код письма-напоминания для каждой проводки, но обработка писем-напоминаний будет основываться на уровне одного письма-напоминания, сохраненного для клиента.</span><span class="sxs-lookup"><span data-stu-id="1bd88-146">You can also set up collection letters at the customer level so that the collection letter code for each transaction is tracked, but the collection letter processing will be based on a single collection letter level that is stored for the customer.</span></span> <span data-ttu-id="1bd88-147">Одно письмо-напоминание будет содержать все проводки, просроченные для клиента.</span><span class="sxs-lookup"><span data-stu-id="1bd88-147">The single collection letter will contain all transactions that are overdue for the customer.</span></span> <span data-ttu-id="1bd88-148">Так как теперь льготный период отслеживается на уровне клиентов, следующее письмо-напоминание не будет отправлено, пока не пройдет количество дней льготного периода для следующего письма-напоминания в последовательности, даже если проводки станут просроченными после отправки последнего письма-напоминания.</span><span class="sxs-lookup"><span data-stu-id="1bd88-148">Because the grace days are now tracked on the customer level, the next collection letter will not be sent until the number of grace days has passed for the next collection letter in the sequence, even though transactions become overdue after the last collection letter was sent.</span></span> <span data-ttu-id="1bd88-149">Этот параметр уменьшает количество писем-напоминаний, которые будут отправлены каждому клиенту.</span><span class="sxs-lookup"><span data-stu-id="1bd88-149">This option reduces the number of collection letters you will send per customer.</span></span> 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a><span data-ttu-id="1bd88-150">Настройка клиента для управления письмами-напоминаниями на уровне клиента</span><span class="sxs-lookup"><span data-stu-id="1bd88-150">Set up the customer to control collection letters at the customer level</span></span>
1.  <span data-ttu-id="1bd88-151">Выберите **Кредит и сборы > Настройка > Параметры модуля расчетов с клиентами** и выберите вкладку **Сборы**.</span><span class="sxs-lookup"><span data-stu-id="1bd88-151">Go to **Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2.  <span data-ttu-id="1bd88-152">Измените значение **Создать письмо-напоминание для** на **Клиент**.</span><span class="sxs-lookup"><span data-stu-id="1bd88-152">Change the value of **Create collection letter per** to **Customer**.</span></span> 
3.  <span data-ttu-id="1bd88-153">Перейдите в раздел **Кредиты и сборы > Письмо-напоминание > Просмотр и обработка писем-напоминаний**.</span><span class="sxs-lookup"><span data-stu-id="1bd88-153">Go to **Credit and collections > Collection letter > Review and process collection letters**.</span></span> <span data-ttu-id="1bd88-154">Будет создано только одно письмо-напоминание для клиента со всеми просроченными проводками.</span><span class="sxs-lookup"><span data-stu-id="1bd88-154">Only one collection letter will be generated for a customer with all the overdue transactions.</span></span>

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a><span data-ttu-id="1bd88-155">Игнорировать платежи и кредит-ноты при расчете кода письма-напоминания</span><span class="sxs-lookup"><span data-stu-id="1bd88-155">Ignore payments and credit memos when calculating the collection letter code</span></span>
<span data-ttu-id="1bd88-156">Если включить платежи и кредит-ноты в проводки, которые будут включены в письма-напоминания, можно иметь платежи или кредит-ноты, которые будут запускать письмо-напоминание.</span><span class="sxs-lookup"><span data-stu-id="1bd88-156">If you include payments and credit memos in the transactions that will be included in the collection letters, you may have payments or credit memos that will trigger a collection letter.</span></span> <span data-ttu-id="1bd88-157">Можно управлять тем, каким образом платежи и кредит-ноты управляют кодом письма-напоминания, изменив значение параметра **Игнорировать платежи и кредит-ноты при расчете кода письма-напоминания**.</span><span class="sxs-lookup"><span data-stu-id="1bd88-157">You can control how payments and credit memos control the collection letter code by changing the value of the **Ignore payments and credit memos when calculating the collection letter code** parameter.</span></span> 

<span data-ttu-id="1bd88-158">Чтобы игнорировать платежи и кредит-ноты при расчете кода письма-напоминания, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1bd88-158">To ignore payments and credit memos when calculating the collection letter code, do the following.</span></span>
1. <span data-ttu-id="1bd88-159">Выберите **Кредит и сборы > Настройка > Параметры модуля расчетов с клиентами** и выберите вкладку **Сборы**.</span><span class="sxs-lookup"><span data-stu-id="1bd88-159">Go to **Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2. <span data-ttu-id="1bd88-160">Измените значение параметра **Игнорировать платежи и кредит-ноты при расчете кода письма-напоминания** на **Да**.</span><span class="sxs-lookup"><span data-stu-id="1bd88-160">Change the value of **Ignore payments and credit memos when calculating the collection letter code** to **Yes**.</span></span>

