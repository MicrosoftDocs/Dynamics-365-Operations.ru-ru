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
ms.search.form: CAMCostControlWorkspaceConfigurationPerUser
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 61f25b93440495b2d1b70227ecda011c43c2e564
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208783"
---
# <a name="configure-cost-control-workspace-parameters"></a><span data-ttu-id="a2faf-103">Настройка параметров рабочей области управления затратами</span><span class="sxs-lookup"><span data-stu-id="a2faf-103">Configure cost control workspace parameters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a2faf-104">Эта процедура используется для настройки рабочей области "Управление затратами" таким образом, чтобы менеджеры на различных уровнях организации могли получать представление о своих объектах затрат, например центрах затрат и группах продуктов.</span><span class="sxs-lookup"><span data-stu-id="a2faf-104">Use this procedure to configure the Cost control workspace so that managers at various levels in an organization can gain insight into their cost objects, such as cost centers and product groups.</span></span> <span data-ttu-id="a2faf-105">Для создания этой записи использовалась демонстрационная компания USP2.</span><span class="sxs-lookup"><span data-stu-id="a2faf-105">The USP2 demo company was used to create this recording.</span></span>

1. <span data-ttu-id="a2faf-106">Перейдите в раздел "Учет затрат" > "Настройка" > "Конфигурация рабочей области управления затратами".</span><span class="sxs-lookup"><span data-stu-id="a2faf-106">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
2. <span data-ttu-id="a2faf-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a2faf-107">Click New.</span></span>
3. <span data-ttu-id="a2faf-108">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a2faf-108">In the Name field, type a value.</span></span>
4. <span data-ttu-id="a2faf-109">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="a2faf-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a2faf-110">Выберите значение "Да" в поле "Опубликовано".</span><span class="sxs-lookup"><span data-stu-id="a2faf-110">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="a2faf-111">При выборе варианта «Да» просматривать отчет в рабочей области "Управление затратами" могут пользователи, которым назначена одна из следующих ролей: диспетчер учета затрат, бухгалтер по учету затрат, младший бухгалтер по учету затрат или контроллер объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="a2faf-111">If you set this option to Yes, users who are assigned one of these roles can see the report in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, or cost object controller.</span></span> <span data-ttu-id="a2faf-112">При выборе варианта «Нет» просматривать отчет в рабочей области "Управление затратами" могут только пользователи, которым назначена одна из следующих ролей: диспетчер учета затрат, бухгалтер по учету затрат, младший бухгалтер по учету затрат или контроллер объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="a2faf-112">If you set this option to No, only users who are assigned one of these roles can see the report in the Cost control workspace: cost accounting manager, cost accountant, or cost accountant clerk.</span></span>  
6. <span data-ttu-id="a2faf-113">Разверните раздел "Фильтрация данных".</span><span class="sxs-lookup"><span data-stu-id="a2faf-113">Expand the Data filtering section.</span></span>
7. <span data-ttu-id="a2faf-114">В поле "Единица управления затратами" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a2faf-114">In the Cost control unit field, enter or select a value.</span></span>
8. <span data-ttu-id="a2faf-115">В поле "Исходная версия бюджета" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a2faf-115">In the Budget original version field, enter or select a value.</span></span>
9. <span data-ttu-id="a2faf-116">В поле "Иерархия аналитик элементов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a2faf-116">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
10. <span data-ttu-id="a2faf-117">В поле "Иерархия аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a2faf-117">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
11. <span data-ttu-id="a2faf-118">Разверните раздел "Назначить записи расчета".</span><span class="sxs-lookup"><span data-stu-id="a2faf-118">Expand the Assign calculation records section.</span></span>
12. <span data-ttu-id="a2faf-119">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="a2faf-119">Click New.</span></span>
13. <span data-ttu-id="a2faf-120">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="a2faf-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="a2faf-121">В поле "Период финансового календаря" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a2faf-121">In the Fiscal calendar period field, enter or select a value.</span></span>
15. <span data-ttu-id="a2faf-122">В поле "Фактическая версия" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a2faf-122">In the Actual version field, enter or select a value.</span></span>
16. <span data-ttu-id="a2faf-123">Разверните раздел "Финансовые периоды по столбцам".</span><span class="sxs-lookup"><span data-stu-id="a2faf-123">Expand the Fiscal periods per column section.</span></span>
17. <span data-ttu-id="a2faf-124">Выберите "Да" в поле "Текущий период".</span><span class="sxs-lookup"><span data-stu-id="a2faf-124">Select Yes in the Current period field.</span></span>
18. <span data-ttu-id="a2faf-125">Разверните раздел "Столбцы для отображения затрат".</span><span class="sxs-lookup"><span data-stu-id="a2faf-125">Expand the Columns to display for costs section.</span></span>
19. <span data-ttu-id="a2faf-126">Выберите "Да" в поле "Постоянные затраты".</span><span class="sxs-lookup"><span data-stu-id="a2faf-126">Select Yes in the Fixed cost field.</span></span>
20. <span data-ttu-id="a2faf-127">Выберите "Да" в поле "Переменные затраты".</span><span class="sxs-lookup"><span data-stu-id="a2faf-127">Select Yes in the Variable cost field.</span></span>
21. <span data-ttu-id="a2faf-128">Выберите "Да" в поле "Общие затраты".</span><span class="sxs-lookup"><span data-stu-id="a2faf-128">Select Yes in the Total cost field.</span></span>
22. <span data-ttu-id="a2faf-129">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="a2faf-129">Click Save.</span></span>
23. <span data-ttu-id="a2faf-130">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="a2faf-130">Close the page.</span></span>
24. <span data-ttu-id="a2faf-131">Перейдите в раздел "Учет затрат" > "Рабочие области" > "Управление затратами".</span><span class="sxs-lookup"><span data-stu-id="a2faf-131">Go to Cost accounting > Workspaces > Cost control.</span></span>
25. <span data-ttu-id="a2faf-132">Выберите отчет для просмотра постоянных, переменных, общих и неклассифицированных затрат для выбранных финансовых периодов.</span><span class="sxs-lookup"><span data-stu-id="a2faf-132">Select a statement to see fixed, variable, total, and unclassified costs for the selected fiscal periods.</span></span>
26. <span data-ttu-id="a2faf-133">В поле "Период финансового календаря" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a2faf-133">In the Fiscal calendar period field, enter or select a value.</span></span>
27. <span data-ttu-id="a2faf-134">В поле "Узел иерархии аналитик объектов затрат" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="a2faf-134">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="a2faf-135">Выбрав иерархию аналитик объектов затрат, разверните иерархию аналитик элементов затрат для просмотра желаемых значений затрат.</span><span class="sxs-lookup"><span data-stu-id="a2faf-135">After you've selected a Cost object dimension hierarchy, expand the Cost element dimension hierarchy to see the desired cost values.</span></span> <span data-ttu-id="a2faf-136">Например, можно развернуть иерархию до производственных накладных расходов, чтобы увидеть значение.</span><span class="sxs-lookup"><span data-stu-id="a2faf-136">For example, you can expand the hierarchy to Manufacturing overhead to see the value.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]