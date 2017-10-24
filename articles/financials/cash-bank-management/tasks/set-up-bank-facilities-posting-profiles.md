--- 
title: "Настройка банковских услуг и профилей разноски для гарантийного письма"
description: "Эта задача создает банковскую услугу и профиль разноски, который необходим для обработки гарантийного письма."
author: kweekley
manager: AnnBe
ms.date: 02/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 022b5d411b8240390c543ba726fe0d6838752944
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="b4204-103">Настройка банковских услуг и профилей разноски для гарантийного письма</span><span class="sxs-lookup"><span data-stu-id="b4204-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b4204-104">Эта задача создает банковскую услугу и профиль разноски, который необходим для обработки гарантийного письма.</span><span class="sxs-lookup"><span data-stu-id="b4204-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="b4204-105">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="b4204-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="b4204-106">Параметр главной книги</span><span class="sxs-lookup"><span data-stu-id="b4204-106">General ledger parameter</span></span>
1. <span data-ttu-id="b4204-107">Перейдите в раздел "Управление банком и кассовыми операциями" > "Настройка" > "Параметры управления банком и кассовыми операциями".</span><span class="sxs-lookup"><span data-stu-id="b4204-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="b4204-108">Разверните раздел "Банковский документ".</span><span class="sxs-lookup"><span data-stu-id="b4204-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="b4204-109">Выберите параметр "Разрешить гарантийные письма".</span><span class="sxs-lookup"><span data-stu-id="b4204-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="b4204-110">В поле "Журнал проводок" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="b4204-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="b4204-111">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="b4204-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="b4204-112">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="b4204-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="b4204-113">Откройте вкладку Номерные серии.</span><span class="sxs-lookup"><span data-stu-id="b4204-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="b4204-114">Определение кода номерной серии для номеров гарантийного письма и ссылок на проводки гарантийного письма</span><span class="sxs-lookup"><span data-stu-id="b4204-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="b4204-115">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="b4204-115">Click Save.</span></span>
9. <span data-ttu-id="b4204-116">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b4204-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="b4204-117">Создание банковской услуги</span><span class="sxs-lookup"><span data-stu-id="b4204-117">Create Bank facility</span></span>
1. <span data-ttu-id="b4204-118">Перейдите в раздел "Управление банком и кассовыми операциями" > "Настройка" > "Банковские ссуды".</span><span class="sxs-lookup"><span data-stu-id="b4204-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="b4204-119">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="b4204-119">Click New.</span></span>
3. <span data-ttu-id="b4204-120">В поле "Группа ссуды" введите имя группы банковских услуг для проводки гарантийного письма.</span><span class="sxs-lookup"><span data-stu-id="b4204-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="b4204-121">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b4204-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b4204-122">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="b4204-122">Click Save.</span></span>
6. <span data-ttu-id="b4204-123">Перейдите на вкладку "Типы ссуд".</span><span class="sxs-lookup"><span data-stu-id="b4204-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="b4204-124">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="b4204-124">Click New.</span></span>
8. <span data-ttu-id="b4204-125">В поле "Тип ссуды" введите имя типа банковской услуги, которая связана с договором о банковских услугах.</span><span class="sxs-lookup"><span data-stu-id="b4204-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="b4204-126">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b4204-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="b4204-127">В поле "Группа ссуды" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="b4204-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="b4204-128">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="b4204-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="b4204-129">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="b4204-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="b4204-130">В поле "Характер ссуды" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="b4204-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="b4204-131">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="b4204-131">Click Save.</span></span>
15. <span data-ttu-id="b4204-132">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b4204-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="b4204-133">Профиль разноски банка</span><span class="sxs-lookup"><span data-stu-id="b4204-133">Bank posting profile</span></span>
1. <span data-ttu-id="b4204-134">Перейдите в раздел "Управление банком и кассовыми операциями" > "Настройка" > "Профиль разноски банковских документов".</span><span class="sxs-lookup"><span data-stu-id="b4204-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="b4204-135">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="b4204-135">Click New.</span></span>
3. <span data-ttu-id="b4204-136">В поле "Номер счета/группы" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="b4204-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b4204-137">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="b4204-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="b4204-138">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="b4204-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b4204-139">В поле "Закрытие счета" выберите счет ГК для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="b4204-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="b4204-140">В поле "Счет расходов" выберите счет для расходных проводок.</span><span class="sxs-lookup"><span data-stu-id="b4204-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="b4204-141">В поле "Счет маржи" выберите счет для проводки маржи.</span><span class="sxs-lookup"><span data-stu-id="b4204-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="b4204-142">В поле "Счет ликвидации" выберите счет ликвидации для проводки гарантийного письма.</span><span class="sxs-lookup"><span data-stu-id="b4204-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="b4204-143">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="b4204-143">Click Save.</span></span>
11. <span data-ttu-id="b4204-144">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b4204-144">Close the page.</span></span>

