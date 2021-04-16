---
title: Устранение неполадок конфигурации склада
description: В этом разделе описывается устранение распространенных проблем, которые могут встретиться при настройке Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1dbd947f0740d22e0f79e6d5c272beb64715c8a5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814400"
---
# <a name="troubleshoot-warehouse-configuration"></a><span data-ttu-id="d20e4-103">Устранение неполадок конфигурации склада</span><span class="sxs-lookup"><span data-stu-id="d20e4-103">Troubleshoot warehouse configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d20e4-104">В этом разделе описывается устранение распространенных проблем, которые могут встретиться при настройке Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d20e4-104">This topic describes how to fix common issues that you might encounter while you configure Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a><span data-ttu-id="d20e4-105">Я получил следующее сообщение об ошибке: "Грузоместо или местонахождение недействительно."</span><span class="sxs-lookup"><span data-stu-id="d20e4-105">I receive the following error message: "The license plate or location is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="d20e4-106">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="d20e4-106">Issue description</span></span>

<span data-ttu-id="d20e4-107">Вы получаете это сообщение об ошибке при сканировании кода грузоместа или местоположения.</span><span class="sxs-lookup"><span data-stu-id="d20e4-107">You receive this error message when you scan a license plate ID or location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d20e4-108">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="d20e4-108">Issue resolution</span></span>

<span data-ttu-id="d20e4-109">Убедитесь в том, что код грузоместа не зарезервирован чем-то еще.</span><span class="sxs-lookup"><span data-stu-id="d20e4-109">Make sure that the license plate ID isn't reserved by something else.</span></span> <span data-ttu-id="d20e4-110">Эта проблема возникает, когда значение, которое сканируется пользователем в мобильном приложении управления складом, является допустимым местонахождением и допустимым кодом грузоместа.</span><span class="sxs-lookup"><span data-stu-id="d20e4-110">This issue used to occur when the value that a user scanned in the Warehouse Management mobile app was both a valid location and a valid license plate ID.</span></span> <span data-ttu-id="d20e4-111">Однако эта проблема была устранена в версии 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="d20e4-111">However, this issue was resolved in version 10.0.11.</span></span>

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a><span data-ttu-id="d20e4-112">Я получил следующее сообщение об ошибке: "Грузоместо должно быть указано для этого местонахождения."</span><span class="sxs-lookup"><span data-stu-id="d20e4-112">I receive the following error message: "License plate must be specified for this location."</span></span>

### <a name="issue-description"></a><span data-ttu-id="d20e4-113">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="d20e4-113">Issue description</span></span>

<span data-ttu-id="d20e4-114">Это сообщение об ошибке появляется, если заказ на перемещение создается с использованием склада, который активирован для расширенного управления складом (WMS), а затем, после завершения работы, вы пытаетесь подтвердить отгрузку.</span><span class="sxs-lookup"><span data-stu-id="d20e4-114">You receive this error message if you create a transfer order by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d20e4-115">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="d20e4-115">Issue resolution</span></span>

<span data-ttu-id="d20e4-116">Поле **Местоположение прихода по умолчанию** пусто для транзитного склада у склада "из".</span><span class="sxs-lookup"><span data-stu-id="d20e4-116">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="d20e4-117">Чтобы решить эту проблему, необходимо указать местоположение прихода по умолчанию на транзитном складе.</span><span class="sxs-lookup"><span data-stu-id="d20e4-117">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="d20e4-118">Убедитесь, что это местоположение управляется грузоместом.</span><span class="sxs-lookup"><span data-stu-id="d20e4-118">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a><span data-ttu-id="d20e4-119">Получено следующее сообщение об ошибке: "Невозможно создать строку шаблона работы для изменения статуса запасов, так как тип работы недопустим.</span><span class="sxs-lookup"><span data-stu-id="d20e4-119">I receive the following error message: "You can't create a work template line for Inventory status change because the work type is not valid.</span></span> <span data-ttu-id="d20e4-120">Выберите другой тип работы."</span><span class="sxs-lookup"><span data-stu-id="d20e4-120">Select a different work type."</span></span>

### <a name="issue-description"></a><span data-ttu-id="d20e4-121">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="d20e4-121">Issue description</span></span>

<span data-ttu-id="d20e4-122">Для шаблона работы невозможно выбрать *Изменение статуса запасов* в столбце **Тип работы** раздела **Сведения о шаблоне работ**.</span><span class="sxs-lookup"><span data-stu-id="d20e4-122">For a work template, you can't select *Inventory status change* in the **Work type** column of the **Work template details** section.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d20e4-123">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="d20e4-123">Issue resolution</span></span>

<span data-ttu-id="d20e4-124">Такое поведение предусмотрено разработчиками.</span><span class="sxs-lookup"><span data-stu-id="d20e4-124">This behavior is by design.</span></span> <span data-ttu-id="d20e4-125">Тип работы *Изменения статуса запасов* используется только в системных процессах.</span><span class="sxs-lookup"><span data-stu-id="d20e4-125">The *Inventory status change* work type is used only by system processes.</span></span> <span data-ttu-id="d20e4-126">Это нельзя настроить.</span><span class="sxs-lookup"><span data-stu-id="d20e4-126">It can't be configured.</span></span> <span data-ttu-id="d20e4-127">Так как список типов работы фиксируется как перечисление, дополнительные записи не могут быть отфильтрованы из выпадающего меню **Тип работы**.</span><span class="sxs-lookup"><span data-stu-id="d20e4-127">Because the list of work types is fixed as an enumeration, the extra entries can't be filtered out of the **Work type** drop-down menu.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="d20e4-128">Я получил следующее сообщение об ошибке: "Количество недействительно для единицы 1%."</span><span class="sxs-lookup"><span data-stu-id="d20e4-128">I receive the following error message: "The Quantity is not valid for unit 1%."</span></span>

### <a name="issue-description"></a><span data-ttu-id="d20e4-129">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="d20e4-129">Issue description</span></span>

<span data-ttu-id="d20e4-130">Количество недействительно для единицы измерения *шт.*, когда одна работа по комплектации содержит несколько грузомест в одном местоположении.</span><span class="sxs-lookup"><span data-stu-id="d20e4-130">The quantity isn't valid for the *ea* unit when there is picking work that has multiple license plates in one location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d20e4-131">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="d20e4-131">Issue resolution</span></span>

<span data-ttu-id="d20e4-132">Убедитесь, что поля **Код группы упорядочения единиц** и **Пересчеты единиц измерения** для выпущенного продукта или варианта продукта установлены правильно.</span><span class="sxs-lookup"><span data-stu-id="d20e4-132">Verify that the **Unit sequence group ID** and **Unit conversions** fields on the released product or product variant are set correctly.</span></span>

<span data-ttu-id="d20e4-133">Обратите внимание, что сообщение об ошибке было улучшено в версии 10.0.15 (см. статью базы знаний [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span><span class="sxs-lookup"><span data-stu-id="d20e4-133">Note that the error message has been improved in version 10.0.15 (see [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span></span> <span data-ttu-id="d20e4-134">Новое сообщение об ошибке "Количество является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="d20e4-134">The new error message is, "The quantity is not valid.</span></span> <span data-ttu-id="d20e4-135">Ожидалось %1 %2."</span><span class="sxs-lookup"><span data-stu-id="d20e4-135">Expected %1 %2."</span></span>

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a><span data-ttu-id="d20e4-136">В директивах местоположения для работы размещения по заказам на продажу параметр нескольких SKU не выполняет оценку нескольких действий директивы местоположения.</span><span class="sxs-lookup"><span data-stu-id="d20e4-136">In location directives for sales order put work, the multiple SKU option doesn't evaluate multiple location directive actions.</span></span>

### <a name="issue-description"></a><span data-ttu-id="d20e4-137">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="d20e4-137">Issue description</span></span>

<span data-ttu-id="d20e4-138">Директивы местоположения типа заказа на работу *Заказы на продажу* и типа работы *Размещение* не оценивают несколько действий директивы местоположения при выборе параметра **Несколько SKU**.</span><span class="sxs-lookup"><span data-stu-id="d20e4-138">Location directives of the *Sales orders* work order type and the *Put* work type don't evaluate multiple location directive actions when the **Multiple SKU** option is selected.</span></span> <span data-ttu-id="d20e4-139">Оценивается только действие директивы первого местоположения.</span><span class="sxs-lookup"><span data-stu-id="d20e4-139">Only the first location directive action is evaluated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d20e4-140">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="d20e4-140">Issue resolution</span></span>

<span data-ttu-id="d20e4-141">Новая функция *Оценивать все действия для директив местоположения с несколькими SKU* была добавлена в версии 10.0.15 (см. статью базы знаний [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span><span class="sxs-lookup"><span data-stu-id="d20e4-141">A new feature, *Evaluate all actions for Multi SKU location directives*, has been added in version 10.0.15 (see [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span></span> <span data-ttu-id="d20e4-142">Эта функция оценивает все действия для директив местоположения с несколькими единицами складского учета SKU.</span><span class="sxs-lookup"><span data-stu-id="d20e4-142">This feature evaluates all actions for multi-SKU location directives.</span></span> <span data-ttu-id="d20e4-143">Если вам требуется эта функция, используйте [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), чтобы включить ее.</span><span class="sxs-lookup"><span data-stu-id="d20e4-143">If you require this feature, use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn it on.</span></span>

## <a name="i-cant-use-the-warehouse-management-mobile-app-to-do-partial-picking"></a><span data-ttu-id="d20e4-144">Я не могу использовать мобильное приложение управления складом для частичной комплектации.</span><span class="sxs-lookup"><span data-stu-id="d20e4-144">I can't use the Warehouse Management mobile app to do partial picking.</span></span>

### <a name="issue-description"></a><span data-ttu-id="d20e4-145">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="d20e4-145">Issue description</span></span>

<span data-ttu-id="d20e4-146">Для заказов на продажу и на перемещение нельзя пропустить номенклатуру и выполнить частичную комплектацию.</span><span class="sxs-lookup"><span data-stu-id="d20e4-146">For sales and transfer orders, you can't skip items and do partial picking.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d20e4-147">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="d20e4-147">Issue resolution</span></span>

<span data-ttu-id="d20e4-148">На странице **Пункты меню мобильного устройства** для каждого пункта меню, настроенного для обработки заказов на продажу или заказов на перемещение, установите для параметра **Разрешить разделение работы** на экспресс-вкладке **Общие** значение *Да*.</span><span class="sxs-lookup"><span data-stu-id="d20e4-148">On the **Mobile device menu items** page, for each menu item that is set up to process sales orders or transfer orders, set the **Allow splitting of work** option on the **General** FastTab to *Yes*.</span></span>

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a><span data-ttu-id="d20e4-149">Как можно изменить статус складских запасов для работы с неполным объемом?</span><span class="sxs-lookup"><span data-stu-id="d20e4-149">How can I do an inventory status change for partial quantity work?</span></span>

### <a name="issue-description"></a><span data-ttu-id="d20e4-150">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="d20e4-150">Issue description</span></span>

<span data-ttu-id="d20e4-151">Вы хотите изменить статус запасов для неполного количества партии.</span><span class="sxs-lookup"><span data-stu-id="d20e4-151">You want to do an inventory status change for a partial quantity of a batch.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d20e4-152">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="d20e4-152">Issue resolution</span></span>

<span data-ttu-id="d20e4-153">Чтобы разрешить работникам выполнять это изменение, можно создать пункт меню для мобильного приложения управления складом.</span><span class="sxs-lookup"><span data-stu-id="d20e4-153">To enable workers to make this change, you can create a menu item for the Warehouse Management mobile app.</span></span> <span data-ttu-id="d20e4-154">На странице **Пункты меню мобильного устройства** создайте (или измените) пункт меню, который имеет следующие настройки:</span><span class="sxs-lookup"><span data-stu-id="d20e4-154">On the **Mobile device menu items** page, create (or edit) a menu item that has the following settings:</span></span>

- <span data-ttu-id="d20e4-155">**Режим:** *Работа*</span><span class="sxs-lookup"><span data-stu-id="d20e4-155">**Mode:** *Work*</span></span>
- <span data-ttu-id="d20e4-156">**Использовать существующую работу:** *Нет*</span><span class="sxs-lookup"><span data-stu-id="d20e4-156">**Use existing work:** *No*</span></span>
- <span data-ttu-id="d20e4-157">**Процесс создания работы:** *Перемещение*</span><span class="sxs-lookup"><span data-stu-id="d20e4-157">**Work creation process:** *Movement*</span></span>
- <span data-ttu-id="d20e4-158">**Показать статус запасов:** *Да*</span><span class="sxs-lookup"><span data-stu-id="d20e4-158">**Display inventory status:** *Yes*</span></span>

<span data-ttu-id="d20e4-159">При необходимости на этой странице можно настроить другие поля.</span><span class="sxs-lookup"><span data-stu-id="d20e4-159">You can set other fields on the page as you require.</span></span>

## <a name="the-dock-management-profile-of-a-location-profile-is-not-preventing-inventory-types-from-being-mixed"></a><span data-ttu-id="d20e4-160">Профиль управления доком профиля местоположения не препятствует смешению типов запасов.</span><span class="sxs-lookup"><span data-stu-id="d20e4-160">The dock management profile of a location profile is not preventing inventory types from being mixed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="d20e4-161">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="d20e4-161">Issue description</span></span>

<span data-ttu-id="d20e4-162">Вы используете *политики консолидации отгрузок*.</span><span class="sxs-lookup"><span data-stu-id="d20e4-162">You are using *shipment consolidation policies*.</span></span> <span data-ttu-id="d20e4-163">Вы настроили *профиль управления доком* для *профиля местоположения*, но при создании работы типы запасов смешиваются в конечном местоположении.</span><span class="sxs-lookup"><span data-stu-id="d20e4-163">You have set up a *dock management profile* for a *location profile*, but when work is created, the inventory types are mixed at the final location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d20e4-164">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="d20e4-164">Issue resolution</span></span>

<span data-ttu-id="d20e4-165">Для профилей управления доком требуется, чтобы работа была разбита заранее.</span><span class="sxs-lookup"><span data-stu-id="d20e4-165">Dock management profiles require work to be split up front.</span></span> <span data-ttu-id="d20e4-166">Иными словами, профиль управления доком ожидает, что в заголовке работы не будет несколько местоположений размещения.</span><span class="sxs-lookup"><span data-stu-id="d20e4-166">In other words, the dock management profile expects that a work header won't have multiple put locations.</span></span>

<span data-ttu-id="d20e4-167">Чтобы профиль управления доком эффективно управлял смешением запасов, необходимо настроить разбивку заголовка работ.</span><span class="sxs-lookup"><span data-stu-id="d20e4-167">For the dock management profile to effectively manage the mixing of inventory, a work header break must be set up.</span></span>

<span data-ttu-id="d20e4-168">В этом примере наш профиль управления доком настроен таким образом, что **Типы запасов, которые не следует смешивать** задано как *Код отгрузки*, и для него настраивается забивка заголовка работы:</span><span class="sxs-lookup"><span data-stu-id="d20e4-168">In this example our dock management profile is configured such that **Inventory types that should not be mixed** is set to *Shipment ID*, and we'll set up a work header break for it:</span></span>

1. <span data-ttu-id="d20e4-169">Перейдите в раздел **Управление складом \> Настройка \> Работа \> Шаблоны работ**.</span><span class="sxs-lookup"><span data-stu-id="d20e4-169">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="d20e4-170">Выберите **Типа заказа на работу** для редактирования (например, *Заказы на покупку*).</span><span class="sxs-lookup"><span data-stu-id="d20e4-170">Select the **Work order type** to edit (for example, *Purchase orders*).</span></span>
1. <span data-ttu-id="d20e4-171">Выберите шаблон работы для редактирования.</span><span class="sxs-lookup"><span data-stu-id="d20e4-171">Select the work template to edit.</span></span>
1. <span data-ttu-id="d20e4-172">На панели операций выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="d20e4-172">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="d20e4-173">Откройте вкладку **Сортировка** и добавьте строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="d20e4-173">Open the **Sorting** tab and add a row with the following settings:</span></span>
    - <span data-ttu-id="d20e4-174">**Таблица** - *Временные рабочие проводки*</span><span class="sxs-lookup"><span data-stu-id="d20e4-174">**Table** - *Temporary work transactions*</span></span>
    - <span data-ttu-id="d20e4-175">**Производная таблица** - *Временные рабочие проводки*</span><span class="sxs-lookup"><span data-stu-id="d20e4-175">**Derived table** - *Temporary work transactions*</span></span>
    - <span data-ttu-id="d20e4-176">**Поле** - *Код отгрузки*</span><span class="sxs-lookup"><span data-stu-id="d20e4-176">**Field** - *Shipment ID*</span></span>
1. <span data-ttu-id="d20e4-177">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d20e4-177">Select **OK**.</span></span>
1. <span data-ttu-id="d20e4-178">Вы возвращаетесь на страницу **Шаблоны работ**.</span><span class="sxs-lookup"><span data-stu-id="d20e4-178">You return to the **Work templates** page.</span></span> <span data-ttu-id="d20e4-179">В панели операций выберите **Разрывы заголовка работы**.</span><span class="sxs-lookup"><span data-stu-id="d20e4-179">On the Action Pane, select **Work header breaks**.</span></span>
1. <span data-ttu-id="d20e4-180">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="d20e4-180">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="d20e4-181">Установите флажок, связанный с **Имя поля** *Код отгрузки*.</span><span class="sxs-lookup"><span data-stu-id="d20e4-181">Select the check box associated with the **Field name** *Shipment ID*.</span></span>
1. <span data-ttu-id="d20e4-182">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d20e4-182">On the Action Pane, select **Save**.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
