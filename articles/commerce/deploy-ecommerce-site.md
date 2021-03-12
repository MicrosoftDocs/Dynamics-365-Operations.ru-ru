---
title: Развертывание нового клиента электронной коммерции
description: В этом разделе описывается, как развернуть новый сайт электронной коммерции Dynamics 365 Commerce, используя службы Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3b750ee89a85688dcebe673f9c3ff13693e9fcad
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976746"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="5001c-103">Развертывание нового клиента электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="5001c-103">Deploy a new e-commerce tenant</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5001c-104">В этом разделе описывается, как развернуть новый сайт электронной коммерции Dynamics 365 Commerce, используя службы Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="5001c-104">This topic describes how to deploy a new Dynamics 365 Commerce e-commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="5001c-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="5001c-105">Overview</span></span>

<span data-ttu-id="5001c-106">Microsoft Dynamics Lifecycle Services (LCS) — это рабочая область совместной работы на основе облака, которую партнеры и клиенты могут использовать для управления проектами и средами, просмотра последних сведений о продуктах и функциях Microsoft Dynamics, а также для создания, отслеживания и просмотра обращений в службу технической поддержки.</span><span class="sxs-lookup"><span data-stu-id="5001c-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="5001c-107">Функции управления электронной коммерцией интегрированы в LCS.</span><span class="sxs-lookup"><span data-stu-id="5001c-107">E-commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="5001c-108">Дополнительные сведения о LCS см. в [Руководстве пользователя Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="5001c-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="5001c-109">Начать</span><span class="sxs-lookup"><span data-stu-id="5001c-109">Get started</span></span>

<span data-ttu-id="5001c-110">Прежде чем можно будет инициализировать электронную коммерцию, необходимо инициализировать проект, среду и Retail Cloud Scale Unit (RCSU).</span><span class="sxs-lookup"><span data-stu-id="5001c-110">Before you can initialize e-commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="5001c-111">Чтобы выполнить инициализацию в LCS, необходимо иметь разрешения для роли владельца проекта или руководителя среды.</span><span class="sxs-lookup"><span data-stu-id="5001c-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="5001c-112">Поддерживаются топологии производственной среды и песочницы.</span><span class="sxs-lookup"><span data-stu-id="5001c-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="5001c-113">Дополнительные сведения о средах см. в разделе [Планирование среды](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="5001c-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="5001c-114">Дополнительные сведения о RCSU см. в разделе [Инициализация Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="5001c-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="5001c-115">Инициализация электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="5001c-115">Initialize e-commerce</span></span>

<span data-ttu-id="5001c-116">Эта процедура используется для инициализации функции электронной коммерции в существующей среде.</span><span class="sxs-lookup"><span data-stu-id="5001c-116">Use this procedure to initialize the e-commerce feature in an existing environment.</span></span>

<span data-ttu-id="5001c-117">Прежде чем начать, убедитесь, что имеются следующие требуемые сведения:</span><span class="sxs-lookup"><span data-stu-id="5001c-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="5001c-118">RCSU, который будет использован.</span><span class="sxs-lookup"><span data-stu-id="5001c-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="5001c-119">Группа безопасности Microsoft Azure Active Directory, которая будет использоваться для системных администраторов электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="5001c-119">The Microsoft Azure Active Directory security group that will be used for e-commerce system admins.</span></span>
- <span data-ttu-id="5001c-120">Группа безопасности Microsoft Azure Active Directory, которая будет использоваться для модераторов оценок и отзывов.</span><span class="sxs-lookup"><span data-stu-id="5001c-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="5001c-121">Домены, которые будут связаны со средой.</span><span class="sxs-lookup"><span data-stu-id="5001c-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="5001c-122">Кроме того, можно собрать следующие дополнительные сведения:</span><span class="sxs-lookup"><span data-stu-id="5001c-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="5001c-123">Сведения Azure AD B2C:</span><span class="sxs-lookup"><span data-stu-id="5001c-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="5001c-124">Имя владельца.</span><span class="sxs-lookup"><span data-stu-id="5001c-124">Tenant Name.</span></span>
    - <span data-ttu-id="5001c-125">Код клиента.</span><span class="sxs-lookup"><span data-stu-id="5001c-125">Client ID.</span></span>
    - <span data-ttu-id="5001c-126">Пользовательский домен для входа.</span><span class="sxs-lookup"><span data-stu-id="5001c-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="5001c-127">URL-адрес для ответа.</span><span class="sxs-lookup"><span data-stu-id="5001c-127">Reply URL.</span></span>
    - <span data-ttu-id="5001c-128">Идентификатор политики регистрации или входа.</span><span class="sxs-lookup"><span data-stu-id="5001c-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="5001c-129">Код политики сброса пароля.</span><span class="sxs-lookup"><span data-stu-id="5001c-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="5001c-130">Идентификатор политики изменения профиля.</span><span class="sxs-lookup"><span data-stu-id="5001c-130">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="5001c-131">Эти сведения могут быть добавлены позже через запрос на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="5001c-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="5001c-132">После сбора необходимых сведений выполните следующие действия для инициализации электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="5001c-132">After you've collected the required information, follow these steps to initialize e-commerce.</span></span>

1. <span data-ttu-id="5001c-133">Войдите в [LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="5001c-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="5001c-134">Откройте проект, содержащий среду, в которой необходимо инициализировать электронную коммерцию.</span><span class="sxs-lookup"><span data-stu-id="5001c-134">Open the project that contains the environment where you want to initialize e-commerce.</span></span>
1. <span data-ttu-id="5001c-135">В разделе **Среды** выберите среду.</span><span class="sxs-lookup"><span data-stu-id="5001c-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="5001c-136">В разделе **Компоненты среды** выберите ссылку **Управление розничной торговлей**.</span><span class="sxs-lookup"><span data-stu-id="5001c-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="5001c-137">На вкладке **Электронная коммерция** выберите **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="5001c-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="5001c-138">Появится диалоговое окно, в котором необходимо ввести сведения, необходимые для подготовки.</span><span class="sxs-lookup"><span data-stu-id="5001c-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="5001c-139">Введите требуемые сведения, затем перейдите к следующей странице.</span><span class="sxs-lookup"><span data-stu-id="5001c-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="5001c-140">На следующей странице заполните требуемые сведения, затем отправьте форму.</span><span class="sxs-lookup"><span data-stu-id="5001c-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="5001c-141">Вы возвращаетесь на вкладку **Электронная коммерция**, где вы должны видеть, что инициализация запущена.</span><span class="sxs-lookup"><span data-stu-id="5001c-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="5001c-142">Чтобы просмотреть статус инициализации, выберите команду **Обновить** или вернитесь на вкладку **Электронная коммерция** позднее.</span><span class="sxs-lookup"><span data-stu-id="5001c-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="5001c-143">При инициализации электронной коммерции из LCS система подготавливает несколько компонентов, необходимых для электронной коммерции, и связывает их со средой.</span><span class="sxs-lookup"><span data-stu-id="5001c-143">When e-commerce is initialized from LCS, the system provisions several components that are required for e-commerce and associates them with the environment.</span></span> <span data-ttu-id="5001c-144">После завершения подготовки вкладка **Электронная коммерция** на странице **Управление розничной торговлей** обновляется, чтобы отразить подготовку.</span><span class="sxs-lookup"><span data-stu-id="5001c-144">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="5001c-145">На странице отображаются последние развертывания настроек и статус всех остальных текущих развертываний.</span><span class="sxs-lookup"><span data-stu-id="5001c-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="5001c-146">Она также содержит ссылки на сайт электронной коммерции и построитель сайтов электронной коммерции, где создаются сайты.</span><span class="sxs-lookup"><span data-stu-id="5001c-146">It also includes links to the e-commerce site and the Commerce site builder where sites are authored.</span></span>

## <a name="access-commerce-site-builder"></a><span data-ttu-id="5001c-147">Доступ к построителю сайтов Commerce</span><span class="sxs-lookup"><span data-stu-id="5001c-147">Access Commerce site builder</span></span>

<span data-ttu-id="5001c-148">Для доступа к построителю сайтов Commerce перейдите на вкладку **Электронная коммерция** на странице **Управление розничной торговлей** в LCS и выберите ссылку **Средство управления сайтом электронной коммерции**.</span><span class="sxs-lookup"><span data-stu-id="5001c-148">To access Commerce site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="5001c-149">Страница построителя сайтов отображает представление на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="5001c-149">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="5001c-150">На этой странице можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5001c-150">From this page, you can:</span></span>

- <span data-ttu-id="5001c-151">Изменение настроек на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="5001c-151">Modify tenant-level settings.</span></span>
- <span data-ttu-id="5001c-152">Перейти на любой созданный сайт, для которого есть разрешение на просмотр.</span><span class="sxs-lookup"><span data-stu-id="5001c-152">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="5001c-153">Получить доступ к таким функциям, как модерация и отчетность.</span><span class="sxs-lookup"><span data-stu-id="5001c-153">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="5001c-154">Создать новый сайт.</span><span class="sxs-lookup"><span data-stu-id="5001c-154">Create a new site.</span></span> <span data-ttu-id="5001c-155">Дополнительные сведения о создании и развертывание сайта см. в разделе [Создание сайта электронной коммерции](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="5001c-155">For more information about how to create a new site, see [Create an e-commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="5001c-156">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5001c-156">Additional resources</span></span>

[<span data-ttu-id="5001c-157">Настройка доменного имени</span><span class="sxs-lookup"><span data-stu-id="5001c-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="5001c-158">Создание сайта электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="5001c-158">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="5001c-159">Связывание сайта Dynamics 365 Commerce с интернет-каналом</span><span class="sxs-lookup"><span data-stu-id="5001c-159">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="5001c-160">Управление файлами robots.txt</span><span class="sxs-lookup"><span data-stu-id="5001c-160">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="5001c-161">Пакетная отправка перенаправлений URL-адресов</span><span class="sxs-lookup"><span data-stu-id="5001c-161">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="5001c-162">Настройка клиента B2C в Commerce</span><span class="sxs-lookup"><span data-stu-id="5001c-162">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="5001c-163">Настройка специальных страниц для входа пользователей</span><span class="sxs-lookup"><span data-stu-id="5001c-163">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="5001c-164">Настройка нескольких клиентов B2C в среде Commerce</span><span class="sxs-lookup"><span data-stu-id="5001c-164">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="5001c-165">Добавление поддержки сети доставки контента (CDN)</span><span class="sxs-lookup"><span data-stu-id="5001c-165">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="5001c-166">Включение обнаружения магазинов на основе местоположения</span><span class="sxs-lookup"><span data-stu-id="5001c-166">Enable location-based store detection</span></span>](enable-store-detection.md)
