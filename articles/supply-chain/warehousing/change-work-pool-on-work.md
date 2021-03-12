---
title: Изменить пул работ в работе
description: В этой теме объясняется, как можно использовать кнопку "Изменить пул работ" для изменения пула работ существующей работы.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPool,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 66d110c3235e8a87b64bf160bdad8524fad6abe5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001157"
---
# <a name="change-work-pool-on-work"></a><span data-ttu-id="1c1dd-103">Изменить пул работ в работе</span><span class="sxs-lookup"><span data-stu-id="1c1dd-103">Change work pool on work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c1dd-104">Пулы работ можно использовать для организации работы в группы.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-104">You can use work pools to organize work into groups.</span></span> <span data-ttu-id="1c1dd-105">Например, можно создать пул работ для классификации работы, которая выполняется в определенном местонахождении склада.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-105">For example, you can create a work pool to classify work that occurs in a specific warehouse location.</span></span>

<span data-ttu-id="1c1dd-106">Функция *Изменить пул работ на работу* добавляет кнопку **Изменить пул работ** на панель операций для рабочих элементов.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-106">The *Change work pool on work* feature adds a **Change work pool** button to the Action Pane for work items.</span></span> <span data-ttu-id="1c1dd-107">Таким образом, менеджеры склада могут легко изменять пул работ существующей работы.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-107">Therefore, warehouse managers can easily change the work pool of existing work.</span></span> <span data-ttu-id="1c1dd-108">Эта функция позволяет менеджерам быстро реагировать на изменения в помещении склада, что позволяет улучшить их возможности адаптации на изменяющиеся ситуации и необходимость переноса работы в другой пул работ.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-108">This feature lets managers react quickly to changes on the warehouse shop floor, and it helps improve their ability to adapt to changing situations and the need to transfer work to another work pool.</span></span>

## <a name="turn-on-the-change-work-pool-on-work-feature"></a><span data-ttu-id="1c1dd-109">Включение функции изменения пула работ для работы</span><span class="sxs-lookup"><span data-stu-id="1c1dd-109">Turn on the Change work pool on work feature</span></span>

<span data-ttu-id="1c1dd-110">Прежде чем начать настройку или использовать эту функцию, необходимо убедиться, что она доступна в системе.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-110">Before you begin to set up or use this feature, you must make sure that it's available in your system.</span></span> <span data-ttu-id="1c1dd-111">Администраторы могут использовать параметры [управления компонентами](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения, если это требуется.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="1c1dd-112">В рабочей области **Управление функциями** эта функция перечисляется следующими способами:</span><span class="sxs-lookup"><span data-stu-id="1c1dd-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="1c1dd-113">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="1c1dd-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="1c1dd-114">**Имя функции:** *Изменение пула работ для работы*</span><span class="sxs-lookup"><span data-stu-id="1c1dd-114">**Feature name:** *Change work pool on work*</span></span>

## <a name="set-up-the-change-work-pool-on-work-feature"></a><span data-ttu-id="1c1dd-115">Настройка функции изменения пула работ для работы</span><span class="sxs-lookup"><span data-stu-id="1c1dd-115">Set up the Change work pool on work feature</span></span>

<span data-ttu-id="1c1dd-116">Для использования этой функции необходимо настроить некоторые пулы работ.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-116">To use this feature, you must have some work pools set up.</span></span> <span data-ttu-id="1c1dd-117">Можно также настроить шаблоны работ таким образом, чтобы они автоматически назначали пул.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-117">You might also set up your work templates so that they automatically assign a pool.</span></span> <span data-ttu-id="1c1dd-118">Если вы хотите работать с примером сценария, который приведен ниже в этом разделе, настройте систему, как описано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-118">If you want to work through the example scenario that is provided later in this topic, set up your system as described in this section.</span></span>

### <a name="set-up-work-pools"></a><span data-ttu-id="1c1dd-119">Настройка пулов работ</span><span class="sxs-lookup"><span data-stu-id="1c1dd-119">Set up work pools</span></span>

<span data-ttu-id="1c1dd-120">Пулы работ позволяют организовывать рабочие элементы по типам.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-120">Work pools let you organize work items by type.</span></span> <span data-ttu-id="1c1dd-121">Для работы с функцией *Изменение пула работ для работы* необходимо иметь как минимум два доступных пула работ.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-121">To work with the *Change work pool on work* feature, you must have at least two work pools available.</span></span> <span data-ttu-id="1c1dd-122">Для просмотра и добавления пулов работ выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-122">To view and add work pools, follow these steps.</span></span>

1. <span data-ttu-id="1c1dd-123">Перейдите в раздел **Управление складом \> Настройка \> Работа \> Пулы работ**.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-123">Go to **Warehouse management \> Setup \> Work \> Work pools**.</span></span>
1. <span data-ttu-id="1c1dd-124">Если вы работаете с демонстрационными данными компании **USMF** и будете работать с примером сценария позже в этом разделе, добавьте два пула рабочих пулов со следующими настройками:</span><span class="sxs-lookup"><span data-stu-id="1c1dd-124">If you're working with demo data from the **USMF** company and will work through the example scenario later in this topic, add two work pools that have the following settings:</span></span>

    - <span data-ttu-id="1c1dd-125">Пул работ 1:</span><span class="sxs-lookup"><span data-stu-id="1c1dd-125">Work pool 1:</span></span>

        - <span data-ttu-id="1c1dd-126">**Код пула работ:** *Webshop*</span><span class="sxs-lookup"><span data-stu-id="1c1dd-126">**Work pool ID:** *Webshop*</span></span>
        - <span data-ttu-id="1c1dd-127">**Описание:** *Интернет-магазин*</span><span class="sxs-lookup"><span data-stu-id="1c1dd-127">**Description:** *Web Shop*</span></span>

    - <span data-ttu-id="1c1dd-128">Пул работ 2:</span><span class="sxs-lookup"><span data-stu-id="1c1dd-128">Work pool 2:</span></span>

        - <span data-ttu-id="1c1dd-129">**Код пула работ:** *CallCenter*</span><span class="sxs-lookup"><span data-stu-id="1c1dd-129">**Work pool ID:** *CallCenter*</span></span>
        - <span data-ttu-id="1c1dd-130">**Описание:** *Центр обработки вызовов*</span><span class="sxs-lookup"><span data-stu-id="1c1dd-130">**Description:** *Call Center*</span></span>

1. <span data-ttu-id="1c1dd-131">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-131">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="1c1dd-132">Настройка шаблонов работ</span><span class="sxs-lookup"><span data-stu-id="1c1dd-132">Set up work templates</span></span>

<span data-ttu-id="1c1dd-133">Для каждого из шаблонов работы можно настроить используемый по умолчанию пул работ, как требуется.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-133">For each of your work templates, you can set a default work pool, as you require.</span></span> <span data-ttu-id="1c1dd-134">Для каждого соответствующего шаблона пул работ назначается в столбце **Код пула работ**.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-134">For each relevant template, you assign a work pool in the **Work pool ID** column.</span></span> <span data-ttu-id="1c1dd-135">В этом случае все рабочие элементы, созданные с использованием данного шаблона, автоматически наследуют назначенный пул работ.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-135">In this case, all work items that are generated by using a given template automatically inherit the assigned work pool.</span></span> <span data-ttu-id="1c1dd-136">Если вы работаете с демонстрационными данными компании **USMF** и будете работать с примером сценария позже в этом разделе, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-136">If you're working with the demo data from the **USMF** company and will work through the example scenario later in this topic, follow these steps.</span></span>

1. <span data-ttu-id="1c1dd-137">Перейдите в раздел **Управление складом \> Настройка \> Работа \> Шаблоны работ**.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-137">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="1c1dd-138">В области действий выберите **Правка**, чтобы перевести страницу в режим редактирования.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-138">On the Action Pane, select **Edit** to put the page into editing mode.</span></span>
1. <span data-ttu-id="1c1dd-139">Отредактируйте шаблон, задав следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1c1dd-139">Edit the template by setting the following values:</span></span>

    - <span data-ttu-id="1c1dd-140">**Шаблон работы:** *62 Из комплектации на упаковку*</span><span class="sxs-lookup"><span data-stu-id="1c1dd-140">**Work template:** *62 Pick to pack*</span></span>
    - <span data-ttu-id="1c1dd-141">**Код пула работ:** *Webshop*</span><span class="sxs-lookup"><span data-stu-id="1c1dd-141">**Work pool ID:** *Webshop*</span></span>

1. <span data-ttu-id="1c1dd-142">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-142">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="1c1dd-143">Пример сценария</span><span class="sxs-lookup"><span data-stu-id="1c1dd-143">Example scenario</span></span>

<span data-ttu-id="1c1dd-144">В этом сценарии показано, как изменить поток обработки для существующего рабочего элемента путем изменения его пула работ.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-144">This scenario shows how to change the stream of processing for an existing work item by changing its work pool.</span></span> <span data-ttu-id="1c1dd-145">Он использует демонстрационные данные компании **USMF** и настройки, которые были предложены ранее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-145">It uses demo data from the **USMF** company and the settings that were suggested earlier in this topic.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="1c1dd-146">Создание заказа на продажу и выпуск его на склад</span><span class="sxs-lookup"><span data-stu-id="1c1dd-146">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="1c1dd-147">Убедитесь, что имеется достаточное количество запасов в наличии для номенклатур *A0001* и *A0002* на складе *62*.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-147">Confirm that there is enough on-hand inventory for items *A0001* and *A0002* in warehouse *62*.</span></span> <span data-ttu-id="1c1dd-148">Перейдите в раздел **Управление запасами \> Запросы и отчеты \> Список количества в наличии** и измените фильтры, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="1c1dd-148">Go to **Inventory management \> Inquiries and reports \> On-hand list**, and edit the filters as shown here:</span></span>

    - <span data-ttu-id="1c1dd-149">Значение **Склад** начинается с *62*.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-149">The **Warehouse** value begins with *62*.</span></span>
    - <span data-ttu-id="1c1dd-150">**Код номенклатуры** имеет значение *A001* или *A002*.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-150">The **Item number** value is either *A001* or *A002*.</span></span>

    <span data-ttu-id="1c1dd-151">Демонстрационные данные должны иметь количество 10.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-151">Demo data should have a quantity of 10 each.</span></span>

    <span data-ttu-id="1c1dd-152">Затем необходимо создать заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-152">Next, you must create a sales order.</span></span>

1. <span data-ttu-id="1c1dd-153">Перейдите в раздел **Продажи и маркетинг \> Заказы на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-153">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="1c1dd-154">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-154">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="1c1dd-155">В диалоговом окне **Создание заказа на продажу** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1c1dd-155">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="1c1dd-156">**Счет клиента:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="1c1dd-156">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="1c1dd-157">**Склад:** *62*</span><span class="sxs-lookup"><span data-stu-id="1c1dd-157">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="1c1dd-158">Выберите **ОК**, чтобы создать заказ на продажу и закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-158">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="1c1dd-159">Открывается новый заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-159">The new sales order is opened.</span></span> <span data-ttu-id="1c1dd-160">Он должно включать новую пустую строку в сетке на экспресс-вкладке **Строки заказа на продажу**.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-160">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="1c1dd-161">В этой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1c1dd-161">On this line, set the following values:</span></span>

    - <span data-ttu-id="1c1dd-162">**Код номенклатуры:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="1c1dd-162">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="1c1dd-163">**Количество:** *2*</span><span class="sxs-lookup"><span data-stu-id="1c1dd-163">**Quantity:** *2*</span></span>

1. <span data-ttu-id="1c1dd-164">В меню **Запасы** над сеткой выберите **Резервирование**.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-164">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="1c1dd-165">На странице **Резервирование** на панели операций выберите **Резервирование лота** для резервирования запасов.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-165">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="1c1dd-166">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-166">Close the page.</span></span>
1. <span data-ttu-id="1c1dd-167">На экспресс-вкладке **Строки заказа на продажу** выберите **Добавить строку**, чтобы добавить строку в заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-167">On the **Sales order lines** FastTab, select **Add line** to add another line to your sales order.</span></span> <span data-ttu-id="1c1dd-168">В этой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1c1dd-168">On this line, set the following values:</span></span>

    - <span data-ttu-id="1c1dd-169">**Код номенклатуры:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="1c1dd-169">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="1c1dd-170">**Количество:** *2*</span><span class="sxs-lookup"><span data-stu-id="1c1dd-170">**Quantity:** *2*</span></span>

1. <span data-ttu-id="1c1dd-171">В меню **Запасы** над сеткой выберите **Резервирование**.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-171">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="1c1dd-172">На странице **Резервирование** на панели операций выберите **Резервирование лота** для резервирования запасов.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-172">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="1c1dd-173">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-173">Close the page.</span></span>
1. <span data-ttu-id="1c1dd-174">На панели операций на вкладке **Склад** выберите вариант **Выпустить на склад**.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-174">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="1c1dd-175">Вы получите информационные сообщения, которые указывают код волны и код отгрузки, которые были созданы из выпуска.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-175">You receive informational messages that show the wave ID and shipment ID that were created from the release.</span></span> <span data-ttu-id="1c1dd-176">Запишите код волны.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-176">Make a note of the wave ID.</span></span>

### <a name="review-the-outbound-wave"></a><span data-ttu-id="1c1dd-177">Просмотр исходящей волны</span><span class="sxs-lookup"><span data-stu-id="1c1dd-177">Review the outbound wave</span></span>

1. <span data-ttu-id="1c1dd-178">Перейдите в раздел **Управление складом \> Исходящие волны \> Волны отгрузок \> Все волны**.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-178">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="1c1dd-179">В сетке найдите код волны, который был создан из выпуска заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-179">In the grid, search for the wave ID that was created from the release of the sales order.</span></span>
1. <span data-ttu-id="1c1dd-180">Выберите код волны для просмотра сведений.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-180">Select the wave ID to view the details.</span></span>
1. <span data-ttu-id="1c1dd-181">Убедитесь, что на экспресс-вкладке **Строки волны** отображается код отгрузки для заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-181">On the **Wave lines** FastTab, make sure that a shipment ID is shown for the sales order.</span></span>

    > [!TIP]
    > <span data-ttu-id="1c1dd-182">Если в настройке для шаблона отгрузки волны для параметра **Обрабатывать волну перед запуском на склад** задано значение *Нет*, необходимо вручную обработать волну, выбрав **Обработать** на вкладке **Волна** в области действий для создания работы.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-182">If the **Process wave at release to warehouse** option is set to *No* in the setup for the shipping wave template, you must manually process the wave by selecting **Process** from the **Wave** tab on the Action Pane to create work.</span></span>

1. <span data-ttu-id="1c1dd-183">Убедитесь, что волна была обработана.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-183">Make sure that the wave has been processed.</span></span> <span data-ttu-id="1c1dd-184">Эта обработка создает необходимую работу.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-184">This processing creates the required work.</span></span>

### <a name="view-work-details-and-change-the-work-pool"></a><span data-ttu-id="1c1dd-185">Просмотр сведений о работе и изменение пула работ</span><span class="sxs-lookup"><span data-stu-id="1c1dd-185">View work details and change the work pool</span></span>

<span data-ttu-id="1c1dd-186">Можно использовать страницу **Сведения о работе** для просмотра созданной работы и управления пулом работ.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-186">You can use the **Work details** page to view the work that was created and to manage the work pool.</span></span>

1. <span data-ttu-id="1c1dd-187">Перейдите в раздел **Управление складом \> Работа \> Сведения о работе**.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-187">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="1c1dd-188">Выберите строку для работы, которая была только что создана.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-188">Select the row for the work that was just created.</span></span> <span data-ttu-id="1c1dd-189">В столбце **Номер заказа** отображается номер заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-189">The **Order number** column will show the sales order number.</span></span>

    <span data-ttu-id="1c1dd-190">В поле **Код пула работ** будет установлен код пула работ, который был настроен в шаблоне работы.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-190">The **Work pool ID** field will be set to the work pool ID that was set up in the work template.</span></span>

    > [!TIP]
    > <span data-ttu-id="1c1dd-191">Если поле **Код пула работ** не отображается, добавьте этот столбец в сетку, затем обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-191">If you don't see the **Work pool ID** field, add the column to the grid, and then refresh the page.</span></span>

1. <span data-ttu-id="1c1dd-192">Для изменения пула работ, связанного с кодом работы, на панели операций на вкладке **Работа** выберите **Изменить код пула работ**.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-192">To change the work pool that is associated with the work ID, on the Action Pane, on the **Work** tab, select **Change Work pool ID**.</span></span>
1. <span data-ttu-id="1c1dd-193">В диалоговом окне **Изменение пула работ** на экспресс-вкладке **Параметры** в поле **Код пула работ** выберите *CallCenter*.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-193">In the **Change work pool** dialog box, on the **Parameters** FastTab, in the **Work pool ID** field, select *CallCenter*.</span></span>
1. <span data-ttu-id="1c1dd-194">Выберите **ОК**, чтобы применить изменения.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-194">Select **OK** to apply your change.</span></span>
1. <span data-ttu-id="1c1dd-195">Обратите внимание, что значение поля **Код пула работ** было изменено на *CallCenter*.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-195">Notice that the value of the **Work pool ID** field has now been changed to *CallCenter*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1c1dd-196">При появлении диалогового окна **Изменение пула работ** поле **Код пула работ** по умолчанию может быть пустым.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-196">When the **Change work pool** dialog box appears, the **Work pool ID** field might be blank by default.</span></span> <span data-ttu-id="1c1dd-197">Если это поле пусто, то при выборе **ОК** для применения изменений пул работ будет полностью удален из работы.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-197">If the field is blank when you select **OK** to apply changes, you will remove the work pool completely from the work.</span></span>
>
> <span data-ttu-id="1c1dd-198">Кроме переключения пулов работ, эту процедуру можно использовать для добавления пула работ в любой рабочий элемент, который не имеет пула, либо для удаления пула работ из любого рабочего элемента, в котором он имеется.</span><span class="sxs-lookup"><span data-stu-id="1c1dd-198">In addition to switching work pools, you can use this procedure to add a work pool to any work item that doesn't have one, or to remove a work pool from any work item that does have one.</span></span>
