---
title: "Подключение к системе справки"
description: "В этом разделе описываются компоненты системы Справки для Microsoft Dynamics 365 for Finance and Operations и приводится обзор того, как подключить их и сводку того, как создать собственную справки."
author: margoc
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 87ca6afe817d27de12479f1b7d8155d11d800233
ms.openlocfilehash: a2ca5f5302751ad2c4ddc3c6921a8a9b6c2d57df
ms.contentlocale: ru-ru
ms.lasthandoff: 12/04/2018

---

# <a name="connect-the-help-system"></a><span data-ttu-id="26468-103">Подключение к системе справки</span><span class="sxs-lookup"><span data-stu-id="26468-103">Connect the Help system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26468-104">В этой теме описываются компоненты системы Справки для Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="26468-104">This topic describes the components of the Help system for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="26468-105">В нем приводится обзор того, как подключить эти компоненты, и сводку того, как создать собственную справку.</span><span class="sxs-lookup"><span data-stu-id="26468-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span> 

## <a name="help-architecture"></a><span data-ttu-id="26468-106">Архитектура справки</span><span class="sxs-lookup"><span data-stu-id="26468-106">Help architecture</span></span>
<span data-ttu-id="26468-107">На следующем рисунке показаны части системы Справки Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="26468-107">The following illustration shows the parts of the Finance and Operations Help system.</span></span> <span data-ttu-id="26468-108">Система встроенной в продукт справки извлекает статьи с вики-сайта справки Finance and Operations по адресу https://docs.microsoft.com, а также руководства по задачам, хранящиеся в средстве моделирования бизнес-процессов в Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="26468-108">The in-product Help system pulls articles from the Finance and Operations site on https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span> 
> [!NOTE]
> <span data-ttu-id="26468-109">Функции на диаграмме, рядом с которыми указана звездочка (\*), запланированы, но еще недоступны.</span><span class="sxs-lookup"><span data-stu-id="26468-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span> <span data-ttu-id="26468-110">[![Архитектура справки](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="26468-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>


## <a name="connecting-the-help-system"></a><span data-ttu-id="26468-111">Подключение системы справки</span><span class="sxs-lookup"><span data-stu-id="26468-111">Connecting the Help system</span></span>
> [!NOTE]
> <span data-ttu-id="26468-112">Вкладка **Проводники по задачам** в настоящее время недоступна в Microsoft Dynamics 365 for Talent и Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="26468-112">The **Task guides** tab is currently not available in Microsoft Dynamics 365 for Talent and Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="26468-113">Мы в настоящее время работаем для включения этой функции в будущих выпусках.</span><span class="sxs-lookup"><span data-stu-id="26468-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="26468-114">Проводники по задачам в разделе начала работы в Talent остаются доступными для работы с основными функциями.</span><span class="sxs-lookup"><span data-stu-id="26468-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="26468-115">Практические советы можно также получить на сайте docs.microsoft.com ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) для Retail и Talent.</span><span class="sxs-lookup"><span data-stu-id="26468-115">Procedural help is also available on the docs.microsoft.com site ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) for both Retail and Talent.</span></span>


<span data-ttu-id="26468-116">С помощью страницы **Системные параметры** системные администраторы подключают части системы справки для реализации.</span><span class="sxs-lookup"><span data-stu-id="26468-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span> <span data-ttu-id="26468-117">[![Форма "Системные параметры" с настройками системы справки](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) На странице **Системные параметры** выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="26468-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="26468-118">При первом открытии вкладки **Справка** необходимо подключиться к службами Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="26468-118">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="26468-119">Необходимо нажать на ссылку в середине формы, дождаться подключения, закрыть диалоговое окно, затем нажать **ОК**, чтобы перейти на страницу **Системные параметры**.[![Подключение к LCS](./media/connect-to-lcs-crop-1024x365.png "Подключение к LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="26468-119">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1.  <span data-ttu-id="26468-120">Выберите проект Lifecycle Services для подключения.</span><span class="sxs-lookup"><span data-stu-id="26468-120">Select the Lifecycle Services project to connect to.</span></span>
2.  <span data-ttu-id="26468-121">Выберите библиотеки BPM (в пределах выбранного проекта), из которых требуется извлечь записи задач.</span><span class="sxs-lookup"><span data-stu-id="26468-121">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
    - <span data-ttu-id="26468-122">В Finance and Operations для содержимого Microsoft выберите самую последнюю унифицированную библиотеку APQC для Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="26468-122">For Finance and Operations, for Microsoft content, select the most recent APQC Unified Library for Finance and Operations.</span></span> 
    - <span data-ttu-id="26468-123">Для Retail мы выпустим библиотеку в ближайшем будущем.</span><span class="sxs-lookup"><span data-stu-id="26468-123">For Retail, we will be releasing a library in the near future.</span></span> 
    - <span data-ttu-id="26468-124">Нет необходимости выбирать библиотеку для Talent: правильная библиотека уже подключена.</span><span class="sxs-lookup"><span data-stu-id="26468-124">You do not need to select a library for Talent—the connection to the correct library is established for you.</span></span> 

3.  <span data-ttu-id="26468-125">Задайте порядок отображения библиотек BPM.</span><span class="sxs-lookup"><span data-stu-id="26468-125">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="26468-126">Это определяет порядок, в котором записи задач из библиотек будут отображаться в области **Справка**.</span><span class="sxs-lookup"><span data-stu-id="26468-126">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="26468-127">После выполнения этих шагов вы можете открыть область **Справка** и перейти на вкладку **Проводники по задачам**. Вы увидите проводники по задачам, относящиеся к странице, на которой вы в данный момент находитесь в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="26468-127">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you’re currently on in Finance and Operations.</span></span> <span data-ttu-id="26468-128">Если руководства по задачам не найдены, можно ввести ключевые слова для уточнения поиска.</span><span class="sxs-lookup"><span data-stu-id="26468-128">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="26468-129">Отображение переведенных руководств по задачам</span><span class="sxs-lookup"><span data-stu-id="26468-129">Showing translated task guides</span></span>

<span data-ttu-id="26468-130">Переведенные руководства по задачам были впервые поставлены в унифицированной библиотеке APQC (май 2016) и библиотеке начала работы.</span><span class="sxs-lookup"><span data-stu-id="26468-130">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="26468-131">В Finance and Operations для просмотра локализованной справки руководств по задачам проверьте, что вы подключены к библиотеке за май.</span><span class="sxs-lookup"><span data-stu-id="26468-131">In Finance and Operations, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="26468-132">Язык, на котором отображается руководство по задаче, контролируется для каждого пользователя на основании языковых параметров, заданных в разделе **Параметры** &gt; **Предпочтительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="26468-132">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span> 

> [!NOTE]
> <span data-ttu-id="26468-133">Несмотря на то что было переведено множество руководств по задачам, сейчас в клиенте Finance and Operations не отображаются имена переведенных руководств по задачам.</span><span class="sxs-lookup"><span data-stu-id="26468-133">Even though many task guides have been translated, right now the Finance and Operations client is not showing the translated task guide names.</span></span> <span data-ttu-id="26468-134">Кроме того, в данный момент только руководства по задачам, которые были выпущены в феврале 2016 г., доступны в переводе в библиотеке за май.</span><span class="sxs-lookup"><span data-stu-id="26468-134">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="26468-135">Мы выпустим обновленную библиотеку с дополнительными переводами.</span><span class="sxs-lookup"><span data-stu-id="26468-135">We will release an updated library with additional translations.</span></span>
> -   <span data-ttu-id="26468-136">Если руководство по задаче было переведено, при открытии этого руководства по задаче весь текст руководства по задаче будет отображаться на выбранном языке.</span><span class="sxs-lookup"><span data-stu-id="26468-136">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> -   <span data-ttu-id="26468-137">Если руководство по задаче еще не было переведено, при открытии этого руководства только некоторый текст (текст элементов управления) будет отображаться на выбранном языке.</span><span class="sxs-lookup"><span data-stu-id="26468-137">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="26468-138">Создание пользовательской справки</span><span class="sxs-lookup"><span data-stu-id="26468-138">Creating custom help</span></span>
<span data-ttu-id="26468-139">Можно использовать руководства по задачам для создания настраиваемой справки или подключить веб-сайт к области справки.</span><span class="sxs-lookup"><span data-stu-id="26468-139">You can use task guides to create custom help, or connect a website to the Help pane.</span></span> 

### <a name="create-custom-help-with-task-guides"></a><span data-ttu-id="26468-140">Создание пользовательской справки с помощью руководств по задачам</span><span class="sxs-lookup"><span data-stu-id="26468-140">Create custom help with task guides</span></span>
<span data-ttu-id="26468-141">Можно создать пользовательскую справку для реализации Finance and Operations и для Retail, создав записи задач, которые отражают данную реализацию, и сохранив их в библиотеке бизнес-процессов LCS.</span><span class="sxs-lookup"><span data-stu-id="26468-141">You can create custom help for Finance and Operations, and for Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="26468-142">Нельзя создавать пользовательские проводники по задаче для Talent.</span><span class="sxs-lookup"><span data-stu-id="26468-142">You cannot create custom task guides for Talent.</span></span> 

<span data-ttu-id="26468-143">Если вы являетесь партнером и обновляете библиотеку до корпоративной библиотеки и включаете ее в решение, она будет доступна вашим клиентам.</span><span class="sxs-lookup"><span data-stu-id="26468-143">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="26468-144">Вы также можете сделать копию глобальной унифицированной библиотеки APQC, а затем открыть копию, открыть записи задач из нее, изменить их и сохранить записи с изменениями.</span><span class="sxs-lookup"><span data-stu-id="26468-144">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="26468-145">Дополнительные сведения см. в разделе [Создание записи задачи для использования как документации или обучения](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="26468-145">For more information, see [How to create a task recording to use as documentation or training](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-site"></a><span data-ttu-id="26468-146">Подключение пользовательского сайта</span><span class="sxs-lookup"><span data-stu-id="26468-146">Connect a custom site</span></span>
<span data-ttu-id="26468-147">Корпорация Майкрософт предоставляет официальный документ и пример кода, описывающие, как создать и подключить пользовательский сайт справки к области справки.</span><span class="sxs-lookup"><span data-stu-id="26468-147">Microsoft has provided a white paper and sample code that describe how to create and connect a custom help site to the Help pane.</span></span> <span data-ttu-id="26468-148">Дополнительные сведения см.</span><span class="sxs-lookup"><span data-stu-id="26468-148">For more information, see:</span></span> 
- [<span data-ttu-id="26468-149">Создание пользовательской справки для Finance and Operations (технический документ)</span><span class="sxs-lookup"><span data-stu-id="26468-149">Create Custom Help for Finance and Operations (white paper)</span></span>](https://go.microsoft.com/fwlink/?linkid=2041185)
- [<span data-ttu-id="26468-150">Репозиторий GitHub пользовательской справки</span><span class="sxs-lookup"><span data-stu-id="26468-150">Custom help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)



<a name="additional-resources"></a><span data-ttu-id="26468-151">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="26468-151">Additional resources</span></span>
--------

[<span data-ttu-id="26468-152">Обзор справки</span><span class="sxs-lookup"><span data-stu-id="26468-152">Help overview</span></span>](help-overview.md)

[<span data-ttu-id="26468-153">Обзор регистратора задач</span><span class="sxs-lookup"><span data-stu-id="26468-153">Task recorder overview</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="26468-154">Создание записи задачи для использования в качестве документации или обучения</span><span class="sxs-lookup"><span data-stu-id="26468-154">How to create a task recording to use as documentation or training</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)





