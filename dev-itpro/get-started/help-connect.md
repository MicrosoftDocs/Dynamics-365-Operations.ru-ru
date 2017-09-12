---
title: "Подключение к системе справки"
description: "В этом разделе описываются компоненты системы Справки для Microsoft Dynamics 365 for Finance and Operations и приводится обзор того, как подключить их и сводку того, как создать собственную справки."
author: margoc
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: acb832c422ccb5ddb98d6ddd6b69d2e2c3e11057
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---

# <a name="connect-the-help-system"></a><span data-ttu-id="12be0-103">Подключение к системе справки</span><span class="sxs-lookup"><span data-stu-id="12be0-103">Connect the Help system</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="12be0-104">В этой теме описываются компоненты системы Справки для Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="12be0-104">This topic describes the components of the Help system for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="12be0-105">В нем приводится обзор того, как подключить эти компоненты, и сводку того, как создать собственную справку.</span><span class="sxs-lookup"><span data-stu-id="12be0-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span> 

## <a name="help-architecture"></a><span data-ttu-id="12be0-106">Архитектура справки</span><span class="sxs-lookup"><span data-stu-id="12be0-106">Help architecture</span></span>
<span data-ttu-id="12be0-107">На следующем рисунке показаны части системы Справки Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="12be0-107">The following illustration shows the parts of the Finance and Operations Help system.</span></span> <span data-ttu-id="12be0-108">Система встроенной в продукт справки извлекает статьи с вики-сайта справки Finance and Operations по адресу https://docs.microsoft.com, а также руководства по задачам, хранящиеся в средстве моделирования бизнес-процессов в Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="12be0-108">The in-product Help system pulls articles from the Finance and Operations site on https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span> 
> [!NOTE]
> <span data-ttu-id="12be0-109">Функции на диаграмме, рядом с которыми указана звездочка (\*), запланированы, но еще недоступны.</span><span class="sxs-lookup"><span data-stu-id="12be0-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span> <span data-ttu-id="12be0-110">[![Архитектура справки](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="12be0-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>


## <a name="connecting-the-help-system"></a><span data-ttu-id="12be0-111">Подключение системы справки</span><span class="sxs-lookup"><span data-stu-id="12be0-111">Connecting the Help system</span></span>
> [!NOTE]
> <span data-ttu-id="12be0-112">Вкладка **Проводники по задачам** в настоящее время недоступна в Microsoft Dynamics 365 for Talent и Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="12be0-112">The **Task guides** tab is currently not available in Microsoft Dynamics 365 for Talent and Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="12be0-113">Мы в настоящее время работаем для включения этой функции в будущих выпусках.</span><span class="sxs-lookup"><span data-stu-id="12be0-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="12be0-114">Проводники по задачам в разделе начала работы в Talent остаются доступными для работы с основными функциями.</span><span class="sxs-lookup"><span data-stu-id="12be0-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="12be0-115">Практические советы можно также получить на сайте docs.microsoft.com ([docs.microsoft.com/dynamics365/operations](/dynamics365/unified-operations/fin-and-ops/index)) для Retail и Talent.</span><span class="sxs-lookup"><span data-stu-id="12be0-115">Procedural help is also available on the docs.microsoft.com site ([docs.microsoft.com/dynamics365/operations](/dynamics365/unified-operations/fin-and-ops/index)) for both Retail and Talent.</span></span>
 

<span data-ttu-id="12be0-116">С помощью страницы **Системные параметры** системные администраторы подключают части системы справки для реализации.</span><span class="sxs-lookup"><span data-stu-id="12be0-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span> <span data-ttu-id="12be0-117">[![Форма "Системные параметры" с настройками системы справки](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) На странице **Системные параметры** выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="12be0-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="12be0-118">При первом открытии вкладки **Справка** необходимо подключиться к службами Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="12be0-118">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="12be0-119">Необходимо нажать на ссылку в середине формы, дождаться подключения, закрыть диалоговое окно, затем нажать **ОК**, чтобы перейти на страницу **Системные параметры**.[![Подключение к LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="12be0-119">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1.  <span data-ttu-id="12be0-120">Выберите проект Lifecycle Services для подключения.</span><span class="sxs-lookup"><span data-stu-id="12be0-120">Select the Lifecycle Services project to connect to.</span></span>
2.  <span data-ttu-id="12be0-121">Выберите библиотеки BPM (в пределах выбранного проекта), из которых требуется извлечь записи задач.</span><span class="sxs-lookup"><span data-stu-id="12be0-121">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
    - <span data-ttu-id="12be0-122">В Finance and Operations для содержимого Microsoft выберите февраль 2017 г. "Унифицированная библиотека QPC" для Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="12be0-122">For Finance and Operations, for Microsoft content, select the February 2017 QPC Unified Library for Microsoft Dynamics 365 for Finance and Operations.</span></span> 
    - <span data-ttu-id="12be0-123">Для Retail мы выпустим библиотеку в июле.</span><span class="sxs-lookup"><span data-stu-id="12be0-123">For Retail, we will be releasing a library in July.</span></span> 
    - <span data-ttu-id="12be0-124">Нет необходимости выбирать библиотеку для Talent: правильная библиотека уже подключена.</span><span class="sxs-lookup"><span data-stu-id="12be0-124">You do not need to select a library for Talent—the connection to the correct library is established for you.</span></span> 

3.  <span data-ttu-id="12be0-125">Задайте порядок отображения библиотек BPM.</span><span class="sxs-lookup"><span data-stu-id="12be0-125">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="12be0-126">Это определяет порядок, в котором записи задач из библиотек будут отображаться в области **Справка**.</span><span class="sxs-lookup"><span data-stu-id="12be0-126">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="12be0-127">После завершения этих шагов вы сможете открыть область **Справка** и перейти на вкладку **Руководства по задачам**.</span><span class="sxs-lookup"><span data-stu-id="12be0-127">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab.</span></span> <span data-ttu-id="12be0-128">Теперь вы увидите руководства задачи, которые применяются к странице, на которой вы в данный момент в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="12be0-128">You'll now see the task guides that apply to the page that you’re currently on in Finance and Operations.</span></span> <span data-ttu-id="12be0-129">Если руководства по задачам не найдены, можно ввести ключевые слова для уточнения поиска.</span><span class="sxs-lookup"><span data-stu-id="12be0-129">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="12be0-130">Отображение переведенных руководств по задачам</span><span class="sxs-lookup"><span data-stu-id="12be0-130">Showing translated task guides</span></span>

<span data-ttu-id="12be0-131">Переведенные руководства по задачам были впервые поставлены в унифицированной библиотеке APQC (май 2016) и библиотеке начала работы.</span><span class="sxs-lookup"><span data-stu-id="12be0-131">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="12be0-132">В Finance and Operations для просмотра локализованной справки руководств по задачам проверьте, что вы подключены к библиотеке за май.</span><span class="sxs-lookup"><span data-stu-id="12be0-132">In Finance and Operations, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="12be0-133">Язык, на котором отображается руководство по задаче, контролируется для каждого пользователя на основании языковых параметров, заданных в разделе **Параметры** &gt; **Предпочтительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="12be0-133">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span> 

> [!NOTE]
> <span data-ttu-id="12be0-134">Несмотря на то что было переведено множество руководств по задачам, сейчас в клиенте Finance and Operations не отображаются имена переведенных руководств по задачам.</span><span class="sxs-lookup"><span data-stu-id="12be0-134">Even though many task guides have been translated, right now the Finance and Operations client is not showing the translated task guide names.</span></span> <span data-ttu-id="12be0-135">Кроме того, в данный момент только руководства по задачам, которые были выпущены в феврале 2016 г., доступны в переводе в библиотеке за май.</span><span class="sxs-lookup"><span data-stu-id="12be0-135">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="12be0-136">Мы выпустим обновленную библиотеку с дополнительными переводами.</span><span class="sxs-lookup"><span data-stu-id="12be0-136">We will release an updated library with additional translations.</span></span>
> -   <span data-ttu-id="12be0-137">Если руководство по задаче было переведено, при открытии этого руководства по задаче весь текст руководства по задаче будет отображаться на выбранном языке.</span><span class="sxs-lookup"><span data-stu-id="12be0-137">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> -   <span data-ttu-id="12be0-138">Если руководство по задаче еще не было переведено, при открытии этого руководства только некоторый текст (текст элементов управления) будет отображаться на выбранном языке.</span><span class="sxs-lookup"><span data-stu-id="12be0-138">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="12be0-139">Создание пользовательской справки</span><span class="sxs-lookup"><span data-stu-id="12be0-139">Creating custom help</span></span>
<span data-ttu-id="12be0-140">Можно создать пользовательскую справку для реализации Finance and Operations и для Retail, создав записи задач, которые отражают данную реализацию, и сохранив их в библиотеке бизнес-процессов LCS.</span><span class="sxs-lookup"><span data-stu-id="12be0-140">You can create custom help for Finance and Operations, and for Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="12be0-141">Нельзя создавать пользовательские проводники по задаче для Talent.</span><span class="sxs-lookup"><span data-stu-id="12be0-141">You cannot create custom task guides for Talent.</span></span> 

<span data-ttu-id="12be0-142">Если вы являетесь партнером и обновляете библиотеку до корпоративной библиотеки и включаете ее в решение, она будет доступна вашим клиентам.</span><span class="sxs-lookup"><span data-stu-id="12be0-142">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="12be0-143">Вы также можете сделать копию глобальной унифицированной библиотеки APQC, а затем открыть копию, открыть записи задач из нее, изменить их и сохранить записи с изменениями.</span><span class="sxs-lookup"><span data-stu-id="12be0-143">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="12be0-144">Дополнительные сведения см. в разделе [Создание записи задачи для использования как документации или обучения](../user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="12be0-144">For more information, see [How to create a task recording to use as documentation or training](../user-interface/task-recorder.md).</span></span>

<a name="see-also"></a><span data-ttu-id="12be0-145">См. также</span><span class="sxs-lookup"><span data-stu-id="12be0-145">See also</span></span>
--------

[<span data-ttu-id="12be0-146">Обзор справки</span><span class="sxs-lookup"><span data-stu-id="12be0-146">Help overview</span></span>](help-overview.md)

[<span data-ttu-id="12be0-147">Обзор регистратора задач</span><span class="sxs-lookup"><span data-stu-id="12be0-147">Task recorder overview</span></span>](../user-interface/task-recorder.md)

[<span data-ttu-id="12be0-148">Создание записи задачи для использования в качестве документации или обучения</span><span class="sxs-lookup"><span data-stu-id="12be0-148">How to create a task recording to use as documentation or training</span></span>](../user-interface/task-recorder-training-docs.md)





