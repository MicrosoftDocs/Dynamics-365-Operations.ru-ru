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
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b6da3b9358192997de1d0231e5c9c8eaba92a23b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976275"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="d3526-103">Настройка банковских услуг и профилей разноски для гарантийного письма</span><span class="sxs-lookup"><span data-stu-id="d3526-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d3526-104">Эта задача создает банковскую услугу и профиль разноски, который необходим для обработки гарантийного письма.</span><span class="sxs-lookup"><span data-stu-id="d3526-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="d3526-105">В этой задаче используется демонстрационная компания USMF.</span><span class="sxs-lookup"><span data-stu-id="d3526-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="d3526-106">Параметр главной книги</span><span class="sxs-lookup"><span data-stu-id="d3526-106">General ledger parameter</span></span>
1. <span data-ttu-id="d3526-107">Перейдите в раздел "Управление банком и кассовыми операциями" > "Настройка" > "Параметры управления банком и кассовыми операциями".</span><span class="sxs-lookup"><span data-stu-id="d3526-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="d3526-108">Разверните раздел "Банковский документ".</span><span class="sxs-lookup"><span data-stu-id="d3526-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="d3526-109">Выберите параметр "Разрешить гарантийные письма".</span><span class="sxs-lookup"><span data-stu-id="d3526-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="d3526-110">В поле "Журнал проводок" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="d3526-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="d3526-111">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="d3526-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="d3526-112">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="d3526-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="d3526-113">Откройте вкладку Номерные серии.</span><span class="sxs-lookup"><span data-stu-id="d3526-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="d3526-114">Определение кода номерной серии для номеров гарантийного письма и ссылок на проводки гарантийного письма</span><span class="sxs-lookup"><span data-stu-id="d3526-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="d3526-115">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="d3526-115">Click Save.</span></span>
9. <span data-ttu-id="d3526-116">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d3526-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="d3526-117">Создание банковской услуги</span><span class="sxs-lookup"><span data-stu-id="d3526-117">Create Bank facility</span></span>
1. <span data-ttu-id="d3526-118">Перейдите в раздел "Управление банком и кассовыми операциями" > "Настройка" > "Банковские ссуды".</span><span class="sxs-lookup"><span data-stu-id="d3526-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="d3526-119">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="d3526-119">Click New.</span></span>
3. <span data-ttu-id="d3526-120">В поле "Группа ссуды" введите имя группы банковских услуг для проводки гарантийного письма.</span><span class="sxs-lookup"><span data-stu-id="d3526-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="d3526-121">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d3526-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d3526-122">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="d3526-122">Click Save.</span></span>
6. <span data-ttu-id="d3526-123">Перейдите на вкладку "Типы ссуд".</span><span class="sxs-lookup"><span data-stu-id="d3526-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="d3526-124">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="d3526-124">Click New.</span></span>
8. <span data-ttu-id="d3526-125">В поле "Тип ссуды" введите имя типа банковской услуги, которая связана с договором о банковских услугах.</span><span class="sxs-lookup"><span data-stu-id="d3526-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="d3526-126">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="d3526-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="d3526-127">В поле "Группа ссуды" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="d3526-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="d3526-128">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="d3526-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="d3526-129">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="d3526-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="d3526-130">В поле "Характер ссуды" выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="d3526-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="d3526-131">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="d3526-131">Click Save.</span></span>
15. <span data-ttu-id="d3526-132">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d3526-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="d3526-133">Профиль разноски банка</span><span class="sxs-lookup"><span data-stu-id="d3526-133">Bank posting profile</span></span>
1. <span data-ttu-id="d3526-134">Перейдите в раздел "Управление банком и кассовыми операциями" > "Настройка" > "Профиль разноски банковских документов".</span><span class="sxs-lookup"><span data-stu-id="d3526-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="d3526-135">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="d3526-135">Click New.</span></span>
3. <span data-ttu-id="d3526-136">В поле "Номер счета/группы" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="d3526-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="d3526-137">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="d3526-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d3526-138">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="d3526-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="d3526-139">В поле "Закрытие счета" выберите счет ГК для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="d3526-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="d3526-140">В поле "Счет расходов" выберите счет для расходных проводок.</span><span class="sxs-lookup"><span data-stu-id="d3526-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="d3526-141">В поле "Счет маржи" выберите счет для проводки маржи.</span><span class="sxs-lookup"><span data-stu-id="d3526-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="d3526-142">В поле "Счет ликвидации" выберите счет ликвидации для проводки гарантийного письма.</span><span class="sxs-lookup"><span data-stu-id="d3526-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="d3526-143">Нажмите кнопку Сохранить.</span><span class="sxs-lookup"><span data-stu-id="d3526-143">Click Save.</span></span>
11. <span data-ttu-id="d3526-144">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d3526-144">Close the page.</span></span>

