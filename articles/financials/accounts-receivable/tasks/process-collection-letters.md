---
title: Обработка писем-напоминаний
description: Ниже описан порядок создания, печати и разноски писем-напоминаний.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/04/2018
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
ms.openlocfilehash: 8db80b184d565f71f62f99051c7378c4e6e45fb9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834423"
---
# <a name="process-collection-letters"></a><span data-ttu-id="d591f-103">Обработка писем-напоминаний</span><span class="sxs-lookup"><span data-stu-id="d591f-103">Process collection letters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d591f-104">Ниже описан порядок создания, печати и разноски писем-напоминаний.</span><span class="sxs-lookup"><span data-stu-id="d591f-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="d591f-105">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="d591f-105">This task uses the USMF demo company.</span></span>

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="d591f-106">Настройка последовательности писем-напоминаний в профиле разноски</span><span class="sxs-lookup"><span data-stu-id="d591f-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="d591f-107">Перейдите в раздел **Кредит и сборы > Настройка > Профили разноски по клиенту**.</span><span class="sxs-lookup"><span data-stu-id="d591f-107">Go to **Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="d591f-108">Выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="d591f-108">Click **Edit**.</span></span>
3. <span data-ttu-id="d591f-109">Выберите последовательность писем-напоминаний из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="d591f-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="d591f-110">Если вы не хотите создавать письма-напоминания для проводок с использованием этого профиля разноски, оставьте поле пустым.</span><span class="sxs-lookup"><span data-stu-id="d591f-110">If you do not want to generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
4. <span data-ttu-id="d591f-111">Разверните вкладку табличных ограничений, чтобы изменить способ обработки писем-напоминаний.</span><span class="sxs-lookup"><span data-stu-id="d591f-111">Expand the table restriction tab to change the way that collection letters are processed.</span></span> <span data-ttu-id="d591f-112">Если это поле установлено на значение **Да**, для данного профиля разноски будут создаваться письма-напоминания.</span><span class="sxs-lookup"><span data-stu-id="d591f-112">If this field is set to **Yes**, then collection letters will be created for this posting profile.</span></span>  

## <a name="create-collection-letters"></a><span data-ttu-id="d591f-113">Создать письма-напоминания</span><span class="sxs-lookup"><span data-stu-id="d591f-113">Create collection letters</span></span>
1. <span data-ttu-id="d591f-114">Перейдите в раздел **Кредиты и сборы > Письмо-напоминание > Создание писем-напоминаний**.</span><span class="sxs-lookup"><span data-stu-id="d591f-114">Go to **Credit and collections > Collection letter > Create collection letters**.</span></span>
2. <span data-ttu-id="d591f-115">Выберите типы проводки, для которых будут использоваться письма-напоминания.</span><span class="sxs-lookup"><span data-stu-id="d591f-115">Select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="d591f-116">Все открытые проводки для этих типов будут включены в расчет.</span><span class="sxs-lookup"><span data-stu-id="d591f-116">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="d591f-117">В поле **Письмо-напоминание** выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="d591f-117">In the **Collection letter** field, select an option.</span></span>
3. <span data-ttu-id="d591f-118">Введите дату письма-напоминания.</span><span class="sxs-lookup"><span data-stu-id="d591f-118">Enter the date of the collection letter.</span></span>
4. <span data-ttu-id="d591f-119">Выберите профиль разноски, если вы изменили значение **Использовать профиль разноски из** на **Выбрать**.</span><span class="sxs-lookup"><span data-stu-id="d591f-119">Select a posting profile if you changed **Use posting profile from** to **Select**.</span></span> <span data-ttu-id="d591f-120">Имеются два варианта профиля разноски:</span><span class="sxs-lookup"><span data-stu-id="d591f-120">There are two posting profile options:</span></span>   
   - <span data-ttu-id="d591f-121">**Счет** — используется профиль разноски, назначенный для счета клиента, для каждой процент-ноты.</span><span class="sxs-lookup"><span data-stu-id="d591f-121">**Account** – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   
   - <span data-ttu-id="d591f-122">**Выбор** — используется профиль разноски, выбранный в поле **Профиль разноски**.</span><span class="sxs-lookup"><span data-stu-id="d591f-122">**Select** – Use the posting profile that you select in the **Posting profile** field.</span></span>  
5. <span data-ttu-id="d591f-123">Разверните раздел **Записи для добавления**.</span><span class="sxs-lookup"><span data-stu-id="d591f-123">Expand the **Records to include** section.</span></span>
6. <span data-ttu-id="d591f-124">Щелкните **Фильтр**.</span><span class="sxs-lookup"><span data-stu-id="d591f-124">Click **Filter**.</span></span>
7. <span data-ttu-id="d591f-125">В поле **Критерии** введите код клиента.</span><span class="sxs-lookup"><span data-stu-id="d591f-125">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="d591f-126">Например, введите "US-001".</span><span class="sxs-lookup"><span data-stu-id="d591f-126">For example, enter 'US-001'.</span></span>
8. <span data-ttu-id="d591f-127">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d591f-127">Click **OK**.</span></span>
9. <span data-ttu-id="d591f-128">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d591f-128">Click **OK**.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="d591f-129">Печатать писем-напоминаний</span><span class="sxs-lookup"><span data-stu-id="d591f-129">Print collection letters</span></span>
1. <span data-ttu-id="d591f-130">Перейдите в раздел **Кредиты и сборы > Письмо-напоминание > Просмотр и обработка писем-напоминаний**.</span><span class="sxs-lookup"><span data-stu-id="d591f-130">Go to **Credit and collections > Collection letter > Review and process collection letters**.</span></span>
2. <span data-ttu-id="d591f-131">В поле **Статус** выберите **Создано**.</span><span class="sxs-lookup"><span data-stu-id="d591f-131">In the **Status** field, select **Created**.</span></span>
3. <span data-ttu-id="d591f-132">В поле **Напечатано** выберите **Не напечатано**.</span><span class="sxs-lookup"><span data-stu-id="d591f-132">In the **Printed** field, select **Not printed**.</span></span>
4. <span data-ttu-id="d591f-133">Нажмите кнопку **Печать**.</span><span class="sxs-lookup"><span data-stu-id="d591f-133">Click **Print**.</span></span>
5. <span data-ttu-id="d591f-134">Щелкните **Примечание к письму-напоминанию**.</span><span class="sxs-lookup"><span data-stu-id="d591f-134">Click **Collection letter note**.</span></span>
6. <span data-ttu-id="d591f-135">Разверните раздел **Записи для добавления**.</span><span class="sxs-lookup"><span data-stu-id="d591f-135">Expand the **Records to include** section.</span></span>
7. <span data-ttu-id="d591f-136">Введите дату прекращения для разноски.</span><span class="sxs-lookup"><span data-stu-id="d591f-136">Enter the cutoff date for postings.</span></span>
8. <span data-ttu-id="d591f-137">Нажмите **ОК**, чтобы напечатать письмо-напоминание.</span><span class="sxs-lookup"><span data-stu-id="d591f-137">Click **OK** to print the collection letter.</span></span>
9. <span data-ttu-id="d591f-138">Разноска письма-напоминания.</span><span class="sxs-lookup"><span data-stu-id="d591f-138">Post the collection letter.</span></span>
   1. <span data-ttu-id="d591f-139">Щелкните **Разнести**.</span><span class="sxs-lookup"><span data-stu-id="d591f-139">Click **Post**.</span></span>
   2. <span data-ttu-id="d591f-140">Введите дату разноски письма-напоминания".</span><span class="sxs-lookup"><span data-stu-id="d591f-140">Enter the posting date for the collection letter.</span></span>
   3. <span data-ttu-id="d591f-141">Разверните раздел **Записи для добавления**.</span><span class="sxs-lookup"><span data-stu-id="d591f-141">Expand the **Records to include** section.</span></span>
   4. <span data-ttu-id="d591f-142">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d591f-142">Click **OK**.</span></span>
   5. <span data-ttu-id="d591f-143">В поле **Статус** выберите **Разнесено**.</span><span class="sxs-lookup"><span data-stu-id="d591f-143">In the **Status** field, select **Posted**.</span></span>
   6. <span data-ttu-id="d591f-144">В поле **Распечатано** выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="d591f-144">In the **Printed** field, select an option.</span></span>

## <a name="control-collection-letters-at-the-customer-level"></a><span data-ttu-id="d591f-145">Управление письмами-напоминаниями на уровне клиента</span><span class="sxs-lookup"><span data-stu-id="d591f-145">Control collection letters at the customer level</span></span>
<span data-ttu-id="d591f-146">Можно также настроить письма-напоминания на уровне клиентов, чтобы отслеживать код письма-напоминания для каждой проводки, но обработка писем-напоминаний будет основываться на уровне одного письма-напоминания, сохраненного для клиента.</span><span class="sxs-lookup"><span data-stu-id="d591f-146">You can also set up collection letters at the customer level so that the collection letter code for each transaction is tracked, but the collection letter processing will be based on a single collection letter level that is stored for the customer.</span></span> <span data-ttu-id="d591f-147">Одно письмо-напоминание будет содержать все проводки, просроченные для клиента.</span><span class="sxs-lookup"><span data-stu-id="d591f-147">The single collection letter will contain all transactions that are overdue for the customer.</span></span> <span data-ttu-id="d591f-148">Так как теперь льготный период отслеживается на уровне клиентов, следующее письмо-напоминание не будет отправлено, пока не пройдет количество дней льготного периода для следующего письма-напоминания в последовательности, даже если проводки станут просроченными после отправки последнего письма-напоминания.</span><span class="sxs-lookup"><span data-stu-id="d591f-148">Because the grace days are now tracked on the customer level, the next collection letter will not be sent until the number of grace days has passed for the next collection letter in the sequence, even though transactions become overdue after the last collection letter was sent.</span></span> <span data-ttu-id="d591f-149">Этот параметр уменьшает количество писем-напоминаний, которые будут отправлены каждому клиенту.</span><span class="sxs-lookup"><span data-stu-id="d591f-149">This option reduces the number of collection letters you will send per customer.</span></span> 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a><span data-ttu-id="d591f-150">Настройка клиента для управления письмами-напоминаниями на уровне клиента</span><span class="sxs-lookup"><span data-stu-id="d591f-150">Set up the customer to control collection letters at the customer level</span></span>
1.  <span data-ttu-id="d591f-151">Выберите **Кредит и сборы > Настройка > Параметры модуля расчетов с клиентами** и выберите вкладку **Сборы**.</span><span class="sxs-lookup"><span data-stu-id="d591f-151">Go to **Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2.  <span data-ttu-id="d591f-152">Измените значение **Создать письмо-напоминание для** на **Клиент**.</span><span class="sxs-lookup"><span data-stu-id="d591f-152">Change the value of **Create collection letter per** to **Customer**.</span></span> 
3.  <span data-ttu-id="d591f-153">Перейдите в раздел **Кредиты и сборы > Письмо-напоминание > Просмотр и обработка писем-напоминаний**.</span><span class="sxs-lookup"><span data-stu-id="d591f-153">Go to **Credit and collections > Collection letter > Review and process collection letters**.</span></span> <span data-ttu-id="d591f-154">Будет создано только одно письмо-напоминание для клиента со всеми просроченными проводками.</span><span class="sxs-lookup"><span data-stu-id="d591f-154">Only one collection letter will be generated for a customer with all the overdue transactions.</span></span>

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a><span data-ttu-id="d591f-155">Игнорировать платежи и кредит-ноты при расчете кода письма-напоминания</span><span class="sxs-lookup"><span data-stu-id="d591f-155">Ignore payments and credit memos when calculating the collection letter code</span></span>
<span data-ttu-id="d591f-156">Если включить платежи и кредит-ноты в проводки, которые будут включены в письма-напоминания, можно иметь платежи или кредит-ноты, которые будут запускать письмо-напоминание.</span><span class="sxs-lookup"><span data-stu-id="d591f-156">If you include payments and credit memos in the transactions that will be included in the collection letters, you may have payments or credit memos that will trigger a collection letter.</span></span> <span data-ttu-id="d591f-157">Можно управлять тем, каким образом платежи и кредит-ноты управляют кодом письма-напоминания, изменив значение параметра **Игнорировать платежи и кредит-ноты при расчете кода письма-напоминания**.</span><span class="sxs-lookup"><span data-stu-id="d591f-157">You can control how payments and credit memos control the collection letter code by changing the value of the **Ignore payments and credit memos when calculating the collection letter code** parameter.</span></span> 

<span data-ttu-id="d591f-158">Чтобы игнорировать платежи и кредит-ноты при расчете кода письма-напоминания, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d591f-158">To ignore payments and credit memos when calculating the collection letter code, do the following.</span></span>
1. <span data-ttu-id="d591f-159">Выберите **Кредит и сборы > Настройка > Параметры модуля расчетов с клиентами** и выберите вкладку **Сборы**.</span><span class="sxs-lookup"><span data-stu-id="d591f-159">Go to **Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2. <span data-ttu-id="d591f-160">Измените значение параметра **Игнорировать платежи и кредит-ноты при расчете кода письма-напоминания** на **Да**.</span><span class="sxs-lookup"><span data-stu-id="d591f-160">Change the value of **Ignore payments and credit memos when calculating the collection letter code** to **Yes**.</span></span>
