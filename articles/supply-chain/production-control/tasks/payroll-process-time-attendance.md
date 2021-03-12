---
title: Включение процесса обработки зарплаты по посещаемости и времени присутствия
description: Следующая процедура используется для включения обработки зарплаты по времени присутствия и посещаемости.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c855f388e8afbd12559cd633cfcdebc7740bce6a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977796"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="168db-103">Включение процесса обработки зарплаты по посещаемости и времени присутствия</span><span class="sxs-lookup"><span data-stu-id="168db-103">Enable the payroll process for time and attendance</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="168db-104">Следующая процедура используется для включения обработки зарплаты по времени присутствия и посещаемости.</span><span class="sxs-lookup"><span data-stu-id="168db-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="168db-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="168db-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="168db-106">Создание вида оплаты со связанной ставкой оплаты</span><span class="sxs-lookup"><span data-stu-id="168db-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="168db-107">"Посещаемость и время присутствия" > "Настройка" > "Заработная плата" > "Виды оплаты"</span><span class="sxs-lookup"><span data-stu-id="168db-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="168db-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="168db-108">Click New.</span></span>
3. <span data-ttu-id="168db-109">В поле "Вид оплаты" введите значение.</span><span class="sxs-lookup"><span data-stu-id="168db-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="168db-110">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="168db-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="168db-111">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="168db-111">Click Save.</span></span>
6. <span data-ttu-id="168db-112">Щелкните "Ставки".</span><span class="sxs-lookup"><span data-stu-id="168db-112">Click Rates.</span></span>
    * <span data-ttu-id="168db-113">Ставки для типов оплаты настраиваются для определенных интервалов времени и для отдельных работников могут быть назначены индивидуальные ставки.</span><span class="sxs-lookup"><span data-stu-id="168db-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="168db-114">Не всегда требуется создать ставки для типов оплаты по времени и посещаемости.</span><span class="sxs-lookup"><span data-stu-id="168db-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="168db-115">Эта информация может уже существовать в системе зарплаты, которая используется для генерирования зарплат.</span><span class="sxs-lookup"><span data-stu-id="168db-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="168db-116">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="168db-116">Click New.</span></span>
8. <span data-ttu-id="168db-117">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="168db-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="168db-118">В поле "Ставка" введите число.</span><span class="sxs-lookup"><span data-stu-id="168db-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="168db-119">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="168db-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="168db-120">Создание соглашения по зарплате</span><span class="sxs-lookup"><span data-stu-id="168db-120">Create a pay agreement</span></span>
1. <span data-ttu-id="168db-121">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="168db-121">Close the page.</span></span>
2. <span data-ttu-id="168db-122">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="168db-122">Close the page.</span></span>
3. <span data-ttu-id="168db-123">Перейдите в раздел "Соглашения по оплате".</span><span class="sxs-lookup"><span data-stu-id="168db-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="168db-124">"Посещаемость и время присутствия" > "Настройка" > "Соглашения по оплате"</span><span class="sxs-lookup"><span data-stu-id="168db-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="168db-125">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="168db-125">Click New.</span></span>
5. <span data-ttu-id="168db-126">В поле "Соглашение по оплате" введите значение.</span><span class="sxs-lookup"><span data-stu-id="168db-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="168db-127">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="168db-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="168db-128">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="168db-128">Click Save.</span></span>
8. <span data-ttu-id="168db-129">Щелкните "Строки соглашения".</span><span class="sxs-lookup"><span data-stu-id="168db-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="168db-130">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="168db-130">Click New.</span></span>
10. <span data-ttu-id="168db-131">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="168db-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="168db-132">В поле "Тип профиля" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="168db-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="168db-133">В поле "Вид оплаты" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="168db-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="168db-134">Настройка соглашения по оплате по времени присутствия и регистрации работника</span><span class="sxs-lookup"><span data-stu-id="168db-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="168db-135">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="168db-135">Close the page.</span></span>
2. <span data-ttu-id="168db-136">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="168db-136">Close the page.</span></span>
3. <span data-ttu-id="168db-137">Перейдите в раздел "Регистрация времени - работники".</span><span class="sxs-lookup"><span data-stu-id="168db-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="168db-138">"Посещаемость и время присутствия" > "Настройка" > "Регистрация времени — работники"</span><span class="sxs-lookup"><span data-stu-id="168db-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="168db-139">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="168db-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="168db-140">Перейдите на вкладку "Занятость".</span><span class="sxs-lookup"><span data-stu-id="168db-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="168db-141">Разверните раздел "Регистрация времени".</span><span class="sxs-lookup"><span data-stu-id="168db-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="168db-142">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="168db-142">Click Edit.</span></span>
8. <span data-ttu-id="168db-143">В поле "Соглашение по оплате" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="168db-143">In the Pay agreement field, enter or select a value.</span></span>

