---
title: Учебник по настройке и установке средства Regression Suite Automation Tool
description: В этом разделе представлен учебник, в котором показано, как настроить и установить средство Regression Suite Automation Tool (RSAT).
author: robinarh
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761, NotInToc
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2019-05-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 7c6e4dcbd854cfadbc34f0040dcffd277d32a8d9
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909042"
---
# <a name="set-up-and-install-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="3a07d-103">Учебник по настройке и установке средства Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="3a07d-103">Set up and install Regression suite automation tool tutorial</span></span>

<span data-ttu-id="3a07d-104">Этот раздел представляет собой учебник, который поможет вам настроить и начать работу с RSAT и средствами, связанными с использованием RSAT.</span><span class="sxs-lookup"><span data-stu-id="3a07d-104">This topic is a tutorial that helps you get setup and get started with RSAT and the tools associated with using RSAT.</span></span>

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="3a07d-105">Загрузите и сохраните эту страницу в формате PDF с помощью средств веб-браузера.</span><span class="sxs-lookup"><span data-stu-id="3a07d-105">Use your internet browser tools to download and save this page in PDF format.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="3a07d-106">Ключевые понятия</span><span class="sxs-lookup"><span data-stu-id="3a07d-106">Key concepts</span></span>

- <span data-ttu-id="3a07d-107">Изучите порядок установки и необходимые условия для настройки, необходимые для различных приложений, которые поддерживают средство Regression Suite Automation Tool (RSAT).</span><span class="sxs-lookup"><span data-stu-id="3a07d-107">Understand the installation and prerequisite setup that are required for the various applications that support Regression suite automation tool (RSAT).</span></span>
- <span data-ttu-id="3a07d-108">Узнайте, как функция регистратора задач в сочетании со службами Microsoft Dynamics Lifecycle Services (LCS) и Microsoft Azure DevOps позволяют создавать, настраивать, выполнять и исследовать тестовые случаи, а также подготавливать отчеты по ним.</span><span class="sxs-lookup"><span data-stu-id="3a07d-108">Understand how the Task recorder feature, together with Microsoft Dynamics Lifecycle Services (LCS) and Microsoft Azure DevOps, let you create, configure, run, investigate, and report on test cases.</span></span>
- <span data-ttu-id="3a07d-109">Предоставьте функциональным пользователям возможность записи деловых задач с помощью регистратора задач, а затем преобразуйте записи задач в набор автоматических тестов без написания исходного кода.</span><span class="sxs-lookup"><span data-stu-id="3a07d-109">Empower functional users to record business tasks by using Task recorder, and then convert the task recordings into a suite of automated tests, without having to write source code.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="3a07d-110">Перед началом</span><span class="sxs-lookup"><span data-stu-id="3a07d-110">Before you begin</span></span>

### <a name="prerequisites"></a><span data-ttu-id="3a07d-111">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="3a07d-111">Prerequisites</span></span>

- <span data-ttu-id="3a07d-112">Среда, в которой выполняется Microsoft Dynamics 365 for Finance and Operations версии 10.0 (апрель 2019) или более поздняя, необходима для работы с этим учебником.</span><span class="sxs-lookup"><span data-stu-id="3a07d-112">An environment that runs Microsoft Dynamics 365 for Finance and Operations version 10.0 (April 2019) or later is required for this tutorial.</span></span> <span data-ttu-id="3a07d-113">Для клиентов, использующих Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3, также поддерживается обновление платформы Platform update 20 (PU20) или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="3a07d-113">For customers who are using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3, Platform update 20 (PU20) or later is also supported.</span></span>
- <span data-ttu-id="3a07d-114">Пользователь должен иметь права администратора для этой среды.</span><span class="sxs-lookup"><span data-stu-id="3a07d-114">The user must have admin rights to the environment.</span></span>
- <span data-ttu-id="3a07d-115">Необходимо иметь доступ к службам LCS арендатора клиента и к Azure DevOps (ранее известной как Microsoft Visual Studio Team Services \[VSTS\]).</span><span class="sxs-lookup"><span data-stu-id="3a07d-115">You must have access to the customer tenant LCS and Azure DevOps (previously known as Microsoft Visual Studio Team Services \[VSTS\]).</span></span>
- <span data-ttu-id="3a07d-116">Пользователь, который создает наборы тестов и управляет ими, должен иметь лицензию Azure DevOps Test Plans (планы испытаний) или Test Manager (менеджер испытаний).</span><span class="sxs-lookup"><span data-stu-id="3a07d-116">The user that is creating and managing tests suites must have an Azure DevOps Test Plans or Test Manager license.</span></span> <span data-ttu-id="3a07d-117">Следующие лицензии также дают доступ к планам испытаний:</span><span class="sxs-lookup"><span data-stu-id="3a07d-117">The following licenses will also give you access to Test Plans:</span></span>
    - <span data-ttu-id="3a07d-118">Лицензия Visual Studio Enterprise</span><span class="sxs-lookup"><span data-stu-id="3a07d-118">Visual Studio Enterprise license</span></span>
    - <span data-ttu-id="3a07d-119">Лицензия Visual Studio Test Professional</span><span class="sxs-lookup"><span data-stu-id="3a07d-119">Visual Studio Test Professional license</span></span>
    - <span data-ttu-id="3a07d-120">Лицензия подписчика на платформы MSDN</span><span class="sxs-lookup"><span data-stu-id="3a07d-120">MSDN Platforms subscriber license</span></span>
- <span data-ttu-id="3a07d-121">RSAT должен иметь доступ к тестовой среде через веб-браузер.</span><span class="sxs-lookup"><span data-stu-id="3a07d-121">RSAT must have access to the test environment via a web browser.</span></span>
- <span data-ttu-id="3a07d-122">Для создания и изменения параметров тестирования необходимо установить Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="3a07d-122">To generate and edit test parameters, you must have Microsoft Excel installed.</span></span>

## <a name="configure-azure-devops"></a><span data-ttu-id="3a07d-123">Настроить Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="3a07d-123">Configure Azure DevOps</span></span>

### <a name="user-eligibility"></a><span data-ttu-id="3a07d-124">Приемлемость пользователей</span><span class="sxs-lookup"><span data-stu-id="3a07d-124">User eligibility</span></span>

<span data-ttu-id="3a07d-125">Убедитесь, что пользователь создан в Azure DevOps и имеет уровень подписки, обеспечивающий доступ к планам испытаний Azure Test Plans.</span><span class="sxs-lookup"><span data-stu-id="3a07d-125">Make sure that the user is created in Azure DevOps and has a subscription level that provides access to Azure Test Plans.</span></span> <span data-ttu-id="3a07d-126">Лицензия Azure DevOps Test Plans требуется только в том случае, если пользователь создает тестовые случаи и управляет ими (то есть, не все пользователи RSAT нуждаются в этой лицензии).</span><span class="sxs-lookup"><span data-stu-id="3a07d-126">An Azure DevOps Test Plans license is required only if the user will create and manage test cases (that is, not all RSAT users require this license).</span></span> <span data-ttu-id="3a07d-127">Сведения о требованиях к лицензии см. в разделе [Требования к лицензии](/azure/devops/test/manual-test-permissions#license-requirements).</span><span class="sxs-lookup"><span data-stu-id="3a07d-127">For information about the license requirements, see [License requirements](/azure/devops/test/manual-test-permissions#license-requirements).</span></span>

### <a name="create-a-new-azure-devops-project"></a><span data-ttu-id="3a07d-128">Создание нового проекта Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="3a07d-128">Create a new Azure DevOps project</span></span>

<span data-ttu-id="3a07d-129">RSAT использует Azure DevOps для управления тестовыми случаями и наборами тестов, создания отчетов и изучения результатов тестов.</span><span class="sxs-lookup"><span data-stu-id="3a07d-129">RSAT uses Azure Devops for test case and test suite management, reporting, and investigating test run results.</span></span>

> [!NOTE]
> <span data-ttu-id="3a07d-130">Можно использовать существующий проект Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="3a07d-130">You can use an existing Azure DevOps project.</span></span> <span data-ttu-id="3a07d-131">Однако если существующий проект Azure DevOps настроен таким образом, что он имеет пользовательский шаблон, то при синхронизации тестовых случаев из средства моделирования бизнес-процессов (BPM) с Azure DevOps будет выдаваться сообщение об ошибке "Ошибка синхронизации VSTS" (см. раздел [Тест синхронизации из BPM в Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops)).</span><span class="sxs-lookup"><span data-stu-id="3a07d-131">However, if your existing Azure DevOps project is set up so that it has a custom template, you will receive a "VSTS Sync Failure" error when you sync test cases from Business process modeler (BPM) to Azure DevOps (see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section).</span></span> <span data-ttu-id="3a07d-132">Если выполнены следующие рекомендации для пользовательского шаблона, можно будет синхронизировать тестовые случаи с Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="3a07d-132">If the following best practices have been followed for the custom template, you will be able to sync the test cases to Azure DevOps.</span></span> <span data-ttu-id="3a07d-133">(Рекомендации приведены в сообщении об ошибке.)</span><span class="sxs-lookup"><span data-stu-id="3a07d-133">(These best practices are listed in the error message.)</span></span>

- <span data-ttu-id="3a07d-134">Не удалять типы рабочих элементов или готовые поля.</span><span class="sxs-lookup"><span data-stu-id="3a07d-134">Do not delete any work item types or out-of-the-box fields.</span></span>
- <span data-ttu-id="3a07d-135">Не удалять состояния типа рабочего элемента.</span><span class="sxs-lookup"><span data-stu-id="3a07d-135">Do not delete any state of a work item type.</span></span>
- <span data-ttu-id="3a07d-136">Не добавлять обязательные поля в тип рабочего элемента.</span><span class="sxs-lookup"><span data-stu-id="3a07d-136">Do not add any required fields to a work item type.</span></span>

![Сообщение об ошибке со списком рекомендаций](./media/setup_rsa_tool_02.png)

<span data-ttu-id="3a07d-138">В противном случае в этом учебнике рекомендуется создать новый проект Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="3a07d-138">Otherwise, for this tutorial, we recommend that you create a new Azure DevOps project.</span></span> <span data-ttu-id="3a07d-139">Дополнительные сведения см. в разделе [Вопросы, связанные с синхронизацией с BPM с помощью специального шаблона процесса Azure DevOps (VSTS)](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).</span><span class="sxs-lookup"><span data-stu-id="3a07d-139">For more information, see [Issues when syncing to BPM using a custom Azure DevOps (VSTS) process template](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).</span></span>

1. <span data-ttu-id="3a07d-140">Откройте URL-адрес Azure DevOps (`https://dev.azure.com/<Azure DevOps Name>`).</span><span class="sxs-lookup"><span data-stu-id="3a07d-140">Open the Azure DevOps URL (`https://dev.azure.com/<Azure DevOps Name>`).</span></span>
2. <span data-ttu-id="3a07d-141">Выберите **Создать проект** в верхнем правом углу страницы Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="3a07d-141">Select **Create project** in the upper-right corner of the Azure DevOps page.</span></span>

    ![Кнопка создания проекта](./media/setup_rsa_tool_03.png)

3. <span data-ttu-id="3a07d-143">Заполните следующие поля, затем выберите **Создать**:</span><span class="sxs-lookup"><span data-stu-id="3a07d-143">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="3a07d-144">**Наименование проекта**</span><span class="sxs-lookup"><span data-stu-id="3a07d-144">**Project name**</span></span>
    - <span data-ttu-id="3a07d-145">**Управление версиями** — выберите **Управление версиями Team Foundation**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-145">**Version control** – Select **Team Foundation Version Control**.</span></span> <span data-ttu-id="3a07d-146">Обратите внимание, что параметр по умолчанию **Git** не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3a07d-146">Note that the default option, **Git**, isn't supported.</span></span>
    - <span data-ttu-id="3a07d-147">**Процесс рабочего элемента**</span><span class="sxs-lookup"><span data-stu-id="3a07d-147">**Work item process**</span></span>

    ![Диалоговое окно создания нового проекта](./media/setup_rsa_tool_04.png)

### <a name="create-a-personal-access-token"></a><span data-ttu-id="3a07d-149">Создание личного маркера доступа</span><span class="sxs-lookup"><span data-stu-id="3a07d-149">Create a personal access token</span></span>

<span data-ttu-id="3a07d-150">В этом учебнике будет использоваться средство моделирования бизнес-процессов (BPM) LCS, чтобы создать библиотеку тестовых случаев и синхронизировать тестовые случаи с Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="3a07d-150">In this tutorial, you will use the LCS Business Process Modeler (BPM) to create a test case library and synchronize your test cases with Azure DevOps.</span></span> <span data-ttu-id="3a07d-151">Вам понадобится личный маркер доступа для синхронизации BPM с Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="3a07d-151">You will need a personal access token to sync BPM with Azure DevOps.</span></span>

1. <span data-ttu-id="3a07d-152">Выберите значок профиля в верхнем правом углу страницы для своего проекта Azure DevOps, затем выберите **Безопасность**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-152">Select the profile icon in the upper-right corner of the page for your Azure DevOps project, and then select **Security**.</span></span>

    ![Команда безопасности](./media/setup_rsa_tool_05.png)

2. <span data-ttu-id="3a07d-154">В левой области в разделе **Безопасность** выберите **Личные маркеры доступа**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-154">In the left pane, under **Security**, select **Personal access tokens**.</span></span> <span data-ttu-id="3a07d-155">Затем выберите **Создать маркер**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-155">Then select **New Token**.</span></span>

    ![Кнопка "Создать маркер" на вкладке "Личные маркеры доступа" в разделе "Параметры пользователя"](./media/setup_rsa_tool_06.png)

3. <span data-ttu-id="3a07d-157">Заполните следующие поля, затем выберите **Создать**:</span><span class="sxs-lookup"><span data-stu-id="3a07d-157">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="3a07d-158">**Название**</span><span class="sxs-lookup"><span data-stu-id="3a07d-158">**Name**</span></span>
    - <span data-ttu-id="3a07d-159">**Окончание срока действия (UTC)** — выберите **Определяемый пользователем**, затем с помощью средства выбора даты выберите последнюю доступную дату.</span><span class="sxs-lookup"><span data-stu-id="3a07d-159">**Expiration (UTC)** – Select **Custom defined**, and then use the date picker to select the last available date.</span></span>
    - <span data-ttu-id="3a07d-160">**Области** — выберите параметр **Полный доступ**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-160">**Scopes** – Select the **Full access** option.</span></span>

    ![Диалоговое окно создания нового личного маркера доступа](./media/setup_rsa_tool_07.png)

    > [!NOTE]
    > <span data-ttu-id="3a07d-162">Запишите созданный личный маркер доступа.</span><span class="sxs-lookup"><span data-stu-id="3a07d-162">Make a note of the personal access token that is created.</span></span> <span data-ttu-id="3a07d-163">Он потребуется позже при настройке конфигурации RSAT.</span><span class="sxs-lookup"><span data-stu-id="3a07d-163">You will need it later when you set up the RSAT configuration.</span></span>

    ![Личный маркер доступа](./media/setup_rsa_tool_08.png)

## <a name="configure-the-lcs-project"></a><span data-ttu-id="3a07d-165">Настройка проекта LCS</span><span class="sxs-lookup"><span data-stu-id="3a07d-165">Configure the LCS project</span></span>

<span data-ttu-id="3a07d-166">Для основной библиотеки тестов необходим проект Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="3a07d-166">You need a Lifecycle Services (LCS) project for your master test library.</span></span> <span data-ttu-id="3a07d-167">Средство моделирования бизнес-процессов (BPM) LCS используется в качестве основной библиотеки для тестовых случаев.</span><span class="sxs-lookup"><span data-stu-id="3a07d-167">The LCS Business Process Modeler (BPM) is used as the master library for your test cases.</span></span> <span data-ttu-id="3a07d-168">BPM используется для управления и распространения библиотек тестирования в проектах LCS.</span><span class="sxs-lookup"><span data-stu-id="3a07d-168">BPM is used to manage and distribute test libraries across LCS projects.</span></span> <span data-ttu-id="3a07d-169">Например, партнер Майкрософт или независимый поставщик программных продуктов (ISV), создающие библиотеки тестов, выпускают тестовые случаи в форме библиотек BPM.</span><span class="sxs-lookup"><span data-stu-id="3a07d-169">For example, a Microsoft partner or independent software vendor (ISV) building test libraries will release test cases in the form of BPM libraries.</span></span> <span data-ttu-id="3a07d-170">В BPM тестовые случаи организованы по бизнес-процессам.</span><span class="sxs-lookup"><span data-stu-id="3a07d-170">In BPM, test cases are organized by business process.</span></span> <span data-ttu-id="3a07d-171">BPM не определяет порядок выполнения или частоту проходов теста.</span><span class="sxs-lookup"><span data-stu-id="3a07d-171">BPM doesn't define the execution order or frequency of your test pass.</span></span> <span data-ttu-id="3a07d-172">Эти сведения контролируются в Azure DevOps, как описано ниже в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="3a07d-172">These details are managed in Azure DevOps, as described later in this topic.</span></span>  

<span data-ttu-id="3a07d-173">Для проекта LCS можно использовать существующую пользовательскую реализацию или проект партнера.</span><span class="sxs-lookup"><span data-stu-id="3a07d-173">For your LCS project, you can use an existing customer implementation or partner project.</span></span>

### <a name="update-the-lcs-language"></a><span data-ttu-id="3a07d-174">Обновление языка LCS</span><span class="sxs-lookup"><span data-stu-id="3a07d-174">Update the LCS language</span></span>

> [!NOTE]
> <span data-ttu-id="3a07d-175">Для правильного отображения бизнес-процессов в пользовательском интерфейсе должен быть установлен предпочитаемый язык LCS **Английский (США)**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-175">For the user interface (UI) to correctly show business processes, the LCS preferred language must be set to **English (United States)**.</span></span>

1. <span data-ttu-id="3a07d-176">Перейдите в проект реализации LCS.</span><span class="sxs-lookup"><span data-stu-id="3a07d-176">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="3a07d-177">Выберите кнопку **Параметры** (символ шестеренки) в верхнем правом углу, затем выберите **Предпочитаемый язык**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-177">Select the **Settings** button (the gear symbol) in the upper-right corner, and then select **Language preference**.</span></span>

    ![Обновление предпочтительного языка](./media/setup_rsa_tool_09.png)

3. <span data-ttu-id="3a07d-179">В поле **Предпочтительный язык** выберите **Английский (США)**, затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-179">In the **Preferred language** field, select **English (United States)**, and then select **Save**.</span></span>

    ![Вкладка "Предпочитаемый язык" в параметрах пользователя](./media/setup_rsa_tool_10.png)

### <a name="configure-lcs-to-connect-to-the-azure-devops-project"></a><span data-ttu-id="3a07d-181">Настройка LCS для подключения к проекту Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="3a07d-181">Configure LCS to connect to the Azure DevOps project</span></span>

<span data-ttu-id="3a07d-182">Если ранее был создан новый проект Azure DevOps, настройте проект LCS для подключения к нему.</span><span class="sxs-lookup"><span data-stu-id="3a07d-182">If you created a new Azure DevOps project earlier, configure the LCS project to connect to it.</span></span> <span data-ttu-id="3a07d-183">В противном случае, если проект LCS уже подключен к проекту Azure DevOps, можно перейти к следующему разделу.</span><span class="sxs-lookup"><span data-stu-id="3a07d-183">Otherwise, if your LCS project is already connected to your Azure DevOps project, you can continue to the next section.</span></span>

1. <span data-ttu-id="3a07d-184">Перейдите в проект реализации LCS.</span><span class="sxs-lookup"><span data-stu-id="3a07d-184">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="3a07d-185">Выберите кнопку **Меню**, затем выберите **Параметры проекта**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-185">Select the **Menu** button, and then select **Project settings**.</span></span>

    ![Команда "Параметры проекта"](./media/setup_rsa_tool_11.png)

3. <span data-ttu-id="3a07d-187">В левой области выберите **Visual Studio Team Services**, затем выберите пункт **Настройка Visual Studio Team Services**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-187">In the left pane, select **Visual Studio Team Services**, and then select **Setup Visual Studio Team Services**.</span></span>

    ![Вкладка Visual Studio Team Services в параметрах проекта](./media/setup_rsa_tool_12.png)

4. <span data-ttu-id="3a07d-189">В поле **URL-адрес сайта Azure DevOps** введите URL-адрес сайта Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="3a07d-189">In the **Azure DevOps site URL** field, enter the URL of the Azure DevOps site.</span></span> <span data-ttu-id="3a07d-190">В поле **Личный маркер доступа** введите личный маркер доступа, созданный ранее.</span><span class="sxs-lookup"><span data-stu-id="3a07d-190">In the **Personal access token** field, enter the personal access token that was created earlier.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3a07d-191">Несмотря на то, что VSTS не известен как Azure DevOps, для подключения LCS к проекту Azure DevOps используется старый URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="3a07d-191">Although VSTS is now known as Azure DevOps, to connect LCS to your Azure DevOps project, use the old URL.</span></span> <span data-ttu-id="3a07d-192">Например, URL-адрес Azure DevOps, используемый в этом учебнике, — это `https://dev.azure.com/D365FOFastTrack/`.</span><span class="sxs-lookup"><span data-stu-id="3a07d-192">For example, the Azure DevOps URL that is used in this tutorial is `https://dev.azure.com/D365FOFastTrack/`.</span></span> <span data-ttu-id="3a07d-193">Однако на следующем рисунке он вводится как `https://D365FOFastTrack.visualstudio.com/`.</span><span class="sxs-lookup"><span data-stu-id="3a07d-193">However, in the following illustration, it's entered as `https://D365FOFastTrack.visualstudio.com/`.</span></span>

    ![Шаг 1 в настройке Visual Studio Team Services](./media/setup_rsa_tool_13.png)

5. <span data-ttu-id="3a07d-195">Выберите **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-195">Select **Continue**.</span></span>
6. <span data-ttu-id="3a07d-196">В поле **Проект Visual Studio Team Services** выберите проект VSTS на выбранном сайте, чтобы связать с проектом LCS.</span><span class="sxs-lookup"><span data-stu-id="3a07d-196">In the **Visual Studio Team Services project** field, select the VSTS project on the selected site to link with the LCS project.</span></span> <span data-ttu-id="3a07d-197">По умолчанию для поля **Шаблон процесса** установлено значение **Гибкость**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-197">The **Process template** field is set to **Agile** by default.</span></span> <span data-ttu-id="3a07d-198">Для пользовательского шаблона следует ознакомиться с практическим руководством в разделе [Создание нового проекта Azure DevOps](#create-a-new-azure-devops-project).</span><span class="sxs-lookup"><span data-stu-id="3a07d-198">For a custom template, review the best practice guidance in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span> <span data-ttu-id="3a07d-199">Затем выберите **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-199">Then select **Continue**.</span></span>

    ![Шаг 2 в настройке Visual Studio Team Services](./media/setup_rsa_tool_14.png)

7. <span data-ttu-id="3a07d-201">Проверьте настройки, затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-201">Review your settings, and then select **Save**.</span></span>

    ![Шаг 3 в настройке Visual Studio Team Services](./media/setup_rsa_tool_15.png)

8. <span data-ttu-id="3a07d-203">Выберите **Авторизовать** для авторизации LCS для доступа к настроенному сайту Azure DevOps от вашего имени и включения функций, которые интегрируются с VSTS.</span><span class="sxs-lookup"><span data-stu-id="3a07d-203">Select **Authorize** to authorize LCS to access the configured Azure DevOps site on your behalf and to turn on features that integrate with VSTS.</span></span>

    ![Кнопка "Авторизовать"](./media/setup_rsa_tool_16.png)

9. <span data-ttu-id="3a07d-205">Открывается окно с сообщением "Вы будете перенаправлены на внешний сайт для авторизации LCS на подключение к Visual Studio Team Services от вашего имени.</span><span class="sxs-lookup"><span data-stu-id="3a07d-205">A message box appears that states, "You are about to be redirected to an eternal site to authorize LCS to connect to Visual Studio Team Services on your behalf.</span></span> <span data-ttu-id="3a07d-206">Продолжить?"</span><span class="sxs-lookup"><span data-stu-id="3a07d-206">Proceed?"</span></span> <span data-ttu-id="3a07d-207">Выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-207">Select **Yes**.</span></span>

    ![Окно сообщения](./media/setup_rsa_tool_17.png)

10. <span data-ttu-id="3a07d-209">Выберите **Принять**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-209">Select **Accept**.</span></span>

    ![Авторизация доступа](./media/setup_rsa_tool_18.png)

11. <span data-ttu-id="3a07d-211">Если вы уполномочены как пользователь, пользовательский интерфейс должен вернуться на страницу параметров проекта LCS.</span><span class="sxs-lookup"><span data-stu-id="3a07d-211">If you're authorized as a user, the UI should you return to the LCS project settings page.</span></span>

    ![Авторизованный пользователь](./media/setup_rsa_tool_19.png)

### <a name="create-a-new-bpm-library"></a><span data-ttu-id="3a07d-213">Создание новой библиотеки BPM</span><span class="sxs-lookup"><span data-stu-id="3a07d-213">Create a new BPM library</span></span>

1. <span data-ttu-id="3a07d-214">Перейдите в проект реализации LCS.</span><span class="sxs-lookup"><span data-stu-id="3a07d-214">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="3a07d-215">Выберите кнопку **Меню**, затем выберите **Средство моделирования бизнес-процессов**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-215">Select the **Menu** button, and then select **Business process modeler**.</span></span>

    ![Команда средства моделирования бизнес-процессов](./media/setup_rsa_tool_20.png)

3. <span data-ttu-id="3a07d-217">Выберите **Создать библиотеку**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-217">Select **New library**.</span></span>

    ![Кнопка "Создать библиотеку"](./media/setup_rsa_tool_21.png)

4. <span data-ttu-id="3a07d-219">В поле **Имя библиотеки** введите имя, затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-219">In the **Library name** field, enter a name, and then select **Create**.</span></span> <span data-ttu-id="3a07d-220">Для данного учебника назовите библиотеку BPM **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-220">For this tutorial, name the BPM library **RSAT**.</span></span>

    ![Диалоговое окно создания новой библиотеки](./media/setup_rsa_tool_22.png)

5. <span data-ttu-id="3a07d-222">Откройте новую библиотеку BPM **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-222">Open the new **RSAT** BPM library.</span></span>
6. <span data-ttu-id="3a07d-223">Выберите процесс **Образец основного бизнес-процесса**, затем в правой части выберите **Режим редактирования**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-223">Select the **Sample Core Business Process** process, and then, on the right, select **Edit mode**.</span></span>

    ![Кнопка "Режим редактирования"](./media/setup_rsa_tool_23.png)

7. <span data-ttu-id="3a07d-225">Измените значение обоих полей **Имя** и **Описание** на **Создать продукт**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-225">Change the value of both the **Name** field and the **Description** field to **Create a product**.</span></span> <span data-ttu-id="3a07d-226">Затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-226">Then select **Save**.</span></span>

    ![Поля имени и описания](./media/setup_rsa_tool_24.png)

## <a name="environment"></a><span data-ttu-id="3a07d-228">Окружение</span><span class="sxs-lookup"><span data-stu-id="3a07d-228">Environment</span></span>

### <a name="version-requirement"></a><span data-ttu-id="3a07d-229">Требования к версии</span><span class="sxs-lookup"><span data-stu-id="3a07d-229">Version requirement</span></span>

<span data-ttu-id="3a07d-230">Требуется тестовая среда или среда песочницы, в которой работает версия 10.</span><span class="sxs-lookup"><span data-stu-id="3a07d-230">A test or sandbox environment that runs version 10 is required.</span></span> <span data-ttu-id="3a07d-231">Для клиентов, использующих версию 7.3, также поддерживается обновление платформы Platform update 20 или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="3a07d-231">For customers that are using version 7.3, Platform update 20 or later is also supported.</span></span>

> [!NOTE]
> <span data-ttu-id="3a07d-232">RSAT должен иметь доступ к вашей тестовой среде через веб-браузер.</span><span class="sxs-lookup"><span data-stu-id="3a07d-232">RSAT must have access to your test environment via a web browser.</span></span>

### <a name="user-criteria"></a><span data-ttu-id="3a07d-233">Критерии пользователя</span><span class="sxs-lookup"><span data-stu-id="3a07d-233">User criteria</span></span>

<span data-ttu-id="3a07d-234">Пользователь должен иметь права администратора для этой среды.</span><span class="sxs-lookup"><span data-stu-id="3a07d-234">The user must have admin rights to this environment.</span></span>

### <a name="set-up-help-settings-to-connect-with-lcs"></a><span data-ttu-id="3a07d-235">Настройка параметров справки для подключения к LCS</span><span class="sxs-lookup"><span data-stu-id="3a07d-235">Set up Help settings to connect with LCS</span></span>

<span data-ttu-id="3a07d-236">Этот шаг требуется для подключения к LCS, чтобы записи задач можно было сохранить в соответствующую библиотеку BPM в LCS через клиент.</span><span class="sxs-lookup"><span data-stu-id="3a07d-236">This step is required in order to connect with LCS so that task recordings can be saved to the appropriate BPM library in LCS through the client.</span></span>

1. <span data-ttu-id="3a07d-237">Откройте клиент.</span><span class="sxs-lookup"><span data-stu-id="3a07d-237">Open the client.</span></span>
2. <span data-ttu-id="3a07d-238">Перейдите в раздел **Администрирование системы \> Настройка \> Параметры системы**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-238">Go to **System Administration \> Setup \> System parameters**.</span></span>
3. <span data-ttu-id="3a07d-239">На вкладке **Справка** в поле **Настройка справки Lifecycle Services** выберите соответствующий проект LCS (**RSAT** для этого учебника).</span><span class="sxs-lookup"><span data-stu-id="3a07d-239">On the **Help** tab, in the **Lifecycle Services help configuration** field, select the relevant LCS project (**RSAT** for this tutorial).</span></span>

    ![Поле настройки справки Lifecycle Services на вкладке "Справка"](./media/setup_rsa_tool_25.png)

    <span data-ttu-id="3a07d-241">Библиотеки BPM заполняются в соответствующем проекте LCS.</span><span class="sxs-lookup"><span data-stu-id="3a07d-241">BPM libraries are filled in under the appropriate LCS project.</span></span>

4. <span data-ttu-id="3a07d-242">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-242">Select **Save**.</span></span>
5. <span data-ttu-id="3a07d-243">Возможно потребуется обновить браузер, чтобы увидеть обновленное содержимое справки.</span><span class="sxs-lookup"><span data-stu-id="3a07d-243">You might have to refresh the browser to see the updated Help content.</span></span>

    ![Уведомление об обновлении браузера](./media/setup_rsa_tool_26.png)

## <a name="task-recordings"></a><span data-ttu-id="3a07d-245">Запись задач</span><span class="sxs-lookup"><span data-stu-id="3a07d-245">Task recordings</span></span>

> [!NOTE]
> <span data-ttu-id="3a07d-246">Убедитесь, что все записи задач начинаются с главной панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="3a07d-246">Make sure that all your task recordings start on the main dashboard.</span></span> <span data-ttu-id="3a07d-247">Старайтесь, чтобы отдельные записи были короткими, и сосредоточьтесь на деловой задаче, например на создании заказа на продажу.</span><span class="sxs-lookup"><span data-stu-id="3a07d-247">Keep individual recordings short, and focus on one business task, such as creating a sales order.</span></span>

### <a name="create-a-task-recording-and-save-it-to-the-bpm-library"></a><span data-ttu-id="3a07d-248">Создание записи задачи и сохранение ее в библиотеке BPM</span><span class="sxs-lookup"><span data-stu-id="3a07d-248">Create a task recording and save it to the BPM library</span></span>

<span data-ttu-id="3a07d-249">Создайте соответствующую запись задачи, которую можно приложить к простому бизнес-процессу, созданному в новой библиотеке BPM.</span><span class="sxs-lookup"><span data-stu-id="3a07d-249">Create a corresponding task recording that you can attach to the simple business process that was created in the new BPM library.</span></span>

1. <span data-ttu-id="3a07d-250">Откройте клиент.</span><span class="sxs-lookup"><span data-stu-id="3a07d-250">Open the client.</span></span>
2. <span data-ttu-id="3a07d-251">На главной панели мониторинга выберите кнопку **Настройки** (символ шестеренки), затем выберите **Регистратор задач**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-251">On the main dashboard, select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>

    ![Выберите регистратор задач в меню настройки](./media/setup_rsa_tool_27.png)

3. <span data-ttu-id="3a07d-253">Выберите **Создать запись**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-253">Select **Create recording**.</span></span>

    ![Кнопка "Создать запись"](./media/setup_rsa_tool_28.png)

4. <span data-ttu-id="3a07d-255">Заполните поля **Имя записи** и **Описание записи**, затем выберите **Начать**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-255">Fill in the **Recording name** and **Recording description** fields, and then select **Start**.</span></span>

    ![Поля "Имя записи" и "Описание записи"](./media/setup_rsa_tool_29.png)

5. <span data-ttu-id="3a07d-257">Запишите шаги по созданию продукта.</span><span class="sxs-lookup"><span data-stu-id="3a07d-257">Record the steps for creating a product.</span></span> <span data-ttu-id="3a07d-258">По завершении нажмите кнопку **Остановить**, чтобы остановить запись.</span><span class="sxs-lookup"><span data-stu-id="3a07d-258">When you've finished, select **Stop** to stop recording.</span></span>

    ![Шаги для создания продукта](./media/setup_rsa_tool_30.png)

6. <span data-ttu-id="3a07d-260">Выберите **Сохраните файл в Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-260">Select **Save to Lifecycle Services**.</span></span>

    ![Сохранение записи задачи в Lifecycle Services](./media/setup_rsa_tool_31.png)

    <span data-ttu-id="3a07d-262">Сведения о библиотеке загружаются из LCS.</span><span class="sxs-lookup"><span data-stu-id="3a07d-262">Library information is loaded from LCS.</span></span>

    ![Загрузка информации о библиотеке](./media/setup_rsa_tool_32.png)

7. <span data-ttu-id="3a07d-264">Выберите библиотеку BPM, с которой требуется связать запись задачи.</span><span class="sxs-lookup"><span data-stu-id="3a07d-264">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="3a07d-265">В данном учебнике выберите библиотеку BPM **RSAT**, созданную ранее, и бизнес -процесс **Создание продукта** в ней.</span><span class="sxs-lookup"><span data-stu-id="3a07d-265">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Create a product** business process under it.</span></span> <span data-ttu-id="3a07d-266">Затем выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-266">Then select **OK**.</span></span>

    ![Связывание записи задачи с библиотекой BPM и бизнес-процессом](./media/setup_rsa_tool_33.png)

    <span data-ttu-id="3a07d-268">Появляется сообщение "Сохранение в Lifecycle Services выполнено успешно".</span><span class="sxs-lookup"><span data-stu-id="3a07d-268">A "Saving to Lifecycle Services was successful" message appears.</span></span>

    ![Сообщение об успешном сохранении в LCS](./media/setup_rsa_tool_34.png)

8. <span data-ttu-id="3a07d-270">Если требуется сохранить запись задачи локально, а затем отправить ее в BPM через LCS, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="3a07d-270">If you want to save the task recording locally and then upload it to BPM through LCS, follow these steps:</span></span>

    1. <span data-ttu-id="3a07d-271">После завершения записи выберите **Сохранить на этом компьютере**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-271">After the recording is completed, select **Save to this PC**.</span></span>

        ![Сохранить на этот компьютер](./media/setup_rsa_tool_35.png)

    2. <span data-ttu-id="3a07d-273">В панели уведомлений браузера выберите **Сохранить** или **Сохранить как**, чтобы сохранить файл на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="3a07d-273">In the browser's Notification bar, select **Save** or **Save As** to save the file on your local computer.</span></span>

        ![Панель уведомлений](./media/setup_rsa_tool_36.png)

    3. <span data-ttu-id="3a07d-275">Перейдите в библиотеку BPM **RSAT** и выберите бизнес-процесс, для которого необходимо сохранить запись задачи.</span><span class="sxs-lookup"><span data-stu-id="3a07d-275">Go to the **RSAT** BPM library, and select the business process to save the task recording against.</span></span>
    4. <span data-ttu-id="3a07d-276">На вкладке **Обзор** выберите **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-276">On the **Overview** tab, select **Upload**.</span></span>

        ![Кнопка отправки](./media/setup_rsa_tool_37.png)

    5. <span data-ttu-id="3a07d-278">Выберите **Обзор** и выберите сохраненный ранее файл .axtr.</span><span class="sxs-lookup"><span data-stu-id="3a07d-278">Select **Browse**, and select the .axtr file that you saved earlier.</span></span> <span data-ttu-id="3a07d-279">Затем выберите **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-279">Then select **Upload**.</span></span>

        ![Выбор файла .axtr для отправки](./media/setup_rsa_tool_38.png)

### <a name="test-the-synchronization-from-bpm-to-azure-devops"></a><span data-ttu-id="3a07d-281">Проверка синхронизации из BPM в Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="3a07d-281">Test the synchronization from BPM to Azure DevOps</span></span>

<span data-ttu-id="3a07d-282">Теперь, когда запись задачи связана с бизнес-процессом, необходимо проверить, что бизнес-процесс и связанная с ним запись задачи могут быть синхронизированы Azure DevOps в качестве функции и тестового случая (соответственно) с помощью функции синхронизации VSTS в LCS.</span><span class="sxs-lookup"><span data-stu-id="3a07d-282">Now that a task recording is attached to the business process, you must validate that the business process and the associated task recording can be synced to Azure DevOps as a feature and a test case (respectively) by using the VSTS sync feature in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="3a07d-283">Соответствующий тип рабочего элемента, созданный в Azure DevOps, будет изменяться в зависимости от шаблона процесса, выбранного при настройке проекта LCS с помощью Azure DevOps, как описано в разделе [Создание нового проекта Azure DevOps](#create-a-new-azure-devops-project).</span><span class="sxs-lookup"><span data-stu-id="3a07d-283">The corresponding work item type that is created in Azure DevOps will vary, depending on the process template that you selected when you configured the LCS project with Azure DevOps, as described in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span>

1. <span data-ttu-id="3a07d-284">Перейдите к библиотеке BPM и откройте созданную ранее библиотеку **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-284">Go to the BPM library, and open the **RSAT** library that you created earlier.</span></span>
2. <span data-ttu-id="3a07d-285">Нажмите кнопку с многоточием (**...**) и выберите **Синхронизация VSTS**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-285">Select the ellipsis button (**...**), and select **VSTS sync**.</span></span>

    ![Команда синхронизации VSTS в меню с многоточием](./media/setup_rsa_tool_39.png)

    <span data-ttu-id="3a07d-287">После завершения синхронизации VSTS в левой части отображается вкладка **Требования**, содержащая соответствующий рабочий элемент Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="3a07d-287">After VSTS sync is completed, a **Requirements** tab appears on the left side and includes the corresponding Azure DevOps work item.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3a07d-288">Созданный в Azure DevOps рабочий элемент будет иметь имя "Библиотека BPM" в качестве префикса заголовка.</span><span class="sxs-lookup"><span data-stu-id="3a07d-288">The work item that is created in Azure DevOps will have the BPM library name as the title prefix.</span></span>

    ![Вкладка требований](./media/setup_rsa_tool_40.png)

3. <span data-ttu-id="3a07d-290">Обновите страницу.</span><span class="sxs-lookup"><span data-stu-id="3a07d-290">Refresh the page.</span></span>
4. <span data-ttu-id="3a07d-291">Выберите кнопку с многоточием (**...**). Будет отображен дополнительный параметр **Синхронизировать тестовые случаи**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-291">Select the ellipsis button (**...**). You will see an additional option, **Sync test cases**.</span></span> <span data-ttu-id="3a07d-292">Выберите этот параметр.</span><span class="sxs-lookup"><span data-stu-id="3a07d-292">Select this option.</span></span>

    ![Команда синхронизации тестовых случаев в меню с многоточием](./media/setup_rsa_tool_41.png)

    > [!NOTE]
    > <span data-ttu-id="3a07d-294">Если параметр **Синхронизировать тестовые случаи** недоступен после обновления страницы, перейдите на главную страницу для BPM и выберите **Синхронизировать тестовые случаи** для всей библиотеки.</span><span class="sxs-lookup"><span data-stu-id="3a07d-294">If the **Sync test cases** option isn't available after you refresh the page, go to main page for BPM, and select **Sync test cases** for the whole library itself.</span></span> <span data-ttu-id="3a07d-295">Таким образом можно эффективно принудительно выполнить синхронизацию для всей библиотеки.</span><span class="sxs-lookup"><span data-stu-id="3a07d-295">In this way, you effectively force a synchronization for the whole library.</span></span>
    >
    > ![Выбор синхронизации тестовых случаев для всей библиотеки](./media/setup_rsa_tool_42.png)

    <span data-ttu-id="3a07d-297">После завершения синхронизации тестовых случаев создается новый тестовый случай на вкладке **Требования**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-297">After Sync test cases is completed, a new test case is created on the **Requirements** tab.</span></span>

    ![Новый тестовый случай на вкладке "Требования"](./media/setup_rsa_tool_43.png)

5. <span data-ttu-id="3a07d-299">Перейдите к проекту Azure DevOps и выберите **Панели \> Рабочие элементы**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-299">Go to your Azure DevOps project, and select **Boards \> Work Items**.</span></span>

    ![Команда рабочих элементов в разделе панелей](./media/setup_rsa_tool_44.png)

6. <span data-ttu-id="3a07d-301">Убедитесь, что рабочий элемент и тестовый случай, созданный с помощью синхронизации BPM, существует.</span><span class="sxs-lookup"><span data-stu-id="3a07d-301">Validate that the work item and test case that you created through BPM synchronization exist.</span></span>

    ![Рабочий элемент и тестовый случай](./media/setup_rsa_tool_45.png)

## <a name="install-and-configure-rsat"></a><span data-ttu-id="3a07d-303">Установка и настройка RSAT</span><span class="sxs-lookup"><span data-stu-id="3a07d-303">Install and Configure RSAT</span></span>

<span data-ttu-id="3a07d-304">RSAT можно установить на любой компьютер, на котором работает Windows 10, и который может подключаться к среде с помощью веб-браузера (Internet Explorer или Google Chrome).</span><span class="sxs-lookup"><span data-stu-id="3a07d-304">RSAT can be installed on any computer that runs Windows 10 and that can connect to the environment via a web browser (Internet Explorer or Google Chrome).</span></span>

> [!NOTE]
> <span data-ttu-id="3a07d-305">Перед установкой новой версии средства рекомендуется удалить предыдущую версию.</span><span class="sxs-lookup"><span data-stu-id="3a07d-305">Before you install a new version of the tool, we recommend that you uninstall the previous version.</span></span>

### <a name="install-an-authentication-certificate"></a><span data-ttu-id="3a07d-306">Установка сертификата проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="3a07d-306">Install an authentication certificate</span></span>

<span data-ttu-id="3a07d-307">Чтобы включить проверку подлинности, необходимо создать и установить сертификат на том же компьютере, на котором запущено приложение RSAT.</span><span class="sxs-lookup"><span data-stu-id="3a07d-307">To enable authentication, you must generate and install a certificate on the same computer that RSAT is running on.</span></span>

#### <a name="generate-a-certificate"></a><span data-ttu-id="3a07d-308">Создание сертификата</span><span class="sxs-lookup"><span data-stu-id="3a07d-308">Generate a certificate</span></span>

1. <span data-ttu-id="3a07d-309">Чтобы создать файл сертификата, откройте окно Microsoft Windows PowerShell в качестве администратора и выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="3a07d-309">To generate a certificate file, open a Microsoft Windows PowerShell window as an admin, and run the following command.</span></span>

    ```powershell
    $certificate = New-SelfSignedCertificate -dnsname 127.0.0.1 -CertStoreLocation cert:\LocalMachine\My -FriendlyName "D365 Automated testing certificate" -Provider "Microsoft Strong Cryptographic Provider"
    ```

2. <span data-ttu-id="3a07d-310">Откройте диспетчер сертификатов, введя **certlm.msc** в диалоговом окне **Выполнить** и убедитесь, что сертификат **Сертификат автоматического тестирования D365** был создан в разделе **Личные \> Сертификаты**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-310">Open certificate manager by entering **certlm.msc** in the **Run** dialog box, and confirm that the **D365 Automated testing certificate** certificate is created under **Personal \> Certificates**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3a07d-311">Убедитесь, что введено **certlm.msc**, а не **certmgr.msc**, так как сертификаты хранятся на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="3a07d-311">Be sure to enter **certlm.msc**, not **certmgr.msc**, because the certificates are stored on the local computer.</span></span>

    ![Сертификат автоматического тестирования D365](./media/setup_rsa_tool_46.png)

3. <span data-ttu-id="3a07d-313">Щелкните сертификат правой кнопкой мыши, затем выберите **Копировать**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-313">Right-click the certificate, and then select **Copy**.</span></span>
4. <span data-ttu-id="3a07d-314">Перейдите в раздел **Доверенные корневые центры сертификации \> Сертификаты**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-314">Go to **Trusted Root Certification Authorities \> Certificates**.</span></span>

    ![Папка "Сертификаты" в папке "Доверенные корневые центры сертификации"](./media/setup_rsa_tool_47.png)

5. <span data-ttu-id="3a07d-316">В меню **Действие** выберите команду **Вставить**, чтобы скопировать сертификат в расположение **Доверенные корневые центры сертификации**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-316">On the **Action** menu, select **Paste** to copy the certificate to the **Trusted Root Certification Authorities** location.</span></span>

    ![Команда вставки в меню действий](./media/setup_rsa_tool_48.png)

6. <span data-ttu-id="3a07d-318">Чтобы получить отпечаток установленного сертификата, но без пробелов и специальных символов, откройте окно Windows PowerShell в качестве администратора и выполните следующие команды.</span><span class="sxs-lookup"><span data-stu-id="3a07d-318">To get the thumbprint of the installed certificate, but without spaces or special characters, open a Windows PowerShell window as an admin, and run the following commands.</span></span>

    ```powershell
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    > [!NOTE]
    > <span data-ttu-id="3a07d-319">Сохраните отпечаток, так как он потребуется позже при обновлении файлов .wif для сервера Application Object Server (AOS) и настройки конфигурации RSAT.</span><span class="sxs-lookup"><span data-stu-id="3a07d-319">Save the thumbprint, because you will need it later when you update the .wif files for Application Object Server (AOS) and set up the RSAT configuration.</span></span>

#### <a name="configure-the-aos-computer-to-trust-the-connection"></a><span data-ttu-id="3a07d-320">Настройка компьютера AOS, чтобы он доверял данному подключению</span><span class="sxs-lookup"><span data-stu-id="3a07d-320">Configure the AOS computer to trust the connection</span></span>

> [!NOTE]
> <span data-ttu-id="3a07d-321">Если среда является средой уровня 2+, отпечаток сертификата необходимо обновить в файле wif.config для **всех** компьютеров AOS в среде.</span><span class="sxs-lookup"><span data-stu-id="3a07d-321">If the environment is a Tier 2+ environment, the certificate thumbprint must be updated in the wif.config file for **all** AOS computers for the environment.</span></span>

1. <span data-ttu-id="3a07d-322">Создайте подключение по протоколу удаленного рабочего стола (RDP) на компьютере с сервером AOS.</span><span class="sxs-lookup"><span data-stu-id="3a07d-322">Establish a Remote Desktop Protocol (RDP) connection to the AOS computer.</span></span> <span data-ttu-id="3a07d-323">Сведения о входе доступны на странице сведений о среде в LCS.</span><span class="sxs-lookup"><span data-stu-id="3a07d-323">Sign-in details are available on the environment details page in LCS.</span></span>
2. <span data-ttu-id="3a07d-324">Откройте службы Microsoft Internet Information Services (IIS) и найдите **AOSService** в списке сайтов.</span><span class="sxs-lookup"><span data-stu-id="3a07d-324">Open Microsoft Internet Information Services (IIS), and find **AOSService** in the list of sites.</span></span>

    ![AOSService в списке сайтов](./media/setup_rsa_tool_49.png)

3. <span data-ttu-id="3a07d-326">Щелкните правой кнопкой мыши **Проводник**, чтобы открыть папку **\<Drive\>: \\AosService\\WebRoot**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-326">Right-click **Explore** to open the **\<Drive\>: \\AosService\\WebRoot** folder.</span></span> <span data-ttu-id="3a07d-327">Найдите файл **wif.config**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-327">Find the **wif.config** file.</span></span>

    ![Файл Wif.config в папке WebRoot](./media/setup_rsa_tool_50.png)

4. <span data-ttu-id="3a07d-329">Обновите файл **wif.config**, добавив новую запись центра для имени сертификата и центра, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="3a07d-329">Update the **wif.config** file by adding a new authority entry for your certificate and authority name, as shown in the following example.</span></span>

    ```Xml
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry,Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
            </keys>
            <validIssuers>
                <add name="CN=127.0.0.1" />
            </validIssuers>
        </authority>
    ```

    > [!NOTE]
    > <span data-ttu-id="3a07d-330">Если несколько пользователей используют одно и то же приложение, каждый пользователь должен создать отдельные отпечатки, а каждый из этих отпечаток должен быть добавлен в раздел **\<keys\>**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-330">If multiple users are using the same application, each user must generate separate thumbprints, and each of those thumbprints must be added in the **\<keys\>** section.</span></span>

5. <span data-ttu-id="3a07d-331">Если имеется более одного компьютера AOS, повторите шаги с 3 по 4 для каждого дополнительного компьютера.</span><span class="sxs-lookup"><span data-stu-id="3a07d-331">If there is more than one AOS computer, repeat steps 3 through 4 for each additional computer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3a07d-332">В отличие от старых сред уровня 2, новые среды уровня 2 развертываются с двумя экземплярами AOS.</span><span class="sxs-lookup"><span data-stu-id="3a07d-332">Unlike older Tier 2 environments, new Tier 2 environments are deployed with two AOS instances.</span></span>

6. <span data-ttu-id="3a07d-333">Выполните команду **iisreset** на всех компьютерах AOS.</span><span class="sxs-lookup"><span data-stu-id="3a07d-333">Run **iisreset** on all the AOS computers.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3a07d-334">Если у вас нет прав администратора для запуска **iisreset** на компьютере уровня 1, на странице сведений о среде в LCS выберите параметр "Поддержка > Перезапуск служб".</span><span class="sxs-lookup"><span data-stu-id="3a07d-334">If you don't have admin rights to run **iisreset** on a Tier 1 computer, on the Environment details page in LCS, select Maintain > Restart services.</span></span>

#### <a name="tier-2-environment"></a><span data-ttu-id="3a07d-335">Среда уровня 2+</span><span class="sxs-lookup"><span data-stu-id="3a07d-335">Tier 2+ environment</span></span>

<span data-ttu-id="3a07d-336">Если используются среда уровня 2 + (песочница "стандартный приемочный тест" или выше), проверьте или установите следующий параметр реестра на компьютере, на котором установлен RSAT.</span><span class="sxs-lookup"><span data-stu-id="3a07d-336">If a Tier 2+ (Standard Acceptance Test sandbox or higher) environment is used, verify or set the following registry setting on the computer where RSAT is installed.</span></span> <span data-ttu-id="3a07d-337">Этот шаг является обязательным, поскольку он позволяет избежать ошибок проверке подлинности или подключения RSAT.</span><span class="sxs-lookup"><span data-stu-id="3a07d-337">This step is required because it helps you avoid authentication or RSAT connection errors.</span></span>

```PowerShell
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

### <a name="install-rsat"></a><span data-ttu-id="3a07d-338">Установка RSAT</span><span class="sxs-lookup"><span data-stu-id="3a07d-338">Install RSAT</span></span>

1. <span data-ttu-id="3a07d-339">Перейдите к пункту <https://www.microsoft.com/download/details.aspx?id=57357> и выберите **Загрузить**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-339">Go to <https://www.microsoft.com/download/details.aspx?id=57357>, and select **Download**.</span></span>
2. <span data-ttu-id="3a07d-340">Выберите все файлы, затем выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-340">Select all the files, and then select **Next**.</span></span>

    ![Выбор всех файлов](./media/setup_rsa_tool_51.png)

3. <span data-ttu-id="3a07d-342">Дважды щелкните пакет .msi, чтобы запустить установщик.</span><span class="sxs-lookup"><span data-stu-id="3a07d-342">Double-click the .msi package to run the installer.</span></span> <span data-ttu-id="3a07d-343">Затем, после завершения установки, выберите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-343">Then, when the installation is completed, select **Finish**.</span></span>

    ![Файл установщика RSAT](./media/setup_rsa_tool_52.png)

### <a name="install-selenium-and-browser-drivers"></a><span data-ttu-id="3a07d-345">Установка драйверов Selenium и драйверов браузера</span><span class="sxs-lookup"><span data-stu-id="3a07d-345">Install Selenium and browser drivers</span></span>

<span data-ttu-id="3a07d-346">В предыдущих версиях RSAT необходимо установить драйверы Selenium и драйверы браузера.</span><span class="sxs-lookup"><span data-stu-id="3a07d-346">In older versions of RSAT, you had to install Selenium and browser drivers.</span></span> <span data-ttu-id="3a07d-347">Больше не нужно устанавливать эти драйверы, поскольку они автоматически устанавливаются.</span><span class="sxs-lookup"><span data-stu-id="3a07d-347">You no longer have to install these drivers because they are automatically installed.</span></span>

1. <span data-ttu-id="3a07d-348">При первом открытии программы RSAT появится запрос на автоматическую загрузку и установку Selenium.</span><span class="sxs-lookup"><span data-stu-id="3a07d-348">The first time that you open RSAT, you're prompted to automatically download and install Selenium.</span></span> <span data-ttu-id="3a07d-349">Дополнительные сведения см. в разделе [Настройка RSAT](#configure-rsat).</span><span class="sxs-lookup"><span data-stu-id="3a07d-349">For more information, see the [Configure RSAT](#configure-rsat) section.</span></span>
2. <span data-ttu-id="3a07d-350">Прежде чем можно будет выполнить тестовый случай, вам будет предложено автоматически загрузить и установить драйвер браузера, соответствующий браузеру по умолчанию, выбранному в конфигурации RSAT.</span><span class="sxs-lookup"><span data-stu-id="3a07d-350">Before you can run a test case, you're prompted to automatically download and install the browser driver that corresponds to the default browser that is selected in the RSAT configuration.</span></span> <span data-ttu-id="3a07d-351">Дополнительные сведения см. в разделе [Загрузка и выполнение тестовых случаев](#load-and-run-test-cases).</span><span class="sxs-lookup"><span data-stu-id="3a07d-351">For more information, see the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

## <a name="get-started-with-rsat"></a><span data-ttu-id="3a07d-352">Начало работы с RSAT</span><span class="sxs-lookup"><span data-stu-id="3a07d-352">Get started with RSAT</span></span>

### <a name="create-a-test-plan-and-test-suites"></a><span data-ttu-id="3a07d-353">Создание плана тестирования и наборов тестов</span><span class="sxs-lookup"><span data-stu-id="3a07d-353">Create a test plan and test suites</span></span>

1. <span data-ttu-id="3a07d-354">Перейдите к проекту Azure DevOps и выберите **Планы испытаний**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-354">Go to the Azure DevOps project, and select **Test Plans**.</span></span>

    ![Команда "Планы испытаний"](./media/setup_rsa_tool_53.png)

2. <span data-ttu-id="3a07d-356">Выберите **Создать план испытаний**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-356">Select **New Test Plan**.</span></span>

    ![Кнопка создания плана испытаний](./media/setup_rsa_tool_54.png)

3. <span data-ttu-id="3a07d-358">Заполните поле **Имя**, затем выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-358">Fill in the **Name** field, and then select **Create**.</span></span> <span data-ttu-id="3a07d-359">В данном учебнике назовите план испытаний **План испытаний RSAT**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-359">For this tutorial, name the test plan **RSAT Test Plan**.</span></span>

    ![Диалоговое окно создания плана испытаний](./media/setup_rsa_tool_55.png)

4. <span data-ttu-id="3a07d-361">Выберите знак "плюс" (**+**), затем выберите **Статический набор**, чтобы создать статический набор в новом плане тестирования.</span><span class="sxs-lookup"><span data-stu-id="3a07d-361">Select the plus sign (**+**), and then select **Static suite** to create a static suite under the new test plan.</span></span> <span data-ttu-id="3a07d-362">Назовите новый набор тестов **T01 – От производства до склада**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-362">Name the new test suite **T01 – Make to Stock**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3a07d-363">Кроме того, можно создать набор на основе запросов, если необходимо автоматически перенести новые тестовые случаи из BPM в набор тестов RSAT.</span><span class="sxs-lookup"><span data-stu-id="3a07d-363">You can also create a query-based suite, if you want the new test cases from BPM to be automatically pulled into the RSAT test suite.</span></span>

    ![Создание статического набора](./media/setup_rsa_tool_56.png)

### <a name="attach-test-cases-to-test-suites"></a><span data-ttu-id="3a07d-365">Подключение тестовых случаев к наборам тестов</span><span class="sxs-lookup"><span data-stu-id="3a07d-365">Attach test cases to test suites</span></span>

1. <span data-ttu-id="3a07d-366">Выберите **Добавить существующее** в правой части, чтобы добавить существующие тестовые случаи в набор тестов.</span><span class="sxs-lookup"><span data-stu-id="3a07d-366">Select **Add existing** on the right side to add existing test cases to the test suite.</span></span>

    ![Кнопка добавления существующих](./media/setup_rsa_tool_57.png)

2. <span data-ttu-id="3a07d-368">На странице **Добавление тестовых случаев в набор** выберите **Выполнить запрос**, затем выберите тестовый случай, который требуется добавить в набор тестов.</span><span class="sxs-lookup"><span data-stu-id="3a07d-368">On the **Add test cases to suite** page, select **Run query**, and then select the test case to add to the test suite.</span></span> <span data-ttu-id="3a07d-369">Для этого учебника выберите тестовый случай **Создание нового продукта**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-369">For this tutorial, select the **Create a new product** test case.</span></span> <span data-ttu-id="3a07d-370">Затем выберите **Добавить тестовые случаи** в нижнем правом углу страницы (эта кнопка не отображается на следующем рисунке).</span><span class="sxs-lookup"><span data-stu-id="3a07d-370">Then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![Кнопка запуска запроса](./media/setup_rsa_tool_58.png)

    <span data-ttu-id="3a07d-372">Тестовый случай добавляется к набору тестов **T01 — От производства до склада**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-372">The test case is added to the **T01-Make to Stock** test suite.</span></span>

    ![Тестовый случай, добавленный в набор тестов](./media/setup_rsa_tool_59.png)

### <a name="configure-rsat"></a><span data-ttu-id="3a07d-374">Настройка RSAT</span><span class="sxs-lookup"><span data-stu-id="3a07d-374">Configure RSAT</span></span>

1. <span data-ttu-id="3a07d-375">Откройте RSAT.</span><span class="sxs-lookup"><span data-stu-id="3a07d-375">Open RSAT.</span></span>

    ![Значок RSAT](./media/setup_rsa_tool_60.png)

2. <span data-ttu-id="3a07d-377">Вы получите предупреждающее сообщение с текстом "Для Regression Suite Automation Tool требуется Selenium, хотите загрузить и установить его автоматически?"</span><span class="sxs-lookup"><span data-stu-id="3a07d-377">You receive a warning message that states, "The Regression Suite Automation Tool requires Selenium, do you want to automatically download and install it now?"</span></span> <span data-ttu-id="3a07d-378">Выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-378">Select **Yes**.</span></span>

    ![Сообщение, предупреждающее о том, что для Regression Suite Automation Tool требуется Selenium](./media/setup_rsa_tool_61.png)

3. <span data-ttu-id="3a07d-380">Нажмите кнопку **Настройки** (символ шестеренки) в верхнем правом углу, затем в появившемся диалоговом окне заполните следующие поля:</span><span class="sxs-lookup"><span data-stu-id="3a07d-380">Select the **Settings** button (the gear symbol) in the upper-right corner, and then, in the dialog box that appears, fill in the following fields:</span></span>

    - <span data-ttu-id="3a07d-381">**URL-адрес Azure DevOps** — введите URL-адрес проекта Azure DevOps, например `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span><span class="sxs-lookup"><span data-stu-id="3a07d-381">**Azure DevOps Url** – Enter the URL of your Azure DevOps project, such as `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span></span>
    - <span data-ttu-id="3a07d-382">**Маркер доступа** — введите маркер доступа, который позволяет средству подключиться к Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="3a07d-382">**Access Token** – Enter the access token that lets the tool connect to Azure DevOps.</span></span> <span data-ttu-id="3a07d-383">Используйте личный маркер доступа, созданный ранее в этом учебнике.</span><span class="sxs-lookup"><span data-stu-id="3a07d-383">Use the personal access token that you created earlier in this tutorial.</span></span> <span data-ttu-id="3a07d-384">Дополнительные сведения см. в разделе [Проверка подлинности с использованием личных маркеров доступа](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span><span class="sxs-lookup"><span data-stu-id="3a07d-384">For more information, see [Authenticate access with personal access tokens](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span></span>
    - <span data-ttu-id="3a07d-385">**Название проекта** — выберите имя своего проекта Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="3a07d-385">**Project Name** – Select the name of your Azure DevOps project.</span></span>
    - <span data-ttu-id="3a07d-386">**План испытаний** — выберите план тестирования Azure DevOps, содержащий тестовые случаи.</span><span class="sxs-lookup"><span data-stu-id="3a07d-386">**Test Plan** – Select the Azure DevOps test plan that contains your test cases.</span></span> <span data-ttu-id="3a07d-387">Дополнительные сведения см. в разделе [Создание планов испытаний и наборов тестов](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span><span class="sxs-lookup"><span data-stu-id="3a07d-387">For more information, see [Create test plans and test suites](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span></span> <span data-ttu-id="3a07d-388">После выбора плана тестирования выберите **Проверить подключение**, чтобы проверить подключение к Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="3a07d-388">After you select a test plan, select **Test Connection** to test your connection to Azure DevOps.</span></span>
    - <span data-ttu-id="3a07d-389">**Имя узла** — введите имя узла для среды испытаний, например **\<myaos\>.cloudax.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-389">**Hostname** – Enter the host name of the test environment, such as **\<myaos\>.cloudax.dynamics.com**.</span></span> <span data-ttu-id="3a07d-390">Не включайте префикс **https://** или **http://**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-390">Don't include the **https://** or **http://** prefix.</span></span>
    - <span data-ttu-id="3a07d-391">**Имя узла SOAP** — введите имя узла SOAP тестовой среды.</span><span class="sxs-lookup"><span data-stu-id="3a07d-391">**SOAP Hostname** – Enter the SOAP host name of the test environment.</span></span> <span data-ttu-id="3a07d-392">Обычно имя узла SOAP совпадает с именем хоста, но имеет суффикс **soap**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-392">Typically, the SOAP host name is the same as the host name, but it has a **soap** suffix.</span></span> <span data-ttu-id="3a07d-393">Например: **\<myaos\>soap.cloudax.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-393">Here is an example: **\<myaos\>soap.cloudax.dynamics.com**.</span></span> <span data-ttu-id="3a07d-394">Не включайте префикс **https://** или **http://**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-394">Don't include the **https://** or **http://** prefix.</span></span>

        > [!NOTE]
        > <span data-ttu-id="3a07d-395">Чтобы найти имя узла и имя узла SOAP, откройте диспетчер служб IIS, щелкните правой кнопкой мыши **Сайты \> AOSService** и выберите команду **Изменить привязки**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-395">To find the host name and SOAP host name, open IIS Manager, right-click **Sites \> AOSService**, and then select **Edit bindings**.</span></span> <span data-ttu-id="3a07d-396">Значения в столбце **Имя узла** дают имя узла и имя узла SOAP (имя узла SOAP содержит суффикс **soap** в URL-адресе).</span><span class="sxs-lookup"><span data-stu-id="3a07d-396">The values in the **Host Name** column give you the host name and SOAP host name (the SOAP host name has the suffix **soap** in the URL).</span></span>

        ![Имя узла и имя узла SOAP в столбце имени узла](./media/setup_rsa_tool_63.png)

    - <span data-ttu-id="3a07d-398">**Имя пользователя-администратора** — введите адрес электронной почты пользователя-администратора в среде тестирования.</span><span class="sxs-lookup"><span data-stu-id="3a07d-398">**Admin user name** – Enter the email address of an admin user in the test environment.</span></span>
    - <span data-ttu-id="3a07d-399">**Отпечаток** — введите отпечаток сертификата проверки подлинности, как описано ранее в этом учебнике.</span><span class="sxs-lookup"><span data-stu-id="3a07d-399">**Thumbprint** – Enter the thumbprint of the authentication certificate, as described earlier in this tutorial.</span></span>
    - <span data-ttu-id="3a07d-400">**Рабочий каталог** — укажите местоположение папки для хранения файлов автоматизации тестирования, таких как файлы данных тестирования Excel.</span><span class="sxs-lookup"><span data-stu-id="3a07d-400">**Working directory** – Specify the folder location for storing test automation files, such as Excel test data files.</span></span> <span data-ttu-id="3a07d-401">Например, введите или выберите **C:\\Temp\\RegressionTool**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-401">For example, enter or select **C:\\Temp\\RegressionTool**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="3a07d-402">Если имя папки содержит пробелы, выполнение будет неудачным, так как папка будет не найдена.</span><span class="sxs-lookup"><span data-stu-id="3a07d-402">If the name of the folder has spaces, execution will fail because the folder can't be found.</span></span> <span data-ttu-id="3a07d-403">Эта проблема известна и должна быть исправлена в последней версии средства.</span><span class="sxs-lookup"><span data-stu-id="3a07d-403">This issue is a known issue and should be fixed in the latest version of the tool.</span></span>

    - <span data-ttu-id="3a07d-404">**Браузер по умолчанию** — выберите **Internet Explorer** или **Google Chrome**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-404">**Default browser** – Select either **Internet Explorer** or **Google Chrome**.</span></span> <span data-ttu-id="3a07d-405">Убедитесь, что установлены соответствующие драйверы браузера.</span><span class="sxs-lookup"><span data-stu-id="3a07d-405">Make sure that the appropriate browser drivers have been installed.</span></span>
    - <span data-ttu-id="3a07d-406">**Время ожидания тестового запуска** — укажите период ожидания в минутах для тестовых запусков.</span><span class="sxs-lookup"><span data-stu-id="3a07d-406">**Test run timeout** – Specify the time-out period, in minutes, for test runs.</span></span> <span data-ttu-id="3a07d-407">По истечении времени ожидания все активные окна закрываются, а ожидающие тестовые случаи заканчиваются сбоем.</span><span class="sxs-lookup"><span data-stu-id="3a07d-407">When the time-out period elapses, all active windows are closed, and pending test cases fail.</span></span>
    - <span data-ttu-id="3a07d-408">**Время ожидания действия проверки** — это поле определяет период ожидания в минутах для запросов сервера среды Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3a07d-408">**Test action timeout** – This field controls the time-out period, in minutes, for Finance and Operation environment server requests.</span></span> <span data-ttu-id="3a07d-409">Обычно должно быть достаточно значения по умолчанию (2 минуты).</span><span class="sxs-lookup"><span data-stu-id="3a07d-409">Usually, the default value (2 minutes) should be enough.</span></span> <span data-ttu-id="3a07d-410">Однако для более медленных сред может возникнуть необходимость увеличить значение, если происходят ошибки, связанные со временем ожидания.</span><span class="sxs-lookup"><span data-stu-id="3a07d-410">However, for slower environments, you might want to increase the value if errors that are related to time-outs occur.</span></span>
    - <span data-ttu-id="3a07d-411">**Название компании** — введите название компании, которое будет использоваться в качестве компании по умолчанию при создании файлов параметров Excel.</span><span class="sxs-lookup"><span data-stu-id="3a07d-411">**Company name** – Enter the company name to use as your default company when Excel parameter files are created.</span></span> <span data-ttu-id="3a07d-412">Позднее можно изменить компанию, отредактировав файл параметров Excel.</span><span class="sxs-lookup"><span data-stu-id="3a07d-412">You can change the company later by editing the Excel parameter file.</span></span>

    ![Диалоговое окно настроек](./media/setup_rsa_tool_62.png)

4. <span data-ttu-id="3a07d-414">Выберите **Применить** для применения и сохранения настроек.</span><span class="sxs-lookup"><span data-stu-id="3a07d-414">Select **Apply** to apply and save your settings.</span></span>

    <span data-ttu-id="3a07d-415">Для сохранения текущих настроек в файл конфигурации на компьютере выберите **Сохранить как**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-415">To save your current settings to a configuration file on your computer, select **Save as**.</span></span> <span data-ttu-id="3a07d-416">Для восстановления настроек из файла конфигурации на компьютер выберите **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-416">To restore your settings from a configuration file on your computer, select **Open**.</span></span>

5. <span data-ttu-id="3a07d-417">Выберите **Закрыть**, чтобы закрыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="3a07d-417">Select **Close** to close the dialog box.</span></span>

### <a name="load-and-run-test-cases"></a><span data-ttu-id="3a07d-418">Загрузка и выполнение тестовых случаев</span><span class="sxs-lookup"><span data-stu-id="3a07d-418">Load and run test cases</span></span>

1. <span data-ttu-id="3a07d-419">Выберите **Загрузить**, чтобы загрузить план испытаний **План испытаний RSAT** из проекта Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="3a07d-419">Select **Load** to load the **RSAT Test Plan** test plan from the Azure DevOps project.</span></span>

    ![Кнопка загрузки](./media/setup_rsa_tool_64.png)

2. <span data-ttu-id="3a07d-421">Выберите тестовый случай **Создание нового продукта** из набора тестов, затем выберите **Создать \> Создание выполнения теста и файлов параметров**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-421">Select the **Create a new product** test case from the test suite, and then select **New \> Generate Test Execution and Parameter files**.</span></span>

    ![Команда создания выполнения тестов и файлов параметров в меню создания](./media/setup_rsa_tool_65.png)

    <span data-ttu-id="3a07d-423">Файл параметров Excel создается в локальной папке, указанной в конфигурации RSAT (например, **C:\\Temp\\RegressionTool**).</span><span class="sxs-lookup"><span data-stu-id="3a07d-423">The Excel parameter file is created in the local folder that you specified in the RSAT configuration (for example, **C:\\Temp\\RegressionTool**).</span></span>

    ![Создан файл параметров Excel](./media/setup_rsa_tool_66.png)

3. <span data-ttu-id="3a07d-425">Если требуется сохранить файлы параметров, выберите **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-425">If you want to save the parameter files, select **Upload**.</span></span> <span data-ttu-id="3a07d-426">Файлы автоматизации тестирования для всех выбранных тестовых случаев отправляются в Azure DevOps для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="3a07d-426">Test automation files of all selected test cases are uploaded to Azure DevOps for future use.</span></span> <span data-ttu-id="3a07d-427">(Эти файлы включают файлы параметров тестирования Excel.)</span><span class="sxs-lookup"><span data-stu-id="3a07d-427">(These files include Excel test parameter files.)</span></span>

    <span data-ttu-id="3a07d-428">Таким образом, можно выбрать команду **Загрузка** для загрузки файлов параметров (и файлов автоматизации) непосредственно из тестового случая в Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="3a07d-428">In this way, you can select **Load** to load the parameter files (and automation files) from the test case directly from Azure DevOps.</span></span> <span data-ttu-id="3a07d-429">Нет необходимости повторно формировать файлы параметров.</span><span class="sxs-lookup"><span data-stu-id="3a07d-429">You don't have to regenerate the parameter files.</span></span> <span data-ttu-id="3a07d-430">Этот подход будет важен в дальнейшем, когда необходимо сохранить изменения в файле параметров и не нужно перезаписывать их.</span><span class="sxs-lookup"><span data-stu-id="3a07d-430">This approach will become important later, when you want to keep the modifications in the parameter file and don't want them to be overwritten.</span></span>

4. <span data-ttu-id="3a07d-431">Чтобы убедиться, что файлы автоматизации и файлы параметров сохранены в Azure DevOps, перейдите в проект Azure DevOps, выберите **Панели \> Рабочие элементы** и выберите тестовый случай **Создание нового продукта**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-431">To verify that the automation files and parameter files are saved to Azure DevOps, go to the Azure DevOps project, select **Boards \> Work Items**, and select the **Create a new product** test case.</span></span> <span data-ttu-id="3a07d-432">На вкладке **Вложения** должны быть видны четыре файла:</span><span class="sxs-lookup"><span data-stu-id="3a07d-432">On the **Attachments** tab, you should see four files:</span></span>

    - <span data-ttu-id="3a07d-433">**.cs** — файл автоматизации C\#</span><span class="sxs-lookup"><span data-stu-id="3a07d-433">**.cs** – C\# automation file</span></span>
    - <span data-ttu-id="3a07d-434">**.dll** — скомпилированный файл автоматизации в виде сборки</span><span class="sxs-lookup"><span data-stu-id="3a07d-434">**.dll** – Compiled automation file as an assembly</span></span>
    - <span data-ttu-id="3a07d-435">**.xlsx** — файл параметров Excel</span><span class="sxs-lookup"><span data-stu-id="3a07d-435">**.xlsx** – Excel parameter file</span></span>
    - <span data-ttu-id="3a07d-436">**.xml** — файл записи</span><span class="sxs-lookup"><span data-stu-id="3a07d-436">**.xml** – Recording file</span></span>

    ![Файлы на вкладке "Вложения"](./media/setup_rsa_tool_67.png)

5. <span data-ttu-id="3a07d-438">Выберите тестовый случай, который необходимо выполнить, затем выберите **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-438">Select the test case to run, and then select **Run**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3a07d-439">Перед запуском тестовых случаев, если используется браузер Internet Explorer, убедитесь, что для разрешения рабочего стола установлено значение **100%** в поле **Настройка дисплея Windows \> Масштаб и формат**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-439">Before you run test cases, if you're using Internet Explorer as the browser, make sure that your desktop resolution is set to **100%** at **Windows Display settings \> Scale and layout**.</span></span> <span data-ttu-id="3a07d-440">Если вы не можете изменить этот параметр на виртуальной машине (ВМ), измените его на клиенте (ноутбуке), с которого вы пытаетесь получить доступ к ВМ.</span><span class="sxs-lookup"><span data-stu-id="3a07d-440">If you can't change this setting on a virtual machine (VM), change it on the client (laptop) that you're trying to access the VM from.</span></span> <span data-ttu-id="3a07d-441">Затем параметры разрешения наследуются настройками дисплея виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3a07d-441">The resolution settings will then be inherited by the VM display settings.</span></span>

    ![Разрешение рабочего стола установлено на 100%](./media/setup_rsa_tool_68.png)

6. <span data-ttu-id="3a07d-443">Если драйверы браузера не установлены в системе, выводится предупреждающее сообщение "Для этой операции требуется драйвер \<browser name\>.</span><span class="sxs-lookup"><span data-stu-id="3a07d-443">If the browser drivers aren't installed in the system, you receive a warning message that states, "This operation requires the \<browser name\> driver.</span></span> <span data-ttu-id="3a07d-444">Вы хотите загрузить и установить его автоматически?"</span><span class="sxs-lookup"><span data-stu-id="3a07d-444">Do you want to automatically downloads and install it now?"</span></span> <span data-ttu-id="3a07d-445">Выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-445">Select **Yes**.</span></span>

    ![Предупреждающее сообщение для Internet Explorer](./media/setup_rsa_tool_69.png)

    ![Предупреждающее сообщение для Chrome](./media/setup_rsa_tool_70.png)

    > [!NOTE]
    > <span data-ttu-id="3a07d-448">Если в качестве браузера используется Chrome и получено сообщение об ошибке, в котором говорится, что сеанс не был создан из-за неправильной версии Chrome, загрузите последний драйвер Chrome с сайта <http://chromedriver.chromium.org/downloads> в папку **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-448">If you're using Chrome as the browser and receive an error message that states that the session wasn't created because the Chrome version isn't correct, download the latest Chrome driver from <http://chromedriver.chromium.org/downloads> to the **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium** folder.</span></span>

    ![Сообщение об ошибке для Chrome](./media/setup_rsa_tool_71.png)

    <span data-ttu-id="3a07d-450">Выполняется тестовый случай, и поле **Результат** обновляется.</span><span class="sxs-lookup"><span data-stu-id="3a07d-450">The test case is run, and the **Result** field is updated.</span></span>

    ![Обновленное поле результата](./media/setup_rsa_tool_72.png)

    <span data-ttu-id="3a07d-452">Если вы буквально следовали данному учебнику, то тестовый случай **Создание нового продукта** будет неудачным, поскольку запись задачи для создания продукта сохранит название продукта в виде жестко запрограммированного значения.</span><span class="sxs-lookup"><span data-stu-id="3a07d-452">If you've followed this tutorial as it's written, the **Create a new product** test case will fail, because the task recording for creating a product saved the product name as a hard-coded value.</span></span> <span data-ttu-id="3a07d-453">При повторном запуске того же тестового случая должно быть получено сообщение об ошибке, поскольку продукт уже существует.</span><span class="sxs-lookup"><span data-stu-id="3a07d-453">If you rerun the same test case, you should receive an error message, because the product already exists.</span></span>

    ![В поле результата задано значение "Не пройден"](./media/setup_rsa_tool_72.png)

### <a name="view-the-test-results"></a><span data-ttu-id="3a07d-455">Просмотр результатов теста</span><span class="sxs-lookup"><span data-stu-id="3a07d-455">View the test results</span></span>

1. <span data-ttu-id="3a07d-456">Дважды щелкните неудачный тестовый случай.</span><span class="sxs-lookup"><span data-stu-id="3a07d-456">Double-click the failed test case.</span></span>

    <span data-ttu-id="3a07d-457">Вы получаете сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="3a07d-457">You receive an error message.</span></span>

    ![Сообщение об ошибке](./media/setup_rsa_tool_73.png)

2. <span data-ttu-id="3a07d-459">Выберите **Сведения** для просмотра сообщения об ошибке целиком.</span><span class="sxs-lookup"><span data-stu-id="3a07d-459">Select **Details** to view the whole error message.</span></span>

    ![Все сообщение об ошибке](./media/setup_rsa_tool_74.png)

3. <span data-ttu-id="3a07d-461">Чтобы просмотреть подробную версию сообщения об ошибке в Azure DevOps, выберите **Открыть в Azure DevOps**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-461">To view a detailed version of the error message in Azure DevOps, select **Open in Azure DevOps**.</span></span> <span data-ttu-id="3a07d-462">В Azure DevOps можно просмотреть статус тестового случая и подробное сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="3a07d-462">In Azure DevOps, you can view the status of the test case and the detailed error message.</span></span>

    ![Подробное сообщение об ошибке в Azure DevOps](./media/setup_rsa_tool_75.png)

4. <span data-ttu-id="3a07d-464">Чтобы просмотреть результаты тестирования непосредственно в проекте Azure DevOps, перейдите в раздел **Планы испытаний \> Планы испытаний \> Выполнения**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-464">To view the test results directly in the Azure DevOps project, go to **Test Plans \> Test Plans \> Runs**.</span></span> <span data-ttu-id="3a07d-465">Дважды щелкните выполнение теста, для которого необходимо просмотреть дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="3a07d-465">Double-click the test run that you want to see more details for.</span></span>

    ![Список тестовых запусков в Azure DevOps](./media/setup_rsa_tool_76.png)

5. <span data-ttu-id="3a07d-467">Вкладка **Сводка выполнения** указывает, что тестовый случай завершился ошибкой, но не предоставляет фактическое сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="3a07d-467">The **Run summary** tab indicates that the test case failed, but it doesn't provide the actual error message.</span></span> <span data-ttu-id="3a07d-468">Чтобы просмотреть подробное сообщение об ошибке, перейдите на вкладку **Результаты проверки**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-468">To view the detailed error message, select the **Test results** tab.</span></span>

    ![Вкладка "Результаты проверки"](./media/setup_rsa_tool_77.png)

    <span data-ttu-id="3a07d-470">На вкладке **Результаты проверки** выводятся сведения о тестовом случае вместе с результатом и сообщением об ошибке.</span><span class="sxs-lookup"><span data-stu-id="3a07d-470">The **Test results** tab provides the test case information, together with the outcome and the error message.</span></span>

    ![Вкладка результатов проверки](./media/setup_rsa_tool_78.png)

6. <span data-ttu-id="3a07d-472">Дважды щелкните соответствующую запись, чтобы просмотреть подробное сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="3a07d-472">Double-click the relevant record to view the detailed error message.</span></span>

    ![Подробное сообщение об ошибке](./media/setup_rsa_tool_79.png)

    > [!NOTE]
    > <span data-ttu-id="3a07d-474">Все сообщения об ошибках также доступны локально в файле **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-474">All error messages are also available locally in **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.</span></span>

7. <span data-ttu-id="3a07d-475">Можно также экспортировать результаты выполнения теста из уровня плана тестирования, выбрав **Экспорт**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-475">You can also export the test run results from the test plan level by selecting **Export**.</span></span>

    ![Экспорт плана испытаний](./media/setup_rsa_tool_80.png)

### <a name="modify-the-excel-parameter-file"></a><span data-ttu-id="3a07d-477">Изменение файла параметров Excel</span><span class="sxs-lookup"><span data-stu-id="3a07d-477">Modify the Excel parameter file</span></span>

1. <span data-ttu-id="3a07d-478">Откройте RSAT.</span><span class="sxs-lookup"><span data-stu-id="3a07d-478">Open RSAT.</span></span>
2. <span data-ttu-id="3a07d-479">Выберите тестовый случай, затем выберите **Правка**, чтобы открыть файл параметров Excel.</span><span class="sxs-lookup"><span data-stu-id="3a07d-479">Select the test case, and then select **Edit** to open the Excel parameter file.</span></span>

    <span data-ttu-id="3a07d-480">На листе **EcoResProductCreate** обратите внимание, что значение поля **Код продукта** является жестко закодированным.</span><span class="sxs-lookup"><span data-stu-id="3a07d-480">On the **EcoResProductCreate** sheet, notice that the value of the **Product number** field is hard-coded.</span></span> <span data-ttu-id="3a07d-481">Перед повторным запуском тестового случая необходимо обновить это поле до нового номера продукта.</span><span class="sxs-lookup"><span data-stu-id="3a07d-481">You must update this field to a new product number before you run the test case again.</span></span>

3. <span data-ttu-id="3a07d-482">Чтобы создать уникальный номер продукта для каждого запуска без повторного открытия файла параметров Excel и ручного обновления номера продукта каждый раз, используйте следующую формулу Excel.</span><span class="sxs-lookup"><span data-stu-id="3a07d-482">To generate a unique product number for each run without having to reopen the Excel parameter file and manually update the product number every time, use the following Excel formula.</span></span>

    ```vba
    ="RSAT_"&TEXT(NOW(),"yyymmddhhmm")
    ```

    > [!NOTE]
    > <span data-ttu-id="3a07d-483">В дополнение к вкладке **Общие**, файл параметров Excel содержит вкладку данных для каждой страницы формы, которую посещает тестовый случай.</span><span class="sxs-lookup"><span data-stu-id="3a07d-483">In addition to the **General** tab, the Excel parameter file contains a data tab for every form page the test case visits.</span></span>

    ![Поле номера продукта](./media/setup_rsa_tool_81.png)

4. <span data-ttu-id="3a07d-485">Выберите **Сохранить** и закройте книгу Excel.</span><span class="sxs-lookup"><span data-stu-id="3a07d-485">Select **Save**, and then close the Excel workbook.</span></span>
5. <span data-ttu-id="3a07d-486">Выберите **Отправить**, чтобы сохранить файл параметров Excel в Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="3a07d-486">Select **Upload** to save the Excel parameter file to Azure DevOps.</span></span>

    ![Сообщение об успешной отправке](./media/setup_rsa_tool_82.png)

    > [!NOTE]
    > <span data-ttu-id="3a07d-488">Чтобы выполнить тестовые случаи в конкретном контексте пользователя, введите код электронной почты пользователя в поле **Тестовый пользователь** на вкладке **Общие** в файле параметров Excel.</span><span class="sxs-lookup"><span data-stu-id="3a07d-488">To run test cases in a specific user context, enter the user's email ID in the **Test User** field on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="3a07d-489">В последней версии средства RSAT макет полей в файле параметров Excel был обновлен, но концепция остается одинаковой.</span><span class="sxs-lookup"><span data-stu-id="3a07d-489">In the latest version of RSAT, the layout of the fields in the Excel parameter file has been updated, but the concept remains the same.</span></span>
    >
    > ![Поле тестового пользователя](./media/setup_rsa_tool_83.png)

### <a name="validate-the-results"></a><span data-ttu-id="3a07d-491">Проверка результатов</span><span class="sxs-lookup"><span data-stu-id="3a07d-491">Validate the results</span></span>

- <span data-ttu-id="3a07d-492">Выберите **Выполнить**, чтобы повторно запустить тестовый случай, и проверьте, что тестовый случай пройден.</span><span class="sxs-lookup"><span data-stu-id="3a07d-492">Select **Run** to rerun the test case, and verify that the test case has passed.</span></span> <span data-ttu-id="3a07d-493">Результаты испытаний можно просмотреть, как описано в разделе [Просмотр результатов испытаний](#view-the-test-results).</span><span class="sxs-lookup"><span data-stu-id="3a07d-493">You can view the test results as described in the [View the test results](#view-the-test-results) section.</span></span>

    ![В поле результата задано значение "Выполнено"](./media/setup_rsa_tool_84.png)

### <a name="chaining-of-test-cases"></a><span data-ttu-id="3a07d-495">Объединение тестовых случаев</span><span class="sxs-lookup"><span data-stu-id="3a07d-495">Chaining of test cases</span></span>

<span data-ttu-id="3a07d-496">Одной из важнейших функций RSAT является связывание тестовых случаев (то есть, возможность передачи значений из одного испытания в другие испытания).</span><span class="sxs-lookup"><span data-stu-id="3a07d-496">One key feature of RSAT is the chaining of test cases (that is, the capability of a test to pass values to other tests).</span></span> <span data-ttu-id="3a07d-497">Тестовые случаи выполняются в соответствии с определенным порядком в плане тестирования Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="3a07d-497">Test cases are run according to their defined order in the Azure DevOps test plan.</span></span> <span data-ttu-id="3a07d-498">(Этот порядок также можно обновить в самом средстве тестирования.) Таким образом, если необходимо передать переменные из одного тестового случая в другой, очень важно, чтобы испытания выполнялись в нужном порядке.</span><span class="sxs-lookup"><span data-stu-id="3a07d-498">(This order can also be updated in the test tool itself.) Therefore, if you want to pass variables from one test case to another, it's very important that the tests be in the correct order.</span></span>

<span data-ttu-id="3a07d-499">В этом разделе создается сохраненная переменная в первом тестовом случае, создается второй тестовый случай и передается сохраненная переменная из первого тестового случая во второй тестовый случай.</span><span class="sxs-lookup"><span data-stu-id="3a07d-499">In this section, you will create a saved variable in the first test case, create a second test case, and pass the saved variable from the first test case to the second test case.</span></span> <span data-ttu-id="3a07d-500">Затем тестовые случаи выполняются как связанный тестовый случай в средстве RSAT.</span><span class="sxs-lookup"><span data-stu-id="3a07d-500">You will then run the test cases as a chained test case in RSAT.</span></span>

#### <a name="modify-an-existing-task-recording-to-create-a-saved-variable"></a><span data-ttu-id="3a07d-501">Изменение существующей записи задачи для создания сохраненной переменной</span><span class="sxs-lookup"><span data-stu-id="3a07d-501">Modify an existing task recording to create a saved variable</span></span>

1. <span data-ttu-id="3a07d-502">Откройте клиент.</span><span class="sxs-lookup"><span data-stu-id="3a07d-502">Open the client.</span></span>
2. <span data-ttu-id="3a07d-503">Выберите кнопку **Настройки** (символ шестеренки), затем выберите **Регистратор задач**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-503">Select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>
3. <span data-ttu-id="3a07d-504">Выберите **Редактировать запись**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-504">Select **Edit Recording**.</span></span>

    ![Кнопка "Редактировать запись"](./media/setup_rsa_tool_85.png)

4. <span data-ttu-id="3a07d-506">Выберите **Открыть из Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-506">Select **Open from Lifecycle Services**.</span></span>

    ![Кнопка "Открыть из Lifecycle Services"](./media/setup_rsa_tool_86.png)

5. <span data-ttu-id="3a07d-508">Выберите **Выберите библиотеку Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-508">Select **Select the Lifecycle Services library**.</span></span>

    ![Кнопка "Выберите библиотеку Lifecycle Services."](./media/setup_rsa_tool_87.png)

    <span data-ttu-id="3a07d-510">Библиотеки BPM загружаются из LCS.</span><span class="sxs-lookup"><span data-stu-id="3a07d-510">BPM libraries are loaded from LCS.</span></span>

    ![Загрузка библиотек BPM](./media/setup_rsa_tool_88.png)

6. <span data-ttu-id="3a07d-512">После загрузки библиотек BPM из LCS выберите библиотеку BPM **RSAT** и бизнес-процесс **Создание нового продукта**, с которым была связана запись задачи.</span><span class="sxs-lookup"><span data-stu-id="3a07d-512">After the BPM libraries are loaded from LCS, select the **RSAT** BPM library and the **Create a new product** business process that the task recording was associated with.</span></span> <span data-ttu-id="3a07d-513">Затем выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-513">Then select **OK**.</span></span>

    ![Выбор библиотеки BPM и бизнес-процесса](./media/setup_rsa_tool_89.png)

7. <span data-ttu-id="3a07d-515">Имя соответствующей записи задачи вводится в поле **Имя записи**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-515">The name of the appropriate task recording is entered in the **Recording name** field.</span></span> <span data-ttu-id="3a07d-516">Выберите **Пуск**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-516">Select **Start**.</span></span>

    ![Имя записи задачи в поле "Имя записи"](./media/setup_rsa_tool_90.png)

8. <span data-ttu-id="3a07d-518">Перейдите в пункт **Управление сведениями о продукте \> Продукты**, затем выберите **Создать**, чтобы открыть страницу, в которой была записана исходная запись задачи **Создание продукта**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-518">Go to **Product information management \> Products**, and select **New** to open the page where the original task recording, **Create a product**, was recorded.</span></span>
9. <span data-ttu-id="3a07d-519">Выберите пункт **Вставить шаг**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-519">Select **Insert step**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3a07d-520">Новый шаг добавляется **после** шага, выбранного в области.</span><span class="sxs-lookup"><span data-stu-id="3a07d-520">The new step is inserted **after** the step that you selected in the pane.</span></span>

    ![Кнопка "Вставить шаг"](./media/setup_rsa_tool_91.png)

10. <span data-ttu-id="3a07d-522">Щелкните правой кнопкой мыши поле **Номер продукта**, затем выберите **Регистратор задач \> Копировать**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-522">Right-click the **Product number** field, and then select **Task recorder \> Copy**.</span></span>

    ![Команда копирования](./media/setup_rsa_tool_92.png)

11. <span data-ttu-id="3a07d-524">В области добавляется новый шаг.</span><span class="sxs-lookup"><span data-stu-id="3a07d-524">A new step is added in the pane.</span></span> <span data-ttu-id="3a07d-525">Запишите значение в поле **Номер продукта**, поскольку оно потребуется позже.</span><span class="sxs-lookup"><span data-stu-id="3a07d-525">Make a note of the value in the **Product number** field, because you will need it later.</span></span>

    ![Добавлен новый шаг](./media/setup_rsa_tool_93.png)

12. <span data-ttu-id="3a07d-527">Выберите **Редактирование завершено**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-527">Select **Done editing**.</span></span>
13. <span data-ttu-id="3a07d-528">Выберите **Сохраните файл в Lifecycle Services** и свяжите новую запись задачи с той же библиотекой BPM и бизнес-процессом, с которыми была связана оригинальная запись задачи.</span><span class="sxs-lookup"><span data-stu-id="3a07d-528">Select **Save to Lifecycle Services**, and associate the new task recording with the same BPM library and business process that the original task recording was associated with.</span></span> <span data-ttu-id="3a07d-529">Для получения дополнительных сведений см. раздел [Создание записи задачи и сохранение ее в библиотеке BPM](#create-a-task-recording-and-save-it-to-the-bpm-library).</span><span class="sxs-lookup"><span data-stu-id="3a07d-529">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>
14. <span data-ttu-id="3a07d-530">Перейдите к библиотеке BPM и выберите **Синхронизировать тестовые случаи**, чтобы перезаписать запись задачи, прикрепленную к тестовому случаю в Azure DevOps, как описано в разделе [Проверка синхронизации из BPM в Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops).</span><span class="sxs-lookup"><span data-stu-id="3a07d-530">Go to the BPM library, and select **Sync testcases** to overwrite the task recording that is attached to the test case in Azure DevOps, as described in the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>
15. <span data-ttu-id="3a07d-531">Откройте RSAT и выберите пункт **Загрузить**, чтобы перезагрузить все тестовые случаи в наборе тестов.</span><span class="sxs-lookup"><span data-stu-id="3a07d-531">Open RSAT, and select **Load** to reload all the test cases in the test suite.</span></span> <span data-ttu-id="3a07d-532">Необходимо повторно создать автоматизацию и файлы параметров для соответствующего тестового случая путем выбора тестового случая и выбора **Создать \> Создание выполнения теста и файлов параметров**, как описано в разделе [Загрузка и выполнение тестовых случаев](#load-and-run-test-cases).</span><span class="sxs-lookup"><span data-stu-id="3a07d-532">You must regenerate the automation and parameter files for the appropriate test case by selecting the test case and then selecting **New \> Generate Test Execution and Parameter files**, as described in the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3a07d-533">Если файл параметров Excel был оставлен открытым, при повторном создании произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="3a07d-533">If the Excel parameter file was left open, regeneration will fail.</span></span> <span data-ttu-id="3a07d-534">Поэтому перед созданием нового файла параметров Excel убедитесь, что файл параметров Excel для тестового случая закрыт.</span><span class="sxs-lookup"><span data-stu-id="3a07d-534">Therefore, make sure that the Excel parameter file for the test case is closed before you generate the new Excel parameter file.</span></span>

16. <span data-ttu-id="3a07d-535">Выберите **Правка**, чтобы открыть новый файл параметров Excel.</span><span class="sxs-lookup"><span data-stu-id="3a07d-535">Select **Edit** to open the new Excel parameter file.</span></span> <span data-ttu-id="3a07d-536">Будет отображена новая запись **Сохраненная переменная** в строке 9.</span><span class="sxs-lookup"><span data-stu-id="3a07d-536">You will see a new **Saved variable** entry on line 9.</span></span> <span data-ttu-id="3a07d-537">Эта переменная, **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, сохраняется в XML-файле записи задачи и может использоваться в последующих испытаниях.</span><span class="sxs-lookup"><span data-stu-id="3a07d-537">This variable, **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, is saved in the task recording's XML file and can be used in subsequent tests.</span></span>

    ![Запись сохраненной переменной](./media/setup_rsa_tool_94.png)

#### <a name="create-a-new-test-case"></a><span data-ttu-id="3a07d-539">Создание нового тестового случая</span><span class="sxs-lookup"><span data-stu-id="3a07d-539">Create a new test case</span></span>

1. <span data-ttu-id="3a07d-540">Перейти в библиотеку BPM **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-540">Go to the **RSAT** BPM library.</span></span>
2. <span data-ttu-id="3a07d-541">Выберите процесс **Образец вспомогательного бизнес-процесса**, затем в правой части выберите **Режим редактирования**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-541">Select the **Sample Support Business Process** process, and then, on the right, select **Edit mode**.</span></span>
3. <span data-ttu-id="3a07d-542">Измените значение обоих полей **Имя** и **Описание** на **Выпуск продукта**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-542">Change the value of both the **Name** field and the **Description** field to **Release a product**.</span></span> <span data-ttu-id="3a07d-543">Затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-543">Then select **Save**.</span></span>

    ![Имя и описание изменены на "Выпуск продукта"](./media/setup_rsa_tool_95.png)

#### <a name="create-a-new-task-recording-that-has-a-validate-function"></a><span data-ttu-id="3a07d-545">Создание новой записи задачи с функцией проверки</span><span class="sxs-lookup"><span data-stu-id="3a07d-545">Create a new task recording that has a Validate function</span></span>

- <span data-ttu-id="3a07d-546">Создайте запись задачи для выпуска продукта, который был создан ранее, в юридическом лице USRT.</span><span class="sxs-lookup"><span data-stu-id="3a07d-546">Create a task recording to release the product that was created earlier to the USRT legal entity.</span></span> <span data-ttu-id="3a07d-547">Для получения дополнительных сведений см. раздел [Создание записи задачи и сохранение ее в библиотеке BPM](#create-a-task-recording-and-save-it-to-the-bpm-library).</span><span class="sxs-lookup"><span data-stu-id="3a07d-547">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3a07d-548">Для связанных тестовых случаев всегда рекомендуется найти или отфильтровать запись, которая требуется, *вручную введя значение поля*.</span><span class="sxs-lookup"><span data-stu-id="3a07d-548">For chained test cases, we always recommend that you find or filter for the record that you require by *manually typing the value of the field*.</span></span> <span data-ttu-id="3a07d-549">Таким образом, средство может определить запись, с которой действие должно быть выполнено, в последующем тестовом случае.</span><span class="sxs-lookup"><span data-stu-id="3a07d-549">In that way, the tool can determine the record that the action must be taken against in the subsequent test case.</span></span>

    ![Новая запись задачи с функцией проверки](./media/setup_rsa_tool_96.png)

    <span data-ttu-id="3a07d-551">Как показано на предыдущем рисунке, после того, как продукт найден с помощью экспресс-фильтра, но до выбора **Выпуск продуктов**, можно проверить значение поля **Номер продукта**, чтобы убедиться, что код продукта — это код продукта, который был создан ранее.</span><span class="sxs-lookup"><span data-stu-id="3a07d-551">As the preceding illustration shows, after the product is found by using the Quick Filter, but before you select **Release products**, you validate the value of the **Product number** field to make sure that the product ID is the product ID that was created earlier.</span></span> <span data-ttu-id="3a07d-552">Для проверки значения щелкните правой кнопкой мыши поле **Номер продукта**, затем выберите **Регистратор задач \> Проверить \> Текущее значение**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-552">To validate the value, right-click the **Product number** field, and then select **Task recorder \> Validate \> Current Value**.</span></span>

    ![Проверка текущего значения](./media/setup_rsa_tool_97.png)

#### <a name="save-the-task-recording-to-bpm"></a><span data-ttu-id="3a07d-554">Сохранение записи задачи в BPM</span><span class="sxs-lookup"><span data-stu-id="3a07d-554">Save the task recording to BPM</span></span>

1. <span data-ttu-id="3a07d-555">После завершения записи задачи выберите **Сохранить в Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-555">After the task recording is completed, select **Save to Lifecycle Services**.</span></span>

    ![Сохранение завершенной записи задачи в Lifecycle Services](./media/setup_rsa_tool_98.png)

2. <span data-ttu-id="3a07d-557">Сведения о библиотеке загружаются из LCS.</span><span class="sxs-lookup"><span data-stu-id="3a07d-557">Library information is loaded from LCS.</span></span>

    ![Загрузка информации о библиотеке из LCS](./media/setup_rsa_tool_99.png)

3. <span data-ttu-id="3a07d-559">Выберите библиотеку BPM, с которой требуется связать запись задачи.</span><span class="sxs-lookup"><span data-stu-id="3a07d-559">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="3a07d-560">В данном учебнике выберите библиотеку BPM **RSAT**, созданную ранее, и бизнес -процесс **Выпуск продукта** в ней.</span><span class="sxs-lookup"><span data-stu-id="3a07d-560">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Release a product** business process under it.</span></span> <span data-ttu-id="3a07d-561">Затем выберите **OK**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-561">Then select **OK**.</span></span>

#### <a name="sync-bpm-to-azure-devops"></a><span data-ttu-id="3a07d-562">Синхронизация BPM с Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="3a07d-562">Sync BPM to Azure DevOps</span></span>

1. <span data-ttu-id="3a07d-563">Перейдите в библиотеку BPM и откройте библиотеку **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-563">Go to the BPM library, and open the **RSAT** library.</span></span>
2. <span data-ttu-id="3a07d-564">Выберите **Синхронизация VSTS**, затем **Синхронизировать тестовые случаи**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-564">Select **VSTS sync** and then **Sync test cases**.</span></span> <span data-ttu-id="3a07d-565">Дополнительные сведения см. в разделе [Проверка синхронизации из BPM в Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops).</span><span class="sxs-lookup"><span data-stu-id="3a07d-565">For more information, see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>

    <span data-ttu-id="3a07d-566">После завершения синхронизации новый рабочий элемент и соответствующий ему тестовый случай для бизнес-процесса **Выпуск продукта** отображаются в Azure DevOps в разделе **Панели \> Рабочие элементы**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-566">After the synchronization is completed, the new work item and the corresponding test case for the **Release a product** business process appear in Azure DevOps at **Boards \> Work Items**.</span></span>

#### <a name="add-the-new-test-case-to-the-existing-test-suite"></a><span data-ttu-id="3a07d-567">Добавление нового тестового случая в существующий набор тестов</span><span class="sxs-lookup"><span data-stu-id="3a07d-567">Add the new test case to the existing test suite</span></span>

1. <span data-ttu-id="3a07d-568">Перейдите в раздел **Планы испытаний \> Планы испытаний** и выберите область **План испытаний RSAT**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-568">Go to **Test plans \> Test plans**, and select the **RSAT Test Plan** plan.</span></span>
2. <span data-ttu-id="3a07d-569">Выберите **Добавить существующий**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-569">Select **Add existing**.</span></span>
3. <span data-ttu-id="3a07d-570">На странице **Добавление тестовых случаев в набор** выберите **Выполнить запрос**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-570">On the **Add test cases to suite** page, select **Run query**.</span></span>
4. <span data-ttu-id="3a07d-571">Выберите новый тестовый случай, который был создан для процесса **Выпуск продукта**, затем выберите **Добавить тестовые случаи** в нижнем правом углу страницы (эта кнопка не отображается на следующем рисунке).</span><span class="sxs-lookup"><span data-stu-id="3a07d-571">Select the new test case that was created for **Release a product**, and then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![Страница добавления тестовых случаев в набор](./media/setup_rsa_tool_100.png)

    <span data-ttu-id="3a07d-573">Теперь набор тестов включает два тестовых случая.</span><span class="sxs-lookup"><span data-stu-id="3a07d-573">The test suite now has two test cases.</span></span>

    ![Два тестовых случая в наборе тестов.](./media/setup_rsa_tool_101.png)

#### <a name="load-test-cases-into-rsat"></a><span data-ttu-id="3a07d-575">Загрузка тестовых случаев в RSAT</span><span class="sxs-lookup"><span data-stu-id="3a07d-575">Load test cases into RSAT</span></span>

1. <span data-ttu-id="3a07d-576">Откройте RSAT и выберите команду **Загрузить**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-576">Open RSAT, and select **Load**.</span></span>
2. <span data-ttu-id="3a07d-577">После загрузки тестовых случаев выводится предупреждение "Это действие приведет к перезаписи файлов тестовых данных Excel, локальные изменения будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="3a07d-577">The test cases are loaded, and you receive a warning that states, "This action will overwrite Excel test data files, local changes will be lost.</span></span> <span data-ttu-id="3a07d-578">Продолжить?"</span><span class="sxs-lookup"><span data-stu-id="3a07d-578">Do you want to proceed?"</span></span> <span data-ttu-id="3a07d-579">Выберите **Да** для обновления файлов параметров Excel в локальной системе, но не файлов параметров Excel, которые были отправлены в Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="3a07d-579">Select **Yes** to update the Excel parameter files in the local system but not the Excel parameter files that were uploaded to Azure DevOps.</span></span>

    ![Это действие приведет к перезаписи файлов тестовых данных Excel](./media/setup_rsa_tool_102.png)

    <span data-ttu-id="3a07d-581">Загружаются оба тестовых случая вместе с файлом параметров Excel для первого тестового случая.</span><span class="sxs-lookup"><span data-stu-id="3a07d-581">Both the test cases are loaded, together with the Excel parameter file for the first test case.</span></span> <span data-ttu-id="3a07d-582">Поскольку при последнем выполнении было выбрано значение **Отправить**, файлы параметров извлекаются из Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="3a07d-582">Because you selected **Upload** in the last run, the parameter files are pulled from Azure DevOps.</span></span>

    ![Загруженные тестовые случаи](./media/setup_rsa_tool_103.png)

3. <span data-ttu-id="3a07d-584">Выберите только второй тестовый случай, затем выберите **Создать \> Создание выполнения теста и файлов параметров**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-584">Select only the second test case, and then select **New \> Generate test execution and parameter files**.</span></span>

#### <a name="edit-the-excel-parameter-file"></a><span data-ttu-id="3a07d-585">Правка файла параметров Excel</span><span class="sxs-lookup"><span data-stu-id="3a07d-585">Edit the Excel parameter file</span></span>

1. <span data-ttu-id="3a07d-586">Выберите только второй тестовый случай, затем выберите **Правка**, чтобы открыть соответствующий файл параметров Excel.</span><span class="sxs-lookup"><span data-stu-id="3a07d-586">Select only the second test case, and then select **Edit** to open the corresponding Excel parameter file.</span></span>
2. <span data-ttu-id="3a07d-587">Скопируйте сохраненную переменную **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** (см. раздел [Изменение существующей записи задачи для создания сохраненной переменной](#modify-an-existing-task-recording-to-create-a-saved-variable)) из первого тестового случая во все поля, в которых используется номер продукта.</span><span class="sxs-lookup"><span data-stu-id="3a07d-587">Copy the **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** saved variable (see the [Modify an existing task recording to create a saved variable](#modify-an-existing-task-recording-to-create-a-saved-variable) section) from the first test case into all the fields where the product number is used.</span></span> <span data-ttu-id="3a07d-588">В этом случае переменная копируется в поля **Номер продукта** и **Проверьте номер продукта** на листе **EcoResProductListPage**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-588">In this case, you copy the variable into the **Product number** and **Validate Product number** fields on the **EcoResProductListPage** sheet.</span></span>

    ![Поля "Номер продукта" и "Проверьте номер продукта"](./media/setup_rsa_tool_104.png)

    > [!NOTE]
    > <span data-ttu-id="3a07d-590">Переменные могут передаваться между проверками только в ходе одного тестового запуска.</span><span class="sxs-lookup"><span data-stu-id="3a07d-590">Variables can be passed between tests only during the same test run.</span></span> <span data-ttu-id="3a07d-591">Имена переменных должны точно совпадать.</span><span class="sxs-lookup"><span data-stu-id="3a07d-591">The names of the variables must match exactly.</span></span>

3. <span data-ttu-id="3a07d-592">Выберите **Сохранить** и закройте книгу Excel.</span><span class="sxs-lookup"><span data-stu-id="3a07d-592">Select **Save**, and then close the Excel workbook.</span></span>
4. <span data-ttu-id="3a07d-593">Выберите **Отправить**, чтобы сохранить изменения, внесенные в файл параметров Excel.</span><span class="sxs-lookup"><span data-stu-id="3a07d-593">Select **Upload** to save the changes that you made to the Excel parameter file.</span></span>

#### <a name="run-the-chained-test-cases"></a><span data-ttu-id="3a07d-594">Выполнение связанных тестовых случаев</span><span class="sxs-lookup"><span data-stu-id="3a07d-594">Run the chained test cases</span></span>

1. <span data-ttu-id="3a07d-595">Выберите оба тестовых случая, затем выберите **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="3a07d-595">Select both the test cases, and then select **Run**.</span></span>
2. <span data-ttu-id="3a07d-596">Убедитесь, что оба тестовых случая прошли успешно.</span><span class="sxs-lookup"><span data-stu-id="3a07d-596">Verify that both test cases have passed.</span></span>

    ![Поле "Результат" со значением успешного прохождения для обоих тестовых случаев](./media/setup_rsa_tool_105.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]