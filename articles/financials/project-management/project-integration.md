---
title: "Интеграция с клиентом Microsoft Project"
description: "Планирование и поддержка графика проекта может быть сложным делом, поэтому руководители проектов должны использовать средства, помогающие справиться с этой задачей. Интеграция с клиентом Microsoft Project обеспечивает поддержку для открытия и управления структурной декомпозицией работ по проекту."
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: a72963f755f8eddb19b8526d2938eff039ab7df2
ms.contentlocale: ru-ru
ms.lasthandoff: 01/17/2018

---

# <a name="microsoft-project-client-integration"></a><span data-ttu-id="55109-104">Интеграция с клиентом Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="55109-104">Microsoft Project client integration</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="55109-105">Планирование и поддержка графика проекта может быть сложным делом, поэтому руководители проектов должны использовать средства, помогающие справиться с этой задачей.</span><span class="sxs-lookup"><span data-stu-id="55109-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="55109-106">Интеграция с клиентом Microsoft Project обеспечивает поддержку для открытия и управления структурной декомпозицией работ по проекту.</span><span class="sxs-lookup"><span data-stu-id="55109-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="55109-107">Руководитель проекта может обратно публиковать любые изменения в структурной декомпозиции работ по проекту в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="55109-107">The project manager can publish any changes back to the Finance and Operations project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="55109-108">При использовании Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, обновление от июля 2017 г., необходимо установить пакеты обновления KB 4054797 и 4055884.</span><span class="sxs-lookup"><span data-stu-id="55109-108">If you are using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, July update, you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="55109-109">Настройка надстройки клиента Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="55109-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="55109-110">Чтобы включить интеграцию с клиентом Microsoft Project, необходимо установить надстройку Microsoft Dynamics 365 в клиентское приложение Microsoft Project пользователя.</span><span class="sxs-lookup"><span data-stu-id="55109-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="55109-111">Это можно сделать, открыв **рабочую область управления проектами**.</span><span class="sxs-lookup"><span data-stu-id="55109-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="55109-112">• Щелкните **Настройка надстройки клиента Project** в разделе **Ссылки** > **Настройка** рабочей области.</span><span class="sxs-lookup"><span data-stu-id="55109-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="55109-113">• Щелкните **Открыть**, щелкните **Выполнить** в ответ на запрос.</span><span class="sxs-lookup"><span data-stu-id="55109-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="55109-114">Открытие и редактирование существующего черновика структурной декомпозиции работ в клиенте Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="55109-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="55109-115">Если для проекта в Finance and Operations уже создана структурная декомпозиция работ, эту структурную декомпозицию работ можно открыть в клиентском приложении Microsoft Project, если эта структурная декомпозиция работ имеет статус черновика.</span><span class="sxs-lookup"><span data-stu-id="55109-115">If a project in Finance and Operations already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="55109-116">Чтобы открыть со страницы **Проект**, щелкните ссылку **Открыть в Microsoft Project** на вкладке **План**. Эту страницу также можно открыть из клиентского приложения Microsoft Project, щелкнув **Открыть** на вкладке **Microsoft Dynamics 365**. Выберите **Юридическое лицо** и **Проект** из списка.</span><span class="sxs-lookup"><span data-stu-id="55109-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="55109-117">При использовании браузера Internet Explorer потребуется щелкнуть **Сохранить**, чтобы вручную открыть из расположения, в которое загружен файл.</span><span class="sxs-lookup"><span data-stu-id="55109-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="55109-118">Можно также щелкнуть **Сохранить и открыть**, чтобы открыть файл в клиенте Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="55109-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="55109-119">Не изменяйте имя файла при сохранении.</span><span class="sxs-lookup"><span data-stu-id="55109-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="55109-120">Прежде чем вносить изменения в файл с помощью клиента Microsoft Project необходимо его извлечь. Щелкните **Извлечь** на вкладке **Microsoft Dynamics 365**. Это исключает одновременное изменение структурной декомпозиции работ в Finance and Operations другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="55109-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance and Operations at the same time.</span></span> <span data-ttu-id="55109-121">Чтобы опубликовать структурную декомпозицию работ после завершения всех изменений, нажмите кнопку **Вернуть** на вкладке **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="55109-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="55109-122">Если проектная группа уже добавлена в проект в Finance and Operations, список ресурсов будет заполнен членами группы.</span><span class="sxs-lookup"><span data-stu-id="55109-122">If a project team has already been added to the project in Finance and Operations, the resource list will be populated with the team members.</span></span> <span data-ttu-id="55109-123">Если проектная группа еще не была добавлена в проект, можно выбрать ресурсы и создать рабочую группы в клиенте Microsoft Project, щелкнув кнопку **Ресурсы** на вкладке **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="55109-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="55109-124">Следующие данные будет синхронизированы обратно с Finance and Operations как часть процесса возврата:</span><span class="sxs-lookup"><span data-stu-id="55109-124">The following data will be synced back to Finance and Operations as part of the check in process:</span></span>

<span data-ttu-id="55109-125">• Имя задачи</span><span class="sxs-lookup"><span data-stu-id="55109-125">•   Task name</span></span>

<span data-ttu-id="55109-126">• Дата начала</span><span class="sxs-lookup"><span data-stu-id="55109-126">•   Start date</span></span>

<span data-ttu-id="55109-127">• Дата завершения</span><span class="sxs-lookup"><span data-stu-id="55109-127">•   Finish date</span></span>

<span data-ttu-id="55109-128">• Предшествующие элементы</span><span class="sxs-lookup"><span data-stu-id="55109-128">•   Predecessors</span></span>

<span data-ttu-id="55109-129">• Наименования ресурсов</span><span class="sxs-lookup"><span data-stu-id="55109-129">•   Resource names</span></span>

<span data-ttu-id="55109-130">• Категория</span><span class="sxs-lookup"><span data-stu-id="55109-130">•   Category</span></span>

<span data-ttu-id="55109-131">• Категория ресурсов</span><span class="sxs-lookup"><span data-stu-id="55109-131">•   Resource category</span></span>

<span data-ttu-id="55109-132">• Отработанные часы</span><span class="sxs-lookup"><span data-stu-id="55109-132">•   Work hours</span></span>

<span data-ttu-id="55109-133">• Заметки</span><span class="sxs-lookup"><span data-stu-id="55109-133">•   Notes</span></span>

<span data-ttu-id="55109-134">• Приоритет</span><span class="sxs-lookup"><span data-stu-id="55109-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="55109-135">Если добавить любые другие столбцы в файл клиента Microsoft Project, они не будут сохранены в файл и не будет отображаться при следующем открытии файла.</span><span class="sxs-lookup"><span data-stu-id="55109-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="55109-136">Создание структурной декомпозиции работ для существующего проекта с помощью клиента Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="55109-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="55109-137">Для создания структурной декомпозиции работ для существующего проекта с помощью клиента Microsoft Project выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="55109-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="55109-138">Откройте клиент Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="55109-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="55109-139">На вкладке **Microsoft Dynamics 365** щелкните **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="55109-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="55109-140">Выберите **Юридическое лицо** для проекта.</span><span class="sxs-lookup"><span data-stu-id="55109-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="55109-141">Выберите **Проект**.</span><span class="sxs-lookup"><span data-stu-id="55109-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="55109-142">Щелкните **Извлечь** на вкладке **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="55109-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="55109-143">Когда все будет готово для публикации в Finance and Operations, щелкните **Вернуть** на вкладке **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="55109-143">When ready to publish to Finance and Operations, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="55109-144">Замена существующей структурной декомпозиции работ для существующего проекта с помощью клиента Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="55109-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="55109-145">Чтобы создать новую структурную декомпозицию работ с помощью клиента Microsoft Project и заменить существующую структурную декомпозицию работ для существующего проекта, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="55109-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="55109-146">Откройте клиент Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="55109-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="55109-147">Создание план в клиенте Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="55109-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="55109-148">На вкладке **Microsoft Dynamics 365** щелкните **Сохранить изменения** > **Заменить существующий проект**.</span><span class="sxs-lookup"><span data-stu-id="55109-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="55109-149">Выберите **Юридическое лицо** для проекта.</span><span class="sxs-lookup"><span data-stu-id="55109-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="55109-150">Выберите **Проект**.</span><span class="sxs-lookup"><span data-stu-id="55109-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="55109-151">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="55109-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="55109-152">Создание нового проекта из клиента Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="55109-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="55109-153">Откройте клиент Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="55109-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="55109-154">Создание план в клиенте Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="55109-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="55109-155">На вкладке **Microsoft Dynamics 365** щелкните **Сохранить изменения** > **Сохранить в новый проект**.</span><span class="sxs-lookup"><span data-stu-id="55109-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="55109-156">Выберите **Юридическое лицо** для проекта.</span><span class="sxs-lookup"><span data-stu-id="55109-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="55109-157">Введите **Код проекта**, если требуется.</span><span class="sxs-lookup"><span data-stu-id="55109-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="55109-158">Введите **Имя проекта**.</span><span class="sxs-lookup"><span data-stu-id="55109-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="55109-159">Выберите значения в полях **Тип проекта**, **Группа проекта** и **Код контракта по проекту**.</span><span class="sxs-lookup"><span data-stu-id="55109-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="55109-160">Можно также создать новый контракт по проекту, щелкнув **Создать**.</span><span class="sxs-lookup"><span data-stu-id="55109-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="55109-161">Выберите **Календарь** для подбора ресурсов.</span><span class="sxs-lookup"><span data-stu-id="55109-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="55109-162">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="55109-162">Click **OK**.</span></span>

