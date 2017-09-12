--- 
title: "Включение печати меток грузомест"
description: "Эта процедура позволяет автоматически печатать этикетку с кодом SSCC после комплектации последней номенклатуры из запасов в процессе работы комплектации для продаж."
author: perlynne
manager: AnnBe
ms.date: 11/03/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6d186bf7e4aee8cfa97adbd90b9090085e842f9b
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="0bbdf-103">Включение печати меток грузомест</span><span class="sxs-lookup"><span data-stu-id="0bbdf-103">Enable license plate label printing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0bbdf-104">Эта процедура позволяет автоматически печатать этикетку с кодом SSCC после комплектации последней номенклатуры из запасов в процессе работы комплектации для продаж.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-104">This procedure enables the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="0bbdf-105">Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="0bbdf-106">При выполнении этой процедуры с использованием собственных данных необходимо настроить номерную серию для номерных знаков.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-106">If you’re run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="0bbdf-107">Необходимо настроить принтер этикеток перед началом этой задачи.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="0bbdf-108">Перейдите в раздел "Управление организацией" > "Настройка" > "Сетевые принтеры".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="0bbdf-109">В области действий щелкните "Параметры" и нажмите кнопку "Загрузить установщик агента маршрутизации документов".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="0bbdf-110">Запустите установщик и убедитесь, что сетевой принтер работает и для него задано значение "Активно", прежде чем продолжить выполнение процедуры.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="0bbdf-111">Настройка префикса компании GS1</span><span class="sxs-lookup"><span data-stu-id="0bbdf-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="0bbdf-112">Перейдите в раздел "Управление складом" > "Настройка" > "Параметры управления складом".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-112">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="0bbdf-113">В поле "Префикс компании GS1" введите 7 чисел для номера компании GS1.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-113">In the GS1 company prefix field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="0bbdf-114">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-114">Click Save.</span></span>
4. <span data-ttu-id="0bbdf-115">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="0bbdf-116">Настройка номерной серии номерного знака SSCC</span><span class="sxs-lookup"><span data-stu-id="0bbdf-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="0bbdf-117">Перейдите в раздел "Управление организацией" > "Номерные серии" > "Номерные серии".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-117">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="0bbdf-118">В поле "Область" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-118">In the Area field, select an option.</span></span>
3. <span data-ttu-id="0bbdf-119">В поле "Ссылка" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-119">In the Reference field, select an option.</span></span>
4. <span data-ttu-id="0bbdf-120">В поле "Компания" введите значение.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-120">In the Company field, type a value.</span></span>
5. <span data-ttu-id="0bbdf-121">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-121">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="0bbdf-122">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="0bbdf-123">Разверните раздел "Сегменты".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-123">Expand the Segments section.</span></span>
8. <span data-ttu-id="0bbdf-124">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-124">Click Edit.</span></span>
9. <span data-ttu-id="0bbdf-125">В таблице "Сегменты" выберите первую строку.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-125">In the Segments table, select the first row</span></span>
10. <span data-ttu-id="0bbdf-126">Щелкните "Удалить".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-126">Click Remove.</span></span>
11. <span data-ttu-id="0bbdf-127">Щелкните "Удалить".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-127">Click Remove.</span></span>
12. <span data-ttu-id="0bbdf-128">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-128">Click Save.</span></span>
13. <span data-ttu-id="0bbdf-129">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-129">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="0bbdf-130">Создание макета маршрута документа</span><span class="sxs-lookup"><span data-stu-id="0bbdf-130">Create the document route layout</span></span>
1. <span data-ttu-id="0bbdf-131">Перейдите в раздел "Управление складом" > "Настройка" > "Маршрутизация документов" > "Форматы маршрутизации документов".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-131">Go to Warehouse management > Setup > Document routing > Document routing layouts.</span></span>
    * <span data-ttu-id="0bbdf-132">Включите макет SSCC.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-132">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="0bbdf-133">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-133">Click New.</span></span>
3. <span data-ttu-id="0bbdf-134">В поле "Код макета" введите значение.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-134">In the Layout ID field, type a value.</span></span>
4. <span data-ttu-id="0bbdf-135">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-135">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0bbdf-136">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-136">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="0bbdf-137">Щелкните "Вставить в конце текста".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-137">Click Insert at end of text.</span></span>
7. <span data-ttu-id="0bbdf-138">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-138">Click Save.</span></span>
8. <span data-ttu-id="0bbdf-139">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-139">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="0bbdf-140">Настройка маршрутизации документов</span><span class="sxs-lookup"><span data-stu-id="0bbdf-140">Set up the document routing</span></span>
1. <span data-ttu-id="0bbdf-141">Перейдите в раздел "Управление складом" > "Настройка" > "Маршрутизация документов" > "Маршрутизация документов".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-141">Go to Warehouse management > Setup > Document routing > Document routing.</span></span>
2. <span data-ttu-id="0bbdf-142">В поле "Тип заказа на выполнение работ" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-142">In the Work order type field, select an option.</span></span>
3. <span data-ttu-id="0bbdf-143">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-143">Click New.</span></span>
4. <span data-ttu-id="0bbdf-144">В поле "Склад" введите значение.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-144">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="0bbdf-145">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-145">In the Name field, type a value.</span></span>
6. <span data-ttu-id="0bbdf-146">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-146">Click New.</span></span>
7. <span data-ttu-id="0bbdf-147">В поле "Код макета" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-147">In the Layout ID field, enter or select a value.</span></span>
8. <span data-ttu-id="0bbdf-148">В поле "Имя" введите имя принтера, который необходимо использовать.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-148">In the Name field, enter the printer name that you want to use..</span></span>
9. <span data-ttu-id="0bbdf-149">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-149">Click Save.</span></span>
10. <span data-ttu-id="0bbdf-150">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-150">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="0bbdf-151">Создание меню мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="0bbdf-151">Create mobile device menu</span></span>
1. <span data-ttu-id="0bbdf-152">Перейдите в раздел "Управление складом" > "Настройка" > "Мобильное устройство" > "Пункты меню мобильного устройства".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-152">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="0bbdf-153">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-153">Click New.</span></span>
3. <span data-ttu-id="0bbdf-154">В поле "Имя пункта меню" введите значение.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-154">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="0bbdf-155">В поле "Заголовок" введите значение.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-155">In the Title field, type a value.</span></span>
5. <span data-ttu-id="0bbdf-156">В поле "Режим" выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-156">In the Mode field, select an option.</span></span>
6. <span data-ttu-id="0bbdf-157">Выберите значение "Да" в поле "Использовать существующую работу".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-157">Select Yes in the Use existing work field.</span></span>
7. <span data-ttu-id="0bbdf-158">Выберите значение "Да" в поле "Создать номерной знак".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-158">Select Yes in the Generate license plate field.</span></span>
8. <span data-ttu-id="0bbdf-159">Разверните раздел "Классы работы".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-159">Expand the Work classes section.</span></span>
9. <span data-ttu-id="0bbdf-160">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-160">Click New.</span></span>
10. <span data-ttu-id="0bbdf-161">В поле "Код класса работы" введите значение.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-161">In the Work class ID field, type a value.</span></span>
11. <span data-ttu-id="0bbdf-162">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-162">Click Save.</span></span>
12. <span data-ttu-id="0bbdf-163">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-163">Close the page.</span></span>
13. <span data-ttu-id="0bbdf-164">Перейдите в раздел "Управление складом" > "Настройка" > "Мобильное устройство" > "Меню мобильного устройства".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-164">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
14. <span data-ttu-id="0bbdf-165">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-165">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="0bbdf-166">В дереве выберите "В дереве выберите пункт меню, созданный ранее".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-166">In the tree, select 'In the tree, select the menu item that you created before.'.</span></span>
16. <span data-ttu-id="0bbdf-167">Выберите Изменить.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-167">Click Edit.</span></span>
17. <span data-ttu-id="0bbdf-168">Щелкните стрелку для добавления пункта меню в меню.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-168">Click on the arrow to add the menu item to the menu.</span></span>
18. <span data-ttu-id="0bbdf-169">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-169">Click Save.</span></span>
19. <span data-ttu-id="0bbdf-170">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-170">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="0bbdf-171">Обновление шаблона работы</span><span class="sxs-lookup"><span data-stu-id="0bbdf-171">Update a work template</span></span>
1. <span data-ttu-id="0bbdf-172">Перейдите в раздел "Управление складом" > "Настройка" > "Работа" > "Шаблоны работ".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-172">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="0bbdf-173">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-173">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="0bbdf-174">Щелкните "Изменить".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-174">Click Edit.</span></span>
4. <span data-ttu-id="0bbdf-175">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-175">Click New.</span></span>
5. <span data-ttu-id="0bbdf-176">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-176">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="0bbdf-177">В поле "Тип работы" выберите "Печать".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-177">In the Work type field, select 'Print'.</span></span>
7. <span data-ttu-id="0bbdf-178">В поле "Код класса работы" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-178">In the Work class ID field, enter or select a value.</span></span>
8. <span data-ttu-id="0bbdf-179">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-179">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="0bbdf-180">Щелкните "Переместить вверх".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-180">Click Move up.</span></span>
10. <span data-ttu-id="0bbdf-181">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="0bbdf-181">Click Save.</span></span>
11. <span data-ttu-id="0bbdf-182">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="0bbdf-182">Close the page.</span></span>


