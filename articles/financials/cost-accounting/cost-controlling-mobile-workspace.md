---
title: "Мобильная рабочая область управления затратами"
description: "В этой теме содержится информация о мобильной рабочей области \"Управление затратами\". Эта рабочая область позволяет менеджерам центра затрат просматривать сведения о производительности центра затрат в любое время и в любом месте."
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 0dc79371d63818fb0f6d55389a146012c269a684
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---

# <a name="cost-controlling-mobile-workspace"></a><span data-ttu-id="0d882-104">Мобильная рабочая область управления затратами</span><span class="sxs-lookup"><span data-stu-id="0d882-104">Cost controlling mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0d882-105">В этой теме содержится информация о мобильной рабочей области **Управление затратами**.</span><span class="sxs-lookup"><span data-stu-id="0d882-105">This topic provides information about the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="0d882-106">Эта рабочая область позволяет менеджерам центра затрат просматривать сведения о производительности центра затрат в любое время и в любом месте.</span><span class="sxs-lookup"><span data-stu-id="0d882-106">This workspace lets cost center managers view information about cost center performance anytime and anywhere.</span></span>

<span data-ttu-id="0d882-107">Эту мобильную рабочую область можно использовать с мобильным приложением Microsoft Dynamics 365 for Unified Operations.</span><span class="sxs-lookup"><span data-stu-id="0d882-107">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="0d882-108">Обзор</span><span class="sxs-lookup"><span data-stu-id="0d882-108">Overview</span></span>
<span data-ttu-id="0d882-109">Мобильная рабочая область **Управление затратами** обеспечивает мгновенное отображение текущей производительности центров затрат путем сравнения фактических затрат с бюджетными затратами.</span><span class="sxs-lookup"><span data-stu-id="0d882-109">The **Cost controlling** mobile workspace provides an instant view of the current performance of cost centers by comparing actual costs against the budgeted costs.</span></span> <span data-ttu-id="0d882-110">Можно выполнить детализацию до статуса отдельных элементов затрат.</span><span class="sxs-lookup"><span data-stu-id="0d882-110">You can drill down to the status of individual cost elements.</span></span>

<span data-ttu-id="0d882-111">Например, сотрудник получает приглашение на международную конференцию, но организация должна оплатить все командировочные расходы.</span><span class="sxs-lookup"><span data-stu-id="0d882-111">For example, an employee receives an invitation to an international conference, but the organization must cover all the travel expenses.</span></span> <span data-ttu-id="0d882-112">Сотрудник запрашивает у своего менеджера разрешение на посещение этой конференции.</span><span class="sxs-lookup"><span data-stu-id="0d882-112">The employee asks his manager whether he can attend the conference.</span></span> <span data-ttu-id="0d882-113">Менеджер открывает мобильную рабочую область **Управление затратами** на своем мобильном устройстве и смотрит, имеет ли она бюджет для оплаты посещения конференции сотрудником.</span><span class="sxs-lookup"><span data-stu-id="0d882-113">The manager opens the **Cost controlling** mobile workspace on her mobile device to see whether she has budget for the employee to attend the conference.</span></span>

### <a name="data-security"></a><span data-ttu-id="0d882-114">Безопасность данных</span><span class="sxs-lookup"><span data-stu-id="0d882-114">Data security</span></span>
<span data-ttu-id="0d882-115">Данные в мобильной рабочей области **Управление затратами** защищены учетными данными пользователя.</span><span class="sxs-lookup"><span data-stu-id="0d882-115">The data in the **Cost controlling** mobile workspace is secured through user credentials.</span></span> <span data-ttu-id="0d882-116">Менеджеры центра затрат могут просматривать сведения только для своего собственного центра затрат.</span><span class="sxs-lookup"><span data-stu-id="0d882-116">Cost center managers are allowed to see data only for their own cost center.</span></span> <span data-ttu-id="0d882-117">Управление безопасностью уровня доступа осуществляется в модуле **Учет затрат**.</span><span class="sxs-lookup"><span data-stu-id="0d882-117">The access-level security is managed in the **Cost accounting** module.</span></span>

<span data-ttu-id="0d882-118">Бухгалтеры по учету затрат определяют конфигурацию мобильной рабочей области **Управление затратами** в модуле **Учет затрат**.</span><span class="sxs-lookup"><span data-stu-id="0d882-118">Cost accountants define the configuration of the **Cost controlling** mobile workspace in the **Cost accounting** module.</span></span> <span data-ttu-id="0d882-119">После публикации рабочей области в мобильном приложении она становится доступна в приложении.</span><span class="sxs-lookup"><span data-stu-id="0d882-119">After the workspace is published to the mobile app, it's available in the app.</span></span> <span data-ttu-id="0d882-120">Таким образом, все менеджеры центров затрат в рамках организации могут просматривать данные в одинаковом формате.</span><span class="sxs-lookup"><span data-stu-id="0d882-120">Therefore, all cost center managers in the organization can view data in the same format.</span></span>

### <a name="actions-views-and-links"></a><span data-ttu-id="0d882-121">Действия, представления и ссылки</span><span class="sxs-lookup"><span data-stu-id="0d882-121">Actions, views, and links</span></span>
<span data-ttu-id="0d882-122">Мобильная рабочая область **Управление затратами** содержит действия, представления и ссылки:</span><span class="sxs-lookup"><span data-stu-id="0d882-122">The **Cost controlling** mobile workspace provides the following actions, views, and links:</span></span>

-   <span data-ttu-id="0d882-123">**Действия:**</span><span class="sxs-lookup"><span data-stu-id="0d882-123">**Actions:**</span></span>

    -   <span data-ttu-id="0d882-124">Используйте **Выбрать конфигурацию** для выбора макета.</span><span class="sxs-lookup"><span data-stu-id="0d882-124">Use **Select configuration** to select a layout.</span></span>
    -   <span data-ttu-id="0d882-125">Используйте **Выбрать объект затрат** для выбора центров затрат, по которым требуется фильтровать данные.</span><span class="sxs-lookup"><span data-stu-id="0d882-125">Use **Select cost object** to select the cost centers to filter data on.</span></span>
    
        > [!NOTE]
        > <span data-ttu-id="0d882-126">Центры затрат, которые отображаются в списке, зависят от уровня доступа, предоставленного в модуле **Учет затрат**.</span><span class="sxs-lookup"><span data-stu-id="0d882-126">The cost centers that appear in the list depend on the access that is granted in the **Cost accounting** module.</span></span>

-   <span data-ttu-id="0d882-127">**Представления:** на основании выбранных действий и конфигурации в модуле **Учет затрат** можно просмотреть следующую информацию на карточках.</span><span class="sxs-lookup"><span data-stu-id="0d882-127">**Views:** Based on the actions that are selected and the configuration in the **Cost accounting** module, you can view the following information on the cards:</span></span>

    -   <span data-ttu-id="0d882-128">Факт/бюджет (текущий период)</span><span class="sxs-lookup"><span data-stu-id="0d882-128">Actual vs budget (current period)</span></span>
    -   <span data-ttu-id="0d882-129">Факт/Пересмотренный бюджет (текущий период)</span><span class="sxs-lookup"><span data-stu-id="0d882-129">Actual vs revised budget (current period)</span></span>
    -   <span data-ttu-id="0d882-130">Факт/бюджет (предыдущий период)</span><span class="sxs-lookup"><span data-stu-id="0d882-130">Actual vs budget (previous period)</span></span>
    -   <span data-ttu-id="0d882-131">Факт/пересмотренный бюджет (предыдущий период)</span><span class="sxs-lookup"><span data-stu-id="0d882-131">Actual vs revised budget (previous period)</span></span>
    -   <span data-ttu-id="0d882-132">Факт/бюджет (с начала года)</span><span class="sxs-lookup"><span data-stu-id="0d882-132">Actual vs budget (year to date)</span></span>
    -   <span data-ttu-id="0d882-133">Факс/пересмотренный бюджет (с начала года)</span><span class="sxs-lookup"><span data-stu-id="0d882-133">Actual vs revised budget (year to date)</span></span>

    <span data-ttu-id="0d882-134">В каждой карточке показаны следующие суммы: фактическая, бюджет, отклонение и % отклонения.</span><span class="sxs-lookup"><span data-stu-id="0d882-134">The following amounts are shown on every card: Actual, Budget, Variance, and Variance %.</span></span>

-   <span data-ttu-id="0d882-135">**Ссылки:**</span><span class="sxs-lookup"><span data-stu-id="0d882-135">**Links:**</span></span>

    -   <span data-ttu-id="0d882-136">Сведения для текущего периода</span><span class="sxs-lookup"><span data-stu-id="0d882-136">Details for current period</span></span>
    -   <span data-ttu-id="0d882-137">Сведения для предыдущего периода</span><span class="sxs-lookup"><span data-stu-id="0d882-137">Details for previous period</span></span>
    -   <span data-ttu-id="0d882-138">Сведения с начала года</span><span class="sxs-lookup"><span data-stu-id="0d882-138">Details for year to date</span></span>

    <span data-ttu-id="0d882-139">При выборе ссылки отображается карта для каждого элемента затрат.</span><span class="sxs-lookup"><span data-stu-id="0d882-139">When you select a link, a card is shown for each cost element.</span></span> <span data-ttu-id="0d882-140">На каждой карточке отображаются следующее суммы: фактическая, бюджетная, отклонение от бюджета, отклонение от бюджета в процентах, пересмотренный бюджет, отклонение от пересмотренного бюджета и отклонение от пересмотренного бюджета в процентах.</span><span class="sxs-lookup"><span data-stu-id="0d882-140">The following amounts are shown on every card: Actual, Budget, Budget variance, Budget variance %, Revised budget, Revised budget variance, and Revised budget variance %.</span></span>
    
    <span data-ttu-id="0d882-141">[![Карточка для элемента затрат ](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span><span class="sxs-lookup"><span data-stu-id="0d882-141">[![Card for a cost element](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0d882-142">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="0d882-142">Prerequisites</span></span>
<span data-ttu-id="0d882-143">Предварительные условия различаются, в зависимости от версии Microsoft Dynamics 365, развернутой в организации.</span><span class="sxs-lookup"><span data-stu-id="0d882-143">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="0d882-144">Необходимые условия при использовании Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (июль 2017 г.)</span><span class="sxs-lookup"><span data-stu-id="0d882-144">Prerequisites if you use Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>
<span data-ttu-id="0d882-145">Если в вашей организации развернута система Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (июль 2017 г.), системный администратор должен опубликовать мобильную рабочую область **Управление затратами**.</span><span class="sxs-lookup"><span data-stu-id="0d882-145">If Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) has been deployed for your organization, the system administrator must publish the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="0d882-146">См. инструкции в [Публикация мобильной рабочей области](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="0d882-146">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="0d882-147">Необходимые условия при использовании Microsoft Dynamics 365 for Operations версии 1611 с платформой обновления 3 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="0d882-147">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with platform update 3 or later</span></span>
<span data-ttu-id="0d882-148">Если в вашей организации развернута Microsoft Dynamics 365 for Operations версии 1611 с платформой обновления 3 или более поздней версии, системный администратор должен выполнить следующие условия.</span><span class="sxs-lookup"><span data-stu-id="0d882-148">If Microsoft Dynamics 365 for Operations version 1611 with platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0d882-149">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="0d882-149">Prerequisite</span></span></th>
<th><span data-ttu-id="0d882-150">Роль</span><span class="sxs-lookup"><span data-stu-id="0d882-150">Role</span></span></th>
<th><span data-ttu-id="0d882-151">описание</span><span class="sxs-lookup"><span data-stu-id="0d882-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0d882-152">Реализовать КБ 4013633.</span><span class="sxs-lookup"><span data-stu-id="0d882-152">Implement KB 4013633.</span></span></td>
<td><span data-ttu-id="0d882-153">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="0d882-153">System administrator</span></span></td>

<td><span data-ttu-id="0d882-154">KB 4013633 является обновлением X++ или исправлением метаданных, содержащим мобильную рабочую область <strong>Управление затратами</strong>.</span><span class="sxs-lookup"><span data-stu-id="0d882-154">KB 4013633 is an X++ update or metadata hotfix that contains the <strong>Cost controlling</strong> mobile workspace.</span></span> <span data-ttu-id="0d882-155">Для установки KB 4013633 системный администратор должен выполнить следующие задачи.</span><span class="sxs-lookup"><span data-stu-id="0d882-155">To implement KB 4013633, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="0d882-156"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Загрузите исправление метаданных из Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="0d882-156"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="0d882-157"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Установите исправление метаданных</a>.</span><span class="sxs-lookup"><span data-stu-id="0d882-157"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="0d882-158"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Создайте пакет развертывания</a>, содержащий модель <strong>SCMMobile</strong>, затем отправьте пакет развертывания в LCS.</span><span class="sxs-lookup"><span data-stu-id="0d882-158"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="0d882-159"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Примените готовый к развертыванию пакет</a>.</span><span class="sxs-lookup"><span data-stu-id="0d882-159"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d882-160">Опубликуйте мобильную рабочую область <strong>Управление затратами</strong>.</span><span class="sxs-lookup"><span data-stu-id="0d882-160">Publish the <strong>Cost controlling</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="0d882-161">Системный администратор</span><span class="sxs-lookup"><span data-stu-id="0d882-161">System administrator</span></span></td>
<td><span data-ttu-id="0d882-162">См. <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Публикация мобильной рабочей области</a>.</span><span class="sxs-lookup"><span data-stu-id="0d882-162">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>


## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="0d882-163">Загрузите и установите мобильное приложение</span><span class="sxs-lookup"><span data-stu-id="0d882-163">Download and install the mobile app</span></span>
<span data-ttu-id="0d882-164">Загрузите и установите мобильное приложение Dynamics 365 for Unified Operations:</span><span class="sxs-lookup"><span data-stu-id="0d882-164">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="0d882-165">Для ОС Android</span><span class="sxs-lookup"><span data-stu-id="0d882-165">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="0d882-166">Для iPhone</span><span class="sxs-lookup"><span data-stu-id="0d882-166">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="0d882-167">Войдите в систему в мобильном приложении</span><span class="sxs-lookup"><span data-stu-id="0d882-167">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="0d882-168">Запустите приложение на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="0d882-168">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="0d882-169">Введите URL-адрес Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="0d882-169">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="0d882-170">При первом входе появится запрос имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="0d882-170">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="0d882-171">Введите свои учетные данные.</span><span class="sxs-lookup"><span data-stu-id="0d882-171">Enter your credentials.</span></span>
4.  <span data-ttu-id="0d882-172">После входа будут показаны доступные рабочие области для вашей компании.</span><span class="sxs-lookup"><span data-stu-id="0d882-172">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="0d882-173">Обратите внимание, что если позже системный администратор опубликует новую рабочую область, вам потребуется обновить список мобильных рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="0d882-173">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="0d882-174">[![Потянуть для обновления](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="0d882-174">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a><span data-ttu-id="0d882-175">Просмотр производительности центра затрат с помощью мобильной рабочей области управления затратами</span><span class="sxs-lookup"><span data-stu-id="0d882-175">View the performance of your cost center by using the Cost controlling mobile workspace</span></span>

1.  <span data-ttu-id="0d882-176">На мобильном устройстве выберите рабочую область **Управление затратами**.</span><span class="sxs-lookup"><span data-stu-id="0d882-176">On your mobile device, select the **Cost controlling** workspace.</span></span>
2.  <span data-ttu-id="0d882-177">Выберите **Управление объектами затрат**.</span><span class="sxs-lookup"><span data-stu-id="0d882-177">Select **Cost object controlling**.</span></span>
3.  <span data-ttu-id="0d882-178">Выберите **Действия**.</span><span class="sxs-lookup"><span data-stu-id="0d882-178">Select **Actions**.</span></span>
4.  <span data-ttu-id="0d882-179">Выберите **Выбрать конфигурацию**, чтобы выбрать макет управления затратами.</span><span class="sxs-lookup"><span data-stu-id="0d882-179">Select **Select configuration** to select a cost controlling layout.</span></span>
5.  <span data-ttu-id="0d882-180">Выберите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="0d882-180">Select **Done**.</span></span>
6.  <span data-ttu-id="0d882-181">Выберите **Действия**.</span><span class="sxs-lookup"><span data-stu-id="0d882-181">Select **Actions**.</span></span>
7.  <span data-ttu-id="0d882-182">Выберите **Выбрать объект затрат** для выбора центров затрат, к которым вам предоставлен доступ.</span><span class="sxs-lookup"><span data-stu-id="0d882-182">Select **Select cost object** to select the cost centers that you've been granted access to.</span></span>
8.  <span data-ttu-id="0d882-183">Выберите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="0d882-183">Select **Done**.</span></span>
9.  <span data-ttu-id="0d882-184">Просмотрите общую производительность вашего центра затрат.</span><span class="sxs-lookup"><span data-stu-id="0d882-184">View the overall performance of your cost center.</span></span>
10. <span data-ttu-id="0d882-185">Выберите ссылку **Сведений для текущего периода**.</span><span class="sxs-lookup"><span data-stu-id="0d882-185">Select the **Details for current period** link.</span></span>
11. <span data-ttu-id="0d882-186">Просмотрите производительность конкретного центра затрат.</span><span class="sxs-lookup"><span data-stu-id="0d882-186">View the performance of individual cost elements.</span></span>
12. <span data-ttu-id="0d882-187">Можно также выполнять поиск конкретных элементов затрат.</span><span class="sxs-lookup"><span data-stu-id="0d882-187">You can also search for specific cost elements.</span></span>

