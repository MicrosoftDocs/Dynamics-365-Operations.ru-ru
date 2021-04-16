---
title: Настройка мобильной рабочей области управления активами
description: В этой теме описывается, как настроить Microsoft Dynamics 365 Supply Chain Management и мобильное приложение Finance and Operations (Dynamics 365) для запуска мобильной рабочей области управления активами, которую работники могут использовать для выполнения задач управления активами.
author: johanhoffmann
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-22
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: bc170df2fc58ae6b42fbc8834caad0bb7cd16f69
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837785"
---
# <a name="set-up-the-asset-management-mobile-workspace"></a><span data-ttu-id="3e483-103">Настройка мобильной рабочей области управления активами</span><span class="sxs-lookup"><span data-stu-id="3e483-103">Set up the Asset management mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3e483-104">В этой теме описывается, как настроить Microsoft Dynamics 365 Supply Chain Management и мобильное приложение Finance and Operations (Dynamics 365) для запуска мобильной рабочей области **Управление активами**, которую работники могут использовать для выполнения задач управления активами.</span><span class="sxs-lookup"><span data-stu-id="3e483-104">This topic describes how to set up Microsoft Dynamics 365 Supply Chain Management and the Finance and Operations (Dynamics 365) mobile app to run an **Asset management** mobile workspace that workers can use to perform asset management tasks.</span></span>

## <a name="set-up-maintenance-worker-users-in-supply-chain-management"></a><span data-ttu-id="3e483-105">Настройка пользователей-специалистов по обслуживанию в Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3e483-105">Set up maintenance worker users in Supply Chain Management</span></span>

<span data-ttu-id="3e483-106">Для каждого пользователя, которому требуется доступ к мобильной рабочей области **Управление активами**, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3e483-106">For each user that requires access to the **Asset management** mobile workspace, follow these steps.</span></span>

1. <span data-ttu-id="3e483-107">В Supply Chain Management перейдите в раздел **Управление персоналом \> Работники** и убедитесь, что для пользователя, которого требуется настроить, существует запись работника.</span><span class="sxs-lookup"><span data-stu-id="3e483-107">In Supply Chain Management, go to **Human resources \> Workers**, and make sure that a worker record exists for the user that you want to set up.</span></span> <span data-ttu-id="3e483-108">Создайте новую запись работника, если требуется.</span><span class="sxs-lookup"><span data-stu-id="3e483-108">Create a new worker record as required.</span></span>
1. <span data-ttu-id="3e483-109">Перейдите в раздел **Управление активами \> Настройка \> Работники \> Работники** и убедитесь, что запись сотрудника, которую вы идентифицировали (или создали) на предыдущем шаге, сопоставлена с записью работника по обслуживанию.</span><span class="sxs-lookup"><span data-stu-id="3e483-109">Go to **Asset management \> Setup \> Workers \> Workers**, and make sure that the worker record that you identified (or created) in the previous step is mapped to a maintenance worker record.</span></span> <span data-ttu-id="3e483-110">Создайте новую запись работника по обслуживанию, если необходимо, и задайте в поле **Работник** запись работника из предыдущего шага.</span><span class="sxs-lookup"><span data-stu-id="3e483-110">Create a new maintenance worker record as required, and set the **Worker** field to the worker record from the previous step.</span></span>
1. <span data-ttu-id="3e483-111">Перейдите в раздел **Управление активами \> Настройка \> Работники \> Группы работников по обслуживанию** и убедитесь, что запись работника по обслуживанию, которую вы идентифицировали (или создали) на предыдущем шаге, принадлежит к группе работников по обслуживанию.</span><span class="sxs-lookup"><span data-stu-id="3e483-111">Go to **Asset management \> Setup \> Workers \> Maintenance worker groups**, and make sure that the maintenance worker record that you identified (or created) in the previous step belongs to a maintenance worker group.</span></span>
1. <span data-ttu-id="3e483-112">Перейдите в раздел **Администрирование системы \> Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="3e483-112">Go to **System administration \> Users**.</span></span>
1. <span data-ttu-id="3e483-113">Выберите соответствующего пользователя в сетке.</span><span class="sxs-lookup"><span data-stu-id="3e483-113">Select the relevant user in the grid.</span></span>
1. <span data-ttu-id="3e483-114">На экспресс-вкладке **Сведения о пользователе** в поле **Физическое лицо** укажите учетную запись работника, которую необходимо связать с текущей учетной записью пользователя.</span><span class="sxs-lookup"><span data-stu-id="3e483-114">On the **User Details** FastTab, set the **Person** field to the worker account that you want to associate with the current user account.</span></span> <span data-ttu-id="3e483-115">Эта учетная запись работника должна быть записью работника, которая была определена (или создана) на шаге 1 и сопоставлена с записью работника по обслуживанию на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="3e483-115">This worker account should be the worker record that you identified (or created) in step 1 and mapped to a maintenance worker record in step 2.</span></span>

> [!NOTE]
> <span data-ttu-id="3e483-116">Разрешения пользователей и роли безопасности применяются к функциям мобильной рабочей области **Управление активами** точно так же, как они применяются к функциям пользовательского интерфейса Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3e483-116">User permissions and security roles apply to the features of the **Asset management** mobile workspace just as they apply to the features of the Supply Chain Management user interface.</span></span> <span data-ttu-id="3e483-117">Таким образом, каждый пользователь, настроенный на доступ к мобильной рабочей области **Управление активами**, должен иметь роли безопасности, необходимые для выполнения подобных операций непосредственно в Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3e483-117">Therefore, every user that you set up to access the **Asset management** mobile workspace must have the security roles that are required to perform similar operations directly in Supply Chain Management.</span></span>

## <a name="publish-the-asset-management-mobile-workspace"></a><span data-ttu-id="3e483-118">Публикация мобильной рабочей области управления активами</span><span class="sxs-lookup"><span data-stu-id="3e483-118">Publish the Asset management mobile workspace</span></span>

<span data-ttu-id="3e483-119">Чтобы функции управления активами были доступны в мобильном приложении Finance and Operations (Dynamics 365), необходимо опубликовать мобильную рабочую область **Управление активами**.</span><span class="sxs-lookup"><span data-stu-id="3e483-119">To make asset management features available in the Finance and Operations (Dynamics 365) mobile app, you must publish the **Asset management** mobile workspace.</span></span>

1. <span data-ttu-id="3e483-120">В Supply Chain Management выберите кнопку **Настройки** (символ шестеренки в верхнем правом углу), затем выберите **Мобильное приложение** в меню.</span><span class="sxs-lookup"><span data-stu-id="3e483-120">In Supply Chain Management, select the **Settings** button (the gear symbol in upper-right corner), and then select **Mobile app** on the menu.</span></span>
1. <span data-ttu-id="3e483-121">В диалоговом окне **Управление мобильным приложением** найдите плитку **Управление активами**.</span><span class="sxs-lookup"><span data-stu-id="3e483-121">In the **Manage mobile app** dialog box, find the **Asset Management** tile.</span></span> <span data-ttu-id="3e483-122">Если она содержит текст "В метаданных — не опубликовано", рабочая область еще не опубликована.</span><span class="sxs-lookup"><span data-stu-id="3e483-122">If it contains the text "In metadata - not published," the workspace hasn't yet been published.</span></span> <span data-ttu-id="3e483-123">Если она содержит текст "В метаданных — опубликована", рабочая область уже опубликована, и оставшаяся часть процедуры может быть пропущена.</span><span class="sxs-lookup"><span data-stu-id="3e483-123">If it contains the text "In metadata - published," the workspace has already been published, and you can skip the rest of this procedure.</span></span>

    <span data-ttu-id="3e483-124">![Диалоговое окно управления мобильным приложением](media/mobile-workspaces.png "Диалоговое окно управления мобильным приложением")</span><span class="sxs-lookup"><span data-stu-id="3e483-124">![Manage mobile app dialog box](media/mobile-workspaces.png "Manage mobile app dialog box")</span></span>

1. <span data-ttu-id="3e483-125">Выберите плитку **Управление активами**, затем выберите **Опубликовать** на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="3e483-125">Select the **Asset Management** tile, and then select **Publish** on the toolbar.</span></span> <span data-ttu-id="3e483-126">Через несколько секунд вы должны получить уведомление о том, что рабочая область успешно опубликована.</span><span class="sxs-lookup"><span data-stu-id="3e483-126">After a few seconds, you should receive a notification that states that the workspace has been successfully published.</span></span> <span data-ttu-id="3e483-127">Кроме того, текст на плитке должен измениться на "В метаданных — опубликована".</span><span class="sxs-lookup"><span data-stu-id="3e483-127">Additionally, the text on the tile should change to "In metadata - published."</span></span>

## <a name="install-and-set-up-the-finance-and-operations-dynamics-365-mobile-app"></a><span data-ttu-id="3e483-128">Установка и настройка мобильного приложения Finance and Operations (Dynamics 365)</span><span class="sxs-lookup"><span data-stu-id="3e483-128">Install and set up the Finance and Operations (Dynamics 365) mobile app</span></span>

1. <span data-ttu-id="3e483-129">Перейдите к одному из следующих магазинов приложений для установки приложения **Microsoft Finance and Operations (Dynamics 365)** на мобильном устройстве:</span><span class="sxs-lookup"><span data-stu-id="3e483-129">Go to one of the following app stores to install the **Microsoft Finance and Operations (Dynamics 365)** app on your mobile device:</span></span>

    - [<span data-ttu-id="3e483-130">Для устройств Google Android</span><span class="sxs-lookup"><span data-stu-id="3e483-130">For Google Android devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
    - [<span data-ttu-id="3e483-131">Для устройств Apple iOS</span><span class="sxs-lookup"><span data-stu-id="3e483-131">For Apple iOS devices</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

1. <span data-ttu-id="3e483-132">Откройте приложение Finance and Operations (Dynamics 365).</span><span class="sxs-lookup"><span data-stu-id="3e483-132">Open the Finance and Operations (Dynamics 365) app.</span></span> <span data-ttu-id="3e483-133">Должна появиться страница входа.</span><span class="sxs-lookup"><span data-stu-id="3e483-133">The sign-in page should appear.</span></span> <span data-ttu-id="3e483-134">В поле **Вход** введите URL-адрес Supply Chain Management или выберите последний URL-адрес в списке **Последние среды**, а затем нажмите **Подключить**.</span><span class="sxs-lookup"><span data-stu-id="3e483-134">In the **Sign in** field, enter your Supply Chain Management URL, or select a recent URL in the **Recent environments** list, and then tap **Connect**.</span></span>

    <span data-ttu-id="3e483-135">![Страница входа](media/mobile-app-sign-in.png "Страница входа")</span><span class="sxs-lookup"><span data-stu-id="3e483-135">![Sign-in page](media/mobile-app-sign-in.png "Sign-in page")</span></span>

1. <span data-ttu-id="3e483-136">Если будет предложено подтвердить подключение, установите флажок **Я понимаю**, затем нажмите **Подключить**.</span><span class="sxs-lookup"><span data-stu-id="3e483-136">If you're prompted to confirm the connection, select the **I understand** check box, and then tap **Connect**.</span></span>
1. <span data-ttu-id="3e483-137">На странице **Выберите учетную запись** используйте свою учетную запись Майкрософт для входа в мобильное приложение.</span><span class="sxs-lookup"><span data-stu-id="3e483-137">On the **Pick an account** page, use your Microsoft account to sign in to the mobile application.</span></span>

    <span data-ttu-id="3e483-138">Появится страница **Рабочие области**.</span><span class="sxs-lookup"><span data-stu-id="3e483-138">The **Workspaces** page appears.</span></span> <span data-ttu-id="3e483-139">На ней перечисляются все мобильные рабочие области, опубликованные вашим экземпляром Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3e483-139">It lists every mobile workspace that has been published by your Supply Chain Management instance.</span></span>

    <span data-ttu-id="3e483-140">![Список рабочих областей](media/mobile-app-workspaces.png "Список рабочих областей")</span><span class="sxs-lookup"><span data-stu-id="3e483-140">![List of workspaces](media/mobile-app-workspaces.png "List of workspaces")</span></span>

1. <span data-ttu-id="3e483-141">Если необходимо изменить юридическое лицо (компанию), коснитесь кнопки меню (иногда называемой "гамбургер" или "кнопка-гамбургер") в верхнем левом углу, затем коснитесь **Изменить компанию**.</span><span class="sxs-lookup"><span data-stu-id="3e483-141">If you must change the legal entity (company), tap the Menu button (sometimes referred to as the hamburger or the hamburger button) in the upper-left corner, and then tap **Change company**.</span></span>

    <span data-ttu-id="3e483-142">![Изменение юридического лица](media/mobile-app-change-comp.png "Изменение юридического лица")</span><span class="sxs-lookup"><span data-stu-id="3e483-142">![Changing the legal entity](media/mobile-app-change-comp.png "Changing the legal entity")</span></span>

1. <span data-ttu-id="3e483-143">На странице **Рабочие области** выберите рабочую область, с которой хотите работать, чтобы открыть ее.</span><span class="sxs-lookup"><span data-stu-id="3e483-143">On the **Workspaces** page, select the workspace that you want to work with to open it.</span></span>

    <span data-ttu-id="3e483-144">![Мобильная рабочая область управления активами](media/mobile-app-asset-workspace.png "Мобильная рабочая область управления активами")</span><span class="sxs-lookup"><span data-stu-id="3e483-144">![Asset management mobile workspace](media/mobile-app-asset-workspace.png "Asset management mobile workspace")</span></span>

## <a name="work-with-the-asset-management-mobile-workspace"></a><span data-ttu-id="3e483-145">Работа с мобильной рабочей областью управления активами</span><span class="sxs-lookup"><span data-stu-id="3e483-145">Work with the Asset management mobile workspace</span></span>

<span data-ttu-id="3e483-146">Дополнительные сведения о работе с мобильной рабочей областью **Управление активами** см. в разделе [Использование мобильной рабочей области управления активами](asset-management-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="3e483-146">For more information about how to work with the **Asset management** mobile workspace, see [Use the Asset management mobile workspace](asset-management-mobile-workspace.md).</span></span>

<span data-ttu-id="3e483-147">Дополнительные сведения о мобильном приложении Finance and Operations (Dynamics 365) см. в разделе [Главная страница мобильного приложения](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="3e483-147">For more information about the Finance and Operations (Dynamics 365) mobile app, see the [Mobile app home page](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]