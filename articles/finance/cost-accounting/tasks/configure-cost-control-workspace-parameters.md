---
title: Настройка параметров рабочей области управления затратами
description: Эта процедура используется для настройки рабочей области "Управление затратами" таким образом, чтобы менеджеры на различных уровнях организации могли получать представление о своих объектах затрат, например центрах затрат и группах продуктов.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 867bfd2f2d1ff486e683cb11c38906dd0efe8c14
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187874"
---
# <a name="configure-cost-control-workspace-parameters"></a><span data-ttu-id="b2b2b-103">Настройка параметров рабочей области управления затратами</span><span class="sxs-lookup"><span data-stu-id="b2b2b-103">Configure cost control workspace parameters</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b2b2b-104">Эта процедура используется для настройки рабочей области "Управление затратами" таким образом, чтобы менеджеры на различных уровнях организации могли получать представление о своих объектах затрат, например центрах затрат и группах продуктов.</span><span class="sxs-lookup"><span data-stu-id="b2b2b-104">Use this procedure to configure the Cost control workspace so that managers at various levels in an organization can gain insight into their cost objects, such as cost centers and product groups.</span></span> <span data-ttu-id="b2b2b-105">Для создания этой записи использовалась демонстрационная компания USP2.</span><span class="sxs-lookup"><span data-stu-id="b2b2b-105">The USP2 demo company was used to create this recording.</span></span>

1. <span data-ttu-id="b2b2b-106">Перейдите в раздел "Учет затрат" > "Настройка" > "Конфигурация рабочей области управления затратами".</span><span class="sxs-lookup"><span data-stu-id="b2b2b-106">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
2. <span data-ttu-id="b2b2b-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="b2b2b-107">Click New.</span></span>
3. <span data-ttu-id="b2b2b-108">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b2b2b-108">In the Name field, type a value.</span></span>
4. <span data-ttu-id="b2b2b-109">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b2b2b-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b2b2b-110">Выберите значение "Да" в поле "Опубликовано".</span><span class="sxs-lookup"><span data-stu-id="b2b2b-110">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="b2b2b-111">При выборе варианта «Да» просматривать отчет в рабочей области "Управление затратами" могут пользователи, которым назначена одна из следующих ролей: диспетчер учета затрат, бухгалтер по учету затрат, младший бухгалтер по учету затрат или контроллер объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="b2b2b-111">If you set this option to Yes, users who are assigned one of these roles can see the report in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, or cost object controller.</span></span> <span data-ttu-id="b2b2b-112">При выборе варианта «Нет» просматривать отчет в рабочей области "Управление затратами" могут только пользователи, которым назначена одна из следующих ролей: диспетчер учета затрат, бухгалтер по учету затрат, младший бухгалтер по учету затрат или контроллер объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="b2b2b-112">If you set this option to No, only users who are assigned one of these roles can see the report in the Cost control workspace: cost accounting manager, cost accountant, or cost accountant clerk.</span></span>  
6. <span data-ttu-id="b2b2b-113">Разверните раздел "Фильтрация данных".</span><span class="sxs-lookup"><span data-stu-id="b2b2b-113">Expand the Data filtering section.</span></span>
7. <span data-ttu-id="b2b2b-114">В поле "Единица управления затратами" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b2b2b-114">In the Cost control unit field, enter or select a value.</span></span>
8. <span data-ttu-id="b2b2b-115">В поле "Исходная версия бюджета" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b2b2b-115">In the Budget original version field, enter or select a value.</span></span>
9. <span data-ttu-id="b2b2b-116">В поле "Иерархия аналитик элементов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b2b2b-116">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
10. <span data-ttu-id="b2b2b-117">В поле "Иерархия аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b2b2b-117">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
11. <span data-ttu-id="b2b2b-118">Разверните раздел "Назначить записи расчета".</span><span class="sxs-lookup"><span data-stu-id="b2b2b-118">Expand the Assign calculation records section.</span></span>
12. <span data-ttu-id="b2b2b-119">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="b2b2b-119">Click New.</span></span>
13. <span data-ttu-id="b2b2b-120">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="b2b2b-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="b2b2b-121">В поле "Период финансового календаря" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b2b2b-121">In the Fiscal calendar period field, enter or select a value.</span></span>
15. <span data-ttu-id="b2b2b-122">В поле "Фактическая версия" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b2b2b-122">In the Actual version field, enter or select a value.</span></span>
16. <span data-ttu-id="b2b2b-123">Разверните раздел "Финансовые периоды по столбцам".</span><span class="sxs-lookup"><span data-stu-id="b2b2b-123">Expand the Fiscal periods per column section.</span></span>
17. <span data-ttu-id="b2b2b-124">Выберите "Да" в поле "Текущий период".</span><span class="sxs-lookup"><span data-stu-id="b2b2b-124">Select Yes in the Current period field.</span></span>
18. <span data-ttu-id="b2b2b-125">Разверните раздел "Столбцы для отображения затрат".</span><span class="sxs-lookup"><span data-stu-id="b2b2b-125">Expand the Columns to display for costs section.</span></span>
19. <span data-ttu-id="b2b2b-126">Выберите "Да" в поле "Постоянные затраты".</span><span class="sxs-lookup"><span data-stu-id="b2b2b-126">Select Yes in the Fixed cost field.</span></span>
20. <span data-ttu-id="b2b2b-127">Выберите "Да" в поле "Переменные затраты".</span><span class="sxs-lookup"><span data-stu-id="b2b2b-127">Select Yes in the Variable cost field.</span></span>
21. <span data-ttu-id="b2b2b-128">Выберите "Да" в поле "Общие затраты".</span><span class="sxs-lookup"><span data-stu-id="b2b2b-128">Select Yes in the Total cost field.</span></span>
22. <span data-ttu-id="b2b2b-129">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="b2b2b-129">Click Save.</span></span>
23. <span data-ttu-id="b2b2b-130">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="b2b2b-130">Close the page.</span></span>
24. <span data-ttu-id="b2b2b-131">Перейдите в раздел "Учет затрат" > "Рабочие области" > "Управление затратами".</span><span class="sxs-lookup"><span data-stu-id="b2b2b-131">Go to Cost accounting > Workspaces > Cost control.</span></span>
25. <span data-ttu-id="b2b2b-132">Выберите отчет для просмотра постоянных, переменных, общих и неклассифицированных затрат для выбранных финансовых периодов.</span><span class="sxs-lookup"><span data-stu-id="b2b2b-132">Select a statement to see fixed, variable, total, and unclassified costs for the selected fiscal periods.</span></span>
26. <span data-ttu-id="b2b2b-133">В поле "Период финансового календаря" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b2b2b-133">In the Fiscal calendar period field, enter or select a value.</span></span>
27. <span data-ttu-id="b2b2b-134">В поле "Узел иерархии аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="b2b2b-134">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="b2b2b-135">Выбрав иерархию аналитик объектов затрат, разверните иерархию аналитик элементов затрат для просмотра желаемых значений затрат.</span><span class="sxs-lookup"><span data-stu-id="b2b2b-135">After you've selected a Cost object dimension hierarchy, expand the Cost element dimension hierarchy to see the desired cost values.</span></span> <span data-ttu-id="b2b2b-136">Например, можно развернуть иерархию до производственных накладных расходов, чтобы увидеть значение.</span><span class="sxs-lookup"><span data-stu-id="b2b2b-136">For example, you can expand the hierarchy to Manufacturing overhead to see the value.</span></span>  

