---
title: Настройка элемента меню мобильного устройства для выполнения работы типа "заказ на покупку"
description: В этой процедуре показано, как настроить пункт меню "Мобильное устройство".
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFAutoConfirm, WHSRFMenu
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 707fc9c798da8eac30cc9f56c158be3d96b271d6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847119"
---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-of-type-purchase-order"></a><span data-ttu-id="00cd5-103">Настройка элемента меню мобильного устройства для выполнения работы типа "заказ на покупку"</span><span class="sxs-lookup"><span data-stu-id="00cd5-103">Set up a mobile device menu item for completing work of type Purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="00cd5-104">В этой процедуре показано, как настроить пункт меню "Мобильное устройство".</span><span class="sxs-lookup"><span data-stu-id="00cd5-104">This procedure shows how to set up a Mobile device menu item.</span></span> <span data-ttu-id="00cd5-105">В этом примере этот пункт меню используется для выполнения работы типа "Заказ на покупку".</span><span class="sxs-lookup"><span data-stu-id="00cd5-105">In this example, the menu item is used for performing work of type Purchase order.</span></span> <span data-ttu-id="00cd5-106">Допустимость работы определяется классом работы, связанным с пунктом меню.</span><span class="sxs-lookup"><span data-stu-id="00cd5-106">The work class that’s associated with the menu item determines which work is valid.</span></span> <span data-ttu-id="00cd5-107">Это руководство можно использовать в компании с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="00cd5-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="00cd5-108">Обычно эта процедура выполняется начальником склада.</span><span class="sxs-lookup"><span data-stu-id="00cd5-108">This procedure is typically carried out by a warehouse manager.</span></span>


## <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="00cd5-109">Создание элемента меню мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="00cd5-109">Create a mobile device menu item</span></span>
1. <span data-ttu-id="00cd5-110">Перейдите к элементам меню мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="00cd5-110">Go to Mobile device menu items.</span></span>
2. <span data-ttu-id="00cd5-111">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="00cd5-111">Click New.</span></span>
3. <span data-ttu-id="00cd5-112">В поле "Имя пункта меню" введите значение.</span><span class="sxs-lookup"><span data-stu-id="00cd5-112">In the Menu item name field, type a value.</span></span>
    * <span data-ttu-id="00cd5-113">Введите уникальное значение.</span><span class="sxs-lookup"><span data-stu-id="00cd5-113">Enter a unique value.</span></span> <span data-ttu-id="00cd5-114">Например, можно ввести "POMove".</span><span class="sxs-lookup"><span data-stu-id="00cd5-114">For example, you could type POMove.</span></span> <span data-ttu-id="00cd5-115">Запомните значение, оно понадобится позднее.</span><span class="sxs-lookup"><span data-stu-id="00cd5-115">Remember the value, you'll need it later.</span></span>  
4. <span data-ttu-id="00cd5-116">В поле "Заголовок" введите значение.</span><span class="sxs-lookup"><span data-stu-id="00cd5-116">In the Title field, type a value.</span></span>
    * <span data-ttu-id="00cd5-117">Это заголовок, который будет отображаться на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="00cd5-117">This is the title which will be displayed on the mobile device.</span></span> <span data-ttu-id="00cd5-118">Например, можно ввести "PO Move".</span><span class="sxs-lookup"><span data-stu-id="00cd5-118">For example, you could type PO Move.</span></span>  
5. <span data-ttu-id="00cd5-119">В поле "Режим" выберите "Работа".</span><span class="sxs-lookup"><span data-stu-id="00cd5-119">In the Mode field, select 'Work'.</span></span>
6. <span data-ttu-id="00cd5-120">Выберите значение "Да" в поле "Использовать существующую работу".</span><span class="sxs-lookup"><span data-stu-id="00cd5-120">Select Yes in the Use existing work field.</span></span>
    * <span data-ttu-id="00cd5-121">Этот пункт меню мобильного устройства используется для выполнения существующей работы.</span><span class="sxs-lookup"><span data-stu-id="00cd5-121">This mobile device menu item is used to perform existing work.</span></span> <span data-ttu-id="00cd5-122">Поэтому необходимо установить значение "Да".</span><span class="sxs-lookup"><span data-stu-id="00cd5-122">Therefore you must set this value to Yes.</span></span>  
    * <span data-ttu-id="00cd5-123">Поле "Показать статус запасов" определяет, будет ли отображаться статус запасов в наличии для работника склада на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="00cd5-123">The Display inventory status field determines whether the inventory status of the on-hand inventory will be displayed to the warehouse worker on the mobile device.</span></span>  
7. <span data-ttu-id="00cd5-124">В поле "Кем управляется" выберите "Системная группировка".</span><span class="sxs-lookup"><span data-stu-id="00cd5-124">In the Directed by field, select 'System grouping'.</span></span>
    * <span data-ttu-id="00cd5-125">При выборе значения в поле "Кем управляется" отображаются дополнительные поля в разделе "Общее" на этой странице.</span><span class="sxs-lookup"><span data-stu-id="00cd5-125">When you select something in the Directed by field, additional fields appear in the General section on this page.</span></span> <span data-ttu-id="00cd5-126">Отображаемые поля зависят от выбранного варианта.</span><span class="sxs-lookup"><span data-stu-id="00cd5-126">The fields that appear depend on what you selected.</span></span> <span data-ttu-id="00cd5-127">При выборе параметра "Системная группировка" добавляется два новых поля.</span><span class="sxs-lookup"><span data-stu-id="00cd5-127">When you select System grouping, two new fields are added.</span></span> <span data-ttu-id="00cd5-128">Они описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="00cd5-128">These are explained below.</span></span>  
8. <span data-ttu-id="00cd5-129">В поле "Системная группировка" выберите "WorkPoolId".</span><span class="sxs-lookup"><span data-stu-id="00cd5-129">In the System grouping field, select 'WorkPoolId'.</span></span>
    * <span data-ttu-id="00cd5-130">Если работники склада открывают этот пункт меню, отобразится запрос на сканирование кода пула работ.</span><span class="sxs-lookup"><span data-stu-id="00cd5-130">When warehouse workers open this menu item, they’ll be asked to scan a Work pool ID.</span></span> <span data-ttu-id="00cd5-131">Все заказы на выполнение работ с этим кодом пула работ и строки открытых заказов на выполнение работ с одним из классов работ, добавленных в этот пункт меню, будут представлены пользователю.</span><span class="sxs-lookup"><span data-stu-id="00cd5-131">All work orders with this Work pool ID and open work order lines with one of the work classes added to this menu item will be pushed to the user.</span></span>  
9. <span data-ttu-id="00cd5-132">В системе "Метка системной группировки" введите значение.</span><span class="sxs-lookup"><span data-stu-id="00cd5-132">In the System grouping label field, type a value.</span></span>
    * <span data-ttu-id="00cd5-133">Это текст, отображаемый для пользователя на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="00cd5-133">This is the text displayed to the user on the mobile device.</span></span> <span data-ttu-id="00cd5-134">Например, можно ввести "Код пула".</span><span class="sxs-lookup"><span data-stu-id="00cd5-134">For example, you could type Work pool.</span></span>  
10. <span data-ttu-id="00cd5-135">Выберите "Да" в поле "Переопределить номерной знак во время размещения".</span><span class="sxs-lookup"><span data-stu-id="00cd5-135">Select Yes in the Override license plate during put field.</span></span>
    * <span data-ttu-id="00cd5-136">Этот параметр позволяет работникам склада переопределять целевой номерной знак при размещении номенклатур в местонахождение под управлением номерного знака.</span><span class="sxs-lookup"><span data-stu-id="00cd5-136">This option allows warehouse workers to override the target license plate when items are put down on a license plate controlled location.</span></span>  
11. <span data-ttu-id="00cd5-137">Выберите "Да" в поле "Отложить группу".</span><span class="sxs-lookup"><span data-stu-id="00cd5-137">Select Yes in the Group put away field.</span></span>
    * <span data-ttu-id="00cd5-138">Если все строки размещения в заказе на выполнение работ используют одно и то же местонахождение, пользователь получит одну объединенную инструкцию по размещению для всех строк.</span><span class="sxs-lookup"><span data-stu-id="00cd5-138">If all the Put lines on the work order share the same location, the user will receive one combined Put instruction for all lines.</span></span>  
    * <span data-ttu-id="00cd5-139">Код шаблона аудита — шаблон аудита работы позволяет указать, что процесс работы для пункта меню следует прервать, чтобы можно было выполнить другую операцию.</span><span class="sxs-lookup"><span data-stu-id="00cd5-139">Audit template ID: A work audit template allows you to specify that the work process for a menu item should be interrupted so that another operation can be performed.</span></span> <span data-ttu-id="00cd5-140">Например, если пункт меню предназначен для входящей работы, шаблон аудита может требовать, чтобы работник проверял температуру.</span><span class="sxs-lookup"><span data-stu-id="00cd5-140">For example, if this menu item is for inbound work, the audit template might require that the worker checks the temperature.</span></span> <span data-ttu-id="00cd5-141">Точка, в которой прерывается процесс, определяется в шаблоне аудита и, например, может приходиться на момент начала или завершения работы либо на момент изменения статуса.</span><span class="sxs-lookup"><span data-stu-id="00cd5-141">The point at which the process is interrupted is specified on the audit template and can be, for example, when work is started or completed, or when its status changes.</span></span>  
12. <span data-ttu-id="00cd5-142">Разверните раздел "Классы работы".</span><span class="sxs-lookup"><span data-stu-id="00cd5-142">Expand the Work classes section.</span></span>
13. <span data-ttu-id="00cd5-143">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="00cd5-143">Click New.</span></span>
14. <span data-ttu-id="00cd5-144">В поле "Код класса работы" введите "Покупка".</span><span class="sxs-lookup"><span data-stu-id="00cd5-144">In the Work class ID field, type 'Purchase'.</span></span>
    * <span data-ttu-id="00cd5-145">Пул работ ограничивает работу, для которой можно использовать пункт меню.</span><span class="sxs-lookup"><span data-stu-id="00cd5-145">The work pool restricts the work that the menu item can be used for.</span></span> <span data-ttu-id="00cd5-146">В этом случае он будет использоваться для строк открытых заказов на выполнение работ с кодом класса работы "Покупка".</span><span class="sxs-lookup"><span data-stu-id="00cd5-146">In this case it will be used for open work order lines that have the Purchase work class ID.</span></span>  
15. <span data-ttu-id="00cd5-147">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="00cd5-147">Click Save.</span></span>

## <a name="set-up-work-confirmation"></a><span data-ttu-id="00cd5-148">Настройка подтверждения работы</span><span class="sxs-lookup"><span data-stu-id="00cd5-148">Set up work confirmation</span></span>
1. <span data-ttu-id="00cd5-149">Щелкните "Настройка подтверждения работы".</span><span class="sxs-lookup"><span data-stu-id="00cd5-149">Click Work confirmation setup.</span></span>
2. <span data-ttu-id="00cd5-150">В поле "Тип работы" выберите "Комплектация".</span><span class="sxs-lookup"><span data-stu-id="00cd5-150">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="00cd5-151">Установите флажок "Автоматическое подтверждение".</span><span class="sxs-lookup"><span data-stu-id="00cd5-151">Select the Auto confirm check box.</span></span>
    * <span data-ttu-id="00cd5-152">Рабочая инструкция с типом работы "Комплектация" будет подтверждена автоматически.</span><span class="sxs-lookup"><span data-stu-id="00cd5-152">The work instruction with work type Pick will be auto-confirmed.</span></span> <span data-ttu-id="00cd5-153">Эта инструкция не будет отображаться для пользователя.</span><span class="sxs-lookup"><span data-stu-id="00cd5-153">This instruction will not be presented to the user.</span></span>  
4. <span data-ttu-id="00cd5-154">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="00cd5-154">Click New.</span></span>
5. <span data-ttu-id="00cd5-155">В поле "Тип работы" выберите "Поместить".</span><span class="sxs-lookup"><span data-stu-id="00cd5-155">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="00cd5-156">Установите флажок "Подтверждение местонахождения".</span><span class="sxs-lookup"><span data-stu-id="00cd5-156">Select the Location confirmation check box.</span></span>
    * <span data-ttu-id="00cd5-157">Работнику склада будет предложено выполнить подтверждающее сканирование местонахождения при размещении номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="00cd5-157">The warehouse worker will be asked to perform a confirmation scan of the location, when the item is put down.</span></span>  
7. <span data-ttu-id="00cd5-158">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="00cd5-158">Click Save.</span></span>
8. <span data-ttu-id="00cd5-159">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="00cd5-159">Close the page.</span></span>
9. <span data-ttu-id="00cd5-160">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="00cd5-160">Close the page.</span></span>

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="00cd5-161">Добавление элемента меню в меню мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="00cd5-161">Add the menu item to a mobile device menu</span></span>
1. <span data-ttu-id="00cd5-162">Перейдите к элементам "Мобильное устройство".</span><span class="sxs-lookup"><span data-stu-id="00cd5-162">Go to Mobile device menu.</span></span>
2. <span data-ttu-id="00cd5-163">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="00cd5-163">Click Edit.</span></span>
3. <span data-ttu-id="00cd5-164">Используйте экспресс-фильтр для поиска записей.</span><span class="sxs-lookup"><span data-stu-id="00cd5-164">Use the Quick Filter to find records.</span></span> <span data-ttu-id="00cd5-165">Например, отфильтруйте поле "Имя" по значению "входящие".</span><span class="sxs-lookup"><span data-stu-id="00cd5-165">For example, filter on the Name field with a value of 'inbound'.</span></span>
    * <span data-ttu-id="00cd5-166">Вы хотите найти меню, используемое для входящих пунктов меню.</span><span class="sxs-lookup"><span data-stu-id="00cd5-166">You want to find the menu you use for inbound menu items.</span></span> <span data-ttu-id="00cd5-167">В USMF это называется "Входящие".</span><span class="sxs-lookup"><span data-stu-id="00cd5-167">In USMF this is called Inbound.</span></span>  
4. <span data-ttu-id="00cd5-168">В дереве выберите "значение".</span><span class="sxs-lookup"><span data-stu-id="00cd5-168">In the tree, select 'a value'.</span></span>
5. <span data-ttu-id="00cd5-169">Щелкните стрелку вправо.</span><span class="sxs-lookup"><span data-stu-id="00cd5-169">Click on the arrow that points to the right.</span></span>
6. <span data-ttu-id="00cd5-170">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="00cd5-170">Click Save.</span></span>
7. <span data-ttu-id="00cd5-171">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="00cd5-171">Close the page.</span></span>

