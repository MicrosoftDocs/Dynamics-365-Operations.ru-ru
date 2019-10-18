---
title: Реализация программы льгот сотрудника
description: В этой задаче показано, как создать элементы льгот, которые будут использоваться при создании новой льготы.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmBenefitElementSetup, HcmBenefit, HcmBenefitNewBenefit, HcmBenefitPlanLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0285c2be49edde701d6c6cf83ccdeac994434ab
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190542"
---
# <a name="deliver-employee-benefits-program"></a><span data-ttu-id="70230-103">Реализация программы льгот сотрудника</span><span class="sxs-lookup"><span data-stu-id="70230-103">Deliver employee benefits program</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="70230-104">В этой задаче показано, как создать элементы льгот, которые будут использоваться при создании новой льготы.</span><span class="sxs-lookup"><span data-stu-id="70230-104">This task will show you how to create benefit elements which will be used when creating a new benefit.</span></span> <span data-ttu-id="70230-105">В качестве компании с демонстрационными данными для создания этой задачи используется USMF.</span><span class="sxs-lookup"><span data-stu-id="70230-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="70230-106">Эта задача предназначена для менеджера по компенсациям и льготам.</span><span class="sxs-lookup"><span data-stu-id="70230-106">This task is intended for a Compensation and Benefits manager.</span></span>


## <a name="create-benefit-elements"></a><span data-ttu-id="70230-107">Создание элементов льготы</span><span class="sxs-lookup"><span data-stu-id="70230-107">Create benefit elements</span></span>
1. <span data-ttu-id="70230-108">Эта задача начинается со страницы списка "Льготы ".</span><span class="sxs-lookup"><span data-stu-id="70230-108">This task starts from the Benefits list page.</span></span> <span data-ttu-id="70230-109">Запустите задачу, открыв эту страницу или выполнив поиск страницы списка "Льготы".</span><span class="sxs-lookup"><span data-stu-id="70230-109">Start the task by opening that page or searching the Benefits list page.</span></span>
2. <span data-ttu-id="70230-110">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="70230-110">Click New.</span></span>
3. <span data-ttu-id="70230-111">В поле "Тип" введите имя создаваемого типа льготы.</span><span class="sxs-lookup"><span data-stu-id="70230-111">In the Type field, Enter the name of the type of benefit you are creating..</span></span>
4. <span data-ttu-id="70230-112">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="70230-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="70230-113">В поле "Одновременная регистрация" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="70230-113">In the Concurrent enrollment field, select an option.</span></span>
    * <span data-ttu-id="70230-114">Чтобы ограничить возможность сотрудников регистрироваться в нескольких медицинских планах, установите флажок "Одна регистрация для каждого типа".</span><span class="sxs-lookup"><span data-stu-id="70230-114">To restrict employees' ability to enroll in multiple medical plans, select One enrollment per type.</span></span>  
6. <span data-ttu-id="70230-115">В поле "Категория по зарплате" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="70230-115">In the Payroll category field, select an option.</span></span>
7. <span data-ttu-id="70230-116">Перейдите на вкладку "Планы".</span><span class="sxs-lookup"><span data-stu-id="70230-116">Click the Plans tab.</span></span>
8. <span data-ttu-id="70230-117">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="70230-117">Click New.</span></span>
9. <span data-ttu-id="70230-118">В поле "План" введите значение.</span><span class="sxs-lookup"><span data-stu-id="70230-118">In the Plan field, type a value.</span></span>
10. <span data-ttu-id="70230-119">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="70230-119">In the Description field, type a value.</span></span>
11. <span data-ttu-id="70230-120">В поле "Тип" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="70230-120">In the Type field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="70230-121">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="70230-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="70230-122">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="70230-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="70230-123">В поле "Влияние на зарплату" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="70230-123">In the Payroll impact field, select an option.</span></span>
15. <span data-ttu-id="70230-124">Перейдите на вкладку "Параметры".</span><span class="sxs-lookup"><span data-stu-id="70230-124">Click the Options tab.</span></span>
16. <span data-ttu-id="70230-125">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="70230-125">Click New.</span></span>
17. <span data-ttu-id="70230-126">В поле "Параметр" введите значение.</span><span class="sxs-lookup"><span data-stu-id="70230-126">In the Option field, type a value.</span></span>
18. <span data-ttu-id="70230-127">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="70230-127">In the Description field, type a value.</span></span>

## <a name="create-a-benefit"></a><span data-ttu-id="70230-128">Создание льготы</span><span class="sxs-lookup"><span data-stu-id="70230-128">Create a benefit</span></span>
1. <span data-ttu-id="70230-129">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="70230-129">Close the page.</span></span>
2. <span data-ttu-id="70230-130">Перейдите в раздел "Управление персоналом" > "Льготы" > "Льготы".</span><span class="sxs-lookup"><span data-stu-id="70230-130">Go to Human resources > Benefits > Benefits.</span></span>
3. <span data-ttu-id="70230-131">Щелкните "Создать", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="70230-131">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="70230-132">В поле "План" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="70230-132">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="70230-133">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="70230-133">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="70230-134">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="70230-134">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="70230-135">В поле "Параметр" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="70230-135">In the Option field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="70230-136">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="70230-136">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="70230-137">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="70230-137">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="70230-138">В поле "Действует" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="70230-138">In the Effective field, enter a date and time.</span></span>
11. <span data-ttu-id="70230-139">Щелкните "Создать льготу".</span><span class="sxs-lookup"><span data-stu-id="70230-139">Click Create benefit.</span></span>
12. <span data-ttu-id="70230-140">Переключите развертывание раздела "Сведения по зарплате".</span><span class="sxs-lookup"><span data-stu-id="70230-140">Toggle the expansion of the Payroll details section.</span></span>
13. <span data-ttu-id="70230-141">В поле "Частота" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="70230-141">In the Frequency field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="70230-142">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="70230-142">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="70230-143">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="70230-143">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="70230-144">В поле "Основание" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="70230-144">In the Basis field, select an option.</span></span>
17. <span data-ttu-id="70230-145">В поле "Сумма или ставка" введите число.</span><span class="sxs-lookup"><span data-stu-id="70230-145">In the Amount or rate field, enter a number.</span></span>

