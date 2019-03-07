---
title: Реализация программы льгот сотрудника
description: В этой задаче показано, как создать элементы льгот, которые будут использоваться при создании новой льготы.
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmBenefitElementSetup, HcmBenefit, HcmBenefitNewBenefit, HcmBenefitPlanLookup
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5bf886086fe7ebe20e329c3b69697c390e1db998
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "329605"
---
# <a name="deliver-employee-benefits-program"></a><span data-ttu-id="dc969-103">Реализация программы льгот сотрудника</span><span class="sxs-lookup"><span data-stu-id="dc969-103">Deliver employee benefits program</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dc969-104">В этой задаче показано, как создать элементы льгот, которые будут использоваться при создании новой льготы.</span><span class="sxs-lookup"><span data-stu-id="dc969-104">This task will show you how to create benefit elements which will be used when creating a new benefit.</span></span> <span data-ttu-id="dc969-105">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="dc969-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="dc969-106">Эта задача предназначена для менеджера по компенсациям и льготам.</span><span class="sxs-lookup"><span data-stu-id="dc969-106">This task is intended for a Compensation and Benefits manager.</span></span>


## <a name="create-benefit-elements"></a><span data-ttu-id="dc969-107">Создание элементов льготы</span><span class="sxs-lookup"><span data-stu-id="dc969-107">Create benefit elements</span></span>
1. <span data-ttu-id="dc969-108">Эта задача начинается со страницы списка "Льготы ".</span><span class="sxs-lookup"><span data-stu-id="dc969-108">This task starts from the Benefits list page.</span></span> <span data-ttu-id="dc969-109">Запустите задачу, открыв эту страницу или выполнив поиск страницы списка "Льготы".</span><span class="sxs-lookup"><span data-stu-id="dc969-109">Start the task by opening that page or searching the Benefits list page.</span></span>
2. <span data-ttu-id="dc969-110">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="dc969-110">Click New.</span></span>
3. <span data-ttu-id="dc969-111">В поле "Тип" введите имя создаваемого типа льготы.</span><span class="sxs-lookup"><span data-stu-id="dc969-111">In the Type field, Enter the name of the type of benefit you are creating..</span></span>
4. <span data-ttu-id="dc969-112">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="dc969-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="dc969-113">В поле "Одновременная регистрация" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="dc969-113">In the Concurrent enrollment field, select an option.</span></span>
    * <span data-ttu-id="dc969-114">Чтобы ограничить возможность сотрудников регистрироваться в нескольких медицинских планах, установите флажок "Одна регистрация для каждого типа".</span><span class="sxs-lookup"><span data-stu-id="dc969-114">To restrict employees' ability to enroll in multiple medical plans, select One enrollment per type.</span></span>  
6. <span data-ttu-id="dc969-115">В поле "Категория по зарплате" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="dc969-115">In the Payroll category field, select an option.</span></span>
7. <span data-ttu-id="dc969-116">Перейдите на вкладку "Планы".</span><span class="sxs-lookup"><span data-stu-id="dc969-116">Click the Plans tab.</span></span>
8. <span data-ttu-id="dc969-117">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="dc969-117">Click New.</span></span>
9. <span data-ttu-id="dc969-118">В поле "План" введите значение.</span><span class="sxs-lookup"><span data-stu-id="dc969-118">In the Plan field, type a value.</span></span>
10. <span data-ttu-id="dc969-119">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="dc969-119">In the Description field, type a value.</span></span>
11. <span data-ttu-id="dc969-120">В поле "Тип" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="dc969-120">In the Type field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="dc969-121">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="dc969-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="dc969-122">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="dc969-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="dc969-123">В поле "Влияние на зарплату" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="dc969-123">In the Payroll impact field, select an option.</span></span>
15. <span data-ttu-id="dc969-124">Перейдите на вкладку "Параметры".</span><span class="sxs-lookup"><span data-stu-id="dc969-124">Click the Options tab.</span></span>
16. <span data-ttu-id="dc969-125">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="dc969-125">Click New.</span></span>
17. <span data-ttu-id="dc969-126">В поле "Параметр" введите значение.</span><span class="sxs-lookup"><span data-stu-id="dc969-126">In the Option field, type a value.</span></span>
18. <span data-ttu-id="dc969-127">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="dc969-127">In the Description field, type a value.</span></span>

## <a name="create-a-benefit"></a><span data-ttu-id="dc969-128">Создание льготы</span><span class="sxs-lookup"><span data-stu-id="dc969-128">Create a benefit</span></span>
1. <span data-ttu-id="dc969-129">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="dc969-129">Close the page.</span></span>
2. <span data-ttu-id="dc969-130">Перейдите в раздел "Управление персоналом" > "Льготы" > "Льготы".</span><span class="sxs-lookup"><span data-stu-id="dc969-130">Go to Human resources > Benefits > Benefits.</span></span>
3. <span data-ttu-id="dc969-131">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="dc969-131">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="dc969-132">В поле "План" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="dc969-132">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="dc969-133">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="dc969-133">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="dc969-134">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="dc969-134">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="dc969-135">В поле "Параметр" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="dc969-135">In the Option field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="dc969-136">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="dc969-136">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="dc969-137">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="dc969-137">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="dc969-138">В поле "Действует" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="dc969-138">In the Effective field, enter a date and time.</span></span>
11. <span data-ttu-id="dc969-139">Щелкните "Создать льготу".</span><span class="sxs-lookup"><span data-stu-id="dc969-139">Click Create benefit.</span></span>
12. <span data-ttu-id="dc969-140">Переключите развертывание раздела "Сведения по зарплате".</span><span class="sxs-lookup"><span data-stu-id="dc969-140">Toggle the expansion of the Payroll details section.</span></span>
13. <span data-ttu-id="dc969-141">В поле "Частота" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="dc969-141">In the Frequency field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="dc969-142">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="dc969-142">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="dc969-143">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="dc969-143">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="dc969-144">В поле "Основание" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="dc969-144">In the Basis field, select an option.</span></span>
17. <span data-ttu-id="dc969-145">В поле "Сумма или ставка" введите число.</span><span class="sxs-lookup"><span data-stu-id="dc969-145">In the Amount or rate field, enter a number.</span></span>

