---
title: Группировка шаблонов волны
description: Группировка шаблонов волны позволяет системе использовать настройки шаблона волн, чтобы определить в зависимости от того, какие критерии были определены, как разбить выпущенные строки и назначить их новым или существующим волнам. Эта функция может быть полезной на складах, где волны создаются на основе определённых критериев, но где менеджеры предпочитают создавать волны автоматически, а не вручную.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9cbc0b6655de740628bcf3709d250ac02238038b
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4015834"
---
# <a name="wave-template-grouping"></a><span data-ttu-id="355d7-104">Группировка шаблонов волны</span><span class="sxs-lookup"><span data-stu-id="355d7-104">Wave template grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="355d7-105">Группировка шаблонов волны позволяет системе использовать настройки [шаблона волн](tasks/configure-wave-processing.md), чтобы определить в зависимости от того, какие критерии были определены, как разбить выпущенные строки и назначить их новым или существующим волнам.</span><span class="sxs-lookup"><span data-stu-id="355d7-105">Wave template grouping enables the system to use [wave template](tasks/configure-wave-processing.md) setups to determine, based on criteria that you define, how it should split released lines and assign them to new or existing waves.</span></span> <span data-ttu-id="355d7-106">Эта функция может быть полезной на складах, где волны создаются на основе определённых критериев, но где менеджеры предпочитают создавать волны автоматически, а не вручную.</span><span class="sxs-lookup"><span data-stu-id="355d7-106">This feature can be useful in warehouses where waves are created based on specific criteria, but where managers prefer to create waves automatically instead of manually.</span></span> <span data-ttu-id="355d7-107">Она позволяет системе добавлять каждую вновь выпущенную отгрузку в первую волну, которую она найдет с соответствующими значениями полей группировки.</span><span class="sxs-lookup"><span data-stu-id="355d7-107">It enables the system to add each newly released shipment to the first wave that it finds that has matching grouping field values.</span></span> <span data-ttu-id="355d7-108">Если совпадений не найдено, система создает новую волну для новой отгрузки.</span><span class="sxs-lookup"><span data-stu-id="355d7-108">If no match is found, the system creates a new wave for the new shipment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="355d7-109">Группировка шаблона волны не поддерживается для типов работ *комплектацией сырья для производства* или *комплектации канбана*.</span><span class="sxs-lookup"><span data-stu-id="355d7-109">Wave template grouping isn't supported for the work types *production raw material picking* or *Kanban picking*.</span></span> <span data-ttu-id="355d7-110">Это объясняется тем, что группировка волны базируется на отгрузках, а эти типы работ не используют отгрузки.</span><span class="sxs-lookup"><span data-stu-id="355d7-110">This is because wave grouping is based on shipments and these work types don't use shipments.</span></span>

## <a name="turn-on-the-wave-template-grouping-feature"></a><span data-ttu-id="355d7-111">Включение функции группировки шаблонов волн</span><span class="sxs-lookup"><span data-stu-id="355d7-111">Turn on the Wave template grouping feature</span></span>

<span data-ttu-id="355d7-112">Прежде чем использовать функцию *Группировка шаблонов волн* , она должна быть включена в системе.</span><span class="sxs-lookup"><span data-stu-id="355d7-112">Before you can use the *Wave template grouping* feature, it must be turned on in your system.</span></span> <span data-ttu-id="355d7-113">Администраторы могут использовать параметры [управления компонентами](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения, если это требуется.</span><span class="sxs-lookup"><span data-stu-id="355d7-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="355d7-114">В рабочей области **Управление функциями** эта функция перечисляется следующими способами:</span><span class="sxs-lookup"><span data-stu-id="355d7-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="355d7-115">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="355d7-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="355d7-116">**Имя функции:** *Группировка шаблонов волн*</span><span class="sxs-lookup"><span data-stu-id="355d7-116">**Feature name:** *Wave template grouping*</span></span>

## <a name="set-a-wave-template-to-use-wave-template-grouping"></a><a name="set-up-template"></a><span data-ttu-id="355d7-117">Настройка шаблона волн для использования группировки шаблонов волн</span><span class="sxs-lookup"><span data-stu-id="355d7-117">Set a wave template to use wave template grouping</span></span>

<span data-ttu-id="355d7-118">Чтобы сделать группировку шаблонов волн доступной, выполните следующие действия, чтобы настроить [шаблон волны](tasks/configure-wave-processing.md).</span><span class="sxs-lookup"><span data-stu-id="355d7-118">To make wave template grouping available, follow these steps to set up your [wave template](tasks/configure-wave-processing.md).</span></span>

1. <span data-ttu-id="355d7-119">Перейдите в раздел **Управление складом \> Настройка \> Волны \> Шаблоны волны**.</span><span class="sxs-lookup"><span data-stu-id="355d7-119">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="355d7-120">В левой области выберите шаблон волны для настройки.</span><span class="sxs-lookup"><span data-stu-id="355d7-120">In the left pane, select the wave template to set up.</span></span> <span data-ttu-id="355d7-121">При подготовке к работе с сценарием далее в этом разделе с использованием демонстрационных данных выберите шаблон **62 Отгрузка по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="355d7-121">If you're preparing to work through the scenario later in this topic by using demo data, select the **62 Shipping default** template.</span></span>
1. <span data-ttu-id="355d7-122">Выберите **Правка** , чтобы перевести страницу в режим редактирования.</span><span class="sxs-lookup"><span data-stu-id="355d7-122">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="355d7-123">На экспресс-вкладке **Общие** установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="355d7-123">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="355d7-124">**Создавать волны автоматически:** *Да*</span><span class="sxs-lookup"><span data-stu-id="355d7-124">**Automate wave creation:** *Yes*</span></span>
    - <span data-ttu-id="355d7-125">**Назначить открытым волнам:** *Да*</span><span class="sxs-lookup"><span data-stu-id="355d7-125">**Assign to open waves:** *Yes*</span></span>
    - <span data-ttu-id="355d7-126">**Обрабатывать волну перед запуском на склад:** *Нет*</span><span class="sxs-lookup"><span data-stu-id="355d7-126">**Process wave at release to warehouse:** *No*</span></span>

1. <span data-ttu-id="355d7-127">На панели операций выберите **Изменить запрос** , чтобы открыть диалоговое окно запроса.</span><span class="sxs-lookup"><span data-stu-id="355d7-127">On the Action Pane, select **Edit query** to open the query dialog box.</span></span>
1. <span data-ttu-id="355d7-128">В диалоговом окне запроса на вкладке **Сортировка** проверьте критерии сортировки и убедитесь, что имеется правило, включающее поле, которое должно использоваться для группировки волн.</span><span class="sxs-lookup"><span data-stu-id="355d7-128">In the query dialog box, on the **Sorting** tab, review the sorting criteria, and make sure that there is a rule that includes the field that you want to use to group your waves.</span></span>

    <span data-ttu-id="355d7-129">При подготовке к работе с помощью сценария с использованием демонстрационных данных добавьте строку со следующими значениями:</span><span class="sxs-lookup"><span data-stu-id="355d7-129">If you're preparing to work through the scenario by using demo data, add a row that has the following values:</span></span>

    - <span data-ttu-id="355d7-130">**Таблица:** *Отгрузки*</span><span class="sxs-lookup"><span data-stu-id="355d7-130">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="355d7-131">**Производная таблица:** *Отгрузки*</span><span class="sxs-lookup"><span data-stu-id="355d7-131">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="355d7-132">**Поле:** *Услуга перевозчика*</span><span class="sxs-lookup"><span data-stu-id="355d7-132">**Field:** *Carrier service*</span></span>

        > [!NOTE]
        > <span data-ttu-id="355d7-133">После выбора этого значения может появиться следующее сообщение: "Поле услуги перевозчика не является индексным полем.</span><span class="sxs-lookup"><span data-stu-id="355d7-133">After you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="355d7-134">Хотите добавить сортировку по нему?"</span><span class="sxs-lookup"><span data-stu-id="355d7-134">Do you want to add sorting on this?"</span></span> <span data-ttu-id="355d7-135">Чтобы добавить сортировку, выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="355d7-135">Select **Yes** to add sorting.</span></span>

    - <span data-ttu-id="355d7-136">**Направление поиска:** *Восходящее*</span><span class="sxs-lookup"><span data-stu-id="355d7-136">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="355d7-137">Выберите **ОК** , чтобы сохранить изменения и закрыть диалоговое окно запроса.</span><span class="sxs-lookup"><span data-stu-id="355d7-137">Select **OK** to save your changes and close the query dialog box.</span></span>
1. <span data-ttu-id="355d7-138">В области действий выберите **Группировка шаблонов волн**.</span><span class="sxs-lookup"><span data-stu-id="355d7-138">On the Action Pane, select **Wave template grouping**.</span></span>
1. <span data-ttu-id="355d7-139">На странице **Группировка шаблонов волн** установите флажок **Группировать по** для каждой строки, которую необходимо использовать для группировки строк заказа в волны.</span><span class="sxs-lookup"><span data-stu-id="355d7-139">On the **Wave template grouping** page, select the **Group by** check box for each row that you want to use to group your order lines into waves, as required.</span></span> <span data-ttu-id="355d7-140">При подготовке к работе в сценарии с использованием демонстрационных данных выберите флажок **Группировать по** для строки *Услуга перевозчика*.</span><span class="sxs-lookup"><span data-stu-id="355d7-140">If you're preparing to work through the scenario by using demo data, select the **Group by** check box for the *Carrier service* row.</span></span>
1. <span data-ttu-id="355d7-141">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="355d7-141">Select **Save**.</span></span>
1. <span data-ttu-id="355d7-142">Закройте страницу **Группировка шаблонов волн**.</span><span class="sxs-lookup"><span data-stu-id="355d7-142">Close the **Wave template grouping** page.</span></span>
1. <span data-ttu-id="355d7-143">Выберите **Сохранить** для сохранения шаблона.</span><span class="sxs-lookup"><span data-stu-id="355d7-143">Select **Save** to save your template.</span></span>

## <a name="scenario"></a><span data-ttu-id="355d7-144">Сценарий</span><span class="sxs-lookup"><span data-stu-id="355d7-144">Scenario</span></span>

<span data-ttu-id="355d7-145">В этом разделе представлен скрипт, с помощью которого можно узнать, что делает эта функция и как работать с ней.</span><span class="sxs-lookup"><span data-stu-id="355d7-145">This section provides a script that you can work through to learn what this feature does and how to work with it.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="355d7-146">Сделать образцы данных доступными</span><span class="sxs-lookup"><span data-stu-id="355d7-146">Make sample data available</span></span>

<span data-ttu-id="355d7-147">Для работы с этим сценарием с помощью образцов записей и значений, указанных здесь, необходимо использовать систему, в которой установлены стандартные [демонстрационные данные](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="355d7-147">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="355d7-148">Дополнительно перед началом необходимо выбрать юридическое лицо **USMF**.</span><span class="sxs-lookup"><span data-stu-id="355d7-148">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="355d7-149">Этот сценарий можно также использовать в качестве руководства по использованию этой функции при работе в производственной системе.</span><span class="sxs-lookup"><span data-stu-id="355d7-149">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="355d7-150">Однако в этом случае необходимо подставить собственные значения, и у вас могут отсутствовать некоторые типы необходимых записей, предоставляемых стандартными демонстрационными данными.</span><span class="sxs-lookup"><span data-stu-id="355d7-150">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="scenario-wave-template-grouping"></a><span data-ttu-id="355d7-151">Сценарий: группировка шаблонов волны</span><span class="sxs-lookup"><span data-stu-id="355d7-151">Scenario: Wave template grouping</span></span>

<span data-ttu-id="355d7-152">В этом сценарии показано, как использовать группировку шаблонов волн для автоматического создания нескольких волн на основе критериев группировки, определенных в шаблоне волны.</span><span class="sxs-lookup"><span data-stu-id="355d7-152">This scenario shows how to use wave template grouping to automatically create multiple waves, based on grouping criteria that are defined in a wave template.</span></span> <span data-ttu-id="355d7-153">В этом сценарии шаблон волны настраивается в системе для создания одной волны на каждого перевозчика.</span><span class="sxs-lookup"><span data-stu-id="355d7-153">In this scenario, the wave template is set up in the system to create one wave per carrier service.</span></span>

<span data-ttu-id="355d7-154">Прежде чем начать, подготовьте шаблон волны, как описано в разделе [Настройка шаблона волны для использования группировки шаблонов волн](#set-up-template) ранее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="355d7-154">Before you begin, prepare your wave template as described in the [Set a wave template to use wave template grouping](#set-up-template) section earlier in this topic.</span></span> <span data-ttu-id="355d7-155">Если вы будете работать с демонстрационными данными для этого сценария, убедитесь, что используются значения демонстрационных данных, предлагаемые в этой процедуре.</span><span class="sxs-lookup"><span data-stu-id="355d7-155">If you will be working with demo data for this scenario, be sure to use the demo data values that are suggested in that procedure.</span></span> <span data-ttu-id="355d7-156">Эта настройка будет группировать волны в соответствии со службой перевозчика, которая настроена для каждого заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="355d7-156">This setup will group your waves according to the carrier service that is set for each sales order.</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="355d7-157">Создание заказа на продажу 1</span><span class="sxs-lookup"><span data-stu-id="355d7-157">Create sales order 1</span></span>

1. <span data-ttu-id="355d7-158">Перейдите в раздел **Продажи и маркетинг \> Заказы на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="355d7-158">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="355d7-159">Выберите **Создать** , чтобы создать заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="355d7-159">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="355d7-160">В диалоговом окне **Создание заказа на продажу** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="355d7-160">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="355d7-161">На экспресс-вкладке **Клиент** задайте для поля **Счет клиента** значение *US-004*.</span><span class="sxs-lookup"><span data-stu-id="355d7-161">On the **Customer** FastTab, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="355d7-162">На экспресс-вкладке **Общее** задайте в поле **Склад** значение *62*.</span><span class="sxs-lookup"><span data-stu-id="355d7-162">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="355d7-163">Выберите **ОК** , чтобы создать новый заказ на продажу и закрыть диалоговое окно **Создание заказа на продажу**.</span><span class="sxs-lookup"><span data-stu-id="355d7-163">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="355d7-164">Новый заказ на продажу открывается в представлении **Строки**.</span><span class="sxs-lookup"><span data-stu-id="355d7-164">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="355d7-165">Запишите номер заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="355d7-165">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="355d7-166">Перейдите к представлению **Заголовок**.</span><span class="sxs-lookup"><span data-stu-id="355d7-166">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="355d7-167">На Экспресс-вкладке **Доставка** в разделе **Транспортировка** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="355d7-167">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="355d7-168">**Перевозчик, осуществляющий доставку:** *Воздушный грузовой*</span><span class="sxs-lookup"><span data-stu-id="355d7-168">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="355d7-169">**Услуга перевозчика:** *Air*</span><span class="sxs-lookup"><span data-stu-id="355d7-169">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="355d7-170">Перейдите обратно в представление **Строки**.</span><span class="sxs-lookup"><span data-stu-id="355d7-170">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="355d7-171">В разделе **Строки заказа на продажу** выберите **Добавить строку** для добавления строки к сетке.</span><span class="sxs-lookup"><span data-stu-id="355d7-171">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="355d7-172">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="355d7-172">On the new line, set the following values:</span></span>

    - <span data-ttu-id="355d7-173">**Код номенклатуры:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="355d7-173">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="355d7-174">**Количество:** *2*</span><span class="sxs-lookup"><span data-stu-id="355d7-174">**Quantity:** *2*</span></span>

1. <span data-ttu-id="355d7-175">Выберите новую строку заказа, затем в меню **Запасы** над сеткой выберите **Резервирование**.</span><span class="sxs-lookup"><span data-stu-id="355d7-175">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="355d7-176">На странице **Резервирование** на панели операций выберите **Резервирование лота** , чтобы зарезервировать полное количество выбранной строки на складе.</span><span class="sxs-lookup"><span data-stu-id="355d7-176">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="355d7-177">Закройте страницу **Резервирование** , чтобы вернуться в заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="355d7-177">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="355d7-178">На панели операций на вкладке **Склад** в группе **Действия** выберите вариант **Запуск на склад**.</span><span class="sxs-lookup"><span data-stu-id="355d7-178">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="355d7-179">Вы получаете информационное сообщение, в котором отображаются отгрузка и волна для данного заказа.</span><span class="sxs-lookup"><span data-stu-id="355d7-179">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="355d7-180">Запишите номер кода волны и номера кодов отгрузки.</span><span class="sxs-lookup"><span data-stu-id="355d7-180">Make a note of the wave ID number and the shipment ID numbers.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-1"></a><span data-ttu-id="355d7-181">Просмотрите волну, созданную из заказа на продажу 1</span><span class="sxs-lookup"><span data-stu-id="355d7-181">View the wave that was created from sales order 1</span></span>

1. <span data-ttu-id="355d7-182">Перейдите в раздел **Управление складом \> Исходящие волны \> Волны отгрузок \> Все волны**.</span><span class="sxs-lookup"><span data-stu-id="355d7-182">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="355d7-183">Выберите код волны, созданной из заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="355d7-183">Select the wave ID that was created from the sales order.</span></span>
1. <span data-ttu-id="355d7-184">Выберите ссылку кода волны, чтобы открыть страницу сведений о волне.</span><span class="sxs-lookup"><span data-stu-id="355d7-184">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="355d7-185">Обратите внимание, что отгрузка была добавлена на экспресс-вкладку **Строки волны**.</span><span class="sxs-lookup"><span data-stu-id="355d7-185">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="355d7-186">Создание заказа на продажу 2</span><span class="sxs-lookup"><span data-stu-id="355d7-186">Create sales order 2</span></span>

1. <span data-ttu-id="355d7-187">Перейдите в раздел **Продажи и маркетинг \> Заказы на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="355d7-187">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="355d7-188">Выберите **Создать** , чтобы создать заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="355d7-188">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="355d7-189">В диалоговом окне **Создание заказа на продажу** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="355d7-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="355d7-190">На экспресс-вкладке **Клиент** задайте для поля **Счет клиента** значение *US-005*.</span><span class="sxs-lookup"><span data-stu-id="355d7-190">On the **Customer** FastTab, set the **Customer account** field to *US-005*.</span></span>
    - <span data-ttu-id="355d7-191">На экспресс-вкладке **Общее** задайте в поле **Склад** значение *62*.</span><span class="sxs-lookup"><span data-stu-id="355d7-191">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="355d7-192">Выберите **ОК** , чтобы создать новый заказ на продажу и закрыть диалоговое окно **Создание заказа на продажу**.</span><span class="sxs-lookup"><span data-stu-id="355d7-192">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="355d7-193">Новый заказ на продажу открывается в представлении **Строки**.</span><span class="sxs-lookup"><span data-stu-id="355d7-193">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="355d7-194">Запишите номер заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="355d7-194">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="355d7-195">Перейдите к представлению **Заголовок**.</span><span class="sxs-lookup"><span data-stu-id="355d7-195">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="355d7-196">На Экспресс-вкладке **Доставка** в разделе **Транспортировка** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="355d7-196">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="355d7-197">**Перевозчик, осуществляющий доставку:** *Перевозка цветов*</span><span class="sxs-lookup"><span data-stu-id="355d7-197">**Shipping carrier:** *Flower moving*</span></span>
    - <span data-ttu-id="355d7-198">**Услуга перевозчика:** *Стандартная*</span><span class="sxs-lookup"><span data-stu-id="355d7-198">**Carrier service:** *Std*</span></span>

1. <span data-ttu-id="355d7-199">Перейдите обратно в представление **Строки**.</span><span class="sxs-lookup"><span data-stu-id="355d7-199">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="355d7-200">В разделе **Строки заказа на продажу** выберите **Добавить строку** для добавления строки к сетке.</span><span class="sxs-lookup"><span data-stu-id="355d7-200">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="355d7-201">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="355d7-201">On the new line, set the following values:</span></span>

    - <span data-ttu-id="355d7-202">**Код номенклатуры:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="355d7-202">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="355d7-203">**Количество:** *1*</span><span class="sxs-lookup"><span data-stu-id="355d7-203">**Quantity:** *1*</span></span>

1. <span data-ttu-id="355d7-204">Выберите новую строку заказа, затем в меню **Запасы** над сеткой выберите **Резервирование**.</span><span class="sxs-lookup"><span data-stu-id="355d7-204">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="355d7-205">На странице **Резервирование** на панели операций выберите **Резервирование лота** , чтобы зарезервировать полное количество выбранной строки на складе.</span><span class="sxs-lookup"><span data-stu-id="355d7-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="355d7-206">Закройте страницу **Резервирование** , чтобы вернуться в заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="355d7-206">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="355d7-207">На панели операций на вкладке **Склад** в группе **Действия** выберите вариант **Запуск на склад**.</span><span class="sxs-lookup"><span data-stu-id="355d7-207">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="355d7-208">Вы получаете информационное сообщение, в котором отображаются отгрузка и волна для данного заказа.</span><span class="sxs-lookup"><span data-stu-id="355d7-208">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="355d7-209">Запишите номер кода волны и номера кодов отгрузки.</span><span class="sxs-lookup"><span data-stu-id="355d7-209">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="355d7-210">Обратите внимание, что код волны отличается от кода волны первого заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="355d7-210">Notice that the wave ID differs from the wave ID of the first sales order.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-2"></a><span data-ttu-id="355d7-211">Просмотрите волну, созданную из заказа на продажу 2</span><span class="sxs-lookup"><span data-stu-id="355d7-211">View the wave that was created from sales order 2</span></span>

1. <span data-ttu-id="355d7-212">Перейдите в раздел **Управление складом \> Исходящие волны \> Волны отгрузок \> Все волны**.</span><span class="sxs-lookup"><span data-stu-id="355d7-212">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="355d7-213">Выберите код волны, созданной из второго заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="355d7-213">Select the wave ID that was created from the second sales order.</span></span>
1. <span data-ttu-id="355d7-214">Выберите ссылку кода волны, чтобы открыть страницу сведений о волне.</span><span class="sxs-lookup"><span data-stu-id="355d7-214">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="355d7-215">Обратите внимание, что отгрузка была добавлена на экспресс-вкладку **Строки волны**.</span><span class="sxs-lookup"><span data-stu-id="355d7-215">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

<span data-ttu-id="355d7-216">Для этой отгрузки была создана новая волна, так как в ней используется другая услуга перевозчика, отличная в первом заказе на продажу.</span><span class="sxs-lookup"><span data-stu-id="355d7-216">A new wave was created for this shipment, because it uses a different carrier service than the first sales order.</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="355d7-217">Создание заказа на продажу 3</span><span class="sxs-lookup"><span data-stu-id="355d7-217">Create sales order 3</span></span>

1. <span data-ttu-id="355d7-218">Перейдите в раздел **Продажи и маркетинг \> Заказы на продажу \> Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="355d7-218">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="355d7-219">Выберите **Создать** , чтобы создать заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="355d7-219">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="355d7-220">В диалоговом окне **Создание заказа на продажу** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="355d7-220">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="355d7-221">На экспресс-вкладке **Клиент** задайте для поля **Счет клиента** значение *US-006*.</span><span class="sxs-lookup"><span data-stu-id="355d7-221">On the **Customer** FastTab, set the **Customer account** field to *US-006*.</span></span>
    - <span data-ttu-id="355d7-222">На экспресс-вкладке **Общее** задайте в поле **Склад** значение *62*.</span><span class="sxs-lookup"><span data-stu-id="355d7-222">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="355d7-223">Выберите **ОК** , чтобы создать новый заказ на продажу и закрыть диалоговое окно **Создание заказа на продажу**.</span><span class="sxs-lookup"><span data-stu-id="355d7-223">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="355d7-224">Новый заказ на продажу открывается в представлении **Строки**.</span><span class="sxs-lookup"><span data-stu-id="355d7-224">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="355d7-225">Запишите номер заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="355d7-225">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="355d7-226">Перейдите к представлению **Заголовок**.</span><span class="sxs-lookup"><span data-stu-id="355d7-226">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="355d7-227">На Экспресс-вкладке **Доставка** в разделе **Транспортировка** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="355d7-227">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="355d7-228">**Перевозчик, осуществляющий доставку:** *Воздушный грузовой*</span><span class="sxs-lookup"><span data-stu-id="355d7-228">**Shipping carrier:** *Air Cargo*</span></span>
    - <span data-ttu-id="355d7-229">**Услуга перевозчика:** *Air*</span><span class="sxs-lookup"><span data-stu-id="355d7-229">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="355d7-230">Перейдите обратно в представление **Строки**.</span><span class="sxs-lookup"><span data-stu-id="355d7-230">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="355d7-231">В разделе **Строки заказа на продажу** выберите **Добавить строку** для добавления строки к сетке.</span><span class="sxs-lookup"><span data-stu-id="355d7-231">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="355d7-232">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="355d7-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="355d7-233">**Код номенклатуры:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="355d7-233">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="355d7-234">**Количество:** *1*</span><span class="sxs-lookup"><span data-stu-id="355d7-234">**Quantity:** *1*</span></span>

1. <span data-ttu-id="355d7-235">Выберите новую строку заказа, затем в меню **Запасы** над сеткой выберите **Резервирование**.</span><span class="sxs-lookup"><span data-stu-id="355d7-235">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="355d7-236">На странице **Резервирование** на панели операций выберите **Резервирование лота** , чтобы зарезервировать полное количество выбранной строки на складе.</span><span class="sxs-lookup"><span data-stu-id="355d7-236">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="355d7-237">Закройте страницу **Резервирование** , чтобы вернуться в заказ на продажу.</span><span class="sxs-lookup"><span data-stu-id="355d7-237">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="355d7-238">На панели операций на вкладке **Склад** в группе **Действия** выберите вариант **Запуск на склад**.</span><span class="sxs-lookup"><span data-stu-id="355d7-238">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="355d7-239">Вы получаете информационное сообщение, в котором отображаются отгрузка и волна для данного заказа.</span><span class="sxs-lookup"><span data-stu-id="355d7-239">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="355d7-240">Запишите номер кода волны и номера кодов отгрузки.</span><span class="sxs-lookup"><span data-stu-id="355d7-240">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="355d7-241">Отгрузка была назначена существующей волне из первого заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="355d7-241">The shipment has been assigned to the existing wave from the first sales order.</span></span>

#### <a name="view-the-wave-for-sales-orders-1-and-3"></a><span data-ttu-id="355d7-242">Просмотр волны для заказов на продажу 1 и 3</span><span class="sxs-lookup"><span data-stu-id="355d7-242">View the wave for sales orders 1 and 3</span></span>

1. <span data-ttu-id="355d7-243">Перейдите в раздел **Управление складом \> Исходящие волны \> Волны отгрузок \> Все волны**.</span><span class="sxs-lookup"><span data-stu-id="355d7-243">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="355d7-244">Выберите код волны, созданной из третьего заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="355d7-244">Select the wave ID that was created from the third sales order.</span></span>
1. <span data-ttu-id="355d7-245">Выберите ссылку кода волны, чтобы открыть страницу сведений о волне.</span><span class="sxs-lookup"><span data-stu-id="355d7-245">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="355d7-246">Обратите внимание, что отгрузка была добавлена на экспресс-вкладку **Строки волны** вместе с отгрузкой по первому заказу на продажу.</span><span class="sxs-lookup"><span data-stu-id="355d7-246">Notice that the shipment has been added to the **Wave lines** FastTab, together with the shipment for the first sales order.</span></span>
