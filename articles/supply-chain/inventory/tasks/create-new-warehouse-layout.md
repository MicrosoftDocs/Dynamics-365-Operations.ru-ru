---
title: Создание нового макета склада
description: В этом разделе описывается, как настроить информацию о местонахождениях на складе.
author: perlynne
manager: AnnBe
ms.date: 07/29/2019
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
ms.openlocfilehash: 302c028a93dfdb57972e4759abbbc4fdedabbd17
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867251"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="d997b-103">Создание нового макета склада</span><span class="sxs-lookup"><span data-stu-id="d997b-103">Create a new warehouse layout</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d997b-104">В этом разделе описывается, как настроить информацию о местонахождениях на складе.</span><span class="sxs-lookup"><span data-stu-id="d997b-104">This topic describes how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="d997b-105">Она применяется только к складам, созданным с помощью функции базового управления складами в модуле "Управление запасами", и не применяется к складам, созданным в модуле "Управление складом".</span><span class="sxs-lookup"><span data-stu-id="d997b-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="d997b-106">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="d997b-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="d997b-107">Настройка вместимости местонахождения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d997b-107">Set the default location capacity</span></span>
1. <span data-ttu-id="d997b-108">В области перехода выберите **Модули > Управление запасами > Настройка > Параметры модуля Управление запасами и складами**.</span><span class="sxs-lookup"><span data-stu-id="d997b-108">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="d997b-109">Выберите вкладку **Ячейки**.</span><span class="sxs-lookup"><span data-stu-id="d997b-109">Select the **Locations** tab.</span></span>
3. <span data-ttu-id="d997b-110">В поле **Стандартная ширина** введите число.</span><span class="sxs-lookup"><span data-stu-id="d997b-110">In the **Standard width** field, enter a number.</span></span>
4. <span data-ttu-id="d997b-111">В поле **Стандартная глубина** введите число.</span><span class="sxs-lookup"><span data-stu-id="d997b-111">In the **Standard depth** field, enter a number.</span></span>
5. <span data-ttu-id="d997b-112">В поле **Стандартная высота** введите число.</span><span class="sxs-lookup"><span data-stu-id="d997b-112">In the **Standard height** field, enter a number.</span></span>
6. <span data-ttu-id="d997b-113">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d997b-113">Select **Save**.</span></span>
7. <span data-ttu-id="d997b-114">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d997b-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="d997b-115">Определение формата имени местонахождения</span><span class="sxs-lookup"><span data-stu-id="d997b-115">Define the location name format</span></span>
1. <span data-ttu-id="d997b-116">В области перехода выберите **Модули > Управление запасами > Настройка > Разделение запасов > Склады**.</span><span class="sxs-lookup"><span data-stu-id="d997b-116">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>
2. <span data-ttu-id="d997b-117">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d997b-117">Select **New**.</span></span>
3. <span data-ttu-id="d997b-118">В поле **Склад** введите значение.</span><span class="sxs-lookup"><span data-stu-id="d997b-118">In the **Warehouse** field, type a value.</span></span>
4. <span data-ttu-id="d997b-119">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="d997b-119">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="d997b-120">В поле **Сайт** выберите требуемую запись в поле подстановки.</span><span class="sxs-lookup"><span data-stu-id="d997b-120">In the **Site** field, select the desired record in the lookup.</span></span>
6. <span data-ttu-id="d997b-121">Переключите развертывание раздела **Имена местонахождений**.</span><span class="sxs-lookup"><span data-stu-id="d997b-121">Toggle the expansion of the **Location names** section.</span></span> <span data-ttu-id="d997b-122">Параметры в этом разделе определяют формат по умолчанию для имен местонахождений.</span><span class="sxs-lookup"><span data-stu-id="d997b-122">The options in this section define the default format for location names.</span></span> <span data-ttu-id="d997b-123">В нашем примере мы включим номер прохода, номер стеллажа и номер полки.</span><span class="sxs-lookup"><span data-stu-id="d997b-123">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
7. <span data-ttu-id="d997b-124">Установите для параметра **Включать проход** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="d997b-124">Set the **Include aisle** option to **Yes**.</span></span>
8. <span data-ttu-id="d997b-125">Установите для параметра **Включать стеллаж** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="d997b-125">Set the **Include rack** option to **Yes**.</span></span> 
9. <span data-ttu-id="d997b-126">В поле **Формат** введите значение для стеллажа.</span><span class="sxs-lookup"><span data-stu-id="d997b-126">In the **Format** field, for the rack, type a value.</span></span>
10. <span data-ttu-id="d997b-127">Установите для параметра **Включать полку** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="d997b-127">Set the **Include shelf** option to **Yes**.</span></span>
11. <span data-ttu-id="d997b-128">В поле **Формат** введите значение для полки.</span><span class="sxs-lookup"><span data-stu-id="d997b-128">In the **Format** field, for the shelf, type a value.</span></span>

## <a name="define-warehouse-locations"></a><span data-ttu-id="d997b-129">Определение местонахождений склада</span><span class="sxs-lookup"><span data-stu-id="d997b-129">Define warehouse locations</span></span>
1. <span data-ttu-id="d997b-130">На панели операций выберите **Склад**.</span><span class="sxs-lookup"><span data-stu-id="d997b-130">On the Action Pane, select **Warehouse**.</span></span>
2. <span data-ttu-id="d997b-131">Выберите **Мастер ячеек хранения**.</span><span class="sxs-lookup"><span data-stu-id="d997b-131">Select **Location Wizard**.</span></span>
3. <span data-ttu-id="d997b-132">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="d997b-132">Select **Next**.</span></span>
4. <span data-ttu-id="d997b-133">Отмена выбора параметра **Дебаркадеры отгрузки**</span><span class="sxs-lookup"><span data-stu-id="d997b-133">De-select the **Outbound docks** option</span></span>
5. <span data-ttu-id="d997b-134">Отмена выбора параметра **Буферные ячейки**</span><span class="sxs-lookup"><span data-stu-id="d997b-134">De-select the **Bulk locations** option</span></span>
6. <span data-ttu-id="d997b-135">Нажимайте **Далее**, пока не перейдете к параметру для выбора **Готово**.</span><span class="sxs-lookup"><span data-stu-id="d997b-135">Select **Next** until you come to the option to select **Finish**.</span></span>
7. <span data-ttu-id="d997b-136">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d997b-136">Close the page.</span></span>
8. <span data-ttu-id="d997b-137">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="d997b-137">Refresh the page.</span></span>

