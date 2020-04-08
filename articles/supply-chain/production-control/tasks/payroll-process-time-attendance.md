---
title: Включение процесса обработки зарплаты по посещаемости и времени присутствия
description: Следующая процедура используется для включения обработки зарплаты по времени присутствия и посещаемости.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2df4695b796b4e96e01fe5dac538b344cb76b910
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146729"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="f118a-103">Включение процесса обработки зарплаты по посещаемости и времени присутствия</span><span class="sxs-lookup"><span data-stu-id="f118a-103">Enable the payroll process for time and attendance</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f118a-104">Следующая процедура используется для включения обработки зарплаты по времени присутствия и посещаемости.</span><span class="sxs-lookup"><span data-stu-id="f118a-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="f118a-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="f118a-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="f118a-106">Создание вида оплаты со связанной ставкой оплаты</span><span class="sxs-lookup"><span data-stu-id="f118a-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="f118a-107">"Посещаемость и время присутствия" > "Настройка" > "Заработная плата" > "Виды оплаты"</span><span class="sxs-lookup"><span data-stu-id="f118a-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="f118a-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="f118a-108">Click New.</span></span>
3. <span data-ttu-id="f118a-109">В поле "Вид оплаты" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f118a-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="f118a-110">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f118a-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f118a-111">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="f118a-111">Click Save.</span></span>
6. <span data-ttu-id="f118a-112">Щелкните "Ставки".</span><span class="sxs-lookup"><span data-stu-id="f118a-112">Click Rates.</span></span>
    * <span data-ttu-id="f118a-113">Ставки для типов оплаты настраиваются для определенных интервалов времени и для отдельных работников могут быть назначены индивидуальные ставки.</span><span class="sxs-lookup"><span data-stu-id="f118a-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="f118a-114">Не всегда требуется создать ставки для типов оплаты по времени и посещаемости.</span><span class="sxs-lookup"><span data-stu-id="f118a-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="f118a-115">Эта информация может уже существовать в системе зарплаты, которая используется для генерирования зарплат.</span><span class="sxs-lookup"><span data-stu-id="f118a-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="f118a-116">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="f118a-116">Click New.</span></span>
8. <span data-ttu-id="f118a-117">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="f118a-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="f118a-118">В поле "Ставка" введите число.</span><span class="sxs-lookup"><span data-stu-id="f118a-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="f118a-119">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="f118a-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="f118a-120">Создание соглашения по зарплате</span><span class="sxs-lookup"><span data-stu-id="f118a-120">Create a pay agreement</span></span>
1. <span data-ttu-id="f118a-121">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f118a-121">Close the page.</span></span>
2. <span data-ttu-id="f118a-122">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f118a-122">Close the page.</span></span>
3. <span data-ttu-id="f118a-123">Перейдите в раздел "Соглашения по оплате".</span><span class="sxs-lookup"><span data-stu-id="f118a-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="f118a-124">"Посещаемость и время присутствия" > "Настройка" > "Соглашения по оплате"</span><span class="sxs-lookup"><span data-stu-id="f118a-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="f118a-125">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="f118a-125">Click New.</span></span>
5. <span data-ttu-id="f118a-126">В поле "Соглашение по оплате" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f118a-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="f118a-127">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="f118a-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="f118a-128">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="f118a-128">Click Save.</span></span>
8. <span data-ttu-id="f118a-129">Щелкните "Строки соглашения".</span><span class="sxs-lookup"><span data-stu-id="f118a-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="f118a-130">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="f118a-130">Click New.</span></span>
10. <span data-ttu-id="f118a-131">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="f118a-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="f118a-132">В поле "Тип профиля" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="f118a-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="f118a-133">В поле "Вид оплаты" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="f118a-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="f118a-134">Настройка соглашения по оплате по времени присутствия и регистрации работника</span><span class="sxs-lookup"><span data-stu-id="f118a-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="f118a-135">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f118a-135">Close the page.</span></span>
2. <span data-ttu-id="f118a-136">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="f118a-136">Close the page.</span></span>
3. <span data-ttu-id="f118a-137">Перейдите в раздел "Регистрация времени - работники".</span><span class="sxs-lookup"><span data-stu-id="f118a-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="f118a-138">"Посещаемость и время присутствия" > "Настройка" > "Регистрация времени — работники"</span><span class="sxs-lookup"><span data-stu-id="f118a-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="f118a-139">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="f118a-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="f118a-140">Перейдите на вкладку "Занятость".</span><span class="sxs-lookup"><span data-stu-id="f118a-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="f118a-141">Разверните раздел "Регистрация времени".</span><span class="sxs-lookup"><span data-stu-id="f118a-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="f118a-142">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="f118a-142">Click Edit.</span></span>
8. <span data-ttu-id="f118a-143">В поле "Соглашение по оплате" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="f118a-143">In the Pay agreement field, enter or select a value.</span></span>

