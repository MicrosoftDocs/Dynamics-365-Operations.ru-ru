---
title: Подключение к системе справки
description: В этом разделе описываются компоненты системы справки для приложений Finance and Operations и приводится обзор того, как подключить их и сводку того, как создать собственную справку.
author: margoc
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2955464aa8a220563db1b9ebbb348be52f520659
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812588"
---
# <a name="connect-the-help-system"></a><span data-ttu-id="78dcd-103">Подключение к системе справки</span><span class="sxs-lookup"><span data-stu-id="78dcd-103">Connect the Help system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="78dcd-104">В этой теме описываются компоненты справочной системы для приложений Finance and Operations, таких как Dynamics 365 Finance, Supply Chain Management, Retail и Talent.</span><span class="sxs-lookup"><span data-stu-id="78dcd-104">This topic describes the components of the Help system for Finance and Operations apps, such as Dynamics 365 Finance, Supply Chain Management, Retail, and Talent.</span></span> <span data-ttu-id="78dcd-105">В нем приводится обзор того, как подключить эти компоненты, и сводку того, как создать собственную справку.</span><span class="sxs-lookup"><span data-stu-id="78dcd-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="78dcd-106">Архитектура справки</span><span class="sxs-lookup"><span data-stu-id="78dcd-106">Help architecture</span></span>

<span data-ttu-id="78dcd-107">На следующем рисунке показаны части справочной системы.</span><span class="sxs-lookup"><span data-stu-id="78dcd-107">The following illustration shows the parts of the Help system.</span></span> <span data-ttu-id="78dcd-108">Система встроенной в продукт справки извлекает статьи с сайта https://docs.microsoft.com, а также руководства по задачам, хранящиеся в средстве моделирования бизнес-процессов в Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="78dcd-108">The in-product Help system pulls articles from https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span>

> [!NOTE]
> <span data-ttu-id="78dcd-109">Функции на диаграмме, рядом с которыми указана звездочка (\*), запланированы, но еще недоступны.</span><span class="sxs-lookup"><span data-stu-id="78dcd-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span>

<span data-ttu-id="78dcd-110">[![Архитектура справки](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="78dcd-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

## <a name="connecting-the-help-system"></a><span data-ttu-id="78dcd-111">Подключение системы справки</span><span class="sxs-lookup"><span data-stu-id="78dcd-111">Connecting the Help system</span></span>

> [!NOTE]
> <span data-ttu-id="78dcd-112">Вкладка **Проводники по задачам** в настоящее время недоступна в Dynamics 365 Talent или Retail.</span><span class="sxs-lookup"><span data-stu-id="78dcd-112">The **Task guides** tab is currently not available in Dynamics 365 Talent or Retail.</span></span> <span data-ttu-id="78dcd-113">Мы в настоящее время работаем для включения этой функции в будущих выпусках.</span><span class="sxs-lookup"><span data-stu-id="78dcd-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="78dcd-114">Проводники по задачам в разделе начала работы в Talent остаются доступными для работы с основными функциями.</span><span class="sxs-lookup"><span data-stu-id="78dcd-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="78dcd-115">Процедурная справка доступна также на сайте docs.microsoft.com для Retail и Talent.</span><span class="sxs-lookup"><span data-stu-id="78dcd-115">Procedural help is also available on the docs.microsoft.com site for both Retail and Talent.</span></span>

<span data-ttu-id="78dcd-116">С помощью страницы **Системные параметры** системные администраторы подключают части системы справки для реализации.</span><span class="sxs-lookup"><span data-stu-id="78dcd-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span>

<span data-ttu-id="78dcd-117">[![Форма "Системные параметры" с настройками системы справки](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="78dcd-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="78dcd-118">На странице **Системные параметры** выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="78dcd-118">On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="78dcd-119">При первом открытии вкладки **Справка** необходимо подключиться к службами Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="78dcd-119">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="78dcd-120">Необходимо нажать на ссылку в середине формы, дождаться подключения, закрыть диалоговое окно, затем нажать **ОК**, чтобы перейти на страницу **Системные параметры**.</span><span class="sxs-lookup"><span data-stu-id="78dcd-120">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="78dcd-121">[![Подключение к LCS](./media/connect-to-lcs-crop-1024x365.png "Подключение к LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="78dcd-121">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="78dcd-122">Выберите проект Lifecycle Services для подключения.</span><span class="sxs-lookup"><span data-stu-id="78dcd-122">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="78dcd-123">Выберите библиотеки BPM (в пределах выбранного проекта), из которых требуется извлечь записи задач.</span><span class="sxs-lookup"><span data-stu-id="78dcd-123">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
3. <span data-ttu-id="78dcd-124">Задайте порядок отображения библиотек BPM.</span><span class="sxs-lookup"><span data-stu-id="78dcd-124">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="78dcd-125">Это определяет порядок, в котором записи задач из библиотек будут отображаться в области **Справка**.</span><span class="sxs-lookup"><span data-stu-id="78dcd-125">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="78dcd-126">После выполнения этих шагов вы можете открыть область **Справка** и перейти на вкладку **Проводники по задачам**. Вы увидите проводники по задачам, относящиеся к странице, на которой вы в данный момент находитесь в приложениях Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="78dcd-126">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations apps.</span></span> <span data-ttu-id="78dcd-127">Если руководства по задачам не найдены, можно ввести ключевые слова для уточнения поиска.</span><span class="sxs-lookup"><span data-stu-id="78dcd-127">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="78dcd-128">Отображение переведенных руководств по задачам</span><span class="sxs-lookup"><span data-stu-id="78dcd-128">Showing translated task guides</span></span>

<span data-ttu-id="78dcd-129">Переведенные руководства по задачам были впервые поставлены в унифицированной библиотеке APQC (май 2016) и библиотеке начала работы.</span><span class="sxs-lookup"><span data-stu-id="78dcd-129">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="78dcd-130">В приложениях Finance and Operations для просмотра локализованной справки руководств по задачам проверьте, что вы подключены к библиотеке за май.</span><span class="sxs-lookup"><span data-stu-id="78dcd-130">In Finance and Operations apps, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="78dcd-131">Язык, на котором отображается руководство по задаче, контролируется для каждого пользователя на основании языковых параметров, заданных в разделе **Параметры** &gt; **Предпочтительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="78dcd-131">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="78dcd-132">Несмотря на то, что было переведено множество руководств по задачам, сейчас в клиенте не отображаются имена переведенных руководств по задачам.</span><span class="sxs-lookup"><span data-stu-id="78dcd-132">Even though many task guides have been translated, right now the client is not showing the translated task guide names.</span></span> <span data-ttu-id="78dcd-133">Кроме того, в данный момент только руководства по задачам, которые были выпущены в феврале 2016 г., доступны в переводе в библиотеке за май.</span><span class="sxs-lookup"><span data-stu-id="78dcd-133">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="78dcd-134">Мы выпустим обновленную библиотеку с дополнительными переводами.</span><span class="sxs-lookup"><span data-stu-id="78dcd-134">We will release an updated library with additional translations.</span></span>
>
> - <span data-ttu-id="78dcd-135">Если руководство по задаче было переведено, при открытии этого руководства по задаче весь текст руководства по задаче будет отображаться на выбранном языке.</span><span class="sxs-lookup"><span data-stu-id="78dcd-135">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="78dcd-136">Если руководство по задаче еще не было переведено, при открытии этого руководства только некоторый текст (текст элементов управления) будет отображаться на выбранном языке.</span><span class="sxs-lookup"><span data-stu-id="78dcd-136">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="78dcd-137">Создание пользовательской справки</span><span class="sxs-lookup"><span data-stu-id="78dcd-137">Creating custom help</span></span>

<span data-ttu-id="78dcd-138">Можно использовать руководства по задачам для создания настраиваемой справки или подключить веб-сайт к области справки.</span><span class="sxs-lookup"><span data-stu-id="78dcd-138">You can use task guides to create custom help, or connect a website to the Help pane.</span></span>

### <a name="create-custom-help-with-task-guides"></a><span data-ttu-id="78dcd-139">Создание пользовательской справки с помощью руководств по задачам</span><span class="sxs-lookup"><span data-stu-id="78dcd-139">Create custom help with task guides</span></span>

<span data-ttu-id="78dcd-140">Можно создать пользовательскую справку для реализации Finance, Supply Chain Management и Retail, создав записи задач, которые отражают данную реализацию, и сохранив их в библиотеке бизнес-процессов LCS.</span><span class="sxs-lookup"><span data-stu-id="78dcd-140">You can create custom help for Finance, Supply Chain Management, and Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="78dcd-141">Нельзя создавать пользовательские проводники по задаче для Talent.</span><span class="sxs-lookup"><span data-stu-id="78dcd-141">You cannot create custom task guides for Talent.</span></span>

<span data-ttu-id="78dcd-142">Если вы являетесь партнером и обновляете библиотеку до корпоративной библиотеки и включаете ее в решение, она будет доступна вашим клиентам.</span><span class="sxs-lookup"><span data-stu-id="78dcd-142">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="78dcd-143">Вы также можете сделать копию глобальной унифицированной библиотеки APQC, а затем открыть копию, открыть записи задач из нее, изменить их и сохранить записи с изменениями.</span><span class="sxs-lookup"><span data-stu-id="78dcd-143">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="78dcd-144">Дополнительные сведения см. в разделе [Ресурсы регистратора задач](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="78dcd-144">For more information, see [Task recorder resources](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-site"></a><span data-ttu-id="78dcd-145">Подключение пользовательского сайта</span><span class="sxs-lookup"><span data-stu-id="78dcd-145">Connect a custom site</span></span>

<span data-ttu-id="78dcd-146">Корпорация Майкрософт предоставляет официальный документ и пример кода, описывающие, как создать и подключить пользовательский сайт справки к области справки.</span><span class="sxs-lookup"><span data-stu-id="78dcd-146">Microsoft has provided a white paper and sample code that describe how to create and connect a custom help site to the Help pane.</span></span> <span data-ttu-id="78dcd-147">Дополнительные сведения см.</span><span class="sxs-lookup"><span data-stu-id="78dcd-147">For more information, see:</span></span>

- [<span data-ttu-id="78dcd-148">Создание пользовательской справки для приложений Finance and Operations (технический документ)</span><span class="sxs-lookup"><span data-stu-id="78dcd-148">Create Custom Help for Finance and Operations apps (white paper)</span></span>](https://go.microsoft.com/fwlink/?linkid=2041185)
- [<span data-ttu-id="78dcd-149">Репозиторий GitHub пользовательской справки</span><span class="sxs-lookup"><span data-stu-id="78dcd-149">Custom help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a><span data-ttu-id="78dcd-150">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="78dcd-150">Additional resources</span></span>

[<span data-ttu-id="78dcd-151">Система справки</span><span class="sxs-lookup"><span data-stu-id="78dcd-151">Help system</span></span>](help-overview.md)

[<span data-ttu-id="78dcd-152">Ресурсы регистратора задач</span><span class="sxs-lookup"><span data-stu-id="78dcd-152">Task recorder resources</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="78dcd-153">Создание документации или учебных материалов с помощью регистратора задач</span><span class="sxs-lookup"><span data-stu-id="78dcd-153">Create documentation or training with Task Recorder</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)
