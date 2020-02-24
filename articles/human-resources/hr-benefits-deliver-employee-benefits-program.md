---
title: Реализация программы льгот сотрудника
description: В этой статье показано, как создать элементы льгот, которые будут использоваться при создании новой льготы.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmBenefitElementSetup, HcmBenefit, HcmBenefitNewBenefit, HcmBenefitPlanLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: b8631e4f8cb2947ec7e09de86a7ceb075a83a453
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010402"
---
# <a name="deliver-employee-benefits-program"></a><span data-ttu-id="080a5-103">Реализация программы льгот сотрудника</span><span class="sxs-lookup"><span data-stu-id="080a5-103">Deliver employee benefits program</span></span>

<span data-ttu-id="080a5-104">В этой статье показано, как создать элементы льгот, которые будут использоваться при создании новой льготы.</span><span class="sxs-lookup"><span data-stu-id="080a5-104">This article shows you how to create benefit elements which will be used when creating a new benefit.</span></span> <span data-ttu-id="080a5-105">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="080a5-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="080a5-106">Эта задача предназначена для менеджера по компенсациям и льготам.</span><span class="sxs-lookup"><span data-stu-id="080a5-106">This task is intended for a Compensation and Benefits manager.</span></span>


## <a name="create-benefit-elements"></a><span data-ttu-id="080a5-107">Создание элементов льготы</span><span class="sxs-lookup"><span data-stu-id="080a5-107">Create benefit elements</span></span>
1. <span data-ttu-id="080a5-108">Эта задача начинается со страницы списка "Льготы ".</span><span class="sxs-lookup"><span data-stu-id="080a5-108">This task starts from the Benefits list page.</span></span> <span data-ttu-id="080a5-109">Запустите задачу, открыв эту страницу или выполнив поиск страницы списка "Льготы".</span><span class="sxs-lookup"><span data-stu-id="080a5-109">Start the task by opening that page or searching the Benefits list page.</span></span>
2. <span data-ttu-id="080a5-110">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="080a5-110">Click New.</span></span>
3. <span data-ttu-id="080a5-111">В поле "Тип" введите имя создаваемого типа льготы.</span><span class="sxs-lookup"><span data-stu-id="080a5-111">In the Type field, Enter the name of the type of benefit you are creating..</span></span>
4. <span data-ttu-id="080a5-112">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="080a5-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="080a5-113">В поле "Одновременная регистрация" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="080a5-113">In the Concurrent enrollment field, select an option.</span></span>
    * <span data-ttu-id="080a5-114">Чтобы ограничить возможность сотрудников регистрироваться в нескольких медицинских планах, установите флажок "Одна регистрация для каждого типа".</span><span class="sxs-lookup"><span data-stu-id="080a5-114">To restrict employees' ability to enroll in multiple medical plans, select One enrollment per type.</span></span>  
6. <span data-ttu-id="080a5-115">В поле "Категория по зарплате" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="080a5-115">In the Payroll category field, select an option.</span></span>
7. <span data-ttu-id="080a5-116">Перейдите на вкладку "Планы".</span><span class="sxs-lookup"><span data-stu-id="080a5-116">Click the Plans tab.</span></span>
8. <span data-ttu-id="080a5-117">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="080a5-117">Click New.</span></span>
9. <span data-ttu-id="080a5-118">В поле "План" введите значение.</span><span class="sxs-lookup"><span data-stu-id="080a5-118">In the Plan field, type a value.</span></span>
10. <span data-ttu-id="080a5-119">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="080a5-119">In the Description field, type a value.</span></span>
11. <span data-ttu-id="080a5-120">В поле "Тип" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="080a5-120">In the Type field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="080a5-121">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="080a5-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="080a5-122">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="080a5-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="080a5-123">В поле "Влияние на зарплату" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="080a5-123">In the Payroll impact field, select an option.</span></span>
15. <span data-ttu-id="080a5-124">Перейдите на вкладку "Параметры".</span><span class="sxs-lookup"><span data-stu-id="080a5-124">Click the Options tab.</span></span>
16. <span data-ttu-id="080a5-125">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="080a5-125">Click New.</span></span>
17. <span data-ttu-id="080a5-126">В поле "Параметр" введите значение.</span><span class="sxs-lookup"><span data-stu-id="080a5-126">In the Option field, type a value.</span></span>
18. <span data-ttu-id="080a5-127">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="080a5-127">In the Description field, type a value.</span></span>

## <a name="create-a-benefit"></a><span data-ttu-id="080a5-128">Создание льготы</span><span class="sxs-lookup"><span data-stu-id="080a5-128">Create a benefit</span></span>
1. <span data-ttu-id="080a5-129">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="080a5-129">Close the page.</span></span>
2. <span data-ttu-id="080a5-130">Перейдите в раздел "Управление персоналом" > "Льготы" > "Льготы".</span><span class="sxs-lookup"><span data-stu-id="080a5-130">Go to Human resources > Benefits > Benefits.</span></span>
3. <span data-ttu-id="080a5-131">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="080a5-131">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="080a5-132">В поле "План" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="080a5-132">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="080a5-133">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="080a5-133">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="080a5-134">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="080a5-134">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="080a5-135">В поле "Параметр" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="080a5-135">In the Option field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="080a5-136">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="080a5-136">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="080a5-137">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="080a5-137">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="080a5-138">В поле "Действует" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="080a5-138">In the Effective field, enter a date and time.</span></span>
11. <span data-ttu-id="080a5-139">Щелкните "Создать льготу".</span><span class="sxs-lookup"><span data-stu-id="080a5-139">Click Create benefit.</span></span>
12. <span data-ttu-id="080a5-140">Переключите развертывание раздела "Сведения по зарплате".</span><span class="sxs-lookup"><span data-stu-id="080a5-140">Toggle the expansion of the Payroll details section.</span></span>
13. <span data-ttu-id="080a5-141">В поле "Частота" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="080a5-141">In the Frequency field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="080a5-142">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="080a5-142">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="080a5-143">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="080a5-143">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="080a5-144">В поле "Основание" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="080a5-144">In the Basis field, select an option.</span></span>
17. <span data-ttu-id="080a5-145">В поле "Сумма или ставка" введите число.</span><span class="sxs-lookup"><span data-stu-id="080a5-145">In the Amount or rate field, enter a number.</span></span>

