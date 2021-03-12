---
title: Регистратор задач и справка для Retail Modern POS (MPOS) и Cloud POS
description: В этой теме описан порядок использования регистратора задач в Retail Modern POS и Cloud POS.
author: mugunthanm
manager: AnnBe
ms.date: 06/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTerminalTable, SystemParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b0a5ca1e116e931ba992eab51a06dae9fdf92756
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006143"
---
# <a name="task-recorder-and-help-for-retail-modern-pos-mpos-and-cloud-pos"></a><span data-ttu-id="012de-103">Регистратор задач и справка для Retail Modern POS (MPOS) и Cloud POS</span><span class="sxs-lookup"><span data-stu-id="012de-103">Task recorder and Help for Retail Modern POS (MPOS) and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="012de-104">В этой теме описан порядок использования регистратора задач в Retail Modern POS и Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="012de-104">This topic describes how to use Task recorder in Retail Modern POS and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="012de-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="012de-105">Overview</span></span>

<span data-ttu-id="012de-106">Регистратор задач в Retail Modern POS или Cloud POS представляет собой новое решение, созданное для обеспечения высокой отзывчивости.</span><span class="sxs-lookup"><span data-stu-id="012de-106">Task recorder in Retail Modern POS or Cloud POS is a new solution that was built with a focus on high responsiveness.</span></span> <span data-ttu-id="012de-107">Он предоставляет гибкий программный интерфейс (API) для расширения и полной интеграции с потребителями записей бизнес-процессов.</span><span class="sxs-lookup"><span data-stu-id="012de-107">It provides a flexible application programming interface (API) for extensibility and seamless integration with consumers of business process recordings.</span></span> <span data-ttu-id="012de-108">Кроме того, предложена интеграция регистратора задач со средством моделирования бизнес-процессов (BPM) на Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)).</span><span class="sxs-lookup"><span data-stu-id="012de-108">Additionally, Task recorder integration with the Business process modeler (BPM) tool on Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) has been brought forward.</span></span> <span data-ttu-id="012de-109">Таким образом, пользователи могут продолжать создавать схемы бизнес-процессов с широкими возможностями, чтобы анализировать и проектировать свои приложения.</span><span class="sxs-lookup"><span data-stu-id="012de-109">Therefore, users can continue to produce rich business process diagrams from recordings to analyze and design their applications.</span></span>

## <a name="architecture"></a><span data-ttu-id="012de-110">Архитектура</span><span class="sxs-lookup"><span data-stu-id="012de-110">Architecture</span></span>

<span data-ttu-id="012de-111">Регистратор задач может записывать действия пользователя на клиентском компьютере с абсолютной точностью.</span><span class="sxs-lookup"><span data-stu-id="012de-111">Task recorder can record user actions in the client with exact fidelity.</span></span> <span data-ttu-id="012de-112">Каждый элемент управления снабжен инструментами для уведомления регистратора задач о выполнении действий пользователем.</span><span class="sxs-lookup"><span data-stu-id="012de-112">Each control is instrumented to notify Task recorder about the execution of a user action.</span></span> <span data-ttu-id="012de-113">Элемент управления уведомляет регистратор задач о том, что произошло событие, и передает все необходимые сведения о соответствующем действии пользователя в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="012de-113">The control notifies Task recorder that an event occurred and passes along all pertinent information about the corresponding user action in real time.</span></span> <span data-ttu-id="012de-114">На основании этих данных регистратор задач может записать тип действия пользователя (например, нажатие кнопки, ввод значения или переход) и любые данные, относящиеся к действию пользователя (например, тип и значение входных данных, контекст формы или контекст записи).</span><span class="sxs-lookup"><span data-stu-id="012de-114">From this information, Task recorder can capture the type of user action (such as a button click, value entry, or navigation) and any data that is related to the user action (such as the input data value and type, form context, or record context).</span></span> <span data-ttu-id="012de-115">Регистратор задач сохраняет информацию достаточно подробно, помогая гарантировать, что при воспроизведении записи записанные действия могут выполняться точно так же, как они были выполнены пользователем.</span><span class="sxs-lookup"><span data-stu-id="012de-115">Task recorder persists the information with enough detail to help guarantee that a playback of the recording can perform the recorded actions exactly as the user performed them.</span></span> <span data-ttu-id="012de-116">(Функция воспроизведения пока не реализована ни в Retail Modern POS, ни в Cloud POS.)</span><span class="sxs-lookup"><span data-stu-id="012de-116">(The playback feature isn't yet implemented at Retail modern POS or Cloud POS.)</span></span>

## <a name="basic-configuration"></a><span data-ttu-id="012de-117">Базовая конфигурация</span><span class="sxs-lookup"><span data-stu-id="012de-117">Basic configuration</span></span>

<span data-ttu-id="012de-118">Чтобы включить запись задач в POS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="012de-118">To enable task recording in POS, follow these steps.</span></span>

1. <span data-ttu-id="012de-119">Перейдите в раздел **Retail и Commerce** &gt; **Настройка канала** &gt; **Настройка POS** &gt; **Регистры**.</span><span class="sxs-lookup"><span data-stu-id="012de-119">Click **Retail and Commerce** &gt; **Channel Setup** &gt; **POS Setup** &gt; **Registers**.</span></span>
2. <span data-ttu-id="012de-120">Щелкните регистр, чтобы включить запись задач в нем.</span><span class="sxs-lookup"><span data-stu-id="012de-120">Click the register to enable task recording on.</span></span>
3. <span data-ttu-id="012de-121">На вкладке **Регистр** на экспресс-вкладке **Общие** задайте для параметра **Включить запись задачи** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="012de-121">On the **Register** tab, on the **General** FastTab, set the **Enable task recording** option to **Yes**.</span></span>
4. <span data-ttu-id="012de-122">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="012de-122">Click **Save**.</span></span>
5. <span data-ttu-id="012de-123">Перейдите в раздел **Retail и Commerce** &gt; **ИТ Retail и Commerce** &gt; **График распределения**.</span><span class="sxs-lookup"><span data-stu-id="012de-123">Go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedule**.</span></span>
6. <span data-ttu-id="012de-124">Выберите задание **Регистры (1090)** и щелкните **Выполнить сейчас**.</span><span class="sxs-lookup"><span data-stu-id="012de-124">Select the **Registers (1090)** job, and then click **Run now**.</span></span>

## <a name="create-a-recording"></a><span data-ttu-id="012de-125">Создание записи</span><span class="sxs-lookup"><span data-stu-id="012de-125">Create a recording</span></span>

<span data-ttu-id="012de-126">Выполните следующие действия, чтобы создать новую запись с помощью регистратора задач.</span><span class="sxs-lookup"><span data-stu-id="012de-126">Follow these steps to create a new recording using Task recorder.</span></span>

1. <span data-ttu-id="012de-127">Запустите Retail Modern POS или Cloud POS и войдите в систему.</span><span class="sxs-lookup"><span data-stu-id="012de-127">Start Retail Modern POS or Cloud POS, and sign in.</span></span>
2. <span data-ttu-id="012de-128">На странице **Параметры** в разделе **Регистратор задач** щелкните **Открыть регистратор задач**.</span><span class="sxs-lookup"><span data-stu-id="012de-128">On the **Settings** page, in the **Task Recorder** section, click **Open task recorder**.</span></span> <span data-ttu-id="012de-129">Отображается область **Регистратор задач**.</span><span class="sxs-lookup"><span data-stu-id="012de-129">The **Task recorder** pane appears.</span></span> <span data-ttu-id="012de-130">Можно нажать кнопку **Закрыть** (**X**) в правом верхнем углу, чтобы закрыть область **Регистратор задач** перед началом новой записи.</span><span class="sxs-lookup"><span data-stu-id="012de-130">You can click the **Close** button (**X**) in the upper-right corner to close the **Task recorder** pane before you begin a new recording.</span></span> <span data-ttu-id="012de-131">Для повторного открытия области повторите шаг 2.</span><span class="sxs-lookup"><span data-stu-id="012de-131">To reopen the pane, repeat step 2.</span></span>

    <span data-ttu-id="012de-132">[![Область регистратора задач](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)</span><span class="sxs-lookup"><span data-stu-id="012de-132">[![Task recorder pane](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)</span></span>

3. <span data-ttu-id="012de-133">Введите имя и описание записи, затем нажмите **Начать**.</span><span class="sxs-lookup"><span data-stu-id="012de-133">Enter a name and description for the recording, and then click **Start**.</span></span> <span data-ttu-id="012de-134">Сеанс записи начнется в момент нажатия кнопки **Начать**.</span><span class="sxs-lookup"><span data-stu-id="012de-134">The recording session begins as soon as you click **Start**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="012de-135">При нажатии кнопки **Закрыть** (**X**) в правом верхнем углу во время выполнения записи область **Регистратор задач** закрывается, но сеанс записи не завершается.</span><span class="sxs-lookup"><span data-stu-id="012de-135">If you click the **Close** button (**X**) in the upper-right corner while recording is in progress, the **Task recorder** pane is closed, but the recording session isn't ended.</span></span> <span data-ttu-id="012de-136">Чтобы снова открыть область регистратора задач, нажмите кнопку **Справка** (вопросительный знак) в верхней части экрана.</span><span class="sxs-lookup"><span data-stu-id="012de-136">To reopen the Task recorder pane, click the **Help** button (question mark) at the top of the screen.</span></span>
    >
    > <span data-ttu-id="012de-137">[![Вопросительный знак](./media/help.jpg)](./media/help.jpg)</span><span class="sxs-lookup"><span data-stu-id="012de-137">[![Question mark](./media/help.jpg)](./media/help.jpg)</span></span>

4. <span data-ttu-id="012de-138">После нажатия кнопки **Начать** регистратор задач переходит в режим записи.</span><span class="sxs-lookup"><span data-stu-id="012de-138">After you click **Start**, Task recorder enters recording mode.</span></span> <span data-ttu-id="012de-139">В области **Регистратор задач** отображаются сведения и элементы управления, которые относятся к процессу записи.</span><span class="sxs-lookup"><span data-stu-id="012de-139">The **Task recorder** pane shows information and controls that are related to the recording process.</span></span>
5. <span data-ttu-id="012de-140">Выполните действия, которые необходимо выполнить в пользовательском интерфейсе (UI) Retail Modern POS или Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="012de-140">Perform the actions that you want to perform in the Retail Modern POS or Cloud POS user interface (UI).</span></span>
6. <span data-ttu-id="012de-141">Чтобы завершить сеанс записи, нажмите **Остановить**.</span><span class="sxs-lookup"><span data-stu-id="012de-141">To end the recording session, click **Stop**.</span></span>

## <a name="download-options"></a><span data-ttu-id="012de-142">Опции загрузки</span><span class="sxs-lookup"><span data-stu-id="012de-142">Download options</span></span>

<span data-ttu-id="012de-143">После окончания сеанса записи отображается несколько вариантов, чтобы вы могли загрузить свою запись.</span><span class="sxs-lookup"><span data-stu-id="012de-143">After you end the recording session, several options are shown, so that you can download your recording.</span></span>

<span data-ttu-id="012de-144">[![Опции загрузки](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)</span><span class="sxs-lookup"><span data-stu-id="012de-144">[![Download options](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)</span></span>

### <a name="save-to-this-pc"></a><span data-ttu-id="012de-145">Сохранить на этот компьютер</span><span class="sxs-lookup"><span data-stu-id="012de-145">Save to this PC</span></span>

<span data-ttu-id="012de-146">Пакет записи можно использовать для воспроизведения проводника по задаче, для сохранения записи или для редактирования примечаний в записи.</span><span class="sxs-lookup"><span data-stu-id="012de-146">You can use the recording package to play a Task guide, maintain the recording, or edit the annotations in the recording.</span></span> <span data-ttu-id="012de-147">(Эта функция пока не реализована в Retail Modern POS и Cloud POS.)</span><span class="sxs-lookup"><span data-stu-id="012de-147">(This feature isn't yet implemented in Retail Modern POS and Cloud POS.)</span></span>

### <a name="export-as-word-document"></a><span data-ttu-id="012de-148">Экспортировать как документ Word</span><span class="sxs-lookup"><span data-stu-id="012de-148">Export as Word document</span></span>

<span data-ttu-id="012de-149">Можно сохранить запись в виде документа Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="012de-149">You can save the recording as a Microsoft Word document.</span></span> <span data-ttu-id="012de-150">Документ будет содержать записанные шаги и снимки экранов.</span><span class="sxs-lookup"><span data-stu-id="012de-150">The document will contain the recorded steps and the screenshots that were captured.</span></span>

### <a name="save-as-developer-recording"></a><span data-ttu-id="012de-151">Сохранить как запись для разработчика</span><span class="sxs-lookup"><span data-stu-id="012de-151">Save as developer recording</span></span>

<span data-ttu-id="012de-152">Необработанный файл записи будет удобен для сценариев, связанных с разработкой, таких как создание тестового кода.</span><span class="sxs-lookup"><span data-stu-id="012de-152">The raw recording file will be useful for developer scenarios such as test code generation.</span></span> <span data-ttu-id="012de-153">(Эта возможность еще не реализована.)</span><span class="sxs-lookup"><span data-stu-id="012de-153">(This feature isn't yet implemented.)</span></span>

## <a name="recording-controls"></a><span data-ttu-id="012de-154">Элементы управления записью</span><span class="sxs-lookup"><span data-stu-id="012de-154">Recording controls</span></span>

<span data-ttu-id="012de-155">[![Элементы управления записью](./media/controls.jpg)](./media/controls.jpg)</span><span class="sxs-lookup"><span data-stu-id="012de-155">[![Recording controls](./media/controls.jpg)](./media/controls.jpg)</span></span>

### <a name="stop"></a><span data-ttu-id="012de-156">Остановить</span><span class="sxs-lookup"><span data-stu-id="012de-156">Stop</span></span>

<span data-ttu-id="012de-157">Нажмите **Остановить**, чтобы завершить сеанс записи.</span><span class="sxs-lookup"><span data-stu-id="012de-157">Click **Stop** to end the recording session.</span></span> <span data-ttu-id="012de-158">Обратите внимание, что невозможно перезапустить сеанс после его окончания.</span><span class="sxs-lookup"><span data-stu-id="012de-158">Note that you can't restart a session after you end it.</span></span> <span data-ttu-id="012de-159">Поэтому перед окончанием записи убедитесь в том, что она завершена.</span><span class="sxs-lookup"><span data-stu-id="012de-159">Therefore, make sure that the recording is completed before you end it.</span></span>

### <a name="pause"></a><span data-ttu-id="012de-160">Приостановить</span><span class="sxs-lookup"><span data-stu-id="012de-160">Pause</span></span>

<span data-ttu-id="012de-161">Щелкните **Приостановить**, чтобы временно остановить (приостановить) сеанс записи и продолжить работу.</span><span class="sxs-lookup"><span data-stu-id="012de-161">Click **Pause** to temporarily stop (pause) the recording session and continue with the operation.</span></span> <span data-ttu-id="012de-162">Действия, которые выполняются по нажатия кнопки **Приостановить**, не записываются.</span><span class="sxs-lookup"><span data-stu-id="012de-162">Steps that you perform after you click **Pause** aren't recorded.</span></span>

### <a name="continue"></a><span data-ttu-id="012de-163">Продолжить</span><span class="sxs-lookup"><span data-stu-id="012de-163">Continue</span></span>

<span data-ttu-id="012de-164">Для возобновления сеанса записи после его приостановки щелкните **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="012de-164">To resume the recording session after you've paused it, click **Continue**.</span></span>

### <a name="capture-screenshots"></a><span data-ttu-id="012de-165">Захват снимков экрана</span><span class="sxs-lookup"><span data-stu-id="012de-165">Capture screenshots</span></span>

<span data-ttu-id="012de-166">Регистратор задач позволяет записывать снимки экрана пользовательского интерфейса Retail Modern POS во время записи бизнес-процесса.</span><span class="sxs-lookup"><span data-stu-id="012de-166">Task recorder can capture screenshots of the Retail Modern POS UI as you record a business process.</span></span> <span data-ttu-id="012de-167">Чтобы включить функцию записи снимков экрана, задайте для параметра **Захват снимков экрана** значение **Да**, затем произведите запись.</span><span class="sxs-lookup"><span data-stu-id="012de-167">To turn on the screenshot capture feature, set the **Capture screenshot** option to **Yes** and then make the recording.</span></span> <span data-ttu-id="012de-168">После завершения записи щелкните **Стоп** и загрузите документ Word.</span><span class="sxs-lookup"><span data-stu-id="012de-168">Once the recording is completed, click **Stop** and download the Word document.</span></span> <span data-ttu-id="012de-169">Документ будет содержать действия с соответствующими снимками экрана.</span><span class="sxs-lookup"><span data-stu-id="012de-169">The document will contain the steps with relevant screenshots.</span></span>

> [!NOTE]
> <span data-ttu-id="012de-170">Функциональная возможность записи снимков экранов не поддерживается в Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="012de-170">Capture screenshot functionality is not supported in Cloud POS.</span></span>

### <a name="start-task-and-end-task"></a><span data-ttu-id="012de-171">Начать задачу и закончить задачу</span><span class="sxs-lookup"><span data-stu-id="012de-171">Start task and End task</span></span>

<span data-ttu-id="012de-172">Начало и конец набора сгруппированных этапов можно указать с помощью кнопки **Начать задачу** и **Закончить** **задачу**.</span><span class="sxs-lookup"><span data-stu-id="012de-172">You can specify the beginning and end of a set of grouped steps by using the **Start task** and **End** **task** buttons.</span></span> <span data-ttu-id="012de-173">Щелкните **Начать задачу**, чтобы добавить шаг "Начать задачу", затем выполните действия, которые должны быть включены в эту группу.</span><span class="sxs-lookup"><span data-stu-id="012de-173">Click **Start task** to add a "Start Task" step, and then perform the steps that should be included in the group.</span></span> <span data-ttu-id="012de-174">После завершения выполнения шагов для группы нажмите кнопку **Завершить задачу**.</span><span class="sxs-lookup"><span data-stu-id="012de-174">After you've finished performing the steps for the group, click **End task**.</span></span> <span data-ttu-id="012de-175">Задачи помогают упорядочить процедуры.</span><span class="sxs-lookup"><span data-stu-id="012de-175">Tasks help you organize your procedures.</span></span> <span data-ttu-id="012de-176">Задачи могут быть вложенными в другие задачи.</span><span class="sxs-lookup"><span data-stu-id="012de-176">Tasks can be nested within other tasks.</span></span> <span data-ttu-id="012de-177">Таким образом можно лучше организовать очень длинные и сложные бизнес-процессы.</span><span class="sxs-lookup"><span data-stu-id="012de-177">In this way, you can better organize very long and complex business processes.</span></span>

## <a name="adding-annotations"></a><span data-ttu-id="012de-178">Добавление заметок</span><span class="sxs-lookup"><span data-stu-id="012de-178">Adding annotations</span></span>

<span data-ttu-id="012de-179">Заметка представляет собой дополнительный текст, который добавляется к шагу в записи.</span><span class="sxs-lookup"><span data-stu-id="012de-179">An annotation is additional text that you add to a step in a recording.</span></span> <span data-ttu-id="012de-180">Например, можно использовать заметки для предоставления пользователю дополнительного контекста или инструкций.</span><span class="sxs-lookup"><span data-stu-id="012de-180">For example, you can use annotations to give the user more context or instructions.</span></span> <span data-ttu-id="012de-181">Можно добавить заметку до или после шага.</span><span class="sxs-lookup"><span data-stu-id="012de-181">You can add annotations before or after a step.</span></span> <span data-ttu-id="012de-182">Можно добавить заметку к любому шагу, нажав кнопку **Изменить** (символ карандаша) справа от шага.</span><span class="sxs-lookup"><span data-stu-id="012de-182">You can add an annotation to any step by clicking the **Edit** button (pencil symbol) to the right of the step.</span></span>

<span data-ttu-id="012de-183">[![Кнопка "Изменить" для шага](./media/annotate.jpg)](./media/annotate.jpg)</span><span class="sxs-lookup"><span data-stu-id="012de-183">[![Edit button for a step](./media/annotate.jpg)](./media/annotate.jpg)</span></span>

### <a name="texts-and-notes"></a><span data-ttu-id="012de-184">Тексты и примечания</span><span class="sxs-lookup"><span data-stu-id="012de-184">Texts and notes</span></span>

<span data-ttu-id="012de-185">Можно использовать поля **Тексты** и **Примечания**, чтобы добавить текст, который должен быть связан с шагом в проводнике по задаче.</span><span class="sxs-lookup"><span data-stu-id="012de-185">You can use the **Texts** and **Notes** fields to add text that should be associated with a step in a Task guide.</span></span>

<span data-ttu-id="012de-186">[![Поля текста и примечаний](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)</span><span class="sxs-lookup"><span data-stu-id="012de-186">[![Text and Notes fields](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)</span></span>

#### <a name="text"></a><span data-ttu-id="012de-187">Текст</span><span class="sxs-lookup"><span data-stu-id="012de-187">Text</span></span>

<span data-ttu-id="012de-188">Текст, введенный в поле **Текст**, появляется *над* текстом шага проводника по задаче.</span><span class="sxs-lookup"><span data-stu-id="012de-188">Text that you enter in the **Text** field appears *above* the step text in the Task guide.</span></span> <span data-ttu-id="012de-189">Это расположение подходит для текста, который пользователь должен прочитать перед выполнением шага.</span><span class="sxs-lookup"><span data-stu-id="012de-189">This location is appropriate for text that you want the user to read before he or she completes the step.</span></span>

#### <a name="notes"></a><span data-ttu-id="012de-190">Заметки</span><span class="sxs-lookup"><span data-stu-id="012de-190">Notes</span></span>

<span data-ttu-id="012de-191">Текст, введенный в поле **Примечания**, появляется *под* текстом шага проводника по задаче.</span><span class="sxs-lookup"><span data-stu-id="012de-191">Text that you enter in the **Notes** field appears *below* the step text in the Task guide.</span></span> <span data-ttu-id="012de-192">Чтобы прочитать текст примечания, пользователю необходимо развернуть текст шага во всплывающем окне.</span><span class="sxs-lookup"><span data-stu-id="012de-192">To read the note text, the user must expand the step text in the pop-up window.</span></span> <span data-ttu-id="012de-193">Это расположение подходит для необязательных дополнительных материалов и другой информации, которая может быть полезна для пользователя, но не требуется ему для выполнения действия.</span><span class="sxs-lookup"><span data-stu-id="012de-193">This location is appropriate for optional reading material or other information that might be useful to the user, but that the user doesn't require in order to complete the action.</span></span>

## <a name="help-in-retail-modern-pos-and-cloud-pos"></a><span data-ttu-id="012de-194">Справка в Retail Modern POS и Cloud POS</span><span class="sxs-lookup"><span data-stu-id="012de-194">Help in Retail Modern POS and Cloud POS</span></span>

<span data-ttu-id="012de-195">Чтобы отобразить собственные пользовательские записи задач в области справки Retail Modern POS и Cloud POS, чтобы их можно было просмотреть как текст, необходимо сохранить записи задач в собственной библиотеке BPM, а затем обновить параметры системы справки, чтобы она указывала на вашу библиотеку BPM.</span><span class="sxs-lookup"><span data-stu-id="012de-195">To show your own custom task recordings in the Help pane of Retail Modern POS and Cloud POS so that they can be viewed as text, you must save your task recordings to your own BPM library, and then update your Help system parameters to point to your BPM library.</span></span> <span data-ttu-id="012de-196">Дополнительные сведения см. в разделе [Подключение системы справки](../fin-and-ops/get-started/help-connect.md).</span><span class="sxs-lookup"><span data-stu-id="012de-196">For more information, see [Connecting the Help system](../fin-and-ops/get-started/help-connect.md).</span></span> <span data-ttu-id="012de-197">Справка Retail Modern POS и Cloud POS выполняет поиск в LCS в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="012de-197">Retail Modern POS and Cloud POS Help searches LCS in real time.</span></span> <span data-ttu-id="012de-198">Поиск производится во всех библиотеках BPM, которые выбраны в параметрах системы справки Commerce, и отображаются соответствующие результаты.</span><span class="sxs-lookup"><span data-stu-id="012de-198">It searches across all the BPM libraries that are selected in the Commerce Help system parameters and shows the relevant results.</span></span> <span data-ttu-id="012de-199">Для доступа к меню **Справка** щелкните кнопку **Справка** (вопросительный знак), расположенную в верхней части экрана, затем в поле поиска введите имя процесса и нажмите кнопку поиска.</span><span class="sxs-lookup"><span data-stu-id="012de-199">To access the **Help** menu, click the **Help** button (question mark) at the top of the screen and then in the search box type your process name and hit the search button.</span></span>

<span data-ttu-id="012de-200">[![Кнопка "Справка"](./media/help.jpg)](./media/help.jpg)</span><span class="sxs-lookup"><span data-stu-id="012de-200">[![Help button](./media/help.jpg)](./media/help.jpg)</span></span>

<span data-ttu-id="012de-201">При нажатии кнопки проводника по задаче в результатах поиска можно просмотреть шаги в виде раздела справки или экспортировать эти шаги в документ Word.</span><span class="sxs-lookup"><span data-stu-id="012de-201">When you click a Task guide in the search results, you can either view the steps as a Help topic or export the steps to a Word document.</span></span>

> [!NOTE]
> <span data-ttu-id="012de-202">Справка в Retail Modern POS и Cloud POS не открывает проводники по задачам в зависимости от того, в какой форме вы находитесь или какую операцию выполняете.</span><span class="sxs-lookup"><span data-stu-id="012de-202">Help in Retail Modern POS and Cloud POS will not bring up task guides according to what form you're on or operation you're doing.</span></span> <span data-ttu-id="012de-203">Необходимо ввести имя процесса в поле поиска и нажать кнопку **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="012de-203">You have to type the process name in the search box and then click **Search**.</span></span>
