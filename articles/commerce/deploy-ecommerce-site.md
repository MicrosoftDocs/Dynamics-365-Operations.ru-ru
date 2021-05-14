---
title: Развертывание нового клиента электронной коммерции
description: В этом разделе описывается, как развернуть новый сайт электронной коммерции Dynamics 365 Commerce, используя службы Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6b228babfd32a4191eeed2a6d924a8b99f1a5311
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936714"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="85a90-103">Развертывание нового клиента электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="85a90-103">Deploy a new e-commerce tenant</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="85a90-104">В этом разделе описывается, как развернуть новый сайт электронной коммерции Dynamics 365 Commerce, используя службы Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="85a90-104">This topic describes how to deploy a new Dynamics 365 Commerce e-commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="85a90-105">Microsoft Dynamics Lifecycle Services (LCS) — это рабочая область совместной работы на основе облака, которую партнеры и клиенты могут использовать для управления проектами и средами, просмотра последних сведений о продуктах и функциях Microsoft Dynamics, а также для создания, отслеживания и просмотра обращений в службу технической поддержки.</span><span class="sxs-lookup"><span data-stu-id="85a90-105">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="85a90-106">Функции управления электронной коммерцией интегрированы в LCS.</span><span class="sxs-lookup"><span data-stu-id="85a90-106">E-commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="85a90-107">Дополнительные сведения о LCS см. в [Руководстве пользователя Lifecycle Services](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="85a90-107">To learn more about LCS, see the [Lifecycle Services User Guide](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="85a90-108">Начать</span><span class="sxs-lookup"><span data-stu-id="85a90-108">Get started</span></span>

<span data-ttu-id="85a90-109">Прежде чем можно будет инициализировать электронную коммерцию, необходимо инициализировать проект, среду и Retail Cloud Scale Unit (RCSU).</span><span class="sxs-lookup"><span data-stu-id="85a90-109">Before you can initialize e-commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="85a90-110">Чтобы выполнить инициализацию в LCS, необходимо иметь разрешения для роли владельца проекта или руководителя среды.</span><span class="sxs-lookup"><span data-stu-id="85a90-110">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="85a90-111">Поддерживаются топологии производственной среды и песочницы.</span><span class="sxs-lookup"><span data-stu-id="85a90-111">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="85a90-112">Дополнительные сведения о средах см. в разделе [Планирование среды](/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="85a90-112">For more information about environments, see [Environment planning](/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="85a90-113">Дополнительные сведения о RCSU см. в разделе [Инициализация Retail Cloud Scale Unit](/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="85a90-113">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="85a90-114">Инициализация электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="85a90-114">Initialize e-commerce</span></span>

<span data-ttu-id="85a90-115">Эта процедура используется для инициализации функции электронной коммерции в существующей среде.</span><span class="sxs-lookup"><span data-stu-id="85a90-115">Use this procedure to initialize the e-commerce feature in an existing environment.</span></span>

<span data-ttu-id="85a90-116">Прежде чем начать, убедитесь, что имеются следующие требуемые сведения:</span><span class="sxs-lookup"><span data-stu-id="85a90-116">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="85a90-117">RCSU, который будет использован.</span><span class="sxs-lookup"><span data-stu-id="85a90-117">The RCSU that will be used.</span></span>
- <span data-ttu-id="85a90-118">Группа безопасности Microsoft Azure Active Directory, которая будет использоваться для системных администраторов электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="85a90-118">The Microsoft Azure Active Directory security group that will be used for e-commerce system admins.</span></span>
- <span data-ttu-id="85a90-119">Группа безопасности Microsoft Azure Active Directory, которая будет использоваться для модераторов оценок и отзывов.</span><span class="sxs-lookup"><span data-stu-id="85a90-119">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="85a90-120">Домены, которые будут связаны со средой.</span><span class="sxs-lookup"><span data-stu-id="85a90-120">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="85a90-121">Кроме того, можно собрать следующие дополнительные сведения:</span><span class="sxs-lookup"><span data-stu-id="85a90-121">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="85a90-122">Сведения Azure AD B2C:</span><span class="sxs-lookup"><span data-stu-id="85a90-122">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="85a90-123">Имя владельца.</span><span class="sxs-lookup"><span data-stu-id="85a90-123">Tenant Name.</span></span>
    - <span data-ttu-id="85a90-124">Код клиента.</span><span class="sxs-lookup"><span data-stu-id="85a90-124">Client ID.</span></span>
    - <span data-ttu-id="85a90-125">Пользовательский домен для входа.</span><span class="sxs-lookup"><span data-stu-id="85a90-125">Login Custom Domain.</span></span>
    - <span data-ttu-id="85a90-126">URL-адрес для ответа.</span><span class="sxs-lookup"><span data-stu-id="85a90-126">Reply URL.</span></span>
    - <span data-ttu-id="85a90-127">Идентификатор политики регистрации или входа.</span><span class="sxs-lookup"><span data-stu-id="85a90-127">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="85a90-128">Код политики сброса пароля.</span><span class="sxs-lookup"><span data-stu-id="85a90-128">Reset password Policy ID.</span></span>
    - <span data-ttu-id="85a90-129">Идентификатор политики изменения профиля.</span><span class="sxs-lookup"><span data-stu-id="85a90-129">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="85a90-130">Эти сведения могут быть добавлены позже через запрос на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="85a90-130">This information can be added later, through a service request.</span></span>

<span data-ttu-id="85a90-131">После сбора необходимых сведений выполните следующие действия для инициализации электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="85a90-131">After you've collected the required information, follow these steps to initialize e-commerce.</span></span>

1. <span data-ttu-id="85a90-132">Войдите в [LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="85a90-132">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="85a90-133">Откройте проект, содержащий среду, в которой необходимо инициализировать электронную коммерцию.</span><span class="sxs-lookup"><span data-stu-id="85a90-133">Open the project that contains the environment where you want to initialize e-commerce.</span></span>
1. <span data-ttu-id="85a90-134">В разделе **Среды** выберите среду.</span><span class="sxs-lookup"><span data-stu-id="85a90-134">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="85a90-135">В разделе **Компоненты среды** выберите ссылку **Управление розничной торговлей**.</span><span class="sxs-lookup"><span data-stu-id="85a90-135">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="85a90-136">На вкладке **Электронная коммерция** выберите **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="85a90-136">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="85a90-137">Появится диалоговое окно, в котором необходимо ввести сведения, необходимые для подготовки.</span><span class="sxs-lookup"><span data-stu-id="85a90-137">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="85a90-138">Введите требуемые сведения, затем перейдите к следующей странице.</span><span class="sxs-lookup"><span data-stu-id="85a90-138">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="85a90-139">На следующей странице заполните требуемые сведения, затем отправьте форму.</span><span class="sxs-lookup"><span data-stu-id="85a90-139">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="85a90-140">Вы возвращаетесь на вкладку **Электронная коммерция**, где вы должны видеть, что инициализация запущена.</span><span class="sxs-lookup"><span data-stu-id="85a90-140">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="85a90-141">Чтобы просмотреть статус инициализации, выберите команду **Обновить** или вернитесь на вкладку **Электронная коммерция** позднее.</span><span class="sxs-lookup"><span data-stu-id="85a90-141">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="85a90-142">При инициализации электронной коммерции из LCS система подготавливает несколько компонентов, необходимых для электронной коммерции, и связывает их со средой.</span><span class="sxs-lookup"><span data-stu-id="85a90-142">When e-commerce is initialized from LCS, the system provisions several components that are required for e-commerce and associates them with the environment.</span></span> <span data-ttu-id="85a90-143">После завершения подготовки вкладка **Электронная коммерция** на странице **Управление розничной торговлей** обновляется, чтобы отразить подготовку.</span><span class="sxs-lookup"><span data-stu-id="85a90-143">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="85a90-144">На странице отображаются последние развертывания настроек и статус всех остальных текущих развертываний.</span><span class="sxs-lookup"><span data-stu-id="85a90-144">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="85a90-145">Она также содержит ссылки на сайт электронной коммерции и построитель сайтов электронной коммерции, где создаются сайты.</span><span class="sxs-lookup"><span data-stu-id="85a90-145">It also includes links to the e-commerce site and the Commerce site builder where sites are authored.</span></span>

## <a name="access-commerce-site-builder"></a><span data-ttu-id="85a90-146">Доступ к построителю сайтов Commerce</span><span class="sxs-lookup"><span data-stu-id="85a90-146">Access Commerce site builder</span></span>

<span data-ttu-id="85a90-147">Для доступа к построителю сайтов Commerce перейдите на вкладку **Электронная коммерция** на странице **Управление розничной торговлей** в LCS и выберите ссылку **Средство управления сайтом электронной коммерции**.</span><span class="sxs-lookup"><span data-stu-id="85a90-147">To access Commerce site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="85a90-148">Страница построителя сайтов отображает представление на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="85a90-148">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="85a90-149">На этой странице можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="85a90-149">From this page, you can:</span></span>

- <span data-ttu-id="85a90-150">Изменение настроек на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="85a90-150">Modify tenant-level settings.</span></span>
- <span data-ttu-id="85a90-151">Перейти на любой созданный сайт, для которого есть разрешение на просмотр.</span><span class="sxs-lookup"><span data-stu-id="85a90-151">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="85a90-152">Получить доступ к таким функциям, как модерация и отчетность.</span><span class="sxs-lookup"><span data-stu-id="85a90-152">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="85a90-153">Создать новый сайт.</span><span class="sxs-lookup"><span data-stu-id="85a90-153">Create a new site.</span></span> <span data-ttu-id="85a90-154">Дополнительные сведения о создании и развертывание сайта см. в разделе [Создание сайта электронной коммерции](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="85a90-154">For more information about how to create a new site, see [Create an e-commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="85a90-155">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="85a90-155">Additional resources</span></span>

[<span data-ttu-id="85a90-156">Настройка доменного имени</span><span class="sxs-lookup"><span data-stu-id="85a90-156">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="85a90-157">Создание сайта электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="85a90-157">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="85a90-158">Связывание сайта Dynamics 365 Commerce с интернет-каналом</span><span class="sxs-lookup"><span data-stu-id="85a90-158">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="85a90-159">Управление файлами robots.txt</span><span class="sxs-lookup"><span data-stu-id="85a90-159">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="85a90-160">Пакетная отправка перенаправлений URL-адресов</span><span class="sxs-lookup"><span data-stu-id="85a90-160">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="85a90-161">Настройка клиента B2C в Commerce</span><span class="sxs-lookup"><span data-stu-id="85a90-161">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="85a90-162">Настройка специальных страниц для входа пользователей</span><span class="sxs-lookup"><span data-stu-id="85a90-162">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="85a90-163">Настройка нескольких клиентов B2C в среде Commerce</span><span class="sxs-lookup"><span data-stu-id="85a90-163">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="85a90-164">Добавление поддержки сети доставки контента (CDN)</span><span class="sxs-lookup"><span data-stu-id="85a90-164">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="85a90-165">Включение обнаружения магазинов на основе местоположения</span><span class="sxs-lookup"><span data-stu-id="85a90-165">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]