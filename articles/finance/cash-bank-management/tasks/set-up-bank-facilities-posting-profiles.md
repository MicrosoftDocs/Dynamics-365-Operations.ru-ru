---
title: Настройка банковских услуг и профилей разноски для гарантийного письма
description: Эта задача создает банковскую услугу и профиль разноски, который необходим для обработки гарантийного письма.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ff5402b11cd2ccdfde2881268d9cd936947cd77e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4447268"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="2898d-103">Настройка банковских услуг и профилей разноски для гарантийного письма</span><span class="sxs-lookup"><span data-stu-id="2898d-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2898d-104">Эта задача создает банковскую услугу и профиль разноски, который необходим для обработки гарантийного письма.</span><span class="sxs-lookup"><span data-stu-id="2898d-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="2898d-105">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="2898d-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="2898d-106">Параметр главной книги</span><span class="sxs-lookup"><span data-stu-id="2898d-106">General ledger parameter</span></span>
1. <span data-ttu-id="2898d-107">Перейдите в раздел "Управление банком и кассовыми операциями" > "Настройка" > "Параметры управления банком и кассовыми операциями".</span><span class="sxs-lookup"><span data-stu-id="2898d-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="2898d-108">Разверните раздел "Банковский документ".</span><span class="sxs-lookup"><span data-stu-id="2898d-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="2898d-109">Выберите параметр "Разрешить гарантийные письма".</span><span class="sxs-lookup"><span data-stu-id="2898d-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="2898d-110">В поле "Журнал проводок" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="2898d-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="2898d-111">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="2898d-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="2898d-112">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="2898d-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="2898d-113">Откройте вкладку Номерные серии.</span><span class="sxs-lookup"><span data-stu-id="2898d-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="2898d-114">Определение кода номерной серии для номеров гарантийного письма и ссылок на проводки гарантийного письма</span><span class="sxs-lookup"><span data-stu-id="2898d-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="2898d-115">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="2898d-115">Click Save.</span></span>
9. <span data-ttu-id="2898d-116">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2898d-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="2898d-117">Создание банковской услуги</span><span class="sxs-lookup"><span data-stu-id="2898d-117">Create Bank facility</span></span>
1. <span data-ttu-id="2898d-118">Перейдите в раздел "Управление банком и кассовыми операциями" > "Настройка" > "Банковские ссуды".</span><span class="sxs-lookup"><span data-stu-id="2898d-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="2898d-119">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="2898d-119">Click New.</span></span>
3. <span data-ttu-id="2898d-120">В поле "Группа ссуды" введите имя группы банковских услуг для проводки гарантийного письма.</span><span class="sxs-lookup"><span data-stu-id="2898d-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="2898d-121">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2898d-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2898d-122">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="2898d-122">Click Save.</span></span>
6. <span data-ttu-id="2898d-123">Перейдите на вкладку "Типы ссуд".</span><span class="sxs-lookup"><span data-stu-id="2898d-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="2898d-124">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="2898d-124">Click New.</span></span>
8. <span data-ttu-id="2898d-125">В поле "Тип ссуды" введите имя типа банковской услуги, которая связана с договором о банковских услугах.</span><span class="sxs-lookup"><span data-stu-id="2898d-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="2898d-126">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="2898d-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="2898d-127">В поле "Группа ссуды" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="2898d-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="2898d-128">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="2898d-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="2898d-129">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="2898d-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="2898d-130">В поле "Характер ссуды" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="2898d-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="2898d-131">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="2898d-131">Click Save.</span></span>
15. <span data-ttu-id="2898d-132">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2898d-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="2898d-133">Профиль разноски банка</span><span class="sxs-lookup"><span data-stu-id="2898d-133">Bank posting profile</span></span>
1. <span data-ttu-id="2898d-134">Перейдите в раздел "Управление банком и кассовыми операциями" > "Настройка" > "Профиль разноски банковских документов".</span><span class="sxs-lookup"><span data-stu-id="2898d-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="2898d-135">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="2898d-135">Click New.</span></span>
3. <span data-ttu-id="2898d-136">В поле "Номер счета/группы" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="2898d-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="2898d-137">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="2898d-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="2898d-138">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="2898d-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="2898d-139">В поле "Закрытие счета" выберите счет ГК для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="2898d-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="2898d-140">В поле "Счет расходов" выберите счет для расходных проводок.</span><span class="sxs-lookup"><span data-stu-id="2898d-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="2898d-141">В поле "Счет маржи" выберите счет для проводки маржи.</span><span class="sxs-lookup"><span data-stu-id="2898d-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="2898d-142">В поле "Счет ликвидации" выберите счет ликвидации для проводки гарантийного письма.</span><span class="sxs-lookup"><span data-stu-id="2898d-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="2898d-143">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="2898d-143">Click Save.</span></span>
11. <span data-ttu-id="2898d-144">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="2898d-144">Close the page.</span></span>

