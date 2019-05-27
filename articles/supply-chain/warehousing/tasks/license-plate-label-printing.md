---
title: Включение печати меток грузомест
description: Эта процедура позволяет автоматически печатать этикетку с кодом SSCC после комплектации последней номенклатуры из запасов в процессе работы комплектации для продаж.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d906ca9f5a6536870fa0c322a0792ed5672c25e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558111"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="84d69-103">Включение печати меток грузомест</span><span class="sxs-lookup"><span data-stu-id="84d69-103">Enable license plate label printing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="84d69-104">Эта процедура позволяет автоматически печатать этикетку с кодом SSCC после комплектации последней номенклатуры из запасов в процессе работы комплектации для продаж.</span><span class="sxs-lookup"><span data-stu-id="84d69-104">This procedure enables the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="84d69-105">Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="84d69-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="84d69-106">При выполнении этой процедуры с использованием собственных данных необходимо настроить номерную серию для номерных знаков.</span><span class="sxs-lookup"><span data-stu-id="84d69-106">If you’re run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="84d69-107">Необходимо настроить принтер этикеток перед началом этой задачи.</span><span class="sxs-lookup"><span data-stu-id="84d69-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="84d69-108">Перейдите в раздел "Управление организацией" > "Настройка" > "Сетевые принтеры".</span><span class="sxs-lookup"><span data-stu-id="84d69-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="84d69-109">В области действий щелкните "Параметры" и нажмите кнопку "Загрузить установщик агента маршрутизации документов".</span><span class="sxs-lookup"><span data-stu-id="84d69-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="84d69-110">Запустите установщик и убедитесь, что сетевой принтер работает и для него задано значение "Активно", прежде чем продолжить выполнение процедуры.</span><span class="sxs-lookup"><span data-stu-id="84d69-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="84d69-111">Настройка префикса компании GS1</span><span class="sxs-lookup"><span data-stu-id="84d69-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="84d69-112">Перейдите в раздел "Управление складом" > "Настройка" > "Параметры управления складом".</span><span class="sxs-lookup"><span data-stu-id="84d69-112">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="84d69-113">В поле "Префикс компании GS1" введите 7 чисел для номера компании GS1.</span><span class="sxs-lookup"><span data-stu-id="84d69-113">In the GS1 company prefix field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="84d69-114">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="84d69-114">Click Save.</span></span>
4. <span data-ttu-id="84d69-115">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="84d69-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="84d69-116">Настройка номерной серии номерного знака SSCC</span><span class="sxs-lookup"><span data-stu-id="84d69-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="84d69-117">Перейдите в раздел "Управление организацией" > "Номерные серии" > "Номерные серии".</span><span class="sxs-lookup"><span data-stu-id="84d69-117">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="84d69-118">В поле "Область" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="84d69-118">In the Area field, select an option.</span></span>
3. <span data-ttu-id="84d69-119">В поле "Ссылка" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="84d69-119">In the Reference field, select an option.</span></span>
4. <span data-ttu-id="84d69-120">В поле "Компания" введите значение.</span><span class="sxs-lookup"><span data-stu-id="84d69-120">In the Company field, type a value.</span></span>
5. <span data-ttu-id="84d69-121">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="84d69-121">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="84d69-122">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="84d69-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="84d69-123">Разверните раздел "Сегменты".</span><span class="sxs-lookup"><span data-stu-id="84d69-123">Expand the Segments section.</span></span>
8. <span data-ttu-id="84d69-124">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="84d69-124">Click Edit.</span></span>
9. <span data-ttu-id="84d69-125">В таблице "Сегменты" выберите первую строку.</span><span class="sxs-lookup"><span data-stu-id="84d69-125">In the Segments table, select the first row</span></span>
10. <span data-ttu-id="84d69-126">Щелкните "Удалить".</span><span class="sxs-lookup"><span data-stu-id="84d69-126">Click Remove.</span></span>
11. <span data-ttu-id="84d69-127">Щелкните "Удалить".</span><span class="sxs-lookup"><span data-stu-id="84d69-127">Click Remove.</span></span>
12. <span data-ttu-id="84d69-128">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="84d69-128">Click Save.</span></span>
13. <span data-ttu-id="84d69-129">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="84d69-129">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="84d69-130">Создание макета маршрута документа</span><span class="sxs-lookup"><span data-stu-id="84d69-130">Create the document route layout</span></span>
1. <span data-ttu-id="84d69-131">Перейдите в раздел "Управление складом" > "Настройка" > "Маршрутизация документов" > "Форматы маршрутизации документов".</span><span class="sxs-lookup"><span data-stu-id="84d69-131">Go to Warehouse management > Setup > Document routing > Document routing layouts.</span></span>
    * <span data-ttu-id="84d69-132">Включите макет SSCC.</span><span class="sxs-lookup"><span data-stu-id="84d69-132">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="84d69-133">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="84d69-133">Click New.</span></span>
3. <span data-ttu-id="84d69-134">В поле "Код макета" введите значение.</span><span class="sxs-lookup"><span data-stu-id="84d69-134">In the Layout ID field, type a value.</span></span>
4. <span data-ttu-id="84d69-135">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="84d69-135">In the Description field, type a value.</span></span>
5. <span data-ttu-id="84d69-136">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="84d69-136">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="84d69-137">Щелкните "Вставить в конце текста".</span><span class="sxs-lookup"><span data-stu-id="84d69-137">Click Insert at end of text.</span></span>
7. <span data-ttu-id="84d69-138">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="84d69-138">Click Save.</span></span>
8. <span data-ttu-id="84d69-139">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="84d69-139">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="84d69-140">Настройка маршрутизации документов</span><span class="sxs-lookup"><span data-stu-id="84d69-140">Set up the document routing</span></span>
1. <span data-ttu-id="84d69-141">Перейдите в раздел "Управление складом" > "Настройка" > "Маршрутизация документов" > "Маршрутизация документов".</span><span class="sxs-lookup"><span data-stu-id="84d69-141">Go to Warehouse management > Setup > Document routing > Document routing.</span></span>
2. <span data-ttu-id="84d69-142">В поле "Тип заказа на выполнение работ" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="84d69-142">In the Work order type field, select an option.</span></span>
3. <span data-ttu-id="84d69-143">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="84d69-143">Click New.</span></span>
4. <span data-ttu-id="84d69-144">В поле "Склад" введите значение.</span><span class="sxs-lookup"><span data-stu-id="84d69-144">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="84d69-145">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="84d69-145">In the Name field, type a value.</span></span>
6. <span data-ttu-id="84d69-146">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="84d69-146">Click New.</span></span>
7. <span data-ttu-id="84d69-147">В поле "Код макета" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="84d69-147">In the Layout ID field, enter or select a value.</span></span>
8. <span data-ttu-id="84d69-148">В поле "Имя" введите имя принтера, который необходимо использовать.</span><span class="sxs-lookup"><span data-stu-id="84d69-148">In the Name field, enter the printer name that you want to use..</span></span>
9. <span data-ttu-id="84d69-149">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="84d69-149">Click Save.</span></span>
10. <span data-ttu-id="84d69-150">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="84d69-150">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="84d69-151">Создание меню мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="84d69-151">Create mobile device menu</span></span>
1. <span data-ttu-id="84d69-152">Перейдите в раздел "Управление складом" > "Настройка" > "Мобильное устройство" > "Пункты меню мобильного устройства".</span><span class="sxs-lookup"><span data-stu-id="84d69-152">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="84d69-153">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="84d69-153">Click New.</span></span>
3. <span data-ttu-id="84d69-154">В поле "Имя пункта меню" введите значение.</span><span class="sxs-lookup"><span data-stu-id="84d69-154">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="84d69-155">В поле "Заголовок" введите значение.</span><span class="sxs-lookup"><span data-stu-id="84d69-155">In the Title field, type a value.</span></span>
5. <span data-ttu-id="84d69-156">В поле "Режим" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="84d69-156">In the Mode field, select an option.</span></span>
6. <span data-ttu-id="84d69-157">Выберите значение "Да" в поле "Использовать существующую работу".</span><span class="sxs-lookup"><span data-stu-id="84d69-157">Select Yes in the Use existing work field.</span></span>
7. <span data-ttu-id="84d69-158">Выберите значение "Да" в поле "Создать номерной знак".</span><span class="sxs-lookup"><span data-stu-id="84d69-158">Select Yes in the Generate license plate field.</span></span>
8. <span data-ttu-id="84d69-159">Разверните раздел "Классы работы".</span><span class="sxs-lookup"><span data-stu-id="84d69-159">Expand the Work classes section.</span></span>
9. <span data-ttu-id="84d69-160">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="84d69-160">Click New.</span></span>
10. <span data-ttu-id="84d69-161">В поле "Код класса работы" введите значение.</span><span class="sxs-lookup"><span data-stu-id="84d69-161">In the Work class ID field, type a value.</span></span>
11. <span data-ttu-id="84d69-162">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="84d69-162">Click Save.</span></span>
12. <span data-ttu-id="84d69-163">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="84d69-163">Close the page.</span></span>
13. <span data-ttu-id="84d69-164">Перейдите в раздел "Управление складом" > "Настройка" > "Мобильное устройство" > "Меню мобильного устройства".</span><span class="sxs-lookup"><span data-stu-id="84d69-164">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
14. <span data-ttu-id="84d69-165">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="84d69-165">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="84d69-166">В дереве выберите "В дереве выберите пункт меню, созданный ранее".</span><span class="sxs-lookup"><span data-stu-id="84d69-166">In the tree, select 'In the tree, select the menu item that you created before.'.</span></span>
16. <span data-ttu-id="84d69-167">Выберите Изменить.</span><span class="sxs-lookup"><span data-stu-id="84d69-167">Click Edit.</span></span>
17. <span data-ttu-id="84d69-168">Щелкните стрелку для добавления пункта меню в меню.</span><span class="sxs-lookup"><span data-stu-id="84d69-168">Click on the arrow to add the menu item to the menu.</span></span>
18. <span data-ttu-id="84d69-169">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="84d69-169">Click Save.</span></span>
19. <span data-ttu-id="84d69-170">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="84d69-170">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="84d69-171">Обновление шаблона работы</span><span class="sxs-lookup"><span data-stu-id="84d69-171">Update a work template</span></span>
1. <span data-ttu-id="84d69-172">Перейдите в раздел "Управление складом" > "Настройка" > "Работа" > "Шаблоны работ".</span><span class="sxs-lookup"><span data-stu-id="84d69-172">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="84d69-173">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="84d69-173">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="84d69-174">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="84d69-174">Click Edit.</span></span>
4. <span data-ttu-id="84d69-175">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="84d69-175">Click New.</span></span>
5. <span data-ttu-id="84d69-176">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="84d69-176">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="84d69-177">В поле "Тип работы" выберите "Печать".</span><span class="sxs-lookup"><span data-stu-id="84d69-177">In the Work type field, select 'Print'.</span></span>
7. <span data-ttu-id="84d69-178">В поле "Код класса работы" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="84d69-178">In the Work class ID field, enter or select a value.</span></span>
8. <span data-ttu-id="84d69-179">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="84d69-179">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="84d69-180">Щелкните "Переместить вверх".</span><span class="sxs-lookup"><span data-stu-id="84d69-180">Click Move up.</span></span>
10. <span data-ttu-id="84d69-181">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="84d69-181">Click Save.</span></span>
11. <span data-ttu-id="84d69-182">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="84d69-182">Close the page.</span></span>

