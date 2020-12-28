---
title: Настройка перераспределения номенклатур для недоукомплектованности
description: На этой теме показано, как разрешить работникам склада быстро искать альтернативные местоположения, если нет достаточного количества запасов в ячейке, к которой они были направлены.
author: ShylaThompson
manager: tfehr
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker, WHSLocationWithWorkException
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e8f5c23f82e96145f411ec993f766a90137b5b8
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4436393"
---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="dd205-103">Настройка перераспределения номенклатур для недоукомплектованности</span><span class="sxs-lookup"><span data-stu-id="dd205-103">Set up short picking item reallocation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dd205-104">На этой процедуры показано, как разрешить работникам склада быстро искать альтернативные местоположения, если нет достаточного количества запасов в ячейке, к которой они были направлены.</span><span class="sxs-lookup"><span data-stu-id="dd205-104">This procedure shows how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> 

<span data-ttu-id="dd205-105">Процесс перераспределения управляется **Исключением работы** и используется **работником** склада.</span><span class="sxs-lookup"><span data-stu-id="dd205-105">The reallocation process is controlled by a **Work exception** and used by the warehouse **worker.**</span></span>

<span data-ttu-id="dd205-106">Можно использовать автоматические, ручные или оба процесса перераспределения:</span><span class="sxs-lookup"><span data-stu-id="dd205-106">It is possible to use Automatic, Manual, or both reallocation processes:</span></span>

- <span data-ttu-id="dd205-107">Автоматическое перераспределение — директивы местоположения используются, чтобы определить, доступны ли товары в другом местоположении.</span><span class="sxs-lookup"><span data-stu-id="dd205-107">Automatic reallocation - Location directives are used to determine if the goods are available at another location.</span></span> <span data-ttu-id="dd205-108">Если возможно, работа будет обновлена, и пользователь склада будет перенаправлен в альтернативное местоположение.</span><span class="sxs-lookup"><span data-stu-id="dd205-108">If possible, the work will be updated and the warehouse user will be directed to the alternative location.</span></span>
- <span data-ttu-id="dd205-109">Перераспределение вручную — позволяет пользователю склада выбрать одно или несколько местоположений с незарезервированными количествами товаров.</span><span class="sxs-lookup"><span data-stu-id="dd205-109">Manual reallocation - Allows the warehouse user to select from one or more locations with unreserved quantities of goods.</span></span> 
- <span data-ttu-id="dd205-110">Автоматическое и ручное — если системе не удается выполнить автоматическое перераспределение, и доступны местонахождения с незарезервированными количествами, пользователю будет предложено выбрать местонахождение.</span><span class="sxs-lookup"><span data-stu-id="dd205-110">Automatic and manual - If the system is unable to perform an automatic reallocation, and locations are available with unreserved quantities, the user will be prompted to select a location.</span></span>

## <a name="set-up-work-exceptions"></a><span data-ttu-id="dd205-111">Настройка исключений работ</span><span class="sxs-lookup"><span data-stu-id="dd205-111">Set up work exceptions</span></span>
<span data-ttu-id="dd205-112">Можно определить несколько исключений работы с различными политиками переразмещения номенклатур, чтобы рабочий склада мог выбрать одно из них на основе потребностей отгрузки, которую он обрабатывает.</span><span class="sxs-lookup"><span data-stu-id="dd205-112">It's possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>

<span data-ttu-id="dd205-113">Компания USMF с демонстрационными данными используется для создания этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="dd205-113">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="dd205-114">В **области перехода** выберите **Управление складом > Настройка > Работа > Исключения работы**.</span><span class="sxs-lookup"><span data-stu-id="dd205-114">In the **Navigation pane**, go to **Warehouse management > Setup > Work > Work exceptions**.</span></span>
2. <span data-ttu-id="dd205-115">Щелкните **Создать**</span><span class="sxs-lookup"><span data-stu-id="dd205-115">Click **New**</span></span> 
3. <span data-ttu-id="dd205-116">В поле **Код исключения работы** введите значение.</span><span class="sxs-lookup"><span data-stu-id="dd205-116">In the **Work exception code** field, type a value.</span></span> <span data-ttu-id="dd205-117">Это будет название этого исключения.</span><span class="sxs-lookup"><span data-stu-id="dd205-117">This will be the title of this exception .</span></span> <span data-ttu-id="dd205-118">Например, "Руководство по недостаточной комплектации".</span><span class="sxs-lookup"><span data-stu-id="dd205-118">For example, Short picking manual.</span></span>
4. <span data-ttu-id="dd205-119">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="dd205-119">In the **Description** field, type a value.</span></span> <span data-ttu-id="dd205-120">Это будет кратким описанием использования этого исключения.</span><span class="sxs-lookup"><span data-stu-id="dd205-120">This will be a short description of the usage of this exception.</span></span> <span data-ttu-id="dd205-121">Например, недостаточная комплектация — номенклатура недоступна.</span><span class="sxs-lookup"><span data-stu-id="dd205-121">For example, Short picking - item not available.</span></span>
5. <span data-ttu-id="dd205-122">В поле типа **Исключение** выберите **Недоукомплектовать**.</span><span class="sxs-lookup"><span data-stu-id="dd205-122">In the **Exception** type field, select **Short pick**.</span></span>
6. <span data-ttu-id="dd205-123">Установите флажок **Корректировка складских запасов**.</span><span class="sxs-lookup"><span data-stu-id="dd205-123">Select the **Adjust inventory** check box.</span></span> <span data-ttu-id="dd205-124">Если выбрано, запасы будут автоматически скорректированы на 0 в местоположении с недостаточной комплектацией.</span><span class="sxs-lookup"><span data-stu-id="dd205-124">If selected, inventory will automatically be adjusted to 0 at the short picked location.</span></span>
7. <span data-ttu-id="dd205-125">В поле **Код типа корректировки по умолчанию** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="dd205-125">In the **Default adjustment type code** field, enter or select a value.</span></span> <span data-ttu-id="dd205-126">Например, в USMF можно выбрать **Удалить Res Adj Out**. Каждый код типа корректировки содержит четыре характеристики: наименование, описание, имя журнала запасов и **Удалить резервирования**.</span><span class="sxs-lookup"><span data-stu-id="dd205-126">For example, in USMF you can select **Remove Res Adj Out**. Each Adjustment type code contains four characteristics: name, description, inventory journal name, and **Remove reservations**.</span></span> <span data-ttu-id="dd205-127">Если параметр **Удалить резервирование** активирован, резервирования для строки заказа с недостаточной комплектацией будут удалены.</span><span class="sxs-lookup"><span data-stu-id="dd205-127">If **Remove reservations** is enabled, the short-picked order line's reservations will be removed.</span></span>  
8. <span data-ttu-id="dd205-128">В поле **Перераспределение номенклатур** выберите значение, такое как "Ручное".</span><span class="sxs-lookup"><span data-stu-id="dd205-128">In the **Item reallocation** field, select a value, such as Manual.</span></span> <span data-ttu-id="dd205-129">Если выбрано "Вручную" или "Автоматически и вручную", то работнику склада должно быть разрешено выполнять переразмещение вручную.</span><span class="sxs-lookup"><span data-stu-id="dd205-129">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="dd205-130">Настройте работника для использования ручного перераспределения номенклатуры</span><span class="sxs-lookup"><span data-stu-id="dd205-130">Set up a worker to use manual item reallocation</span></span>

<span data-ttu-id="dd205-131">Компания USMF с демонстрационными данными используется для создания этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="dd205-131">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="dd205-132">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="dd205-132">Close the page.</span></span>
2. <span data-ttu-id="dd205-133">В **области перехода** выберите **Управление складом > Настройка > Работник**.</span><span class="sxs-lookup"><span data-stu-id="dd205-133">In the **Navigation pane**, go to **Warehouse management > Setup > Worker**.</span></span>
3. <span data-ttu-id="dd205-134">Выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="dd205-134">Click **Edit**.</span></span>
4. <span data-ttu-id="dd205-135">В списке выберите работника.</span><span class="sxs-lookup"><span data-stu-id="dd205-135">In the list, select worker.</span></span> <span data-ttu-id="dd205-136">Например, Julia Funderburk.</span><span class="sxs-lookup"><span data-stu-id="dd205-136">For example, Julia Funderburk.</span></span>
5. <span data-ttu-id="dd205-137">Разверните экспресс-вкладку **Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="dd205-137">Expand the **Users** FastTab.</span></span>
6. <span data-ttu-id="dd205-138">В списке выберите **Код пользователя**.</span><span class="sxs-lookup"><span data-stu-id="dd205-138">In the list, select a **User ID**.</span></span> <span data-ttu-id="dd205-139">Например, 24.</span><span class="sxs-lookup"><span data-stu-id="dd205-139">For example, 24.</span></span>
7. <span data-ttu-id="dd205-140">Разверните экспресс-вкладку **Работа**.</span><span class="sxs-lookup"><span data-stu-id="dd205-140">Expand the **Work** FastTab.</span></span>
8. <span data-ttu-id="dd205-141">Выберите **Да** в поле **Разрешить перераспределение номенклатур вручную**.</span><span class="sxs-lookup"><span data-stu-id="dd205-141">Select **Yes** in the **Allow manual item reallocation** field.</span></span>
