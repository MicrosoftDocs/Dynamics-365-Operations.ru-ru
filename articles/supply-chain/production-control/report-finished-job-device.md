---
title: Приемка с устройства карты задания
description: В этом разделе описывается, как настроить систему таким образом, чтобы пользователи устройства карты задания могли отчитываться о готовой продукции из производственного заказа в запасы.
author: johanhoffmann
manager: tfehr
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f5d34893ddc8adc3785ec50dbd72438cf8f68c5d
ms.sourcegitcommit: 52ba8d3e6af72df5dab6c04b9684a61454d353ad
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/26/2020
ms.locfileid: "3403270"
---
# <a name="report-as-finished-from-the-job-card-device"></a><span data-ttu-id="67084-103">Приемка с устройства карты задания</span><span class="sxs-lookup"><span data-stu-id="67084-103">Report as finished from the job card device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67084-104">Сотрудники используют страницу **Проверить ход выполнения** на устройстве карты задания для создания отчета о количестве, которое было завершено для производственного задания.</span><span class="sxs-lookup"><span data-stu-id="67084-104">Workers use the **Report progress** page on the job card device to report quantities that have been completed for a production job.</span></span>

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a><span data-ttu-id="67084-105">Управление тем, добавлено ли принятое количество в запасы</span><span class="sxs-lookup"><span data-stu-id="67084-105">Control whether quantities that are reported as finished are added to inventory</span></span>

<span data-ttu-id="67084-106">Чтобы управлять тем, добавлено ли принятое количество по последней операции в запасы, выполните следующее.</span><span class="sxs-lookup"><span data-stu-id="67084-106">To control whether and how the quantities that are reported as finished on the last operation should be added to inventory, follow these steps.</span></span>

1. <span data-ttu-id="67084-107">Перейдите **Управление производством \> Настройка \> Управление производством \> Значения по умолчанию для производственного заказа**.</span><span class="sxs-lookup"><span data-stu-id="67084-107">Go to **Product control \> Setup \> Manufacturing execution \> Production order defaults**.</span></span>
1. <span data-ttu-id="67084-108">На вкладке **Приемка** установите для поля **Обновить конечный отчет** одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="67084-108">On the **Report as finished** tab, set the **Update finished report on-line** field to one of the following values:</span></span>

    - <span data-ttu-id="67084-109">**Нет** — количество не добавляется в запасы, когда сообщается о количестве по последней операции.</span><span class="sxs-lookup"><span data-stu-id="67084-109">**No** – No quantity will be added to inventory when quantities are reported on the last operation.</span></span> <span data-ttu-id="67084-110">Статус производственного заказа никогда не изменится.</span><span class="sxs-lookup"><span data-stu-id="67084-110">The status of the production order will never change.</span></span>
    - <span data-ttu-id="67084-111">**Статус + количество** — статус производственного заказа изменится на *Принятые*, и количество будет учтено как принятое в запасах.</span><span class="sxs-lookup"><span data-stu-id="67084-111">**Status + Quantity** – The status of the production order will change to *Reported as finished*, and the quantity will be reported as finished to inventory.</span></span>
    - <span data-ttu-id="67084-112">**Количество** — статус будет "Принятые" в запасах, но статус производственного заказа никогда не изменится.</span><span class="sxs-lookup"><span data-stu-id="67084-112">**Quantity** – The quantity will be reported as finished to inventory, but the status of the production order will never change.</span></span>
    - <span data-ttu-id="67084-113">**Статус** — изменится только статус производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="67084-113">**Status** – Only the status of the production order will change.</span></span> <span data-ttu-id="67084-114">Количество не добавляется в запасы, когда сообщается о количестве по последней операции.</span><span class="sxs-lookup"><span data-stu-id="67084-114">No quantities will be added to inventory when quantities are reported on the last operation.</span></span>

> [!NOTE]
> <span data-ttu-id="67084-115">Количество не отслеживается в запасах, если операции, которые учтены как принятые, не определены как последняя операция.</span><span class="sxs-lookup"><span data-stu-id="67084-115">Quantities aren't tracked in inventory if the operations that they are reported as finished on aren't defined as the last operation.</span></span> <span data-ttu-id="67084-116">Однако эти количества могут использоваться для просмотра хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="67084-116">However, those quantities can be used to view progress.</span></span> <span data-ttu-id="67084-117">Они также могут быть включены в правила, определяющие, могут ли работники начать следующую операцию, прежде чем будет достигнуто определенное пороговое значение количества, которое было указано в отчете по предыдущей операции.</span><span class="sxs-lookup"><span data-stu-id="67084-117">They can also be included in rules that control whether workers can start the next operation before a defined threshold of reported quantities on the previous operation is reached.</span></span> <span data-ttu-id="67084-118">Эти правила можно определить на вкладке **Проверка количества** на странице **Значения по умолчанию для производственного заказа**.</span><span class="sxs-lookup"><span data-stu-id="67084-118">You can define these rules on the **Quantity validation** tab of the **Production order defaults** page.</span></span>

<span data-ttu-id="67084-119">Дополнительные сведения о работе со страницей **Значения по умолчанию для производственного заказа** см. в разделе [Параметры производства модуля "Управление производством"](production-parameters-manufacturing-execution.md).</span><span class="sxs-lookup"><span data-stu-id="67084-119">For more information about how to work with the **Production order defaults** page, see [Production parameters in Manufacturing execution](production-parameters-manufacturing-execution.md).</span></span>

## <a name="report-batch-controlled-items-as-finished"></a><span data-ttu-id="67084-120">Отчет о приемке контролируемых по партиям номенклатур</span><span class="sxs-lookup"><span data-stu-id="67084-120">Report batch-controlled items as finished</span></span>

<span data-ttu-id="67084-121">Устройство карты задания поддерживает три сценария для отчетности по номенклатурам партии.</span><span class="sxs-lookup"><span data-stu-id="67084-121">The job card device supports three scenarios for reporting on batch items.</span></span> <span data-ttu-id="67084-122">Эти сценарии применяются как к номенклатурам, которые включены для расширенных складских процессов, так и к номенклатурам, не включенным в расширенные складские процессы.</span><span class="sxs-lookup"><span data-stu-id="67084-122">These scenarios apply both to items that are enabled for advanced warehouse processes and to items that aren't enabled for advanced warehouse processes.</span></span>

- <span data-ttu-id="67084-123">**Номера партий, назначенные вручную:** работники вводят настраиваемый номер партии.</span><span class="sxs-lookup"><span data-stu-id="67084-123">**Manually assigned batch numbers:** Workers enter a custom batch number.</span></span> <span data-ttu-id="67084-124">Этот номер партии может поступать из внешнего источника, который неизвестен в системе.</span><span class="sxs-lookup"><span data-stu-id="67084-124">This batch number might come from an external source that isn't known to the system.</span></span>
- <span data-ttu-id="67084-125">**Предварительно определенные номера партий:** работники выбирают номер партии в списке номеров партий, которые система автоматически создает, прежде чем производственный заказ будет направлен в устройство карты задания.</span><span class="sxs-lookup"><span data-stu-id="67084-125">**Predefined batch numbers:** Workers select a batch number in a list of batch numbers that the system automatically generates before the production order is released to the job card device.</span></span>
- <span data-ttu-id="67084-126">**Фиксированные номера партий:** работники не вводят и не выбирают номер партии.</span><span class="sxs-lookup"><span data-stu-id="67084-126">**Fixed batch numbers:** Workers don't enter or select a batch number.</span></span> <span data-ttu-id="67084-127">Вместо этого система автоматически назначает номер партии производственному заказу до его запуска в производство.</span><span class="sxs-lookup"><span data-stu-id="67084-127">Instead, the system automatically assigns a batch number to the production order before it's released.</span></span>

<span data-ttu-id="67084-128">Для включения каждого сценария выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="67084-128">To enable each scenario, follow these steps.</span></span>

1. <span data-ttu-id="67084-129">Выберите **Управление сведениями о продукте \> Продукты \> Выпущенные продукты**.</span><span class="sxs-lookup"><span data-stu-id="67084-129">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="67084-130">Выберите продукт для настройки.</span><span class="sxs-lookup"><span data-stu-id="67084-130">Select the product to configure.</span></span>
1. <span data-ttu-id="67084-131">На экспресс-вкладке **Управление запасами** в поле **Группа номеров партий** выберите группу номеров отслеживания, настроенную для поддержки вашего сценария.</span><span class="sxs-lookup"><span data-stu-id="67084-131">On the **Manage inventory** FastTab, in the **Batch number group** field, select the tracking number group that is set up to support your scenario.</span></span>

> [!NOTE]
> <span data-ttu-id="67084-132">По умолчанию, если для контролируемого по партиям продукта не назначена ни одна группы номеров партий, устройство карты задания предоставляет ручной ввод для номера партии во время приемки.</span><span class="sxs-lookup"><span data-stu-id="67084-132">By default, if no batch number group is assigned to a batch-controlled product, the job card device provides manual entry for the batch number during reporting as finished.</span></span>

<span data-ttu-id="67084-133">В следующих подразделах описывается порядок настройки групп номеров отслеживания для поддержки каждого из трех вариантов отчетности по номенклатурам партии.</span><span class="sxs-lookup"><span data-stu-id="67084-133">The following subsections describe how to set up tracking number groups to support each of the three scenarios for reporting on batch items.</span></span>

### <a name="enable-batch-number-reporting-on-the-job-card-device"></a><span data-ttu-id="67084-134">Включить отчетность по номерам партий на устройстве карты задания</span><span class="sxs-lookup"><span data-stu-id="67084-134">Enable batch number reporting on the job card device</span></span>

<span data-ttu-id="67084-135">Чтобы разрешить устройствам карты задания принимать номер партии во время приемки, необходимо использовать [управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), чтобы включить следующие функции (в этом порядке):</span><span class="sxs-lookup"><span data-stu-id="67084-135">To enable your job card devices to accept a batch number during reporting as finished, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="67084-136">Улучшенное взаимодействие пользователя в диалоговом окне хода выполнения отчета на устройстве карты задания</span><span class="sxs-lookup"><span data-stu-id="67084-136">Improved user experience for the Report progress dialog in the Job Card Device</span></span>
1. <span data-ttu-id="67084-137">Позволяет вводить номера партий и серийные номера при приемке с устройства карты задания (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="67084-137">Enable to enter batch and serial numbers while reporting as finished from the Job Card Device (Preview)</span></span>

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a><span data-ttu-id="67084-138">Настройка группы номеров отслеживания, которая позволяет работникам вручную назначать номер партии</span><span class="sxs-lookup"><span data-stu-id="67084-138">Set up a tracking number group that lets workers manually assign a batch number</span></span>

<span data-ttu-id="67084-139">Чтобы разрешить ручное назначение номеров партий, выполните следующие действия для настройки группы номеров отслеживания.</span><span class="sxs-lookup"><span data-stu-id="67084-139">To allow for manually assigned batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="67084-140">Перейдите **Управление запасами \> Настройка \> Аналитики \> Группы номеров отслеживания**.</span><span class="sxs-lookup"><span data-stu-id="67084-140">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="67084-141">Создайте или выберите группу номеров отслеживания для настройки.</span><span class="sxs-lookup"><span data-stu-id="67084-141">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="67084-142">На экспресс-вкладке **Общие** задайте для параметра **Вручную** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="67084-142">On the **General** FastTab, set the **Manual** option to **Yes**.</span></span>

    <span data-ttu-id="67084-143">![Страница групп номеров отслеживания](media/tracking-number-group-manual.png "Страница групп номеров отслеживания")</span><span class="sxs-lookup"><span data-stu-id="67084-143">![Tracking number groups page](media/tracking-number-group-manual.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="67084-144">Установите другие требуемые значения, а затем выберите эту группу номеров отслеживания в качестве группы номеров партий для выпущенных продуктов, для которых необходимо использовать этот сценарий.</span><span class="sxs-lookup"><span data-stu-id="67084-144">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="67084-145">При использовании этого сценария поле **Номер партии** на странице **Проверить ход выполнения** на устройстве карты задания представляет собой текстовое поле, в которое работники могут ввести любое значение.</span><span class="sxs-lookup"><span data-stu-id="67084-145">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a text box where workers can enter any value.</span></span>

<span data-ttu-id="67084-146">![Страница проверки хода выполнения с полем для ручного ввода номеров партий](media/job-card-device-batch-manual.png "Страница проверки хода выполнения с полем для ручного ввода номеров партий")</span><span class="sxs-lookup"><span data-stu-id="67084-146">![Report progress page with a field for manual batch numbers](media/job-card-device-batch-manual.png "Report progress page with a field for manual batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a><span data-ttu-id="67084-147">Настройка группы номеров отслеживания, которая предоставляет список предварительно определенных номеров партий</span><span class="sxs-lookup"><span data-stu-id="67084-147">Set up a tracking number group that provides a list of predefined batch numbers</span></span>

<span data-ttu-id="67084-148">Чтобы разрешить список предварительно заданных номеров партий, выполните следующие действия для настройки группы номеров отслеживания.</span><span class="sxs-lookup"><span data-stu-id="67084-148">To provide a list of predefined batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="67084-149">Перейдите **Управление запасами \> Настройка > Аналитики \> Группы номеров отслеживания**.</span><span class="sxs-lookup"><span data-stu-id="67084-149">Go to **Inventory management \> Setup > Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="67084-150">Создайте или выберите группу номеров отслеживания для настройки.</span><span class="sxs-lookup"><span data-stu-id="67084-150">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="67084-151">На экспресс-вкладке **Общие** установите для параметра **Только для проводок по запасам** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="67084-151">On the **General** FastTab, set the **Only for inventory transactions** option to **Yes**.</span></span>
1. <span data-ttu-id="67084-152">Используйте поле **За кол-во.** для разбиения номеров партий по количеству на основе введенного значения.</span><span class="sxs-lookup"><span data-stu-id="67084-152">Use the **Per qty.** field to split batch numbers per quantity, based on the value that you enter.</span></span> <span data-ttu-id="67084-153">Например, есть производственный заказ на десять штук, а для поля **За кол-во.** в поле указано *2*.</span><span class="sxs-lookup"><span data-stu-id="67084-153">For example, you have a production order for ten pieces, and the **Per qty.** field is set to *2*.</span></span> <span data-ttu-id="67084-154">В этом случае при создании производственного заказа будет назначено пять номеров партий.</span><span class="sxs-lookup"><span data-stu-id="67084-154">In this case, five batch numbers will be assigned to the production order when it's created.</span></span>

    <span data-ttu-id="67084-155">![Страница групп номеров отслеживания](media/tracking-number-group-predefined.png "Страница групп номеров отслеживания")</span><span class="sxs-lookup"><span data-stu-id="67084-155">![Tracking number groups page](media/tracking-number-group-predefined.png "The Tracking number groups page")</span></span>

1. <span data-ttu-id="67084-156">Установите другие требуемые значения, а затем выберите эту группу номеров отслеживания в качестве группы номеров партий для выпущенных продуктов, для которых необходимо использовать этот сценарий.</span><span class="sxs-lookup"><span data-stu-id="67084-156">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="67084-157">При использовании этого сценария поле **Номер партии** на странице **Проверить ход выполнения** на устройстве карты задания представляет собой раскрывающийся список, где работники должны выбирать заранее заданное значение.</span><span class="sxs-lookup"><span data-stu-id="67084-157">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a drop-down list where workers must select a predefined value.</span></span>

<span data-ttu-id="67084-158">![Страница проверки хода выполнения со списком предварительно заданных номеров партий](media/job-card-device-batch-predefined.png "Страница проверки хода выполнения со списком предварительно заданных номеров партий")</span><span class="sxs-lookup"><span data-stu-id="67084-158">![Report progress page with a list of predefined batch numbers](media/job-card-device-batch-predefined.png "Report progress page with a list of predefined batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a><span data-ttu-id="67084-159">Настройка группы номеров отслеживания, которая автоматически назначает номера партий</span><span class="sxs-lookup"><span data-stu-id="67084-159">Set up a tracking number group that automatically assigns batch numbers</span></span>

<span data-ttu-id="67084-160">Если номера партий должны назначаться автоматически, без ввода работником, выполните следующие шаги для настройки группы номеров отслеживания.</span><span class="sxs-lookup"><span data-stu-id="67084-160">If batch numbers should be assigned automatically, without worker input, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="67084-161">Перейдите **Управление запасами \> Настройка \> Аналитики \> Группы номеров отслеживания**.</span><span class="sxs-lookup"><span data-stu-id="67084-161">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="67084-162">Создайте или выберите группу номеров отслеживания для настройки.</span><span class="sxs-lookup"><span data-stu-id="67084-162">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="67084-163">На экспресс-вкладке **Общие** установите для параметра **Только для проводок по запасам** значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="67084-163">On the **General** FastTab, set the **Only for inventory transactions** option to **No**.</span></span>
1. <span data-ttu-id="67084-164">Задайте для параметра **Вручную** значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="67084-164">Set the **Manual** option to **No**.</span></span>

    <span data-ttu-id="67084-165">![Страница групп номеров отслеживания](media/tracking-number-group-fixed.png "Страница групп номеров отслеживания")</span><span class="sxs-lookup"><span data-stu-id="67084-165">![Tracking number groups page](media/tracking-number-group-fixed.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="67084-166">Установите другие требуемые значения, а затем выберите эту группу номеров отслеживания в качестве группы номеров партий для выпущенных продуктов, для которых необходимо использовать этот сценарий.</span><span class="sxs-lookup"><span data-stu-id="67084-166">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="67084-167">При использовании этого сценария поле **Номер партии** на странице **Проверить ход выполнения** на устройстве карты задания представляет собой значение, которое работники не могут изменить.</span><span class="sxs-lookup"><span data-stu-id="67084-167">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides shows a value, but workers can't edit it.</span></span>

<span data-ttu-id="67084-168">![Страница проверки хода выполнения с фиксированным номером партии](media/job-card-device-batch-fixed.png "Страница проверки хода выполнения с фиксированным номером партии")</span><span class="sxs-lookup"><span data-stu-id="67084-168">![Report progress page with a fixed batch number](media/job-card-device-batch-fixed.png "Report progress page with a fixed batch number")</span></span>

## <a name="report-as-finished-to-a-license-plate"></a><span data-ttu-id="67084-169">Приемка для грузоместа</span><span class="sxs-lookup"><span data-stu-id="67084-169">Report as finished to a license plate</span></span>

<span data-ttu-id="67084-170">Дополнительные складские процессы могут использовать аналитику грузомест для отслеживания запасов на складах, настроенных для этой цели.</span><span class="sxs-lookup"><span data-stu-id="67084-170">Advanced warehouse processes can use the license plate dimension to track inventory on warehouse locations that have been set up for this purpose.</span></span> <span data-ttu-id="67084-171">В этом случае номерной знак необходим, когда работник сообщает количество как "приемка".</span><span class="sxs-lookup"><span data-stu-id="67084-171">In this case, the license plate number is required when a worker reports quantities as finished.</span></span>

### <a name="enable-license-plate-reporting-and-label-printing"></a><span data-ttu-id="67084-172">Включение отчетности грузомест и печати меток</span><span class="sxs-lookup"><span data-stu-id="67084-172">Enable license plate reporting and label printing</span></span>

<span data-ttu-id="67084-173">Для использования описанных в этом разделе функций необходимо включить в [управлении функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) следующие функции (в этом порядке):</span><span class="sxs-lookup"><span data-stu-id="67084-173">To use the features that are described in this section, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="67084-174">Грузоместо для приемки добавлено в устройство карты задания</span><span class="sxs-lookup"><span data-stu-id="67084-174">License plate for reporting as finished added to the Job Card Device</span></span>
1. <span data-ttu-id="67084-175">Включение автоматического создания номерного знака при приемке на устройстве карты задания</span><span class="sxs-lookup"><span data-stu-id="67084-175">Enable automatic generation of license plate number when reporting as finished in the job card device</span></span>
1. <span data-ttu-id="67084-176">Печать этикетки с устройства карты задания</span><span class="sxs-lookup"><span data-stu-id="67084-176">Print label from Job Card Device</span></span>

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a><span data-ttu-id="67084-177">Настройка приемки для грузоместа</span><span class="sxs-lookup"><span data-stu-id="67084-177">Set up reporting as finished to a license plate</span></span>

<span data-ttu-id="67084-178">Выполните следующие действия, чтобы указать, следует ли работникам повторно использовать существующее грузоместо или создать новое грузоместо при отчете "принято".</span><span class="sxs-lookup"><span data-stu-id="67084-178">To control whether workers should reuse an existing license plate or generate a new license plate when they report quantities as finished, follow these steps.</span></span>

1. <span data-ttu-id="67084-179">Перейдите в раздел **Управление производством \> Настройка \> Управление производством \> Настроить карту заданий для устройств**.</span><span class="sxs-lookup"><span data-stu-id="67084-179">Go to **Production control \> Setup \> Manufacturing execution \> Configure job card for devices**.</span></span>
2. <span data-ttu-id="67084-180">Настройте следующие параметры для каждого устройства:</span><span class="sxs-lookup"><span data-stu-id="67084-180">Set the following options for each device:</span></span>

    - <span data-ttu-id="67084-181">**Создать грузоместо** — установите этот параметр как **Да**, чтобы создать новое грузоместо для каждой приемки.</span><span class="sxs-lookup"><span data-stu-id="67084-181">**Generate license plate** – Set this option to **Yes** to generate a new license plate for each report as finished.</span></span> <span data-ttu-id="67084-182">Установите значение **Нет**, если следует использовать существующее грузоместо для каждой приемки.</span><span class="sxs-lookup"><span data-stu-id="67084-182">Set it to **No** if an existing license plate should be used for each report as finished.</span></span>
    - <span data-ttu-id="67084-183">**Печать этикетки** — установите этот параметр как **Да**, если работник должен печатать этикетку грузоместа для каждой приемки.</span><span class="sxs-lookup"><span data-stu-id="67084-183">**Print label** – Set this option to **Yes** if the worker must print a license plate label for each report as finished.</span></span> <span data-ttu-id="67084-184">Если метка не требуется, установите значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="67084-184">Set it to **No** if no label is required.</span></span> 

<span data-ttu-id="67084-185">![Страница настройки карты заданий для устройств](media/config-job-card-raf.png "Страница настройки карты заданий для устройств")</span><span class="sxs-lookup"><span data-stu-id="67084-185">![Configure job card for devices page](media/config-job-card-raf.png "Configure job card for devices page")</span></span>

> [!NOTE]
> <span data-ttu-id="67084-186">Чтобы настроить метку, перейдите в раздел **Управление складом \> Настройка \> Маршрутизация документов \> Маршрутизация документов**.</span><span class="sxs-lookup"><span data-stu-id="67084-186">To configure the label, go to **Warehouse management \> Setup \> Document routing \> Document routing**.</span></span> <span data-ttu-id="67084-187">Дополнительные сведения см. в разделе [Включение печати меток грузомест](../warehousing/tasks/license-plate-label-printing.md).</span><span class="sxs-lookup"><span data-stu-id="67084-187">For more information, see [Enable license plate label printing](../warehousing/tasks/license-plate-label-printing.md).</span></span>
