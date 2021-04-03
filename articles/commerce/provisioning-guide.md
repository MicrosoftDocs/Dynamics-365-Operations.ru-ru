---
title: Обеспечение среды оценки Dynamics 365 Commerce
description: В этой теме объясняется, как подготовить ознакомительную среду Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: a57cc02c6d62f288f14b65191c2f4927a019963c
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478172"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="d8c8f-103">Обеспечение среды оценки Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d8c8f-103">Provision a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d8c8f-104">В этой теме объясняется, как подготовить ознакомительную среду Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="d8c8f-105">Прежде чем начать, рекомендуется выполнить быструю проверку данного раздела, чтобы понять, что именно требуется для этого процесса.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="d8c8f-106">Ознакомительные среды Commerce не являются общедоступными и предоставляются партнерам и клиентам по запросам по запросу.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-106">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="d8c8f-107">Для получения дополнительных сведений обратитесь к своему контакту Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-107">For more information, reach out to your Microsoft partner contact.</span></span>

<span data-ttu-id="d8c8f-108">Чтобы успешно предоставить ознакомительную среду Commerce, необходимо создать проект с определенным названием и типом продукта.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-108">To successfully provision a Commerce evaluation environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="d8c8f-109">У среды и Commerce Scale Unit (CSU) также есть некоторые специальные параметры, которые необходимо использовать, если вы планируете подготовить электронную коммерцию позже.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-109">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you expect to provision e-Commerce later.</span></span> <span data-ttu-id="d8c8f-110">Инструкции в этой теме описывают все необходимые шаги, которые вы должны выполнить, и параметры, которые вы должны использовать.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-110">The instructions in this topic describe all the steps that are required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="d8c8f-111">После успешного предоставления ознакомительной среды Commerce необходимо выполнить несколько шагов после подготовки, чтобы подготовить ее к использованию.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-111">After you successfully provision your Commerce evaluation environment, you must complete a few post-provisioning steps to prepare it for use.</span></span> <span data-ttu-id="d8c8f-112">Некоторые шаги являются необязательными, в зависимости от того, какие аспекты системы вы хотите оценить.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="d8c8f-113">Вы всегда можете выполнить дополнительные шаги позже.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="d8c8f-114">Для получения информации о том, как настроить ознакомительную среду Commerce после подготовки, см. в [Настройка ознакомительной среды Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="d8c8f-114">For information about how to configure your Commerce evaluation environment after you provision it, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="d8c8f-115">Для сведений о том, как настроить дополнительные функции для ознакомительной среды Commerce, см. [Настройка дополнительных функций для ознакомительной среды Commerce](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="d8c8f-115">For information about how to configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d8c8f-116">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="d8c8f-116">Prerequisites</span></span>

<span data-ttu-id="d8c8f-117">Для того, чтобы предоставить ознакомительную среду Commerce, необходимо предусмотреть следующие предварительные условия:</span><span class="sxs-lookup"><span data-stu-id="d8c8f-117">The following prerequisites must be in place before you can provision your Commerce evaluation environment:</span></span>

- <span data-ttu-id="d8c8f-118">Вы присоединились к программе оценки и получили емкость для оценочной среды.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-118">You have been onboarded into the evaluation program and granted capacity for an evaluation environment.</span></span>
- <span data-ttu-id="d8c8f-119">У вас есть доступ к порталу Lifecycle Services Microsoft Dynamics (LCS)</span><span class="sxs-lookup"><span data-stu-id="d8c8f-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="d8c8f-120">Вы являетесь существующим партнером или клиентом Microsoft Dynamics 365 и можете создать проект Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="d8c8f-121">У вас есть права администратора на доступ к вашей подписке Microsoft Azure, либо вы находитесь в контакте с администратором подписки, который может помочь вам в случае необходимости.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-121">You have administrator access to your Microsoft Azure subscription, or you're in contact with a subscription administrator who can assist you if required.</span></span>
- <span data-ttu-id="d8c8f-122">В вас есть доступный код клиента Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="d8c8f-122">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="d8c8f-123">Вы создали группу безопасности Azure AD, которую можно использовать в качестве группы администраторов системы электронной коммерции, и у вас есть ее идентификатор.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-123">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="d8c8f-124">Вы создали группу безопасности Azure AD, которую можно использовать в качестве группы модератора оценок и рецензий, и у вас есть ее идентификатор.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-124">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="d8c8f-125">(Эта группа безопасности может быть такой же, как группа администрирования системы электронной коммерции.)</span><span class="sxs-lookup"><span data-stu-id="d8c8f-125">(This security group can be the same as the e-Commerce system admin group.)</span></span>

<span data-ttu-id="d8c8f-126">Обратите внимание, что этот список не является исчерпывающим.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-126">Note that this list isn't exhaustive.</span></span> <span data-ttu-id="d8c8f-127">При возникновении каких-либо проблем обратитесь за помощью к партнеру корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-127">If you experience any issues, reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="provision-your-commerce-evaluation-environment"></a><span data-ttu-id="d8c8f-128">Обеспечение своей ознакомительной среды Commerce</span><span class="sxs-lookup"><span data-stu-id="d8c8f-128">Provision your Commerce evaluation environment</span></span>

<span data-ttu-id="d8c8f-129">Эти процедуры объясняют, как обеспечить ознакомительную среду Commerce.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-129">These procedures explain how to provision a Commerce evaluation environment.</span></span> <span data-ttu-id="d8c8f-130">После их успешного завершения ознакомительная среда Commerce будет готова к настройке.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-130">After you successfully complete them, the Commerce evaluation environment will be ready for configuration.</span></span> <span data-ttu-id="d8c8f-131">Все действия, описанные здесь, выполняются на портале LCS.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-131">All the activities that are described here occur in the LCS portal.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="d8c8f-132">Создать новый проект</span><span class="sxs-lookup"><span data-stu-id="d8c8f-132">Create a new project</span></span>

<span data-ttu-id="d8c8f-133">Чтобы создать новый проект в LCS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-133">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="d8c8f-134">На главной странице LCS выберите знак плюса (**+**) для создания проекта.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-134">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="d8c8f-135">В правой области выполните один из следующих шагов:</span><span class="sxs-lookup"><span data-stu-id="d8c8f-135">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="d8c8f-136">Если вы являетесь партнером, выберите **Миграция, создание решений и знакомство**.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-136">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="d8c8f-137">Если вы клиент, выберите **Перспективный клиент — предпродажная подготовка**.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-137">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="d8c8f-138">Введите название, описание и отрасль.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-138">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="d8c8f-139">В поле **Наименование продукта** выберите **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-139">In the **Product name** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="d8c8f-140">В поле **Версия продукта** выберите **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-140">In the **Product version** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="d8c8f-141">В поле **Методология** выберите **Методология реализации Dynamics Retail**.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-141">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="d8c8f-142">Необязательно: можно импортировать роли и пользователей из существующего проекта.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-142">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="d8c8f-143">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-143">Select **Create**.</span></span> <span data-ttu-id="d8c8f-144">Появится представление проекта.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-144">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="d8c8f-145">Добавление соединителя Azure</span><span class="sxs-lookup"><span data-stu-id="d8c8f-145">Add the Azure Connector</span></span>

<span data-ttu-id="d8c8f-146">Чтобы добавить соединитель Azure в проект LCS, выполните шаги из раздела [Выполнение процесса адаптации Azure Resource Manager (ARM)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span><span class="sxs-lookup"><span data-stu-id="d8c8f-146">To add the Azure Connector to your LCS project, follow the steps in [Complete the Azure Resource Manager (ARM) onboarding process](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span></span>

### <a name="deploy-the-environment"></a><span data-ttu-id="d8c8f-147">Развернуть среду</span><span class="sxs-lookup"><span data-stu-id="d8c8f-147">Deploy the environment</span></span>

<span data-ttu-id="d8c8f-148">Выполните следующие действия, чтобы развернуть среду.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-148">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="d8c8f-149">Возможно, вам не придется выполнять шаги 6, 7 и/или 8, потому что страницы с одним вариантом пропускаются.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-149">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="d8c8f-150">Когда вы находитесь в представлении **Параметры среды**, подтвердите, что текст **Dynamics 365 Commerce — демонстрация (10.0.* x* с обновлением платформы *xx*)\*\* отображается непосредственно над полем **Имя среды**.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-150">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="d8c8f-151">Сведения см. на изображении, которое появляется после шага 8.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-151">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="d8c8f-152">В верхнем меню выберите **Размещенные в облаке среды**.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-152">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="d8c8f-153">Выберите **Добавить**, чтобы добавить среду.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-153">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="d8c8f-154">В поле **Версия приложения** выберите самую последнюю версию.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-154">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="d8c8f-155">Если требуется выбрать версию приложения, отличающуюся от самой последней версии, не выбирайте версию, предшествующую **10.0.14**.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-155">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.14**.</span></span>
1. <span data-ttu-id="d8c8f-156">В поле **Версия платформы** используйте версию платформы, которая выбирается автоматически для выбранной версии приложения.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-156">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Выбор приложения и версий платформы](./media/project1.png)

1. <span data-ttu-id="d8c8f-158">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-158">Select **Next**.</span></span>
1. <span data-ttu-id="d8c8f-159">Выберите **Демонстрация** в качестве топологии среды.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-159">Select **Demo** as the environment topology.</span></span>

    ![Выбор топологии среды 1](./media/project2.png)

1. <span data-ttu-id="d8c8f-161">На странице **Развернуть среду** введите имя среды.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-161">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="d8c8f-162">Оставьте дополнительные настройки без изменений.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-162">Leave the advanced settings as they are.</span></span>

    ![Страница развертывания среды](./media/project4.png)

1. <span data-ttu-id="d8c8f-164">По мере необходимости настройте размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-164">Adjust the VM size as required.</span></span> <span data-ttu-id="d8c8f-165">(Мы рекомендуем единицу складского хранения VM \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="d8c8f-165">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="d8c8f-166">Просмотрите условия ценообразования и лицензирования, а затем поставьте флажок, чтобы указать, что вы согласны с ними.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-166">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="d8c8f-167">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-167">Select **Next**.</span></span>
1. <span data-ttu-id="d8c8f-168">На странице подтверждения развертывания убедитесь, что сведения правильные и затем выберите **Развернуть**.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-168">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="d8c8f-169">Будет возвращено представление **Размещенные в облаке среды**, и ваша среда появится в списке.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-169">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="d8c8f-170">Запрошенная среда отобразится в очереди, затем будет развернута.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-170">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="d8c8f-171">Для завершения рабочих процессов среды потребуется некоторое время.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-171">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="d8c8f-172">Поэтому проверьте примерно через шесть-девять часов.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-172">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="d8c8f-173">Перед продолжением убедитесь, что состояние вашей среды — **Развернуто**.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-173">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="d8c8f-174">Инициализация Commerce Scale Unit (облако)</span><span class="sxs-lookup"><span data-stu-id="d8c8f-174">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="d8c8f-175">Чтобы инициализировать CSU, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-175">To initialize the CSU, follow these steps.</span></span>

1. <span data-ttu-id="d8c8f-176">В представлении **Размещенные в облаке среды** выберите свою среду из списка.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-176">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="d8c8f-177">Выберите **Полные сведения** в представлении среды с правой стороны.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-177">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="d8c8f-178">Появится представление сведений о среде.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-178">The environment details view appears.</span></span>
1. <span data-ttu-id="d8c8f-179">В **Компоненты среды** выберите **Управление**.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-179">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="d8c8f-180">На вкладке **Commerce** выберите **Инициализация**.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-180">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="d8c8f-181">Будет отображено представление параметров инициализации CSU.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-181">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="d8c8f-182">В поле **Регион** выберите область, совпадающую с областью, в которую вы развернули среду, или близкий к ней.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-182">In the **Region** field, select the region that is the same or close to the region that you deployed the environment to.</span></span>
1. <span data-ttu-id="d8c8f-183">Оставьте поле **Версия** без изменений.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-183">Leave the **Version** field as it is.</span></span>
1. <span data-ttu-id="d8c8f-184">Выберите **Инициализация**.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-184">Select **Initialize**.</span></span>
1. <span data-ttu-id="d8c8f-185">На странице подтверждения развертывания убедитесь, что сведения правильные и затем выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-185">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="d8c8f-186">Отобразится представление **Управление Commerce**, в котором будет выбрана вкладка **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-186">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="d8c8f-187">Ваш CSU был поставлен в очередь для подготовки.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-187">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="d8c8f-188">Перед продолжением убедитесь, что состояние CSU — **Успех**.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-188">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="d8c8f-189">Инициализация занимает примерно два-пять часов.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-189">Initialization takes approximately two to five hours.</span></span>

<span data-ttu-id="d8c8f-190">Если вы не можете найти ссылку **Управление** в представлении сведений о среде, обратитесь за помощью к своему контакту в Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-190">If you can't find the **Manage** link in the environment details view, reach out to your Microsoft contact for assistance.</span></span>

<span data-ttu-id="d8c8f-191">Во время процесса развертывания может появиться следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="d8c8f-191">During the deployment process, you might receive the following error message:</span></span>

> <span data-ttu-id="d8c8f-192">Ознакомительным (демонстрационные и тестовые) средам необходимо зарегистрировать приложение соединителя Scale Unit \<application ID\> в Headquarters.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-192">Evaluation (demo/test) environments need to register the scale unit connector application \<application ID\> in headquarters.</span></span>

<span data-ttu-id="d8c8f-193">Если из-за сбоя инициализации устройства CSU появляется это сообщение об ошибке, запишите идентификатор приложения, который является глобальным уникальным идентификатором (GUID), затем выполните действия, указанные в следующем разделе, чтобы зарегистрировать приложение развертывания CSU в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-193">If the CSU initialization fails and you receive this error message, make a note of the application ID, which is a globally unique identifier (GUID), and then follow the steps in the next section to register the CSU deployment application in Commerce headquarters.</span></span>

### <a name="register-the-csu-deployment-application-in-commerce-headquarters-if-required"></a><span data-ttu-id="d8c8f-194">Регистрация приложения развертывания CSU в Commerce headquarters (если необходимо)</span><span class="sxs-lookup"><span data-stu-id="d8c8f-194">Register the CSU deployment application in Commerce headquarters (if required)</span></span>

<span data-ttu-id="d8c8f-195">Чтобы зарегистрировать приложение развертывания CSU в Commerce headquarters, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-195">To register the CSU deployment application in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="d8c8f-196">В Commerce headquarters перейдите в раздел **Администрирование системы \> Настройка \> Приложения Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-196">In Commerce headquarters, go to **System administration \> Setup \> Azure Active Directory applications**.</span></span>
1. <span data-ttu-id="d8c8f-197">В столбце **Код клиента** введите код приложения из полученного сообщения об ошибке инициализации CSU.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-197">In the **Client Id** column, enter the application ID from the CSU initialization error message that you received.</span></span>
1. <span data-ttu-id="d8c8f-198">В столбце **Имя** введите любой описательный текст (например, **Оценка CSU**).</span><span class="sxs-lookup"><span data-stu-id="d8c8f-198">In the **Name** column, enter any descriptive text (for example, **CSU Eval**).</span></span>
1. <span data-ttu-id="d8c8f-199">В столбце **Код пользователя** введите **RetailServiceAccount**.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-199">In the **User ID** column, enter **RetailServiceAccount**.</span></span>
1. <span data-ttu-id="d8c8f-200">Повторите инициализацию CSU и развертывание из LCS.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-200">Retry the CSU initialization and deployment from LCS.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="d8c8f-201">Инициализация электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="d8c8f-201">Initialize e-Commerce</span></span>

<span data-ttu-id="d8c8f-202">Чтобы инициализировать электронную коммерцию, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-202">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="d8c8f-203">На вкладке **Электронная коммерция** просмотрите согласие на ознакомительную версию, затем выберите **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-203">On the **e-Commerce** tab, review the evaluation consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="d8c8f-204">В поле **Имя среды электронной коммерции** введите имя.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-204">In the **e-Commerce environment name** field, enter a name.</span></span> <span data-ttu-id="d8c8f-205">Обратите внимание, что это имя появится в некоторых URL-адресах, указывающих на экземпляр электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-205">Be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="d8c8f-206">В поле **Имя Commerce Scale Unit** выберите CSU в списке.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-206">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="d8c8f-207">(В списке должен быть только один вариант.)</span><span class="sxs-lookup"><span data-stu-id="d8c8f-207">(The list should have only one option.)</span></span>

    <span data-ttu-id="d8c8f-208">Поле **География электронной коммерции** настраивается автоматически.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-208">The **e-Commerce geography** field is set automatically.</span></span>

1. <span data-ttu-id="d8c8f-209">Выберите **Далее** для продолжения.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-209">Select **Next** to continue.</span></span>
1. <span data-ttu-id="d8c8f-210">В поле **Поддерживаемые имена узлов** введите любой допустимый домен, например `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-210">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1. <span data-ttu-id="d8c8f-211">В поле **Группа безопасности AAD для системного администратора** введите первые несколько букв имени группы безопасности, которую необходимо использовать, затем выберите символ лупы для просмотра результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-211">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="d8c8f-212">Выберите правильную группу безопасности в списке.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-212">Select the correct security group in the list.</span></span>
1.  <span data-ttu-id="d8c8f-213">В поле **Группа безопасности AAD для модератора оценок и отзывов** введите первые несколько букв имени группы безопасности, которую необходимо использовать, затем выберите символ лупы для просмотра результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-213">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="d8c8f-214">Выберите правильную группу безопасности в списке.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-214">Select the correct security group in the list.</span></span>
1. <span data-ttu-id="d8c8f-215">Оставьте для параметра **Включить службу оценок и отзывов** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-215">Leave the **Enable ratings and review service** option set to **Yes**.</span></span>
1. <span data-ttu-id="d8c8f-216">Выберите **Инициализация**.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-216">Select **Initialize**.</span></span> <span data-ttu-id="d8c8f-217">Отобразится представление **Управление Commerce**, в котором будет выбрана вкладка **Электронная коммерция**.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-217">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="d8c8f-218">Инициализация электронной коммерции начата.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-218">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="d8c8f-219">Перед продолжением необходимо подождать, пока состояние инициализации электронной коммерции не станет **Успешная инициализация**.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-219">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="d8c8f-220">В **Ссылки** в нижнем правом углу запишите URL-адреса для следующих ссылок:</span><span class="sxs-lookup"><span data-stu-id="d8c8f-220">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="d8c8f-221">**Сайт электронной коммерции** — ссылка на корневой узел вашего сайта электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-221">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="d8c8f-222">**Конфигуратор сайта электронной коммерции** — ссылка на средство управления сайтом.</span><span class="sxs-lookup"><span data-stu-id="d8c8f-222">**Commerce site builder** – The link to the site management tool.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d8c8f-223">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="d8c8f-223">Next steps</span></span>

<span data-ttu-id="d8c8f-224">Для продолжения процесса предоставления и настройки вашей ознакомительной среды Commerce см. [Настройка ознакомительной среды Commerce](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="d8c8f-224">To continue the process of provisioning and configuring your Commerce evaluation environment, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d8c8f-225">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d8c8f-225">Additional resources</span></span>

[<span data-ttu-id="d8c8f-226">Обзор ознакомительной среды Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d8c8f-226">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="d8c8f-227">Настройка ознакомительной среды Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d8c8f-227">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="d8c8f-228">Настройка BOPIS в ознакомительной среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d8c8f-228">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="d8c8f-229">Настройка дополнительных функций ознакомительной среды Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d8c8f-229">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="d8c8f-230">Вопросы и ответы по ознакомительной среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d8c8f-230">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="d8c8f-231">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="d8c8f-231">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="d8c8f-232">Commerce Scale Unit (облако)</span><span class="sxs-lookup"><span data-stu-id="d8c8f-232">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="d8c8f-233">Портал Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="d8c8f-233">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="d8c8f-234">Веб-сайт Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d8c8f-234">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
