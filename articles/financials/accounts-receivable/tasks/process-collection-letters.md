--- 
title: "Обработка писем-напоминаний"
description: "Ниже описан порядок создания, печати и разноски писем-напоминаний."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: dc837ea6513992a5f94e48baa366e279df297866
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="process-collection-letters"></a><span data-ttu-id="aad97-103">Обработка писем-напоминаний</span><span class="sxs-lookup"><span data-stu-id="aad97-103">Process collection letters</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aad97-104">Ниже описан порядок создания, печати и разноски писем-напоминаний.</span><span class="sxs-lookup"><span data-stu-id="aad97-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="aad97-105">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="aad97-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="aad97-106">Настройка последовательности писем-напоминаний в профиле разноски</span><span class="sxs-lookup"><span data-stu-id="aad97-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="aad97-107">Перейдите в раздел "Кредит и сборы" > "Настройка" > "Профили разноски по клиенту".</span><span class="sxs-lookup"><span data-stu-id="aad97-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="aad97-108">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="aad97-108">Click Edit.</span></span>
    * <span data-ttu-id="aad97-109">Выберите последовательность писем-напоминаний из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="aad97-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="aad97-110">Если вы не хотите создавать письма-напоминания для проводок с использованием этого профиля разноски, оставьте поле пустым.</span><span class="sxs-lookup"><span data-stu-id="aad97-110">If you do not want generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="aad97-111">Вкладка табличных ограничений позволяет изменить способ обработки писем-напоминаний.</span><span class="sxs-lookup"><span data-stu-id="aad97-111">The table restriction tab allows you to change the way that collection letters are processed.</span></span> <span data-ttu-id="aad97-112">Если это поле установлено на значение "Да", для данного профиля разноски будут создаваться письма-напоминания.</span><span class="sxs-lookup"><span data-stu-id="aad97-112">If this field is set to Yes, then collection letters will be created for this posting profile.</span></span>  
3. <span data-ttu-id="aad97-113">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="aad97-113">Close the page.</span></span>

## <a name="create-collection-letters"></a><span data-ttu-id="aad97-114">Создать письма-напоминания</span><span class="sxs-lookup"><span data-stu-id="aad97-114">Create collection letters</span></span>
1. <span data-ttu-id="aad97-115">Перейдите в раздел "Кредиты и сборы" > "Письмо-напоминание" > "Создание писем-напоминаний".</span><span class="sxs-lookup"><span data-stu-id="aad97-115">Go to Credit and collections > Collection letter > Create collection letters.</span></span>
    * <span data-ttu-id="aad97-116">Необходимо выбрать типы проводки, для которых будут использоваться письма-напоминания.</span><span class="sxs-lookup"><span data-stu-id="aad97-116">You must select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="aad97-117">Все открытые проводки для этих типов будут включены в расчет.</span><span class="sxs-lookup"><span data-stu-id="aad97-117">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="aad97-118">В поле "Письмо-напоминание" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="aad97-118">In the Collection letter field, select an option.</span></span>
3. <span data-ttu-id="aad97-119">Введите дату письма-напоминания.</span><span class="sxs-lookup"><span data-stu-id="aad97-119">Enter the date of the collection letter.</span></span>
    * <span data-ttu-id="aad97-120">Есть два параметра профиля разноски:   "Счет" — используется профиль разноски, назначенный для счета клиента для каждой процент-ноты.</span><span class="sxs-lookup"><span data-stu-id="aad97-120">There are two posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="aad97-121">"Выбор" — используется профиль разноски, выбранный в поле "Профиль разноски".</span><span class="sxs-lookup"><span data-stu-id="aad97-121">Select – Use the posting profile that you select in the Posting profile field.</span></span>  
    * <span data-ttu-id="aad97-122">Выберите профиль разноски, если вы изменили значение "Использовать профиль разноски из" на "Выбрать".</span><span class="sxs-lookup"><span data-stu-id="aad97-122">Select a posting profile if you changed "Use posting profile from" to "Select".</span></span>  
4. <span data-ttu-id="aad97-123">Разверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="aad97-123">Expand the Records to include section.</span></span>
5. <span data-ttu-id="aad97-124">Щелкните "Фильтр".</span><span class="sxs-lookup"><span data-stu-id="aad97-124">Click Filter.</span></span>
6. <span data-ttu-id="aad97-125">В поле "Критерии" введите код клиента.</span><span class="sxs-lookup"><span data-stu-id="aad97-125">In the Criteria field, In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="aad97-126">Например, введите "US-001".</span><span class="sxs-lookup"><span data-stu-id="aad97-126">For example, enter 'US-001'..</span></span>
7. <span data-ttu-id="aad97-127">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="aad97-127">Click OK.</span></span>
8. <span data-ttu-id="aad97-128">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="aad97-128">Click OK.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="aad97-129">Печатать писем-напоминаний</span><span class="sxs-lookup"><span data-stu-id="aad97-129">Print collection letters</span></span>
1. <span data-ttu-id="aad97-130">Перейдите в раздел "Кредиты и сборы" > "Письмо-напоминание" > "Просмотр и обработка писем-напоминаний".</span><span class="sxs-lookup"><span data-stu-id="aad97-130">Go to Credit and collections > Collection letter > Review and process collection letters.</span></span>
2. <span data-ttu-id="aad97-131">В поле "Статус" выберите "Создано".</span><span class="sxs-lookup"><span data-stu-id="aad97-131">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="aad97-132">В поле "Напечатано" выберите "Не напечатано".</span><span class="sxs-lookup"><span data-stu-id="aad97-132">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="aad97-133">Нажмите кнопку Печать.</span><span class="sxs-lookup"><span data-stu-id="aad97-133">Click Print.</span></span>
5. <span data-ttu-id="aad97-134">Щелкните "Примечание к письму-напоминанию".</span><span class="sxs-lookup"><span data-stu-id="aad97-134">Click Collection letter note.</span></span>
6. <span data-ttu-id="aad97-135">Разверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="aad97-135">Expand the Records to include section.</span></span>
7. <span data-ttu-id="aad97-136">Введите дату прекращения для разноски.</span><span class="sxs-lookup"><span data-stu-id="aad97-136">Enter the cutoff date for postings</span></span>
8. <span data-ttu-id="aad97-137">Нажмите "ОК", чтобы напечатать письмо-напоминание.</span><span class="sxs-lookup"><span data-stu-id="aad97-137">Click OK to print the collection letter.</span></span>

## <a name="post-the-collection-letter"></a><span data-ttu-id="aad97-138">Разноска письма-напоминания</span><span class="sxs-lookup"><span data-stu-id="aad97-138">Post the collection letter</span></span>
1. <span data-ttu-id="aad97-139">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="aad97-139">Click Post.</span></span>
2. <span data-ttu-id="aad97-140">Введите дату разноски письма-напоминания".</span><span class="sxs-lookup"><span data-stu-id="aad97-140">Enter the posting date for the collection letter.</span></span>
3. <span data-ttu-id="aad97-141">Разверните раздел "Записи для добавления".</span><span class="sxs-lookup"><span data-stu-id="aad97-141">Expand the Records to include section.</span></span>
4. <span data-ttu-id="aad97-142">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="aad97-142">Click OK.</span></span>
5. <span data-ttu-id="aad97-143">В поле "Статус" выберите "Разнесено".</span><span class="sxs-lookup"><span data-stu-id="aad97-143">In the Status field, select 'Posted'.</span></span>
6. <span data-ttu-id="aad97-144">В поле "Распечатано" выберите параметр.</span><span class="sxs-lookup"><span data-stu-id="aad97-144">In the Printed field, select an option.</span></span>


