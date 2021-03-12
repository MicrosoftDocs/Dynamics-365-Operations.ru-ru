---
title: Настройка справочной системы для приложений Finance and Operations
description: В этом разделе приводятся сведения о компонентах системы справки для некоторых приложений Microsoft Dynamics 365. Здесь также объясняется, как подключить эти приложения и приводятся сведения о процессе создания пользовательской справки.
author: margoc
manager: AnnBe
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d000c3f801d382921a027c8ee259fd44ac5cdc80
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798288"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a><span data-ttu-id="6b1ef-104">Настройка справочной системы для приложений Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6b1ef-104">Configure the Help experience for Finance and Operations apps</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6b1ef-105">В этом разделе содержится обзор компонентов системы справки для приложений Finance and Operations, таких как Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce и Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-105">In this topic, you will find an overview of the components of the Help system for Finance and Operations apps, such as Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources.</span></span> <span data-ttu-id="6b1ef-106">В этом разделе также объясняется, как подключить эти компоненты и приводятся сведения о процессе создания пользовательской справки.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-106">The topic also explains how to connect these components and provides a summary of the process for creating custom Help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="6b1ef-107">Архитектура справки</span><span class="sxs-lookup"><span data-stu-id="6b1ef-107">Help architecture</span></span>

<span data-ttu-id="6b1ef-108">Приложения Finance and Operations включают концептуальные обзоры и другие разделы, опубликованные на сайте [https://docs.microsoft.com/dynamics365](/dynamics365/).</span><span class="sxs-lookup"><span data-stu-id="6b1ef-108">Finance and Operations apps include conceptual overviews and other topics that are published to the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span> <span data-ttu-id="6b1ef-109">К этому содержимому можно получить доступ в области встроенной в продукт **справки**.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-109">This content can then be accessed from the in-product **Help** pane.</span></span> <span data-ttu-id="6b1ef-110">На следующем рисунке показаны части справочной системы.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-110">The following illustration shows the parts of the Help system.</span></span>

<span data-ttu-id="6b1ef-111">[![Архитектура справки](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="6b1ef-111">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

<span data-ttu-id="6b1ef-112">Система встроенной в продукт справки извлекает статьи с docs.microsoft.com и других подключенных веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-112">The in-product Help system pulls articles from docs.microsoft.com and other connected websites.</span></span> <span data-ttu-id="6b1ef-113">Он также извлекает проводники по задачам, которые хранятся в Средстве моделирования бизнес-процессов (BPM) в Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="6b1ef-113">It also pulls in task guides that are stored in Business process modeler (BPM) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="adding-task-guides"></a><span data-ttu-id="6b1ef-114">Добавление проводники по задачам</span><span class="sxs-lookup"><span data-stu-id="6b1ef-114">Adding task guides</span></span>

> [!NOTE]
> <span data-ttu-id="6b1ef-115">Вкладка **Проводники по задачам** в настоящее время недоступна в Human Resources или Commerce.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-115">The **Task guides** tab isn't currently available in Human Resources or Commerce.</span></span> <!--We are currently working to enable this functionality in a future release.--> <span data-ttu-id="6b1ef-116">Тем не менее, проводники по задачам в разделе начала работы в Human Resources остаются доступными для работы с основными функциями.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-116">However, the task guides in the Getting Started experience in Human Resources remain available to cover basic functionality.</span></span> <span data-ttu-id="6b1ef-117">Процедурная справка для Human Resources и Commerce доступна также на сайте [https://docs.microsoft.com/dynamics365](/dynamics365/).</span><span class="sxs-lookup"><span data-stu-id="6b1ef-117">For both Human Resources and Commerce, procedural Help is available on the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span>

<span data-ttu-id="6b1ef-118">На странице **Системные параметры** системные администраторы могут настроить доступ к соответствующим библиотекам проводников по задаче для реализации.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-118">On the **System parameters** page, system admins can configure access to the relevant task guide libraries for an implementation.</span></span>

> [!NOTE]
> - <span data-ttu-id="6b1ef-119">Для настройки Справки необходимо войти с помощью учетной записи в том же владельце, что и владелец, в котором развернуто приложение.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-119">To configure Help, you must sign in by using an account in the same tenant as the tenant where the app is deployed.</span></span>
> - <span data-ttu-id="6b1ef-120">Невозможно подключить библиотеку LCS из экземпляра приложения, выполняемого на локальном виртуальном жестком диске (VHD).</span><span class="sxs-lookup"><span data-stu-id="6b1ef-120">An LCS library can't be connected from an instance of the app that is running on a local virtual hard drive (VHD).</span></span>

<span data-ttu-id="6b1ef-121">[![Форма "Системные параметры" с настройками системы справки](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="6b1ef-121">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="6b1ef-122">Чтобы настроить проводники по задачам для решения, выполните следующие действия на странице **Системные параметры**.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-122">To configure task guides for a solution, follow these steps on the **System parameters** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b1ef-123">При первом открытии вкладки **Справка** необходимо подключиться к службами Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-123">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="6b1ef-124">Необходимо выбрать на ссылку в середине формы, дождаться подключения, закрыть диалоговое окно, затем выбрать **ОК**, чтобы перейти на страницу **Системные параметры**.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-124">Be sure to select the link in the middle of the form, wait for the connection, close the dialog box, and then select **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="6b1ef-125">[![Подключение к LCS](./media/connect-to-lcs-crop-1024x365.png "Подключение к LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="6b1ef-125">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="6b1ef-126">Выберите проект Lifecycle Services для подключения.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-126">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="6b1ef-127">Выберите библиотеки BPM (в пределах выбранного проекта), из которых требуется извлечь записи задач.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-127">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
3. <span data-ttu-id="6b1ef-128">Задайте порядок отображения библиотек BPM.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-128">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="6b1ef-129">Порядок отображения определяет порядок, в котором записи задач из библиотек будут отображаться в области **Справка**.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-129">The display order defines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="6b1ef-130">После выполнения этих шагов вы можете открыть область **Справка** и выберите вкладку **Проводники по задачам**. Вы увидите проводники по задачам, относящиеся к странице, на которой вы в данный момент находитесь в приложениях Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-130">After you complete these steps, you can open the **Help** pane and select the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations apps.</span></span> <span data-ttu-id="6b1ef-131">Если руководства по задачам не найдены, можно ввести ключевые слова для уточнения поиска.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-131">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="6b1ef-132">Отображение переведенных руководств по задачам</span><span class="sxs-lookup"><span data-stu-id="6b1ef-132">Showing translated task guides</span></span>

<span data-ttu-id="6b1ef-133">Переведенные проводники по задачам были впервые выпущены в унифицированной библиотеке APQC (май 2016) и в библиотеке начала работы.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-133">Translated task guides were first released in the May 2016 APQC Unified Library and in the Getting Started library.</span></span> <span data-ttu-id="6b1ef-134">Для просмотра локализованной справки проводников по задачам проверьте, что ваше решение Dynamics 365 подключено к библиотеке за май 2016.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-134">To view localized task guide Help, make sure that your Dynamics 365 solution is connected to the May 2016 library.</span></span> <span data-ttu-id="6b1ef-135">Пользователь может изменить язык, на котором отображается проводник по задаче, изменив языковые параметры в разделе **Параметры** &gt; **Предпочтения**.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-135">Users can change the language that a task guide appears in by changing the language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="6b1ef-136">Хотя множество проводников по задачам было переведено, в клиенте на данный момент не отображаются имена переведенных проводников по задачам.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-136">Although many task guides have been translated, the client doesn't currently show the translated task guide names.</span></span> <span data-ttu-id="6b1ef-137">Кроме того, в библиотеке за май 2016 года переводы доступны только для проводников по задачам, выпущенных в феврале 2016 года.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-137">Additionally, in the May 2016 library, translations are available only for the task guides that were released in February 2016.</span></span> <span data-ttu-id="6b1ef-138">Microsoft выпустит обновленную библиотеку, включающую дополнительные переводы.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-138">Microsoft will release an updated library that includes additional translations.</span></span>
>
> - <span data-ttu-id="6b1ef-139">Если руководство по задаче было переведено, при открытии этого руководства по задаче весь текст руководства по задаче будет отображаться на выбранном языке.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-139">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="6b1ef-140">Если руководство по задаче еще не было переведено, при открытии этого руководства только некоторый текст (текст элементов управления) будет отображаться на выбранном языке.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-140">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="adding-custom-help"></a><span data-ttu-id="6b1ef-141">Добавление пользовательской справки</span><span class="sxs-lookup"><span data-stu-id="6b1ef-141">Adding custom Help</span></span>

<span data-ttu-id="6b1ef-142">Можно использовать проводники по задачам для создания настраиваемой справки или подключить веб-сайт пользовательской справки к области **справки**.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-142">You can use task guides to create custom Help, or you can connect a custom Help website to the **Help** pane.</span></span>

### <a name="create-custom-help-by-using-task-guides"></a><span data-ttu-id="6b1ef-143">Создание пользовательской справки с помощью проводников по задачам</span><span class="sxs-lookup"><span data-stu-id="6b1ef-143">Create custom Help by using task guides</span></span>

<span data-ttu-id="6b1ef-144">Можно создать пользовательскую справку для поддерживаемых приложений, создав записи задач, которые отражают данную реализацию, и затем сохранив их в библиотеке бизнес-процессов в LCS.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-144">You can create custom Help for the supported apps by creating task recordings that reflect your implementation and then saving them to a Business process library in LCS.</span></span> <span data-ttu-id="6b1ef-145">Кроме того, нельзя создавать пользовательские проводники по задаче для Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-145">You can't create custom task guides for Human Resources.</span></span>

<span data-ttu-id="6b1ef-146">Если вы являетесь партнером и обновляете библиотеку до корпоративной библиотеки и включаете ее в решение, она будет доступна вашим клиентам.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-146">If you're a partner, and you promote a library to a corporate library and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="6b1ef-147">Вы также можете сделать копию унифицированной библиотеки APQC, а затем открыть записи задач в копии, изменить их и сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-147">You can also make a copy of the APQC Unified Library, and then open the task recordings in the copy, edit them, and save your changes.</span></span> <span data-ttu-id="6b1ef-148">Дополнительные сведения см. в разделе [Ресурсы регистратора задач](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="6b1ef-148">For more information, see [Task recorder resources](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-help-site"></a><span data-ttu-id="6b1ef-149">Подключение к пользовательскому сайту справки</span><span class="sxs-lookup"><span data-stu-id="6b1ef-149">Connect a custom Help site</span></span>

<span data-ttu-id="6b1ef-150">Приложения Finance and Operations редко используются в готовой форме.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-150">Finance and Operations apps are rarely used in their out-of-box form.</span></span> <span data-ttu-id="6b1ef-151">Вместо этого решение настраивается и расширяется в соответствии с потребностями организации.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-151">Instead, the solution is customized and extended to fit the organization's needs.</span></span> <span data-ttu-id="6b1ef-152">Можно также настроить и расширить справочную систему.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-152">You can also customize and extend the Help experience.</span></span> <span data-ttu-id="6b1ef-153">Например, можно добавить пользовательскую справку в область встроенной в продукт **справки**.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-153">For example, you can add custom Help to the in-product **Help** pane.</span></span>

<span data-ttu-id="6b1ef-154">Microsoft представила набор средств, помогающих развернуть и подключить пользовательскую справку к области **справки**.</span><span class="sxs-lookup"><span data-stu-id="6b1ef-154">Microsoft has provided a toolkit to help you deploy and connect custom Help to the **Help** pane.</span></span> <span data-ttu-id="6b1ef-155">Сведения о настройке решения пользовательского справки, которое связано с областью **справки**, см. в разделе [Обзор пользовательской справки](../../dev-itpro/help/custom-help-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6b1ef-155">For information about how you can set up a custom Help solution that is connected to the **Help** pane, see [Custom Help overview](../../dev-itpro/help/custom-help-overview.md).</span></span>

<span data-ttu-id="6b1ef-156">Если требуется совместная работа с Microsoft по средствам и процессам для настройки справки, заполните форму в [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).</span><span class="sxs-lookup"><span data-stu-id="6b1ef-156">If you want to collaborate with Microsoft on tools and processes for customizing Help, fill in the form at [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).</span></span>

## <a name="see-also"></a><span data-ttu-id="6b1ef-157">См. также</span><span class="sxs-lookup"><span data-stu-id="6b1ef-157">See also</span></span>

[<span data-ttu-id="6b1ef-158">Система справки</span><span class="sxs-lookup"><span data-stu-id="6b1ef-158">Help system</span></span>](help-overview.md)  
[<span data-ttu-id="6b1ef-159">Обзор пользовательской справки</span><span class="sxs-lookup"><span data-stu-id="6b1ef-159">Custom Help overview</span></span>](../../dev-itpro/help/custom-help-overview.md)  
[<span data-ttu-id="6b1ef-160">Ресурсы регистратора задач</span><span class="sxs-lookup"><span data-stu-id="6b1ef-160">Task recorder resources</span></span>](../../dev-itpro/user-interface/task-recorder.md)  
[<span data-ttu-id="6b1ef-161">Создание документации или учебных материалов с помощью регистратора задач</span><span class="sxs-lookup"><span data-stu-id="6b1ef-161">Create documentation or training with Task Recorder</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[<span data-ttu-id="6b1ef-162">Репозиторий GitHub пользовательской справки</span><span class="sxs-lookup"><span data-stu-id="6b1ef-162">Custom Help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)  
