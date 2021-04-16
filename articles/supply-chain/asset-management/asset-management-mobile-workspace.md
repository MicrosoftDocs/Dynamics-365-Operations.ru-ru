---
title: Использование мобильной рабочей области управления активами
description: В этой теме содержится информация о мобильной рабочей области управления активами.
author: johanhoffmann
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.dyn365.ops.version: 10.0.5
ms.search.validFrom: 2019-08-31
ms.openlocfilehash: 98f935a11ad8a5272cde0270f9ae0471411b914a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837953"
---
# <a name="use-the-asset-management-mobile-workspace"></a><span data-ttu-id="bae12-103">Использование мобильной рабочей области управления активами</span><span class="sxs-lookup"><span data-stu-id="bae12-103">Use the Asset management mobile workspace</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bae12-104">В этой теме содержится информация о мобильной рабочей области **Управление активами**.</span><span class="sxs-lookup"><span data-stu-id="bae12-104">This topic provides information about the **Asset management** mobile workspace.</span></span> <span data-ttu-id="bae12-105">Эта рабочая область позволяет пользователям просматривать и создавать запросы на обслуживание и заказы на работу.</span><span class="sxs-lookup"><span data-stu-id="bae12-105">This workspace lets users view and create maintenance requests and work orders.</span></span> <span data-ttu-id="bae12-106">Пользователи также могут просматривать назначенные задания заказов на работу в представлении календаря или списка.</span><span class="sxs-lookup"><span data-stu-id="bae12-106">Users can also view the assigned work order jobs in a calendar or list view.</span></span> <span data-ttu-id="bae12-107">Можно также просматривать и искать активы и функциональные местоположения.</span><span class="sxs-lookup"><span data-stu-id="bae12-107">Assets and functional locations can also be viewed and searched for.</span></span>

## <a name="overview"></a><span data-ttu-id="bae12-108">Обзор</span><span class="sxs-lookup"><span data-stu-id="bae12-108">Overview</span></span>

<span data-ttu-id="bae12-109">«Управление активами» является передовым модулем для управления активами и заданиями заказов на работу в Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="bae12-109">Asset Management is an advanced module for managing assets and work order jobs in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="bae12-110">Мобильное рабочее пространство **Управления активами** позволяет пользователям быстро просматривать назначенные задания заказов на работу на мобильном устройстве по своему усмотрению.</span><span class="sxs-lookup"><span data-stu-id="bae12-110">The **Asset management** mobile workspace lets users quickly view assigned work order jobs on the mobile device of their choice.</span></span> <span data-ttu-id="bae12-111">Пользователи также могут создавать запросы на обслуживание и управлять ими, обновлять состояние жизненного цикла, а также просматривать сведения о активах и функциональных местоположениях с помощью своего мобильного устройства.</span><span class="sxs-lookup"><span data-stu-id="bae12-111">Users can also create and manage maintenance requests, update lifecycle state, and view asset and functional location details by using their mobile device.</span></span>

<span data-ttu-id="bae12-112">В частности, мобильная рабочая область **Управление активами** позволяет пользователям выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="bae12-112">Specifically, the **Asset management** mobile workspace lets users perform these tasks:</span></span>

- <span data-ttu-id="bae12-113">Создание, просмотр и изменение запросов на обслуживание, съемка фотографии или вложение существующего изображения в запрос обслуживания, изменение состояния жизненного цикла запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="bae12-113">Create, view, and edit maintenance requests, take a photo or attach an existing image to the maintenance request, change the maintenance request lifecycle state.</span></span> 
- <span data-ttu-id="bae12-114">Создание, просмотр и изменение заказов на работу, съемка фотографии или вложение существующего изображения в заказ на работу, изменение состояния жизненного заказа на работу, просмотр заданий заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="bae12-114">Create, view, and edit work orders, take a photo or attach an existing image to the work order, change the work order lifecycle state, view work order jobs.</span></span>
- <span data-ttu-id="bae12-115">Просмотр назначенных заданий заказов на работу в представлении календаря.</span><span class="sxs-lookup"><span data-stu-id="bae12-115">View assigned work order jobs in a calendar view.</span></span>
- <span data-ttu-id="bae12-116">Создание, просмотр и редактирование заданий по заказу на работу, обновление счетчиков активов, просмотр контрольного списка обслуживания, просмотр и изменение примечаний к заданиям заказа на работу, просмотр инструментов, необходимых для задания заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="bae12-116">Create, view, and edit work order job, update asset counters, view maintenance checklist, view and edit work order job notes, view the tools required for the work order job.</span></span>
- <span data-ttu-id="bae12-117">Просмотр или поиск конкретного актива или функционального местоположения.</span><span class="sxs-lookup"><span data-stu-id="bae12-117">View or search for a specific asset or functional location.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bae12-118">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="bae12-118">Prerequisites</span></span>

<span data-ttu-id="bae12-119">Прежде чем можно будет использовать мобильную рабочую область **Управление активами**, администратор должен настроить требуемые учетные записи пользователей и работников и опубликовать рабочую область.</span><span class="sxs-lookup"><span data-stu-id="bae12-119">Before you can use the **Asset management** mobile workspace, your admin must set up the required user and worker accounts, and publish the workspace.</span></span> <span data-ttu-id="bae12-120">Дополнительные сведения см. в разделе [Настройка мобильной рабочей области управления активами](set-up-asset-management-mobile.md).</span><span class="sxs-lookup"><span data-stu-id="bae12-120">For more information, see [Set up the Asset management mobile workspace](set-up-asset-management-mobile.md).</span></span>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="bae12-121">Загрузите и установите мобильное приложение</span><span class="sxs-lookup"><span data-stu-id="bae12-121">Download and install the mobile app</span></span>

<span data-ttu-id="bae12-122">Загрузите и установите мобильное приложение Dynamics 365 for Unified Operations:</span><span class="sxs-lookup"><span data-stu-id="bae12-122">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

- [<span data-ttu-id="bae12-123">Для телефонов Android</span><span class="sxs-lookup"><span data-stu-id="bae12-123">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
- [<span data-ttu-id="bae12-124">Для iPhone</span><span class="sxs-lookup"><span data-stu-id="bae12-124">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="bae12-125">Войдите в систему в мобильном приложении</span><span class="sxs-lookup"><span data-stu-id="bae12-125">Sign in to the mobile app</span></span>

1. <span data-ttu-id="bae12-126">Запустите приложение на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="bae12-126">Start the app on your mobile device.</span></span>

1. <span data-ttu-id="bae12-127">Введите URL-адрес Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="bae12-127">Enter your Dynamics 365 URL.</span></span>

1. <span data-ttu-id="bae12-128">При первом входе появится запрос имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="bae12-128">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="bae12-129">Введите свои учетные данные.</span><span class="sxs-lookup"><span data-stu-id="bae12-129">Enter your credentials.</span></span>

1. <span data-ttu-id="bae12-130">После входа будут показаны доступные рабочие области для вашей компании.</span><span class="sxs-lookup"><span data-stu-id="bae12-130">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="bae12-131">Обратите внимание, что если позже системный администратор опубликует новую рабочую область, вам потребуется обновить список мобильных рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="bae12-131">Note that if your system administrator publishes a new workspace later, you'll have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="bae12-132">![Выберите рабочую область](media/am-mobile-01.png "Выберите рабочую область")</span><span class="sxs-lookup"><span data-stu-id="bae12-132">![Select a workspace](media/am-mobile-01.png "Select a workspace")</span></span>

## <a name="view-assigned-work-order-jobs-in-calendar-view"></a><span data-ttu-id="bae12-133">Просмотр назначенных заданий заказов на работу в представлении календаря</span><span class="sxs-lookup"><span data-stu-id="bae12-133">View assigned work order jobs in calendar view</span></span>

1. <span data-ttu-id="bae12-134">На мобильном устройстве откройте рабочую область **Управление активами**.</span><span class="sxs-lookup"><span data-stu-id="bae12-134">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="bae12-135">Выберите **Календарь моих заданий заказов на работу**.</span><span class="sxs-lookup"><span data-stu-id="bae12-135">Select **My work order jobs calendar**.</span></span>

1. <span data-ttu-id="bae12-136">Выберите дату, на которую вы хотите просмотреть задания заказов на работу.</span><span class="sxs-lookup"><span data-stu-id="bae12-136">Select the date you want to view work order jobs for.</span></span> <span data-ttu-id="bae12-137">В списке вы увидите код актива и код функционального местоположения для каждого задания заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="bae12-137">In the list, you'll see the asset ID and functional location ID for each work order job.</span></span>

1. <span data-ttu-id="bae12-138">Выберите задание заказа на работу в списке, чтобы просмотреть подробные сведения о задании: сведения о активах и функциональных местоположениях, а также другие навигационные ссылки для просмотра пунктов **Вложения**, **Контрольные списки**, **Инструменты**, **Счетчики активов**, **Примечания**, **Журналы**.</span><span class="sxs-lookup"><span data-stu-id="bae12-138">Select a work order job in the list to see job details: Asset and functional location details as well as other navigation links to view **Attachments**, **Checklists**, **Tools**, **Asset counters**, **Notes**, **Journals**.</span></span>

    <span data-ttu-id="bae12-139">![Просмотр назначенных заданий заказов на работу в представлении календаря](media/am-mobile-02.png "Просмотр назначенных заданий заказов на работу в представлении календаря")</span><span class="sxs-lookup"><span data-stu-id="bae12-139">![View assigned work order jobs in calendar view](media/am-mobile-02.png "View assigned work order jobs in calendar view")</span></span>

## <a name="create-a-work-order-job"></a><span data-ttu-id="bae12-140">Создание задания заказа на работу</span><span class="sxs-lookup"><span data-stu-id="bae12-140">Create a work order job</span></span>

1. <span data-ttu-id="bae12-141">На мобильном устройстве откройте рабочую область **Управление активами**.</span><span class="sxs-lookup"><span data-stu-id="bae12-141">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="bae12-142">Выберите **Все заказы на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="bae12-142">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="bae12-143">Выберите заказ на работу, для которого требуется создать новое задание заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="bae12-143">Select the work order you want to create a new work order job for.</span></span>

1. <span data-ttu-id="bae12-144">Выберите кнопку **Добавить строку**.</span><span class="sxs-lookup"><span data-stu-id="bae12-144">Select the **Add line** button.</span></span>

1. <span data-ttu-id="bae12-145">Выберите **Актив**, для которого требуется создать задание заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="bae12-145">Select the **Asset** you want to create a work order job for.</span></span>

1. <span data-ttu-id="bae12-146">Выберите **Тип задания обслуживания**, **Вариант типа задания обслуживания** и **Специальность**.</span><span class="sxs-lookup"><span data-stu-id="bae12-146">Select **Maintenance job type**, **Maintenance job type variant** and **Trade**.</span></span>

1. <span data-ttu-id="bae12-147">Выберите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="bae12-147">Select **Done**.</span></span>

    <span data-ttu-id="bae12-148">![Экран добавления строки](media/am-mobile-03.png "Экран добавления строки")</span><span class="sxs-lookup"><span data-stu-id="bae12-148">![The Add line screen](media/am-mobile-03.png "The Add line screen")</span></span>


## <a name="add-attachment-to-a-work-order-job"></a><span data-ttu-id="bae12-149">Добавление вложения в задание заказа на работу</span><span class="sxs-lookup"><span data-stu-id="bae12-149">Add attachment to a work order job</span></span>

1. <span data-ttu-id="bae12-150">На мобильном устройстве откройте рабочую область **Управление активами**.</span><span class="sxs-lookup"><span data-stu-id="bae12-150">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="bae12-151">Выберите **Все заказы на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="bae12-151">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="bae12-152">Выберите заказ на работу > задание заказа на работу, для которого требуется добавить вложение.</span><span class="sxs-lookup"><span data-stu-id="bae12-152">Select the work order > work order job you want to add an attachment to.</span></span>
    - <span data-ttu-id="bae12-153">Кроме того, можно выбрать **Календарь моих заданий заказов на работу** или **Список моих заданий заказов на работу** на домашней странице, чтобы перейти на страницу **Сведения о задании заказа на работу**.</span><span class="sxs-lookup"><span data-stu-id="bae12-153">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **Work order job details** page.</span></span>

1. <span data-ttu-id="bae12-154">Выберите **Вложения** на странице **Сведения о задании заказа на работу**.</span><span class="sxs-lookup"><span data-stu-id="bae12-154">Select **Attachments** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="bae12-155">Вы увидите существующие вложения в задании заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="bae12-155">You'll see existing attachments on the work order job.</span></span> <span data-ttu-id="bae12-156">Выберите **Добавить вложение**.</span><span class="sxs-lookup"><span data-stu-id="bae12-156">Select **Add attachment**.</span></span>

1. <span data-ttu-id="bae12-157">Введите **Имя** и **Примечания** для вложения.</span><span class="sxs-lookup"><span data-stu-id="bae12-157">Enter **Name** and **Notes** for the attachment.</span></span>

1. <span data-ttu-id="bae12-158">Выберите **Выбрать изображение**, чтобы выбрать фотографию из галереи мобильного устройства, или **Снять фотографию**, чтобы сделать фотографию.</span><span class="sxs-lookup"><span data-stu-id="bae12-158">Select **Choose image** to select a photo from the mobile gallery, or **Take photo** to take a photo.</span></span>

1. <span data-ttu-id="bae12-159">Выберите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="bae12-159">Select **Done**.</span></span>

    <span data-ttu-id="bae12-160">![Просмотр и добавление вложений в задание заказа на работу](media/am-mobile-04.png "Просмотр и добавление вложений в задание заказа на работу")</span><span class="sxs-lookup"><span data-stu-id="bae12-160">![View and add attachments for a work order job](media/am-mobile-04.png "View and add attachments for a work order job")</span></span>

## <a name="view-maintenance-checklist-on-a-work-order-job"></a><span data-ttu-id="bae12-161">Просмотр контрольного списка обслуживания для задания заказа на работу</span><span class="sxs-lookup"><span data-stu-id="bae12-161">View maintenance checklist on a work order job</span></span>

1. <span data-ttu-id="bae12-162">На мобильном устройстве откройте рабочую область **Управление активами**.</span><span class="sxs-lookup"><span data-stu-id="bae12-162">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="bae12-163">Выберите **Все заказы на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="bae12-163">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="bae12-164">Выберите заказ на работу > задание заказа на работу, для которого требуется просмотреть контрольный список.</span><span class="sxs-lookup"><span data-stu-id="bae12-164">Select the work order > work order job you want to view checklists for.</span></span>
    - <span data-ttu-id="bae12-165">Кроме того, можно выбрать **Календарь моих заданий заказов на работу** или **Список моих заданий заказов на работу** на домашней странице, чтобы перейти на страницу **Сведения о задании заказа на работу**.</span><span class="sxs-lookup"><span data-stu-id="bae12-165">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

1. <span data-ttu-id="bae12-166">Выберите **Контрольные списки** на странице **Сведения о задании заказа на работу**.</span><span class="sxs-lookup"><span data-stu-id="bae12-166">Select **Checklists** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="bae12-167">Будет отображен список строк контрольного списка, связанного с заданием заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="bae12-167">You'll see a list of checklist lines related to the work order job.</span></span> <span data-ttu-id="bae12-168">Выбор строку контрольного списка для просмотра **Инструкций** и добавления **Примечаний**.</span><span class="sxs-lookup"><span data-stu-id="bae12-168">Select a checklist line to view **Instructions** and add **Notes**.</span></span>

1. <span data-ttu-id="bae12-169">Нажмите кнопку возврата (**<**), чтобы вернуться на предыдущую страницу.</span><span class="sxs-lookup"><span data-stu-id="bae12-169">Select the back button (**<**) to return to the previous page.</span></span>

    <span data-ttu-id="bae12-170">![Контрольный список обслуживания и сведения о строке](media/am-mobile-05.png "Контрольный список обслуживания и сведения о строке")</span><span class="sxs-lookup"><span data-stu-id="bae12-170">![Maintenance checklist and line details](media/am-mobile-05.png "Maintenance checklist and line details")</span></span>

## <a name="view-and-update-asset-counters-on-a-work-order-job"></a><span data-ttu-id="bae12-171">Просмотр и обновление счетчиков активов в задании заказа на работу</span><span class="sxs-lookup"><span data-stu-id="bae12-171">View and update asset counters on a work order job</span></span>

1. <span data-ttu-id="bae12-172">На мобильном устройстве откройте рабочую область **Управление активами**.</span><span class="sxs-lookup"><span data-stu-id="bae12-172">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="bae12-173">Выберите **Все заказы на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="bae12-173">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="bae12-174">Выберите заказ на работу > задание заказа на работу, для которого требуется просмотреть счетчики активов.</span><span class="sxs-lookup"><span data-stu-id="bae12-174">Select the work order > work order job you want to view asset counters for.</span></span>
    - <span data-ttu-id="bae12-175">Кроме того, можно выбрать **Календарь моих заданий заказов на работу** или **Список моих заданий заказов на работу** на домашней странице, чтобы перейти на страницу **Сведения о задании заказа на работу**.</span><span class="sxs-lookup"><span data-stu-id="bae12-175">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

1. <span data-ttu-id="bae12-176">Выберите **Счетчики актива** на странице **Сведения о задании заказа на работу**.</span><span class="sxs-lookup"><span data-stu-id="bae12-176">Select **Asset counters** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="bae12-177">Вы увидите список счетчиков актива, связанного с заданием заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="bae12-177">You see a list of asset counters related to the work order job.</span></span> <span data-ttu-id="bae12-178">Чтобы обновить значение счетчика, выберите значок карандаша в строке счетчика актива.</span><span class="sxs-lookup"><span data-stu-id="bae12-178">Select the pencil icon on an asset counter line to update the counter value.</span></span>

1. <span data-ttu-id="bae12-179">Введите новое значение счетчика и выберите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="bae12-179">Enter a new counter value, and select **Done**.</span></span>

    <span data-ttu-id="bae12-180">![Просмотр и обновление счетчиков актива](media/am-mobile-06.png "Просмотр и обновление счетчиков актива")</span><span class="sxs-lookup"><span data-stu-id="bae12-180">![View and update asset counters](media/am-mobile-06.png "View and update asset counters")</span></span>

## <a name="register-consumption-on-a-work-order-job"></a><span data-ttu-id="bae12-181">Регистрация потребления в задании заказа на работу</span><span class="sxs-lookup"><span data-stu-id="bae12-181">Register consumption on a work order job</span></span>

1. <span data-ttu-id="bae12-182">На мобильном устройстве откройте рабочую область **Управление активами**.</span><span class="sxs-lookup"><span data-stu-id="bae12-182">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="bae12-183">Выберите **Все заказы на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="bae12-183">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="bae12-184">Выберите заказ на работу > задание заказа на работу, для которого требуется добавить регистрации потребления.</span><span class="sxs-lookup"><span data-stu-id="bae12-184">Select the work order > work order job you want to add consumption registrations for.</span></span>
    - <span data-ttu-id="bae12-185">Кроме того, можно выбрать **Календарь моих заданий заказов на работу** или **Список моих заданий заказов на работу** на домашней странице, чтобы перейти на страницу **Сведения о задании заказа на работу**.</span><span class="sxs-lookup"><span data-stu-id="bae12-185">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

1. <span data-ttu-id="bae12-186">Выберите **Журналы** на странице **Сведения о задании заказа на работу**.</span><span class="sxs-lookup"><span data-stu-id="bae12-186">Select **Journals** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="bae12-187">Выберите **Добавление часов** для создания регистраций рабочего времени.</span><span class="sxs-lookup"><span data-stu-id="bae12-187">Select **Add hours** to create work hour registrations.</span></span>
    1. <span data-ttu-id="bae12-188">Выберите **Категорию** в поле подстановки.</span><span class="sxs-lookup"><span data-stu-id="bae12-188">Select the **Category** from the lookup.</span></span>
    1. <span data-ttu-id="bae12-189">В поле **Часы** введите количество рабочих часов, потраченных на задание заказа на работу.</span><span class="sxs-lookup"><span data-stu-id="bae12-189">In the **Hours** field, enter the number of work hours spent on the work order job.</span></span>
    1. <span data-ttu-id="bae12-190">Выберите соответствующее **Свойство строки**.</span><span class="sxs-lookup"><span data-stu-id="bae12-190">Select the appropriate **Line property**.</span></span>
    1. <span data-ttu-id="bae12-191">Выберите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="bae12-191">Select **Done**.</span></span>

1. <span data-ttu-id="bae12-192">Выберите **Добавить номенклатуры** для создания регистраций номенклатур.</span><span class="sxs-lookup"><span data-stu-id="bae12-192">Select **Add items** to create item registrations.</span></span>
    1. <span data-ttu-id="bae12-193">Выберите **Код номенклатуры** в поле подстановки.</span><span class="sxs-lookup"><span data-stu-id="bae12-193">Select the **Item number** from the lookup.</span></span>
    1. <span data-ttu-id="bae12-194">Выберите **Место** в поле подстановки.</span><span class="sxs-lookup"><span data-stu-id="bae12-194">Select the **Site** from the lookup.</span></span>
    1. <span data-ttu-id="bae12-195">Введите **Количество** израсходованной номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="bae12-195">Enter the **Quantity** of items consumed.</span></span>
    1. <span data-ttu-id="bae12-196">Выберите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="bae12-196">Select **Done**.</span></span>

1. <span data-ttu-id="bae12-197">Выберите **Добавить расход** для создания регистраций расходов.</span><span class="sxs-lookup"><span data-stu-id="bae12-197">Select **Add expense** to create expense registrations.</span></span>
    1. <span data-ttu-id="bae12-198">Выберите **Категорию** в поле подстановки.</span><span class="sxs-lookup"><span data-stu-id="bae12-198">Select the **Category** from the lookup.</span></span>
    1. <span data-ttu-id="bae12-199">Ввод количества для регистрации расхода.</span><span class="sxs-lookup"><span data-stu-id="bae12-199">Enter the quantity for the expense registration.</span></span>
    1. <span data-ttu-id="bae12-200">Выберите **Валюту продажи** в поле подстановки.</span><span class="sxs-lookup"><span data-stu-id="bae12-200">Select the **Sales currency** from the lookup.</span></span>
    1. <span data-ttu-id="bae12-201">Введите **Себестоимость** для регистрации расхода.</span><span class="sxs-lookup"><span data-stu-id="bae12-201">Enter the **Cost price** for the expense registration.</span></span>
    1. <span data-ttu-id="bae12-202">Выберите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="bae12-202">Select **Done**.</span></span>

    <span data-ttu-id="bae12-203">![Обновление журнала заказов на работу](media/am-mobile-07.png "Обновление журнала заказов на работу")</span><span class="sxs-lookup"><span data-stu-id="bae12-203">![Update a work order journal](media/am-mobile-07.png "Update a work order journal")</span></span>

## <a name="update-lifecycle-state-on-a-work-order"></a><span data-ttu-id="bae12-204">Обновление состояния жизненного цикла по заказу на работу</span><span class="sxs-lookup"><span data-stu-id="bae12-204">Update lifecycle state on a work order</span></span>

1. <span data-ttu-id="bae12-205">На мобильном устройстве откройте рабочую область **Управление активами**.</span><span class="sxs-lookup"><span data-stu-id="bae12-205">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="bae12-206">Выберите **Все заказы на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="bae12-206">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="bae12-207">Выберите заказ на работу, для которого требуется обновить состояние жизненного цикла.</span><span class="sxs-lookup"><span data-stu-id="bae12-207">Select the work order you want to update lifecycle state for.</span></span>

1. <span data-ttu-id="bae12-208">Выберите кнопку **Обновить состояние** в нижней части экрана.</span><span class="sxs-lookup"><span data-stu-id="bae12-208">Select the **Update state** button at the bottom of the screen.</span></span>

1. <span data-ttu-id="bae12-209">Выберите новое состояние жизненного цикла из списка.</span><span class="sxs-lookup"><span data-stu-id="bae12-209">Select a new lifecycle state from the list.</span></span>

1. <span data-ttu-id="bae12-210">Выберите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="bae12-210">Select **Done**.</span></span>

    <span data-ttu-id="bae12-211">![Обновление состояния жизненного цикла по заказу на работу](media/am-mobile-08.png "Обновление состояния жизненного цикла по заказу на работу")</span><span class="sxs-lookup"><span data-stu-id="bae12-211">![Update lifecycle state on a work order](media/am-mobile-08.png "Update lifecycle state on a work order")</span></span>

## <a name="create-a-maintenance-request"></a><span data-ttu-id="bae12-212">Создание запроса на обслуживание</span><span class="sxs-lookup"><span data-stu-id="bae12-212">Create a maintenance request</span></span>

1. <span data-ttu-id="bae12-213">На мобильном устройстве откройте рабочую область **Управление активами**.</span><span class="sxs-lookup"><span data-stu-id="bae12-213">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="bae12-214">Выберите **Все запросы на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="bae12-214">Select **All maintenance requests**.</span></span>

1. <span data-ttu-id="bae12-215">Выберите **Действия** в нижней части экрана и выберите **Создать запрос на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="bae12-215">Select **Actions** at the bottom of the screen, and select **Create maintenance request**.</span></span>

1. <span data-ttu-id="bae12-216">Если для запросов на обслуживание в модуле **Управление активами** включена номерная серия , поле **Запрос на обслуживание** скрыто, поскольку оно заполняется автоматически. Если поле **Запрос на обслуживание** является видимым, введите код запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="bae12-216">If number sequence is enabled for maintenance requests in **Asset management**, the **Maintenance request** field is hidden because it is automatically filled out. If the **Maintenance request** field is visible, enter a maintenance request ID.</span></span>

1. <span data-ttu-id="bae12-217">Выберите **Тип запроса на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="bae12-217">Select a **Maintenance request type**.</span></span>

1. <span data-ttu-id="bae12-218">Введите **Описание** для запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="bae12-218">Enter a **Description** for the maintenance request.</span></span>

1. <span data-ttu-id="bae12-219">Выберите **Актив**, для которого требуется создать запрос.</span><span class="sxs-lookup"><span data-stu-id="bae12-219">Select the **Asset** you want to create the request for.</span></span>

1. <span data-ttu-id="bae12-220">Выберите **Уровень обслуживания** для запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="bae12-220">Select the **Service level** for the maintenance request.</span></span>

1. <span data-ttu-id="bae12-221">Выберите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="bae12-221">Select **Done**.</span></span>

    <span data-ttu-id="bae12-222">![Создание запроса на обслуживание](media/am-mobile-09.png "Создание запроса на обслуживание")</span><span class="sxs-lookup"><span data-stu-id="bae12-222">![Create a maintenance request](media/am-mobile-09.png "Create a maintenance request")</span></span>

## <a name="add-attachment-to-a-maintenance-request"></a><span data-ttu-id="bae12-223">Добавление вложения в запрос на обслуживание</span><span class="sxs-lookup"><span data-stu-id="bae12-223">Add attachment to a maintenance request</span></span>

1. <span data-ttu-id="bae12-224">На мобильном устройстве откройте рабочую область **Управление активами**.</span><span class="sxs-lookup"><span data-stu-id="bae12-224">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="bae12-225">Выберите **Все запросы на обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="bae12-225">Select **All maintenance requests**.</span></span>

1. <span data-ttu-id="bae12-226">Выберите запрос на обслуживание, в который требуется добавить вложение.</span><span class="sxs-lookup"><span data-stu-id="bae12-226">Select the maintenance request you want to add an attachment to.</span></span>

1. <span data-ttu-id="bae12-227">Выберите **Вложения** в нижней части экрана.</span><span class="sxs-lookup"><span data-stu-id="bae12-227">Select **Attachments** at the bottom of the screen.</span></span>

1. <span data-ttu-id="bae12-228">Выберите **Добавить вложения**.</span><span class="sxs-lookup"><span data-stu-id="bae12-228">Select **Add attachments**.</span></span>

1. <span data-ttu-id="bae12-229">Введите **Имя** и **Примечания** для вложения.</span><span class="sxs-lookup"><span data-stu-id="bae12-229">Enter **Name** and **Notes** for the attachment.</span></span>

1. <span data-ttu-id="bae12-230">Выберите **Выбрать изображение**, чтобы выбрать фотографию из галереи мобильного устройства, или **Снять фотографию**, чтобы сделать фотографию.</span><span class="sxs-lookup"><span data-stu-id="bae12-230">Select **Choose image** to select a photo from the mobile gallery or **Take photo** to take a photo.</span></span>

1. <span data-ttu-id="bae12-231">Выберите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="bae12-231">Select **Done**.</span></span>

    <span data-ttu-id="bae12-232">![Добавление вложения в запрос на обслуживание](media/am-mobile-10.png "Добавление вложения в запрос на обслуживание")</span><span class="sxs-lookup"><span data-stu-id="bae12-232">![Add an attachment to a maintenance request](media/am-mobile-10.png "Add an attachment to a maintenance request")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]