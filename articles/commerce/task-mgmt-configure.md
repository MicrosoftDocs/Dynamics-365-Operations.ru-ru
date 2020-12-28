---
title: Настройка управления задачами
description: В этом разделе описывается, как настроить функции управления задачами в Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 9a4775c2dba2b9aa8e671ab6c246000303b3a37e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4415303"
---
# <a name="configure-task-management"></a><span data-ttu-id="a0608-103">Настройка управления задачами</span><span class="sxs-lookup"><span data-stu-id="a0608-103">Configure task management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a0608-104">В этом разделе описывается, как настроить функции управления задачами в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a0608-104">This topic describes how to configure task management features in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a0608-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="a0608-105">Overview</span></span>

<span data-ttu-id="a0608-106">Прежде чем руководители и сотрудники Dynamics 365 Commerce смогут использовать функции управления задачами в модуле Commerce, необходимо настроить управление задачами.</span><span class="sxs-lookup"><span data-stu-id="a0608-106">Before Dynamics 365 Commerce managers and employees can use the task management features in Commerce, task management must be configured.</span></span> <span data-ttu-id="a0608-107">Этапы настройки включают предоставление разрешений руководителям и сотрудникам, распространение разрешений на клиентов POS-терминалов, настройку уведомлений POS и настройку плитки **задачи** на домашней странице приложения POS.</span><span class="sxs-lookup"><span data-stu-id="a0608-107">Configuration steps include granting permissions to managers and employees, distributing permissions to point of sale (POS) clients, setting up POS notifications, and configuring the **Tasks** tile on the home page of a POS application.</span></span>

## <a name="configure-permissions-for-store-managers"></a><span data-ttu-id="a0608-108">Настройка разрешений для руководителей магазинов</span><span class="sxs-lookup"><span data-stu-id="a0608-108">Configure permissions for store managers</span></span>

<span data-ttu-id="a0608-109">Каждый работник в определенном магазине может просматривать все задачи, назначенные этому магазину.</span><span class="sxs-lookup"><span data-stu-id="a0608-109">Every worker in a given store can view all tasks that are assigned to that store.</span></span> <span data-ttu-id="a0608-110">Они также могут обновлять статус назначенных им задач.</span><span class="sxs-lookup"><span data-stu-id="a0608-110">They can also update the status of the tasks that are assigned to them.</span></span> <span data-ttu-id="a0608-111">Однако для управления задачами, назначенными магазину, и создания одноцелевых задач такие лица, как руководители магазинов, должны иметь разрешения на управление задачами.</span><span class="sxs-lookup"><span data-stu-id="a0608-111">However, personas such as store managers must have task management permissions to manage tasks that are assigned to the store and to create single-purpose tasks.</span></span>

<span data-ttu-id="a0608-112">Чтобы настроить разрешения управления задачами для руководителей магазинов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a0608-112">To configure task management permissions for store managers, follow these steps.</span></span>

1. <span data-ttu-id="a0608-113">Перейдите в раздел **Retail и Commerce \> Сотрудники \> Группы разрешений**.</span><span class="sxs-lookup"><span data-stu-id="a0608-113">Go to **Retail and Commerce \> Employees \> Permission groups**.</span></span>
1. <span data-ttu-id="a0608-114">Выберите определенную группу разрешений (например **Руководитель**), а затем выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="a0608-114">Select a specific permission group (for example, **Manager**), and then select **Edit**.</span></span>
1. <span data-ttu-id="a0608-115">На экспресс-вкладке **Разрешения** задайте для параметра **Разрешить управление задачами** значение **да**.</span><span class="sxs-lookup"><span data-stu-id="a0608-115">On the **Permissions** FastTab, set the **Allow task management** option to **Yes**.</span></span>
1. <span data-ttu-id="a0608-116">На экспресс-вкладке **уведомления** добавьте операцию **Управление задачами** и введите значение в поле **Порядок отображения**.</span><span class="sxs-lookup"><span data-stu-id="a0608-116">On the **Notifications** FastTab, add the **Task management** operation, and enter a value in the **Display order** field.</span></span> <span data-ttu-id="a0608-117">Например, введите **2**, если операция **Выполнение заказов** уже имеет значение **Порядок отображения** равное **1**.</span><span class="sxs-lookup"><span data-stu-id="a0608-117">For example, enter **2** if the **Order fulfillment** operation already has a **Display order** value of **1**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="a0608-118">Если пользователь, не являющийся руководителем, должен иметь разрешения на управление задачами в POS, можно предоставить разрешение на доступ к конкретному пользователю.</span><span class="sxs-lookup"><span data-stu-id="a0608-118">If a non-manager persona must have task management permissions in the POS, you can grant permission to the individual.</span></span> <span data-ttu-id="a0608-119">Кроме того, можно создать новую группу разрешений для не являющихся руководителями пользователей и установить для параметра **Разрешить управление задачами** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="a0608-119">Alternatively, you can create a new permission group for non-managers and set the **Allow task management** option to **Yes**.</span></span>

<span data-ttu-id="a0608-120">На следующем рисунке показано, как настроить разрешения управления задачами для руководителей магазинов.</span><span class="sxs-lookup"><span data-stu-id="a0608-120">The following illustration shows how to configure task management permissions for store managers.</span></span>

![Настройка разрешения управления задачами для руководителей магазинов](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a><span data-ttu-id="a0608-122">Настройка разрешений для сотрудников</span><span class="sxs-lookup"><span data-stu-id="a0608-122">Configure permissions for employees</span></span>

<span data-ttu-id="a0608-123">Сотрудники должны иметь разрешения на создание списков задач, управление критериями назначения и настройку повторения любого списка задач.</span><span class="sxs-lookup"><span data-stu-id="a0608-123">Employees must have permissions to create task lists, manage assignment criteria, and configure the recurrence of any task list.</span></span> <span data-ttu-id="a0608-124">Для настройки этих разрешений назначьте сотрудникам роль **Руководителя задачи Retail**.</span><span class="sxs-lookup"><span data-stu-id="a0608-124">To configure these permissions, you assign employees to the **Retail task manager** role.</span></span>

<span data-ttu-id="a0608-125">Чтобы настроить разрешения для сотрудника, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a0608-125">To configure permissions for an employee, follow these steps.</span></span>

1. <span data-ttu-id="a0608-126">Перейдите в раздел **Retail и Commerce \> Сотрудники \> Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="a0608-126">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="a0608-127">Выберите сотрудника.</span><span class="sxs-lookup"><span data-stu-id="a0608-127">Select an employee.</span></span>
1. <span data-ttu-id="a0608-128">На экспресс-вкладке **Роли пользователя** выберите **Назначить роли**.</span><span class="sxs-lookup"><span data-stu-id="a0608-128">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="a0608-129">В диалоговом окне **Назначение ролей пользователю** выберите роль **Руководителя задачи Retail** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a0608-129">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

## <a name="distribute-permissions-to-pos-clients"></a><span data-ttu-id="a0608-130">Распределение разрешений для клиентов POS</span><span class="sxs-lookup"><span data-stu-id="a0608-130">Distribute permissions to POS clients</span></span>

<span data-ttu-id="a0608-131">Прежде чем сотрудники смогут использовать клиенты POS, необходимо распределить разрешения и синхронизировать их с этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="a0608-131">Before employees can use POS clients, permissions must be distributed and synced to those clients.</span></span>

<span data-ttu-id="a0608-132">Чтобы распределить разрешения на клиенты POS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a0608-132">To distribute permissions to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="a0608-133">Перейдите в раздел **Retail и Commerce \> ИТ Retail и Commerce \> График распределения**.</span><span class="sxs-lookup"><span data-stu-id="a0608-133">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="a0608-134">Выберите план распределения **1060** (**персонал**), а затем выберите **выполнить**.</span><span class="sxs-lookup"><span data-stu-id="a0608-134">Select the **1060** (**Staff**) distribution schedule, and then select **Run now**.</span></span>
1. <span data-ttu-id="a0608-135">Выберите план распределения **1070** (**конфигурация канала**), а затем выберите **выполнить**.</span><span class="sxs-lookup"><span data-stu-id="a0608-135">Select the **1070** (**Channel configuration**) distribution schedule, and then select **Run now**.</span></span>

## <a name="configure-pos-notifications-for-tasks"></a><span data-ttu-id="a0608-136">Настройка уведомлений POS для задач</span><span class="sxs-lookup"><span data-stu-id="a0608-136">Configure POS notifications for tasks</span></span>

<span data-ttu-id="a0608-137">Управление задачами должно быть настроено таким образом, чтобы уведомления были доступны в приложении POS.</span><span class="sxs-lookup"><span data-stu-id="a0608-137">Task management must be configured so that notifications are available in the POS application.</span></span>

<span data-ttu-id="a0608-138">Чтобы настроить уведомления POS для задач, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a0608-138">To configure POS notifications for tasks, follow these steps.</span></span>

1. <span data-ttu-id="a0608-139">Перейдите к **Retail и Commerce \> Настройка канала \> Настройка POS \> POS \> Операции POS**.</span><span class="sxs-lookup"><span data-stu-id="a0608-139">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="a0608-140">Найдите операцию **1400** (**управление задачами**) и установите флажок **включить уведомления** для этого поля.</span><span class="sxs-lookup"><span data-stu-id="a0608-140">Find operation **1400** (**Task management**), and select the **Enable notifications** check box for it.</span></span>

<span data-ttu-id="a0608-141">На следующем рисунке показана операция **управления задачами** на странице **Операции POS**.</span><span class="sxs-lookup"><span data-stu-id="a0608-141">The following illustration shows the **Task management** operation on the **POS operations** page.</span></span>

![Операция управления задачами на странице Операций POS](media/HQ-POS-Tasks-Notifications.png)

<span data-ttu-id="a0608-143">Дополнительные сведения о настройке уведомлений POS см. в [Отображение уведомлений о заказах в POS-терминале](notifications-pos.md).</span><span class="sxs-lookup"><span data-stu-id="a0608-143">For more information about how to configure POS notifications, see [Show order notifications in the point of sale (POS)](notifications-pos.md).</span></span>

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a><span data-ttu-id="a0608-144">Настройка плитки «задачи» на домашней странице приложения POS</span><span class="sxs-lookup"><span data-stu-id="a0608-144">Configure the Tasks tile on a POS application home page</span></span>

<span data-ttu-id="a0608-145">Прежде чем настроить плитку **задачи** на домашней странице приложения POS, см. [Макеты экрана для POS-терминала](pos-screen-layouts.md) для получения сведений о настройке и добавлении новых кнопок в макет экрана POS.</span><span class="sxs-lookup"><span data-stu-id="a0608-145">Before you configure the **Tasks** tile on the home page of a POS application, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information about how to configure and add new buttons to a POS screen layout.</span></span>

<span data-ttu-id="a0608-146">Чтобы настроить плитку **задачи** на домашней странице приложения POS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a0608-146">To configure the **Tasks** tile on a POS application home page, follow these steps.</span></span>

1. <span data-ttu-id="a0608-147">Перейдите в раздел **Retail и Commerce \> Настройка канала \> Настройка POS \> POS \> Макеты экрана**.</span><span class="sxs-lookup"><span data-stu-id="a0608-147">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> Screen layouts**.</span></span>
1. <span data-ttu-id="a0608-148">Выберите макет экрана, выберите размер макета и выберите сетку кнопок.</span><span class="sxs-lookup"><span data-stu-id="a0608-148">Select a screen layout, select a layout size, and select a button grid.</span></span>
1. <span data-ttu-id="a0608-149">На экспресс-вкладке **сетки кнопок** выберите **конструктор**, чтобы изменить выбранную сетку кнопок.</span><span class="sxs-lookup"><span data-stu-id="a0608-149">On the **Button grids** FastTab, select **Designer** to edit the selected button grid.</span></span>
1. <span data-ttu-id="a0608-150">Добавьте плитку **задачи** в соответствующий раздел домашней страницы.</span><span class="sxs-lookup"><span data-stu-id="a0608-150">Add a **Tasks** tile to the appropriate section of the home page.</span></span>

<span data-ttu-id="a0608-151">На следующем рисунке показан пример плитки **Задачи** на домашней странице POS.</span><span class="sxs-lookup"><span data-stu-id="a0608-151">The following illustration shows an example of a **Tasks** tile on a POS home page.</span></span>

![Плитка «задачи» на домашней странице POS](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a><span data-ttu-id="a0608-153">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a0608-153">Additional resources</span></span>

[<span data-ttu-id="a0608-154">Обзор управления задачами</span><span class="sxs-lookup"><span data-stu-id="a0608-154">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="a0608-155">Создание списков задач и добавление задач</span><span class="sxs-lookup"><span data-stu-id="a0608-155">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="a0608-156">Назначение списков задач магазинам или сотрудникам</span><span class="sxs-lookup"><span data-stu-id="a0608-156">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="a0608-157">Управление задачами в POS</span><span class="sxs-lookup"><span data-stu-id="a0608-157">Task management in POS</span></span>](task-mgmt-POS.md)
