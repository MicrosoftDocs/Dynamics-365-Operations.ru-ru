---
title: Планирование создания работы во время волны
description: В этой тепе описывается, как настроить и использовать метод обработки планирования создания работы во время волны.
author: perlynne
manager: mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 36a450f78695f617056875f8d236fe46bc66aaaf
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501230"
---
# <a name="schedule-work-creation-during-wave"></a><span data-ttu-id="a71d3-103">Планирование создания работы во время волны</span><span class="sxs-lookup"><span data-stu-id="a71d3-103">Schedule work creation during wave</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="a71d3-104">Используйте функцию *Планирование содания работ* в рамках процесса волны, чтобы повысить пропускную способность обработки волны, настроив систему на создание работы с использованием параллельной обработки.</span><span class="sxs-lookup"><span data-stu-id="a71d3-104">Use the *Schedule work creation* feature as part of your waving process to help increase wave processing throughput by having the system create work using parallel processing.</span></span>

<span data-ttu-id="a71d3-105">Когда функциональность активирована, запланированная работа будет автоматически создана, и система будет в конечном итоге обрабатывать для создания фактической работы.</span><span class="sxs-lookup"><span data-stu-id="a71d3-105">When the functionality is enabled, planned work will automatically get created, which the system will eventually process to create actual work.</span></span> <span data-ttu-id="a71d3-106">Если количество строк загрузки волны достигает заранее определенного порога, система создает фактическую работу быстрее путем применения параллельной асинхронной обработки.</span><span class="sxs-lookup"><span data-stu-id="a71d3-106">If the number of wave load lines reaches a predetermined threshold, the system will create actual work more quickly by applying parallel, asynchronous processing.</span></span>

## <a name="enable-the-schedule-work-creation-feature"></a><span data-ttu-id="a71d3-107">Включение функции планирования создания работы</span><span class="sxs-lookup"><span data-stu-id="a71d3-107">Enable the Schedule work creation feature</span></span>

### <a name="enable-the-feature-in-feature-management"></a><span data-ttu-id="a71d3-108">Включение функции в управлении функциями</span><span class="sxs-lookup"><span data-stu-id="a71d3-108">Enable the feature in feature management</span></span>

<span data-ttu-id="a71d3-109">Прежде чем использовать функцию *Планирование создания работы*, она должна быть включена в системе.</span><span class="sxs-lookup"><span data-stu-id="a71d3-109">Before you can use the *Schedule work creation* feature, it must be turned on in your system.</span></span> <span data-ttu-id="a71d3-110">Администраторы могут использовать рабочую область [Управление функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функции и ее включения, если это требуется.</span><span class="sxs-lookup"><span data-stu-id="a71d3-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="a71d3-111">В этом случае функция указана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a71d3-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="a71d3-112">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="a71d3-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="a71d3-113">**Название функции:** *Планирование создания работы*</span><span class="sxs-lookup"><span data-stu-id="a71d3-113">**Feature name:** *Schedule work creation*</span></span>

> [!NOTE]
> <span data-ttu-id="a71d3-114">Функция *Блокировка работы для всей организации* должна быть включена, прежде чем можно будет включить функцию *Планирование создания работы*.</span><span class="sxs-lookup"><span data-stu-id="a71d3-114">The *Organization-wide work blocking* feature must be enabled before you can enable *Schedule work creation*.</span></span>

### <a name="manually-enable-batch-processing-of-waves"></a><span data-ttu-id="a71d3-115">Ручное включение пакетной обработки волн</span><span class="sxs-lookup"><span data-stu-id="a71d3-115">Manually enable batch processing of waves</span></span>

<span data-ttu-id="a71d3-116">Чтобы воспользоваться преимуществом параллельного асинхронного метода создания складских работ, необходимо, чтобы ваш процесс волны был запущен в пакетном режиме.</span><span class="sxs-lookup"><span data-stu-id="a71d3-116">To take advantage of a parallel asynchronous method to create warehouse work, your wave process must be running in batch.</span></span> <span data-ttu-id="a71d3-117">Чтобы это настроить:</span><span class="sxs-lookup"><span data-stu-id="a71d3-117">To set this up:</span></span>

1. <span data-ttu-id="a71d3-118">Перейдите в раздел  **Управление складом \> Настройка \> Параметры управления складом**.</span><span class="sxs-lookup"><span data-stu-id="a71d3-118">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>

1. <span data-ttu-id="a71d3-119">На вкладке **Общие** задайте для параметра **Обрабатывать волны в партии** значение *Да*.</span><span class="sxs-lookup"><span data-stu-id="a71d3-119">On the **General** tab, set **Process waves in batch** to *Yes*.</span></span> <span data-ttu-id="a71d3-120">При желании можно также выбрать специальную **Группа партий обработки волны**, чтобы предотвратить выполнение обработки пакетной очереди в то же время, что и другие процессы.</span><span class="sxs-lookup"><span data-stu-id="a71d3-120">Optionally, you can also select a dedicated **Wave processing batch group** to prevent your batch queue processing from running at the same time as other processes.</span></span>

1. <span data-ttu-id="a71d3-121">Установите **Время ожидания блокировки (мс)**, которое применяется, когда система обрабатывает несколько волн в одно и то же время.</span><span class="sxs-lookup"><span data-stu-id="a71d3-121">Set the **Wait for lock (ms) time**, which applies when the system is processing several waves at the same time.</span></span> <span data-ttu-id="a71d3-122">Для большинства больших процессов волн рекомендуется установить значение *60000*.</span><span class="sxs-lookup"><span data-stu-id="a71d3-122">For most larger waving processes, we recommend a value of *60000*.</span></span>

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a><span data-ttu-id="a71d3-123">Ручное включение нового метода шага волны для существующих шаблонов волн</span><span class="sxs-lookup"><span data-stu-id="a71d3-123">Manually enable the new wave step method for existing wave templates</span></span>

<span data-ttu-id="a71d3-124">Начните с создания нового метода шага волны и включения его для параллельной асинхронной обработки задач.</span><span class="sxs-lookup"><span data-stu-id="a71d3-124">Start by creating the new wave step method and enabling it for parallel asynchronous task processing.</span></span>

1. <span data-ttu-id="a71d3-125">Перейдите в раздел  **Управление складом \> Настройка \> Волны \> Методы обработки волн**.</span><span class="sxs-lookup"><span data-stu-id="a71d3-125">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>

1. <span data-ttu-id="a71d3-126">Выберите  **Восстановить метод** и обратите внимание, что *WHSScheduleWorkCreationWaveStepMethod* был добавлен в список методов обработки волны, которые можно использовать в шаблонах волны отгрузки.</span><span class="sxs-lookup"><span data-stu-id="a71d3-126">Select  **Regenerate method** and note that *WHSScheduleWorkCreationWaveStepMethod* has been added to the list of wave process methods you can use in your shipping wave templates.</span></span>

1. <span data-ttu-id="a71d3-127">Выберите запись, в которой **Имя метода** равно *WHSScheduleWorkCreationWaveStepMethod*, и выберите **Конфигурация задачи**.</span><span class="sxs-lookup"><span data-stu-id="a71d3-127">Select the record with the **Method name** *WHSScheduleWorkCreationWaveStepMethod* and select **Task configuration**.</span></span>

1. <span data-ttu-id="a71d3-128">Чтобы добавить новую строку в сетку, выберите **Создать** на панели действий и используйте следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="a71d3-128">To add a new row to the grid, select **New** on the Action Pane and use the following settings:</span></span>

    - <span data-ttu-id="a71d3-129">**Склад** — выберите склад, который будет использоваться для планирования обработки создания работ.</span><span class="sxs-lookup"><span data-stu-id="a71d3-129">**Warehouse** - Select the warehouse you will use to schedule work creation processing.</span></span>

    - <span data-ttu-id="a71d3-130">**Максимальное число пакетных задач** — указывает максимальное число пакетных задач.</span><span class="sxs-lookup"><span data-stu-id="a71d3-130">**Maximum number of batch tasks** - Specify a maximum number of batch tasks.</span></span> <span data-ttu-id="a71d3-131">В большинстве случаев это значение должно находиться в диапазоне от 8 до 16, однако рекомендуется поэкспериментировать с оптимальной настройкой на основе ваших сценариев.</span><span class="sxs-lookup"><span data-stu-id="a71d3-131">In most cases, this value should be in the range from 8-16, however we recommend that you experiment with the optimal setting based on your scenarios.</span></span>

    - <span data-ttu-id="a71d3-132">**Группа пакетов обработки волн** — выберите специальную группу пакетов обработки волн для оптимизации обработки очереди пакетных заданий.</span><span class="sxs-lookup"><span data-stu-id="a71d3-132">**Wave processing batch group** - Select a dedicated wave processing batch group to optimize your batch queue processing.</span></span>

<span data-ttu-id="a71d3-133">Теперь можно обновить существующий шаблон волны (или создать новый) для использования метода обработки волны *Планирование создания работ*.</span><span class="sxs-lookup"><span data-stu-id="a71d3-133">Now you are ready to update an existing wave template (or create a new one) to use the *Schedule work creation* wave processing method.</span></span>

1. <span data-ttu-id="a71d3-134">Перейдите в раздел  **Управление складом \> Настройка \> Волны \> Шаблоны волны**.</span><span class="sxs-lookup"><span data-stu-id="a71d3-134">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>

1. <span data-ttu-id="a71d3-135">Выберите **Правка** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="a71d3-135">Select **Edit** on the Action Pane.</span></span>

1. <span data-ttu-id="a71d3-136">В области списка выберите шаблон волны, который требуется обновить (если тестируется производится с помощью демонстрационных данных, можно использовать *Доставка 24 по умолчанию*).</span><span class="sxs-lookup"><span data-stu-id="a71d3-136">In the list pane, select the wave template you would like to update (if you are testing using demo data, then you could use *24 Shipping default*).</span></span>

1. <span data-ttu-id="a71d3-137">Разверните экспресс-вкладку **Методы** и выберите строку, в которой **Имя** равно *Планирование создания работ* в сетке **Оставшиеся методы**.</span><span class="sxs-lookup"><span data-stu-id="a71d3-137">Expand the **Methods** FastTab and select the row with the **Name** *Schedule work creation* in the **Remaining methods** grid.</span></span>

1. <span data-ttu-id="a71d3-138">Выберите стрелку, указывающую на столбец **Выбранные методы**, чтобы переместить выбранную строку в этот столбец.</span><span class="sxs-lookup"><span data-stu-id="a71d3-138">Select the arrow pointing to the **Selected methods** column to move the selected row to that column.</span></span> <span data-ttu-id="a71d3-139">(Допускается только один выбранный метод за раз, использующий *WHSScheduleWorkCreationWaveStepMethod* или *createWork*, поэтому существующая строка, в которой **Имя метода** равно *createWork*, автоматически перемещается в сетку **Оставшиеся методы**.)</span><span class="sxs-lookup"><span data-stu-id="a71d3-139">(You can only have one selected method at a time that uses either *WHSScheduleWorkCreationWaveStepMethod* or *createWork*, so the existing row with **Method name** *createWork* is automatically moved to the **Remaining methods** grid.)</span></span>

## <a name="set-wave-task-processing-threshold-data"></a><span data-ttu-id="a71d3-140">Установка пороговых значений обработки задач волны</span><span class="sxs-lookup"><span data-stu-id="a71d3-140">Set wave task processing threshold data</span></span>

<span data-ttu-id="a71d3-141">Система создаст пороговые данные обработки задач волны по умолчанию при первом запуске процесса волны с использованием любой обработки на основе задач.</span><span class="sxs-lookup"><span data-stu-id="a71d3-141">The system will create default wave task processing threshold data the first time a wave process runs using any task-based processing.</span></span> <span data-ttu-id="a71d3-142">Данные используются для управления тем, когда обработка волны выполняется асинхронно и должна быть основана на задачах, что позволяет ей параллельно обрабатывать и создавать работу.</span><span class="sxs-lookup"><span data-stu-id="a71d3-142">The data is used to control when wave processing will run asynchronously and be task-based, which enables it to process and create work in parallel.</span></span>

<span data-ttu-id="a71d3-143">Данные по умолчанию изначально будут использовать пороговое значение 15 для минимального количества строк загрузки (MINIMUMWAVELOADLINES).</span><span class="sxs-lookup"><span data-stu-id="a71d3-143">The default data will initially use a threshold value of 15 for the minimum number of load lines (MINIMUMWAVELOADLINES).</span></span> <span data-ttu-id="a71d3-144">Это означает, что когда система обрабатывает волну с более чем 15 строками загрузки, она будет использовать асинхронную обработку задач.</span><span class="sxs-lookup"><span data-stu-id="a71d3-144">This means that when the system processes a wave with more than 15 loads lines, it will use asynchronous task processing.</span></span> <span data-ttu-id="a71d3-145">Эти данные можно вручну ювставить в таблицу **WHSWaveTaskProcessingThresholdParameters** в тестовых средах, но если вам необходимо изменить этот параметр в производственной среде, необходимо обратиться в службу поддержки Майкрософт, чтобы запросить обновление.</span><span class="sxs-lookup"><span data-stu-id="a71d3-145">You can manually insert/update this data in the **WHSWaveTaskProcessingThresholdParameters** table in your test environments, but if you need to change this setting in a production environment, you must contact Microsoft Support to request the update.</span></span>

## <a name="work-with-the-feature"></a><span data-ttu-id="a71d3-146">Работа с функцией</span><span class="sxs-lookup"><span data-stu-id="a71d3-146">Work with the feature</span></span>

<span data-ttu-id="a71d3-147">Когда функция *Планирование создания работ* активирована, при обработке волн создается запланированная работа, которая в конечном итоге будет использоваться в новом процессе создания работы.</span><span class="sxs-lookup"><span data-stu-id="a71d3-147">When the *Schedule work creation* functionality is enabled, wave processing will create planned work, which will eventually be used by the new work creation process.</span></span> <span data-ttu-id="a71d3-148">Во время создания работы эта работа будет заблокирована с помощью функции *Блокировка работы для всей организации*.</span><span class="sxs-lookup"><span data-stu-id="a71d3-148">During work creation, the work will be blocked using the *Organization-wide work blocking* feature.</span></span>

<span data-ttu-id="a71d3-149">В следующей блок-схеме показано, как создается запланированная работа во время обработки волны.</span><span class="sxs-lookup"><span data-stu-id="a71d3-149">The following flowchart shows how planned work is created during wave processing.</span></span>

![Запланировать создание работы](media/schedule-work-creation-process.png)

### <a name="planned-work"></a><span data-ttu-id="a71d3-151">Запланированная работа</span><span class="sxs-lookup"><span data-stu-id="a71d3-151">Planned work</span></span>

<span data-ttu-id="a71d3-152">Страница **Сведения о запланированной работе** (**Управление складом \> Работа \> Сведения о запланированной работе**) отображает сведения о запланированной работе, которая первоначально создается во время обработки волны.</span><span class="sxs-lookup"><span data-stu-id="a71d3-152">The **Planned work details** page (**Warehouse management \> Work \> Planned work details**) shows information about the planned work, which is initially created during wave processing.</span></span> <span data-ttu-id="a71d3-153">Доступны следующие значения **Статус процесса**:</span><span class="sxs-lookup"><span data-stu-id="a71d3-153">The following **Process status** values are available:</span></span>

- <span data-ttu-id="a71d3-154">**В очереди** — запланированная работа ожидает использования для создания работы.</span><span class="sxs-lookup"><span data-stu-id="a71d3-154">**Queued** - The planned work is waiting to be used to create work.</span></span>
- <span data-ttu-id="a71d3-155">**Завершено** — запланированная работа была использована для создания работы.</span><span class="sxs-lookup"><span data-stu-id="a71d3-155">**Completed** - The planned work has been used to create work.</span></span>
- <span data-ttu-id="a71d3-156">**Сбой** — обработка волны завершилась с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="a71d3-156">**Failed** – The wave processing has failed.</span></span> <span data-ttu-id="a71d3-157">Обратите внимание, что запланированная работа может находиться в состоянии **Сбой** с соответствующей фактический работой или без нее.</span><span class="sxs-lookup"><span data-stu-id="a71d3-157">Note that the planned work can be in a **Failed** state with or without related actual work.</span></span> <span data-ttu-id="a71d3-158">Когда процесс создания фактической работы заканчивается сбоем, фактическая работа остается в состоянии *Отменено*.</span><span class="sxs-lookup"><span data-stu-id="a71d3-158">When the actual work creation process fails, the actual work remains in status *Cancelled*.</span></span>

### <a name="batch-job-for-the-work-creation-process"></a><span data-ttu-id="a71d3-159">Пакетное задание для процесса создания работы</span><span class="sxs-lookup"><span data-stu-id="a71d3-159">Batch job for the work creation process</span></span>

<span data-ttu-id="a71d3-160">Для просмотра пакетных заданий для обработки волн выберите **Пакетные задания** на панели операций на странице **Все волны**.</span><span class="sxs-lookup"><span data-stu-id="a71d3-160">To view the batch jobs for processing waves, select **Batch jobs** on the Action Pane on the **All waves** page.</span></span>

<span data-ttu-id="a71d3-161">Отсюда можно просмотреть все подробные сведения о пакетной задаче для каждого из кодов пакетных заданий.</span><span class="sxs-lookup"><span data-stu-id="a71d3-161">From here, you can view all the batch task details for each of the batch job IDs.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]