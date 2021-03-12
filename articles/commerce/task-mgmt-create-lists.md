---
title: Создание списков задач и добавление задач
description: В этом разделе описывается, как создавать списки задач и добавлять задачи в них в Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: cca5e0efd6516d02c372e8a616b6bb0c39f3088c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006218"
---
# <a name="create-task-lists-and-add-tasks"></a><span data-ttu-id="2defb-103">Создание списков задач и добавление задач</span><span class="sxs-lookup"><span data-stu-id="2defb-103">Create task lists and add tasks</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2defb-104">В этом разделе описывается, как создавать списки задач и добавлять задачи в них в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2defb-104">This topic describes how to create task lists and add tasks to them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2defb-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="2defb-105">Overview</span></span>

<span data-ttu-id="2defb-106">*Задача* определяет конкретный объем работ или действие, которое должно быть выполнено на указанную дату или до ее наступления.</span><span class="sxs-lookup"><span data-stu-id="2defb-106">A *task* defines a specific piece of work or an action that someone must complete on or before a specified due date.</span></span> <span data-ttu-id="2defb-107">В Dynamics 365 Commerce задача может включать подробные инструкции и сведения о контактном лице.</span><span class="sxs-lookup"><span data-stu-id="2defb-107">In Dynamics 365 Commerce, a task can include detailed instructions and information about a contact person.</span></span> <span data-ttu-id="2defb-108">Она также может включать в себя ссылки на операции бэк-офис, операции POS-терминала или на страницы сайта, чтобы повысить производительность и предоставить контекст, необходимый владельцу задачи для эффективного выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="2defb-108">It can also include links to back-office operations, point of sale (POS) operations, or site pages, to help improve productivity and provide the context that the task owner requires to complete the task efficiently.</span></span>

<span data-ttu-id="2defb-109">*Список задач* — это совокупность задач, которые должны быть завершены как часть бизнес-процесса.</span><span class="sxs-lookup"><span data-stu-id="2defb-109">A *task list* is a collection of tasks that must be completed as part of a business process.</span></span> <span data-ttu-id="2defb-110">Например, это может быть список задач, который новый работник должен заполнить во время регистрации, список задач для кассиров, работающих в вечерние смены, или список задач, который необходимо заполнить, чтобы подготовить магазин к предстоящему сезону отпусков.</span><span class="sxs-lookup"><span data-stu-id="2defb-110">For example, there might be a task list that a new worker must complete during onboarding, a task list for cashiers who work evening shifts, or a task list that must be completed to prepare the store for an upcoming holiday season.</span></span> <span data-ttu-id="2defb-111">В Commerce каждый список задач с целевой датой может быть назначен любому количеству магазинов или сотрудников, и его можно настроить для повторения.</span><span class="sxs-lookup"><span data-stu-id="2defb-111">In Commerce, every task list that has a target date can be assigned to any number of stores or employees, and it can be configured to recur.</span></span>

<span data-ttu-id="2defb-112">Менеджеры и работники могут создавать списки задач в бэк-офисе Commerce, а затем назначить их набору магазинов.</span><span class="sxs-lookup"><span data-stu-id="2defb-112">Both managers and workers can create task lists in Commerce back office, and then assign them to a set of stores.</span></span>

## <a name="create-a-task-list"></a><span data-ttu-id="2defb-113">Создать список задач</span><span class="sxs-lookup"><span data-stu-id="2defb-113">Create a task list</span></span>

<span data-ttu-id="2defb-114">Выполните следующие действия, чтобы создать список задач.</span><span class="sxs-lookup"><span data-stu-id="2defb-114">To create a task list, follow these steps.</span></span>

1. <span data-ttu-id="2defb-115">Перейдите в **Retail и Commerce \> Управление задачами \> Администрирование управления задачами**.</span><span class="sxs-lookup"><span data-stu-id="2defb-115">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="2defb-116">Выберите **Создать**, а затем введите значения в поля **Имя**, **Описание** и **Владелец**.</span><span class="sxs-lookup"><span data-stu-id="2defb-116">Select **New**, and then enter values in the **Name**, **Description**, and **Owner** fields.</span></span>
1. <span data-ttu-id="2defb-117">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="2defb-117">Select **Save**.</span></span>

## <a name="add-tasks-to-a-task-list"></a><span data-ttu-id="2defb-118">Добавление задач в список задач</span><span class="sxs-lookup"><span data-stu-id="2defb-118">Add tasks to a task list</span></span>

<span data-ttu-id="2defb-119">Чтобы добавить задачи в список задач, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2defb-119">To add tasks to a task list, follow these steps.</span></span>
 
1. <span data-ttu-id="2defb-120">На экспресс-вкладке **Задачи** существующего списка задач выберите **Создать**, чтобы добавить задачу.</span><span class="sxs-lookup"><span data-stu-id="2defb-120">On the **Tasks** FastTab of an existing task list, select **New** to add a task.</span></span>
1. <span data-ttu-id="2defb-121">В диалоговом окне **Создать новую задачу** введите имя задачи в поле **Имя**.</span><span class="sxs-lookup"><span data-stu-id="2defb-121">In the **Create a new task** dialog box, in the **Name** field, enter a name for the task.</span></span>
1. <span data-ttu-id="2defb-122">В поле **Смещение срока от целевой даты** введите положительное или отрицательное целочисленное значение.</span><span class="sxs-lookup"><span data-stu-id="2defb-122">In the **Due data offset from target date** field, enter a positive or negative integer value.</span></span> <span data-ttu-id="2defb-123">Например, введите **-2**, если задача должна быть выполнена за два дня до срока выполнения списка задач.</span><span class="sxs-lookup"><span data-stu-id="2defb-123">For example, enter **-2** if the task should be completed two days before the task list's due date.</span></span>
1. <span data-ttu-id="2defb-124">В поле **примечания** введите подробные инструкции.</span><span class="sxs-lookup"><span data-stu-id="2defb-124">In the **Notes** field, enter detailed instructions.</span></span>
1. <span data-ttu-id="2defb-125">В поле **Контактное лицо** введите имя специалиста по теме, к которому владелец задачи может обратиться, если он нуждается в помощи.</span><span class="sxs-lookup"><span data-stu-id="2defb-125">In the **Contact person** field, enter the name of a subject matter expert that the task owner can contact if he or she needs help.</span></span>
1. <span data-ttu-id="2defb-126">В поле **Ссылка на задачу** введите ссылку на основе природы задачи.</span><span class="sxs-lookup"><span data-stu-id="2defb-126">In the **Task link** field, enter a link, based on the nature of the task.</span></span>

> [!TIP]
> <span data-ttu-id="2defb-127">Хотя поле **назначено** можно использовать для назначения задач пользователю при создании списка задач, рекомендуется избегать назначения задач во время создания списка задач.</span><span class="sxs-lookup"><span data-stu-id="2defb-127">Although you can use the **Assigned to** field to assign tasks to someone while you're creating a task list, we recommend that you avoid assigning tasks during task list creation.</span></span> <span data-ttu-id="2defb-128">Вместо этого назначьте задачи после создания экземпляра списка для отдельных магазинов.</span><span class="sxs-lookup"><span data-stu-id="2defb-128">Instead, assign the tasks after the list is instantiated for individual stores.</span></span>

## <a name="use-task-links-to-help-improve-worker-productivity"></a><span data-ttu-id="2defb-129">Ссылки на задачи позволяют повысить производительность работника</span><span class="sxs-lookup"><span data-stu-id="2defb-129">Use task links to help improve worker productivity</span></span>

<span data-ttu-id="2defb-130">Commerce позволяет связывать задачи с отдельными операциями POS, такими как запуск отчета о продажах, просмотр интерактивного учебного видео для ознакомительного обучения нового сотрудника или выполнение операции бэк-офис.</span><span class="sxs-lookup"><span data-stu-id="2defb-130">Commerce lets you link tasks to specific POS operations, such as running a sales report, viewing an online training video for new employee orientation, or performing a back-office operation.</span></span> <span data-ttu-id="2defb-131">Эта функция помогает владельцам задач получить сведения, необходимые для эффективного выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="2defb-131">This feature helps task owners get the information that they need to complete a task efficiently.</span></span>

<span data-ttu-id="2defb-132">Чтобы добавить ссылки на задачу во время создания задачи, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2defb-132">To add task links while you create a task, follow these steps.</span></span>

1. <span data-ttu-id="2defb-133">На экспресс-вкладке **Задачи** существующего списка задач выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="2defb-133">On the **Tasks** FastTab of an existing task list, select **Edit**.</span></span>
1. <span data-ttu-id="2defb-134">В диалоговом окне **Изменить задачу** в поле **Ссылка на задачу** выберите один или несколько из следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="2defb-134">In the **Edit task** dialog box, in the **Task link** field, select one or more of the following options:</span></span>

    - <span data-ttu-id="2defb-135">Выберите **пункт меню**, чтобы настроить операции бэк-офис, например, "Комплекты продуктов".</span><span class="sxs-lookup"><span data-stu-id="2defb-135">Select **Menu item** to configure a back-office operation, such as "Product kits."</span></span>
    - <span data-ttu-id="2defb-136">Выберите **Операции POS** для настройки операций POS, например "отчеты о продажах".</span><span class="sxs-lookup"><span data-stu-id="2defb-136">Select **POS Operation** to configure a POS operation, such as "Sales reports."</span></span>
    - <span data-ttu-id="2defb-137">Выберите **URL-адрес** для настройки абсолютного URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="2defb-137">Select **URL** to configure an absolute URL.</span></span>

<span data-ttu-id="2defb-138">На следующем рисунке показан выбор ссылки на задачу в диалоговом окне **Изменить задачу**.</span><span class="sxs-lookup"><span data-stu-id="2defb-138">The following illustration shows the selection of task links in the **Edit task** dialog box.</span></span>

![Выбор ссылки на задачу в диалоговом окне «Изменить задачу»](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a><span data-ttu-id="2defb-140">Настройка операции POS, чтобы она могла быть связана с задачей</span><span class="sxs-lookup"><span data-stu-id="2defb-140">Configure a POS operation so that it can be linked to a task</span></span>

<span data-ttu-id="2defb-141">Чтобы настроить операцию POS, чтобы она могла быть связана с задачей, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2defb-141">To configure a POS operation so that it can be linked to a task, follow these steps.</span></span>

1. <span data-ttu-id="2defb-142">Перейдите к **Retail и Commerce \> Настройка канала \> Настройка POS \> POS \> Операции POS**.</span><span class="sxs-lookup"><span data-stu-id="2defb-142">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="2defb-143">Выберите **Правка**, найдите операцию POS и затем установите флажок **Включить управление задачами** для этого.</span><span class="sxs-lookup"><span data-stu-id="2defb-143">Select **Edit**, find the POS operation, and then select the **Enable Task Management** check box for it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2defb-144">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2defb-144">Additional resources</span></span>

[<span data-ttu-id="2defb-145">Обзор управления задачами</span><span class="sxs-lookup"><span data-stu-id="2defb-145">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="2defb-146">Настройка управления задачами</span><span class="sxs-lookup"><span data-stu-id="2defb-146">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="2defb-147">Назначение списков задач магазинам или сотрудникам</span><span class="sxs-lookup"><span data-stu-id="2defb-147">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="2defb-148">Управление задачами в POS</span><span class="sxs-lookup"><span data-stu-id="2defb-148">Task management in POS</span></span>](task-mgmt-POS.md)
