---
title: Regulatory Configuration Service (RCS) — функции глобализации
description: В этом разделе объясняется, как использовать Microsoft Regulatory Configuration Service (RCS) и глобальный репозиторий для создания и использования функций глобализации.
author: JaneA07
manager: AnnBe
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RCS, RCSWorkspace, e-Invoicing service
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: b701e6bfa14ac30e02bfe79666963db4ee657302
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5002803"
---
# <a name="regulatory-configuration-services-rcs---globalization-features"></a><span data-ttu-id="7570a-103">Regulatory Configuration Service (RCS) — функции глобализации</span><span class="sxs-lookup"><span data-stu-id="7570a-103">Regulatory Configuration Services (RCS) - Globalization features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7570a-104">Для создания функции глобализации, которая может использоваться в службах глобализации, например в службе электронных накладных, можно использовать Microsoft Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="7570a-104">You can use Microsoft Regulatory Configuration Services (RCS) to create a Globalization feature that can be used in Globalization services, such as an e-invoicing service.</span></span> <span data-ttu-id="7570a-105">RCS позволяет выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="7570a-105">RCS lets you perform these tasks:</span></span>

- <span data-ttu-id="7570a-106">Определение связанных компонентов функции.</span><span class="sxs-lookup"><span data-stu-id="7570a-106">Define related components of a feature.</span></span>
- <span data-ttu-id="7570a-107">Управление жизненным циклом функции с помощью статуса функции.</span><span class="sxs-lookup"><span data-stu-id="7570a-107">Manage the feature lifecycle through a feature's status.</span></span>
- <span data-ttu-id="7570a-108">Сделать функцию доступной для указанных сред.</span><span class="sxs-lookup"><span data-stu-id="7570a-108">Make a feature available for defined environments.</span></span>
- <span data-ttu-id="7570a-109">Совместное использование функции с другими организациями.</span><span class="sxs-lookup"><span data-stu-id="7570a-109">Share a feature with other organizations.</span></span>

<span data-ttu-id="7570a-110">Следующие процедуры показывают, как пользователь в RCS может добавить функцию глобализации и связанные компоненты, обновить статус функции и сделать функцию доступной, чтобы ее можно было использовать в службах глобализации.</span><span class="sxs-lookup"><span data-stu-id="7570a-110">The following procedures explain how a user in RCS can add a Globalization feature and related components, update the feature's status, and make the feature available so that it can be used in Globalization services.</span></span>

<span data-ttu-id="7570a-111">Перед выполнением процедур необходимо выполнить шаги, которые относятся к следующим задачам:</span><span class="sxs-lookup"><span data-stu-id="7570a-111">Before you complete the procedures, you must complete the steps that are related to the following tasks:</span></span>

- <span data-ttu-id="7570a-112">Доступ к экземпляру RCS.</span><span class="sxs-lookup"><span data-stu-id="7570a-112">Accessing an RCS instance.</span></span>
- <span data-ttu-id="7570a-113">Создание и активация поставщика конфигураций.</span><span class="sxs-lookup"><span data-stu-id="7570a-113">Creating and activating a configuration provider.</span></span> <span data-ttu-id="7570a-114">Дополнительные сведения см. в [Создание поставщиков конфигураций и пометка их как активных](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="7570a-114">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="7570a-115">В экземпляре приложений Finance and Operations выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7570a-115">In your Finance and Operations apps instance, follow these steps.</span></span>

1. <span data-ttu-id="7570a-116">Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="7570a-116">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7570a-117">Если у вашей компании нет среды RCS, щелкните **Regulatory Services — конфигурация** и следуйте инструкциям по подготовке среды.</span><span class="sxs-lookup"><span data-stu-id="7570a-117">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration**, and follow the instructions to provision one.</span></span>

> [!NOTE]
> <span data-ttu-id="7570a-118">Если среда RCS уже подготовлена для вашей компании, воспользуйтесь URL-адресом страницы для доступа к ней, выбрав параметр входа.</span><span class="sxs-lookup"><span data-stu-id="7570a-118">If an RCS environment has already been provisioned for your company, use the page URL to access the environment by selecting the sign-in option.</span></span>

## <a name="turn-on-the-globalization-features"></a><span data-ttu-id="7570a-119">Включение функций глобализации</span><span class="sxs-lookup"><span data-stu-id="7570a-119">Turn on the Globalization features</span></span>

1. <span data-ttu-id="7570a-120">В экземпляре RCS выберите плитку **Управление функциями**.</span><span class="sxs-lookup"><span data-stu-id="7570a-120">In your RCS instance, select the **Feature management** tile.</span></span>
2. <span data-ttu-id="7570a-121">В рабочей области **Управление функциями** выберите **Функции глобализации** в списке и выберите **Включить**.</span><span class="sxs-lookup"><span data-stu-id="7570a-121">In the **Feature management** workspace, select **Globalization features** in the list, and then select **Enable now**.</span></span>

    ![Функции глобализации в управлении функциями](./media/RCS_GlobalF_1%20Feature%20mgmt.JPG)

## <a name="globalization-features"></a><span data-ttu-id="7570a-123">Функции глобализации</span><span class="sxs-lookup"><span data-stu-id="7570a-123">Globalization features</span></span>

<span data-ttu-id="7570a-124">Чтобы использовать функцию глобализации, необходимо сначала импортировать ее из глобального репозитория и создать для нее свою собственную версию.</span><span class="sxs-lookup"><span data-stu-id="7570a-124">To use a Globalization feature, you must first import it from the the Global repository and create your own version of it.</span></span> <span data-ttu-id="7570a-125">Есть два способа добавления функций глобализации:</span><span class="sxs-lookup"><span data-stu-id="7570a-125">There are two ways to add Globalization features:</span></span>

- <span data-ttu-id="7570a-126">Добавление производной функции, основанной на существующей функции, которая была опубликована или передана в общий доступ.</span><span class="sxs-lookup"><span data-stu-id="7570a-126">Add a derived feature that is based on an existing feature that has been published or shared.</span></span>
- <span data-ttu-id="7570a-127">Добавление новой функции, созданной с нуля.</span><span class="sxs-lookup"><span data-stu-id="7570a-127">Add a new feature that you've created from scratch.</span></span>

## <a name="access-globalization-features"></a><span data-ttu-id="7570a-128">Доступ к функциям глобализации</span><span class="sxs-lookup"><span data-stu-id="7570a-128">Access Globalization features</span></span>

1. <span data-ttu-id="7570a-129">Убедитесь, что функция **Функции глобализации** в модуле "Управление функциями" включена, как описано ранее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="7570a-129">Make sure that the **Globalization features** feature is turned on in Feature management, as described earlier in this topic.</span></span>
2. <span data-ttu-id="7570a-130">Откройте новую рабочую область **Функции глобализации**, а затем в разделе **Функции** выберите плитку **Электронные накладные**.</span><span class="sxs-lookup"><span data-stu-id="7570a-130">Open the new **Globalization Features** workspace, and then, under **Features**, select the **e-Invoicing** tile.</span></span>

    ![Рабочая область глобальных функций](./media/RCS_GlobalF_2%20Feature%20wrkspace.JPG)

    <span data-ttu-id="7570a-132">Открывается страница **Функции электронных накладных**.</span><span class="sxs-lookup"><span data-stu-id="7570a-132">The **e-Invoicing Features** page is opened.</span></span>

    ![Страница функций электронных накладных](./media/RCS_GlobalF_3%20Feature%20form.JPG)

## <a name="add-a-derived-globalization-feature"></a><span data-ttu-id="7570a-134">Добавление производной функции глобализации</span><span class="sxs-lookup"><span data-stu-id="7570a-134">Add a derived Globalization feature</span></span>

<span data-ttu-id="7570a-135">Можно добавить новую функцию глобализации, создав производную от нее функцию, которая была опубликована или передана в общий доступ.</span><span class="sxs-lookup"><span data-stu-id="7570a-135">You can add a new Globalization feature by deriving it from an existing feature that has been published or shared.</span></span>

1. <span data-ttu-id="7570a-136">Выберите **Импорт**, чтобы открыть страницу **Импорт функции из глобального репозитория**.</span><span class="sxs-lookup"><span data-stu-id="7570a-136">Select **Import** to open the **Import feature from Global repository** page.</span></span>

    ![Страница импорта функции из глобального репозитория](./media/RCS_GlobalF_4%20Feature%20import%20form%20GR.JPG)

2. <span data-ttu-id="7570a-138">Выберите **Синхронизировать** для получения последних функций.</span><span class="sxs-lookup"><span data-stu-id="7570a-138">Select **Synchronize** to get the latest features.</span></span>

    <span data-ttu-id="7570a-139">В синхронизированном списке указаны доступные для пользователя функции, поскольку они были опубликованы корпорацией Майкрософт или для них был открыт общий доступ другим поставщиком конфигураций.</span><span class="sxs-lookup"><span data-stu-id="7570a-139">The synced list includes features that are available to you either because they were published by Microsoft or because they were shared with you by another configuration provider.</span></span>

    ![Синхронизированный список функций](./media/RCS_GlobalF_5%20Feature%20GR%20sync.JPG)

3. <span data-ttu-id="7570a-141">В списке выберите функции для импортирования, а затем выберите **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="7570a-141">In the list, select the features to import, and then select **Import**.</span></span> <span data-ttu-id="7570a-142">При успешном импорте выбранных функций появится сообщение.</span><span class="sxs-lookup"><span data-stu-id="7570a-142">You receive a message when the selected features have been successfully imported.</span></span>

    ![Сообщение об успешном импорте](./media/RCS_GlobalF_6%20Feature%20GR%20import%20success.JPG)

4. <span data-ttu-id="7570a-144">Выберите **Добавить**, а затем в раскрывающемся диалоговом окне выберите **На основе существующей версии**.</span><span class="sxs-lookup"><span data-stu-id="7570a-144">Select **Add**, and then, in the drop-down dialog box, select the **Based on existing version** option.</span></span>
5. <span data-ttu-id="7570a-145">Введите имя и описание для функции.</span><span class="sxs-lookup"><span data-stu-id="7570a-145">Enter a name and description for the feature.</span></span>
6. <span data-ttu-id="7570a-146">В списке доступных функций выберите базовую версию функции, а затем выберите **Создать функцию**.</span><span class="sxs-lookup"><span data-stu-id="7570a-146">In the list of available features, select the base version of the feature, and then select **Create feature**.</span></span>

    ![Добавление производной функции](./media/RCS_GlobalF_7%20Feature%20create%20derived.JPG)

    <span data-ttu-id="7570a-148">Добавленная функция создается, ей присваивается статус **Черновик**.</span><span class="sxs-lookup"><span data-stu-id="7570a-148">The feature that you added is created and has a status of **Draft**.</span></span>

    ![Производная функция со статусом "Черновик"](./media/RCS_GlobalF_8%20Feature%20draft%20create.JPG)

7. <span data-ttu-id="7570a-150">Просмотрите компоненты функций, чтобы определить, требуются ли обновления:</span><span class="sxs-lookup"><span data-stu-id="7570a-150">Review the feature components to determine whether updates are required:</span></span>

    - <span data-ttu-id="7570a-151">Просмотрите конфигурации, в случае необходимости настройки форматов электронной отчетности (ER) и их привязки к сопоставлениям форматов для версии функции.</span><span class="sxs-lookup"><span data-stu-id="7570a-151">Review the configurations, in case you need to customize the Electronic reporting (ER) formats and their binding with format mappings for the feature version.</span></span>
    - <span data-ttu-id="7570a-152">Просмотрите настройки, если необходимо настроить вкладку **Действия**, **Правила применимости** или **Переменные** для версии функции.</span><span class="sxs-lookup"><span data-stu-id="7570a-152">Review the setup, in case you need to customize the **Actions** tab, **Applicability rules** tab, or **Variables** tab for the feature version.</span></span>

8. <span data-ttu-id="7570a-153">На вкладке **Версии** выберите дату **Действует с** и введите описание, если поле **Описание** пустое.</span><span class="sxs-lookup"><span data-stu-id="7570a-153">On the **Versions** tab, select an **Effective from** date, and enter a description if the **Description** field is blank.</span></span>
9. <span data-ttu-id="7570a-154">Выберите **Изменить статус** для завершения функции.</span><span class="sxs-lookup"><span data-stu-id="7570a-154">Select **Change status** to complete the feature.</span></span> <span data-ttu-id="7570a-155">Выполненные функции могут быть доступны для определенной среды, чтобы их можно было использовать в службах глобализации, либо они могут быть опубликованы в глобальном репозитории.</span><span class="sxs-lookup"><span data-stu-id="7570a-155">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="7570a-156">Функции со значением **Статус версии функции** — **Опубликовано** могут использоваться совместно с внешними организациями.</span><span class="sxs-lookup"><span data-stu-id="7570a-156">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="add-a-new-globalization-feature"></a><span data-ttu-id="7570a-157">Добавление новой функции глобализации</span><span class="sxs-lookup"><span data-stu-id="7570a-157">Add a new Globalization feature</span></span>

<span data-ttu-id="7570a-158">Можно добавить новую функцию глобализации, создав ее с нуля.</span><span class="sxs-lookup"><span data-stu-id="7570a-158">You can add a new Globalization feature by creating it from scratch.</span></span>

1. <span data-ttu-id="7570a-159">На странице **Импорт функции из глобального репозитория** выберите **Добавить**, а затем в раскрывающемся диалоговом окне выберите параметр **Создать функцию**.</span><span class="sxs-lookup"><span data-stu-id="7570a-159">On the **Import feature from Global repository** page, select **Add**, and then, in the drop-down dialog box, select the **New feature** option.</span></span>
2. <span data-ttu-id="7570a-160">Введите имя и описание для функции.</span><span class="sxs-lookup"><span data-stu-id="7570a-160">Enter a name and description for the feature.</span></span>
3. <span data-ttu-id="7570a-161">Выберите **создать функцию**.</span><span class="sxs-lookup"><span data-stu-id="7570a-161">Select **Create feature**.</span></span>

    ![Добавление новой функции](./media/RCS_GlobalF_9%20Feature%20create%20new.JPG)

4. <span data-ttu-id="7570a-163">На вкладке **Версии** выберите дату **Действует с**, а затем выберите **Изменить статус**, чтобы завершить функцию.</span><span class="sxs-lookup"><span data-stu-id="7570a-163">On the **Versions** tab, select an **Effective from** date, and then select **Change status** to complete the feature.</span></span> <span data-ttu-id="7570a-164">Выполненные функции могут быть доступны для определенной среды, чтобы их можно было использовать в службах глобализации, либо они могут быть опубликованы в глобальном репозитории.</span><span class="sxs-lookup"><span data-stu-id="7570a-164">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="7570a-165">Функции со значением **Статус версии функции** — **Опубликовано** могут использоваться совместно с внешними организациями.</span><span class="sxs-lookup"><span data-stu-id="7570a-165">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="feature-component-overview"></a><span data-ttu-id="7570a-166">Обзор компонентов функций</span><span class="sxs-lookup"><span data-stu-id="7570a-166">Feature component overview</span></span>

<span data-ttu-id="7570a-167">Для функций глобализации есть следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="7570a-167">Globalization features have several components:</span></span>

- <span data-ttu-id="7570a-168">**Версия** — этот компонент поддерживает управление жизненным циклом функции и позволяет пользователям управлять статусом для разных версий функции.</span><span class="sxs-lookup"><span data-stu-id="7570a-168">**Version** – This component supports feature lifecycle management and lets users manage the status for different versions of the feature.</span></span>
- <span data-ttu-id="7570a-169">**Конфигурации** — этот компонент позволяет пользователям управлять, просматривать и изменять соответствующие форматы электронной отчетности и сопоставления форматов.</span><span class="sxs-lookup"><span data-stu-id="7570a-169">**Configurations** – This component lets users manage, view, and edit related ER formats and format mappings.</span></span>
- <span data-ttu-id="7570a-170">**Настройки** — этот компонент позволяет пользователям служб глобализации, например службы электронных накладных, управлять настройкой связанной версии функции.</span><span class="sxs-lookup"><span data-stu-id="7570a-170">**Setups** – This component lets users of Globalization services, such as an e-invoicing service, manage the setup of the related feature version.</span></span> <span data-ttu-id="7570a-171">Таким образом, он поддерживает гибкое создание правил обмена данными и реакции.</span><span class="sxs-lookup"><span data-stu-id="7570a-171">Therefore, it supports the flexible construction of communication and responses rules.</span></span>
- <span data-ttu-id="7570a-172">**Среда** — этот компонент позволяет пользователям служб глобализации, например службы электронных накладных, управлять средой, в которой используется настройка версии функций, и предоставлять авторизацию пользователям, которые будут иметь к ней доступ.</span><span class="sxs-lookup"><span data-stu-id="7570a-172">**Environment** – This component lets users of Globalization services, such as an e-invoicing service, manage the environment where the feature version setup is used and grant authorization to the users who will have access to it.</span></span>
- <span data-ttu-id="7570a-173">**Организации** — этот компонент позволяет пользователям использовать функцию совместно с внешними организациями.</span><span class="sxs-lookup"><span data-stu-id="7570a-173">**Organizations** – This component lets users to share the feature with external organizations.</span></span>

## <a name="configuring-feature-components"></a><span data-ttu-id="7570a-174">Настройка компонентов функций</span><span class="sxs-lookup"><span data-stu-id="7570a-174">Configuring feature components</span></span>

### <a name="version-and-status"></a><span data-ttu-id="7570a-175">Версия и статус</span><span class="sxs-lookup"><span data-stu-id="7570a-175">Version and status</span></span>

<span data-ttu-id="7570a-176">Версия используется для управления жизненным циклом функции глобализации.</span><span class="sxs-lookup"><span data-stu-id="7570a-176">The version is used to manage the Globalization feature lifecycle.</span></span>

<span data-ttu-id="7570a-177">Статус можно изменить в поле **Статус** на вкладке **Версия**. Доступны следующие статусы:</span><span class="sxs-lookup"><span data-stu-id="7570a-177">The status can be changed in the **Status** field on the **Version** tab. The following statuses are available:</span></span>

- <span data-ttu-id="7570a-178">**Черновик** — функция может быть изменена только в том случае, если у нее есть этот статус.</span><span class="sxs-lookup"><span data-stu-id="7570a-178">**Draft** – The feature can be edited only when it's in this status.</span></span>
- <span data-ttu-id="7570a-179">**Завершено** — функция и все связанные компоненты были завершены и не могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="7570a-179">**Complete** – The feature and all related components have been finalized (completed) and can't be edited.</span></span>
- <span data-ttu-id="7570a-180">**Опубликовано** — функция и все связанные компоненты были опубликованы в глобальном репозитории.</span><span class="sxs-lookup"><span data-stu-id="7570a-180">**Published** – The feature and all related components have been published to the Global repository.</span></span>
- <span data-ttu-id="7570a-181">**Общий** — функция и все связанные компоненты являются общими для внешних организаций.</span><span class="sxs-lookup"><span data-stu-id="7570a-181">**Shared** – The feature and all related components have been shared with external organizations.</span></span>
- <span data-ttu-id="7570a-182">**Включено** — функция и все связанные компоненты включены для использования в службе глобализации, такой как служба электронных накладных.</span><span class="sxs-lookup"><span data-stu-id="7570a-182">**Enabled** – The feature and all related components have been enabled for use in a Globalization service, such as an e-invoicing service.</span></span>

> [!NOTE]
> <span data-ttu-id="7570a-183">Для функций должны последовательно изменяться некоторые статусы.</span><span class="sxs-lookup"><span data-stu-id="7570a-183">Features must move sequentially through some of these statuses.</span></span> <span data-ttu-id="7570a-184">Таким образом, не все статусы могут быть доступны на каждом этапе жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="7570a-184">Therefore, not every status might be available at every lifecycle stage.</span></span>

### <a name="configurations"></a><span data-ttu-id="7570a-185">Конфигурации</span><span class="sxs-lookup"><span data-stu-id="7570a-185">Configurations</span></span>

<span data-ttu-id="7570a-186">Для конфигураций доступны следующие действия:</span><span class="sxs-lookup"><span data-stu-id="7570a-186">The following actions are available for configurations:</span></span>

- <span data-ttu-id="7570a-187">**Просмотреть** — просмотр основных конфигураций функций, которые не требуют обновления.</span><span class="sxs-lookup"><span data-stu-id="7570a-187">**View** – View the underlying feature configurations that don't require any update.</span></span>
- <span data-ttu-id="7570a-188">**Изменить** — создание черновой версии выбранной конфигурации, чтобы можно было редактировать формат или сопоставление форматов в конструкторе форматов.</span><span class="sxs-lookup"><span data-stu-id="7570a-188">**Edit** – Create a draft version of a selected configuration so that you can edit the format or format mapping in the Format designer.</span></span>
- <span data-ttu-id="7570a-189">**Удалить** — удаление выбранной конфигурации из функции.</span><span class="sxs-lookup"><span data-stu-id="7570a-189">**Delete** – Delete a selected configuration from the feature.</span></span>
- <span data-ttu-id="7570a-190">**Повторно разместить** — повторно разместить функцию.</span><span class="sxs-lookup"><span data-stu-id="7570a-190">**Rebase** – Rebase the feature.</span></span> <span data-ttu-id="7570a-191">Дополнительные сведения см. в разделе [Повторно разместить функции глобализации](#rebase) далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="7570a-191">For more information, see the [Rebase derived Globalization features](#rebase) section later in this topic.</span></span>

### <a name="setups"></a><span data-ttu-id="7570a-192">Настройки</span><span class="sxs-lookup"><span data-stu-id="7570a-192">Setups</span></span>

<span data-ttu-id="7570a-193">Для настроек функций доступны следующие действия:</span><span class="sxs-lookup"><span data-stu-id="7570a-193">The following actions are available for feature setups:</span></span>

- <span data-ttu-id="7570a-194">**Добавить** — создание новой настройки функции.</span><span class="sxs-lookup"><span data-stu-id="7570a-194">**Add** – Create a new feature setup.</span></span> <span data-ttu-id="7570a-195">Эта настройка функций может быть производной из существующей настройки функции или создана с нуля.</span><span class="sxs-lookup"><span data-stu-id="7570a-195">This feature setup can be derived from an existing feature setup or created from scratch.</span></span>
- <span data-ttu-id="7570a-196">**Удалить** — удаление выбранной настройки функции.</span><span class="sxs-lookup"><span data-stu-id="7570a-196">**Delete** – Delete a selected feature setup.</span></span>
- <span data-ttu-id="7570a-197">**Просмотреть** — просмотр базовой настройки функции, которая не требует каких-либо изменений.</span><span class="sxs-lookup"><span data-stu-id="7570a-197">**View** – View an underlying feature setup that doesn't require any changes.</span></span>
- <span data-ttu-id="7570a-198">**Изменить** — создание, удаление или изменение атрибутов трех основных компонентов настройки функции:</span><span class="sxs-lookup"><span data-stu-id="7570a-198">**Edit** – Create, delete, or modify the attributes of the three main components of a feature setup:</span></span>

    - <span data-ttu-id="7570a-199">Действия и их параметры</span><span class="sxs-lookup"><span data-stu-id="7570a-199">Actions and their parameters</span></span>
    - <span data-ttu-id="7570a-200">Правила применимости</span><span class="sxs-lookup"><span data-stu-id="7570a-200">Applicability rules</span></span>
    - <span data-ttu-id="7570a-201">Переменные</span><span class="sxs-lookup"><span data-stu-id="7570a-201">Variables</span></span>

![Страница настройки версии функции](./media/RCS_GlobalF_10%20Feature%20set%20up.JPG)

### <a name="environments"></a><span data-ttu-id="7570a-203">Среды</span><span class="sxs-lookup"><span data-stu-id="7570a-203">Environments</span></span>

<span data-ttu-id="7570a-204">Для среды доступны следующие действия:</span><span class="sxs-lookup"><span data-stu-id="7570a-204">The following actions are available for environments:</span></span>

- <span data-ttu-id="7570a-205">**Включить** — для выбранной версии функции выберите опубликованную среду и выберите дату **Действует с**, когда она должна быть доступна.</span><span class="sxs-lookup"><span data-stu-id="7570a-205">**Enable** – For a selected feature version, select a published environment, and select an **Effective from** date when it should be available.</span></span> <span data-ttu-id="7570a-206">Дополнительные сведения см. в разделе [Настройка сред для включения](#configureenvironment) далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="7570a-206">For more information, see the [Configure environments for enablement](#configureenvironment) section later in this topic.</span></span>
- <span data-ttu-id="7570a-207">**Отмена** — удаление среды для настройки функции.</span><span class="sxs-lookup"><span data-stu-id="7570a-207">**Cancel** – Remove an environment for a feature setup.</span></span>

### <a name="organizations"></a><span data-ttu-id="7570a-208">Организации</span><span class="sxs-lookup"><span data-stu-id="7570a-208">Organizations</span></span>

<span data-ttu-id="7570a-209">Выполните следующие действия, чтобы совместно использовать функцию глобализации с внешней организацией.</span><span class="sxs-lookup"><span data-stu-id="7570a-209">Follow these steps to share a Globalization feature with an external organization.</span></span>

1. <span data-ttu-id="7570a-210">На странице **Функции электронных накладных** выберите функцию и версию функции для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="7570a-210">On the **e-Invoicing features** page, select the feature and the feature version to share.</span></span>
2. <span data-ttu-id="7570a-211">На вкладке **Организации** выберите **Поделиться**, а затем в раскрывающемся диалоговом окне введите имя домена организации.</span><span class="sxs-lookup"><span data-stu-id="7570a-211">On the **Organizations** tab, select **Share with**, and then, in the drop-down dialog box, enter the organization's domain name.</span></span>
3. <span data-ttu-id="7570a-212">Выберите **Поделиться**.</span><span class="sxs-lookup"><span data-stu-id="7570a-212">Select **Share**.</span></span>

    ![Совместное использование функции с организацией](./media/RCS_GlobalF_20%20Feature%20orgn_share%20with.JPG)

<span data-ttu-id="7570a-214">Функция используется совместно с выбранной организацией и доступна для данной организации в глобальном репозитории.</span><span class="sxs-lookup"><span data-stu-id="7570a-214">The feature is shared with the selected organization and is available for that organization in the Global repository.</span></span> <span data-ttu-id="7570a-215">После этого эту функцию можно импортировать в экземпляр RCS организации Dynamics 365 Finance, чтобы ее можно было использовать.</span><span class="sxs-lookup"><span data-stu-id="7570a-215">From there, the feature can be imported into the organization's instance of RCS or Dynamics 365 Finance so that it can be used.</span></span>

## <a name="rebase-derived-globalization-features"></a><a name="rebase"></a><span data-ttu-id="7570a-216">Повторное размещение производных функций глобализации</span><span class="sxs-lookup"><span data-stu-id="7570a-216">Rebase derived Globalization features</span></span>

<span data-ttu-id="7570a-217">Производную функцию глобализации можно повторно изменить в новой или обновленной базовой версии функции.</span><span class="sxs-lookup"><span data-stu-id="7570a-217">You can rebase a derived Globalization feature to the new or updated base feature version.</span></span> <span data-ttu-id="7570a-218">Таким образом, изменения, произошедшие в базовой версии, могут быть автоматически обновлены.</span><span class="sxs-lookup"><span data-stu-id="7570a-218">In this way, changes that have occurred in the base version can be automatically updated.</span></span> <span data-ttu-id="7570a-219">Обновленная базовая версия функции создается поставщиком исходной конфигурации и затем публикуется или совместно используется.</span><span class="sxs-lookup"><span data-stu-id="7570a-219">The updated base feature version is created by the originating configuration provider, and it's then published or shared.</span></span>

![Обновленная базовая версия функции](./media/RCS_GlobalF_12%20Feature%20new%20version.JPG)

<span data-ttu-id="7570a-221">Например, если необходимо повторно разместить производную версию созданной функции, сначала нужно получить последнюю версию функции, импортировав ее из глобального репозитория.</span><span class="sxs-lookup"><span data-stu-id="7570a-221">For example, if you want to rebase the derived version of a feature that you created, you first get the latest version of the feature by importing it from the Global repository.</span></span>

1. <span data-ttu-id="7570a-222">На странице **Функции электронных накладных** выберите **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="7570a-222">On the **e-Invoicing features** page, select **Import**.</span></span>
2. <span data-ttu-id="7570a-223">Выберите **Синхронизировать** для получения последних функций.</span><span class="sxs-lookup"><span data-stu-id="7570a-223">Select **Synchronize** to get the latest features.</span></span>
3. <span data-ttu-id="7570a-224">В списке функций выберите функции для импортирования, а затем выберите **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="7570a-224">In the list of features, select the features to import, and then select **Import**.</span></span>

    ![Импорт последней версии функции](./media/RCS_GlobalF_13%20Feature%20new%20version%20import.JPG)

4. <span data-ttu-id="7570a-226">В списке функций выберите функцию для повторного размещения.</span><span class="sxs-lookup"><span data-stu-id="7570a-226">In the list of features, select the feature to rebase.</span></span>
5. <span data-ttu-id="7570a-227">На вкладке **Версия** выберите **Создать**, чтобы создать черновую версию.</span><span class="sxs-lookup"><span data-stu-id="7570a-227">On the **Version** tab, select **New** to create a draft version.</span></span>

    ![Создана новая черновая версия](./media/RCS_GlobalF_14%20Feature%20new%20base%20version.JPG)

6. <span data-ttu-id="7570a-229">Выберите **Повторно разместить**.</span><span class="sxs-lookup"><span data-stu-id="7570a-229">Select **Rebase**.</span></span>
7. <span data-ttu-id="7570a-230">В диалоговом окне **Повторно разместить** выберите последнюю версию функции, куда следует выполнить повторное размещение.</span><span class="sxs-lookup"><span data-stu-id="7570a-230">In the **Rebase** dialog box, select the latest version of the feature to rebase to.</span></span>

    ![Диалоговое окно повторного размещения](./media/RCS_GlobalF_15%20Feature%20rebase%20version.JPG)

8. <span data-ttu-id="7570a-232">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="7570a-232">Select **OK**.</span></span>
9. <span data-ttu-id="7570a-233">Просмотрите компоненты функции и внесите необходимые изменения.</span><span class="sxs-lookup"><span data-stu-id="7570a-233">Review the feature components, and make any changes that are required.</span></span>
10. <span data-ttu-id="7570a-234">Выберите **Изменить статус** для завершения повторного размещения функции.</span><span class="sxs-lookup"><span data-stu-id="7570a-234">Select **Change status** to complete the rebased feature.</span></span> <span data-ttu-id="7570a-235">После завершения повторного размещения можно выполнить дополнительные действия.</span><span class="sxs-lookup"><span data-stu-id="7570a-235">When the rebase is completed, you can perform additional actions.</span></span> <span data-ttu-id="7570a-236">Например, можно опубликовать функцию и сделать ее доступной для использования в службах глобализации.</span><span class="sxs-lookup"><span data-stu-id="7570a-236">For example, you can publish the feature and make it available for use in Globalization services.</span></span>

    ![Статус функции обновлен до "Завершено"](./media/RCS_GlobalF_16%20Feature%20rebase%20version%20complete.JPG)

## <a name="configure-environments-for-globalization-features"></a><a name="configureenvironment"></a><span data-ttu-id="7570a-238">Настройка сред для функций глобализации</span><span class="sxs-lookup"><span data-stu-id="7570a-238">Configure environments for Globalization features</span></span>

<span data-ttu-id="7570a-239">Пользователи служб глобализации могут управлять средой, чтобы настроить функцию глобализации и предоставить авторизацию другим пользователям, у которых будет к ней доступ.</span><span class="sxs-lookup"><span data-stu-id="7570a-239">Users of Globalization services can manage the environment to set up a Globalization feature and grant authorization to other users who will have access to it.</span></span>

1. <span data-ttu-id="7570a-240">В рабочей области **Функции глобализации**, а затем в разделе **Среды** выберите плитку **Электронные накладные**.</span><span class="sxs-lookup"><span data-stu-id="7570a-240">In the **Globalization Features** workspace, under **Environments**, select the **e-Invoicing** tile.</span></span>

    ![Рабочая область функций глобализации](./media/RCS_GlobalF_17%20Feature%20environment.JPG)

2. <span data-ttu-id="7570a-242">Выберите **Параметры хранилища ключей**, а затем выберите **Создать**, чтобы создать секрет хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="7570a-242">Select **Key Vault parameters**, and then select **New** to create an Azure Key Vault secret.</span></span>
3. <span data-ttu-id="7570a-243">Введите имя и описание для хранилища ключей, а затем в поле **URI хранилища ключей** введите URL-адрес, идентифицирующий ресурс хранилища ключей в Azure.</span><span class="sxs-lookup"><span data-stu-id="7570a-243">Enter a name and description for the key vault, and then, in the **Key Vault URI** field, enter the URL that identifies the Key Vault resource in Azure.</span></span>
4. <span data-ttu-id="7570a-244">На экспресс-вкладке **Сертификаты** выберите **Добавить**, чтобы добавить сертификат, а затем введите имя и описание для каждого сертификата.</span><span class="sxs-lookup"><span data-stu-id="7570a-244">On the **Certificates** FastTab, select **Add** to add the certificate, and enter a name and description for each certificate.</span></span>

    ![Сертификат добавлен](./media/RCS_GlobalF_18%20Feature%20envn%20key%20vault%20parameter.JPG)

5. <span data-ttu-id="7570a-246">Выберите **Создать** для создания новой среды.</span><span class="sxs-lookup"><span data-stu-id="7570a-246">Select **New** to create a new environment.</span></span>
6. <span data-ttu-id="7570a-247">Введите имя, описание и секретный ключ маркера подписи общего доступа, необходимый для хранения.</span><span class="sxs-lookup"><span data-stu-id="7570a-247">Enter a name, a description, and the shared access signature token secret required for the storage.</span></span>
7. <span data-ttu-id="7570a-248">На экспресс-вкладке **Пользователи** выберите **Создать**, чтобы добавить пользователя, у которого будет разрешение на доступ к этой среде.</span><span class="sxs-lookup"><span data-stu-id="7570a-248">On the **Users** FastTab, select **New** to add a user who will have permission to access this environment.</span></span>
8. <span data-ttu-id="7570a-249">Введите код пользователя и адрес электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="7570a-249">Enter the user's user ID and email address.</span></span>
9. <span data-ttu-id="7570a-250">Повторите шаги 7 и 8, чтобы добавить пользователей.</span><span class="sxs-lookup"><span data-stu-id="7570a-250">Repeat steps 7 and 8 to add more users.</span></span>
10. <span data-ttu-id="7570a-251">Выберите **Опубликовать**, чтобы опубликовать среду.</span><span class="sxs-lookup"><span data-stu-id="7570a-251">Select **Publish** to publish the environment.</span></span>

    ![Опубликованная среда](./media/RCS_GlobalF_19%20Feature%20envn%20publishing.JPG)
