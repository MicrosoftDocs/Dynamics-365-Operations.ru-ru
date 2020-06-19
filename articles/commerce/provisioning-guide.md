---
title: Обеспечение среды предварительной версии Dynamics 365 Commerce
description: В этой теме объясняется, как предоставить среду предварительного просмотра Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: c109c2326cf01739255b49587c15aa34ad884f6a
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426473"
---
# <a name="provision-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="dbe45-103">Обеспечение среды предварительной версии Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="dbe45-103">Provision a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="dbe45-104">В этой теме объясняется, как предоставить среду предварительного просмотра Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="dbe45-104">This topic explains how to provision a Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="dbe45-105">Прежде чем начать, рекомендуется выполнить быструю проверку данного раздела, чтобы понять, что именно требуется для этого процесса.</span><span class="sxs-lookup"><span data-stu-id="dbe45-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="dbe45-106">Если вы еще не получили доступ к предварительной версии Dynamics 365 Commerce, вы можете запросить доступ к предварительной версии на [веб-сайте Dynamics 365 Commerce](https://aka.ms/Dynamics365CommerceWebsite).</span><span class="sxs-lookup"><span data-stu-id="dbe45-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Dynamics 365 Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="dbe45-107">Обзор</span><span class="sxs-lookup"><span data-stu-id="dbe45-107">Overview</span></span>

<span data-ttu-id="dbe45-108">Чтобы успешно предоставить среду предварительного просмотра Commerce, необходимо создать проект с определенным названием и типом продукта.</span><span class="sxs-lookup"><span data-stu-id="dbe45-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="dbe45-109">У среды и Commerce Scale Unit (CSU) также есть некоторые специальные параметры, которые необходимо использовать для подготовки электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="dbe45-109">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="dbe45-110">Инструкции в этой теме описывают все необходимые шаги, которые вы должны выполнить, и параметры, которые вы должны использовать.</span><span class="sxs-lookup"><span data-stu-id="dbe45-110">The instructions in this topic describe all the steps required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="dbe45-111">После успешного предоставления среды предварительного просмотра Commerce необходимо выполнить несколько шагов после обеспечения для подготовки.</span><span class="sxs-lookup"><span data-stu-id="dbe45-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="dbe45-112">Некоторые шаги являются необязательными, в зависимости от того, какие аспекты системы вы хотите оценить.</span><span class="sxs-lookup"><span data-stu-id="dbe45-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="dbe45-113">Вы всегда можете выполнить дополнительные шаги позже.</span><span class="sxs-lookup"><span data-stu-id="dbe45-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="dbe45-114">Для получения информации о том, как настроить среду предварительного просмотра Commerce после подготовки, см. в [Настройка среды предварительной версии Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="dbe45-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="dbe45-115">Для сведений о том, как настроить дополнительные функции для среды предварительного просмотра Commerce, см. [Настройка дополнительных функций для среды предварительного просмотра Commerce](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="dbe45-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="dbe45-116">Если имеются какие-либо вопросы о шагах подготовки или возникли какие-либо ошибки, сообщите Microsoft о них в [группе Yammer предварительной версии Microsoft Dynamics 365 Commerce](https://aka.ms/Dynamics365CommercePreviewYammer).</span><span class="sxs-lookup"><span data-stu-id="dbe45-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="dbe45-117">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="dbe45-117">Prerequisites</span></span>

<span data-ttu-id="dbe45-118">Для того, чтобы предоставить среду предварительного просмотра Commerce, необходимо предусмотреть следующие предварительные условия:</span><span class="sxs-lookup"><span data-stu-id="dbe45-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="dbe45-119">У вас есть доступ к порталу Lifecycle Services Microsoft Dynamics (LCS)</span><span class="sxs-lookup"><span data-stu-id="dbe45-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="dbe45-120">Вы являетесь существующим партнером или клиентом Microsoft Dynamics 365 и можете создать проект Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="dbe45-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="dbe45-121">Вы приняли приглашение принять участие в программе предварительной версии Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="dbe45-121">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="dbe45-122">У вас имеются необходимые разрешения на создание проекта для **Миграция, создание решений и знакомство**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-122">You have the required permissions to create a project for **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="dbe45-123">Пользователь является членом роли **Менеджер среды** или **Владелец проекта** в проекте, в котором будет выполняться подготовка среды.</span><span class="sxs-lookup"><span data-stu-id="dbe45-123">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="dbe45-124">У вас есть административный доступ к вашей подписке Microsoft Azure или вы можете обратиться к администратору подписки, который может выполнить два шага, требующих права администратора, от вашего имени</span><span class="sxs-lookup"><span data-stu-id="dbe45-124">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="dbe45-125">В вас есть доступный код клиента Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="dbe45-125">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="dbe45-126">Вы создали группу безопасности Azure AD, которую можно использовать в качестве группы администраторов системы электронной коммерции, и у вас есть ее идентификатор.</span><span class="sxs-lookup"><span data-stu-id="dbe45-126">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="dbe45-127">Вы создали группу безопасности Azure AD, которую можно использовать в качестве группы модератора оценок и рецензий, и у вас есть ее идентификатор.</span><span class="sxs-lookup"><span data-stu-id="dbe45-127">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="dbe45-128">(Эта группа безопасности может быть такой же, как группа администрирования системы электронной коммерции.)</span><span class="sxs-lookup"><span data-stu-id="dbe45-128">(This security group can be the same as the e-Commerce system admin group.)</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="dbe45-129">Обеспечение своей среды предварительной версии Commerce</span><span class="sxs-lookup"><span data-stu-id="dbe45-129">Provision your Commerce preview environment</span></span>

<span data-ttu-id="dbe45-130">Эти процедуры объясняют, как обеспечить среду предварительного просмотра Commerce.</span><span class="sxs-lookup"><span data-stu-id="dbe45-130">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="dbe45-131">После их успешного завершения среда предварительного просмотра Commerce будет готова к настройке.</span><span class="sxs-lookup"><span data-stu-id="dbe45-131">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="dbe45-132">Все действия, описанные здесь, выполняются на портале LCS.</span><span class="sxs-lookup"><span data-stu-id="dbe45-132">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dbe45-133">Предварительный доступ привязан к учетной записи LCS и организации, указанной в приложении предварительного просмотра Commerce.</span><span class="sxs-lookup"><span data-stu-id="dbe45-133">Preview access is tied to the LCS account and organization that you specified in your Commerce preview application.</span></span> <span data-ttu-id="dbe45-134">Вы должны использовать ту же учетную запись для предоставления среды предварительного просмотра Commerce.</span><span class="sxs-lookup"><span data-stu-id="dbe45-134">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="dbe45-135">Если для среды предварительного просмотра Commerce необходимо использовать другую учетную запись LCS или клиента, вы должны предоставить в Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dbe45-135">If you need to use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="dbe45-136">Для получения контактной информации см. раздел [Поддержка среды предварительного просмотра Commerce](#commerce-preview-environment-support) далее в этой теме.</span><span class="sxs-lookup"><span data-stu-id="dbe45-136">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="dbe45-137">Убедитесь, что функции предварительного просмотра доступны и включены в LCS</span><span class="sxs-lookup"><span data-stu-id="dbe45-137">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="dbe45-138">Чтобы подтвердить, что функции предварительного просмотра доступны и включены в LCS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="dbe45-138">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="dbe45-139">Войдите на [портал LCS](https://lcs.dynamics.com), используя ту же учетную запись LCS, которую вы использовали для запроса доступа к предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="dbe45-139">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="dbe45-140">На главной странице LCS выполните прокрутку до конца вправо, затем выберите плитку **Управление компонентами предварительной версии**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-140">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![Плитка управления предварительной версией](./media/preview1.png)

1. <span data-ttu-id="dbe45-142">Выполните прокрутку до **Компоненты частной предварительной версии** и убедитесь, что доступны и включены следующие функции:</span><span class="sxs-lookup"><span data-stu-id="dbe45-142">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="dbe45-143">Оценка электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="dbe45-143">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="dbe45-144">Среды программы предварительной версии Commerce</span><span class="sxs-lookup"><span data-stu-id="dbe45-144">Commerce Preview Program Environments</span></span>

    ![Компоненты частной предварительной версии](./media/preview2.png)

1. <span data-ttu-id="dbe45-146">Если эти функции не отображаются в списке, свяжитесь с корпорацией Майкрософт и укажите свой рабочий адрес электронной почты, учетную запись LCS и сведения о клиенте.</span><span class="sxs-lookup"><span data-stu-id="dbe45-146">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="dbe45-147">Для получения контактной информации см. раздел [Поддержка среды предварительного просмотра Commerce](#commerce-preview-environment-support).</span><span class="sxs-lookup"><span data-stu-id="dbe45-147">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="dbe45-148">Создать новый проект</span><span class="sxs-lookup"><span data-stu-id="dbe45-148">Create a new project</span></span>

<span data-ttu-id="dbe45-149">Чтобы создать новый проект в LCS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="dbe45-149">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="dbe45-150">На главной странице LCS выберите знак плюса (**+**) для создания проекта.</span><span class="sxs-lookup"><span data-stu-id="dbe45-150">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="dbe45-151">В правой области выполните один из следующих шагов:</span><span class="sxs-lookup"><span data-stu-id="dbe45-151">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="dbe45-152">Если вы являетесь партнером, выберите **Миграция, создание решений и знакомство**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-152">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="dbe45-153">Если вы клиент, выберите **Перспективный клиент — предпродажная подготовка**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-153">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="dbe45-154">Введите название, описание и отрасль.</span><span class="sxs-lookup"><span data-stu-id="dbe45-154">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="dbe45-155">В поле **Наименование продукта** выберите **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-155">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="dbe45-156">В поле **Версия продукта** выберите **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-156">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="dbe45-157">В поле **Методология** выберите **Методология реализации Dynamics Retail**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-157">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="dbe45-158">Необязательно: можно импортировать роли и пользователей из существующего проекта.</span><span class="sxs-lookup"><span data-stu-id="dbe45-158">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="dbe45-159">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-159">Select **Create**.</span></span> <span data-ttu-id="dbe45-160">Появится представление проекта.</span><span class="sxs-lookup"><span data-stu-id="dbe45-160">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="dbe45-161">Добавление соединителя Azure</span><span class="sxs-lookup"><span data-stu-id="dbe45-161">Add the Azure Connector</span></span>

<span data-ttu-id="dbe45-162">Чтобы добавить соединитель Azure в проект LCS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="dbe45-162">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="dbe45-163">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="dbe45-163">Follow one of these steps:</span></span>

    - <span data-ttu-id="dbe45-164">Если вы являетесь партнером, выберите плитку **Параметры проекта** справа.</span><span class="sxs-lookup"><span data-stu-id="dbe45-164">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="dbe45-165">Если вы являетесь клиентом, выберите **Параметры проекта** в верхнем меню.</span><span class="sxs-lookup"><span data-stu-id="dbe45-165">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="dbe45-166">Выберите **Соединители Azure**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-166">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="dbe45-167">Выберите **Добавить**, чтобы добавить соединитель Azure.</span><span class="sxs-lookup"><span data-stu-id="dbe45-167">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="dbe45-168">Введите имя.</span><span class="sxs-lookup"><span data-stu-id="dbe45-168">Enter a name.</span></span>
1. <span data-ttu-id="dbe45-169">Введите свой код подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="dbe45-169">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="dbe45-170">Включите параметр **Настройка для использования Azure Resource Manager (ARM)**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-170">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="dbe45-171">Убедитесь, что значение **Домен (или код) арендатора AAD подписки Azure** является правильным.</span><span class="sxs-lookup"><span data-stu-id="dbe45-171">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="dbe45-172">При необходимости обратитесь к администратору подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="dbe45-172">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="dbe45-173">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-173">Select **Next**.</span></span>
1. <span data-ttu-id="dbe45-174">Следуйте инструкциям на странице, чтобы предоставить необходимым приложениям доступ к вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="dbe45-174">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="dbe45-175">При необходимости обратитесь к администратору подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="dbe45-175">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="dbe45-176">Выполните вход на [портал Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="dbe45-176">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="dbe45-177">Убедитесь, что выбран правильный каталог, а затем в меню слева выберите **Подписки**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-177">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="dbe45-178">Найдите правильную подписку из списка и выберите ее.</span><span class="sxs-lookup"><span data-stu-id="dbe45-178">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="dbe45-179">При необходимости используйте функцию поиска.</span><span class="sxs-lookup"><span data-stu-id="dbe45-179">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="dbe45-180">В меню выберите **Управление доступом (IAM)**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-180">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="dbe45-181">Справа в **Добавить назначение роли** выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-181">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="dbe45-182">Появится область **Добавление назначения ролей**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-182">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="dbe45-183">В поле **Роль** выберите **Участник**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-183">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="dbe45-184">В поле **Назначить доступ** оставьте значение по умолчанию, **пользователь Azure AD, группа или субъект-служба**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-184">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="dbe45-185">В области **Выбрать** введите **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-185">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="dbe45-186">Выберите **Службы развертывания Dynamics \[wsfed-enabled\]** из списка.</span><span class="sxs-lookup"><span data-stu-id="dbe45-186">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="dbe45-187">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-187">Select **Save**.</span></span>

1. <span data-ttu-id="dbe45-188">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-188">Select **Next**.</span></span>
1. <span data-ttu-id="dbe45-189">Следуйте инструкциям на странице, чтобы предоставить необходимым приложениям доступ к вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="dbe45-189">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="dbe45-190">При необходимости обратитесь к администратору подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="dbe45-190">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="dbe45-191">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-191">Select **Next**.</span></span>
1. <span data-ttu-id="dbe45-192">В поле **Регион Azure** выберите **Восточная часть США**, **Восточная часть США 2**, **Западная часть США** или **Западная часть США 2**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-192">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="dbe45-193">Выберите **Подключить**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-193">Select **Connect**.</span></span> <span data-ttu-id="dbe45-194">Ваш соединитель Azure должен появиться в списке.</span><span class="sxs-lookup"><span data-stu-id="dbe45-194">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="dbe45-195">Импорт демонстрационного базового расширения предварительной версии Commerce</span><span class="sxs-lookup"><span data-stu-id="dbe45-195">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="dbe45-196">Чтобы импортировать демонстрационное базовое расширение предварительной версии в ваш проект, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="dbe45-196">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="dbe45-197">Откройте домашнюю страницу для проекта, выбрав название проекта в верхней части.</span><span class="sxs-lookup"><span data-stu-id="dbe45-197">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="dbe45-198">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="dbe45-198">Follow one of these steps:</span></span>

    - <span data-ttu-id="dbe45-199">Если вы являетесь партнером, выберите плитку **Библиотека активов** справа.</span><span class="sxs-lookup"><span data-stu-id="dbe45-199">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="dbe45-200">Если вы являетесь клиентом, выберите **Библиотека активов** в верхнем меню.</span><span class="sxs-lookup"><span data-stu-id="dbe45-200">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="dbe45-201">В списке слева выберите **Готовый к развертыванию программный пакет**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-201">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="dbe45-202">Выберите **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-202">Select **Import**.</span></span>
1. <span data-ttu-id="dbe45-203">В **Общая библиотека активов** выберите **Демонстрационное базовое расширение предварительной версии Commerce** из списка активов.</span><span class="sxs-lookup"><span data-stu-id="dbe45-203">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="dbe45-204">Выберите **Комплектовать**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-204">Select **Pick**.</span></span> <span data-ttu-id="dbe45-205">Вы будете возвращены в библиотеку активов, и вы увидите расширение в списке.</span><span class="sxs-lookup"><span data-stu-id="dbe45-205">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="dbe45-206">На следующей иллюстрации показаны действия, которые необходимо выполнить на странице LCS **Библиотека активов**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-206">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![Импорт демонстрационного базового расширения предварительной версии Commerce](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="dbe45-208">Развернуть среду</span><span class="sxs-lookup"><span data-stu-id="dbe45-208">Deploy the environment</span></span>

<span data-ttu-id="dbe45-209">Выполните следующие действия, чтобы развернуть среду.</span><span class="sxs-lookup"><span data-stu-id="dbe45-209">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="dbe45-210">Возможно, вам не придется выполнять шаги 6, 7 и/или 8, потому что страницы с одним вариантом пропускаются.</span><span class="sxs-lookup"><span data-stu-id="dbe45-210">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="dbe45-211">Когда вы находитесь в представлении **Параметры среды**, подтвердите, что текст **Dynamics 365 Commerce — демонстрация (10.0.* x* с обновлением платформы *xx*)\*\* отображается непосредственно над полем **Имя среды**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-211">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="dbe45-212">Сведения см. на изображении, которое появляется после шага 8.</span><span class="sxs-lookup"><span data-stu-id="dbe45-212">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="dbe45-213">В верхнем меню выберите **Размещенные в облаке среды**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-213">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="dbe45-214">Выберите **Добавить**, чтобы добавить среду.</span><span class="sxs-lookup"><span data-stu-id="dbe45-214">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="dbe45-215">В поле **Версия приложения** выберите самую последнюю версию.</span><span class="sxs-lookup"><span data-stu-id="dbe45-215">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="dbe45-216">Если требуется выбрать версию приложения, отличающуюся от самой последней версии, не выбирайте версию, предшествующую **10.0.8**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-216">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.8**.</span></span>
1. <span data-ttu-id="dbe45-217">В поле **Версия платформы** используйте версию платформы, которая выбирается автоматически для выбранной версии приложения.</span><span class="sxs-lookup"><span data-stu-id="dbe45-217">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Выбор приложения и версий платформы](./media/project1.png)

1. <span data-ttu-id="dbe45-219">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-219">Select **Next**.</span></span>
1. <span data-ttu-id="dbe45-220">Выберите **Демонстрация** в качестве топологии среды.</span><span class="sxs-lookup"><span data-stu-id="dbe45-220">Select **Demo** as the environment topology.</span></span>

    ![Выбор топологии среды 1](./media/project2.png)

1. <span data-ttu-id="dbe45-222">Выберите **Dynamics 365 Commerce — демонстрация** в качестве топологии среды.</span><span class="sxs-lookup"><span data-stu-id="dbe45-222">Select **Dynamics 365 Commerce - Demo** as the environment topology.</span></span> <span data-ttu-id="dbe45-223">Если ранее был настроен один соединитель Azure, он будет использоваться для этой среды.</span><span class="sxs-lookup"><span data-stu-id="dbe45-223">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="dbe45-224">Если вы настроили несколько соединителей Azure, вы можете выбрать, какой соединитель использовать: **Восточная часть США**, **Восточная часть США 2**, **Западная часть США** или **Западная часть США 2**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-224">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="dbe45-225">(Для лучшей сквозной производительности, мы рекомендуем выбрать **Западная часть США 2**.)</span><span class="sxs-lookup"><span data-stu-id="dbe45-225">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![Выбор топологии среды 2](./media/project3.png)

1. <span data-ttu-id="dbe45-227">На странице **Развернуть среду** введите имя среды.</span><span class="sxs-lookup"><span data-stu-id="dbe45-227">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="dbe45-228">Оставьте дополнительные настройки без изменений.</span><span class="sxs-lookup"><span data-stu-id="dbe45-228">Leave the advanced settings as they are.</span></span>

    ![Страница развертывания среды](./media/project4.png)

1. <span data-ttu-id="dbe45-230">По мере необходимости настройте размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="dbe45-230">Adjust the VM size as required.</span></span> <span data-ttu-id="dbe45-231">(Мы рекомендуем единицу складского хранения VM \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="dbe45-231">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="dbe45-232">Просмотрите условия ценообразования и лицензирования, а затем поставьте флажок, чтобы указать, что вы согласны с ними.</span><span class="sxs-lookup"><span data-stu-id="dbe45-232">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="dbe45-233">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-233">Select **Next**.</span></span>
1. <span data-ttu-id="dbe45-234">На странице подтверждения развертывания убедитесь, что сведения правильные и затем выберите **Развернуть**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-234">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="dbe45-235">Будет возвращено представление **Размещенные в облаке среды**, и ваша среда появится в списке.</span><span class="sxs-lookup"><span data-stu-id="dbe45-235">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="dbe45-236">Запрошенная среда отобразится в очереди, затем будет развернута.</span><span class="sxs-lookup"><span data-stu-id="dbe45-236">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="dbe45-237">Для завершения рабочих процессов среды потребуется некоторое время.</span><span class="sxs-lookup"><span data-stu-id="dbe45-237">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="dbe45-238">Поэтому проверьте примерно через шесть-девять часов.</span><span class="sxs-lookup"><span data-stu-id="dbe45-238">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="dbe45-239">Перед продолжением убедитесь, что состояние вашей среды — **Развернуто**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-239">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="dbe45-240">Инициализация Commerce Scale Unit (облако)</span><span class="sxs-lookup"><span data-stu-id="dbe45-240">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="dbe45-241">Чтобы инициализировать CSU, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="dbe45-241">To initialize CSU, follow these steps.</span></span>

1. <span data-ttu-id="dbe45-242">В представлении **Размещенные в облаке среды** выберите свою среду из списка.</span><span class="sxs-lookup"><span data-stu-id="dbe45-242">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="dbe45-243">Выберите **Полные сведения** в представлении среды с правой стороны.</span><span class="sxs-lookup"><span data-stu-id="dbe45-243">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="dbe45-244">Появится представление сведений о среде.</span><span class="sxs-lookup"><span data-stu-id="dbe45-244">The environment details view appears.</span></span>
1. <span data-ttu-id="dbe45-245">В **Компоненты среды** выберите **Управление**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-245">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="dbe45-246">На вкладке **Commerce** выберите **Инициализация**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-246">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="dbe45-247">Будет отображено представление параметров инициализации CSU.</span><span class="sxs-lookup"><span data-stu-id="dbe45-247">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="dbe45-248">В поле **Регион** выберите **Восточная часть США**, **Восточная часть США 2**, **Западная часть США** или **Западная часть США 2**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-248">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="dbe45-249">В поле **Версия** выберите **Укажите версию** в списке, а затем укажите **9.18.20014.4** в поле, которое появляется.</span><span class="sxs-lookup"><span data-stu-id="dbe45-249">In the **Version** field, select **Specify a version** in the list, and then specify **9.18.20014.4** in the field that appears.</span></span> <span data-ttu-id="dbe45-250">Не забудьте указать точную версию, которая указана здесь.</span><span class="sxs-lookup"><span data-stu-id="dbe45-250">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="dbe45-251">В противном случае вам придется обновить RCSU до правильной версии позже.</span><span class="sxs-lookup"><span data-stu-id="dbe45-251">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="dbe45-252">Включите параметр **Применить расширение**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-252">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="dbe45-253">В списке расширений выберите **Демонстрационное базовое расширение предварительной версии Commerce**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-253">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="dbe45-254">Выберите **Инициализация**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-254">Select **Initialize**.</span></span>
1. <span data-ttu-id="dbe45-255">На странице подтверждения развертывания убедитесь, что сведения правильные и затем выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-255">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="dbe45-256">Отобразится представление **Управление Commerce**, в котором будет выбрана вкладка **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-256">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="dbe45-257">Ваш CSU был поставлен в очередь для подготовки.</span><span class="sxs-lookup"><span data-stu-id="dbe45-257">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="dbe45-258">Перед продолжением убедитесь, что состояние CSU — **Успех**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-258">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="dbe45-259">Инициализация занимает примерно два-пять часов.</span><span class="sxs-lookup"><span data-stu-id="dbe45-259">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="dbe45-260">Инициализация электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="dbe45-260">Initialize e-Commerce</span></span>

<span data-ttu-id="dbe45-261">Чтобы инициализировать электронную коммерцию, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="dbe45-261">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="dbe45-262">На вкладке **Электронная коммерция** просмотрите согласие на предварительную версию, а затем выберите **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-262">On the **e-Commerce** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="dbe45-263">В поле **Имя клиента электронной коммерции** введите имя.</span><span class="sxs-lookup"><span data-stu-id="dbe45-263">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="dbe45-264">Однако обратите внимание, что это имя появится в некоторых URL-адресах, указывающих на экземпляр электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="dbe45-264">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="dbe45-265">В поле **Имя Commerce Scale Unit** выберите CSU в списке.</span><span class="sxs-lookup"><span data-stu-id="dbe45-265">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="dbe45-266">(В списке должен быть только один вариант.)</span><span class="sxs-lookup"><span data-stu-id="dbe45-266">(The list should have only one option.)</span></span>

    <span data-ttu-id="dbe45-267">Поле **География электронной коммерции** задается автоматически, и значение не может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="dbe45-267">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="dbe45-268">Выберите **Далее** для продолжения.</span><span class="sxs-lookup"><span data-stu-id="dbe45-268">Select **Next** to continue.</span></span>
1. <span data-ttu-id="dbe45-269">В поле **Поддерживаемые имена узлов** введите любой допустимый домен, например `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="dbe45-269">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="dbe45-270">В поле **Группа безопасности AAD для системного администратора** введите первые несколько букв названия группы безопасности, которую вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="dbe45-270">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="dbe45-271">Выберите значок увеличительного стекла для отображения результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="dbe45-271">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="dbe45-272">Выберите правильную группу безопасности из списка.</span><span class="sxs-lookup"><span data-stu-id="dbe45-272">Select the correct security group from the list.</span></span>
2.  <span data-ttu-id="dbe45-273">В поле **Группа безопасности AAD для модератора оценок и отзывов** введите первые несколько букв названия группы безопасности, которую вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="dbe45-273">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="dbe45-274">Выберите значок увеличительного стекла для отображения результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="dbe45-274">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="dbe45-275">Выберите правильную группу безопасности из списка.</span><span class="sxs-lookup"><span data-stu-id="dbe45-275">Select the correct security group from the list.</span></span>
1. <span data-ttu-id="dbe45-276">Оставьте параметр **Включить службу оценок и отзывов** включенным.</span><span class="sxs-lookup"><span data-stu-id="dbe45-276">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="dbe45-277">Выберите **Инициализация**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-277">Select **Initialize**.</span></span> <span data-ttu-id="dbe45-278">Отобразится представление **Управление Commerce**, в котором будет выбрана вкладка **Электронная коммерция**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-278">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="dbe45-279">Инициализация электронной коммерции начата.</span><span class="sxs-lookup"><span data-stu-id="dbe45-279">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="dbe45-280">Перед продолжением необходимо подождать, пока состояние инициализации электронной коммерции не станет **Успешная инициализация**.</span><span class="sxs-lookup"><span data-stu-id="dbe45-280">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="dbe45-281">В **Ссылки** в нижнем правом углу запишите URL-адреса для следующих ссылок:</span><span class="sxs-lookup"><span data-stu-id="dbe45-281">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="dbe45-282">**Сайт электронной коммерции** — ссылка на корневой узел вашего сайта электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="dbe45-282">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="dbe45-283">**Средство управления сайтом электронной коммерции** — ссылка на средство управления сайтом.</span><span class="sxs-lookup"><span data-stu-id="dbe45-283">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="dbe45-284">Поддержка среды предварительной версии Commerce</span><span class="sxs-lookup"><span data-stu-id="dbe45-284">Commerce preview environment support</span></span>

<span data-ttu-id="dbe45-285">Если при выполнении шагов подготовки возникают проблемы, обратитесь за помощью в [группу Yammer предварительной версии Microsoft Dynamics 365 Commerce](https://aka.ms/Dynamics365CommercePreviewYammer).</span><span class="sxs-lookup"><span data-stu-id="dbe45-285">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

## <a name="next-steps"></a><span data-ttu-id="dbe45-286">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="dbe45-286">Next steps</span></span>

<span data-ttu-id="dbe45-287">Для продолжения процесса предоставления и настройки вашей среды предварительной версии Commerce см. [Настройка среды предварительной версии Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="dbe45-287">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dbe45-288">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="dbe45-288">Additional resources</span></span>

[<span data-ttu-id="dbe45-289">Обзор среды предварительной версии Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="dbe45-289">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="dbe45-290">Настройка среды предварительной версии Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="dbe45-290">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="dbe45-291">Настройка дополнительных функций среды предварительной версии Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="dbe45-291">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="dbe45-292">Вопросы и ответы по среде предварительной версии Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="dbe45-292">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="dbe45-293">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="dbe45-293">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="dbe45-294">Commerce Scale Unit (облако)</span><span class="sxs-lookup"><span data-stu-id="dbe45-294">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="dbe45-295">Портал Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="dbe45-295">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="dbe45-296">Веб-сайт Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="dbe45-296">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

