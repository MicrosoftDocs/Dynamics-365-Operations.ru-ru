--- 
title: "Включение процесса обработки зарплаты по посещаемости и времени присутствия"
description: "Следующая процедура используется для включения обработки зарплаты по времени присутствия и посещаемости."
author: johanhoffmann
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 22ce633f65847f10fbe507b71bfc2bb33f595501
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="bb212-103">Включение процесса обработки зарплаты по посещаемости и времени присутствия</span><span class="sxs-lookup"><span data-stu-id="bb212-103">Enable the payroll process for time and attendance</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bb212-104">Следующая процедура используется для включения обработки зарплаты по времени присутствия и посещаемости.</span><span class="sxs-lookup"><span data-stu-id="bb212-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="bb212-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="bb212-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="bb212-106">Создание вида оплаты со связанной ставкой оплаты</span><span class="sxs-lookup"><span data-stu-id="bb212-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="bb212-107">"Посещаемость и время присутствия" > "Настройка" > "Заработная плата" > "Виды оплаты"</span><span class="sxs-lookup"><span data-stu-id="bb212-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="bb212-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="bb212-108">Click New.</span></span>
3. <span data-ttu-id="bb212-109">В поле "Вид оплаты" введите значение.</span><span class="sxs-lookup"><span data-stu-id="bb212-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="bb212-110">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="bb212-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="bb212-111">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="bb212-111">Click Save.</span></span>
6. <span data-ttu-id="bb212-112">Щелкните "Ставки".</span><span class="sxs-lookup"><span data-stu-id="bb212-112">Click Rates.</span></span>
    * <span data-ttu-id="bb212-113">Ставки для типов оплаты настраиваются для определенных интервалов времени и для отдельных работников могут быть назначены индивидуальные ставки.</span><span class="sxs-lookup"><span data-stu-id="bb212-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="bb212-114">Не всегда требуется создать ставки для типов оплаты по времени и посещаемости.</span><span class="sxs-lookup"><span data-stu-id="bb212-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="bb212-115">Эта информация может уже существовать в системе зарплаты, которая используется для генерирования зарплат.</span><span class="sxs-lookup"><span data-stu-id="bb212-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="bb212-116">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="bb212-116">Click New.</span></span>
8. <span data-ttu-id="bb212-117">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="bb212-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="bb212-118">В поле "Ставка" введите число.</span><span class="sxs-lookup"><span data-stu-id="bb212-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="bb212-119">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="bb212-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="bb212-120">Создание соглашения по зарплате</span><span class="sxs-lookup"><span data-stu-id="bb212-120">Create a pay agreement</span></span>
1. <span data-ttu-id="bb212-121">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bb212-121">Close the page.</span></span>
2. <span data-ttu-id="bb212-122">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bb212-122">Close the page.</span></span>
3. <span data-ttu-id="bb212-123">Перейдите в раздел "Соглашения по оплате".</span><span class="sxs-lookup"><span data-stu-id="bb212-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="bb212-124">"Посещаемость и время присутствия" > "Настройка" > "Соглашения по оплате"</span><span class="sxs-lookup"><span data-stu-id="bb212-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="bb212-125">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="bb212-125">Click New.</span></span>
5. <span data-ttu-id="bb212-126">В поле "Соглашение по оплате" введите значение.</span><span class="sxs-lookup"><span data-stu-id="bb212-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="bb212-127">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="bb212-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="bb212-128">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="bb212-128">Click Save.</span></span>
8. <span data-ttu-id="bb212-129">Щелкните "Строки соглашения".</span><span class="sxs-lookup"><span data-stu-id="bb212-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="bb212-130">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="bb212-130">Click New.</span></span>
10. <span data-ttu-id="bb212-131">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="bb212-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="bb212-132">В поле "Тип профиля" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bb212-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="bb212-133">В поле "Вид оплаты" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bb212-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="bb212-134">Настройка соглашения по оплате по времени присутствия и регистрации работника</span><span class="sxs-lookup"><span data-stu-id="bb212-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="bb212-135">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bb212-135">Close the page.</span></span>
2. <span data-ttu-id="bb212-136">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="bb212-136">Close the page.</span></span>
3. <span data-ttu-id="bb212-137">Перейдите в раздел "Регистрация времени - работники".</span><span class="sxs-lookup"><span data-stu-id="bb212-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="bb212-138">"Посещаемость и время присутствия" > "Настройка" > "Регистрация времени — работники"</span><span class="sxs-lookup"><span data-stu-id="bb212-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="bb212-139">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="bb212-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="bb212-140">Перейдите на вкладку "Занятость".</span><span class="sxs-lookup"><span data-stu-id="bb212-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="bb212-141">Разверните раздел "Регистрация времени".</span><span class="sxs-lookup"><span data-stu-id="bb212-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="bb212-142">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="bb212-142">Click Edit.</span></span>
8. <span data-ttu-id="bb212-143">В поле "Соглашение по оплате" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="bb212-143">In the Pay agreement field, enter or select a value.</span></span>


