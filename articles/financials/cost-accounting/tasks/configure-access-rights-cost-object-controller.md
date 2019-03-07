---
title: Настройка прав доступа для контролера объектов затрат
description: Эта процедура используется для конфигурирования прав доступа для контроллера объектов затрат.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b7018f9d4926321341af94efd13911e2c69f5f5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "351179"
---
# <a name="configure-access-rights-for-a-cost-object-controller"></a><span data-ttu-id="8e011-103">Настройка прав доступа для контролера объектов затрат</span><span class="sxs-lookup"><span data-stu-id="8e011-103">Configure access rights for a cost object controller</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8e011-104">Эта процедура используется для конфигурирования прав доступа для контроллера объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="8e011-104">Use this procedure to configure access rights for a cost object controller.</span></span> <span data-ttu-id="8e011-105">В этой записи используется компания с демонстрационными данными USP2.</span><span class="sxs-lookup"><span data-stu-id="8e011-105">This recording uses the USP2 demo data company.</span></span>


## <a name="assign-the-cost-object-controller-role"></a><span data-ttu-id="8e011-106">Назначение роли контроллера объектов затрат</span><span class="sxs-lookup"><span data-stu-id="8e011-106">Assign the cost object controller role</span></span>
1. <span data-ttu-id="8e011-107">Перейдите в раздел "Администрирование системы" > "Пользователи" > "Пользователи".</span><span class="sxs-lookup"><span data-stu-id="8e011-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="8e011-108">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="8e011-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="8e011-109">Например, отфильтруйте поле "Имя пользователя" по значению "Alicia".</span><span class="sxs-lookup"><span data-stu-id="8e011-109">For example, filter on the User name field with a value of 'alicia'.</span></span>
3. <span data-ttu-id="8e011-110">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="8e011-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="8e011-111">Щелкните "Назначить роли".</span><span class="sxs-lookup"><span data-stu-id="8e011-111">Click Assign roles.</span></span>
5. <span data-ttu-id="8e011-112">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="8e011-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="8e011-113">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8e011-113">Click OK.</span></span>

## <a name="enable-access-list-security"></a><span data-ttu-id="8e011-114">Включение безопасности по списку доступа</span><span class="sxs-lookup"><span data-stu-id="8e011-114">Enable access list security</span></span>
1. <span data-ttu-id="8e011-115">Перейдите в раздел "Учет затрат" > "Аналитики" > "Иерархии аналитик".</span><span class="sxs-lookup"><span data-stu-id="8e011-115">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="8e011-116">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="8e011-116">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8e011-117">Выберите "Организация".</span><span class="sxs-lookup"><span data-stu-id="8e011-117">Select Organization.</span></span>  
3. <span data-ttu-id="8e011-118">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="8e011-118">Click Edit.</span></span>
4. <span data-ttu-id="8e011-119">Выберите "Да" в поле "Иерархия списков доступа".</span><span class="sxs-lookup"><span data-stu-id="8e011-119">Select Yes in the Access list hierarchy field.</span></span>
5. <span data-ttu-id="8e011-120">Щелкните "Просмотр иерархии".</span><span class="sxs-lookup"><span data-stu-id="8e011-120">Click View hierarchy.</span></span>

## <a name="assign-access-rights-to-user"></a><span data-ttu-id="8e011-121">Назначение пользователю прав доступа</span><span class="sxs-lookup"><span data-stu-id="8e011-121">Assign access rights to user</span></span>
1. <span data-ttu-id="8e011-122">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8e011-122">Click New.</span></span>
2. <span data-ttu-id="8e011-123">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="8e011-123">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="8e011-124">В поле "Код пользователя" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8e011-124">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="8e011-125">Выберите "Admin".</span><span class="sxs-lookup"><span data-stu-id="8e011-125">Select Admin.</span></span>  
4. <span data-ttu-id="8e011-126">В дереве выберите "Организация\Генеральный директор\Финансовый директор\FIM".</span><span class="sxs-lookup"><span data-stu-id="8e011-126">In the tree, select 'Organization\CEO\CFO\FIM'.</span></span>
5. <span data-ttu-id="8e011-127">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="8e011-127">Click New.</span></span>
6. <span data-ttu-id="8e011-128">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="8e011-128">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="8e011-129">В поле "Код пользователя" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="8e011-129">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="8e011-130">Выберите "Alicia".</span><span class="sxs-lookup"><span data-stu-id="8e011-130">Select Alicia.</span></span>  
8. <span data-ttu-id="8e011-131">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8e011-131">Click Save.</span></span>

## <a name="enable-access-rights-in-cost-accounting"></a><span data-ttu-id="8e011-132">Включение прав доступа в модуле "Учет затрат"</span><span class="sxs-lookup"><span data-stu-id="8e011-132">Enable access rights in Cost accounting</span></span>
1. <span data-ttu-id="8e011-133">Перейдите в раздел "Учет затрат" > "Настройка" > "Параметры".</span><span class="sxs-lookup"><span data-stu-id="8e011-133">Go to Cost accounting > Setup > Parameters.</span></span>
2. <span data-ttu-id="8e011-134">Перейдите на вкладку "Общие".</span><span class="sxs-lookup"><span data-stu-id="8e011-134">Click the General tab.</span></span>
3. <span data-ttu-id="8e011-135">Выберите "Да" в поле "Включить доступ на просмотр по элементам аналитик объектов затрат".</span><span class="sxs-lookup"><span data-stu-id="8e011-135">Select Yes in the Enable view access for cost object dimension members field.</span></span>
4. <span data-ttu-id="8e011-136">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8e011-136">Click Save.</span></span>
5. <span data-ttu-id="8e011-137">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8e011-137">Close the page.</span></span>
6. <span data-ttu-id="8e011-138">Перейдите в раздел "Учет затрат" > "Настройка" > "Конфигурация рабочей области управления затратами".</span><span class="sxs-lookup"><span data-stu-id="8e011-138">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
7. <span data-ttu-id="8e011-139">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="8e011-139">Click Edit.</span></span>
8. <span data-ttu-id="8e011-140">Выберите значение "Да" в поле "Опубликовано".</span><span class="sxs-lookup"><span data-stu-id="8e011-140">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="8e011-141">При выборе значения "Да" просматривать отчеты в рабочей области "Управление затратами" могут пользователи, которым назначена одна из следующих ролей: диспетчер учета затрат, бухгалтер по учету затрат, младший бухгалтер по учету затрат или контроллер объектов затрат.</span><span class="sxs-lookup"><span data-stu-id="8e011-141">If you select Yes, a user who is assigned one of the following four roles can see the reports in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, and cost object controller.</span></span> <span data-ttu-id="8e011-142">При выборе значения "Нет" просматривать отчеты в рабочей области "Управление затратами" могут только пользователи, которым назначена одна из следующих ролей: диспетчер учета затрат, бухгалтер по учету затрат или младший бухгалтер по учету затрат.</span><span class="sxs-lookup"><span data-stu-id="8e011-142">If you select No, only a user who is assigned one of the following roles can see the reports: cost accounting manager, cost accountant, and cost accountant clerk.</span></span>    
9. <span data-ttu-id="8e011-143">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="8e011-143">Click Save.</span></span>

