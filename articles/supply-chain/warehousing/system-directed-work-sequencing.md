---
title: Последовательность работ, управляемая системой
description: В этом разделе приводятся сведения о последовательности работ, управляемой системой. Эта функция позволяет отсортировать и отфильтровать заказы на работу, предоставляемые пользователям системой для выполнения. Это полезно в тех случаях, когда для процесса складской комплектации требуются дополнительные критерии.
author: Mirzaab
manager: tfehr
ms.date: 07/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-03
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 2884c480d20090266f7cffb5e7d0aca58c1174f0
ms.sourcegitcommit: edb46dce498df42b09e8f5ad6de00f86c8022dfa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/03/2020
ms.locfileid: "3534858"
---
# <a name="system-directed-work-sequencing"></a><span data-ttu-id="58ad7-105">Последовательность работ, управляемая системой</span><span class="sxs-lookup"><span data-stu-id="58ad7-105">System-directed work sequencing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="58ad7-106">Последовательность работ, управляемая системой, позволяет отсортировать и отфильтровать заказы на работу, предоставляемые пользователям системой для выполнения.</span><span class="sxs-lookup"><span data-stu-id="58ad7-106">System-directed work sequencing lets you sort and filter the work orders that the system presents to users for execution.</span></span> <span data-ttu-id="58ad7-107">Это полезно в ситуациях, когда для обработки складской комплектации требуются дополнительные критерии (например, время отгрузки, зона комплектации, профиль местоположения или сочетание различных критериев).</span><span class="sxs-lookup"><span data-stu-id="58ad7-107">It's helpful in scenarios where additional criteria (such as the time of shipping, the picking zone, the location profile, or a combination of various criteria) are required to drive the warehouse picking process.</span></span>

<span data-ttu-id="58ad7-108">Эта функция расширяет возможности текущей управляемой системой комплектации путем добавления управляемого системой порядка запросов, где пользователи могут настроить последовательность и один или несколько запросов, которые будут оценивать все созданные заказы на работу.</span><span class="sxs-lookup"><span data-stu-id="58ad7-108">This functionality extends the current system-directed picking functionality by adding a system-directed query order, where users can set up a sequence and one or more queries that will evaluate all work orders that are created.</span></span> <span data-ttu-id="58ad7-109">Будут собраны и представлены только те заказы на работу, которые удовлетворяют критериям, указанным в настройке элемента меню мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="58ad7-109">Only work orders that meet the criteria that are specified in the setup of the mobile device menu item will be captured and presented.</span></span>

<span data-ttu-id="58ad7-110">Таким образом, эта функция позволяет дополнительно оптимизировать процессы комплектации склада, поскольку она определяет заказы на работу, которые соответствуют указанному критерию, назначает их для соответствующего пункта меню мобильного устройства, а затем предоставляет их работнику на основе определенного набора навыков, оборудования комплектации или другого требования.</span><span class="sxs-lookup"><span data-stu-id="58ad7-110">Therefore, this functionality allows for further optimization of warehouse picking processes as it identifies work orders that match the specified criteria, assigns them to the correct mobile device menu item, and then presents them to a worker, based on a specific skill set, picking equipment, or other requirement.</span></span>

> [!NOTE]
> <span data-ttu-id="58ad7-111">При необходимости использования других критериев необходимо использовать несколько пунктов меню мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="58ad7-111">If different criteria are needed, multiple mobile device menu items must be used.</span></span>

## <a name="turn-on-the-organization-wide-system-directed-work-sequencing-feature"></a><span data-ttu-id="58ad7-112">Включение функции последовательности работ под управлением системы во всей организации</span><span class="sxs-lookup"><span data-stu-id="58ad7-112">Turn on the Organization-wide system directed work sequencing feature</span></span>

<span data-ttu-id="58ad7-113">Прежде чем использовать последовательность работ, управляемую системой, эта функция должна быть включена в системе.</span><span class="sxs-lookup"><span data-stu-id="58ad7-113">Before you can use system-directed work sequencing, the feature must be turned on in your system.</span></span> <span data-ttu-id="58ad7-114">Администраторы могут использовать рабочую область [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения, если это требуется.</span><span class="sxs-lookup"><span data-stu-id="58ad7-114">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="58ad7-115">В этом случае функция указана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="58ad7-115">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="58ad7-116">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="58ad7-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="58ad7-117">**Имя функции:** *Последовательность работы под управлением системы во всей организации*</span><span class="sxs-lookup"><span data-stu-id="58ad7-117">**Feature name:** *Organization-wide system directed work sequencing*</span></span>

## <a name="setup"></a><span data-ttu-id="58ad7-118">Настройка</span><span class="sxs-lookup"><span data-stu-id="58ad7-118">Setup</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="58ad7-119">Сделать демонстрационные данные доступными</span><span class="sxs-lookup"><span data-stu-id="58ad7-119">Make demo data available</span></span>

<span data-ttu-id="58ad7-120">Для работы с этим сценарием с помощью значений, представленных в этой теме, следует работать с системой, в которой установлены стандартные демонстрационные данные.</span><span class="sxs-lookup"><span data-stu-id="58ad7-120">To work through the scenario by using the values that are presented in this topic, you must work on a system where the standard demo data is installed.</span></span> <span data-ttu-id="58ad7-121">Дополнительно необходимо выбрать юридическое лицо **USMF**.</span><span class="sxs-lookup"><span data-stu-id="58ad7-121">Additionally, you must select the **USMF** legal entity.</span></span> <span data-ttu-id="58ad7-122">В сценарии используется склад *51* из демонстрационных данных.</span><span class="sxs-lookup"><span data-stu-id="58ad7-122">The scenario uses warehouse *51* from the demo data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="58ad7-123">Перед тем, как выпустить заказы на склад, убедитесь, что в местах комплектации достаточно запасов для всех номенклатур по заказам.</span><span class="sxs-lookup"><span data-stu-id="58ad7-123">Before you release the orders to the warehouse, make sure that the pick locations have enough inventory for all the items on the orders.</span></span>
>
> <span data-ttu-id="58ad7-124">Этот сценарий должны поддерживать данные USMF по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="58ad7-124">Default USMF data should support this scenario.</span></span> <span data-ttu-id="58ad7-125">Если вы не используете демонстрационные данные, проверьте настройку **Директива местонахождения**, чтобы узнать, какие местонахождения комплектации используются для комплектации заказов на продажу.</span><span class="sxs-lookup"><span data-stu-id="58ad7-125">If you aren't using demo data, review the **Location directive** setting to learn which picking locations are used for sales order picking.</span></span> <span data-ttu-id="58ad7-126">Если необходимо скорректировать запасы, можно создать ручные перемещения, воспользуйтесь пополнением или используйте любой другой поток.</span><span class="sxs-lookup"><span data-stu-id="58ad7-126">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span>

### <a name="set-up-a-mobile-device-menu-item"></a><span data-ttu-id="58ad7-127">Настройка пункта меню мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="58ad7-127">Set up a mobile device menu item</span></span>

1. <span data-ttu-id="58ad7-128">Перейдите в раздел **Управление складом \> Настройка \> Мобильное устройство \> Пункты меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="58ad7-128">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="58ad7-129">В списке пунктов меню мобильного устройства выберите **Комплектация продаж — система**.</span><span class="sxs-lookup"><span data-stu-id="58ad7-129">In the list of mobile device menu items, select **Sales Picking – System**.</span></span> <span data-ttu-id="58ad7-130">Требуемый пункт меню уже должен существовать.</span><span class="sxs-lookup"><span data-stu-id="58ad7-130">The required menu item should already exist.</span></span> 
1. <span data-ttu-id="58ad7-131">Подтвердите следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="58ad7-131">Confirm the following settings:</span></span>

    - <span data-ttu-id="58ad7-132">На экспресс-вкладке **Общие** в поле **Кем управляется** должно быть указано *Управляется системой*.</span><span class="sxs-lookup"><span data-stu-id="58ad7-132">On the **General** FastTab, the **Directed by** field should be set to *System directed*.</span></span>
    - <span data-ttu-id="58ad7-133">На экспресс-вкладке **Классы работ** должны отображаться следующие настройки:</span><span class="sxs-lookup"><span data-stu-id="58ad7-133">The **Work classes** FastTab should show the following settings.</span></span>

        | <span data-ttu-id="58ad7-134">Код класса работы</span><span class="sxs-lookup"><span data-stu-id="58ad7-134">Work class ID</span></span> | <span data-ttu-id="58ad7-135">Тип заказа на выполнение работ</span><span class="sxs-lookup"><span data-stu-id="58ad7-135">Work order type</span></span> |
        |---|---|
        | <span data-ttu-id="58ad7-136">Sales</span><span class="sxs-lookup"><span data-stu-id="58ad7-136">Sales</span></span> | <span data-ttu-id="58ad7-137">Заказы на продажу</span><span class="sxs-lookup"><span data-stu-id="58ad7-137">Sales orders</span></span> |
        | <span data-ttu-id="58ad7-138">Комплектация заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="58ad7-138">SO Pick</span></span> | <span data-ttu-id="58ad7-139">Заказы на продажу</span><span class="sxs-lookup"><span data-stu-id="58ad7-139">Sales orders</span></span> |

1. <span data-ttu-id="58ad7-140">В области действий выберите **Запросы последовательности работы под управлением системы**.</span><span class="sxs-lookup"><span data-stu-id="58ad7-140">On the Action Pane, select **System directed work sequence queries**.</span></span>
1. <span data-ttu-id="58ad7-141">Выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="58ad7-141">Select **Edit**.</span></span>
1. <span data-ttu-id="58ad7-142">Удалите существующую строку, затем подтвердите действие, выбрав **Да**.</span><span class="sxs-lookup"><span data-stu-id="58ad7-142">Delete the existing line, and then confirm the action by selecting **Yes**.</span></span>
1. <span data-ttu-id="58ad7-143">На панели операций выберите **Создать** для создания строки.</span><span class="sxs-lookup"><span data-stu-id="58ad7-143">On the Action Pane, select **New** to create a line.</span></span>
1. <span data-ttu-id="58ad7-144">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="58ad7-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="58ad7-145">**Порядковый номер**: *1*</span><span class="sxs-lookup"><span data-stu-id="58ad7-145">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="58ad7-146">**Поле описания:** *Количество работ меньше 20 и убывает*</span><span class="sxs-lookup"><span data-stu-id="58ad7-146">**Description field:** *Work quantity less than 20 and Descending*</span></span>

1. <span data-ttu-id="58ad7-147">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="58ad7-147">Select **Save**.</span></span>
1. <span data-ttu-id="58ad7-148">На панели операций выберите **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="58ad7-148">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="58ad7-149">На вкладке **Объединения** раскройте иерархию объединения, чтобы отобразить таблицу **Строки работ**.</span><span class="sxs-lookup"><span data-stu-id="58ad7-149">On the **Joins** tab, expand the join hierarchy to show the **Work lines** table.</span></span>
1. <span data-ttu-id="58ad7-150">Выберите соединение таблицы **Строки работ**.</span><span class="sxs-lookup"><span data-stu-id="58ad7-150">Select the **Work lines** table join.</span></span>
1. <span data-ttu-id="58ad7-151">Выберите **Добавить соединение таблицы**.</span><span class="sxs-lookup"><span data-stu-id="58ad7-151">Select **Add table join**.</span></span>
1. <span data-ttu-id="58ad7-152">В отобразившемся списке найдите и выберите строку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="58ad7-152">In the list that appears, find and select the row that has the following settings:</span></span>

    - <span data-ttu-id="58ad7-153">**Режим соединения:** *n:1*</span><span class="sxs-lookup"><span data-stu-id="58ad7-153">**Join mode:** *n:1*</span></span>
    - <span data-ttu-id="58ad7-154">**Отношение:** *Местонахождения (местонахождение)*</span><span class="sxs-lookup"><span data-stu-id="58ad7-154">**Relation:** *Locations (Location)*</span></span>

1. <span data-ttu-id="58ad7-155">Выберите **Выбрать**.</span><span class="sxs-lookup"><span data-stu-id="58ad7-155">Select **Select**.</span></span>

    <span data-ttu-id="58ad7-156">Местоположения добавляются к соединению таблицы.</span><span class="sxs-lookup"><span data-stu-id="58ad7-156">Locations are added to the table join.</span></span>

1. <span data-ttu-id="58ad7-157">На вкладке **Сортировка** выберите **добавить**, чтобы добавить строку.</span><span class="sxs-lookup"><span data-stu-id="58ad7-157">On the **Sorting** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="58ad7-158">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="58ad7-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="58ad7-159">**Таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="58ad7-159">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="58ad7-160">**Производная таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="58ad7-160">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="58ad7-161">**Поле:** *Количество работы* (В появившемся окне сообщения выберите **Да**, чтобы добавить сортировку в это поле.)</span><span class="sxs-lookup"><span data-stu-id="58ad7-161">**Field:** *Work quantity* (In the message box that appears, select **Yes** to add sorting to this field.)</span></span>
    - <span data-ttu-id="58ad7-162">**Направление поиска:** *В порядке убывания*</span><span class="sxs-lookup"><span data-stu-id="58ad7-162">**Search direction:** *Descending*</span></span>

1. <span data-ttu-id="58ad7-163">Выберите вкладку **Диапазон**.</span><span class="sxs-lookup"><span data-stu-id="58ad7-163">Select the **Range** tab.</span></span>

    <span data-ttu-id="58ad7-164">Если в последовательность должны быть включены только отдельные критерии работы, их можно указать на вкладке **Диапазон**. В этом примере необходимо включить только работу, когда количество меньше 20 шт. (самая малая единица измерения).</span><span class="sxs-lookup"><span data-stu-id="58ad7-164">If only specific work criteria should be included in the sequencing, you can specify them on the **Range** tab. In this example, you want to include only work where the quantity is less than 20 ea (the lowest unit of measure).</span></span>

    <span data-ttu-id="58ad7-165">Обратите внимание, что некоторые строки уже включены.</span><span class="sxs-lookup"><span data-stu-id="58ad7-165">Notice that some lines are already included.</span></span> <span data-ttu-id="58ad7-166">Эти строки не должны удаляться.</span><span class="sxs-lookup"><span data-stu-id="58ad7-166">Those lines should not be removed.</span></span>

1. <span data-ttu-id="58ad7-167">Выберите **Добавить**, чтобы добавить строку.</span><span class="sxs-lookup"><span data-stu-id="58ad7-167">Select **Add** to add a line.</span></span>
1. <span data-ttu-id="58ad7-168">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="58ad7-168">On the new line, set the following values:</span></span>

    - <span data-ttu-id="58ad7-169">**Таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="58ad7-169">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="58ad7-170">**Производная таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="58ad7-170">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="58ad7-171">**Поле:** *Рабочее количество запасов*</span><span class="sxs-lookup"><span data-stu-id="58ad7-171">**Field:** *Inventory work quantity*</span></span>
    - <span data-ttu-id="58ad7-172">**Критерий:** *\<20* (менее 20)</span><span class="sxs-lookup"><span data-stu-id="58ad7-172">**Criteria:** *\<20* (less than 20)</span></span>

1. <span data-ttu-id="58ad7-173">Выберите **Добавить**, чтобы добавить другую строку.</span><span class="sxs-lookup"><span data-stu-id="58ad7-173">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="58ad7-174">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="58ad7-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="58ad7-175">**Таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="58ad7-175">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="58ad7-176">**Производная таблица:** *Строки работ*</span><span class="sxs-lookup"><span data-stu-id="58ad7-176">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="58ad7-177">**Поле:** *Тип работы*</span><span class="sxs-lookup"><span data-stu-id="58ad7-177">**Field:** *Work type*</span></span>
    - <span data-ttu-id="58ad7-178">**Критерии:** *Комплектации*</span><span class="sxs-lookup"><span data-stu-id="58ad7-178">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="58ad7-179">Выберите **Добавить**, чтобы добавить другую строку.</span><span class="sxs-lookup"><span data-stu-id="58ad7-179">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="58ad7-180">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="58ad7-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="58ad7-181">**Таблица:** *Местонахождения*</span><span class="sxs-lookup"><span data-stu-id="58ad7-181">**Table:** *Locations*</span></span>
    - <span data-ttu-id="58ad7-182">**Производная таблица:** *Местонахождения*</span><span class="sxs-lookup"><span data-stu-id="58ad7-182">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="58ad7-183">**Поле:** *Код профиля местонахождения*</span><span class="sxs-lookup"><span data-stu-id="58ad7-183">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="58ad7-184">**Критерий:** *!STAGE*</span><span class="sxs-lookup"><span data-stu-id="58ad7-184">**Criteria:** *!STAGE*</span></span>

        > [!IMPORTANT]
        > <span data-ttu-id="58ad7-185">Убедитесь, что указан восклицательный знак (*!*) перед *STAGE*.</span><span class="sxs-lookup"><span data-stu-id="58ad7-185">Be sure to include the exclamation point (*!*) in front of *STAGE*.</span></span>

1. <span data-ttu-id="58ad7-186">Выберите **ОК**, чтобы сохранить и закрыть запрос.</span><span class="sxs-lookup"><span data-stu-id="58ad7-186">Select **OK** to save and close the query.</span></span>
1. <span data-ttu-id="58ad7-187">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="58ad7-187">Select **Save**.</span></span>
1. <span data-ttu-id="58ad7-188">Закройте страницу, чтобы вернуться на страницу **Пункты меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="58ad7-188">Close the page to return to the **Mobile device menu items** page.</span></span>

> [!NOTE]
> <span data-ttu-id="58ad7-189">Эта настройка определяет критерии, которые будут использоваться для подачи подходящей работы в пункт меню мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="58ad7-189">This setup defines the criteria that will be used to feed eligible work to the mobile device menu item.</span></span> <span data-ttu-id="58ad7-190">При добавлении дополнительных строк критериев в запрос система сначала будет использовать строку запроса с наименьшим порядковым номером.</span><span class="sxs-lookup"><span data-stu-id="58ad7-190">If you add more criteria lines to the query, the system will use the query line that has lowest sequence number first.</span></span> <span data-ttu-id="58ad7-191">Другими словами, вся подходящая работа для порядкового номера 1 будут представлена пользователю в первую очередь, а затем все работы для порядкового номера 2.</span><span class="sxs-lookup"><span data-stu-id="58ad7-191">In other words, all eligible work for sequence number 1 will be presented to the user first, and then all work for sequence number 2.</span></span> <span data-ttu-id="58ad7-192">Таким образом, если необходимо использовать определенный диапазон и сортировку вместе, они должны быть указаны в одном и том же запросе управляемой системой последовательности работ.</span><span class="sxs-lookup"><span data-stu-id="58ad7-192">Therefore, if a specific range and sorting must be used together, they should be specified in the same system-directed work sequence query.</span></span>
>
> <span data-ttu-id="58ad7-193">При этой настройке будут записаны все работы, содержащие хотя бы одну строку, в которой количество меньше 20 шт.</span><span class="sxs-lookup"><span data-stu-id="58ad7-193">This setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="58ad7-194">Таким образом, если в работе имеется строка, в которой количество равно точно 20 шт. или более 20 шт., она будет действительной, при условии, что в ней также имеется хотя бы одна строка, в которой количество меньше 20 шт.</span><span class="sxs-lookup"><span data-stu-id="58ad7-194">Therefore, if the work has a line where the quantity is exactly 20 ea or more than 20 ea, it will be valid, provided that it also has at least one line where the quantity is less than 20 ea.</span></span>

### <a name="location-directives"></a><span data-ttu-id="58ad7-195">Директивы для мест хранения</span><span class="sxs-lookup"><span data-stu-id="58ad7-195">Location directives</span></span>

<span data-ttu-id="58ad7-196">При использовании данных Contoso по умолчанию изменения запроса для действия директивы расположения не требуются.</span><span class="sxs-lookup"><span data-stu-id="58ad7-196">If you're using default Contoso data, the query for the location directive action won't require changes.</span></span> <span data-ttu-id="58ad7-197">Однако, чтобы гарантировать, что директивы местоположения будут фиксировать номенклатуры в заказах на продажу при применении этой функции в среде, отличной от Contoso, создайте новую директиву местоположения.</span><span class="sxs-lookup"><span data-stu-id="58ad7-197">However, to make sure that the location directives will capture the items on the sales orders when you apply the feature in a non-Contoso environment, create a new location directive.</span></span> <span data-ttu-id="58ad7-198">Чтобы проверить настройки в демонстрационной среде, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="58ad7-198">To verify the settings in the demo environment, follow these steps.</span></span>

1. <span data-ttu-id="58ad7-199">Перейдите к **Управление складом** \> **Настройка** \> **директивы местонахождений**.</span><span class="sxs-lookup"><span data-stu-id="58ad7-199">Go to **Warehouse management** \> **Setup** \> **Location directives**.</span></span>
1. <span data-ttu-id="58ad7-200">В поле **Тип заказа на работу** выберите *Заказы на продажу*.</span><span class="sxs-lookup"><span data-stu-id="58ad7-200">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="58ad7-201">Выберите директиву местоположения с именем *51 Комплектация*.</span><span class="sxs-lookup"><span data-stu-id="58ad7-201">Select the location directive that is named *51 Pick*.</span></span>
1. <span data-ttu-id="58ad7-202">На экспресс-вкладке **Действия директивы местоположения** выберите строку для действия **Комплектация**.</span><span class="sxs-lookup"><span data-stu-id="58ad7-202">On the **Location Directive Actions** FastTab, select the line for the **Pick** action.</span></span>
1. <span data-ttu-id="58ad7-203">Выберите **Изменить запрос** над сеткой.</span><span class="sxs-lookup"><span data-stu-id="58ad7-203">Select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="58ad7-204">Просмотрите запрос **Диапазон**.</span><span class="sxs-lookup"><span data-stu-id="58ad7-204">Review the **Range** query.</span></span>

    1. <span data-ttu-id="58ad7-205">Найдите строку, в которой в поле **Поле** указано *Местонахождение*.</span><span class="sxs-lookup"><span data-stu-id="58ad7-205">Find the line where the **Field** field is set to *Location*.</span></span>
    2. <span data-ttu-id="58ad7-206">Убедитесь, что поле **Критерии** пусто (т. е., отсутствуют ограничения).</span><span class="sxs-lookup"><span data-stu-id="58ad7-206">Make sure that the **Criteria** field is blank (that is, there are no restrictions).</span></span>

## <a name="scenario"></a><span data-ttu-id="58ad7-207">Сценарий</span><span class="sxs-lookup"><span data-stu-id="58ad7-207">Scenario</span></span>

### <a name="create-sales-order-picking-work"></a><span data-ttu-id="58ad7-208">Создание работы комплектации для заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="58ad7-208">Create sales order picking work</span></span>

<span data-ttu-id="58ad7-209">Прежде чем выполнять комплектацию, управляемую системой, должно быть создано несколько исходящих работ.</span><span class="sxs-lookup"><span data-stu-id="58ad7-209">Before system-directed picking is run, some outbound work should be created.</span></span> <span data-ttu-id="58ad7-210">Для этого сценария будут созданы четыре заказа на продажу, которые будут основываться на указанных запросах последовательности работ, управляемых системой.</span><span class="sxs-lookup"><span data-stu-id="58ad7-210">For this scenario, you will create four sales orders that are based on the specified system-directed work sequence queries.</span></span>

<span data-ttu-id="58ad7-211">Вы зарезервируете количества запасов для каждого заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="58ad7-211">You will reserve inventory quantities for each sales order.</span></span> <span data-ttu-id="58ad7-212">Таким образом, зарезервированный запас не может быть извлечен со склада для других заказов, пока резервирование запаса не будет полностью или частично отменено.</span><span class="sxs-lookup"><span data-stu-id="58ad7-212">Therefore, reserved inventory can't be withdrawn from the warehouse for other orders unless the inventory reservation, or part of the inventory reservation, is canceled.</span></span>

<span data-ttu-id="58ad7-213">Затем вы выпустите каждый заказ на продажу в склад для создания исходящей работы.</span><span class="sxs-lookup"><span data-stu-id="58ad7-213">You will then release each sales order to the warehouse to create the outbound work.</span></span>

#### <a name="sales-order-1"></a><span data-ttu-id="58ad7-214">Заказ на продажу 1</span><span class="sxs-lookup"><span data-stu-id="58ad7-214">Sales order 1</span></span>

1. <span data-ttu-id="58ad7-215">Перейдите в раздел **Продажи и маркетинг \> Заказы на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="58ad7-215">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="58ad7-216">На панели операций выберите **Создать** для создания заказа на продажу 1.</span><span class="sxs-lookup"><span data-stu-id="58ad7-216">On the Action Pane, select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="58ad7-217">В диалоговом окне **Создание заказа на продажу** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="58ad7-217">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="58ad7-218">В разделе **Клиент** задайте для поля **Счет клиента** значение *US-004*.</span><span class="sxs-lookup"><span data-stu-id="58ad7-218">In the **Customer** section, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="58ad7-219">В разделе **Общее** задайте в поле **Склад** значение *51*.</span><span class="sxs-lookup"><span data-stu-id="58ad7-219">In the **General** section, set the **Warehouse** field to *51*.</span></span>

1. <span data-ttu-id="58ad7-220">Выберите **OK**, чтобы закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="58ad7-220">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="58ad7-221">Запишите номер заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="58ad7-221">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="58ad7-222">Добавьте строку в новый заказ на работу и задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="58ad7-222">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="58ad7-223">**Код номенклатуры:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="58ad7-223">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="58ad7-224">**Количество:** *20*</span><span class="sxs-lookup"><span data-stu-id="58ad7-224">**Quantity:** *20*</span></span>

1. <span data-ttu-id="58ad7-225">В меню **Запасы** над сеткой выберите **Резервирование**.</span><span class="sxs-lookup"><span data-stu-id="58ad7-225">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="58ad7-226">На странице **Резервирование** выберите **Зарезервировать лот**, чтобы зарезервировать запасы.</span><span class="sxs-lookup"><span data-stu-id="58ad7-226">On the **Reservation** page, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="58ad7-227">Закройте страницу **Резервирование**.</span><span class="sxs-lookup"><span data-stu-id="58ad7-227">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="58ad7-228">На панели операций на вкладке **Склад** выберите вариант **Выпустить на склад**, чтобы создать работу для склада.</span><span class="sxs-lookup"><span data-stu-id="58ad7-228">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse** to create work for the warehouse.</span></span>

    <span data-ttu-id="58ad7-229">Вы получите информационные сообщения, которые указывают код волны и коды отгрузки, которые были созданы для данного заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="58ad7-229">You receive informational messages that show the wave ID and shipment IDs that were created for the sales order.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="58ad7-230">Заказ на продажу 2</span><span class="sxs-lookup"><span data-stu-id="58ad7-230">Sales order 2</span></span>

1. <span data-ttu-id="58ad7-231">На панели операций выберите **Создать** для создания заказа на продажу 2.</span><span class="sxs-lookup"><span data-stu-id="58ad7-231">On the Action Pane, select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="58ad7-232">В диалоговом окне **Создание заказа на продажу** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="58ad7-232">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="58ad7-233">**Счет клиента:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="58ad7-233">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="58ad7-234">**Склад:** *51*</span><span class="sxs-lookup"><span data-stu-id="58ad7-234">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="58ad7-235">Выберите **OK**, чтобы закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="58ad7-235">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="58ad7-236">Запишите номер заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="58ad7-236">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="58ad7-237">Добавьте строку в новый заказ на работу и задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="58ad7-237">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="58ad7-238">**Код номенклатуры:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="58ad7-238">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="58ad7-239">**Количество:** *5*</span><span class="sxs-lookup"><span data-stu-id="58ad7-239">**Quantity:** *5*</span></span>

1. <span data-ttu-id="58ad7-240">Выберите **Добавить строку**, чтобы добавить вторую строку, и установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="58ad7-240">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="58ad7-241">**Код номенклатуры:** *M9201*</span><span class="sxs-lookup"><span data-stu-id="58ad7-241">**Item number:** *M9201*</span></span>
    - <span data-ttu-id="58ad7-242">**Количество:** *1*</span><span class="sxs-lookup"><span data-stu-id="58ad7-242">**Quantity:** *1*</span></span>

1. <span data-ttu-id="58ad7-243">Зарезервируйте запасы для обеих строк.</span><span class="sxs-lookup"><span data-stu-id="58ad7-243">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="58ad7-244">Выпустите заказ на склад.</span><span class="sxs-lookup"><span data-stu-id="58ad7-244">Release the order to the warehouse.</span></span>

#### <a name="sales-order-3"></a><span data-ttu-id="58ad7-245">Заказ на продажу 3</span><span class="sxs-lookup"><span data-stu-id="58ad7-245">Sales order 3</span></span>

1. <span data-ttu-id="58ad7-246">На панели операций выберите **Создать** для создания заказа на продажу 3.</span><span class="sxs-lookup"><span data-stu-id="58ad7-246">On the Action Pane, select **New** to create sales order 3.</span></span>
1. <span data-ttu-id="58ad7-247">В диалоговом окне **Создание заказа на продажу** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="58ad7-247">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="58ad7-248">**Счет клиента:** *US-009*</span><span class="sxs-lookup"><span data-stu-id="58ad7-248">**Customer account:** *US-009*</span></span>
    - <span data-ttu-id="58ad7-249">**Склад:** *51*</span><span class="sxs-lookup"><span data-stu-id="58ad7-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="58ad7-250">Выберите **OK**, чтобы закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="58ad7-250">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="58ad7-251">Запишите номер заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="58ad7-251">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="58ad7-252">Добавьте строку в новый заказ на работу и задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="58ad7-252">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="58ad7-253">**Код номенклатуры:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="58ad7-253">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="58ad7-254">**Количество:** *7*</span><span class="sxs-lookup"><span data-stu-id="58ad7-254">**Quantity:** *7*</span></span>

1. <span data-ttu-id="58ad7-255">Выберите **Добавить строку**, чтобы добавить вторую строку, и установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="58ad7-255">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="58ad7-256">**Код номенклатуры:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="58ad7-256">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="58ad7-257">**Количество:** *8*</span><span class="sxs-lookup"><span data-stu-id="58ad7-257">**Quantity:** *8*</span></span>

1. <span data-ttu-id="58ad7-258">Зарезервируйте запасы для обеих строк.</span><span class="sxs-lookup"><span data-stu-id="58ad7-258">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="58ad7-259">Выпустите заказ на склад.</span><span class="sxs-lookup"><span data-stu-id="58ad7-259">Release the order to the warehouse.</span></span>

#### <a name="sales-order-4"></a><span data-ttu-id="58ad7-260">Заказ на продажу 4</span><span class="sxs-lookup"><span data-stu-id="58ad7-260">Sales order 4</span></span>

1. <span data-ttu-id="58ad7-261">На панели операций выберите **Создать** для создания заказа на продажу 4.</span><span class="sxs-lookup"><span data-stu-id="58ad7-261">On the Action Pane, select **New** to create sales order 4.</span></span>
1. <span data-ttu-id="58ad7-262">В диалоговом окне **Создание заказа на продажу** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="58ad7-262">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="58ad7-263">**Счет клиента:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="58ad7-263">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="58ad7-264">**Склад:** *51*</span><span class="sxs-lookup"><span data-stu-id="58ad7-264">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="58ad7-265">Выберите **OK**, чтобы закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="58ad7-265">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="58ad7-266">Запишите номер заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="58ad7-266">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="58ad7-267">Добавьте строку в новый заказ на работу и задайте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="58ad7-267">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="58ad7-268">**Код номенклатуры:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="58ad7-268">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="58ad7-269">**Количество:** *25*</span><span class="sxs-lookup"><span data-stu-id="58ad7-269">**Quantity:** *25*</span></span>

1. <span data-ttu-id="58ad7-270">Выберите **Добавить строку**, чтобы добавить вторую строку, и установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="58ad7-270">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="58ad7-271">**Код номенклатуры:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="58ad7-271">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="58ad7-272">**Количество:** *10*</span><span class="sxs-lookup"><span data-stu-id="58ad7-272">**Quantity:** *10*</span></span>

1. <span data-ttu-id="58ad7-273">Зарезервируйте запасы для обеих строк.</span><span class="sxs-lookup"><span data-stu-id="58ad7-273">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="58ad7-274">Выпустите заказ на склад.</span><span class="sxs-lookup"><span data-stu-id="58ad7-274">Release the order to the warehouse.</span></span>

### <a name="get-work-ids-for-the-work-that-was-created"></a><span data-ttu-id="58ad7-275">Получение кодов работ для созданной вами работы</span><span class="sxs-lookup"><span data-stu-id="58ad7-275">Get work IDs for the work that was created</span></span>

1. <span data-ttu-id="58ad7-276">Перейдите в раздел **Управление складом \> Работа \> Сведения о работе**.</span><span class="sxs-lookup"><span data-stu-id="58ad7-276">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="58ad7-277">Отфильтруйте по полю **Склад**, чтобы отображалась только работа для склада *51*.</span><span class="sxs-lookup"><span data-stu-id="58ad7-277">Filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="58ad7-278">Должны быть созданы четыре кода работ.</span><span class="sxs-lookup"><span data-stu-id="58ad7-278">Four work IDs should have been created.</span></span> <span data-ttu-id="58ad7-279">Запишите код работы для каждого заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="58ad7-279">Make a note of the work ID for each sales order.</span></span>

    | <span data-ttu-id="58ad7-280">Код заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="58ad7-280">Sales order ID</span></span> | <span data-ttu-id="58ad7-281">Код работы</span><span class="sxs-lookup"><span data-stu-id="58ad7-281">Work ID</span></span> | <span data-ttu-id="58ad7-282">Количество работы</span><span class="sxs-lookup"><span data-stu-id="58ad7-282">Work quantity</span></span> |
    |---|---|---|
    | <span data-ttu-id="58ad7-283">Заказ на продажу 1</span><span class="sxs-lookup"><span data-stu-id="58ad7-283">Sales Order 1</span></span> | <span data-ttu-id="58ad7-284">Код работы 1</span><span class="sxs-lookup"><span data-stu-id="58ad7-284">Work ID 1</span></span> | <span data-ttu-id="58ad7-285">20 шт.</span><span class="sxs-lookup"><span data-stu-id="58ad7-285">20 ea</span></span> |
    | <span data-ttu-id="58ad7-286">Заказ на продажу 2</span><span class="sxs-lookup"><span data-stu-id="58ad7-286">Sales Order 2</span></span> | <span data-ttu-id="58ad7-287">Код работы 2</span><span class="sxs-lookup"><span data-stu-id="58ad7-287">Work ID 2</span></span> | <span data-ttu-id="58ad7-288">6 шт. (сумма по обеим строкам)</span><span class="sxs-lookup"><span data-stu-id="58ad7-288">6 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="58ad7-289">Заказ на продажу 3</span><span class="sxs-lookup"><span data-stu-id="58ad7-289">Sales Order 3</span></span> | <span data-ttu-id="58ad7-290">Код работы 3</span><span class="sxs-lookup"><span data-stu-id="58ad7-290">Work ID 3</span></span> | <span data-ttu-id="58ad7-291">15 шт. (сумма по обеим строкам)</span><span class="sxs-lookup"><span data-stu-id="58ad7-291">15 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="58ad7-292">Заказ на продажу 4</span><span class="sxs-lookup"><span data-stu-id="58ad7-292">Sales Order 4</span></span> | <span data-ttu-id="58ad7-293">Код работы 4</span><span class="sxs-lookup"><span data-stu-id="58ad7-293">Work ID 4</span></span> | <span data-ttu-id="58ad7-294">35 шт. (сумма по обеим строкам)</span><span class="sxs-lookup"><span data-stu-id="58ad7-294">35 ea (sum of both lines)</span></span> |

<span data-ttu-id="58ad7-295">Перед запуском потока на мобильном устройстве убедитесь, что только работа, только что созданная вами, имеет статус *Открыта* для склада *51* и тип заказа на работу *Заказ на продажу*.</span><span class="sxs-lookup"><span data-stu-id="58ad7-295">Before you run the flow on the mobile device, make sure that only the work that you just created is in *Open* status for warehouse *51* and the *Sales order* work order type.</span></span> <span data-ttu-id="58ad7-296">В противном случае результаты теста могут быть разными, так как управляемая системой комплектация будет включать всю подходящую работу.</span><span class="sxs-lookup"><span data-stu-id="58ad7-296">Otherwise, the results of the test might vary, because the system-direct picking will include all eligible work.</span></span>

1. <span data-ttu-id="58ad7-297">Перейдите к пункту **Управление складом \> Работа \> Исходящая \> Открытая работы по продажам**.</span><span class="sxs-lookup"><span data-stu-id="58ad7-297">Go to **Warehouse management \> Work \> Outbound \> Open sales work**.</span></span>
1. <span data-ttu-id="58ad7-298">В сетке **Открытая работа по продажам** отфильтруйте по полю **Склад**, чтобы отображалась только работа для склада *51*.</span><span class="sxs-lookup"><span data-stu-id="58ad7-298">In the **Open sales work** grid, filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="58ad7-299">Убедитесь, что показаны только четыре кода работ, созданные ранее.</span><span class="sxs-lookup"><span data-stu-id="58ad7-299">Confirm that only the four work IDs that you created earlier are shown.</span></span>
1. <span data-ttu-id="58ad7-300">Закройте страницу **Работа**.</span><span class="sxs-lookup"><span data-stu-id="58ad7-300">Close the **Work** page.</span></span>

### <a name="mobile-device-flow-execution"></a><span data-ttu-id="58ad7-301">Выполнение потока на мобильном устройстве</span><span class="sxs-lookup"><span data-stu-id="58ad7-301">Mobile device flow execution</span></span>

<span data-ttu-id="58ad7-302">В зависимости от настройки, система будет подавать пользователю работу, отсортированную от самого большого количества по строке работы до самого маленького.</span><span class="sxs-lookup"><span data-stu-id="58ad7-302">Based on the setup, the system will feed the user work that is sorted from the highest work line quantity to the lowest.</span></span> <span data-ttu-id="58ad7-303">Количество в каждой строке будет менее 20 шт.</span><span class="sxs-lookup"><span data-stu-id="58ad7-303">The quantity on every line will be less than 20 ea.</span></span>

<span data-ttu-id="58ad7-304">Помните, что при этой настройке будут записаны все работы, содержащие хотя бы одну строку, в которой количество меньше 20 шт.</span><span class="sxs-lookup"><span data-stu-id="58ad7-304">Remember that this setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="58ad7-305">Таким образом, если в работе имеется другая строка, в которой количество равно точно 20 шт. или более 20 шт., она также будет действительной.</span><span class="sxs-lookup"><span data-stu-id="58ad7-305">Therefore, if the work has another line where the quantity is exactly 20 ea or more than 20 ea, it will also be valid.</span></span>

#### <a name="mobile-app"></a><span data-ttu-id="58ad7-306">Мобильное приложение</span><span class="sxs-lookup"><span data-stu-id="58ad7-306">Mobile app</span></span>

1. <span data-ttu-id="58ad7-307">Выполните вход в приложение склада как пользователь на складе *51*.</span><span class="sxs-lookup"><span data-stu-id="58ad7-307">Sign in to the warehousing app as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="58ad7-308">Выберите **Исходящие \> Комплектация продаж — система**.</span><span class="sxs-lookup"><span data-stu-id="58ad7-308">Go to **Outbound \> Sales Picking - System**.</span></span>

    <span data-ttu-id="58ad7-309">Будет представлен шаг комплектации для кода работы *4*.</span><span class="sxs-lookup"><span data-stu-id="58ad7-309">The pick step for work ID *4* is presented.</span></span> <span data-ttu-id="58ad7-310">Этот код работы представляется первым из-за настройки заказа запроса, управляемого системой, где в указали, что работа должна быть упорядочена на основе убывания количества в строке работы.</span><span class="sxs-lookup"><span data-stu-id="58ad7-310">This work ID is presented first because of the setup of the system-directed query order, where you specified that work should be sequenced based on descending work line quantity.</span></span>

1. <span data-ttu-id="58ad7-311">Завершите требуемую комплектацию и размещение, чтобы закрыть код работы.</span><span class="sxs-lookup"><span data-stu-id="58ad7-311">Complete the required pick and put to close the work ID.</span></span>

    <span data-ttu-id="58ad7-312">Затем отображается код работы *3*.</span><span class="sxs-lookup"><span data-stu-id="58ad7-312">Next, work ID *3* is presented.</span></span> <span data-ttu-id="58ad7-313">Одна из его строк работы находится следующей в последовательности на основе количества в строке работы.</span><span class="sxs-lookup"><span data-stu-id="58ad7-313">One of its work lines is next in the sequence, based on the work line quantity.</span></span>

1. <span data-ttu-id="58ad7-314">Завершите комплектацию и размещение, чтобы закрыть код работы.</span><span class="sxs-lookup"><span data-stu-id="58ad7-314">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="58ad7-315">Затем отображается код работы *2*.</span><span class="sxs-lookup"><span data-stu-id="58ad7-315">Next, work ID *2* is presented.</span></span> <span data-ttu-id="58ad7-316">Эта строка комплектации работы является следующей в последовательности.</span><span class="sxs-lookup"><span data-stu-id="58ad7-316">This work's pick line is next in the sequence.</span></span>

1. <span data-ttu-id="58ad7-317">Завершите комплектацию и размещение, чтобы закрыть код работы.</span><span class="sxs-lookup"><span data-stu-id="58ad7-317">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="58ad7-318">Вам не должна быть представлена никакая дальнейшая работа.</span><span class="sxs-lookup"><span data-stu-id="58ad7-318">No further work should be presented to you.</span></span> <span data-ttu-id="58ad7-319">Код работы *1* не подходит для данного пункта меню мобильного устройства, поскольку запрос указывает, что заголовки работы рассматриваются только в том случае, если количество в строках работы меньше 20 шт.</span><span class="sxs-lookup"><span data-stu-id="58ad7-319">Work ID *1* isn't eligible for this mobile device menu item, because the query specifies that work headers are considered only if the quantity on the work lines is less than 20 ea.</span></span>

## <a name="tips"></a><span data-ttu-id="58ad7-320">Советы</span><span class="sxs-lookup"><span data-stu-id="58ad7-320">Tips</span></span>

<span data-ttu-id="58ad7-321">Запросы последовательности работ под управлением системы являются *инклюзивными*.</span><span class="sxs-lookup"><span data-stu-id="58ad7-321">The system-directed work sequence queries are *inclusive*.</span></span> <span data-ttu-id="58ad7-322">Важно помнить этот факт для некоторых настроек.</span><span class="sxs-lookup"><span data-stu-id="58ad7-322">It's important that you remember this fact for some setups.</span></span> <span data-ttu-id="58ad7-323">Например, вы хотите, чтобы конкретный пункт меню обрабатывал работу только в том случае, если единицей измерения работы является *шт.*, и это ограничение вы указали на вкладке **Диапазон** запроса.</span><span class="sxs-lookup"><span data-stu-id="58ad7-323">For example, you want a specific menu item to process only work where the work unit is *ea*, and you specify that restriction on the **Range** tab of the query.</span></span> <span data-ttu-id="58ad7-324">В этом случае вся работа, в которой по крайней мере для одной строки работы заданы единицы измерения работы *шт.*, отправляется работнику.</span><span class="sxs-lookup"><span data-stu-id="58ad7-324">In this case, all work where at least one work line has the work unit set to *ea* will be fed to the worker.</span></span> <span data-ttu-id="58ad7-325">Таким образом, эта работа может также включать работу, в которой строки работы имеют единицу измерения, отличную от *шт.* (например, *коробка* или *палета*).</span><span class="sxs-lookup"><span data-stu-id="58ad7-325">Therefore, this work might also include work where work lines have a work unit other than *ea* (such as *box* or *pallet*).</span></span> <span data-ttu-id="58ad7-326">Запрос будет исключать только работу, для которой ни в одной строке работы не заданы единицы измерения работы *шт.*</span><span class="sxs-lookup"><span data-stu-id="58ad7-326">The query will exclude only work where no work line has the work unit set to *ea*.</span></span>

<span data-ttu-id="58ad7-327">Таким образом, в примере из этого сценария код работы *4* также был включен с помощью запроса.</span><span class="sxs-lookup"><span data-stu-id="58ad7-327">Therefore, in the example from this scenario, work ID *4* was also captured by the query.</span></span> <span data-ttu-id="58ad7-328">При создании были добавлены две строки: одна для 25 шт., другая для 10 шт.</span><span class="sxs-lookup"><span data-stu-id="58ad7-328">When it was created, two lines were added: one for 25 ea and another for 10 ea.</span></span> <span data-ttu-id="58ad7-329">Работа все равно была представлена пользователю, так как по крайней мере одна из строк работы имеет количество менее 20 шт.</span><span class="sxs-lookup"><span data-stu-id="58ad7-329">The work was still presented to the user, because at least one work line has a quantity of less than 20 ea.</span></span>

<span data-ttu-id="58ad7-330">В зависимости от сценария, этого поведения можно избежать, используя перерывы работы.</span><span class="sxs-lookup"><span data-stu-id="58ad7-330">Depending on the scenario, you can prevent this behavior by using work breaks.</span></span>
