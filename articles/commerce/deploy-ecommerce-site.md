---
title: Развертывание нового клиента электронной коммерции
description: В этом разделе описывается, как развернуть новый клиент электронной коммерции, используя службы Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c2632632b9b21dd3a88e9a4df0e65cfd28e579d2
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697459"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="39da9-103">Развертывание нового клиента электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="39da9-103">Deploy a new e-Commerce tenant</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="39da9-104">В этом разделе описывается, как развернуть новый сайт электронной коммерции, используя службы Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="39da9-104">This topic describes how to deploy a new e-Commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="39da9-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="39da9-105">Overview</span></span>
    
<span data-ttu-id="39da9-106">Microsoft Dynamics Lifecycle Services (LCS) — это рабочая область совместной работы на основе облака, которую партнеры и клиенты могут использовать для управления проектами и средами, просмотра последних сведений о продуктах и функциях Microsoft Dynamics, а также для создания, отслеживания и просмотра обращений в службу технической поддержки.</span><span class="sxs-lookup"><span data-stu-id="39da9-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="39da9-107">Функции управления электронной коммерцией интегрированы в LCS.</span><span class="sxs-lookup"><span data-stu-id="39da9-107">E-Commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="39da9-108">Дополнительные сведения о LCS см. в [Руководстве пользователя Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="39da9-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="39da9-109">Начало работы</span><span class="sxs-lookup"><span data-stu-id="39da9-109">Get started</span></span>

<span data-ttu-id="39da9-110">Прежде чем можно будет инициализировать электронную коммерцию, необходимо инициализировать проект, среду и Retail Cloud Scale Unit (RCSU).</span><span class="sxs-lookup"><span data-stu-id="39da9-110">Before you can initialize e-Commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="39da9-111">Чтобы выполнить инициализацию в LCS, необходимо иметь разрешения для роли владельца проекта или руководителя среды.</span><span class="sxs-lookup"><span data-stu-id="39da9-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="39da9-112">Поддерживаются топологии производственной среды и песочницы.</span><span class="sxs-lookup"><span data-stu-id="39da9-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="39da9-113">Дополнительные сведения о средах см. в разделе [Планирование среды](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="39da9-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="39da9-114">Дополнительные сведения о RCSU см. в разделе [Инициализация Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="39da9-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="39da9-115">Инициализация электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="39da9-115">Initialize e-Commerce</span></span>

<span data-ttu-id="39da9-116">Эта процедура используется для инициализации функции электронной коммерции в существующей среде.</span><span class="sxs-lookup"><span data-stu-id="39da9-116">Use this procedure to initialize the e-Commerce feature in an existing environment.</span></span>

<span data-ttu-id="39da9-117">Прежде чем начать, убедитесь, что имеются следующие требуемые сведения:</span><span class="sxs-lookup"><span data-stu-id="39da9-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="39da9-118">RCSU, который будет использован.</span><span class="sxs-lookup"><span data-stu-id="39da9-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="39da9-119">Группа безопасности Microsoft Azure Active Directory, которая будет использоваться для системных администраторов электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="39da9-119">The Microsoft Azure Active Directory security group that will be used for e-Commerce system admins.</span></span>
- <span data-ttu-id="39da9-120">Группа безопасности Microsoft Azure Active Directory, которая будет использоваться для модераторов оценок и отзывов.</span><span class="sxs-lookup"><span data-stu-id="39da9-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="39da9-121">Домены, которые будут связаны со средой.</span><span class="sxs-lookup"><span data-stu-id="39da9-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="39da9-122">Кроме того, можно собрать следующие дополнительные сведения:</span><span class="sxs-lookup"><span data-stu-id="39da9-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="39da9-123">Сведения Azure AD B2C:</span><span class="sxs-lookup"><span data-stu-id="39da9-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="39da9-124">Имя владельца.</span><span class="sxs-lookup"><span data-stu-id="39da9-124">Tenant Name.</span></span>
    - <span data-ttu-id="39da9-125">Код клиента.</span><span class="sxs-lookup"><span data-stu-id="39da9-125">Client ID.</span></span>
    - <span data-ttu-id="39da9-126">Пользовательский домен для входа.</span><span class="sxs-lookup"><span data-stu-id="39da9-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="39da9-127">URL-адрес для ответа.</span><span class="sxs-lookup"><span data-stu-id="39da9-127">Reply URL.</span></span>
    - <span data-ttu-id="39da9-128">Идентификатор политики регистрации или входа.</span><span class="sxs-lookup"><span data-stu-id="39da9-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="39da9-129">Код политики сброса пароля.</span><span class="sxs-lookup"><span data-stu-id="39da9-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="39da9-130">Идентификатор политики изменения профиля.</span><span class="sxs-lookup"><span data-stu-id="39da9-130">Edit Profile Policy ID.</span></span>

[!NOTE]
<span data-ttu-id="39da9-131">Эти сведения могут быть добавлены позже через запрос на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="39da9-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="39da9-132">После сбора необходимых сведений выполните следующие действия для инициализации электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="39da9-132">After you've collected the required information, follow these steps to initialize e-Commerce.</span></span>

1. <span data-ttu-id="39da9-133">Войдите в [LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="39da9-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="39da9-134">Откройте проект, содержащий среду, в которой необходимо инициализировать электронную коммерцию.</span><span class="sxs-lookup"><span data-stu-id="39da9-134">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="39da9-135">В разделе **Среды** выберите среду.</span><span class="sxs-lookup"><span data-stu-id="39da9-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="39da9-136">В разделе **Компоненты среды** выберите ссылку **Управление розничной торговлей**.</span><span class="sxs-lookup"><span data-stu-id="39da9-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="39da9-137">На вкладке **Электронная коммерция** выберите **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="39da9-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="39da9-138">Появится диалоговое окно, в котором необходимо ввести сведения, необходимые для подготовки.</span><span class="sxs-lookup"><span data-stu-id="39da9-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="39da9-139">Введите требуемые сведения, затем перейдите к следующей странице.</span><span class="sxs-lookup"><span data-stu-id="39da9-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="39da9-140">На следующей странице заполните требуемые сведения, затем отправьте форму.</span><span class="sxs-lookup"><span data-stu-id="39da9-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="39da9-141">Вы возвращаетесь на вкладку **Электронная коммерция**, где вы должны видеть, что инициализация запущена.</span><span class="sxs-lookup"><span data-stu-id="39da9-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="39da9-142">Чтобы просмотреть статус инициализации, выберите команду **Обновить** или вернитесь на вкладку **Электронная коммерция** позднее.</span><span class="sxs-lookup"><span data-stu-id="39da9-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="39da9-143">При инициализации электронной коммерции из LCS система подготавливает несколько компонентов, необходимых для электронной коммерции, и связывает их со средой.</span><span class="sxs-lookup"><span data-stu-id="39da9-143">When e-Commerce is initialized from LCS, the system provisions several components that are required for e-Commerce and associates them with the environment.</span></span> <span data-ttu-id="39da9-144">После завершения подготовки вкладка **Электронная коммерция** на странице **Управление розничной торговлей** обновляется, чтобы отразить подготовку.</span><span class="sxs-lookup"><span data-stu-id="39da9-144">After provisioning is completed, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="39da9-145">На странице отображаются последние развертывания настроек и статус всех остальных текущих развертываний.</span><span class="sxs-lookup"><span data-stu-id="39da9-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="39da9-146">Она также содержит ссылки на сайт электронной коммерции и средство управления сайтом электронной коммерции (инструмент разработки).</span><span class="sxs-lookup"><span data-stu-id="39da9-146">It also includes links to the e-Commerce site and the e-Commerce site management tool (the authoring tool).</span></span>

## <a name="access-the-authoring-environment"></a><span data-ttu-id="39da9-147">Доступ к среде разработки</span><span class="sxs-lookup"><span data-stu-id="39da9-147">Access the authoring environment</span></span>

<span data-ttu-id="39da9-148">Чтобы получить доступ к среде разработки, перейдите на вкладку **Электронная коммерция** на странице **Управление розничной торговлей**.</span><span class="sxs-lookup"><span data-stu-id="39da9-148">To access the authoring environment, go to the **e-Commerce** tab on the **Retail management** page.</span></span> <span data-ttu-id="39da9-149">Здесь вы увидите ссылки на сайт электронной коммерции и средство управления сайтом.</span><span class="sxs-lookup"><span data-stu-id="39da9-149">There, you will find links to your e-Commerce site and the site management tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="39da9-150">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="39da9-150">Additional resources</span></span>

[<span data-ttu-id="39da9-151">Обзор интернет-магазина</span><span class="sxs-lookup"><span data-stu-id="39da9-151">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="39da9-152">Создание сайта электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="39da9-152">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="39da9-153">Связывание веб-сайта с каналом</span><span class="sxs-lookup"><span data-stu-id="39da9-153">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="39da9-154">Настройка доменного имени</span><span class="sxs-lookup"><span data-stu-id="39da9-154">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="39da9-155">Добавление поддержки сети доставки контента (CDN)</span><span class="sxs-lookup"><span data-stu-id="39da9-155">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="39da9-156">Включение обнаружения магазинов на основе местоположения</span><span class="sxs-lookup"><span data-stu-id="39da9-156">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="39da9-157">Настройка специальных страниц для входа пользователей</span><span class="sxs-lookup"><span data-stu-id="39da9-157">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)
