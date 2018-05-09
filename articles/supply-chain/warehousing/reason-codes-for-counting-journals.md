---
title: "Коды оснований для проведения инвентаризации запасов"
description: "В этом разделе описывается, как настроить и применять коды оснований для задач инвентаризации."
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCountingReasonCodePolicy
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0d787dac50374af11d878652103145c9ae9b6877
ms.contentlocale: ru-ru
ms.lasthandoff: 05/08/2018

---

# <a name="reason-codes-for-inventory-counting"></a><span data-ttu-id="0ac83-103">Коды оснований для проведения инвентаризации запасов</span><span class="sxs-lookup"><span data-stu-id="0ac83-103">Reason codes for inventory counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ac83-104">Коды оснований позволяют анализировать результаты процесса инвентаризации и любых несоответствий, возникающих во время этого процесса.</span><span class="sxs-lookup"><span data-stu-id="0ac83-104">Reason codes let you analyze the results of a counting process and any discrepancies that occur during that process.</span></span> <span data-ttu-id="0ac83-105">Можно указать причину для выполнения инвентаризации, например сломанная палета или корректировка запасов, которая основана на образцах запасов.</span><span class="sxs-lookup"><span data-stu-id="0ac83-105">You can specify the reason for doing the count, such as a broken pallet or a stock adjustment that is based on inventory samples.</span></span>

## <a name="recommendation"></a><span data-ttu-id="0ac83-106">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="0ac83-106">Recommendation</span></span>

<span data-ttu-id="0ac83-107">Перед настройкой системы рекомендуется определить стратегию для работы с кодами оснований.</span><span class="sxs-lookup"><span data-stu-id="0ac83-107">Before you set up the system, we recommend that you define a strategy for working with reason codes.</span></span> <span data-ttu-id="0ac83-108">Например, попробуйте ответить на следующие вопросы:</span><span class="sxs-lookup"><span data-stu-id="0ac83-108">For example, try to answer the following questions:</span></span>

- <span data-ttu-id="0ac83-109">Должны ли коды оснований быть обязательными на складе?</span><span class="sxs-lookup"><span data-stu-id="0ac83-109">Should reason codes be mandatory on warehouses?</span></span>
- <span data-ttu-id="0ac83-110">Должны ли коды оснований быть обязательными или необязательными для некоторых номенклатур?</span><span class="sxs-lookup"><span data-stu-id="0ac83-110">Should reason codes be mandatory or optional on some items?</span></span>
- <span data-ttu-id="0ac83-111">Как много кодов оснований требуется?</span><span class="sxs-lookup"><span data-stu-id="0ac83-111">How many reason codes do you require?</span></span>
- <span data-ttu-id="0ac83-112">Как должны пользователи сканеров штрихкода использовать коды оснований?</span><span class="sxs-lookup"><span data-stu-id="0ac83-112">How should users of barcode scanners use reason codes?</span></span> <span data-ttu-id="0ac83-113">Должны ли коды оснований быть предустановленными, обязательными или недоступны для изменения?</span><span class="sxs-lookup"><span data-stu-id="0ac83-113">Should the reason codes be preselected, mandatory, or not editable?</span></span>
- <span data-ttu-id="0ac83-114">Требуется ли для складских работников другое поведение кодов причин для мобильных сканеров?</span><span class="sxs-lookup"><span data-stu-id="0ac83-114">Do warehouse workers require different reason code behavior on mobile scanners?</span></span> <span data-ttu-id="0ac83-115">Если вы ответили "Да", можно создать дополнительные пункты меню и назначить их разным сотрудникам.</span><span class="sxs-lookup"><span data-stu-id="0ac83-115">If the answer is yes, you can create more menu items and assign them to different people.</span></span>

## <a name="where-reason-codes-apply"></a><span data-ttu-id="0ac83-116">Когда применяются коды оснований</span><span class="sxs-lookup"><span data-stu-id="0ac83-116">Where reason codes apply</span></span>

<span data-ttu-id="0ac83-117">Можно создать несколько политик кодов оснований, и каждая политики кодов оснований может иметь две политики кодов оснований инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="0ac83-117">You can create multiple reason code policies, and each reason code policy can have two counting reason code policies.</span></span> <span data-ttu-id="0ac83-118">Политики кодов оснований инвентаризации могут использоваться на уровне склада или на уровне номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="0ac83-118">The counting reason code policies can be used at the warehouse level or the item level.</span></span>

## <a name="set-up-reason-code-policies"></a><span data-ttu-id="0ac83-119">Настройка политик кодов оснований</span><span class="sxs-lookup"><span data-stu-id="0ac83-119">Set up reason code policies</span></span>

1. <span data-ttu-id="0ac83-120">Выберите **Управление запасами** \> **Настройка** \> **Запасы** \> **Политики кодов оснований для проведения инвентаризации** и создайте новую политику кодов оснований.</span><span class="sxs-lookup"><span data-stu-id="0ac83-120">Select **Inventory management** \> **Setup** \> **Inventory** \> **Counting reason code policies**, and create a new reason code policy.</span></span>
2. <span data-ttu-id="0ac83-121">В поле **Тип кода основания для проведения инвентаризации** выберите **Обязательный** или **Необязательный** для указания, является ли выбора кода основания необязательным или обязательным действием в одном из следующих журналов инвентаризации:</span><span class="sxs-lookup"><span data-stu-id="0ac83-121">In the **Counting reason code type** field, select either **Mandatory** or **Optional** to specify whether selection of a reason code should be an optional or mandatory action in one of the following counting journals:</span></span>

    - <span data-ttu-id="0ac83-122">Цикличный подсчет (мобильное устройство)</span><span class="sxs-lookup"><span data-stu-id="0ac83-122">Cycle Count (mobile device)</span></span>
    - <span data-ttu-id="0ac83-123">Подсчет наличия (мобильное устройство)</span><span class="sxs-lookup"><span data-stu-id="0ac83-123">Spot Count (mobile device)</span></span>
    - <span data-ttu-id="0ac83-124">Пороговый подсчет (мобильное устройство)</span><span class="sxs-lookup"><span data-stu-id="0ac83-124">Threshold Count (mobile device)</span></span>
    - <span data-ttu-id="0ac83-125">Входящая корректировка (мобильном устройстве)</span><span class="sxs-lookup"><span data-stu-id="0ac83-125">Adjustment In (mobile device)</span></span>
    - <span data-ttu-id="0ac83-126">Исходящая корректировка (мобильном устройстве)</span><span class="sxs-lookup"><span data-stu-id="0ac83-126">Adjustment Out (mobile device)</span></span>
    - <span data-ttu-id="0ac83-127">Инвентарный журнал (полный клиент)</span><span class="sxs-lookup"><span data-stu-id="0ac83-127">Counting Journal (rich client)</span></span>

<span data-ttu-id="0ac83-128">Можно также настроить коды оснований для отдельных складов и продуктов.</span><span class="sxs-lookup"><span data-stu-id="0ac83-128">You can also set up reason codes for individual warehouses and for products.</span></span> <span data-ttu-id="0ac83-129">Настройка кода оснований для продуктов можно не принимать во внимание настройку для складов.</span><span class="sxs-lookup"><span data-stu-id="0ac83-129">The reason code setup for products can disregard the setup for warehouses.</span></span>

## <a name="mandatory-reason-codes"></a><span data-ttu-id="0ac83-130">Обязательные коды оснований</span><span class="sxs-lookup"><span data-stu-id="0ac83-130">Mandatory reason codes</span></span>

<span data-ttu-id="0ac83-131">Если задан параметр **Обязательный** в конфигурации кодов оснований для складов или номенклатур, журнал инвентаризации не может быть завершен и закрыт, пока не предоставлен код основания.</span><span class="sxs-lookup"><span data-stu-id="0ac83-131">If the **Mandatory** parameter is set in the configuration of reason codes for warehouses or items, the counting journal can't be completed and closed until a reason code is provided.</span></span>

### <a name="set-up-reason-codes-for-warehouses"></a><span data-ttu-id="0ac83-132">Настройка кодов оснований для складов</span><span class="sxs-lookup"><span data-stu-id="0ac83-132">Set up reason codes for warehouses</span></span>

1. <span data-ttu-id="0ac83-133">Выберите **Управление запасами** \> **Настройка** \> **Разделение запасов** \> **Склады**.</span><span class="sxs-lookup"><span data-stu-id="0ac83-133">Select **Inventory Management** \> **Setup** \> **Inventory breakdown** \> **Warehouses**.</span></span>
2. <span data-ttu-id="0ac83-134">На вкладке **Склад** в поле **Политика кодов оснований для проведения инвентаризации** выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="0ac83-134">On the **Warehouse** tab, in the **Counting reason code policy** field, select one of the following options:</span></span>

    - <span data-ttu-id="0ac83-135">**Пустой** — параметр, настроенный для номенклатуры, используется, чтобы определить, являются ли журналы инвентаризации обязательными для продукта.</span><span class="sxs-lookup"><span data-stu-id="0ac83-135">**Blank** – The parameter that is set up for the item is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="0ac83-136">**Обязательный** — код основания всегда необходим для журналов инвентаризации для склада.</span><span class="sxs-lookup"><span data-stu-id="0ac83-136">**Mandatory** – A reason code is always required on counting journals for the warehouse.</span></span>
    - <span data-ttu-id="0ac83-137">**Необязательный** — код основания не требуется для журналов инвентаризации для склада.</span><span class="sxs-lookup"><span data-stu-id="0ac83-137">**Optional** – A reason code isn't required on counting journals for the warehouse.</span></span>

### <a name="set-up-reason-codes-for-products"></a><span data-ttu-id="0ac83-138">Настройка кодов оснований для продуктов</span><span class="sxs-lookup"><span data-stu-id="0ac83-138">Set up reason codes for products</span></span>

1. <span data-ttu-id="0ac83-139">Выберите **Управление сведениями о продукте** \> **Продукты** \> **Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="0ac83-139">Select **Product information management** \> **Products** \> **Released products**.</span></span>
2. <span data-ttu-id="0ac83-140">На вкладке **Продукт** выберите **Политика кодов оснований для проведения инвентаризации**, затем выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="0ac83-140">On the **Product** tab, select **Counting reason code policy**, and then select one of the following options:</span></span>

    - <span data-ttu-id="0ac83-141">**Пустой** — параметр, настроенный для склада, используется, чтобы определить, являются ли журналы инвентаризации обязательными для продукта.</span><span class="sxs-lookup"><span data-stu-id="0ac83-141">**Blank** – The parameter that is set up for the warehouse is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="0ac83-142">**Обязательный** — код основания всегда необходим для журналов инвентаризации для продукта.</span><span class="sxs-lookup"><span data-stu-id="0ac83-142">**Mandatory** – A reason code is always required on counting journals for the product.</span></span> <span data-ttu-id="0ac83-143">Эта настройка переопределяет любую настройку кода основания на уровне склада.</span><span class="sxs-lookup"><span data-stu-id="0ac83-143">This setting overrides any reason code setting at the warehouse level.</span></span>
    - <span data-ttu-id="0ac83-144">**Необязательный** — код основания не требуется для журналов инвентаризации для продукта.</span><span class="sxs-lookup"><span data-stu-id="0ac83-144">**Optional** – A reason code isn't required on counting journals for the product.</span></span> <span data-ttu-id="0ac83-145">Эта настройка переопределяет любую настройку кода основания на уровне склада.</span><span class="sxs-lookup"><span data-stu-id="0ac83-145">This setting overrides any reason code setting at the warehouse level.</span></span>

### <a name="use-reason-codes-in-counting-journals"></a><span data-ttu-id="0ac83-146">Использование кодов оснований в журналах инвентаризации</span><span class="sxs-lookup"><span data-stu-id="0ac83-146">Use reason codes in counting journals</span></span>

<span data-ttu-id="0ac83-147">В журнале инвентаризации можно добавить коды оснований для инвентаризации следующих типов:</span><span class="sxs-lookup"><span data-stu-id="0ac83-147">In a counting journal, you can add reason codes for counts of the following types:</span></span>

- <span data-ttu-id="0ac83-148">Цикличный подсчет</span><span class="sxs-lookup"><span data-stu-id="0ac83-148">Cycle Count</span></span>
- <span data-ttu-id="0ac83-149">Подсчет наличия</span><span class="sxs-lookup"><span data-stu-id="0ac83-149">Spot Count</span></span>
- <span data-ttu-id="0ac83-150">Пороговый подсчет</span><span class="sxs-lookup"><span data-stu-id="0ac83-150">Threshold Count</span></span>
- <span data-ttu-id="0ac83-151">Входящая корректировка</span><span class="sxs-lookup"><span data-stu-id="0ac83-151">Adjustment In</span></span>
- <span data-ttu-id="0ac83-152">Исходящая корректировка</span><span class="sxs-lookup"><span data-stu-id="0ac83-152">Adjustment Out</span></span>

<span data-ttu-id="0ac83-153">Коды оснований добавляются в строки журнала в журналах инвентаризации типа **Инвентарный журнал**.</span><span class="sxs-lookup"><span data-stu-id="0ac83-153">Reason codes are added to the journal lines in counting journals of the **Counting journal** type.</span></span>

1. <span data-ttu-id="0ac83-154">Выберите **Управление запасами** \> **Записи журнала** \> **Инвентаризация номенклатуры** \> **Инвентаризация**.</span><span class="sxs-lookup"><span data-stu-id="0ac83-154">Select **Inventory management** \> **Journal entries** \> **Item counting** \> **Counting**.</span></span>
2. <span data-ttu-id="0ac83-155">В сведения о строке журнала инвентаризации в поле **Код основания для проведения инвентаризации** выберите вариант.</span><span class="sxs-lookup"><span data-stu-id="0ac83-155">In the line details of the counting journal, in the **Counting reason code** field, select an option.</span></span>

### <a name="view-the-counting-history-as-its-recorded-by-reason-codes"></a><span data-ttu-id="0ac83-156">Просмотр истории инвентаризации в том виде, в котором она зарегистрирована по кодам оснований</span><span class="sxs-lookup"><span data-stu-id="0ac83-156">View the counting history as it's recorded by reason codes</span></span>

- <span data-ttu-id="0ac83-157">Выберите **Управление запасами** \> **Запросы и отчеты** \> **Инвентарный журнал**, а затем в поле **Код основания для проведения инвентаризации** просмотрите историю инвентаризации, которая была записана с использованием кода основания.</span><span class="sxs-lookup"><span data-stu-id="0ac83-157">Select **Inventory management** \> **Inquiries and reports** \> **Counting history**, and then, in the **Counting reason code** field, view the counting history that has been recorded through a reason code.</span></span>

### <a name="use-a-reason-code-for-a-quantity-adjustment"></a><span data-ttu-id="0ac83-158">Использование кода основания для корректировки количества</span><span class="sxs-lookup"><span data-stu-id="0ac83-158">Use a reason code for a quantity adjustment</span></span>

1. <span data-ttu-id="0ac83-159">На странице **Запасы в наличии** выберите **Скорректировать количество**.</span><span class="sxs-lookup"><span data-stu-id="0ac83-159">On the **On-hand inventory** page, select **Adjust quantity**.</span></span> <span data-ttu-id="0ac83-160">Страницу **Запасы в наличии** можно открыть несколькими способами.</span><span class="sxs-lookup"><span data-stu-id="0ac83-160">You can open the **On-hand inventory** page in several ways.</span></span> <span data-ttu-id="0ac83-161">Например, выберите **Управление запасами** \> **Запросы и отчеты** \> **Запасы в наличии**.</span><span class="sxs-lookup"><span data-stu-id="0ac83-161">For example, select **Inventory management** \> **Inquiries and reports** \> **On-hand inventory**.</span></span>
2. <span data-ttu-id="0ac83-162">Выберите **Скорректировать количество**, а затем в поле **Код основания для проведения инвентаризации** выберите код основания.</span><span class="sxs-lookup"><span data-stu-id="0ac83-162">Select **Adjust quantity**, and then, in the **Counting reason code** field, select a reason code.</span></span>

### <a name="configure-reason-codes-for-mobile-device-menu-items"></a><span data-ttu-id="0ac83-163">Настройка кодов оснований для пунктов меню на мобильном устройстве</span><span class="sxs-lookup"><span data-stu-id="0ac83-163">Configure reason codes for mobile device menu items</span></span>

<span data-ttu-id="0ac83-164">Можно настроить коды оснований для любого типа инвентаризации в пункте меню на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="0ac83-164">You can configure reason codes for any type of count on a mobile device menu item.</span></span> <span data-ttu-id="0ac83-165">Конфигурация пункта меню мобильного устройства включает следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="0ac83-165">The configuration of the mobile device menu item includes the following information:</span></span>

- <span data-ttu-id="0ac83-166">Отображается ли код основания на мобильном устройстве работника во время инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="0ac83-166">Whether the reason code is shown to the mobile device worker during counting.</span></span>
- <span data-ttu-id="0ac83-167">Код основания по умолчанию, который отображается в пункте меню на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="0ac83-167">The default reason code that is shown on a mobile device menu item.</span></span>
- <span data-ttu-id="0ac83-168">Может ли пользователь изменять код основания.</span><span class="sxs-lookup"><span data-stu-id="0ac83-168">Whether the user can edit the reason code.</span></span>

### <a name="set-up-reason-codes-on-a-mobile-device"></a><span data-ttu-id="0ac83-169">Настройка кодов оснований на мобильном устройстве</span><span class="sxs-lookup"><span data-stu-id="0ac83-169">Set up reason codes on a mobile device</span></span>

1. <span data-ttu-id="0ac83-170">Выберите **Управление складом** \> **Настройка** \> **Мобильное устройство** \> **Пункты меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="0ac83-170">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="0ac83-171">На вкладке **Цикличный подсчет** выберите **Цикличный подсчет**.</span><span class="sxs-lookup"><span data-stu-id="0ac83-171">On the **Cycle count** tab, select **Cycle counting**.</span></span>
3. <span data-ttu-id="0ac83-172">В поле **Код основания для проведения инвентаризации по умолчанию** задайте код основания по умолчанию, который должен быть записан, когда инвентаризация выполняется с помощью пункта меню мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="0ac83-172">In the **Default counting reason code** field, set the default reason code that should be recorded when counting is done by using the mobile device menu item.</span></span>
4. <span data-ttu-id="0ac83-173">В поле **Показать код основания для проведения инвентаризации** выберите **Строка** для отображения кода основания после записи каждого отклонения.</span><span class="sxs-lookup"><span data-stu-id="0ac83-173">In the **Display counting reason code** field, select **Line** to show the reason code after each variance is recorded.</span></span> <span data-ttu-id="0ac83-174">Вместо этого можно выбрать **Скрыть**, если код основания не должен отображаться.</span><span class="sxs-lookup"><span data-stu-id="0ac83-174">Alternatively, select **Hide** if the reason code shouldn't be shown.</span></span>
5. <span data-ttu-id="0ac83-175">Задайте для параметра **Изменить код основания для проведения инвентаризации** значение **Да** или **Нет**.</span><span class="sxs-lookup"><span data-stu-id="0ac83-175">Set the **Edit counting reason code** option to either **Yes** or **No**.</span></span> <span data-ttu-id="0ac83-176">Если для этого параметра задать значение **Да**, работник может изменить код основания, когда он будет отображаться на мобильном устройстве во время инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="0ac83-176">If you set this option to **Yes**, the worker can edit the reason code when it's shown on the mobile device during counting.</span></span>

> [!NOTE]
> <span data-ttu-id="0ac83-177">Кнопку **Цикличный подсчет** можно включить на любом пункте меню мобильного устройства, на котором может выполняться инвентаризация.</span><span class="sxs-lookup"><span data-stu-id="0ac83-177">The **Cycle counting** button can be enabled on any mobile device menu item where counting can be done.</span></span> <span data-ttu-id="0ac83-178">Примеры включают пункты меню для проверки наличия, работы по указанию пользователя или работы по указанию системы.</span><span class="sxs-lookup"><span data-stu-id="0ac83-178">Example include the menu items for spot counts, user-directed work, and system-directed work.</span></span>

## <a name="cycle-count-approvals"></a><span data-ttu-id="0ac83-179">Утверждения цикличного подсчета</span><span class="sxs-lookup"><span data-stu-id="0ac83-179">Cycle count approvals</span></span>

<span data-ttu-id="0ac83-180">Перед утверждением инвентаризации пользователь может изменить код основания, связанный с инвентаризацией.</span><span class="sxs-lookup"><span data-stu-id="0ac83-180">Before a count is approved, the user can change the reason code that is associated with the count.</span></span> <span data-ttu-id="0ac83-181">После утверждения инвентаризации код основания вводится в строки журнала инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="0ac83-181">When the count is approved, the reason code is entered on the counting journal lines.</span></span>

### <a name="modify-cycle-count-approvals"></a><span data-ttu-id="0ac83-182">Изменение утверждений цикличного подсчета</span><span class="sxs-lookup"><span data-stu-id="0ac83-182">Modify cycle count approvals</span></span>

1. <span data-ttu-id="0ac83-183">Выберите **Управление складом** \> **Цикличный подсчет** \> **Работа цикличного подсчета ожидает рассмотрения**.</span><span class="sxs-lookup"><span data-stu-id="0ac83-183">Select **Warehouse management** \> **Cycle counting** \> **Cycle count work pending review**.</span></span>
2. <span data-ttu-id="0ac83-184">Выберите **Цикличный подсчет**, а затем в поле **Код основания** выберите новый код основания.</span><span class="sxs-lookup"><span data-stu-id="0ac83-184">Select **Cycle counting**, and then, in the **Reason code** field, select a new reason code.</span></span>

### <a name="modify-the-mobile-device-menu-item-for-adjustment-in-and-adjustment-out"></a><span data-ttu-id="0ac83-185">Изменение пункта меню мобильного устройства для входящей корректировки и исходящей корректировки</span><span class="sxs-lookup"><span data-stu-id="0ac83-185">Modify the mobile device menu item for Adjustment in and Adjustment out</span></span>

1. <span data-ttu-id="0ac83-186">Выберите **Управление складом** \> **Настройка** \> **Мобильное устройство** \> **Пункты меню мобильного устройства**, затем выберите **Входящая и исходящая корректировка**.</span><span class="sxs-lookup"><span data-stu-id="0ac83-186">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**, and then select **Adjustment in and out**.</span></span>
2. <span data-ttu-id="0ac83-187">Задайте для параметра **Использовать существующую работу** значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="0ac83-187">Set the **Use existing work** option to **No**.</span></span>
3. <span data-ttu-id="0ac83-188">В поле **Процесс создания работы** выберите **Входящая корректировка**.</span><span class="sxs-lookup"><span data-stu-id="0ac83-188">In the **Work creation process** field, select **Adjustment in**.</span></span>

<span data-ttu-id="0ac83-189">Следующие поля будут добавлены в пункт меню мобильного устройства, когда выбрана **Входящая корректировка** или **Исходящая корректировка** в процессе создания работы:</span><span class="sxs-lookup"><span data-stu-id="0ac83-189">The following fields will be added to the mobile device menu item when **Adjustment in** or **Adjustment out** is selected during the work creation process:</span></span>

- <span data-ttu-id="0ac83-190">Код основания для проведения инвентаризации по умолчанию</span><span class="sxs-lookup"><span data-stu-id="0ac83-190">Default counting reason code</span></span>
- <span data-ttu-id="0ac83-191">Показать код основания для проведения инвентаризации</span><span class="sxs-lookup"><span data-stu-id="0ac83-191">Display counting reason code</span></span>
- <span data-ttu-id="0ac83-192">Изменить код основания для проведения инвентаризации</span><span class="sxs-lookup"><span data-stu-id="0ac83-192">Edit counting reason code</span></span>

