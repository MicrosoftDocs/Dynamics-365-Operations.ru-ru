---
title: Обеспечение среды оценки Dynamics 365 Commerce
description: В этой теме объясняется, как подготовить ознакомительную среду Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 19cedf01d1b916de785454d55448f41d1f5db1df
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792299"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="59ad1-103">Обеспечение среды оценки Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="59ad1-103">Provision a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="59ad1-104">В этой теме объясняется, как подготовить ознакомительную среду Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="59ad1-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="59ad1-105">Прежде чем начать, рекомендуется выполнить быструю проверку данного раздела, чтобы понять, что именно требуется для этого процесса.</span><span class="sxs-lookup"><span data-stu-id="59ad1-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="59ad1-106">Ознакомительные среды Commerce не являются общедоступными и предоставляются партнерам и клиентам по запросам по запросу.</span><span class="sxs-lookup"><span data-stu-id="59ad1-106">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="59ad1-107">Для получения дополнительных сведений обратитесь к своему контакту Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="59ad1-107">For more information, reach out to your Microsoft partner contact.</span></span>

<span data-ttu-id="59ad1-108">Чтобы успешно предоставить ознакомительную среду Commerce, необходимо создать проект с определенным названием и типом продукта.</span><span class="sxs-lookup"><span data-stu-id="59ad1-108">To successfully provision a Commerce evaluation environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="59ad1-109">У среды и Commerce Scale Unit (CSU) также есть некоторые специальные параметры, которые необходимо использовать, если вы планируете подготовить электронную коммерцию позже.</span><span class="sxs-lookup"><span data-stu-id="59ad1-109">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you expect to provision e-Commerce later.</span></span> <span data-ttu-id="59ad1-110">Инструкции в этой теме описывают все необходимые шаги, которые вы должны выполнить, и параметры, которые вы должны использовать.</span><span class="sxs-lookup"><span data-stu-id="59ad1-110">The instructions in this topic describe all the steps that are required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="59ad1-111">После успешного предоставления ознакомительной среды Commerce необходимо выполнить несколько шагов после подготовки, чтобы подготовить ее к использованию.</span><span class="sxs-lookup"><span data-stu-id="59ad1-111">After you successfully provision your Commerce evaluation environment, you must complete a few post-provisioning steps to prepare it for use.</span></span> <span data-ttu-id="59ad1-112">Некоторые шаги являются необязательными, в зависимости от того, какие аспекты системы вы хотите оценить.</span><span class="sxs-lookup"><span data-stu-id="59ad1-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="59ad1-113">Вы всегда можете выполнить дополнительные шаги позже.</span><span class="sxs-lookup"><span data-stu-id="59ad1-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="59ad1-114">Для получения информации о том, как настроить ознакомительную среду Commerce после подготовки, см. в [Настройка ознакомительной среды Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="59ad1-114">For information about how to configure your Commerce evaluation environment after you provision it, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="59ad1-115">Для сведений о том, как настроить дополнительные функции для ознакомительной среды Commerce, см. [Настройка дополнительных функций для ознакомительной среды Commerce](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="59ad1-115">For information about how to configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="59ad1-116">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="59ad1-116">Prerequisites</span></span>

<span data-ttu-id="59ad1-117">Для того, чтобы предоставить ознакомительную среду Commerce, необходимо предусмотреть следующие предварительные условия:</span><span class="sxs-lookup"><span data-stu-id="59ad1-117">The following prerequisites must be in place before you can provision your Commerce evaluation environment:</span></span>

- <span data-ttu-id="59ad1-118">Вы присоединились к программе оценки и получили емкость для оценочной среды.</span><span class="sxs-lookup"><span data-stu-id="59ad1-118">You have been onboarded into the evaluation program and granted capacity for an evaluation environment.</span></span>
- <span data-ttu-id="59ad1-119">У вас есть доступ к порталу Lifecycle Services Microsoft Dynamics (LCS)</span><span class="sxs-lookup"><span data-stu-id="59ad1-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="59ad1-120">Вы являетесь существующим партнером или клиентом Microsoft Dynamics 365 и можете создать проект Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="59ad1-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="59ad1-121">У вас есть права администратора на доступ к вашей подписке Microsoft Azure, либо вы находитесь в контакте с администратором подписки, который может помочь вам в случае необходимости.</span><span class="sxs-lookup"><span data-stu-id="59ad1-121">You have administrator access to your Microsoft Azure subscription, or you're in contact with a subscription administrator who can assist you if required.</span></span>
- <span data-ttu-id="59ad1-122">В вас есть доступный код клиента Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="59ad1-122">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="59ad1-123">Вы создали группу безопасности Azure AD, которую можно использовать в качестве группы администраторов системы электронной коммерции, и у вас есть ее идентификатор.</span><span class="sxs-lookup"><span data-stu-id="59ad1-123">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="59ad1-124">Вы создали группу безопасности Azure AD, которую можно использовать в качестве группы модератора оценок и рецензий, и у вас есть ее идентификатор.</span><span class="sxs-lookup"><span data-stu-id="59ad1-124">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="59ad1-125">(Эта группа безопасности может быть такой же, как группа администрирования системы электронной коммерции.)</span><span class="sxs-lookup"><span data-stu-id="59ad1-125">(This security group can be the same as the e-Commerce system admin group.)</span></span>

<span data-ttu-id="59ad1-126">Обратите внимание, что этот список не является исчерпывающим.</span><span class="sxs-lookup"><span data-stu-id="59ad1-126">Note that this list isn't exhaustive.</span></span> <span data-ttu-id="59ad1-127">При возникновении каких-либо проблем обратитесь за помощью к партнеру корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="59ad1-127">If you experience any issues, reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="provision-your-commerce-evaluation-environment"></a><span data-ttu-id="59ad1-128">Обеспечение своей ознакомительной среды Commerce</span><span class="sxs-lookup"><span data-stu-id="59ad1-128">Provision your Commerce evaluation environment</span></span>

<span data-ttu-id="59ad1-129">Эти процедуры объясняют, как обеспечить ознакомительную среду Commerce.</span><span class="sxs-lookup"><span data-stu-id="59ad1-129">These procedures explain how to provision a Commerce evaluation environment.</span></span> <span data-ttu-id="59ad1-130">После их успешного завершения ознакомительная среда Commerce будет готова к настройке.</span><span class="sxs-lookup"><span data-stu-id="59ad1-130">After you successfully complete them, the Commerce evaluation environment will be ready for configuration.</span></span> <span data-ttu-id="59ad1-131">Все действия, описанные здесь, выполняются на портале LCS.</span><span class="sxs-lookup"><span data-stu-id="59ad1-131">All the activities that are described here occur in the LCS portal.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="59ad1-132">Создать новый проект</span><span class="sxs-lookup"><span data-stu-id="59ad1-132">Create a new project</span></span>

<span data-ttu-id="59ad1-133">Чтобы создать новый проект в LCS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="59ad1-133">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="59ad1-134">На главной странице LCS выберите знак плюса (**+**) для создания проекта.</span><span class="sxs-lookup"><span data-stu-id="59ad1-134">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="59ad1-135">В правой области выполните один из следующих шагов:</span><span class="sxs-lookup"><span data-stu-id="59ad1-135">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="59ad1-136">Если вы являетесь партнером, выберите **Миграция, создание решений и знакомство**.</span><span class="sxs-lookup"><span data-stu-id="59ad1-136">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="59ad1-137">Если вы клиент, выберите **Перспективный клиент — предпродажная подготовка**.</span><span class="sxs-lookup"><span data-stu-id="59ad1-137">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="59ad1-138">Введите название, описание и отрасль.</span><span class="sxs-lookup"><span data-stu-id="59ad1-138">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="59ad1-139">В поле **Наименование продукта** выберите **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="59ad1-139">In the **Product name** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="59ad1-140">В поле **Версия продукта** выберите **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="59ad1-140">In the **Product version** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="59ad1-141">В поле **Методология** выберите **Методология реализации Dynamics Retail**.</span><span class="sxs-lookup"><span data-stu-id="59ad1-141">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="59ad1-142">Необязательно: можно импортировать роли и пользователей из существующего проекта.</span><span class="sxs-lookup"><span data-stu-id="59ad1-142">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="59ad1-143">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="59ad1-143">Select **Create**.</span></span> <span data-ttu-id="59ad1-144">Появится представление проекта.</span><span class="sxs-lookup"><span data-stu-id="59ad1-144">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="59ad1-145">Добавление соединителя Azure</span><span class="sxs-lookup"><span data-stu-id="59ad1-145">Add the Azure Connector</span></span>

<span data-ttu-id="59ad1-146">Чтобы добавить соединитель Azure в проект LCS, выполните шаги из раздела [Выполнение процесса адаптации Azure Resource Manager (ARM)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span><span class="sxs-lookup"><span data-stu-id="59ad1-146">To add the Azure Connector to your LCS project, follow the steps in [Complete the Azure Resource Manager (ARM) onboarding process](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span></span>

### <a name="deploy-the-environment"></a><span data-ttu-id="59ad1-147">Развернуть среду</span><span class="sxs-lookup"><span data-stu-id="59ad1-147">Deploy the environment</span></span>

<span data-ttu-id="59ad1-148">Выполните следующие действия, чтобы развернуть среду.</span><span class="sxs-lookup"><span data-stu-id="59ad1-148">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="59ad1-149">Возможно, вам не придется выполнять шаги 6, 7 и/или 8, потому что страницы с одним вариантом пропускаются.</span><span class="sxs-lookup"><span data-stu-id="59ad1-149">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="59ad1-150">Когда вы находитесь в представлении **Параметры среды**, подтвердите, что текст **Dynamics 365 Commerce — демонстрация (10.0.* x* с обновлением платформы *xx*)\*\* отображается непосредственно над полем **Имя среды**.</span><span class="sxs-lookup"><span data-stu-id="59ad1-150">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="59ad1-151">Сведения см. на изображении, которое появляется после шага 8.</span><span class="sxs-lookup"><span data-stu-id="59ad1-151">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="59ad1-152">В верхнем меню выберите **Размещенные в облаке среды**.</span><span class="sxs-lookup"><span data-stu-id="59ad1-152">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="59ad1-153">Выберите **Добавить**, чтобы добавить среду.</span><span class="sxs-lookup"><span data-stu-id="59ad1-153">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="59ad1-154">В поле **Версия приложения** выберите самую последнюю версию.</span><span class="sxs-lookup"><span data-stu-id="59ad1-154">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="59ad1-155">Если требуется выбрать версию приложения, отличающуюся от самой последней версии, не выбирайте версию, предшествующую **10.0.14**.</span><span class="sxs-lookup"><span data-stu-id="59ad1-155">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.14**.</span></span>
1. <span data-ttu-id="59ad1-156">В поле **Версия платформы** используйте версию платформы, которая выбирается автоматически для выбранной версии приложения.</span><span class="sxs-lookup"><span data-stu-id="59ad1-156">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Выбор приложения и версий платформы](./media/project1.png)

1. <span data-ttu-id="59ad1-158">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="59ad1-158">Select **Next**.</span></span>
1. <span data-ttu-id="59ad1-159">Выберите **Демонстрация** в качестве топологии среды.</span><span class="sxs-lookup"><span data-stu-id="59ad1-159">Select **Demo** as the environment topology.</span></span>

    ![Выбор топологии среды 1](./media/project2.png)

1. <span data-ttu-id="59ad1-161">На странице **Развернуть среду** введите имя среды.</span><span class="sxs-lookup"><span data-stu-id="59ad1-161">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="59ad1-162">Оставьте дополнительные настройки без изменений.</span><span class="sxs-lookup"><span data-stu-id="59ad1-162">Leave the advanced settings as they are.</span></span>

    ![Страница развертывания среды](./media/project4.png)

1. <span data-ttu-id="59ad1-164">По мере необходимости настройте размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="59ad1-164">Adjust the VM size as required.</span></span> <span data-ttu-id="59ad1-165">(Мы рекомендуем единицу складского хранения VM \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="59ad1-165">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="59ad1-166">Просмотрите условия ценообразования и лицензирования, а затем поставьте флажок, чтобы указать, что вы согласны с ними.</span><span class="sxs-lookup"><span data-stu-id="59ad1-166">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="59ad1-167">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="59ad1-167">Select **Next**.</span></span>
1. <span data-ttu-id="59ad1-168">На странице подтверждения развертывания убедитесь, что сведения правильные и затем выберите **Развернуть**.</span><span class="sxs-lookup"><span data-stu-id="59ad1-168">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="59ad1-169">Будет возвращено представление **Размещенные в облаке среды**, и ваша среда появится в списке.</span><span class="sxs-lookup"><span data-stu-id="59ad1-169">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="59ad1-170">Запрошенная среда отобразится в очереди, затем будет развернута.</span><span class="sxs-lookup"><span data-stu-id="59ad1-170">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="59ad1-171">Для завершения рабочих процессов среды потребуется некоторое время.</span><span class="sxs-lookup"><span data-stu-id="59ad1-171">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="59ad1-172">Поэтому проверьте примерно через шесть-девять часов.</span><span class="sxs-lookup"><span data-stu-id="59ad1-172">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="59ad1-173">Перед продолжением убедитесь, что состояние вашей среды — **Развернуто**.</span><span class="sxs-lookup"><span data-stu-id="59ad1-173">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="59ad1-174">Инициализация Commerce Scale Unit (облако)</span><span class="sxs-lookup"><span data-stu-id="59ad1-174">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="59ad1-175">Чтобы инициализировать CSU, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="59ad1-175">To initialize the CSU, follow these steps.</span></span>

1. <span data-ttu-id="59ad1-176">В представлении **Размещенные в облаке среды** выберите свою среду из списка.</span><span class="sxs-lookup"><span data-stu-id="59ad1-176">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="59ad1-177">Выберите **Полные сведения** в представлении среды с правой стороны.</span><span class="sxs-lookup"><span data-stu-id="59ad1-177">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="59ad1-178">Появится представление сведений о среде.</span><span class="sxs-lookup"><span data-stu-id="59ad1-178">The environment details view appears.</span></span>
1. <span data-ttu-id="59ad1-179">В **Компоненты среды** выберите **Управление**.</span><span class="sxs-lookup"><span data-stu-id="59ad1-179">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="59ad1-180">На вкладке **Commerce** выберите **Инициализация**.</span><span class="sxs-lookup"><span data-stu-id="59ad1-180">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="59ad1-181">Будет отображено представление параметров инициализации CSU.</span><span class="sxs-lookup"><span data-stu-id="59ad1-181">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="59ad1-182">В поле **Регион** выберите область, совпадающую с областью, в которую вы развернули среду, или близкий к ней.</span><span class="sxs-lookup"><span data-stu-id="59ad1-182">In the **Region** field, select the region that is the same or close to the region that you deployed the environment to.</span></span>
1. <span data-ttu-id="59ad1-183">Оставьте поле **Версия** без изменений.</span><span class="sxs-lookup"><span data-stu-id="59ad1-183">Leave the **Version** field as it is.</span></span>
1. <span data-ttu-id="59ad1-184">Выберите **Инициализация**.</span><span class="sxs-lookup"><span data-stu-id="59ad1-184">Select **Initialize**.</span></span>
1. <span data-ttu-id="59ad1-185">На странице подтверждения развертывания убедитесь, что сведения правильные и затем выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="59ad1-185">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="59ad1-186">Отобразится представление **Управление Commerce**, в котором будет выбрана вкладка **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="59ad1-186">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="59ad1-187">Ваш CSU был поставлен в очередь для подготовки.</span><span class="sxs-lookup"><span data-stu-id="59ad1-187">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="59ad1-188">Перед продолжением убедитесь, что состояние CSU — **Успех**.</span><span class="sxs-lookup"><span data-stu-id="59ad1-188">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="59ad1-189">Инициализация занимает примерно два-пять часов.</span><span class="sxs-lookup"><span data-stu-id="59ad1-189">Initialization takes approximately two to five hours.</span></span>

<span data-ttu-id="59ad1-190">Если вы не можете найти ссылку **Управление** в представлении сведений о среде, обратитесь за помощью к своему контакту в Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="59ad1-190">If you can't find the **Manage** link in the environment details view, reach out to your Microsoft contact for assistance.</span></span>

<span data-ttu-id="59ad1-191">Во время процесса развертывания может появиться следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="59ad1-191">During the deployment process, you might receive the following error message:</span></span>

> <span data-ttu-id="59ad1-192">Ознакомительным (демонстрационные и тестовые) средам необходимо зарегистрировать приложение соединителя Scale Unit \<application ID\> в Headquarters.</span><span class="sxs-lookup"><span data-stu-id="59ad1-192">Evaluation (demo/test) environments need to register the scale unit connector application \<application ID\> in headquarters.</span></span>

<span data-ttu-id="59ad1-193">Если из-за сбоя инициализации устройства CSU появляется это сообщение об ошибке, запишите идентификатор приложения, который является глобальным уникальным идентификатором (GUID), затем выполните действия, указанные в следующем разделе, чтобы зарегистрировать приложение развертывания CSU в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="59ad1-193">If the CSU initialization fails and you receive this error message, make a note of the application ID, which is a globally unique identifier (GUID), and then follow the steps in the next section to register the CSU deployment application in Commerce headquarters.</span></span>

### <a name="register-the-csu-deployment-application-in-commerce-headquarters-if-required"></a><span data-ttu-id="59ad1-194">Регистрация приложения развертывания CSU в Commerce headquarters (если необходимо)</span><span class="sxs-lookup"><span data-stu-id="59ad1-194">Register the CSU deployment application in Commerce headquarters (if required)</span></span>

<span data-ttu-id="59ad1-195">Чтобы зарегистрировать приложение развертывания CSU в Commerce headquarters, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="59ad1-195">To register the CSU deployment application in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="59ad1-196">В Commerce headquarters перейдите в раздел **Администрирование системы \> Настройка \> Приложения Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="59ad1-196">In Commerce headquarters, go to **System administration \> Setup \> Azure Active Directory applications**.</span></span>
1. <span data-ttu-id="59ad1-197">В столбце **Код клиента** введите код приложения из полученного сообщения об ошибке инициализации CSU.</span><span class="sxs-lookup"><span data-stu-id="59ad1-197">In the **Client Id** column, enter the application ID from the CSU initialization error message that you received.</span></span>
1. <span data-ttu-id="59ad1-198">В столбце **Имя** введите любой описательный текст (например, **Оценка CSU**).</span><span class="sxs-lookup"><span data-stu-id="59ad1-198">In the **Name** column, enter any descriptive text (for example, **CSU Eval**).</span></span>
1. <span data-ttu-id="59ad1-199">В столбце **Код пользователя** введите **RetailServiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="59ad1-199">In the **User ID** column, enter **RetailServiceAccount**.</span></span>
1. <span data-ttu-id="59ad1-200">Повторите инициализацию CSU и развертывание из LCS.</span><span class="sxs-lookup"><span data-stu-id="59ad1-200">Retry the CSU initialization and deployment from LCS.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="59ad1-201">Инициализация электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="59ad1-201">Initialize e-Commerce</span></span>

<span data-ttu-id="59ad1-202">Чтобы инициализировать электронную коммерцию, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="59ad1-202">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="59ad1-203">На вкладке **Электронная коммерция** просмотрите согласие на ознакомительную версию, затем выберите **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="59ad1-203">On the **e-Commerce** tab, review the evaluation consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="59ad1-204">В поле **Имя среды электронной коммерции** введите имя.</span><span class="sxs-lookup"><span data-stu-id="59ad1-204">In the **e-Commerce environment name** field, enter a name.</span></span> <span data-ttu-id="59ad1-205">Обратите внимание, что это имя появится в некоторых URL-адресах, указывающих на экземпляр электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="59ad1-205">Be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="59ad1-206">В поле **Имя Commerce Scale Unit** выберите CSU в списке.</span><span class="sxs-lookup"><span data-stu-id="59ad1-206">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="59ad1-207">(В списке должен быть только один вариант.)</span><span class="sxs-lookup"><span data-stu-id="59ad1-207">(The list should have only one option.)</span></span>

    <span data-ttu-id="59ad1-208">Поле **География электронной коммерции** настраивается автоматически.</span><span class="sxs-lookup"><span data-stu-id="59ad1-208">The **e-Commerce geography** field is set automatically.</span></span>

1. <span data-ttu-id="59ad1-209">Выберите **Далее** для продолжения.</span><span class="sxs-lookup"><span data-stu-id="59ad1-209">Select **Next** to continue.</span></span>
1. <span data-ttu-id="59ad1-210">В поле **Поддерживаемые имена узлов** введите любой допустимый домен, например `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="59ad1-210">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1. <span data-ttu-id="59ad1-211">В поле **Группа безопасности AAD для системного администратора** введите первые несколько букв имени группы безопасности, которую необходимо использовать, затем выберите символ лупы для просмотра результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="59ad1-211">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="59ad1-212">Выберите правильную группу безопасности в списке.</span><span class="sxs-lookup"><span data-stu-id="59ad1-212">Select the correct security group in the list.</span></span>
1.  <span data-ttu-id="59ad1-213">В поле **Группа безопасности AAD для модератора оценок и отзывов** введите первые несколько букв имени группы безопасности, которую необходимо использовать, затем выберите символ лупы для просмотра результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="59ad1-213">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="59ad1-214">Выберите правильную группу безопасности в списке.</span><span class="sxs-lookup"><span data-stu-id="59ad1-214">Select the correct security group in the list.</span></span>
1. <span data-ttu-id="59ad1-215">Оставьте для параметра **Включить службу оценок и отзывов** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="59ad1-215">Leave the **Enable ratings and review service** option set to **Yes**.</span></span>
1. <span data-ttu-id="59ad1-216">Выберите **Инициализация**.</span><span class="sxs-lookup"><span data-stu-id="59ad1-216">Select **Initialize**.</span></span> <span data-ttu-id="59ad1-217">Отобразится представление **Управление Commerce**, в котором будет выбрана вкладка **Электронная коммерция**.</span><span class="sxs-lookup"><span data-stu-id="59ad1-217">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="59ad1-218">Инициализация электронной коммерции начата.</span><span class="sxs-lookup"><span data-stu-id="59ad1-218">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="59ad1-219">Перед продолжением необходимо подождать, пока состояние инициализации электронной коммерции не станет **Успешная инициализация**.</span><span class="sxs-lookup"><span data-stu-id="59ad1-219">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="59ad1-220">В **Ссылки** в нижнем правом углу запишите URL-адреса для следующих ссылок:</span><span class="sxs-lookup"><span data-stu-id="59ad1-220">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="59ad1-221">**Сайт электронной коммерции** — ссылка на корневой узел вашего сайта электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="59ad1-221">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="59ad1-222">**Конфигуратор сайта электронной коммерции** — ссылка на средство управления сайтом.</span><span class="sxs-lookup"><span data-stu-id="59ad1-222">**Commerce site builder** – The link to the site management tool.</span></span>

## <a name="next-steps"></a><span data-ttu-id="59ad1-223">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="59ad1-223">Next steps</span></span>

<span data-ttu-id="59ad1-224">Для продолжения процесса предоставления и настройки вашей ознакомительной среды Commerce см. [Настройка ознакомительной среды Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="59ad1-224">To continue the process of provisioning and configuring your Commerce evaluation environment, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="59ad1-225">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="59ad1-225">Additional resources</span></span>

[<span data-ttu-id="59ad1-226">Обзор ознакомительной среды Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="59ad1-226">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="59ad1-227">Настройка ознакомительной среды Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="59ad1-227">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="59ad1-228">Настройка BOPIS в ознакомительной среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="59ad1-228">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="59ad1-229">Настройка дополнительных функций ознакомительной среды Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="59ad1-229">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="59ad1-230">Вопросы и ответы по ознакомительной среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="59ad1-230">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="59ad1-231">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="59ad1-231">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="59ad1-232">Commerce Scale Unit (облако)</span><span class="sxs-lookup"><span data-stu-id="59ad1-232">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="59ad1-233">Портал Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="59ad1-233">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="59ad1-234">Веб-сайт Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="59ad1-234">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
