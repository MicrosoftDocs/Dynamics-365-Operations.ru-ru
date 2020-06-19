---
title: Регистрация и удаление льгот для работников
description: Эта процедура демонстрирует, как для одного работника можно зарегистрировать одну или несколько льгот, а также как для нескольких работников можно зарегистрировать льготу.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmWorkerEnrollment, HcmBenefitByEligibilityLookup, HcmMassBenefitEnrollment, HcmBenefitLookup, HcmMassBenefitEnrollmentResults, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 36fd724ff27cbb646f3f8a35ca1b30dc86a5afe4
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430793"
---
# <a name="enroll-and-remove-benefits-from-workers"></a><span data-ttu-id="d6dd4-103">Регистрация и удаление льгот для работников</span><span class="sxs-lookup"><span data-stu-id="d6dd4-103">Enroll and remove benefits from workers</span></span>



<span data-ttu-id="d6dd4-104">Эта процедура демонстрирует, как для одного работника можно зарегистрировать одну или несколько льгот, а также как для нескольких работников можно зарегистрировать льготу.</span><span class="sxs-lookup"><span data-stu-id="d6dd4-104">This procedure demonstrates how a single worker can be enrolled in one or more benefits, as well as multiple workers can be enrolled in a benefit.</span></span> <span data-ttu-id="d6dd4-105">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="d6dd4-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="enroll-a-single-worker-in-benefits"></a><span data-ttu-id="d6dd4-106">Регистрация одного работника на льготы</span><span class="sxs-lookup"><span data-stu-id="d6dd4-106">Enroll a single worker in benefits</span></span>
1. <span data-ttu-id="d6dd4-107">Перейдите в раздел "Управление персоналом" > "Работники" > "Сотрудники"</span><span class="sxs-lookup"><span data-stu-id="d6dd4-107">Go to Human resources > Workers > Employees</span></span>
2. <span data-ttu-id="d6dd4-108">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="d6dd4-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d6dd4-109">Щелкните "Льготы".</span><span class="sxs-lookup"><span data-stu-id="d6dd4-109">Click Benefits.</span></span>
4. <span data-ttu-id="d6dd4-110">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="d6dd4-110">Click New.</span></span>
5. <span data-ttu-id="d6dd4-111">В поле "Льгота" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d6dd4-111">In the Benefit field, enter or select a value.</span></span>
6. <span data-ttu-id="d6dd4-112">В поле "Начальная дата покрытия" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="d6dd4-112">In the Coverage start date field, enter a date and time.</span></span>
7. <span data-ttu-id="d6dd4-113">В поле "Конечная дата покрытия" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="d6dd4-113">In the Coverage end date field, enter a date and time.</span></span>
8. <span data-ttu-id="d6dd4-114">Разверните раздел "Бенефициары", если бенефициары должны быть добавлены к льготе.</span><span class="sxs-lookup"><span data-stu-id="d6dd4-114">Expand the Beneficiaries section if beneficiaries need to be added to the benefit.</span></span> <span data-ttu-id="d6dd4-115">Можно также добавить иждивенцев на этой странице, если это применимо к льготе.</span><span class="sxs-lookup"><span data-stu-id="d6dd4-115">You can also add dependents from this page if applicable to the benefit.</span></span>
9. <span data-ttu-id="d6dd4-116">Можно также изменить сведения о регистрации льготы или удалить регистрацию на этой странице.</span><span class="sxs-lookup"><span data-stu-id="d6dd4-116">You can also edit the details of a benefit enrollment or delete an enrollment on this page.</span></span> <span data-ttu-id="d6dd4-117">По завершении внесения изменений в регистрацию льготы закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d6dd4-117">When you have finished making changes to the benefit enrollment, close the page.</span></span>

## <a name="enroll-multiple-workers-in-a-benefit"></a><span data-ttu-id="d6dd4-118">Регистрация нескольких работников для льготы</span><span class="sxs-lookup"><span data-stu-id="d6dd4-118">Enroll multiple workers in a benefit</span></span>
1. <span data-ttu-id="d6dd4-119">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d6dd4-119">Close the page.</span></span>
2. <span data-ttu-id="d6dd4-120">Перейдите в раздел "Управление персоналом" > "Работники" > "Сотрудники"</span><span class="sxs-lookup"><span data-stu-id="d6dd4-120">Go to Human resources > Workers > Employees</span></span>
3. <span data-ttu-id="d6dd4-121">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="d6dd4-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="d6dd4-122">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="d6dd4-122">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d6dd4-123">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="d6dd4-123">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="d6dd4-124">Щелкните "Зарегистрировать для льгот".</span><span class="sxs-lookup"><span data-stu-id="d6dd4-124">Click Enroll in benefits.</span></span>
7. <span data-ttu-id="d6dd4-125">В поле "Льгота" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="d6dd4-125">In the Benefit field, enter or select a value.</span></span>
8. <span data-ttu-id="d6dd4-126">В поле "Начальная дата покрытия" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="d6dd4-126">In the Coverage start date field, enter a date and time.</span></span>
9. <span data-ttu-id="d6dd4-127">В поле "Конечная дата покрытия" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="d6dd4-127">In the Coverage end date field, enter a date and time.</span></span>
10. <span data-ttu-id="d6dd4-128">Щелкните "Зарегистрировать".</span><span class="sxs-lookup"><span data-stu-id="d6dd4-128">Click Enroll.</span></span>
11. <span data-ttu-id="d6dd4-129">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d6dd4-129">Close the page.</span></span>
12. <span data-ttu-id="d6dd4-130">Перейдите в раздел "Управление персоналом" > "Льготы" > "Регистрация" > "Результаты регистрации льготы"</span><span class="sxs-lookup"><span data-stu-id="d6dd4-130">Go to Human Resources > Benefits > Enrollment > Benefit enrollment results</span></span>
13. <span data-ttu-id="d6dd4-131">Найдите запись результатов льготы, которую ищете.</span><span class="sxs-lookup"><span data-stu-id="d6dd4-131">Find the benefit results record that you are looking for.</span></span>
14. <span data-ttu-id="d6dd4-132">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="d6dd4-132">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="d6dd4-133">Эта страница позволяет просматривать сотрудников, которые были зарегистрированы для получения льготы, а также любых других сотрудников, которые не были зарегистрированы.</span><span class="sxs-lookup"><span data-stu-id="d6dd4-133">This page allows you to view which employees have been enrolled in the benefit, as well as any employees who were not enrolled.</span></span>

