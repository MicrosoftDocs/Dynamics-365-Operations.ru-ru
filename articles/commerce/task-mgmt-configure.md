---
title: Настройка управления задачами
description: В этом разделе описывается, как настроить функции управления задачами в Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 742d49b1b7b46952d0a8bb6c8a33cde2a35d124f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791711"
---
# <a name="configure-task-management"></a><span data-ttu-id="a7c8b-103">Настройка управления задачами</span><span class="sxs-lookup"><span data-stu-id="a7c8b-103">Configure task management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a7c8b-104">В этом разделе описывается, как настроить функции управления задачами в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-104">This topic describes how to configure task management features in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a7c8b-105">Прежде чем руководители и сотрудники Dynamics 365 Commerce смогут использовать функции управления задачами в модуле Commerce, необходимо настроить управление задачами.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-105">Before Dynamics 365 Commerce managers and employees can use the task management features in Commerce, task management must be configured.</span></span> <span data-ttu-id="a7c8b-106">Этапы настройки включают предоставление разрешений руководителям и сотрудникам, распространение разрешений на клиентов POS-терминалов, настройку уведомлений POS и настройку плитки **задачи** на домашней странице приложения POS.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-106">Configuration steps include granting permissions to managers and employees, distributing permissions to point of sale (POS) clients, setting up POS notifications, and configuring the **Tasks** tile on the home page of a POS application.</span></span>

## <a name="configure-permissions-for-store-managers"></a><span data-ttu-id="a7c8b-107">Настройка разрешений для руководителей магазинов</span><span class="sxs-lookup"><span data-stu-id="a7c8b-107">Configure permissions for store managers</span></span>

<span data-ttu-id="a7c8b-108">Каждый работник в определенном магазине может просматривать все задачи, назначенные этому магазину.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-108">Every worker in a given store can view all tasks that are assigned to that store.</span></span> <span data-ttu-id="a7c8b-109">Они также могут обновлять статус назначенных им задач.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-109">They can also update the status of the tasks that are assigned to them.</span></span> <span data-ttu-id="a7c8b-110">Однако для управления задачами, назначенными магазину, и создания одноцелевых задач такие лица, как руководители магазинов, должны иметь разрешения на управление задачами.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-110">However, personas such as store managers must have task management permissions to manage tasks that are assigned to the store and to create single-purpose tasks.</span></span>

<span data-ttu-id="a7c8b-111">Чтобы настроить разрешения управления задачами для руководителей магазинов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-111">To configure task management permissions for store managers, follow these steps.</span></span>

1. <span data-ttu-id="a7c8b-112">Перейдите в раздел **Retail и Commerce \> Сотрудники \> Группы разрешений**.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-112">Go to **Retail and Commerce \> Employees \> Permission groups**.</span></span>
1. <span data-ttu-id="a7c8b-113">Выберите определенную группу разрешений (например **Руководитель**), а затем выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-113">Select a specific permission group (for example, **Manager**), and then select **Edit**.</span></span>
1. <span data-ttu-id="a7c8b-114">На экспресс-вкладке **Разрешения** задайте для параметра **Разрешить управление задачами** значение **да**.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-114">On the **Permissions** FastTab, set the **Allow task management** option to **Yes**.</span></span>
1. <span data-ttu-id="a7c8b-115">На экспресс-вкладке **уведомления** добавьте операцию **Управление задачами** и введите значение в поле **Порядок отображения**.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-115">On the **Notifications** FastTab, add the **Task management** operation, and enter a value in the **Display order** field.</span></span> <span data-ttu-id="a7c8b-116">Например, введите **2**, если операция **Выполнение заказов** уже имеет значение **Порядок отображения** равное **1**.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-116">For example, enter **2** if the **Order fulfillment** operation already has a **Display order** value of **1**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="a7c8b-117">Если пользователь, не являющийся руководителем, должен иметь разрешения на управление задачами в POS, можно предоставить разрешение на доступ к конкретному пользователю.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-117">If a non-manager persona must have task management permissions in the POS, you can grant permission to the individual.</span></span> <span data-ttu-id="a7c8b-118">Кроме того, можно создать новую группу разрешений для не являющихся руководителями пользователей и установить для параметра **Разрешить управление задачами** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-118">Alternatively, you can create a new permission group for non-managers and set the **Allow task management** option to **Yes**.</span></span>

<span data-ttu-id="a7c8b-119">На следующем рисунке показано, как настроить разрешения управления задачами для руководителей магазинов.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-119">The following illustration shows how to configure task management permissions for store managers.</span></span>

![Настройка разрешения управления задачами для руководителей магазинов](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a><span data-ttu-id="a7c8b-121">Настройка разрешений для сотрудников</span><span class="sxs-lookup"><span data-stu-id="a7c8b-121">Configure permissions for employees</span></span>

<span data-ttu-id="a7c8b-122">Сотрудники должны иметь разрешения на создание списков задач, управление критериями назначения и настройку повторения любого списка задач.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-122">Employees must have permissions to create task lists, manage assignment criteria, and configure the recurrence of any task list.</span></span> <span data-ttu-id="a7c8b-123">Для настройки этих разрешений назначьте сотрудникам роль **Руководителя задачи Retail**.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-123">To configure these permissions, you assign employees to the **Retail task manager** role.</span></span>

<span data-ttu-id="a7c8b-124">Чтобы настроить разрешения для сотрудника, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-124">To configure permissions for an employee, follow these steps.</span></span>

1. <span data-ttu-id="a7c8b-125">Перейдите в раздел **Retail и Commerce \> Сотрудники \> Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-125">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="a7c8b-126">Выберите сотрудника.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-126">Select an employee.</span></span>
1. <span data-ttu-id="a7c8b-127">На экспресс-вкладке **Роли пользователя** выберите **Назначить роли**.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-127">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="a7c8b-128">В диалоговом окне **Назначение ролей пользователю** выберите роль **Руководителя задачи Retail** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-128">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

## <a name="distribute-permissions-to-pos-clients"></a><span data-ttu-id="a7c8b-129">Распределение разрешений для клиентов POS</span><span class="sxs-lookup"><span data-stu-id="a7c8b-129">Distribute permissions to POS clients</span></span>

<span data-ttu-id="a7c8b-130">Прежде чем сотрудники смогут использовать клиенты POS, необходимо распределить разрешения и синхронизировать их с этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-130">Before employees can use POS clients, permissions must be distributed and synced to those clients.</span></span>

<span data-ttu-id="a7c8b-131">Чтобы распределить разрешения на клиенты POS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-131">To distribute permissions to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="a7c8b-132">Перейдите в раздел **Retail и Commerce \> ИТ Retail и Commerce \> График распределения**.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-132">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="a7c8b-133">Выберите план распределения **1060** (**персонал**), а затем выберите **выполнить**.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-133">Select the **1060** (**Staff**) distribution schedule, and then select **Run now**.</span></span>
1. <span data-ttu-id="a7c8b-134">Выберите план распределения **1070** (**конфигурация канала**), а затем выберите **выполнить**.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-134">Select the **1070** (**Channel configuration**) distribution schedule, and then select **Run now**.</span></span>

## <a name="configure-pos-notifications-for-tasks"></a><span data-ttu-id="a7c8b-135">Настройка уведомлений POS для задач</span><span class="sxs-lookup"><span data-stu-id="a7c8b-135">Configure POS notifications for tasks</span></span>

<span data-ttu-id="a7c8b-136">Управление задачами должно быть настроено таким образом, чтобы уведомления были доступны в приложении POS.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-136">Task management must be configured so that notifications are available in the POS application.</span></span>

<span data-ttu-id="a7c8b-137">Чтобы настроить уведомления POS для задач, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-137">To configure POS notifications for tasks, follow these steps.</span></span>

1. <span data-ttu-id="a7c8b-138">Перейдите к **Retail и Commerce \> Настройка канала \> Настройка POS \> POS \> Операции POS**.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-138">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="a7c8b-139">Найдите операцию **1400** (**управление задачами**) и установите флажок **включить уведомления** для этого поля.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-139">Find operation **1400** (**Task management**), and select the **Enable notifications** check box for it.</span></span>

<span data-ttu-id="a7c8b-140">На следующем рисунке показана операция **управления задачами** на странице **Операции POS**.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-140">The following illustration shows the **Task management** operation on the **POS operations** page.</span></span>

![Операция управления задачами на странице Операций POS](media/HQ-POS-Tasks-Notifications.png)

<span data-ttu-id="a7c8b-142">Дополнительные сведения о настройке уведомлений POS см. в [Отображение уведомлений о заказах в POS-терминале](notifications-pos.md).</span><span class="sxs-lookup"><span data-stu-id="a7c8b-142">For more information about how to configure POS notifications, see [Show order notifications in the point of sale (POS)](notifications-pos.md).</span></span>

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a><span data-ttu-id="a7c8b-143">Настройка плитки «задачи» на домашней странице приложения POS</span><span class="sxs-lookup"><span data-stu-id="a7c8b-143">Configure the Tasks tile on a POS application home page</span></span>

<span data-ttu-id="a7c8b-144">Прежде чем настроить плитку **задачи** на домашней странице приложения POS, см. [Макеты экрана для POS-терминала](pos-screen-layouts.md) для получения сведений о настройке и добавлении новых кнопок в макет экрана POS.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-144">Before you configure the **Tasks** tile on the home page of a POS application, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information about how to configure and add new buttons to a POS screen layout.</span></span>

<span data-ttu-id="a7c8b-145">Чтобы настроить плитку **задачи** на домашней странице приложения POS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-145">To configure the **Tasks** tile on a POS application home page, follow these steps.</span></span>

1. <span data-ttu-id="a7c8b-146">Перейдите в раздел **Retail и Commerce \> Настройка канала \> Настройка POS \> POS \> Макеты экрана**.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-146">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> Screen layouts**.</span></span>
1. <span data-ttu-id="a7c8b-147">Выберите макет экрана, выберите размер макета и выберите сетку кнопок.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-147">Select a screen layout, select a layout size, and select a button grid.</span></span>
1. <span data-ttu-id="a7c8b-148">На экспресс-вкладке **сетки кнопок** выберите **конструктор**, чтобы изменить выбранную сетку кнопок.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-148">On the **Button grids** FastTab, select **Designer** to edit the selected button grid.</span></span>
1. <span data-ttu-id="a7c8b-149">Добавьте плитку **задачи** в соответствующий раздел домашней страницы.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-149">Add a **Tasks** tile to the appropriate section of the home page.</span></span>

<span data-ttu-id="a7c8b-150">На следующем рисунке показан пример плитки **Задачи** на домашней странице POS.</span><span class="sxs-lookup"><span data-stu-id="a7c8b-150">The following illustration shows an example of a **Tasks** tile on a POS home page.</span></span>

![Плитка «задачи» на домашней странице POS](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a><span data-ttu-id="a7c8b-152">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a7c8b-152">Additional resources</span></span>

[<span data-ttu-id="a7c8b-153">Обзор управления задачами</span><span class="sxs-lookup"><span data-stu-id="a7c8b-153">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="a7c8b-154">Создание списков задач и добавление задач</span><span class="sxs-lookup"><span data-stu-id="a7c8b-154">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="a7c8b-155">Назначение списков задач магазинам или сотрудникам</span><span class="sxs-lookup"><span data-stu-id="a7c8b-155">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="a7c8b-156">Управление задачами в POS</span><span class="sxs-lookup"><span data-stu-id="a7c8b-156">Task management in POS</span></span>](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
