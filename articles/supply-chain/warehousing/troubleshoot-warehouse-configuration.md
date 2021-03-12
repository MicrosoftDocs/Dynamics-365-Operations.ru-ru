---
title: Устранение неполадок конфигурации склада
description: В этом разделе описывается устранение распространенных проблем, которые могут встретиться при настройке Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 09b5770190fea9591f422b61ce6deedb2b9fa790
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994011"
---
# <a name="troubleshoot-warehouse-configuration"></a><span data-ttu-id="40a63-103">Устранение неполадок конфигурации склада</span><span class="sxs-lookup"><span data-stu-id="40a63-103">Troubleshoot warehouse configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40a63-104">В этом разделе описывается устранение распространенных проблем, которые могут встретиться при настройке Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="40a63-104">This topic describes how to fix common issues that you might encounter while you configure Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a><span data-ttu-id="40a63-105">Я получил следующее сообщение об ошибке: "Грузоместо или местонахождение недействительно."</span><span class="sxs-lookup"><span data-stu-id="40a63-105">I receive the following error message: "The license plate or location is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="40a63-106">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="40a63-106">Issue description</span></span>

<span data-ttu-id="40a63-107">Вы получаете это сообщение об ошибке при сканировании кода грузоместа или местоположения.</span><span class="sxs-lookup"><span data-stu-id="40a63-107">You receive this error message when you scan a license plate ID or location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="40a63-108">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="40a63-108">Issue resolution</span></span>

<span data-ttu-id="40a63-109">Убедитесь в том, что код грузоместа не зарезервирован чем-то еще.</span><span class="sxs-lookup"><span data-stu-id="40a63-109">Make sure that the license plate ID isn't reserved by something else.</span></span> <span data-ttu-id="40a63-110">Эта проблема возникает, когда значение, которое сканируется пользователем в приложении склада, является допустимым местонахождением и допустимым кодом грузоместа.</span><span class="sxs-lookup"><span data-stu-id="40a63-110">This issue used to occur when the value that a user scanned in the warehouse app was both a valid location and a valid license plate ID.</span></span> <span data-ttu-id="40a63-111">Однако эта проблема была устранена в версии 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="40a63-111">However, this issue was resolved in version 10.0.11.</span></span>

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a><span data-ttu-id="40a63-112">Я получил следующее сообщение об ошибке: "Грузоместо должно быть указано для этого местонахождения."</span><span class="sxs-lookup"><span data-stu-id="40a63-112">I receive the following error message: "License plate must be specified for this location."</span></span>

### <a name="issue-description"></a><span data-ttu-id="40a63-113">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="40a63-113">Issue description</span></span>

<span data-ttu-id="40a63-114">Это сообщение об ошибке появляется, если заказ на перемещение создается с использованием склада, который активирован для расширенного управления складом (WMS), а затем, после завершения работы, вы пытаетесь подтвердить отгрузку.</span><span class="sxs-lookup"><span data-stu-id="40a63-114">You receive this error message if you create a transfer order by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="40a63-115">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="40a63-115">Issue resolution</span></span>

<span data-ttu-id="40a63-116">Поле **Местоположение прихода по умолчанию** пусто для транзитного склада у склада "из".</span><span class="sxs-lookup"><span data-stu-id="40a63-116">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="40a63-117">Чтобы решить эту проблему, необходимо указать местоположение прихода по умолчанию на транзитном складе.</span><span class="sxs-lookup"><span data-stu-id="40a63-117">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="40a63-118">Убедитесь, что это местоположение управляется грузоместом.</span><span class="sxs-lookup"><span data-stu-id="40a63-118">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a><span data-ttu-id="40a63-119">Получено следующее сообщение об ошибке: "Невозможно создать строку шаблона работы для изменения статуса запасов, так как тип работы недопустим.</span><span class="sxs-lookup"><span data-stu-id="40a63-119">I receive the following error message: "You can't create a work template line for Inventory status change because the work type is not valid.</span></span> <span data-ttu-id="40a63-120">Выберите другой тип работы."</span><span class="sxs-lookup"><span data-stu-id="40a63-120">Select a different work type."</span></span>

### <a name="issue-description"></a><span data-ttu-id="40a63-121">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="40a63-121">Issue description</span></span>

<span data-ttu-id="40a63-122">Для шаблона работы невозможно выбрать *Изменение статуса запасов* в столбце **Тип работы** раздела **Сведения о шаблоне работ**.</span><span class="sxs-lookup"><span data-stu-id="40a63-122">For a work template, you can't select *Inventory status change* in the **Work type** column of the **Work template details** section.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="40a63-123">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="40a63-123">Issue resolution</span></span>

<span data-ttu-id="40a63-124">Такое поведение предусмотрено разработчиками.</span><span class="sxs-lookup"><span data-stu-id="40a63-124">This behavior is by design.</span></span> <span data-ttu-id="40a63-125">Тип работы *Изменения статуса запасов* используется только в системных процессах.</span><span class="sxs-lookup"><span data-stu-id="40a63-125">The *Inventory status change* work type is used only by system processes.</span></span> <span data-ttu-id="40a63-126">Это нельзя настроить.</span><span class="sxs-lookup"><span data-stu-id="40a63-126">It can't be configured.</span></span> <span data-ttu-id="40a63-127">Так как список типов работы фиксируется как перечисление, дополнительные записи не могут быть отфильтрованы из выпадающего меню **Тип работы**.</span><span class="sxs-lookup"><span data-stu-id="40a63-127">Because the list of work types is fixed as an enumeration, the extra entries can't be filtered out of the **Work type** drop-down menu.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="40a63-128">Я получил следующее сообщение об ошибке: "Количество недействительно для единицы 1%."</span><span class="sxs-lookup"><span data-stu-id="40a63-128">I receive the following error message: "The Quantity is not valid for unit 1%."</span></span>

### <a name="issue-description"></a><span data-ttu-id="40a63-129">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="40a63-129">Issue description</span></span>

<span data-ttu-id="40a63-130">Количество недействительно для единицы измерения *шт.*, когда одна работа по комплектации содержит несколько грузомест в одном местоположении.</span><span class="sxs-lookup"><span data-stu-id="40a63-130">The quantity isn't valid for the *ea* unit when there is picking work that has multiple license plates in one location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="40a63-131">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="40a63-131">Issue resolution</span></span>

<span data-ttu-id="40a63-132">Убедитесь, что поля **Код группы упорядочения единиц** и **Пересчеты единиц измерения** для выпущенного продукта или варианта продукта установлены правильно.</span><span class="sxs-lookup"><span data-stu-id="40a63-132">Verify that the **Unit sequence group ID** and **Unit conversions** fields on the released product or product variant are set correctly.</span></span>

<span data-ttu-id="40a63-133">Обратите внимание, что сообщение об ошибке было улучшено в версии 10.0.15 (см. статью базы знаний [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span><span class="sxs-lookup"><span data-stu-id="40a63-133">Note that the error message has been improved in version 10.0.15 (see [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span></span> <span data-ttu-id="40a63-134">Новое сообщение об ошибке "Количество является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="40a63-134">The new error message is, "The quantity is not valid.</span></span> <span data-ttu-id="40a63-135">Ожидалось %1 %2."</span><span class="sxs-lookup"><span data-stu-id="40a63-135">Expected %1 %2."</span></span>

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a><span data-ttu-id="40a63-136">В директивах местоположения для работы размещения по заказам на продажу параметр нескольких SKU не выполняет оценку нескольких действий директивы местоположения.</span><span class="sxs-lookup"><span data-stu-id="40a63-136">In location directives for sales order put work, the multiple SKU option doesn't evaluate multiple location directive actions.</span></span>

### <a name="issue-description"></a><span data-ttu-id="40a63-137">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="40a63-137">Issue description</span></span>

<span data-ttu-id="40a63-138">Директивы местоположения типа заказа на работу *Заказы на продажу* и типа работы *Размещение* не оценивают несколько действий директивы местоположения при выборе параметра **Несколько SKU**.</span><span class="sxs-lookup"><span data-stu-id="40a63-138">Location directives of the *Sales orders* work order type and the *Put* work type don't evaluate multiple location directive actions when the **Multiple SKU** option is selected.</span></span> <span data-ttu-id="40a63-139">Оценивается только действие директивы первого местоположения.</span><span class="sxs-lookup"><span data-stu-id="40a63-139">Only the first location directive action is evaluated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="40a63-140">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="40a63-140">Issue resolution</span></span>

<span data-ttu-id="40a63-141">Новая функция *Оценивать все действия для директив местоположения с несколькими SKU* была добавлена в версии 10.0.15 (см. статью базы знаний [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span><span class="sxs-lookup"><span data-stu-id="40a63-141">A new feature, *Evaluate all actions for Multi SKU location directives*, has been added in version 10.0.15 (see [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span></span> <span data-ttu-id="40a63-142">Эта функция оценивает все действия для директив местоположения с несколькими единицами складского учета SKU.</span><span class="sxs-lookup"><span data-stu-id="40a63-142">This feature evaluates all actions for multi-SKU location directives.</span></span> <span data-ttu-id="40a63-143">Если вам требуется эта функция, используйте [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), чтобы включить ее.</span><span class="sxs-lookup"><span data-stu-id="40a63-143">If you require this feature, use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn it on.</span></span>

## <a name="i-cant-use-the-warehouse-app-to-do-partial-picking"></a><span data-ttu-id="40a63-144">Я не могу использовать приложение склада для частичной комплектации.</span><span class="sxs-lookup"><span data-stu-id="40a63-144">I can't use the warehouse app to do partial picking.</span></span>

### <a name="issue-description"></a><span data-ttu-id="40a63-145">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="40a63-145">Issue description</span></span>

<span data-ttu-id="40a63-146">Для заказов на продажу и на перемещение нельзя пропустить номенклатуру и выполнить частичную комплектацию.</span><span class="sxs-lookup"><span data-stu-id="40a63-146">For sales and transfer orders, you can't skip items and do partial picking.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="40a63-147">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="40a63-147">Issue resolution</span></span>

<span data-ttu-id="40a63-148">На странице **Пункты меню мобильного устройства** для каждого пункта меню, настроенного для обработки заказов на продажу или заказов на перемещение, установите для параметра **Разрешить разделение работы** на экспресс-вкладке **Общие** значение *Да*.</span><span class="sxs-lookup"><span data-stu-id="40a63-148">On the **Mobile device menu items** page, for each menu item that is set up to process sales orders or transfer orders, set the **Allow splitting of work** option on the **General** FastTab to *Yes*.</span></span>

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a><span data-ttu-id="40a63-149">Как можно изменить статус складских запасов для работы с неполным объемом?</span><span class="sxs-lookup"><span data-stu-id="40a63-149">How can I do an inventory status change for partial quantity work?</span></span>

### <a name="issue-description"></a><span data-ttu-id="40a63-150">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="40a63-150">Issue description</span></span>

<span data-ttu-id="40a63-151">Вы хотите изменить статус запасов для неполного количества партии.</span><span class="sxs-lookup"><span data-stu-id="40a63-151">You want to do an inventory status change for a partial quantity of a batch.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="40a63-152">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="40a63-152">Issue resolution</span></span>

<span data-ttu-id="40a63-153">Чтобы разрешить работникам выполнять это изменение, можно создать пункт меню для приложения склада.</span><span class="sxs-lookup"><span data-stu-id="40a63-153">To enable workers to make this change, you can create a menu item for the warehouse app.</span></span> <span data-ttu-id="40a63-154">На странице **Пункты меню мобильного устройства** создайте (или измените) пункт меню, который имеет следующие настройки:</span><span class="sxs-lookup"><span data-stu-id="40a63-154">On the **Mobile device menu items** page, create (or edit) a menu item that has the following settings:</span></span>

- <span data-ttu-id="40a63-155">**Режим:** *Работа*</span><span class="sxs-lookup"><span data-stu-id="40a63-155">**Mode:** *Work*</span></span>
- <span data-ttu-id="40a63-156">**Использовать существующую работу:** *Нет*</span><span class="sxs-lookup"><span data-stu-id="40a63-156">**Use existing work:** *No*</span></span>
- <span data-ttu-id="40a63-157">**Процесс создания работы:** *Перемещение*</span><span class="sxs-lookup"><span data-stu-id="40a63-157">**Work creation process:** *Movement*</span></span>
- <span data-ttu-id="40a63-158">**Показать статус запасов:** *Да*</span><span class="sxs-lookup"><span data-stu-id="40a63-158">**Display inventory status:** *Yes*</span></span>

<span data-ttu-id="40a63-159">При необходимости на этой странице можно настроить другие поля.</span><span class="sxs-lookup"><span data-stu-id="40a63-159">You can set other fields on the page as you require.</span></span>
