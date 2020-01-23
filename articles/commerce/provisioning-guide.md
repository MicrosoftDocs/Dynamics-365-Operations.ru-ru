---
title: Обеспечение среды предварительной версии Commerce
description: В этой теме объясняется, как предоставить среду предварительного просмотра Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 01/06/2020
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
ms.openlocfilehash: b77d2cbbc100aeae5dcd53ddbe69ff2e4435da13
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934756"
---
# <a name="provision-a-commerce-preview-environment"></a><span data-ttu-id="15acc-103">Обеспечение среды предварительной версии Commerce</span><span class="sxs-lookup"><span data-stu-id="15acc-103">Provision a Commerce preview environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="15acc-104">В этой теме объясняется, как предоставить среду предварительного просмотра Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="15acc-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="15acc-105">Прежде чем приступать к работе, рекомендуется по крайней мере просмотреть всю тему, чтобы понять, что именно охватывается в этом процессе и что содержит тема.</span><span class="sxs-lookup"><span data-stu-id="15acc-105">Before you begin, we recommend that you at least skim through this whole topic to get an idea of what the process entails and what this topic contains.</span></span>

> [!NOTE]
> <span data-ttu-id="15acc-106">Если вы еще не получили доступ к предварительной версии Dynamics 365 Commerce, вы можете запросить доступ к предварительной версии на [веб-сайте Commerce](https://aka.ms/Dynamics365CommerceWebsite).</span><span class="sxs-lookup"><span data-stu-id="15acc-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="15acc-107">Обзор</span><span class="sxs-lookup"><span data-stu-id="15acc-107">Overview</span></span>

<span data-ttu-id="15acc-108">Чтобы успешно предоставить среду предварительного просмотра Commerce, необходимо создать проект с определенным названием и типом продукта.</span><span class="sxs-lookup"><span data-stu-id="15acc-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="15acc-109">У среды и Retail Cloud Scale Unit (RCSU) также есть некоторые специальные параметры, которые необходимо использовать для подготовки электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="15acc-109">The environment and Retail Cloud Scale Unit (RCSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="15acc-110">Инструкции в этой теме описывают все необходимые шаги, которые вы должны выполнить, и параметры, которые вы должны использовать.</span><span class="sxs-lookup"><span data-stu-id="15acc-110">The instructions in this topic describe all the required steps that you must complete and the parameters that you must use.</span></span>

<span data-ttu-id="15acc-111">После успешного предоставления среды предварительного просмотра Commerce необходимо выполнить несколько шагов после обеспечения для подготовки.</span><span class="sxs-lookup"><span data-stu-id="15acc-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="15acc-112">Некоторые шаги являются необязательными, в зависимости от того, какие аспекты системы вы хотите оценить.</span><span class="sxs-lookup"><span data-stu-id="15acc-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="15acc-113">Вы всегда можете выполнить дополнительные шаги позже.</span><span class="sxs-lookup"><span data-stu-id="15acc-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="15acc-114">Для получения информации о том, как настроить среду предварительного просмотра Commerce после подготовки, см. в [Настройка среды предварительной версии Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="15acc-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="15acc-115">Для сведений о том, как настроить дополнительные функции для среды предварительного просмотра Commerce, см. [Настройка дополнительных функций для среды предварительного просмотра Commerce](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="15acc-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="15acc-116">Если имеются какие-либо вопросы о шагах подготовки или возникли какие-либо ошибки, сообщите Microsoft о них в [группе Yammer предварительной версии Microsoft Dynamics 365 Commerce](https://aka.ms/Dynamics365CommercePreviewYammer).</span><span class="sxs-lookup"><span data-stu-id="15acc-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="15acc-117">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="15acc-117">Prerequisites</span></span>

<span data-ttu-id="15acc-118">Для того, чтобы предоставить среду предварительного просмотра Commerce, необходимо предусмотреть следующие предварительные условия:</span><span class="sxs-lookup"><span data-stu-id="15acc-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="15acc-119">У вас есть доступ к порталу Lifecycle Services Microsoft Dynamics (LCS)</span><span class="sxs-lookup"><span data-stu-id="15acc-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="15acc-120">Вы приняли приглашение принять участие в программе предварительной версии Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="15acc-120">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="15acc-121">У вас имеются необходимые разрешения на создание проекта для **Перспективный клиент — предпродажная подготовка** или **Миграция, создание решений и знакомство**.</span><span class="sxs-lookup"><span data-stu-id="15acc-121">You have the required permissions to create a project for **Prospective presales** or **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="15acc-122">Пользователь является членом роли **Менеджер среды** или **Владелец проекта** в проекте, в котором будет выполняться подготовка среды.</span><span class="sxs-lookup"><span data-stu-id="15acc-122">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="15acc-123">У вас есть административный доступ к вашей подписке Microsoft Azure или вы можете обратиться к администратору подписки, который может выполнить два шага, требующих права администратора, от вашего имени</span><span class="sxs-lookup"><span data-stu-id="15acc-123">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="15acc-124">В вас есть доступный код клиента Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="15acc-124">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="15acc-125">Вы создали группу безопасности Azure AD, которую можно использовать в качестве группы администраторов системы электронной коммерции, и у вас есть ее идентификатор.</span><span class="sxs-lookup"><span data-stu-id="15acc-125">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="15acc-126">Вы создали группу безопасности Azure AD, которую можно использовать в качестве группы модератора оценок и рецензий, и у вас есть ее идентификатор.</span><span class="sxs-lookup"><span data-stu-id="15acc-126">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="15acc-127">(Эта группа безопасности может быть такой же, как группа администрирования системы электронной коммерции.)</span><span class="sxs-lookup"><span data-stu-id="15acc-127">(This security group can be the same as the e-Commerce system admin group.)</span></span>

### <a name="find-your-azure-ad-tenant-id"></a><span data-ttu-id="15acc-128">Поиск своего кода клиента Azure AD</span><span class="sxs-lookup"><span data-stu-id="15acc-128">Find your Azure AD tenant ID</span></span>

<span data-ttu-id="15acc-129">Ваш код клиента Azure AD является глобально уникальным кодом (GUID), который похож на этот пример: **72f988bf-86f1-41af-91ab-2d7cd011db47**.</span><span class="sxs-lookup"><span data-stu-id="15acc-129">Your Azure AD tenant ID is a globally unique identifier (GUID) that resembles this example: **72f988bf-86f1-41af-91ab-2d7cd011db47**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-the-azure-portal"></a><span data-ttu-id="15acc-130">Найдите свой код клиента Azure AD с помощью портала Azure</span><span class="sxs-lookup"><span data-stu-id="15acc-130">Find your Azure AD tenant ID by using the Azure portal</span></span>

1. <span data-ttu-id="15acc-131">Выполните вход на [портал Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="15acc-131">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="15acc-132">Убедитесь, что выбран правильный каталог.</span><span class="sxs-lookup"><span data-stu-id="15acc-132">Make sure that the correct directory is selected.</span></span>
1. <span data-ttu-id="15acc-133">В меню слева выберите **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="15acc-133">On the menu on the left, select **Azure Active Directory**.</span></span>
1. <span data-ttu-id="15acc-134">В **Управление** выберите **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="15acc-134">Under **Manage**, select **Properties**.</span></span> <span data-ttu-id="15acc-135">Ваш код клиента Azure AD отображается в **Код каталога**.</span><span class="sxs-lookup"><span data-stu-id="15acc-135">Your Azure AD tenant ID appears under **Directory ID**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-openid-connect-metadata"></a><span data-ttu-id="15acc-136">Поиск своего кода клиента Azure AD с помощью метаданных OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="15acc-136">Find your Azure AD tenant ID by using OpenID Connect metadata</span></span>

<span data-ttu-id="15acc-137">Создайте URL-адрес OpenID, заменив **\{ВАШ\_ДОМЕН\}** на свой домен, например `microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="15acc-137">Create an OpenID URL by replacing **\{YOUR\_DOMAIN\}** with your domain, such as `microsoft.com`.</span></span> <span data-ttu-id="15acc-138">Например, `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` станет `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.</span><span class="sxs-lookup"><span data-stu-id="15acc-138">For example, `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` will become `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.</span></span>

1. <span data-ttu-id="15acc-139">Перейдите по URL-адресу OpenID, содержащему ваш домен.</span><span class="sxs-lookup"><span data-stu-id="15acc-139">Go to the OpenID URL that contains your domain.</span></span>

    <span data-ttu-id="15acc-140">Код клиента Azure AD может отображаться в нескольких значениях свойств.</span><span class="sxs-lookup"><span data-stu-id="15acc-140">You can find you Azure AD tenant ID in multiple property values.</span></span>

1. <span data-ttu-id="15acc-141">Найдите **авторизация\_конечная точка** и извлеките GUID, который появляется сразу после `login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="15acc-141">Find **authorization\_endpoint**, and extract the GUID that appears immediately after `login.microsoftonline.com/`.</span></span>

### <a name="find-your-azure-ad-security-group-id"></a><span data-ttu-id="15acc-142">Поиск своего кода группы безопасности Azure AD</span><span class="sxs-lookup"><span data-stu-id="15acc-142">Find your Azure AD security group ID</span></span>

<span data-ttu-id="15acc-143">Код вашей группы безопасности Azure AD — это GUID, похожий на этот пример: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.</span><span class="sxs-lookup"><span data-stu-id="15acc-143">The ID of your Azure AD security group is a GUID that resembles this example: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.</span></span>

<span data-ttu-id="15acc-144">Эта процедура предполагает, что вы являетесь участником группы, для которой вы пытаетесь найти код.</span><span class="sxs-lookup"><span data-stu-id="15acc-144">This procedure assumes that you're a member of the group that you're trying to find the ID for.</span></span>

1. <span data-ttu-id="15acc-145">Откройте [песочницу Graph](https://developer.microsoft.com/graph/graph-explorer#).</span><span class="sxs-lookup"><span data-stu-id="15acc-145">Open the [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer#).</span></span>
1. <span data-ttu-id="15acc-146">Выберите **Войти с учетной записью Майкрософт** и выполните вход, используя свои учетные данные.</span><span class="sxs-lookup"><span data-stu-id="15acc-146">Select **Sign In with Microsoft**, and sign in by using your credentials.</span></span>
1. <span data-ttu-id="15acc-147">Слева выберите **показать другие образцы**.</span><span class="sxs-lookup"><span data-stu-id="15acc-147">On the left, select **show more samples**.</span></span>
1. <span data-ttu-id="15acc-148">В правой области включите **Группы**.</span><span class="sxs-lookup"><span data-stu-id="15acc-148">In the right pane, enable **Groups**.</span></span>
1. <span data-ttu-id="15acc-149">Закройте правую область.</span><span class="sxs-lookup"><span data-stu-id="15acc-149">Close the right pane.</span></span>
1. <span data-ttu-id="15acc-150">Выберите **все группы, к которым я принадлежу**.</span><span class="sxs-lookup"><span data-stu-id="15acc-150">Select **all groups I belong to**.</span></span>
1. <span data-ttu-id="15acc-151">В поле **Просмотр ответа** найдите свою группу.</span><span class="sxs-lookup"><span data-stu-id="15acc-151">In the **Response Preview** field, find your group.</span></span> <span data-ttu-id="15acc-152">Код группы безопасности отображается под свойством **id**.</span><span class="sxs-lookup"><span data-stu-id="15acc-152">The security group ID appears under the **id** property.</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="15acc-153">Обеспечение своей среды предварительной версии Commerce</span><span class="sxs-lookup"><span data-stu-id="15acc-153">Provision your Commerce preview environment</span></span>

<span data-ttu-id="15acc-154">Эти процедуры объясняют, как обеспечить среду предварительного просмотра Commerce.</span><span class="sxs-lookup"><span data-stu-id="15acc-154">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="15acc-155">После их успешного завершения среда предварительного просмотра Commerce будет готова к настройке.</span><span class="sxs-lookup"><span data-stu-id="15acc-155">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="15acc-156">Все действия, описанные здесь, выполняются на портале LCS.</span><span class="sxs-lookup"><span data-stu-id="15acc-156">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="15acc-157">Предварительный доступ привязан к учетной записи LCS и организации, указанной в приложении предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="15acc-157">Preview access is tied to the LCS account and organization that you specified in your preview application.</span></span> <span data-ttu-id="15acc-158">Вы должны использовать ту же учетную запись для предоставления среды предварительного просмотра Commerce.</span><span class="sxs-lookup"><span data-stu-id="15acc-158">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="15acc-159">Если для среды предварительного просмотра Commerce необходимо использовать другую учетную запись LCS или клиента, вы должны предоставить в Microsoft.</span><span class="sxs-lookup"><span data-stu-id="15acc-159">If you must use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="15acc-160">Для получения контактной информации см. раздел [Поддержка среды предварительного просмотра Commerce](#commerce-preview-environment-support) далее в этой теме.</span><span class="sxs-lookup"><span data-stu-id="15acc-160">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="grant-access-to-e-commerce-applications"></a><span data-ttu-id="15acc-161">Предоставление доступа к приложениям электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="15acc-161">Grant access to e-Commerce applications</span></span>

> [!IMPORTANT]
> <span data-ttu-id="15acc-162">Лицо, выполняющие вход, должны быть администратором клиента Azure AD, у которого есть код клиента Azure AD.</span><span class="sxs-lookup"><span data-stu-id="15acc-162">The person who signs in must be an Azure AD tenant admin who has the Azure AD tenant ID.</span></span> <span data-ttu-id="15acc-163">Если этот шаг не будет успешно завершен, остальные этапы подготовки невозможны.</span><span class="sxs-lookup"><span data-stu-id="15acc-163">If this step isn't successfully completed, the remaining provisioning steps will fail.</span></span>

<span data-ttu-id="15acc-164">Чтобы разрешить приложениям электронной коммерции доступ к подписке Azure, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="15acc-164">To authorize e-Commerce applications to access your Azure subscription, follow these steps.</span></span>

1. <span data-ttu-id="15acc-165">Соберите URL-адрес в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="15acc-165">Assemble a URL in the following format:</span></span>

    `https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345`

1. <span data-ttu-id="15acc-166">Скопируйте и вставьте URL-адрес в браузер или текстовый редактор и замените **\{AAD\_TENANT\_ID\}** своим кодом клиента Azure AD.</span><span class="sxs-lookup"><span data-stu-id="15acc-166">Copy and paste the URL into your browser or text editor, and replace **\{AAD\_TENANT\_ID\}** with your Azure AD tenant ID.</span></span> <span data-ttu-id="15acc-167">Затем откройте URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="15acc-167">Then open the URL.</span></span>
1. <span data-ttu-id="15acc-168">В диалоговом окне входа Azure AD выполните вход и подтвердите, что вы хотите предоставить для **Dynamics 365 Commerce (предварительная версия)** доступ к подписке.</span><span class="sxs-lookup"><span data-stu-id="15acc-168">In the Azure AD sign-in dialog box, sign in, and confirm that you want to grant **Dynamics 365 Commerce (Preview)** access to your subscription.</span></span> <span data-ttu-id="15acc-169">Вы будете перенаправлены на страницу, которая подтверждает, успешно ли выполнена данная операция.</span><span class="sxs-lookup"><span data-stu-id="15acc-169">You're redirected to a page that indicates whether the operation was successful.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="15acc-170">Убедитесь, что функции предварительного просмотра доступны и включены в LCS</span><span class="sxs-lookup"><span data-stu-id="15acc-170">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="15acc-171">Чтобы подтвердить, что функции предварительного просмотра доступны и включены в LCS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="15acc-171">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="15acc-172">Войдите на [портал LCS](https://lcs.dynamics.com), используя ту же учетную запись LCS, которую вы использовали для запроса доступа к предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="15acc-172">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="15acc-173">На главной странице LCS выполните прокрутку до конца вправо, затем выберите плитку **Управление компонентами предварительной версии**.</span><span class="sxs-lookup"><span data-stu-id="15acc-173">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![Плитка управления предварительной версией](./media/preview1.png)

1. <span data-ttu-id="15acc-175">Выполните прокрутку до **Компоненты частной предварительной версии** и убедитесь, что доступны и включены следующие функции:</span><span class="sxs-lookup"><span data-stu-id="15acc-175">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="15acc-176">Оценка электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="15acc-176">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="15acc-177">Среды программы предварительной версии Commerce</span><span class="sxs-lookup"><span data-stu-id="15acc-177">Commerce Preview Program Environments</span></span>

    ![Компоненты частной предварительной версии](./media/preview2.png)

1. <span data-ttu-id="15acc-179">Если эти функции не отображаются в списке, свяжитесь с корпорацией Майкрософт и укажите свой рабочий адрес электронной почты, учетную запись LCS и сведения о клиенте.</span><span class="sxs-lookup"><span data-stu-id="15acc-179">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="15acc-180">Для получения контактной информации см. раздел [Поддержка среды предварительного просмотра Commerce](#commerce-preview-environment-support).</span><span class="sxs-lookup"><span data-stu-id="15acc-180">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="15acc-181">Создать новый проект</span><span class="sxs-lookup"><span data-stu-id="15acc-181">Create a new project</span></span>

<span data-ttu-id="15acc-182">Чтобы создать новый проект в LCS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="15acc-182">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="15acc-183">На главной странице LCS выберите знак плюса (**+**) для создания проекта.</span><span class="sxs-lookup"><span data-stu-id="15acc-183">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="15acc-184">В правой области выполните один из следующих шагов:</span><span class="sxs-lookup"><span data-stu-id="15acc-184">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="15acc-185">Если вы являетесь партнером, выберите **Миграция, создание решений и знакомство**.</span><span class="sxs-lookup"><span data-stu-id="15acc-185">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="15acc-186">Если вы клиент, выберите **Перспективный клиент — предпродажная подготовка**.</span><span class="sxs-lookup"><span data-stu-id="15acc-186">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="15acc-187">Введите название, описание и отрасль.</span><span class="sxs-lookup"><span data-stu-id="15acc-187">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="15acc-188">В поле **Наименование продукта** выберите **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="15acc-188">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="15acc-189">В поле **Версия продукта** выберите **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="15acc-189">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="15acc-190">В поле **Методология** выберите **Методология реализации Dynamics Retail**.</span><span class="sxs-lookup"><span data-stu-id="15acc-190">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="15acc-191">Необязательно: можно импортировать роли и пользователей из существующего проекта.</span><span class="sxs-lookup"><span data-stu-id="15acc-191">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="15acc-192">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="15acc-192">Select **Create**.</span></span> <span data-ttu-id="15acc-193">Появится представление проекта.</span><span class="sxs-lookup"><span data-stu-id="15acc-193">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="15acc-194">Добавление соединителя Azure</span><span class="sxs-lookup"><span data-stu-id="15acc-194">Add the Azure Connector</span></span>

<span data-ttu-id="15acc-195">Чтобы добавить соединитель Azure в проект LCS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="15acc-195">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="15acc-196">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="15acc-196">Follow one of these steps:</span></span>

    - <span data-ttu-id="15acc-197">Если вы являетесь партнером, выберите плитку **Параметры проекта** справа.</span><span class="sxs-lookup"><span data-stu-id="15acc-197">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="15acc-198">Если вы являетесь клиентом, выберите **Параметры проекта** в верхнем меню.</span><span class="sxs-lookup"><span data-stu-id="15acc-198">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="15acc-199">Выберите **Соединители Azure**.</span><span class="sxs-lookup"><span data-stu-id="15acc-199">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="15acc-200">Выберите **Добавить**, чтобы добавить соединитель Azure.</span><span class="sxs-lookup"><span data-stu-id="15acc-200">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="15acc-201">Введите имя.</span><span class="sxs-lookup"><span data-stu-id="15acc-201">Enter a name.</span></span>
1. <span data-ttu-id="15acc-202">Введите свой код подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="15acc-202">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="15acc-203">Включите параметр **Настройка для использования Azure Resource Manager (ARM)**.</span><span class="sxs-lookup"><span data-stu-id="15acc-203">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="15acc-204">Убедитесь, что значение **Домен (или код) арендатора AAD подписки Azure** является правильным.</span><span class="sxs-lookup"><span data-stu-id="15acc-204">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="15acc-205">При необходимости обратитесь к администратору подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="15acc-205">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="15acc-206">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="15acc-206">Select **Next**.</span></span>
1. <span data-ttu-id="15acc-207">Следуйте инструкциям на странице, чтобы предоставить необходимым приложениям доступ к вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="15acc-207">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="15acc-208">При необходимости обратитесь к администратору подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="15acc-208">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="15acc-209">Выполните вход на [портал Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="15acc-209">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="15acc-210">Убедитесь, что выбран правильный каталог, а затем в меню слева выберите **Подписки**.</span><span class="sxs-lookup"><span data-stu-id="15acc-210">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="15acc-211">Найдите правильную подписку из списка и выберите ее.</span><span class="sxs-lookup"><span data-stu-id="15acc-211">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="15acc-212">При необходимости используйте функцию поиска.</span><span class="sxs-lookup"><span data-stu-id="15acc-212">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="15acc-213">В меню выберите **Управление доступом (IAM)**.</span><span class="sxs-lookup"><span data-stu-id="15acc-213">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="15acc-214">Справа в **Добавить назначение роли** выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="15acc-214">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="15acc-215">Появится область **Добавление назначения ролей**.</span><span class="sxs-lookup"><span data-stu-id="15acc-215">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="15acc-216">В поле **Роль** выберите **Участник**.</span><span class="sxs-lookup"><span data-stu-id="15acc-216">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="15acc-217">В поле **Назначить доступ** оставьте значение по умолчанию, **пользователь Azure AD, группа или субъект-служба**.</span><span class="sxs-lookup"><span data-stu-id="15acc-217">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="15acc-218">В области **Выбрать** введите **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span><span class="sxs-lookup"><span data-stu-id="15acc-218">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="15acc-219">Выберите **Службы развертывания Dynamics \[wsfed-enabled\]** из списка.</span><span class="sxs-lookup"><span data-stu-id="15acc-219">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="15acc-220">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="15acc-220">Select **Save**.</span></span>

1. <span data-ttu-id="15acc-221">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="15acc-221">Select **Next**.</span></span>
1. <span data-ttu-id="15acc-222">Следуйте инструкциям на странице, чтобы предоставить необходимым приложениям доступ к вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="15acc-222">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="15acc-223">При необходимости обратитесь к администратору подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="15acc-223">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="15acc-224">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="15acc-224">Select **Next**.</span></span>
1. <span data-ttu-id="15acc-225">В поле **Регион Azure** выберите **Восточная часть США**, **Восточная часть США 2**, **Западная часть США** или **Западная часть США 2**.</span><span class="sxs-lookup"><span data-stu-id="15acc-225">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="15acc-226">Выберите **Подключить**.</span><span class="sxs-lookup"><span data-stu-id="15acc-226">Select **Connect**.</span></span> <span data-ttu-id="15acc-227">Ваш соединитель Azure должен появиться в списке.</span><span class="sxs-lookup"><span data-stu-id="15acc-227">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="15acc-228">Импорт демонстрационного базового расширения предварительной версии Commerce</span><span class="sxs-lookup"><span data-stu-id="15acc-228">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="15acc-229">Чтобы импортировать демонстрационное базовое расширение предварительной версии в ваш проект, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="15acc-229">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="15acc-230">Откройте домашнюю страницу для проекта, выбрав название проекта в верхней части.</span><span class="sxs-lookup"><span data-stu-id="15acc-230">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="15acc-231">Выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="15acc-231">Follow one of these steps:</span></span>

    - <span data-ttu-id="15acc-232">Если вы являетесь партнером, выберите плитку **Библиотека активов** справа.</span><span class="sxs-lookup"><span data-stu-id="15acc-232">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="15acc-233">Если вы являетесь клиентом, выберите **Библиотека активов** в верхнем меню.</span><span class="sxs-lookup"><span data-stu-id="15acc-233">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="15acc-234">В списке слева выберите **Готовый к развертыванию программный пакет**.</span><span class="sxs-lookup"><span data-stu-id="15acc-234">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="15acc-235">Выберите **Импорт**.</span><span class="sxs-lookup"><span data-stu-id="15acc-235">Select **Import**.</span></span>
1. <span data-ttu-id="15acc-236">В **Общая библиотека активов** выберите **Демонстрационное базовое расширение предварительной версии Commerce** из списка активов.</span><span class="sxs-lookup"><span data-stu-id="15acc-236">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="15acc-237">Выберите **Комплектовать**.</span><span class="sxs-lookup"><span data-stu-id="15acc-237">Select **Pick**.</span></span> <span data-ttu-id="15acc-238">Вы будете возвращены в библиотеку активов, и вы увидите расширение в списке.</span><span class="sxs-lookup"><span data-stu-id="15acc-238">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="15acc-239">На следующей иллюстрации показаны действия, которые необходимо выполнить на странице LCS **Библиотека активов**.</span><span class="sxs-lookup"><span data-stu-id="15acc-239">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![Импорт демонстрационного базового расширения предварительной версии Commerce](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="15acc-241">Развернуть среду</span><span class="sxs-lookup"><span data-stu-id="15acc-241">Deploy the environment</span></span>

<span data-ttu-id="15acc-242">Выполните следующие действия, чтобы развернуть среду.</span><span class="sxs-lookup"><span data-stu-id="15acc-242">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="15acc-243">Возможно, вам не придется выполнять шаги 6, 7 и/или 8, потому что страницы с одним вариантом пропускаются.</span><span class="sxs-lookup"><span data-stu-id="15acc-243">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="15acc-244">Когда вы находитесь в представлении **Параметры среды**, подтвердите, что текст **Dynamics 365 Commerce (предварительная версия) — демонстрация (10.0.6 с обновлением платформы 30)** отображается непосредственно над полем **Имя среды**.</span><span class="sxs-lookup"><span data-stu-id="15acc-244">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce (Preview) - Demo (10.0.6 with Platform update 30)** appears directly above the **Environment name** field.</span></span> <span data-ttu-id="15acc-245">См. изображение, которое появляется после шага 8.</span><span class="sxs-lookup"><span data-stu-id="15acc-245">See the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="15acc-246">В верхнем меню выберите **Размещенные в облаке среды**.</span><span class="sxs-lookup"><span data-stu-id="15acc-246">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="15acc-247">Выберите **Добавить**, чтобы добавить среду.</span><span class="sxs-lookup"><span data-stu-id="15acc-247">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="15acc-248">В поле **Версия приложения** выберите **10.0.6**.</span><span class="sxs-lookup"><span data-stu-id="15acc-248">In the **Application version** field, select **10.0.6**.</span></span>
1. <span data-ttu-id="15acc-249">В поле **Версия платформы** выберите **Обновление платформы 30**.</span><span class="sxs-lookup"><span data-stu-id="15acc-249">In the **Platform version** field, select **Platform Update 30**.</span></span>

    ![Выбор приложения и версий платформы](./media/project1.png)

1. <span data-ttu-id="15acc-251">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="15acc-251">Select **Next**.</span></span>
1. <span data-ttu-id="15acc-252">Выберите **Демонстрация** в качестве топологии среды.</span><span class="sxs-lookup"><span data-stu-id="15acc-252">Select **Demo** as the environment topology.</span></span>

    ![Выбор топологии среды 1](./media/project2.png)

1. <span data-ttu-id="15acc-254">Выберите **Dynamics 365 Commerce (предварительная версия) — демонстрация** в качестве топологии среды.</span><span class="sxs-lookup"><span data-stu-id="15acc-254">Select **Dynamics 365 Commerce (Preview) - Demo** as the environment topology.</span></span> <span data-ttu-id="15acc-255">Если ранее был настроен один соединитель Azure, он будет использоваться для этой среды.</span><span class="sxs-lookup"><span data-stu-id="15acc-255">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="15acc-256">Если вы настроили несколько соединителей Azure, вы можете выбрать, какой соединитель использовать: **Восточная часть США**, **Восточная часть США 2**, **Западная часть США** или **Западная часть США 2**.</span><span class="sxs-lookup"><span data-stu-id="15acc-256">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="15acc-257">(Для лучшей сквозной производительности, мы рекомендуем выбрать **Западная часть США 2**.)</span><span class="sxs-lookup"><span data-stu-id="15acc-257">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![Выбор топологии среды 2](./media/project3.png)

1. <span data-ttu-id="15acc-259">На странице **Развернуть среду** введите имя среды.</span><span class="sxs-lookup"><span data-stu-id="15acc-259">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="15acc-260">Оставьте дополнительные настройки без изменений.</span><span class="sxs-lookup"><span data-stu-id="15acc-260">Leave the advanced settings as they are.</span></span>

    ![Страница развертывания среды](./media/project4.png)

1. <span data-ttu-id="15acc-262">По мере необходимости настройте размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="15acc-262">Adjust the VM size as required.</span></span> <span data-ttu-id="15acc-263">(Мы рекомендуем единицу складского хранения VM \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="15acc-263">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="15acc-264">Просмотрите условия ценообразования и лицензирования, а затем поставьте флажок, чтобы указать, что вы согласны с ними.</span><span class="sxs-lookup"><span data-stu-id="15acc-264">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="15acc-265">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="15acc-265">Select **Next**.</span></span>
1. <span data-ttu-id="15acc-266">На странице подтверждения развертывания убедитесь, что сведения правильные и затем выберите **Развернуть**.</span><span class="sxs-lookup"><span data-stu-id="15acc-266">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="15acc-267">Будет возвращено представление **Размещенные в облаке среды**, и ваша среда появится в списке.</span><span class="sxs-lookup"><span data-stu-id="15acc-267">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="15acc-268">Запрошенная среда отобразится в очереди, затем будет развернута.</span><span class="sxs-lookup"><span data-stu-id="15acc-268">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="15acc-269">Для завершения рабочих процессов среды потребуется некоторое время.</span><span class="sxs-lookup"><span data-stu-id="15acc-269">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="15acc-270">Поэтому проверьте примерно через шесть-девять часов.</span><span class="sxs-lookup"><span data-stu-id="15acc-270">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="15acc-271">Перед продолжением убедитесь, что состояние вашей среды — **Развернуто**.</span><span class="sxs-lookup"><span data-stu-id="15acc-271">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-rcsu"></a><span data-ttu-id="15acc-272">Инициализация RCSU</span><span class="sxs-lookup"><span data-stu-id="15acc-272">Initialize RCSU</span></span>

<span data-ttu-id="15acc-273">Чтобы инициализировать RCSU, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="15acc-273">To initialize RCSU, follow these steps.</span></span>

1. <span data-ttu-id="15acc-274">В представлении **Размещенные в облаке среды** выберите свою среду из списка.</span><span class="sxs-lookup"><span data-stu-id="15acc-274">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="15acc-275">Выберите **Полные сведения** в представлении среды с правой стороны.</span><span class="sxs-lookup"><span data-stu-id="15acc-275">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="15acc-276">Появится представление сведений о среде.</span><span class="sxs-lookup"><span data-stu-id="15acc-276">The environment details view appears.</span></span>
1. <span data-ttu-id="15acc-277">В **Компоненты среды** выберите **Управление**.</span><span class="sxs-lookup"><span data-stu-id="15acc-277">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="15acc-278">На вкладке **Retail** выберите **Инициализация**.</span><span class="sxs-lookup"><span data-stu-id="15acc-278">On the **Retail** tab, select **Initialize**.</span></span> <span data-ttu-id="15acc-279">Будет отображено представление параметров инициализации RCSU.</span><span class="sxs-lookup"><span data-stu-id="15acc-279">The RCSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="15acc-280">В поле **Регион** выберите **Восточная часть США**, **Восточная часть США 2**, **Западная часть США** или **Западная часть США 2**.</span><span class="sxs-lookup"><span data-stu-id="15acc-280">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="15acc-281">В поле **Версия** выберите **Укажите версию** в списке, а затем укажите **9.16.19262.5** в поле, которое появляется.</span><span class="sxs-lookup"><span data-stu-id="15acc-281">In the **Version** field, select **Specify a version** in the list, and then specify **9.16.19262.5** in the field that appears.</span></span> <span data-ttu-id="15acc-282">Не забудьте указать точную версию, которая указана здесь.</span><span class="sxs-lookup"><span data-stu-id="15acc-282">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="15acc-283">В противном случае вам придется обновить RCSU до правильной версии позже.</span><span class="sxs-lookup"><span data-stu-id="15acc-283">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="15acc-284">Включите параметр **Применить расширение**.</span><span class="sxs-lookup"><span data-stu-id="15acc-284">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="15acc-285">В списке расширений выберите **Демонстрационное базовое расширение предварительной версии Commerce**.</span><span class="sxs-lookup"><span data-stu-id="15acc-285">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="15acc-286">Выберите **Инициализация**.</span><span class="sxs-lookup"><span data-stu-id="15acc-286">Select **Initialize**.</span></span>
1. <span data-ttu-id="15acc-287">На странице подтверждения развертывания убедитесь, что сведения правильные и затем выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="15acc-287">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="15acc-288">Пользователь возвращается к представлению **Руководство розничного магазина** с выбранной вкладкой **Retail**.</span><span class="sxs-lookup"><span data-stu-id="15acc-288">You're returned to the **Retail management** view, where the **Retail** tab is selected.</span></span> <span data-ttu-id="15acc-289">Ваш RCSU был поставлен в очередь для подготовки.</span><span class="sxs-lookup"><span data-stu-id="15acc-289">Your RCSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="15acc-290">Перед продолжением убедитесь, что состояние RCSU — **Успех**.</span><span class="sxs-lookup"><span data-stu-id="15acc-290">Before you continue, make sure that the status of your RCSU is **Success**.</span></span> <span data-ttu-id="15acc-291">Инициализация занимает примерно два-пять часов.</span><span class="sxs-lookup"><span data-stu-id="15acc-291">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="15acc-292">Инициализация электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="15acc-292">Initialize e-Commerce</span></span>

<span data-ttu-id="15acc-293">Чтобы инициализировать электронную коммерцию, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="15acc-293">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="15acc-294">На вкладке **Электронная коммерция (предварительная версия)** просмотрите согласие на предварительную версию, а затем выберите **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="15acc-294">On the **e-Commerce (Preview)** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="15acc-295">В поле **Имя клиента электронной коммерции** введите имя.</span><span class="sxs-lookup"><span data-stu-id="15acc-295">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="15acc-296">Однако обратите внимание, что это имя появится в некоторых URL-адресах, указывающих на экземпляр электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="15acc-296">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="15acc-297">В поле **Имя Retail Cloud Scale Unit** выберите RCSU в списке.</span><span class="sxs-lookup"><span data-stu-id="15acc-297">In the **Retail cloud scale unit name** field, select your RCSU in the list.</span></span> <span data-ttu-id="15acc-298">(В списке должен быть только один вариант.)</span><span class="sxs-lookup"><span data-stu-id="15acc-298">(The list should have only one option.)</span></span>

    <span data-ttu-id="15acc-299">Поле **География электронной коммерции** задается автоматически, и значение не может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="15acc-299">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="15acc-300">Выберите **Далее** для продолжения.</span><span class="sxs-lookup"><span data-stu-id="15acc-300">Select **Next** to continue.</span></span>
1. <span data-ttu-id="15acc-301">В поле **Поддерживаемые имена узлов** введите любой допустимый домен, например `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="15acc-301">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="15acc-302">В поле **Группа безопасности AAD для системного администратора** введите первые несколько букв названия группы безопасности, которую вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="15acc-302">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="15acc-303">Выберите значок увеличительного стекла для отображения результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="15acc-303">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="15acc-304">Выберите группу безопасности из списка.</span><span class="sxs-lookup"><span data-stu-id="15acc-304">Select a security group from the list.</span></span>
2.  <span data-ttu-id="15acc-305">В поле **Группа безопасности AAD для модератора оценок и отзывов** введите первые несколько букв названия группы безопасности, которую вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="15acc-305">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="15acc-306">Выберите значок увеличительного стекла для отображения результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="15acc-306">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="15acc-307">Выберите группу безопасности из списка.</span><span class="sxs-lookup"><span data-stu-id="15acc-307">Select a security group from the list.</span></span>
1. <span data-ttu-id="15acc-308">Оставьте параметр **Включить службу оценок и отзывов** включенным.</span><span class="sxs-lookup"><span data-stu-id="15acc-308">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="15acc-309">Если вы уже завершили этап согласия Microsoft Azure Active Directory (Azure AD), описанный разделе "Предоставление доступа к приложениям электронной коммерции", выберите флажок, чтобы подтвердить свое согласие.</span><span class="sxs-lookup"><span data-stu-id="15acc-309">If you have already completed the Microsoft Azure Active Directory (Azure AD) consent step as described in the "Grant access to e-Commerce applications" section, select the check box to confirm your consent.</span></span> <span data-ttu-id="15acc-310">Если вы еще не завершили этот шаг, вам нужно сделать это, прежде чем приступить к инициализации.</span><span class="sxs-lookup"><span data-stu-id="15acc-310">If you have not yet completed this step, you need to do that before proceeding with the initialization.</span></span> <span data-ttu-id="15acc-311">Выберите ссылку в тексте рядом с флажком, чтобы открыть диалоговое окно согласия и завершить шаг.</span><span class="sxs-lookup"><span data-stu-id="15acc-311">Select the link within the text next to the check box to open the consent dialog box and complete the step.</span></span>
1. <span data-ttu-id="15acc-312">Выберите **Инициализация**.</span><span class="sxs-lookup"><span data-stu-id="15acc-312">Select **Initialize**.</span></span> <span data-ttu-id="15acc-313">Пользователь возвращается к представлению **Руководство розничного магазина** где выбрана вкладка **Электронная коммерция (предварительная версия)**.</span><span class="sxs-lookup"><span data-stu-id="15acc-313">You're returned to the **Retail management** view, where the **e-Commerce (Preview)** tab is selected.</span></span> <span data-ttu-id="15acc-314">Инициализация электронной коммерции начата.</span><span class="sxs-lookup"><span data-stu-id="15acc-314">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="15acc-315">Перед продолжением необходимо подождать, пока состояние инициализации электронной коммерции не станет **Успешная инициализация**.</span><span class="sxs-lookup"><span data-stu-id="15acc-315">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="15acc-316">В **Ссылки** в нижнем правом углу запишите URL-адреса для следующих ссылок:</span><span class="sxs-lookup"><span data-stu-id="15acc-316">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="15acc-317">**Сайт электронной коммерции** — ссылка на корневой узел вашего сайта электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="15acc-317">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="15acc-318">**Средство управления сайтом электронной коммерции** — ссылка на средство управления сайтом.</span><span class="sxs-lookup"><span data-stu-id="15acc-318">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="15acc-319">Поддержка среды предварительной версии Commerce</span><span class="sxs-lookup"><span data-stu-id="15acc-319">Commerce preview environment support</span></span>

<span data-ttu-id="15acc-320">Если при выполнении шагов подготовки возникают проблемы, обратитесь за помощью в [группу Yammer предварительной версии Microsoft Dynamics 365 Commerce](https://aka.ms/Dynamics365CommercePreviewYammer).</span><span class="sxs-lookup"><span data-stu-id="15acc-320">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

<span data-ttu-id="15acc-321">Если у вас возникли проблемы с получением доступа к группе Yammer, вы можете связаться с Майкрософт по электронной почте <Dynamics365Commerce@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="15acc-321">If you experience issues when you try to access the Yammer group, you can contact Microsoft by email at <Dynamics365Commerce@microsoft.com>.</span></span> <span data-ttu-id="15acc-322">Этот адрес электронной почты не контролируется постоянно.</span><span class="sxs-lookup"><span data-stu-id="15acc-322">This email address isn't actively monitored.</span></span> <span data-ttu-id="15acc-323">Поэтому ожидайте задержки в ответе.</span><span class="sxs-lookup"><span data-stu-id="15acc-323">Therefore, expect a delay in the response.</span></span>

## <a name="next-steps"></a><span data-ttu-id="15acc-324">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="15acc-324">Next steps</span></span>

<span data-ttu-id="15acc-325">Для продолжения процесса предоставления и настройки вашей среды предварительной версии Commerce см. [Настройка среды предварительной версии Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="15acc-325">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="15acc-326">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="15acc-326">Additional resources</span></span>

[<span data-ttu-id="15acc-327">Обзор среды предварительного просмотра Commerce</span><span class="sxs-lookup"><span data-stu-id="15acc-327">Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="15acc-328">Настройка среды предварительного просмотра Commerce</span><span class="sxs-lookup"><span data-stu-id="15acc-328">Configure a Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="15acc-329">Настройка дополнительных функций для среды предварительного просмотра Commerce</span><span class="sxs-lookup"><span data-stu-id="15acc-329">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="15acc-330">Вопросы и ответы среды предварительного просмотра Commerce</span><span class="sxs-lookup"><span data-stu-id="15acc-330">Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="15acc-331">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="15acc-331">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="15acc-332">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="15acc-332">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="15acc-333">Портал Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="15acc-333">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="15acc-334">Веб-сайт Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="15acc-334">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="15acc-335">Справочные ресурсы для Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="15acc-335">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
