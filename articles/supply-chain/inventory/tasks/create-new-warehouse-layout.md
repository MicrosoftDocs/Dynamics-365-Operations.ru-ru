---
title: Создание нового макета склада
description: Следующая процедура используется для настройки сведений о местонахождениях на складе.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0a52c5d68816a81a94db019387b9ea3ec3efc5a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845530"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="00ddb-103">Создание нового макета склада</span><span class="sxs-lookup"><span data-stu-id="00ddb-103">Create a new warehouse layout</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="00ddb-104">Следующая процедура используется для настройки сведений о местонахождениях на складе.</span><span class="sxs-lookup"><span data-stu-id="00ddb-104">This procedure shows you how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="00ddb-105">Она применяется только к складам, созданным с помощью функции базового управления складами в модуле "Управление запасами", и не применяется к складам, созданным в модуле "Управление складом".</span><span class="sxs-lookup"><span data-stu-id="00ddb-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="00ddb-106">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="00ddb-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="00ddb-107">Настройка вместимости местонахождения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="00ddb-107">Set the default location capacity</span></span>
1. <span data-ttu-id="00ddb-108">Перейдите в раздел "Управление запасами" > "Настройка" > "Параметры управления запасами и складами".</span><span class="sxs-lookup"><span data-stu-id="00ddb-108">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="00ddb-109">Перейдите на вкладку "Местонахождения".</span><span class="sxs-lookup"><span data-stu-id="00ddb-109">Click the Locations tab.</span></span>
3. <span data-ttu-id="00ddb-110">В поле "Стандартная ширина" введите число.</span><span class="sxs-lookup"><span data-stu-id="00ddb-110">In the Standard width field, enter a number.</span></span>
4. <span data-ttu-id="00ddb-111">В поле "Стандартная глубина" введите число.</span><span class="sxs-lookup"><span data-stu-id="00ddb-111">In the Standard depth field, enter a number.</span></span>
5. <span data-ttu-id="00ddb-112">В поле "Стандартная высота" введите число.</span><span class="sxs-lookup"><span data-stu-id="00ddb-112">In the Standard height field, enter a number.</span></span>
6. <span data-ttu-id="00ddb-113">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="00ddb-113">Click Save.</span></span>
7. <span data-ttu-id="00ddb-114">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="00ddb-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="00ddb-115">Определение формата имени местонахождения</span><span class="sxs-lookup"><span data-stu-id="00ddb-115">Define the location name format</span></span>
1. <span data-ttu-id="00ddb-116">Перейдите Управление запасами > Настройка > Разделение запасов > Склады.</span><span class="sxs-lookup"><span data-stu-id="00ddb-116">Go to Inventory management > Setup > Inventory breakdown > Warehouses.</span></span>
2. <span data-ttu-id="00ddb-117">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="00ddb-117">Click New.</span></span>
3. <span data-ttu-id="00ddb-118">В поле "Склад" введите значение.</span><span class="sxs-lookup"><span data-stu-id="00ddb-118">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="00ddb-119">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="00ddb-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="00ddb-120">В поле "Сайт" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="00ddb-120">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="00ddb-121">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="00ddb-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="00ddb-122">Переключите развертывание раздела "Имена местонахождений".</span><span class="sxs-lookup"><span data-stu-id="00ddb-122">Toggle the expansion of the Location names section.</span></span>
    * <span data-ttu-id="00ddb-123">Параметры в этом разделе определяют формат по умолчанию для имен местонахождений.</span><span class="sxs-lookup"><span data-stu-id="00ddb-123">The options in this section define the default format for location names.</span></span> <span data-ttu-id="00ddb-124">В нашем примере мы включим номер прохода, номер стеллажа и номер полки.</span><span class="sxs-lookup"><span data-stu-id="00ddb-124">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
8. <span data-ttu-id="00ddb-125">Установите для параметра "Включать проход" значение "Да".</span><span class="sxs-lookup"><span data-stu-id="00ddb-125">Set the Include aisle option to Yes.</span></span>
9. <span data-ttu-id="00ddb-126">Установите для параметра "Включать стеллаж" значение "Да".</span><span class="sxs-lookup"><span data-stu-id="00ddb-126">Set the Include rack option to Yes.</span></span> 
10. <span data-ttu-id="00ddb-127">В поле "Формат" введите значение для стеллажа.</span><span class="sxs-lookup"><span data-stu-id="00ddb-127">In the Format field, for the rack, type a value.</span></span>
    * <span data-ttu-id="00ddb-128">Пример: -##</span><span class="sxs-lookup"><span data-stu-id="00ddb-128">For example: -##</span></span>  
11. <span data-ttu-id="00ddb-129">Установите для параметра "Включать полку" значение "Да".</span><span class="sxs-lookup"><span data-stu-id="00ddb-129">Set the Include shelf option to Yes.</span></span>
12. <span data-ttu-id="00ddb-130">В поле "Формат" введите значение для полки.</span><span class="sxs-lookup"><span data-stu-id="00ddb-130">In the Format field, for the shelf, type a value.</span></span>
    * <span data-ttu-id="00ddb-131">Пример: -##</span><span class="sxs-lookup"><span data-stu-id="00ddb-131">For example: -##</span></span>  

## <a name="define-warehouse-locations"></a><span data-ttu-id="00ddb-132">Определение местонахождений склада</span><span class="sxs-lookup"><span data-stu-id="00ddb-132">Define warehouse locations</span></span>
1. <span data-ttu-id="00ddb-133">В области действий щелкните "Склад".</span><span class="sxs-lookup"><span data-stu-id="00ddb-133">On the Action Pane, click Warehouse.</span></span>
2. <span data-ttu-id="00ddb-134">Щелкните "Мастер местонахождений".</span><span class="sxs-lookup"><span data-stu-id="00ddb-134">Click Location Wizard.</span></span>
3. <span data-ttu-id="00ddb-135">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="00ddb-135">Click Next.</span></span>
4. <span data-ttu-id="00ddb-136">Отмена выбора параметра "Дебаркадеры отгрузки"</span><span class="sxs-lookup"><span data-stu-id="00ddb-136">De-select the Outbound docks option</span></span>
5. <span data-ttu-id="00ddb-137">Отмена выбора параметра "Буферные ячейки"</span><span class="sxs-lookup"><span data-stu-id="00ddb-137">De-select the Bulk locations option</span></span>
6. <span data-ttu-id="00ddb-138">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="00ddb-138">Click Next.</span></span>
7. <span data-ttu-id="00ddb-139">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="00ddb-139">Click Next.</span></span>
8. <span data-ttu-id="00ddb-140">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="00ddb-140">Click Next.</span></span>
9. <span data-ttu-id="00ddb-141">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="00ddb-141">Click Next.</span></span>
10. <span data-ttu-id="00ddb-142">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="00ddb-142">Click Next.</span></span>
11. <span data-ttu-id="00ddb-143">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="00ddb-143">Click Next.</span></span>
12. <span data-ttu-id="00ddb-144">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="00ddb-144">Click Next.</span></span>
    * <span data-ttu-id="00ddb-145">Обратите внимание, что физические аналитики, отображаемые на данной странице, — это аналитики, настроенные в начале этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="00ddb-145">Note that the physical dimensions shown on this page are the ones that you set at the start of this procedure.</span></span>  
13. <span data-ttu-id="00ddb-146">Щелкните Далее.</span><span class="sxs-lookup"><span data-stu-id="00ddb-146">Click Next.</span></span>
14. <span data-ttu-id="00ddb-147">Нажмите кнопку Готово.</span><span class="sxs-lookup"><span data-stu-id="00ddb-147">Click Finish.</span></span>
15. <span data-ttu-id="00ddb-148">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="00ddb-148">Close the page.</span></span>
16. <span data-ttu-id="00ddb-149">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="00ddb-149">Refresh the page.</span></span>

