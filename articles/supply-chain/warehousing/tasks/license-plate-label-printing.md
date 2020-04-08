---
title: Включение печати меток грузомест
description: В этой теме показано, как включить автоматическую печать этикетки с кодом SSCC после комплектации последней номенклатуры из запасов в процессе работы комплектации для продаж.
author: perlynne
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 545f1c15888bcd0b46e1028f58cbe3a274846c92
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146039"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="1e775-103">Включение печати меток грузомест</span><span class="sxs-lookup"><span data-stu-id="1e775-103">Enable license plate label printing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1e775-104">В этой теме показано, как включить автоматическую печать этикетки с кодом SSCC после комплектации последней номенклатуры из запасов в процессе работы комплектации для продаж.</span><span class="sxs-lookup"><span data-stu-id="1e775-104">This topic shows how to enable the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="1e775-105">Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="1e775-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="1e775-106">При выполнении этой процедуры с использованием собственных данных необходимо настроить номерную серию для номерных знаков.</span><span class="sxs-lookup"><span data-stu-id="1e775-106">If you're run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="1e775-107">Необходимо настроить принтер этикеток перед началом этой задачи.</span><span class="sxs-lookup"><span data-stu-id="1e775-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="1e775-108">Перейдите в раздел "Управление организацией" > "Настройка" > "Сетевые принтеры".</span><span class="sxs-lookup"><span data-stu-id="1e775-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="1e775-109">В области действий щелкните "Параметры" и нажмите кнопку "Загрузить установщик агента маршрутизации документов".</span><span class="sxs-lookup"><span data-stu-id="1e775-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="1e775-110">Запустите установщик и убедитесь, что сетевой принтер работает и для него задано значение "Активно", прежде чем продолжить выполнение процедуры.</span><span class="sxs-lookup"><span data-stu-id="1e775-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="1e775-111">Настройка префикса компании GS1</span><span class="sxs-lookup"><span data-stu-id="1e775-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="1e775-112">Перейдите в **Область перехода > Модули > Управление складом > Настройка > Параметры управления складом**.</span><span class="sxs-lookup"><span data-stu-id="1e775-112">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="1e775-113">В поле **Префикс компании GS1** введите 7 чисел для номера компании GS1.</span><span class="sxs-lookup"><span data-stu-id="1e775-113">In the **GS1 company prefix** field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="1e775-114">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1e775-114">Select **Save**.</span></span>
4. <span data-ttu-id="1e775-115">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1e775-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="1e775-116">Настройка номерной серии номерного знака SSCC</span><span class="sxs-lookup"><span data-stu-id="1e775-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="1e775-117">Перейдите к **Область перехода > Модули > Управление организацией > Номерные серии" > Номерные серии**.</span><span class="sxs-lookup"><span data-stu-id="1e775-117">Go to **Navigation pane > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="1e775-118">В поле **Область** выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="1e775-118">In the **Area** field, select an option.</span></span>
3. <span data-ttu-id="1e775-119">В поле **Ссылка** выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="1e775-119">In the **Reference** field, select an option.</span></span>
4. <span data-ttu-id="1e775-120">В поле **Компания** введите значение.</span><span class="sxs-lookup"><span data-stu-id="1e775-120">In the **Company** field, type a value.</span></span>
5. <span data-ttu-id="1e775-121">Разверните раздел **Сегменты**.</span><span class="sxs-lookup"><span data-stu-id="1e775-121">Expand the **Segments** section.</span></span>
6. <span data-ttu-id="1e775-122">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="1e775-122">Select **Edit**.</span></span>
7. <span data-ttu-id="1e775-123">В таблице **Сегменты** выберите первую строку.</span><span class="sxs-lookup"><span data-stu-id="1e775-123">In the **Segments** table, select the first row</span></span>
8. <span data-ttu-id="1e775-124">Выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="1e775-124">Select **Remove**.</span></span>
9. <span data-ttu-id="1e775-125">Выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="1e775-125">Select **Remove**.</span></span>
10. <span data-ttu-id="1e775-126">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1e775-126">Select **Save**.</span></span>
11. <span data-ttu-id="1e775-127">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1e775-127">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="1e775-128">Создание макета маршрута документа</span><span class="sxs-lookup"><span data-stu-id="1e775-128">Create the document route layout</span></span>
1. <span data-ttu-id="1e775-129">Выберите **Область переходов > Модули > Управление складом > Настройка > Маршрутизация документов > Форматы маршрутизации документов**.</span><span class="sxs-lookup"><span data-stu-id="1e775-129">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing layouts**.</span></span> <span data-ttu-id="1e775-130">Включите макет SSCC.</span><span class="sxs-lookup"><span data-stu-id="1e775-130">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="1e775-131">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="1e775-131">Select **New**.</span></span>
3. <span data-ttu-id="1e775-132">В поле **Код макета** введите значение.</span><span class="sxs-lookup"><span data-stu-id="1e775-132">In the **Layout ID** field, type a value.</span></span>
4. <span data-ttu-id="1e775-133">В поле **Описание** введите значение.</span><span class="sxs-lookup"><span data-stu-id="1e775-133">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="1e775-134">Выберите **Вставить в конце текста**.</span><span class="sxs-lookup"><span data-stu-id="1e775-134">Select **Insert at end of text**.</span></span>
6. <span data-ttu-id="1e775-135">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1e775-135">Select **Save**.</span></span>
7. <span data-ttu-id="1e775-136">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1e775-136">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="1e775-137">Настройка маршрутизации документов</span><span class="sxs-lookup"><span data-stu-id="1e775-137">Set up the document routing</span></span>
1. <span data-ttu-id="1e775-138">Выберите **Область переходов > Модули > Управление складом > Настройка > Маршрутизация документов > Маршрутизация документов**.</span><span class="sxs-lookup"><span data-stu-id="1e775-138">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing**.</span></span>
2. <span data-ttu-id="1e775-139">В поле **Тип заказа на работу** выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="1e775-139">In the **Work order type** field, select an option.</span></span>
3. <span data-ttu-id="1e775-140">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="1e775-140">Select **New**.</span></span>
4. <span data-ttu-id="1e775-141">В поле **Склад** введите значение.</span><span class="sxs-lookup"><span data-stu-id="1e775-141">In the **Warehouse** field, type a value.</span></span>
5. <span data-ttu-id="1e775-142">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="1e775-142">In the **Name** field, type a value.</span></span>
6. <span data-ttu-id="1e775-143">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="1e775-143">Select **New**.</span></span>
7. <span data-ttu-id="1e775-144">В поле **Код макета** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1e775-144">In the **Layout ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="1e775-145">В поле **Имя** введите имя принтера, который необходимо использовать.</span><span class="sxs-lookup"><span data-stu-id="1e775-145">In the **Name** field, enter the printer name that you want to use.</span></span>
9. <span data-ttu-id="1e775-146">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1e775-146">Select **Save**.</span></span>
10. <span data-ttu-id="1e775-147">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1e775-147">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="1e775-148">Создание меню мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="1e775-148">Create mobile device menu</span></span>
1. <span data-ttu-id="1e775-149">Выберите **Область переходов > Модули >Управление складом > Настройка > Мобильное устройство > Пункты меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="1e775-149">Go to **Navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="1e775-150">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="1e775-150">Select **New**.</span></span>
3. <span data-ttu-id="1e775-151">В поле **Имя пункта меню** введите значение.</span><span class="sxs-lookup"><span data-stu-id="1e775-151">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="1e775-152">В поле **Заголовок** введите значение.</span><span class="sxs-lookup"><span data-stu-id="1e775-152">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="1e775-153">В поле **Режим** выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="1e775-153">In the **Mode** field, select an option.</span></span>
6. <span data-ttu-id="1e775-154">Выберите значение **Да** в поле **Использовать существующую работу**.</span><span class="sxs-lookup"><span data-stu-id="1e775-154">Select **Yes** in the **Use existing work** field.</span></span>
7. <span data-ttu-id="1e775-155">Выберите значение **Да** в поле **Создать номерной знак**.</span><span class="sxs-lookup"><span data-stu-id="1e775-155">Select **Yes** in the **Generate license plate** field.</span></span>
8. <span data-ttu-id="1e775-156">Разверните раздел **Классы работы**.</span><span class="sxs-lookup"><span data-stu-id="1e775-156">Expand the **Work classes** section.</span></span>
9. <span data-ttu-id="1e775-157">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="1e775-157">Select **New**.</span></span>
10. <span data-ttu-id="1e775-158">В поле **Код класса работы** введите значение.</span><span class="sxs-lookup"><span data-stu-id="1e775-158">In the **Work class ID** field, type a value.</span></span>
11. <span data-ttu-id="1e775-159">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1e775-159">Select **Save**.</span></span>
12. <span data-ttu-id="1e775-160">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1e775-160">Close the page.</span></span>
13. <span data-ttu-id="1e775-161">Выберите **Область переходов > Модули >Управление складом > Настройка > Мобильное устройство > Меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="1e775-161">Go to **navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
14. <span data-ttu-id="1e775-162">В дереве выберите пункт меню, созданный ранее.</span><span class="sxs-lookup"><span data-stu-id="1e775-162">In the tree, select the menu item that you created before.</span></span>
15. <span data-ttu-id="1e775-163">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="1e775-163">Select **Edit**.</span></span>
16. <span data-ttu-id="1e775-164">Выберите стрелку для добавления элемента меню в меню.</span><span class="sxs-lookup"><span data-stu-id="1e775-164">Select the arrow to add the menu item to the menu.</span></span>
17. <span data-ttu-id="1e775-165">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1e775-165">Select **Save**.</span></span>
18. <span data-ttu-id="1e775-166">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1e775-166">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="1e775-167">Обновление шаблона работы</span><span class="sxs-lookup"><span data-stu-id="1e775-167">Update a work template</span></span>
1. <span data-ttu-id="1e775-168">Выберите **Область переходов > Модули > Управление складом > Настройка > Работа > Шаблоны работ**.</span><span class="sxs-lookup"><span data-stu-id="1e775-168">Go to **Navigation pane > Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="1e775-169">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="1e775-169">Select **Edit**.</span></span>
3. <span data-ttu-id="1e775-170">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="1e775-170">Select **New**.</span></span>
4. <span data-ttu-id="1e775-171">В поле **Тип работы** выберите **Печать**.</span><span class="sxs-lookup"><span data-stu-id="1e775-171">In the **Work type** field, select **Print**.</span></span>
5. <span data-ttu-id="1e775-172">В поле **Код класса работы** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="1e775-172">In the **Work class ID** field, enter or select a value.</span></span>
6. <span data-ttu-id="1e775-173">Выберите **Переместить вверх**.</span><span class="sxs-lookup"><span data-stu-id="1e775-173">Select **Move up**.</span></span>
7. <span data-ttu-id="1e775-174">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1e775-174">Select **Save**.</span></span>
8. <span data-ttu-id="1e775-175">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1e775-175">Close the page.</span></span>

