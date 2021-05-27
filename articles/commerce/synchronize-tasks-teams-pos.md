---
title: Синхронизация управления задачами между Microsoft Teams и Dynamics 365 Commerce POS
description: В этой теме описывается, как синхронизировать управление задачами между Microsoft Teams и POS-терминалом Dynamics 365 Commerce (POS).
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 74d53a850113c83979fba6baa4ff3c3e5d9ca02d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020635"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a><span data-ttu-id="b9ee2-103">Синхронизация управления задачами между Microsoft Teams и Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="b9ee2-103">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b9ee2-104">В этой теме описывается, как синхронизировать управление задачами между Microsoft Teams и POS-терминалом Dynamics 365 Commerce (POS).</span><span class="sxs-lookup"><span data-stu-id="b9ee2-104">This topic describes how to synchronize task management between Microsoft Teams and Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="b9ee2-105">Одной из основных целей интеграции с Teams является обеспечение синхронизации управления задачами между приложением POS и Teams.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-105">One of the main purposes of Teams integration is to enable the synchronization of task management between the POS application and Teams.</span></span> <span data-ttu-id="b9ee2-106">Таким образом сотрудники магазина могут использовать приложение POS или Teams для управления задачами, и им не требуется переключать приложения.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-106">In this way, store employees can use either the POS application or Teams to manage tasks, and don't have to switch applications.</span></span>

<span data-ttu-id="b9ee2-107">Поскольку планировщик используется в качестве репозитория для задач в Teams, должна быть связь между Teams и Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-107">Because Planner is used as a repository for tasks in Teams, there must be a link between Teams and Dynamics 365 Commerce.</span></span> <span data-ttu-id="b9ee2-108">Эта связь устанавливается с помощью определенного кода плана для заданной рабочей группы магазина.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-108">This link is established by using a specific plan ID for a given store team.</span></span>

<span data-ttu-id="b9ee2-109">В следующих процедурах показано, как настроить синхронизацию управления задачами между приложениями POS и Teams.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-109">The following procedures show how to set up task management synchronization between the POS and Teams applications.</span></span>

## <a name="publish-a-test-task-list-in-teams"></a><span data-ttu-id="b9ee2-110">Публикация тестового списка задач в Teams</span><span class="sxs-lookup"><span data-stu-id="b9ee2-110">Publish a test task list in Teams</span></span>

<span data-ttu-id="b9ee2-111">Следующая процедура предполагает, что рабочие группы магазинов используют интеграцию управления задачами Microsoft Teams с Commerce в первый раз.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-111">The following procedure assumes that your store teams are using Microsoft Teams task management integration with Commerce for the first time.</span></span>

<span data-ttu-id="b9ee2-112">Чтобы опубликовать тестовый список задач в Teams, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-112">To publish a test task list in Teams, follow these steps.</span></span>

1. <span data-ttu-id="b9ee2-113">Выполните вход в Teams в качестве менеджера по связям.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-113">Sign in to Teams as a communications manager.</span></span> <span data-ttu-id="b9ee2-114">Обычно менеджеры по связям являются пользователями, которые имеют роль **Региональный менеджер** в Commerce.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-114">Typically, communications managers are users who have the **Regional manager** role in Commerce.</span></span>
1. <span data-ttu-id="b9ee2-115">В левой области навигации выберите **Задачи по планировщику**.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-115">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="b9ee2-116">На вкладке **Опубликованные списки** выберите **Создать список** в левом нижнем углу и присвойте новому списку имя **Тестовый список задач**.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-116">On the **Published lists** tab, select **New list** in the lower left, and name the new list **Test task list**.</span></span>
1. <span data-ttu-id="b9ee2-117">Выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-117">Select **Create**.</span></span> <span data-ttu-id="b9ee2-118">Новый список отобразится в разделе **Черновики**.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-118">The new list appears under **Drafts**.</span></span>
1. <span data-ttu-id="b9ee2-119">В разделе **Название задачи** присвойте первой задаче название **Тестирование интеграции Teams**.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-119">Under **Task title**, give the first task the title **Testing Teams integration**.</span></span> <span data-ttu-id="b9ee2-120">Затем выберите **ВВОД**.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-120">Then select **Enter**.</span></span>
1. <span data-ttu-id="b9ee2-121">В списке **Черновики** выберите список задач.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-121">In the **Drafts** list, select the task list.</span></span> <span data-ttu-id="b9ee2-122">Затем выберите  **Опубликовать** в верхнем правом углу.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-122">Then select **Publish** in the upper-right corner.</span></span>
1. <span data-ttu-id="b9ee2-123">В диалоговом окне **Выберите, для кого предназначена публикация** выберите рабочие группы, которые должны получить тестовый список задач.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-123">In the **Select who to publish to** dialog box, select the teams that should receive the test task list.</span></span>
1. <span data-ttu-id="b9ee2-124">Выберите **Далее**, чтобы просмотреть план публикации.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-124">Select **Next** to review your publication plan.</span></span> <span data-ttu-id="b9ee2-125">Если необходимо внести изменения, выберите  **Назад**.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-125">If you must make changes, select **Back**.</span></span> 
1. <span data-ttu-id="b9ee2-126">Выберите **Подтвердите для продолжения**, затем выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-126">Select **Confirm to proceed**, and then select **Publish**.</span></span>
1. <span data-ttu-id="b9ee2-127">После завершения публикации сообщение в верхней части вкладки **Опубликованные списки** показывает, был ли список задач доставлен успешно.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-127">After publishing is completed, a message at the top of the **Published lists** tab indicates whether your task list was successfully delivered.</span></span>

<span data-ttu-id="b9ee2-128">Дополнительные сведения см. в разделе [Публикация списков задач для создания и отслеживания работы в организации](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).</span><span class="sxs-lookup"><span data-stu-id="b9ee2-128">For more information, see [Publish task lists to create and track work in your organization](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).</span></span>

## <a name="link-pos-and-teams-for-task-management"></a><span data-ttu-id="b9ee2-129">Связь POS и Teams для управления задачами</span><span class="sxs-lookup"><span data-stu-id="b9ee2-129">Link POS and Teams for task management</span></span>

<span data-ttu-id="b9ee2-130">Чтобы связать POS-терминалы и приложения Microsoft Teams для управления задачами в Commerce Headquarters, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-130">To link the POS and Microsoft Teams applications for task management in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="b9ee2-131">Перейдите в раздел **Retail и Commerce \> Управление задачами \> Интеграция задач с Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-131">Go to **Retail and Commerce \> Task management \> Tasks integration with Microsoft Teams**.</span></span>
1. <span data-ttu-id="b9ee2-132">На панели операций выберите **Правка**.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-132">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="b9ee2-133">Установите для параметра **Включить интеграцию управления задачами** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-133">Set the **Enable Task Management Integration** option to **Yes**.</span></span>
1. <span data-ttu-id="b9ee2-134">На панели операций выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-134">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="b9ee2-135">В панели операций выберите **Настройка управления задачами**.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-135">On the Action Pane, select **Setup task management**.</span></span> <span data-ttu-id="b9ee2-136">Вы должны получить уведомление о том, что создается пакетное задание с именем **Подготовка Teams**.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-136">You should receive a notification that indicates that a batch job that is named **Teams provision** is being created.</span></span>
1. <span data-ttu-id="b9ee2-137">Перейдите в раздел **Администрирование системы \> Запросы \> Пакетные задания** и найдите самое последнее задание, которое имеет описание **Подготовка Teams**.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-137">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="b9ee2-138">Дождитесь завершения выполнения этого задания.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-138">Wait until this job has finished running.</span></span>
1. <span data-ttu-id="b9ee2-139">Выполните **Задание CDX 1070**, чтобы опубликовать ИД плана и сохранить ссылки на сервере Retail Server.</span><span class="sxs-lookup"><span data-stu-id="b9ee2-139">Run the **CDX job 1070** to publish the plan ID and store references to Retail Server.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b9ee2-140">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b9ee2-140">Additional resources</span></span>

[<span data-ttu-id="b9ee2-141">Обзор интеграции Dynamics 365 Commerce и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b9ee2-141">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="b9ee2-142">Включение интеграции Dynamics 365 Commerce и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b9ee2-142">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="b9ee2-143">Подготовка Microsoft Teams из Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b9ee2-143">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="b9ee2-144">Управление ролями пользователей в Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b9ee2-144">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="b9ee2-145">Сопоставление магазинов и рабочих групп, если имеются готовые рабочие группы в Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b9ee2-145">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="b9ee2-146">Вопросы и ответы по интеграции Dynamics 365 Commerce и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b9ee2-146">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
