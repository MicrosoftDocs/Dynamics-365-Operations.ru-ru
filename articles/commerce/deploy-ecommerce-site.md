---
title: Развертывание нового клиента электронной коммерции
description: В этом разделе описывается, как развернуть новый клиент электронной коммерции, используя службы Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: 6d7dfcaf244260de5f39a1201ec1ea78e94351e7
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001791"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="483c9-103">Развертывание нового клиента электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="483c9-103">Deploy a new e-Commerce tenant</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="483c9-104">В этом разделе описывается, как развернуть новый сайт электронной коммерции, используя службы Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="483c9-104">This topic describes how to deploy a new e-Commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="483c9-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="483c9-105">Overview</span></span>

<span data-ttu-id="483c9-106">Microsoft Dynamics Lifecycle Services (LCS) — это рабочая область совместной работы на основе облака, которую партнеры и клиенты могут использовать для управления проектами и средами, просмотра последних сведений о продуктах и функциях Microsoft Dynamics, а также для создания, отслеживания и просмотра обращений в службу технической поддержки.</span><span class="sxs-lookup"><span data-stu-id="483c9-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="483c9-107">Функции управления электронной коммерцией интегрированы в LCS.</span><span class="sxs-lookup"><span data-stu-id="483c9-107">E-Commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="483c9-108">Дополнительные сведения о LCS см. в [Руководстве пользователя Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="483c9-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="483c9-109">Начало работы</span><span class="sxs-lookup"><span data-stu-id="483c9-109">Get started</span></span>

<span data-ttu-id="483c9-110">Прежде чем можно будет инициализировать электронную коммерцию, необходимо инициализировать проект, среду и Retail Cloud Scale Unit (RCSU).</span><span class="sxs-lookup"><span data-stu-id="483c9-110">Before you can initialize e-Commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="483c9-111">Чтобы выполнить инициализацию в LCS, необходимо иметь разрешения для роли владельца проекта или руководителя среды.</span><span class="sxs-lookup"><span data-stu-id="483c9-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="483c9-112">Поддерживаются топологии производственной среды и песочницы.</span><span class="sxs-lookup"><span data-stu-id="483c9-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="483c9-113">Дополнительные сведения о средах см. в разделе [Планирование среды](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="483c9-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="483c9-114">Дополнительные сведения о RCSU см. в разделе [Инициализация Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="483c9-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="483c9-115">Инициализация электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="483c9-115">Initialize e-Commerce</span></span>

<span data-ttu-id="483c9-116">Эта процедура используется для инициализации функции электронной коммерции в существующей среде.</span><span class="sxs-lookup"><span data-stu-id="483c9-116">Use this procedure to initialize the e-Commerce feature in an existing environment.</span></span>

<span data-ttu-id="483c9-117">Прежде чем начать, убедитесь, что имеются следующие требуемые сведения:</span><span class="sxs-lookup"><span data-stu-id="483c9-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="483c9-118">RCSU, который будет использован.</span><span class="sxs-lookup"><span data-stu-id="483c9-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="483c9-119">Группа безопасности Microsoft Azure Active Directory, которая будет использоваться для системных администраторов электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="483c9-119">The Microsoft Azure Active Directory security group that will be used for e-Commerce system admins.</span></span>
- <span data-ttu-id="483c9-120">Группа безопасности Microsoft Azure Active Directory, которая будет использоваться для модераторов оценок и отзывов.</span><span class="sxs-lookup"><span data-stu-id="483c9-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="483c9-121">Домены, которые будут связаны со средой.</span><span class="sxs-lookup"><span data-stu-id="483c9-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="483c9-122">Кроме того, можно собрать следующие дополнительные сведения:</span><span class="sxs-lookup"><span data-stu-id="483c9-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="483c9-123">Сведения Azure AD B2C:</span><span class="sxs-lookup"><span data-stu-id="483c9-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="483c9-124">Имя владельца.</span><span class="sxs-lookup"><span data-stu-id="483c9-124">Tenant Name.</span></span>
    - <span data-ttu-id="483c9-125">Код клиента.</span><span class="sxs-lookup"><span data-stu-id="483c9-125">Client ID.</span></span>
    - <span data-ttu-id="483c9-126">Пользовательский домен для входа.</span><span class="sxs-lookup"><span data-stu-id="483c9-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="483c9-127">URL-адрес для ответа.</span><span class="sxs-lookup"><span data-stu-id="483c9-127">Reply URL.</span></span>
    - <span data-ttu-id="483c9-128">Идентификатор политики регистрации или входа.</span><span class="sxs-lookup"><span data-stu-id="483c9-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="483c9-129">Код политики сброса пароля.</span><span class="sxs-lookup"><span data-stu-id="483c9-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="483c9-130">Идентификатор политики изменения профиля.</span><span class="sxs-lookup"><span data-stu-id="483c9-130">Edit Profile Policy ID.</span></span>

[!NOTE]
<span data-ttu-id="483c9-131">Эти сведения могут быть добавлены позже через запрос на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="483c9-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="483c9-132">После сбора необходимых сведений выполните следующие действия для инициализации электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="483c9-132">After you've collected the required information, follow these steps to initialize e-Commerce.</span></span>

1. <span data-ttu-id="483c9-133">Войдите в [LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="483c9-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="483c9-134">Откройте проект, содержащий среду, в которой необходимо инициализировать электронную коммерцию.</span><span class="sxs-lookup"><span data-stu-id="483c9-134">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="483c9-135">В разделе **Среды** выберите среду.</span><span class="sxs-lookup"><span data-stu-id="483c9-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="483c9-136">В разделе **Компоненты среды** выберите ссылку **Управление розничной торговлей**.</span><span class="sxs-lookup"><span data-stu-id="483c9-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="483c9-137">На вкладке **Электронная коммерция** выберите **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="483c9-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="483c9-138">Появится диалоговое окно, в котором необходимо ввести сведения, необходимые для подготовки.</span><span class="sxs-lookup"><span data-stu-id="483c9-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="483c9-139">Введите требуемые сведения, затем перейдите к следующей странице.</span><span class="sxs-lookup"><span data-stu-id="483c9-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="483c9-140">На следующей странице заполните требуемые сведения, затем отправьте форму.</span><span class="sxs-lookup"><span data-stu-id="483c9-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="483c9-141">Вы возвращаетесь на вкладку **Электронная коммерция**, где вы должны видеть, что инициализация запущена.</span><span class="sxs-lookup"><span data-stu-id="483c9-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="483c9-142">Чтобы просмотреть статус инициализации, выберите команду **Обновить** или вернитесь на вкладку **Электронная коммерция** позднее.</span><span class="sxs-lookup"><span data-stu-id="483c9-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="483c9-143">При инициализации электронной коммерции из LCS система подготавливает несколько компонентов, необходимых для электронной коммерции, и связывает их со средой.</span><span class="sxs-lookup"><span data-stu-id="483c9-143">When e-Commerce is initialized from LCS, the system provisions several components that are required for e-Commerce and associates them with the environment.</span></span> <span data-ttu-id="483c9-144">После завершения подготовки вкладка **Электронная коммерция** на странице **Управление розничной торговлей** обновляется, чтобы отразить подготовку.</span><span class="sxs-lookup"><span data-stu-id="483c9-144">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="483c9-145">На странице отображаются последние развертывания настроек и статус всех остальных текущих развертываний.</span><span class="sxs-lookup"><span data-stu-id="483c9-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="483c9-146">Она также содержит ссылки на сайт электронной коммерции и построитель сайтов электронной коммерции, где создаются сайты.</span><span class="sxs-lookup"><span data-stu-id="483c9-146">It also includes links to the e-Commerce site and the e-Commerce site builder where sites are authored.</span></span>

## <a name="access-site-builder"></a><span data-ttu-id="483c9-147">Доступ к построителю сайтов</span><span class="sxs-lookup"><span data-stu-id="483c9-147">Access site builder</span></span>

<span data-ttu-id="483c9-148">Для доступа к построителю сайтов перейдите на вкладку **Электронная коммерция** на странице **Управление розничной торговлей** в LCS и выберите ссылку **Средство управления сайтом электронной коммерции**.</span><span class="sxs-lookup"><span data-stu-id="483c9-148">To access site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="483c9-149">Страница построителя сайтов отображает представление на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="483c9-149">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="483c9-150">На этой странице можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="483c9-150">From this page, you can:</span></span>

- <span data-ttu-id="483c9-151">Изменение настроек на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="483c9-151">Modify tenant-level settings.</span></span>
- <span data-ttu-id="483c9-152">Перейти на любой созданный сайт, для которого есть разрешение на просмотр.</span><span class="sxs-lookup"><span data-stu-id="483c9-152">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="483c9-153">Получить доступ к таким функциям, как модерация и отчетность.</span><span class="sxs-lookup"><span data-stu-id="483c9-153">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="483c9-154">Создать новый сайт.</span><span class="sxs-lookup"><span data-stu-id="483c9-154">Create a new site.</span></span> <span data-ttu-id="483c9-155">Дополнительные сведения о создании и развертывание сайта см. в разделе [Создание сайта электронной коммерции](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="483c9-155">For more information about how to create a new site, see [Create an e-Commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="483c9-156">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="483c9-156">Additional resources</span></span>

[<span data-ttu-id="483c9-157">Настройка доменного имени</span><span class="sxs-lookup"><span data-stu-id="483c9-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="483c9-158">Создание сайта электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="483c9-158">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="483c9-159">Связывание веб-сайта с каналом</span><span class="sxs-lookup"><span data-stu-id="483c9-159">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="483c9-160">Управление файлами robots.txt</span><span class="sxs-lookup"><span data-stu-id="483c9-160">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="483c9-161">Настройка специальных страниц для входа пользователей</span><span class="sxs-lookup"><span data-stu-id="483c9-161">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="483c9-162">Добавление поддержки сети доставки контента (CDN)</span><span class="sxs-lookup"><span data-stu-id="483c9-162">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="483c9-163">Включение обнаружения магазинов на основе местоположения</span><span class="sxs-lookup"><span data-stu-id="483c9-163">Enable location-based store detection</span></span>](enable-store-detection.md)
