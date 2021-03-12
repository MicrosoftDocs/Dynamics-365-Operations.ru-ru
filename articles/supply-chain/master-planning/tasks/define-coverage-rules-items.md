---
title: Определение правил покрытия для номенклатур
description: В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.
author: ShylaThompson
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c156ae4a8a19a428378581a0d5c7dc01d86b5ec7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999889"
---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="d7b90-103">Определение правил покрытия для номенклатур</span><span class="sxs-lookup"><span data-stu-id="d7b90-103">Define coverage rules for items</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d7b90-104">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="d7b90-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d7b90-105">В этой процедуре показано, как создать правила покрытия и переопределить параметры покрытия для определенной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="d7b90-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="d7b90-106">В ней также показано, как задать параметры запасов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d7b90-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="d7b90-107">Создание группы покрытия</span><span class="sxs-lookup"><span data-stu-id="d7b90-107">Create a coverage group</span></span>
1. <span data-ttu-id="d7b90-108">Выберите **Область переходов > Модули > Сводное планирование > Настройка > Группы покрытия**.</span><span class="sxs-lookup"><span data-stu-id="d7b90-108">Go to **Navigation pane > Modules > Master planning > Setup > Coverage groups**.</span></span>
2. <span data-ttu-id="d7b90-109">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d7b90-109">Click **New**.</span></span>
3. <span data-ttu-id="d7b90-110">В поле **Группа покрытия** введите значение.</span><span class="sxs-lookup"><span data-stu-id="d7b90-110">In the **Coverage group** field, type a value.</span></span>
4. <span data-ttu-id="d7b90-111">В поле **Имя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="d7b90-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="d7b90-112">В поле **Календарь** введите значение.</span><span class="sxs-lookup"><span data-stu-id="d7b90-112">In the **Calendar** field, type a value.</span></span> <span data-ttu-id="d7b90-113">Выберите календарь, который будет использоваться при сводном планировании для создания предложений пополнения для номенклатур в этой группе.</span><span class="sxs-lookup"><span data-stu-id="d7b90-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="d7b90-114">В поле **Код покрытия** выберите один из вариантов.</span><span class="sxs-lookup"><span data-stu-id="d7b90-114">In the **Coverage code** field, select an option.</span></span> <span data-ttu-id="d7b90-115">Для этой процедуры выберите "Потребность".</span><span class="sxs-lookup"><span data-stu-id="d7b90-115">Select 'Requirement' for this procedure.</span></span>  
7. <span data-ttu-id="d7b90-116">В поле **Временная граница покрытия (в днях)** введите значение "90".</span><span class="sxs-lookup"><span data-stu-id="d7b90-116">In the **Coverage time fence (days) field**, enter '90'.</span></span> <span data-ttu-id="d7b90-117">Для номенклатур в этой группе при сводном планировании будут созданы предложения пополнения на 90 дней вперед.</span><span class="sxs-lookup"><span data-stu-id="d7b90-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="d7b90-118">В поле **Отрицательные дни** введите значение "1".</span><span class="sxs-lookup"><span data-stu-id="d7b90-118">In the **Negative days** field, enter '1'.</span></span>
9. <span data-ttu-id="d7b90-119">В поле **Положительные дни** введите значение "1".</span><span class="sxs-lookup"><span data-stu-id="d7b90-119">In the **Positive days** field, enter '1'.</span></span>
10. <span data-ttu-id="d7b90-120">Разверните или сверните раздел **Прочее**.</span><span class="sxs-lookup"><span data-stu-id="d7b90-120">Expand or collapse the **Other** section.</span></span>
11. <span data-ttu-id="d7b90-121">В разделе **Резервное время в днях** в поле **Резервное время для поступления, добавленное к дате потребности** введите "1".</span><span class="sxs-lookup"><span data-stu-id="d7b90-121">Under the **Safety margins in days** section, in the **Receipt margin added to requirement date** field, enter '1'.</span></span> <span data-ttu-id="d7b90-122">Например, если для поступления указано резервное время 1 день, а поступление по строке заказа на покупку запланировано на 15 мая, в сводном планировании будет указана скорректированная дата поступления 16 марта.</span><span class="sxs-lookup"><span data-stu-id="d7b90-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="d7b90-123">В поле **Резервное время для расхода, вычтенное из даты потребности** введите значение "1".</span><span class="sxs-lookup"><span data-stu-id="d7b90-123">In the **Issue margin deducted from requirement date** field, enter '1'.</span></span> <span data-ttu-id="d7b90-124">Например, если указано резервное время 1 день, а поставка по строке заказа на продажу запланирована на 15 мая, в сводном планировании будет указана скорректированная дата поставки 14 мая.</span><span class="sxs-lookup"><span data-stu-id="d7b90-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="d7b90-125">В поле **Резервное время для повторного заказа, добавленное ко времени упреждения для номенклатуры** введите значение "1".</span><span class="sxs-lookup"><span data-stu-id="d7b90-125">In the **Reorder margin added to item lead time** field, enter '1'.</span></span>
14. <span data-ttu-id="d7b90-126">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d7b90-126">Click **Save**.</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="d7b90-127">Создание нового продукта</span><span class="sxs-lookup"><span data-stu-id="d7b90-127">Create a new product</span></span>
1. <span data-ttu-id="d7b90-128">Перейдите в раздел **Область переходов > Модули > Управление сведениями о продукте > Продукты > Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="d7b90-128">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="d7b90-129">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d7b90-129">Click **New**.</span></span>
3. <span data-ttu-id="d7b90-130">В поле **Номер продукта** введите значение.</span><span class="sxs-lookup"><span data-stu-id="d7b90-130">In the **Product number** field, type a value.</span></span>
4. <span data-ttu-id="d7b90-131">В поле **Имя продукта** введите значение.</span><span class="sxs-lookup"><span data-stu-id="d7b90-131">In the **Product name** field, type a value.</span></span>
5. <span data-ttu-id="d7b90-132">В поле **Группа номенклатурных моделей** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="d7b90-132">In the **Item model group** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="d7b90-133">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="d7b90-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="d7b90-134">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="d7b90-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="d7b90-135">В поле **Номенклатурная группа** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="d7b90-135">In the **Item group** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="d7b90-136">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="d7b90-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="d7b90-137">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="d7b90-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="d7b90-138">В поле **Группа аналитик хранения** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="d7b90-138">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="d7b90-139">Поиск и выбор требуемой записи в списке.</span><span class="sxs-lookup"><span data-stu-id="d7b90-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="d7b90-140">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="d7b90-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="d7b90-141">В поле **Группа аналитик отслеживания** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="d7b90-141">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="d7b90-142">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="d7b90-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="d7b90-143">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="d7b90-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="d7b90-144">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="d7b90-144">Click **OK**.</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="d7b90-145">Настройка параметров заказов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d7b90-145">Setup default order settings</span></span>
1. <span data-ttu-id="d7b90-146">В области **Панель операций** щелкните **План**.</span><span class="sxs-lookup"><span data-stu-id="d7b90-146">On the **Action Pane**, click **Plan**.</span></span>
2. <span data-ttu-id="d7b90-147">В разделе **Настройки заказа** щелкните **Параметры заказа по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="d7b90-147">Under **Order settings**, click **Default order settings**.</span></span>
3. <span data-ttu-id="d7b90-148">В разделе **Заказ на покупку** в поле **Сайт по умолчанию** введите сайт, используемый по умолчанию при создании заказов на покупку.</span><span class="sxs-lookup"><span data-stu-id="d7b90-148">Under **Purchase order**, in the **Default site** field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="d7b90-149">В поле **Склад по умолчанию** введите сайт, где хранится номенклатура.</span><span class="sxs-lookup"><span data-stu-id="d7b90-149">In the **Default warehouse** field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="d7b90-150">Разверните или сверните раздел **Запасы**.</span><span class="sxs-lookup"><span data-stu-id="d7b90-150">Expand or collapse the **Inventory** section.</span></span>
6. <span data-ttu-id="d7b90-151">В поле **Кратность** введите ''10".</span><span class="sxs-lookup"><span data-stu-id="d7b90-151">In the **Multiple** field, type '10'.</span></span>
7. <span data-ttu-id="d7b90-152">В поле **Мин. количество по заказу** введите "10".</span><span class="sxs-lookup"><span data-stu-id="d7b90-152">In the **Min. order quantity** field, type '10'.</span></span>
8. <span data-ttu-id="d7b90-153">В поле **Макс. количество по заказу** введите "100".</span><span class="sxs-lookup"><span data-stu-id="d7b90-153">In the **Max. order quantity** field, type '100'.</span></span>
9. <span data-ttu-id="d7b90-154">В поле **Стандартное количество заказа** введите "10".</span><span class="sxs-lookup"><span data-stu-id="d7b90-154">In the **Standard order quantity**, type '10'.</span></span>
10. <span data-ttu-id="d7b90-155">В поле **Время упреждения покупки** введите число.</span><span class="sxs-lookup"><span data-stu-id="d7b90-155">In the **Purchase lead time** field, enter a number.</span></span>
11. <span data-ttu-id="d7b90-156">Установите или снимите флажок **Рабочие дни**.</span><span class="sxs-lookup"><span data-stu-id="d7b90-156">Select or clear the **Working days** check box.</span></span>
12. <span data-ttu-id="d7b90-157">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d7b90-157">Click **Save**.</span></span>
13. <span data-ttu-id="d7b90-158">В поле **Тип заказа по умолчанию** выберите "Заказ на покупку".</span><span class="sxs-lookup"><span data-stu-id="d7b90-158">In the **Default order type** field select 'Purchase order'.</span></span>
14. <span data-ttu-id="d7b90-159">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d7b90-159">Click **Save**.</span></span>
15. <span data-ttu-id="d7b90-160">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="d7b90-160">Close the page.</span></span> <span data-ttu-id="d7b90-161">Закройте страницу "Параметры заказа по умолчанию".</span><span class="sxs-lookup"><span data-stu-id="d7b90-161">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="d7b90-162">Добавление номенклатуры в группу покрытия</span><span class="sxs-lookup"><span data-stu-id="d7b90-162">Add an item to a coverage group</span></span>
1. <span data-ttu-id="d7b90-163">Разверните или сверните раздел **План**.</span><span class="sxs-lookup"><span data-stu-id="d7b90-163">Expand or collapse the **Plan** section.</span></span>
2. <span data-ttu-id="d7b90-164">В поле **Группа покрытия** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="d7b90-164">In the **Coverage group** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="d7b90-165">В списке найдите созданный объект **Группа покрытия**.</span><span class="sxs-lookup"><span data-stu-id="d7b90-165">In the list, find the **Coverage group** you have created.</span></span>
4. <span data-ttu-id="d7b90-166">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="d7b90-166">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="d7b90-167">Создание правил покрытия номенклатуры</span><span class="sxs-lookup"><span data-stu-id="d7b90-167">Create item coverage rules</span></span>
1. <span data-ttu-id="d7b90-168">В области **Панель операций** щелкните **План**.</span><span class="sxs-lookup"><span data-stu-id="d7b90-168">On the **Action Pane**, click **Plan**.</span></span>
2. <span data-ttu-id="d7b90-169">В разделе **Покрытие** щелкните **Покрытие номенклатуры**.</span><span class="sxs-lookup"><span data-stu-id="d7b90-169">Under **Coverage**, click **Item coverage**.</span></span>
3. <span data-ttu-id="d7b90-170">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d7b90-170">Click **New**.</span></span>
4. <span data-ttu-id="d7b90-171">Перейдите на вкладку **Общие**.</span><span class="sxs-lookup"><span data-stu-id="d7b90-171">Click the **General** tab.</span></span>
5. <span data-ttu-id="d7b90-172">Установите флажок в заголовке **Переопределить параметры группы покрытия**.</span><span class="sxs-lookup"><span data-stu-id="d7b90-172">Check the box on the header of **Override coverage group** settings.</span></span>
6. <span data-ttu-id="d7b90-173">В поле **Временная граница покрытия (в днях)** введите значение "60".</span><span class="sxs-lookup"><span data-stu-id="d7b90-173">In the **Coverage time fence (days)** field, enter '60'.</span></span> <span data-ttu-id="d7b90-174">Хотя номенклатуры в поле "Потребность" группы покрытия запланированы на 90 дней вперед, эта номенклатура будет планироваться на 60 дней вперед.</span><span class="sxs-lookup"><span data-stu-id="d7b90-174">Although items in coverage group Requiremen are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="d7b90-175">В поле **Отрицательные дни** введите значение "2".</span><span class="sxs-lookup"><span data-stu-id="d7b90-175">In the **Negative days** field, enter '2'.</span></span>
8. <span data-ttu-id="d7b90-176">В поле **Положительные дни** введите значение "2".</span><span class="sxs-lookup"><span data-stu-id="d7b90-176">In the **Positive days** field, enter '2'.</span></span>
9. <span data-ttu-id="d7b90-177">Перейдите на вкладку **Время упреждения**.</span><span class="sxs-lookup"><span data-stu-id="d7b90-177">Click the **Lead time** tab.</span></span>
10. <span data-ttu-id="d7b90-178">Установите флажок в заголовке **Покупка**.</span><span class="sxs-lookup"><span data-stu-id="d7b90-178">Check the box on the header of **Purchase**.</span></span>
11. <span data-ttu-id="d7b90-179">В поле **Время покупки** введите значение "5".</span><span class="sxs-lookup"><span data-stu-id="d7b90-179">In the **Purchase time** field, enter '5'.</span></span>
12. <span data-ttu-id="d7b90-180">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d7b90-180">Click **Save**.</span></span>

