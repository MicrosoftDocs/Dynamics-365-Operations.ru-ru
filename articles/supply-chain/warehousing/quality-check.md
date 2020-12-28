---
title: Проверка качества
description: В этом разделе содержится информация о функции проверки качества. Эта функция позволяет сотрудникам склада выполнять быстрые проверки качества, когда они получают номенклатуры в область дебаркадера приемки.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSQualityCheckTemplate, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSQualityCheckResult
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: dfb71f74732d65409003c4f6f74145442a1efa3f
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4436436"
---
# <a name="quality-check"></a><span data-ttu-id="478e7-104">Проверка качества</span><span class="sxs-lookup"><span data-stu-id="478e7-104">Quality check</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="478e7-105">Функция *Проверка качества* позволяет сотрудникам склада выполнять быстрые проверки качества, когда они получают номенклатуры в область дебаркадера приемки.</span><span class="sxs-lookup"><span data-stu-id="478e7-105">The *Quality check* feature lets warehouse workers do quick spot checks for quality while they receive items to the inbound dock area.</span></span> <span data-ttu-id="478e7-106">Такие быстрые проверки полезны, когда работники проверяют упаковку или другие легко распознаваемые участки номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="478e7-106">These spot checks are beneficial when workers inspect packaging or other easily recognizable parts of an item.</span></span> <span data-ttu-id="478e7-107">Эти пошаговые руководства служат для быстрого просмотра, чтобы определить, является ли что-либо явно неисправным или поврежденным, прежде чем будут храниться запасы в своем местоположении для получения.</span><span class="sxs-lookup"><span data-stu-id="478e7-107">The feature guides workers to take a quick look to see whether anything is obviously faulty or damaged before they stock the inventory in its putaway location.</span></span>

<span data-ttu-id="478e7-108">Эта функция является альтернативой стандарту стандартному процессу проверки качества.</span><span class="sxs-lookup"><span data-stu-id="478e7-108">This feature is an alternative to the standard quality check process.</span></span> <span data-ttu-id="478e7-109">Она обеспечивает более гибкую и быструю обработку.</span><span class="sxs-lookup"><span data-stu-id="478e7-109">It offers more flexibility and faster processing.</span></span>

<span data-ttu-id="478e7-110">При использовании этой функции проверка прибытия и качества выполняется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="478e7-110">When you use this feature, the arrival and quality check occur in the following way:</span></span>

1. <span data-ttu-id="478e7-111">Когда отгрузка прибывает, работник склада регистрирует прибытие.</span><span class="sxs-lookup"><span data-stu-id="478e7-111">When a shipment arrives, a warehouse worker registers the arrival.</span></span> <span data-ttu-id="478e7-112">Работник также сканирует грузоместо для регистрации местоположения.</span><span class="sxs-lookup"><span data-stu-id="478e7-112">The worker also scans a license plate to register the location.</span></span>
1. <span data-ttu-id="478e7-113">Работник выполняет быструю проверку качества и фиксирует результат (пройдено или не пройдено) для данного грузоместа.</span><span class="sxs-lookup"><span data-stu-id="478e7-113">The worker does a quick quality check and records the result (pass or fail) for that license plate.</span></span>
1. <span data-ttu-id="478e7-114">Одно из следующих действий выполняется:</span><span class="sxs-lookup"><span data-stu-id="478e7-114">One of the following actions occurs:</span></span>

    - <span data-ttu-id="478e7-115">Если проверка качества пройдена, грузоместо принимается и направляется в местоположение прибытия как обычно.</span><span class="sxs-lookup"><span data-stu-id="478e7-115">If the quality check is passed, the license plate is accepted and guided to a receiving location, as usual.</span></span>
    - <span data-ttu-id="478e7-116">Если проверка качества не пройдена, грузоместо отклоняется, и существующая работа размещения для него перенаправляется в другое местоположение для дальнейшей проверки.</span><span class="sxs-lookup"><span data-stu-id="478e7-116">If the quality check is failed, the license plate is rejected, and existing putaway work for it is redirected to an alternate location for further inspection.</span></span> <span data-ttu-id="478e7-117">Создается новый заказ для контроля качества.</span><span class="sxs-lookup"><span data-stu-id="478e7-117">A new quality order is created.</span></span> <span data-ttu-id="478e7-118">Для просмотра заказа для контроля качества, который создан из неудачной проверки качества, перейдите в раздел **Управление запасами \> Периодические задачи \> Управление качеством \> Заказы для контроля качества**.</span><span class="sxs-lookup"><span data-stu-id="478e7-118">To view the quality order that is created from the failed quality check, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="478e7-119">Этот процесс можно также настроить таким образом, чтобы все отсканированные грузоместа немедленно находились в местоположении проверки качества.</span><span class="sxs-lookup"><span data-stu-id="478e7-119">This process can also be set up so that all scanned license plates are immediately diverted to the quality check location.</span></span>

## <a name="turn-on-the-quality-check-feature"></a><span data-ttu-id="478e7-120">Включите функцию проверки качества</span><span class="sxs-lookup"><span data-stu-id="478e7-120">Turn on the Quality check feature</span></span>

<span data-ttu-id="478e7-121">Прежде чем использовать функцию *Проверка качества*, она должна быть включена в системе.</span><span class="sxs-lookup"><span data-stu-id="478e7-121">Before you can use the *Quality check* feature, it must be turned on in your system.</span></span> <span data-ttu-id="478e7-122">Администраторы могут использовать параметры [управления компонентами](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения, если это требуется.</span><span class="sxs-lookup"><span data-stu-id="478e7-122">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="478e7-123">В рабочей области **Управление функциями** эта функция перечисляется следующими способами:</span><span class="sxs-lookup"><span data-stu-id="478e7-123">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="478e7-124">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="478e7-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="478e7-125">**Название функции:** *Проверка качества*</span><span class="sxs-lookup"><span data-stu-id="478e7-125">**Feature name:** *Quality check*</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="478e7-126">Настройка функции для примера сценария</span><span class="sxs-lookup"><span data-stu-id="478e7-126">Set up the feature for the example scenario</span></span>

<span data-ttu-id="478e7-127">В этом разделе приводятся инструкции и пример, в котором показано, как настроить функцию *Проверка качества* и подготовить примеры данных для сценария, приведенного ниже в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="478e7-127">This section provides guidelines and an example that shows how to set up the *Quality check* feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="478e7-128">Сделать образцы данных доступными</span><span class="sxs-lookup"><span data-stu-id="478e7-128">Make sample data available</span></span>

<span data-ttu-id="478e7-129">Для работы с этими [примером сценария](#example-scenario) с помощью образцов записей и значений, указанных здесь, необходимо использовать систему, в которой установлены стандартные [демонстрационные данные](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="478e7-129">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="478e7-130">Дополнительно перед началом необходимо выбрать юридическое лицо **USMF**.</span><span class="sxs-lookup"><span data-stu-id="478e7-130">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="quality-check-template"></a><a name="quality-template"></a><span data-ttu-id="478e7-131">Шаблон проверки качества</span><span class="sxs-lookup"><span data-stu-id="478e7-131">Quality check template</span></span>

<span data-ttu-id="478e7-132">Шаблон проверки качества определяет правила выполнения быстрых проверок качества на момент получения.</span><span class="sxs-lookup"><span data-stu-id="478e7-132">The quality check template defines the rules for doing quick spot checks for quality at the time of receiving.</span></span>

1. <span data-ttu-id="478e7-133">Перейдите в раздел **Управление складом \> Настройка \> Работа \> Шаблон проверки качества**.</span><span class="sxs-lookup"><span data-stu-id="478e7-133">Go to **Warehouse management \> Setup \> Work \> Quality check template**.</span></span>
1. <span data-ttu-id="478e7-134">Выберите **Создать**, чтобы добавить шаблон в сетку.</span><span class="sxs-lookup"><span data-stu-id="478e7-134">Select **New** to add a template to the grid.</span></span>
1. <span data-ttu-id="478e7-135">Задайте следующие значения, чтобы определить новый шаблон:</span><span class="sxs-lookup"><span data-stu-id="478e7-135">Set the following values to define the new template:</span></span>

    - <span data-ttu-id="478e7-136">**Имя шаблона проверки качества:** *Проверка дебаркадера*</span><span class="sxs-lookup"><span data-stu-id="478e7-136">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="478e7-137">Введите имя, определяющее политики, применяемые для этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="478e7-137">Enter a name that identifies the policies applied for this template.</span></span>

    - <span data-ttu-id="478e7-138">**Политика принятия:** *Запроса пользователю*</span><span class="sxs-lookup"><span data-stu-id="478e7-138">**Acceptance policy:** *Prompt user*</span></span>

        <span data-ttu-id="478e7-139">Укажите, должны ли пользователи получать запрос на получение или отклонение качества складских запасов, пока они обрабатывают работу, или должно ли качество отклоняться автоматически.</span><span class="sxs-lookup"><span data-stu-id="478e7-139">Specify whether users should be prompted to accept or reject the quality of the inventory while they process the work, or whether the quality should automatically be rejected.</span></span> <span data-ttu-id="478e7-140">Доступные параметры *Автоматически отклонять* и *Запрос пользователю*.</span><span class="sxs-lookup"><span data-stu-id="478e7-140">The available options are *Auto reject* and *Prompt user*.</span></span>

    - <span data-ttu-id="478e7-141">**Политика обработки качества:** *Создание заказа для контроля качества*</span><span class="sxs-lookup"><span data-stu-id="478e7-141">**Quality processing policy:** *Create quality order*</span></span>

        <span data-ttu-id="478e7-142">Выбор политики, которая должна использоваться при отклонении качества запасов.</span><span class="sxs-lookup"><span data-stu-id="478e7-142">Select the policy that should be used when the quality of the inventory is rejected.</span></span> <span data-ttu-id="478e7-143">Имеются следующие варианты:</span><span class="sxs-lookup"><span data-stu-id="478e7-143">The following options are available:</span></span>

        - <span data-ttu-id="478e7-144">*Создание только работы* — просто создание работы, чтобы упростить перемещение запасов.</span><span class="sxs-lookup"><span data-stu-id="478e7-144">*Create work only* – Just create work to facilitate inventory movement.</span></span>
        - <span data-ttu-id="478e7-145">*Создание заказа для контроля качества* — создание заказа для контроля качества для упрощения проверок качества.</span><span class="sxs-lookup"><span data-stu-id="478e7-145">*Create quality order* – Create a quality order to facilitate quality tests.</span></span>

    - <span data-ttu-id="478e7-146">**Проверочная группа:** *Корпус*</span><span class="sxs-lookup"><span data-stu-id="478e7-146">**Test group:** *Enclosure*</span></span>

        <span data-ttu-id="478e7-147">Указывается тестовая группа, которая должна использоваться в созданном заказе для контроля качества.</span><span class="sxs-lookup"><span data-stu-id="478e7-147">Specify the test group that should be used in the quality order that is created.</span></span> <span data-ttu-id="478e7-148">Тестовые группы настраиваются в модуле **Управление запасами**.</span><span class="sxs-lookup"><span data-stu-id="478e7-148">Test groups are set up in the **Inventory management** module.</span></span>

        <span data-ttu-id="478e7-149">Параметр **Текст с разрушением** выключен для тестовой группы.</span><span class="sxs-lookup"><span data-stu-id="478e7-149">Leave the **Destructive text** option turned off for the test group.</span></span> <span data-ttu-id="478e7-150">Этот параметр задает, будет ли образец разрушен при проведении испытаний в рамках проверочной группы.</span><span class="sxs-lookup"><span data-stu-id="478e7-150">This option defines whether the sample will be destroyed as part of the tests in the test group.</span></span> <span data-ttu-id="478e7-151">Если испытание с разрушением используется, система создает складскую проводку, когда создается заказ для контроля качества для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="478e7-151">If a destructive test is used, the system generates an inventory transaction when a quality order is created for an item.</span></span> <span data-ttu-id="478e7-152">Новая складская проводка прогнозирует уменьшение запасов на испытываемое количество.</span><span class="sxs-lookup"><span data-stu-id="478e7-152">The new inventory transaction predicts the inventory reduction for the test quantity.</span></span> <span data-ttu-id="478e7-153">Завершение заказа для контроля качества через этап проверки приведет к сокращению запасов.</span><span class="sxs-lookup"><span data-stu-id="478e7-153">The inventory reduction occurs when the quality order is completed through the validation step.</span></span> <span data-ttu-id="478e7-154">Складская проводка будет идентифицирована как заказ контроля качества.</span><span class="sxs-lookup"><span data-stu-id="478e7-154">The inventory transaction is identified as a quality order.</span></span>

### <a name="work-class--quality-check"></a><a name="work-class"></a><span data-ttu-id="478e7-155">Класс работы — проверка качества</span><span class="sxs-lookup"><span data-stu-id="478e7-155">Work class – Quality check</span></span>

<span data-ttu-id="478e7-156">Классы работы используются для определения и/или ограничения типа строк заказа на работу, которые работники склада могут обрабатывать на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="478e7-156">Work classes are used to direct and/or limit the type of work order lines that warehouse workers can process on a mobile device.</span></span>

1. <span data-ttu-id="478e7-157">Перейдите в раздел **Управление складом \> Настройка \> Работа \> Классы работы**.</span><span class="sxs-lookup"><span data-stu-id="478e7-157">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="478e7-158">Выберите **Создать** для создания класса работы.</span><span class="sxs-lookup"><span data-stu-id="478e7-158">Select **New** to create a work class.</span></span>
1. <span data-ttu-id="478e7-159">В заголовке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="478e7-159">In the header, set the following values:</span></span>

    - <span data-ttu-id="478e7-160">**Код класса работы:** *Проверка QC*</span><span class="sxs-lookup"><span data-stu-id="478e7-160">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="478e7-161">Введите имя, идентифицирующее класс работы.</span><span class="sxs-lookup"><span data-stu-id="478e7-161">Enter a name that identifies the work class.</span></span>

    - <span data-ttu-id="478e7-162">**Описание:** *Проверка QC*</span><span class="sxs-lookup"><span data-stu-id="478e7-162">**Description:** *QC Check*</span></span>

        <span data-ttu-id="478e7-163">Введите краткое описание, которое показывает, для чего используется класс работы.</span><span class="sxs-lookup"><span data-stu-id="478e7-163">Enter a short description that indicates what the work class is used for.</span></span>

    - <span data-ttu-id="478e7-164">**Тип заказа на работу:** *Проверка качества в качестве*</span><span class="sxs-lookup"><span data-stu-id="478e7-164">**Work order type:** *Quality in quality check*</span></span>

        <span data-ttu-id="478e7-165">Выбор типа заказа на работу, созданного классом работы.</span><span class="sxs-lookup"><span data-stu-id="478e7-165">Select the type of work order that is created by the work class.</span></span> <span data-ttu-id="478e7-166">При настройке работы по контролю качества всегда выбирайте уровень *Проверка качества в качестве*.</span><span class="sxs-lookup"><span data-stu-id="478e7-166">When you set up quality control work, always select *Quality in quality check*.</span></span>

1. <span data-ttu-id="478e7-167">На экспресс-вкладке **Допустимые типы местоположений размещения** оставьте поле **Тип местоположения** пустым.</span><span class="sxs-lookup"><span data-stu-id="478e7-167">On the **Valid put location types** FastTab, leave the **Location type** field blank.</span></span>

    <span data-ttu-id="478e7-168">При выборе типа местоположения вы ограничиваете местоположения, в которые номенклатуры могут быть помещены после их комплектации.</span><span class="sxs-lookup"><span data-stu-id="478e7-168">If you select a location type, you limit the locations where items can be put after they are picked.</span></span> <span data-ttu-id="478e7-169">Это поле используется, когда директива места хранения пытается разрешить местонахождение, или если работник склада вручную предоставляет местонахождение для пункта меню мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="478e7-169">This field is used when a location directive tries to resolve the location, or when a warehouse worker manually specifies the location for the mobile device menu item.</span></span>

<span data-ttu-id="478e7-170">Дополнительные сведения о классах работы и порядке их создания см. в разделе [Создание класса работы](tasks/create-work-class.md).</span><span class="sxs-lookup"><span data-stu-id="478e7-170">For more information about work classes and how to create them, see [Create a work class](tasks/create-work-class.md).</span></span>

### <a name="work-template"></a><span data-ttu-id="478e7-171">Шаблон работы</span><span class="sxs-lookup"><span data-stu-id="478e7-171">Work template</span></span>

<span data-ttu-id="478e7-172">Рабочие шаблоны позволяют определить рабочие операции, которые должны быть выполнены на складе.</span><span class="sxs-lookup"><span data-stu-id="478e7-172">Work templates let you define the work operations that must be performed in the warehouse.</span></span> <span data-ttu-id="478e7-173">Как правило, рабочие операции склада состоят из пары действий: рабочий склада комплектует запасы в наличии в одном расположении и помещает скомплектованные запасы в другом расположении.</span><span class="sxs-lookup"><span data-stu-id="478e7-173">Typically, warehouse work operations consist of a pair of actions: a warehouse worker picks on-hand inventory up in one location and then puts the picked inventory down in another location.</span></span> <span data-ttu-id="478e7-174">Шаблон работы для контроля качества определяет рабочие операции для выполнения проверок качества.</span><span class="sxs-lookup"><span data-stu-id="478e7-174">A work template for quality control defines the work operations for doing quality checks.</span></span>

#### <a name="purchase-orders"></a><span data-ttu-id="478e7-175">Заказы на покупку</span><span class="sxs-lookup"><span data-stu-id="478e7-175">Purchase orders</span></span>

1. <span data-ttu-id="478e7-176">Перейдите в раздел **Управление складом \> Настройка \> Работа \> Шаблоны работ**.</span><span class="sxs-lookup"><span data-stu-id="478e7-176">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="478e7-177">В заголовке задайте в поле **Тип заказа на работу** значение *Заказы на покупку*.</span><span class="sxs-lookup"><span data-stu-id="478e7-177">In the header, set the **Work order type** field to *Purchase orders*.</span></span>
1. <span data-ttu-id="478e7-178">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="478e7-178">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="478e7-179">Выберите шаблон работы, который должен включать шаг проверки качества.</span><span class="sxs-lookup"><span data-stu-id="478e7-179">Select a work template that should include a quality check step.</span></span> <span data-ttu-id="478e7-180">В разделе **Обзор** в поле **Шаблон работы** выберите *Поступление 51 PO*.</span><span class="sxs-lookup"><span data-stu-id="478e7-180">In the **Overview** section, in the **Work template** field, select *51 PO Receipt*.</span></span>
1. <span data-ttu-id="478e7-181">В разделе **Сведения шаблона работы** обратите внимание, что сетка содержит две существующие строки: одну для *Комплектация* и одну для *Размещение*.</span><span class="sxs-lookup"><span data-stu-id="478e7-181">In the **Work template details** section, notice that the grid has two existing lines: one for *Pick* and one for *Put*.</span></span>
1. <span data-ttu-id="478e7-182">В разделе **Сведения шаблона работы** выберите **Создать**, чтобы добавить строку для контроля качества в сетку.</span><span class="sxs-lookup"><span data-stu-id="478e7-182">In the **Work template details** section, select **New** to add a row for quality control to the grid.</span></span> <span data-ttu-id="478e7-183">Обратите внимание, что в поле **Номер строки** для новой строки указано значение *3*.</span><span class="sxs-lookup"><span data-stu-id="478e7-183">Notice that the **Line number** field for the new line is set to *3*.</span></span>
1. <span data-ttu-id="478e7-184">В новой строке установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="478e7-184">On the new line, set the following values.</span></span> <span data-ttu-id="478e7-185">Примите для остальных полей значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="478e7-185">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="478e7-186">**Тип работы:** *Проверка качества*</span><span class="sxs-lookup"><span data-stu-id="478e7-186">**Work type:** *Quality check*</span></span>
    - <span data-ttu-id="478e7-187">**Код класса работы:** *Покупка*</span><span class="sxs-lookup"><span data-stu-id="478e7-187">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="478e7-188">**Имя шаблона проверки качества:** *Проверка дебаркадера*</span><span class="sxs-lookup"><span data-stu-id="478e7-188">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="478e7-189">Выберите уникальный идентификатор для класса работы.</span><span class="sxs-lookup"><span data-stu-id="478e7-189">Select the unique ID for the work class.</span></span> <span data-ttu-id="478e7-190">Используйте это значение для настройки пунктов меню на мобильном устройстве и типов работ, которые могут обрабатываться с помощью этих пунктов меню.</span><span class="sxs-lookup"><span data-stu-id="478e7-190">You use this value to configure the menu items on the mobile device and the types of work that those menu items can process.</span></span>

1. <span data-ttu-id="478e7-191">На панели операций выберите **Сохранить**, чтобы сохранить работу на данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="478e7-191">On the Action Pane, select **Save** to save your work so far.</span></span>

    <span data-ttu-id="478e7-192">Вы получите информационное сообщение "Недопустимо. Проверка качества должна идти сразу после комплектации".</span><span class="sxs-lookup"><span data-stu-id="478e7-192">You receive an informational message that states, "Invalid - Quality check must come directly after a pick."</span></span> <span data-ttu-id="478e7-193">Поэтому необходимо изменить значение **Номер строки** для строки, которая только что была добавлена.</span><span class="sxs-lookup"><span data-stu-id="478e7-193">Therefore, you must change the **Line number** value for the line that you just added.</span></span>

1. <span data-ttu-id="478e7-194">Чтобы изменить значение **Номер строки** для новой строки, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="478e7-194">Follow these steps to change the **Line number** value for the new line:</span></span>

    1. <span data-ttu-id="478e7-195">В разделе **Сведения шаблона работы** выберите строку, в которой для поля **Тип работы** задано значение *Проверка качества*.</span><span class="sxs-lookup"><span data-stu-id="478e7-195">In the **Work template details** section, select the line where the **Work type** field is set to *Quality check*.</span></span>
    2. <span data-ttu-id="478e7-196">Нажмите кнопку **Вверх** или **Вниз**, чтобы переместить строку *Проверка качества*, чтобы она отображалась после строки *Комплектация*.</span><span class="sxs-lookup"><span data-stu-id="478e7-196">Select the **Move up** or **Move down** button to move the *Quality check* line so that it's after the *Pick* line.</span></span>

1. <span data-ttu-id="478e7-197">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="478e7-197">On the Action Pane, select **Save**.</span></span>

#### <a name="quality-in-quality-check"></a><span data-ttu-id="478e7-198">Качество при проверке качества</span><span class="sxs-lookup"><span data-stu-id="478e7-198">Quality in quality check</span></span>

<span data-ttu-id="478e7-199">Затем создайте шаблон работы для проверки качества.</span><span class="sxs-lookup"><span data-stu-id="478e7-199">Next, create a work template for the quality check.</span></span>

1. <span data-ttu-id="478e7-200">В заголовке страницы **Шаблоны работы** измените значение в поле **Тип заказа на работу** значение *Проверка качества в качестве*.</span><span class="sxs-lookup"><span data-stu-id="478e7-200">In the header of the **Work templates** page, change the value of the **Work order type** field to *Quality in quality check*.</span></span>
1. <span data-ttu-id="478e7-201">На панели операций выберите **Создать**, чтобы добавить строку в сетку в разделе **Обзор**.</span><span class="sxs-lookup"><span data-stu-id="478e7-201">On the Action Pane, select **New** to add a row to the grid in the **Overview** section.</span></span>
1. <span data-ttu-id="478e7-202">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="478e7-202">In the new row, set the following values:</span></span>

    - <span data-ttu-id="478e7-203">**Шаблон работы:** *51 Проверка качества*</span><span class="sxs-lookup"><span data-stu-id="478e7-203">**Work template:** *51 Quality Check*</span></span>

        <span data-ttu-id="478e7-204">Введите имя шаблона.</span><span class="sxs-lookup"><span data-stu-id="478e7-204">Enter a name for the template.</span></span>

    - <span data-ttu-id="478e7-205">**Описание шаблона работы:** *51 Проверка качества*</span><span class="sxs-lookup"><span data-stu-id="478e7-205">**Work template description:** *51 Quality Check*</span></span>

1. <span data-ttu-id="478e7-206">НА панели действий выберите **Сохранить**, чтобы сделать доступным раздел **Сведения шаблона работы**.</span><span class="sxs-lookup"><span data-stu-id="478e7-206">On the Action Pane, select **Save** to make the **Work template details** section available.</span></span>
1. <span data-ttu-id="478e7-207">Пока новый шаблон все еще выбран в разделе **Обзор**, выберите **Создать** в разделе **Сведения шаблона работы**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="478e7-207">While the new template is still selected in the **Overview** section, select **New** in the **Work template details** section to add a row to the grid there.</span></span>
1. <span data-ttu-id="478e7-208">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="478e7-208">In the new row, set the following values:</span></span>

    - <span data-ttu-id="478e7-209">**Тип работы:** *Комплектация*</span><span class="sxs-lookup"><span data-stu-id="478e7-209">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="478e7-210">**Код класса работы:** *Проверка QC*</span><span class="sxs-lookup"><span data-stu-id="478e7-210">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="478e7-211">Выберите имя [класса работы](#work-class), созданного ранее для работы по контролю качества.</span><span class="sxs-lookup"><span data-stu-id="478e7-211">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="478e7-212">В разделе **Сведения шаблона работы** выберите **Создать**, чтобы добавить новую строку.</span><span class="sxs-lookup"><span data-stu-id="478e7-212">In the **Work template details** section, select **New** again to add another row.</span></span>
1. <span data-ttu-id="478e7-213">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="478e7-213">In the new row, set the following values:</span></span>

    - <span data-ttu-id="478e7-214">**Тип работы:** *Размещение*</span><span class="sxs-lookup"><span data-stu-id="478e7-214">**Work type:** *Put*</span></span>
    - <span data-ttu-id="478e7-215">**Код класса работы:** *Проверка QC*</span><span class="sxs-lookup"><span data-stu-id="478e7-215">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="478e7-216">Выберите имя [класса работы](#work-class), созданного ранее для работы по контролю качества.</span><span class="sxs-lookup"><span data-stu-id="478e7-216">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="478e7-217">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="478e7-217">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="478e7-218">Дополнительные сведения о шаблонах работы см. в разделе [Контроль работы склада с шаблонами работы и директивами для мест хранения](control-warehouse-location-directives.md)</span><span class="sxs-lookup"><span data-stu-id="478e7-218">For more information about work templates, see [Control warehouse work by using work templates and location directives](control-warehouse-location-directives.md)</span></span>

### <a name="location-directive--quality-failures"></a><span data-ttu-id="478e7-219">Директива местоположения — несоответствия качества</span><span class="sxs-lookup"><span data-stu-id="478e7-219">Location directive – Quality failures</span></span>

<span data-ttu-id="478e7-220">Директивы для мест хранения — это правила, с помощью которых можно определить места комплектации и размещения для перемещения запасов.</span><span class="sxs-lookup"><span data-stu-id="478e7-220">Location directives are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="478e7-221">Например, в проводке заказа на продажу директива местонахождения определяет места комплектации и размещения номенклатур.</span><span class="sxs-lookup"><span data-stu-id="478e7-221">For example, in a sales order transaction, a location directive determines where the items will be picked and where the picked items will be put.</span></span> <span data-ttu-id="478e7-222">Необходимо настроить правило директивы местоположения, чтобы определить, как будут обрабатываться неудачные проверки качества.</span><span class="sxs-lookup"><span data-stu-id="478e7-222">You must configure a location directive rule to define how failed quality checks will be handled.</span></span>

1. <span data-ttu-id="478e7-223">Перейдите в раздел **Управление складом \> Настройка \> Директивы местонахождения**.</span><span class="sxs-lookup"><span data-stu-id="478e7-223">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="478e7-224">В левой области задайте в поле **Тип заказа на работу** значение *Заказы на покупку*, чтобы работать с директивами местоположения этого типа.</span><span class="sxs-lookup"><span data-stu-id="478e7-224">In the left pane, set the **Work order type** field to *Purchase orders* to work with location directives of that type.</span></span>
1. <span data-ttu-id="478e7-225">На панели операций выберите **Создать** для создания директивы местоположения для проверок качества.</span><span class="sxs-lookup"><span data-stu-id="478e7-225">On the Action Pane, select **New** to create a location directive for quality checks.</span></span>
1. <span data-ttu-id="478e7-226">В заголовке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="478e7-226">In the header, set the following values:</span></span>

    - <span data-ttu-id="478e7-227">**Порядковый номер:** примите значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="478e7-227">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="478e7-228">**Имя:** *51 На контроль качества*</span><span class="sxs-lookup"><span data-stu-id="478e7-228">**Name:** *51 To Quality*</span></span>

1. <span data-ttu-id="478e7-229">На экспресс-вкладке **Директивы местоположения** установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="478e7-229">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="478e7-230">Примите для остальных полей значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="478e7-230">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="478e7-231">**Тип работы:** *Размещение*</span><span class="sxs-lookup"><span data-stu-id="478e7-231">**Work type:** *Put*</span></span>
    - <span data-ttu-id="478e7-232">**Сайт:** *5*</span><span class="sxs-lookup"><span data-stu-id="478e7-232">**Site:** *5*</span></span>
    - <span data-ttu-id="478e7-233">**Склад:** *51*</span><span class="sxs-lookup"><span data-stu-id="478e7-233">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="478e7-234">На панели действий выберите **Сохранить**, чтобы сохранить директиву и сделать доступной экспресс-вкладку **Строки**.</span><span class="sxs-lookup"><span data-stu-id="478e7-234">On the Action Pane select **Save** to save your directive and make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="478e7-235">На экспресс-вкладке **Строки** выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="478e7-235">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="478e7-236">В новой строке установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="478e7-236">On the new line, set the following values.</span></span> <span data-ttu-id="478e7-237">Примите для остальных полей значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="478e7-237">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="478e7-238">**Количество "От":** *1*</span><span class="sxs-lookup"><span data-stu-id="478e7-238">**From quantity:** *1*</span></span>
    - <span data-ttu-id="478e7-239">**Количество "До":** *1000000*</span><span class="sxs-lookup"><span data-stu-id="478e7-239">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="478e7-240">На панели действий выберите **Сохранить**, чтобы сохранить новую строку и сделать доступной экспресс-вкладку **Действия директивы местоположения**.</span><span class="sxs-lookup"><span data-stu-id="478e7-240">On the Action Pane, select **Save** to save the new line and make the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="478e7-241">Пока новая строка по-прежнему выбрана на экспресс-вкладке **Строки**, выберите **Создать** на экспресс-вкладке **Действия директивы местоположения**, чтобы добавить строку в сетку, чтобы можно было настроить действие для строки.</span><span class="sxs-lookup"><span data-stu-id="478e7-241">While the new line is still selected on the **Lines** FastTab, select **New** on the **Location directive actions** FastTab to add a row to the grid there, so that you can set up an action for the line.</span></span>
1. <span data-ttu-id="478e7-242">В новой строке задайте для поля **Имя** значение *Качество*.</span><span class="sxs-lookup"><span data-stu-id="478e7-242">In the new row, set the **Name** field to *Quality*.</span></span> <span data-ttu-id="478e7-243">Примите для остальных полей значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="478e7-243">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="478e7-244">На панели действий выберите **Сохранить**, чтобы сделать доступной кнопку **Изменить запрос** на экспресс-вкладке **Действия директивы местоположения**.</span><span class="sxs-lookup"><span data-stu-id="478e7-244">On the Action Pane, select **Save** to make the **Edit query** button on the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="478e7-245">Пока добавленная строка все еще выбрана на экспресс-вкладке **Действия директивы местоположения**, выберите **Изменить запрос**, чтобы открыть диалоговое окно, в котором можно изменить запрос для действия.</span><span class="sxs-lookup"><span data-stu-id="478e7-245">While the line that you just added is still selected on the **Location directive actions** FastTab, select **Edit query** to open a dialog box where you can edit the query for the action.</span></span>
1. <span data-ttu-id="478e7-246">На вкладке **Диапазон** выберите **Добавить**, чтобы добавить строку в запрос.</span><span class="sxs-lookup"><span data-stu-id="478e7-246">On the **Range** tab, select **Add** to add a row to the query.</span></span>
1. <span data-ttu-id="478e7-247">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="478e7-247">In the new row, set the following values:</span></span>

    - <span data-ttu-id="478e7-248">**Таблица:** *Местонахождения*</span><span class="sxs-lookup"><span data-stu-id="478e7-248">**Table:** *Locations*</span></span>
    - <span data-ttu-id="478e7-249">**Производная таблица:** *Местонахождения*</span><span class="sxs-lookup"><span data-stu-id="478e7-249">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="478e7-250">**Поле:** *Местонахождение*</span><span class="sxs-lookup"><span data-stu-id="478e7-250">**Field:** *Location*</span></span>
    - <span data-ttu-id="478e7-251">**Критерии:** *QMS*</span><span class="sxs-lookup"><span data-stu-id="478e7-251">**Criteria:** *QMS*</span></span>

    <span data-ttu-id="478e7-252">Местоположение *QMS* является складским местоположением для качества.</span><span class="sxs-lookup"><span data-stu-id="478e7-252">The *QMS* location is a warehouse location for quality.</span></span>

1. <span data-ttu-id="478e7-253">Выберите **OK**, чтобы закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="478e7-253">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="478e7-254">Необходимо изменить последовательность директив местоположения заказов на покупку для склада *51*.</span><span class="sxs-lookup"><span data-stu-id="478e7-254">You must now change the sequence of purchase order location directives for warehouse *51*.</span></span> <span data-ttu-id="478e7-255">Сохраните новую директиву местоположения *51 На контроль качества*, обновите страницу и выберите в списке директиву местоположения.</span><span class="sxs-lookup"><span data-stu-id="478e7-255">Save the new *51 To Quality* location directive, refresh the page, and select the location directive in the list.</span></span> <span data-ttu-id="478e7-256">Затем воспользуйтесь кнопками **Вверх** и **Вниз** на панели операций, чтобы разместить директиву местоположения для склада *51* в следующем порядке.</span><span class="sxs-lookup"><span data-stu-id="478e7-256">Then use the **Move up** and **Move down** buttons on the Action Pane to put the location directive for warehouse *51* in the following order.</span></span> <span data-ttu-id="478e7-257">(Перед выбором **Вверх** или **Вниз**, следует выбрать в списке директиву местоположения.)</span><span class="sxs-lookup"><span data-stu-id="478e7-257">(Before you select **Move up** or **Move down**, you must select a location directive in the list.)</span></span>

    1. <span data-ttu-id="478e7-258">51 На контроль качеству</span><span class="sxs-lookup"><span data-stu-id="478e7-258">51 To Quality</span></span>
    2. <span data-ttu-id="478e7-259">51 PO Директива</span><span class="sxs-lookup"><span data-stu-id="478e7-259">51 PO Direct</span></span>
    3. <span data-ttu-id="478e7-260">51 QMS</span><span class="sxs-lookup"><span data-stu-id="478e7-260">51 QMS</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="478e7-261">Пункты меню мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="478e7-261">Mobile device menu items</span></span>

<span data-ttu-id="478e7-262">Настройте пункт меню, чтобы мобильные устройства могли выполнить функцию **Проверка качества**.</span><span class="sxs-lookup"><span data-stu-id="478e7-262">Configure a menu item so that mobile devices can perform the **Quality Check** function.</span></span>

#### <a name="purchase-putaway"></a><span data-ttu-id="478e7-263">Размещение покупки</span><span class="sxs-lookup"><span data-stu-id="478e7-263">Purchase putaway</span></span>

1. <span data-ttu-id="478e7-264">Перейдите в раздел **Управление складом \> Настройка \> Мобильное устройство \> Пункты меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="478e7-264">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="478e7-265">В списке выберите пункт меню **Размещение покупки**.</span><span class="sxs-lookup"><span data-stu-id="478e7-265">In the list, select the **Purchase put-away** menu item.</span></span>
1. <span data-ttu-id="478e7-266">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="478e7-266">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="478e7-267">В разделе **Классы работ** выберите **Создать**, чтобы добавить строку в сетку.</span><span class="sxs-lookup"><span data-stu-id="478e7-267">In the **Work classes** section, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="478e7-268">В новой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="478e7-268">In the new row, set the following values:</span></span>

    - <span data-ttu-id="478e7-269">**Код класса работы:** *Проверка QC*</span><span class="sxs-lookup"><span data-stu-id="478e7-269">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="478e7-270">Введите имя [класса работы](#work-class), созданного ранее для работы по контролю качества.</span><span class="sxs-lookup"><span data-stu-id="478e7-270">Enter the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

    - <span data-ttu-id="478e7-271">**Тип заказа на работу:** *Проверка качества в качестве*</span><span class="sxs-lookup"><span data-stu-id="478e7-271">**Work order type:** *Quality in quality check*</span></span>

1. <span data-ttu-id="478e7-272">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="478e7-272">On the Action Pane, select **Save**.</span></span>

#### <a name="purchase-order-line-receiving"></a><span data-ttu-id="478e7-273">Получение строки заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="478e7-273">Purchase order line receiving</span></span>

1. <span data-ttu-id="478e7-274">Перейдите в раздел **Управление складом \> Настройка \> Мобильное устройство \> Пункты меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="478e7-274">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="478e7-275">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="478e7-275">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="478e7-276">В заголовке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="478e7-276">In the header, set the following values:</span></span>

    - <span data-ttu-id="478e7-277">**Название пункта меню:** *Получение строки заказа на покупку*</span><span class="sxs-lookup"><span data-stu-id="478e7-277">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="478e7-278">**Заголовок:** *Получение строки заказа на покупку*</span><span class="sxs-lookup"><span data-stu-id="478e7-278">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="478e7-279">**Режим:** *Работа*</span><span class="sxs-lookup"><span data-stu-id="478e7-279">**Mode:** *Work*</span></span>
    - <span data-ttu-id="478e7-280">**Использовать существующую работу:** *Нет*</span><span class="sxs-lookup"><span data-stu-id="478e7-280">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="478e7-281">На экспресс-вкладке **Общие** установите следующие значения.</span><span class="sxs-lookup"><span data-stu-id="478e7-281">On the **General** FastTab, set the following values.</span></span> <span data-ttu-id="478e7-282">Примите для остальных полей значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="478e7-282">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="478e7-283">**Процесс создания работы:** *Получение строки заказа на покупку и размещение*</span><span class="sxs-lookup"><span data-stu-id="478e7-283">**Work creation process:** *Purchase order line receiving and put away*</span></span>
    - <span data-ttu-id="478e7-284">**Создать грузоместо:** *Да*</span><span class="sxs-lookup"><span data-stu-id="478e7-284">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="478e7-285">**Шаблон работы:** *51 PO Поступление*</span><span class="sxs-lookup"><span data-stu-id="478e7-285">**Work template:** *51 PO Receipt*</span></span>

1. <span data-ttu-id="478e7-286">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="478e7-286">On the Action Pane, select **Save**.</span></span>

#### <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="478e7-287">Добавление элемента меню в меню мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="478e7-287">Add the menu item to a mobile device menu</span></span>

1. <span data-ttu-id="478e7-288">Перейдите в раздел **Управление складом \> Настройка \> Мобильное устройство \> Меню мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="478e7-288">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="478e7-289">Выберите меню **Входящие** в левой области.</span><span class="sxs-lookup"><span data-stu-id="478e7-289">In the left pane, select the **Inbound** menu.</span></span>
1. <span data-ttu-id="478e7-290">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="478e7-290">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="478e7-291">В столбце **Доступные меню и пункты меню** найдите и выберите новый пункт меню **Получение строки заказа на покупку**.</span><span class="sxs-lookup"><span data-stu-id="478e7-291">In the **Available menus and menu items** column, select the new **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="478e7-292">Выберите кнопку со стрелкой вправо, чтобы переместить пункт **Получение строки заказа на покупку** в столбец **Структура меню**.</span><span class="sxs-lookup"><span data-stu-id="478e7-292">Select the right arrow button to move **PO line receiving** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="478e7-293">В столбце **Структура меню** выберите **Получение строки заказа на покупку**, а затем нажмите кнопку "стрелка вверх" или "стрелка вниз", чтобы переместить пункт меню в нужную позицию в меню мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="478e7-293">In the **Menu structure** column, select **PO line receiving**, and then select the up arrow or down arrow button to move the menu item to the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="478e7-294">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="478e7-294">On the Action Pane, select **Save**.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="478e7-295">Пример сценария</span><span class="sxs-lookup"><span data-stu-id="478e7-295">Example scenario</span></span>

<span data-ttu-id="478e7-296">После того как вы сделали все ранее описанные образцы данных доступными и настроили их, вы можете работать с этим сценарием, чтобы попробовать функцию *Проверка качества*.</span><span class="sxs-lookup"><span data-stu-id="478e7-296">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Quality check* feature.</span></span> <span data-ttu-id="478e7-297">Значения, показанные в этом сценарии, предполагают, что вы работаете с использованием стандартных демонстрационных данных, выбрано юридическое лицо **USMF** и подготовлены примеры записей, которые описаны ранее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="478e7-297">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="478e7-298">Этот сценарий также служит в качестве примера, показывающего, как функция может использоваться в производственном параметре.</span><span class="sxs-lookup"><span data-stu-id="478e7-298">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="478e7-299">Создание заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="478e7-299">Create a purchase order</span></span>

1. <span data-ttu-id="478e7-300">Перейдите в раздел **Закупки и источники \> Заказы на покупку \> Все заказы на покупку**.</span><span class="sxs-lookup"><span data-stu-id="478e7-300">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="478e7-301">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="478e7-301">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="478e7-302">В диалоговом окне **Создание заказа на покупку** установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="478e7-302">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="478e7-303">**Счет поставщика:** *104*</span><span class="sxs-lookup"><span data-stu-id="478e7-303">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="478e7-304">**Склад:** *51*</span><span class="sxs-lookup"><span data-stu-id="478e7-304">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="478e7-305">Выберите **ОК**, чтобы закрыть диалоговое окно и открыть новый заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="478e7-305">Select **OK** to close the dialog box and open the new purchase order.</span></span>
1. <span data-ttu-id="478e7-306">На экспресс-вкладке **Строки заказа на покупку** сетка содержит новую пустую строку.</span><span class="sxs-lookup"><span data-stu-id="478e7-306">On the **Purchase order lines** FastTab, the grid contains a new, blank line.</span></span> <span data-ttu-id="478e7-307">В этой строке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="478e7-307">On this line, set the following values:</span></span>

    - <span data-ttu-id="478e7-308">**Код номенклатуры:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="478e7-308">**Item number:** *M9203*</span></span>
    - <span data-ttu-id="478e7-309">**Количество:** *3*</span><span class="sxs-lookup"><span data-stu-id="478e7-309">**Quantity:** *3*</span></span>
    - <span data-ttu-id="478e7-310">**Единица измерения:** *PL*</span><span class="sxs-lookup"><span data-stu-id="478e7-310">**Unit:** *PL*</span></span>

1. <span data-ttu-id="478e7-311">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="478e7-311">On the Action Pane, select **Save**.</span></span>

### <a name="process-quality-check-receiving"></a><span data-ttu-id="478e7-312">Получение проверки качества процесса</span><span class="sxs-lookup"><span data-stu-id="478e7-312">Process quality check receiving</span></span>

<span data-ttu-id="478e7-313">После создания заказа на покупку его можно получить, используя пункт меню **Получение строки заказа на покупку** и функцию *Проверка качества*.</span><span class="sxs-lookup"><span data-stu-id="478e7-313">After the purchase order has been created, it can be received by using the **PO line receiving** menu item and the functionality of the *Quality check* feature.</span></span>

#### <a name="receive-pallet-1"></a><span data-ttu-id="478e7-314">Получить палету 1</span><span class="sxs-lookup"><span data-stu-id="478e7-314">Receive pallet 1</span></span>

1. <span data-ttu-id="478e7-315">Выполните вход в приложение склада как пользователь на складе *51*.</span><span class="sxs-lookup"><span data-stu-id="478e7-315">Sign in to the warehouse app as a user for warehouse *51*.</span></span> <span data-ttu-id="478e7-316">(Введите *51* в качестве ИД пользователя и *1* в качестве пароля.)</span><span class="sxs-lookup"><span data-stu-id="478e7-316">(Enter *51* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="478e7-317">Перейдите **Входящие \> Получение строки заказа на покупку**.</span><span class="sxs-lookup"><span data-stu-id="478e7-317">Go to **Inbound \> PO line receiving**.</span></span>
1. <span data-ttu-id="478e7-318">В поле **PONUM** введите свой номер заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="478e7-318">In the **PONUM** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="478e7-319">Подтвердите номер заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="478e7-319">Confirm the purchase order number.</span></span>
1. <span data-ttu-id="478e7-320">В поле **LINENUM** введите номер строки из принимаемого заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="478e7-320">In the **LINENUM** field, enter the number of the purchase order line that is being received.</span></span> <span data-ttu-id="478e7-321">Так как в этом случае в заказе только одна строка, введите *1* в поле **LINENUM** для каждого шага получения.</span><span class="sxs-lookup"><span data-stu-id="478e7-321">Because the order has only one line in this scenario, you will enter *1* in the **LINENUM** field for each receiving step.</span></span>
1. <span data-ttu-id="478e7-322">Подтвердите номер строки.</span><span class="sxs-lookup"><span data-stu-id="478e7-322">Confirm the line number.</span></span>
1. <span data-ttu-id="478e7-323">В поле **КОЛ-ВО** введите количество для получения.</span><span class="sxs-lookup"><span data-stu-id="478e7-323">In the **QTY** field, enter the quantity to receive.</span></span> <span data-ttu-id="478e7-324">Поскольку заказ на покупку состоит из трех палет (*PL*) в этом сценарии, и существует три шага получения, введите *1* в поле **КОЛ-ВО** для каждого шага получения.</span><span class="sxs-lookup"><span data-stu-id="478e7-324">Because the purchase order is for three pallets (*PL*) in this scenario, and there are three receiving steps, you will enter *1* in the **QTY** field for each receiving step.</span></span>
1. <span data-ttu-id="478e7-325">Подтвердите количество.</span><span class="sxs-lookup"><span data-stu-id="478e7-325">Confirm the quantity.</span></span>

    <span data-ttu-id="478e7-326">На странице **Проверка качества**, которая отображается, нет полей ввода.</span><span class="sxs-lookup"><span data-stu-id="478e7-326">The **Quality check** page that appears has no entry fields.</span></span> <span data-ttu-id="478e7-327">На ней имеется только подтверждение (флажок) и кнопка меню (**≡**) в верхней части окна.</span><span class="sxs-lookup"><span data-stu-id="478e7-327">It has only the confirmation (check mark) button at the bottom and the Menu button (**≡**) at the top.</span></span> <span data-ttu-id="478e7-328">(Кнопка меню иногда называется "гамбургер".) Для ускорения процесса проверки качества, когда палета проходит проверку качества, пользователь только подтверждает страницу **Проверка качества**.</span><span class="sxs-lookup"><span data-stu-id="478e7-328">(The Menu button is sometimes referred to as the hamburger or the hamburger button.) To expedite the quality check process, when the pallet passes the quality check, the user just confirms the **Quality check** page.</span></span>

    <span data-ttu-id="478e7-329">![Страница проверки качества](media/quality-check.png "Страница проверки качества")</span><span class="sxs-lookup"><span data-stu-id="478e7-329">![Quality check page](media/quality-check.png "Quality check page")</span></span>

1. <span data-ttu-id="478e7-330">Нажмите кнопку подтверждения, чтобы перейти с проверки качества для палеты 1 из строки 1.</span><span class="sxs-lookup"><span data-stu-id="478e7-330">Select the confirmation button to pass the quality check for pallet 1 from line 1.</span></span>

    <span data-ttu-id="478e7-331">Будет открыта страница **Заказы на покупку: размещение**, на которой отображаются подробные сведения о размещенной работе:</span><span class="sxs-lookup"><span data-stu-id="478e7-331">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="478e7-332">**LOC:** местоположение определяется системой</span><span class="sxs-lookup"><span data-stu-id="478e7-332">**LOC:** The system determined location</span></span>

        <span data-ttu-id="478e7-333">Это местоположение указывает местоположение размещения для получения заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="478e7-333">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="478e7-334">**LP:** созданный системой код грузоместа</span><span class="sxs-lookup"><span data-stu-id="478e7-334">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="478e7-335">**Номенклатура:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="478e7-335">**Item:** *M9203*</span></span>
    - <span data-ttu-id="478e7-336">**Кол-во:** *1 PL: 100 шт.*</span><span class="sxs-lookup"><span data-stu-id="478e7-336">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="478e7-337">Отображается также описание номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="478e7-337">The item description is also shown.</span></span>

1. <span data-ttu-id="478e7-338">Подтвердите работу по размещению.</span><span class="sxs-lookup"><span data-stu-id="478e7-338">Confirm the putaway work.</span></span>

    <span data-ttu-id="478e7-339">На странице **Задачи** для получения строки заказа на покупку вы получаете сообщение "Работа завершена".</span><span class="sxs-lookup"><span data-stu-id="478e7-339">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="478e7-340">Поле **LINENUM** доступно для того, чтобы можно было начать получать следующую палету.</span><span class="sxs-lookup"><span data-stu-id="478e7-340">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

#### <a name="receive-pallet-2"></a><span data-ttu-id="478e7-341">Получить палету 2</span><span class="sxs-lookup"><span data-stu-id="478e7-341">Receive pallet 2</span></span>

<span data-ttu-id="478e7-342">В этом случае палета 2 будет отклонена.</span><span class="sxs-lookup"><span data-stu-id="478e7-342">For this scenario, pallet 2 will be rejected.</span></span>

1. <span data-ttu-id="478e7-343">В поле **LINENUM** введите *1* и подтвердите номер строки.</span><span class="sxs-lookup"><span data-stu-id="478e7-343">In the **LINENUM** field, enter *1*, and confirm the line number.</span></span>
1. <span data-ttu-id="478e7-344">Поле **КОЛ-ВО** теперь доступно.</span><span class="sxs-lookup"><span data-stu-id="478e7-344">The **QTY** field is now available.</span></span> <span data-ttu-id="478e7-345">Введите *1* и подтвердите количество.</span><span class="sxs-lookup"><span data-stu-id="478e7-345">Enter *1*, and confirm the quantity.</span></span>

    <span data-ttu-id="478e7-346">Отображается страница **Проверка качества**.</span><span class="sxs-lookup"><span data-stu-id="478e7-346">The **Quality check** page appears.</span></span> <span data-ttu-id="478e7-347">Для данного получения палета будет отклонена по качеству, она будет помещена в местоположение качества *QMS*.</span><span class="sxs-lookup"><span data-stu-id="478e7-347">For this receipt, the pallet will be rejected for quality, and it will be put into the *QMS* quality location.</span></span>

1. <span data-ttu-id="478e7-348">Выберите кнопку меню (**≡**) в верхней части страницы, а затем в меню выберите **Отклонить**.</span><span class="sxs-lookup"><span data-stu-id="478e7-348">Select the Menu button (**≡**) at the top of the page, and then, on the menu, select **Reject**.</span></span>
1. <span data-ttu-id="478e7-349">На отображаемой странице **Задача** введите **QMS** местоположения *Размещение* для отправки палеты для дальнейшей проверки.</span><span class="sxs-lookup"><span data-stu-id="478e7-349">On the **Task** page that appears, enter **QMS** as the *Put* location to send the pallet to for further inspection.</span></span>

    <span data-ttu-id="478e7-350">Будет открыта страница **Проверка качества в качестве: размещение**, на которой отображаются подробные сведения о размещенной работе:</span><span class="sxs-lookup"><span data-stu-id="478e7-350">The **Quality in quality check: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="478e7-351">**LOC:** *QMS*</span><span class="sxs-lookup"><span data-stu-id="478e7-351">**LOC:** *QMS*</span></span>

        <span data-ttu-id="478e7-352">Это местоположение указывает местоположение размещения для получения отклоненного качества.</span><span class="sxs-lookup"><span data-stu-id="478e7-352">This location is the designated putaway location for rejected quality receiving.</span></span>

    - <span data-ttu-id="478e7-353">**LP:** созданный системой код грузоместа</span><span class="sxs-lookup"><span data-stu-id="478e7-353">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="478e7-354">**Номенклатура:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="478e7-354">**Item:** *M9203*</span></span>
    - <span data-ttu-id="478e7-355">**Кол-во:** *1 PL: 100 шт.*</span><span class="sxs-lookup"><span data-stu-id="478e7-355">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="478e7-356">Отображается также описание номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="478e7-356">The item description is also shown.</span></span>

1. <span data-ttu-id="478e7-357">Подтвердите работу по размещению.</span><span class="sxs-lookup"><span data-stu-id="478e7-357">Confirm the putaway work.</span></span>

    <span data-ttu-id="478e7-358">На странице **Задачи** для получения строки заказа на покупку вы получаете сообщение "Работа завершена".</span><span class="sxs-lookup"><span data-stu-id="478e7-358">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="478e7-359">Поле **LINENUM** доступно для того, чтобы можно было начать получать следующую палету.</span><span class="sxs-lookup"><span data-stu-id="478e7-359">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

<span data-ttu-id="478e7-360">Теперь вы выполнили проверку качества и создали заказ для контроля качества для отклоненной палеты.</span><span class="sxs-lookup"><span data-stu-id="478e7-360">You've now completed the quality check and created a quality order for the rejected pallet.</span></span> <span data-ttu-id="478e7-361">Для просмотра созданного заказа перейдите **Управление запасами \> Периодические задачи \> Управление качеством \> Заказы на контроль качества**.</span><span class="sxs-lookup"><span data-stu-id="478e7-361">To view the order that was created, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="478e7-362">Тестирование заказа для контроля качества теперь может быть обработано.</span><span class="sxs-lookup"><span data-stu-id="478e7-362">Quality order testing can now be processed.</span></span> <span data-ttu-id="478e7-363">Проверка качества не рассматривается в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="478e7-363">Quality testing isn't covered in this topic.</span></span>

<span data-ttu-id="478e7-364">Дополнительные сведения об управлении качеством см. в разделе [Обзор управления качеством](../inventory/enable-quality-management.md).</span><span class="sxs-lookup"><span data-stu-id="478e7-364">For more information about quality management, see [Quality management overview](../inventory/enable-quality-management.md)</span></span>

#### <a name="receive-pallet-3"></a><span data-ttu-id="478e7-365">Получить палету 3</span><span class="sxs-lookup"><span data-stu-id="478e7-365">Receive pallet 3</span></span>

<span data-ttu-id="478e7-366">В этом случае палета 3 будет принята.</span><span class="sxs-lookup"><span data-stu-id="478e7-366">For this scenario, pallet 3 will be accepted.</span></span>

1. <span data-ttu-id="478e7-367">В поле **LINENUM** введите *1* и подтвердите номер строки.</span><span class="sxs-lookup"><span data-stu-id="478e7-367">In the **LINENUM** field, enter *1*, and confirm the line number.</span></span>
1. <span data-ttu-id="478e7-368">Поле **КОЛ-ВО** теперь доступно.</span><span class="sxs-lookup"><span data-stu-id="478e7-368">The **QTY** field is now available.</span></span> <span data-ttu-id="478e7-369">Введите *1* и подтвердите количество.</span><span class="sxs-lookup"><span data-stu-id="478e7-369">Enter *1*, and confirm the quantity.</span></span>

    <span data-ttu-id="478e7-370">Отображается страница **Проверка качества**.</span><span class="sxs-lookup"><span data-stu-id="478e7-370">The **Quality check** page appears.</span></span> <span data-ttu-id="478e7-371">Для данного получения палета будет принята по качеству, она будет помещена в местоположение сборного размещения.</span><span class="sxs-lookup"><span data-stu-id="478e7-371">For this receipt, the pallet will be accepted for quality, and it will be put into a bulk putaway location.</span></span>

1. <span data-ttu-id="478e7-372">Нажмите кнопку подтверждения, чтобы пройти проверку качества.</span><span class="sxs-lookup"><span data-stu-id="478e7-372">Select the confirmation button to pass the quality check.</span></span>

    <span data-ttu-id="478e7-373">Будет открыта страница **Заказы на покупку: размещение**, на которой отображаются подробные сведения о размещенной работе:</span><span class="sxs-lookup"><span data-stu-id="478e7-373">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="478e7-374">**LOC:** местоположение определяется системой</span><span class="sxs-lookup"><span data-stu-id="478e7-374">**LOC:** The system determined location</span></span>

        <span data-ttu-id="478e7-375">Это местоположение указывает местоположение размещения для получения заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="478e7-375">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="478e7-376">**LP:** созданный системой код грузоместа</span><span class="sxs-lookup"><span data-stu-id="478e7-376">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="478e7-377">**Номенклатура:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="478e7-377">**Item:** *M9203*</span></span>
    - <span data-ttu-id="478e7-378">**Кол-во:** *1 PL: 100 шт.*</span><span class="sxs-lookup"><span data-stu-id="478e7-378">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="478e7-379">Отображается также описание номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="478e7-379">The item description is also shown.</span></span>

1. <span data-ttu-id="478e7-380">Подтвердите работу по размещению.</span><span class="sxs-lookup"><span data-stu-id="478e7-380">Confirm the putaway work.</span></span>

    <span data-ttu-id="478e7-381">На странице **Задачи** для получения строки заказа на покупку вы получаете сообщение "Работа завершена".</span><span class="sxs-lookup"><span data-stu-id="478e7-381">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="478e7-382">Поле **LINENUM** доступно для того, чтобы можно было начать получать следующую палету.</span><span class="sxs-lookup"><span data-stu-id="478e7-382">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

1. <span data-ttu-id="478e7-383">Выберите кнопку меню (**≡**) в верхней части страницы, а затем в меню выберите **Отменить**, чтобы вернуться в меню.</span><span class="sxs-lookup"><span data-stu-id="478e7-383">Select the Menu button (**≡**) at the top of the page, and then, on the menu, select **Cancel** to return to the menu.</span></span>

<span data-ttu-id="478e7-384">Теперь можно закрыть мобильное приложение.</span><span class="sxs-lookup"><span data-stu-id="478e7-384">You can now close the mobile app.</span></span>
