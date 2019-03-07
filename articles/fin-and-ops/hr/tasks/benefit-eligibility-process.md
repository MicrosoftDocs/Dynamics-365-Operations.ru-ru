---
title: Обработка применимости льгот
description: Эта процедура показывает, как работает процесс допустимости льготы.
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 859bf2ef369173ce4b6bc380820ea157ae86e13a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "325557"
---
# <a name="benefit-eligibility-process"></a><span data-ttu-id="a09b4-103">Обработка применимости льгот</span><span class="sxs-lookup"><span data-stu-id="a09b4-103">Benefit eligibility process</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a09b4-104">Эта процедура показывает, как работает процесс допустимости льготы.</span><span class="sxs-lookup"><span data-stu-id="a09b4-104">This procedure shows how the benefit eligibility process works.</span></span> <span data-ttu-id="a09b4-105">По завершении процесса можно просмотреть результаты.</span><span class="sxs-lookup"><span data-stu-id="a09b4-105">When the process is complete you can view the results.</span></span> <span data-ttu-id="a09b4-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="a09b4-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="a09b4-107">Перейдите в раздел "Управление персоналом" > "Льготы" > "Льготы".</span><span class="sxs-lookup"><span data-stu-id="a09b4-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="a09b4-108">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="a09b4-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="a09b4-109">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a09b4-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="a09b4-110">Выберите Изменить.</span><span class="sxs-lookup"><span data-stu-id="a09b4-110">Click Edit.</span></span>
5. <span data-ttu-id="a09b4-111">В поле "Приемлемость" выберите "На основе правила".</span><span class="sxs-lookup"><span data-stu-id="a09b4-111">In the Eligibility field, select 'Rule based'.</span></span>
6. <span data-ttu-id="a09b4-112">В поле "Тип правила" выберите правило политики льгот, которое необходимо применить к льготе.</span><span class="sxs-lookup"><span data-stu-id="a09b4-112">In the Rule type field, select the benefit policy rule you would like applied to the benefit.</span></span>
7. <span data-ttu-id="a09b4-113">В области действий щелкните "Льгота".</span><span class="sxs-lookup"><span data-stu-id="a09b4-113">On the Action Pane, click Benefit.</span></span>
8. <span data-ttu-id="a09b4-114">Щелкните "Создать событие допустимости", чтобы открыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a09b4-114">Click Create eligibility event to open the drop dialog.</span></span>
9. <span data-ttu-id="a09b4-115">В поле "Событие" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a09b4-115">In the Event field, type a value.</span></span>
10. <span data-ttu-id="a09b4-116">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a09b4-116">In the Description field, type a value.</span></span>
11. <span data-ttu-id="a09b4-117">В поле "Тип события" выберите "Открытие регистрации".</span><span class="sxs-lookup"><span data-stu-id="a09b4-117">In the Event type field, select 'Open enrollment'.</span></span>
12. <span data-ttu-id="a09b4-118">В поле "Начальная дата покрытия" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="a09b4-118">In the Coverage start date field, enter a date and time.</span></span>
13. <span data-ttu-id="a09b4-119">В поле "Начальная дата периода регистрации" введите дату и время.</span><span class="sxs-lookup"><span data-stu-id="a09b4-119">In the Enrollment period start date field, enter a date and time.</span></span>
14. <span data-ttu-id="a09b4-120">В поле "Дней на регистрацию" введите число.</span><span class="sxs-lookup"><span data-stu-id="a09b4-120">In the Days to enroll field, enter a number.</span></span>
15. <span data-ttu-id="a09b4-121">Щелкните "Создать событие".</span><span class="sxs-lookup"><span data-stu-id="a09b4-121">Click Create event.</span></span>
16. <span data-ttu-id="a09b4-122">На экспресс-вкладке "Работники" щелкните "Добавить".</span><span class="sxs-lookup"><span data-stu-id="a09b4-122">Click Add in the Workers FastTab.</span></span>
17. <span data-ttu-id="a09b4-123">В поле "Показать по типу" выберите "Сотрудники".</span><span class="sxs-lookup"><span data-stu-id="a09b4-123">In the Show by type field, select 'Employees'.</span></span>
18. <span data-ttu-id="a09b4-124">В поле "Показать по информации о компании" выберите "Текущая информация о компании".</span><span class="sxs-lookup"><span data-stu-id="a09b4-124">In the Show by legal entity field, select 'Current legal entity'.</span></span>
19. <span data-ttu-id="a09b4-125">В списке отметьте все строки или отмените отметку всех строк.</span><span class="sxs-lookup"><span data-stu-id="a09b4-125">In the list, mark or unmark all rows.</span></span>
20. <span data-ttu-id="a09b4-126">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a09b4-126">Click OK.</span></span>
21. <span data-ttu-id="a09b4-127">Щелкните "Обработать".</span><span class="sxs-lookup"><span data-stu-id="a09b4-127">Click Process.</span></span>
22. <span data-ttu-id="a09b4-128">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="a09b4-128">Click OK.</span></span>
23. <span data-ttu-id="a09b4-129">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="a09b4-129">Refresh the page.</span></span>
24. <span data-ttu-id="a09b4-130">Щелкните "Показать результаты".</span><span class="sxs-lookup"><span data-stu-id="a09b4-130">Click Show results.</span></span>
25. <span data-ttu-id="a09b4-131">Откройте фильтра столбца "Состояние".</span><span class="sxs-lookup"><span data-stu-id="a09b4-131">Open Status column filter.</span></span>
26. <span data-ttu-id="a09b4-132">Сортировать от А до Я</span><span class="sxs-lookup"><span data-stu-id="a09b4-132">Sort A to Z</span></span>

