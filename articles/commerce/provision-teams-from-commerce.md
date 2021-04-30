---
title: Подготовка Microsoft Teams из Dynamics 365 Commerce
description: В этой теме описывается, как выполнить подготовку Microsoft Teams, используя организационные данные из Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ba7c74942735b723d1015dc4da0068fbb631bc6b
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908912"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a><span data-ttu-id="1cb1d-103">Подготовка Microsoft Teams из Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="1cb1d-103">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1cb1d-104">В этой теме описывается, как выполнить подготовку Microsoft Teams, используя организационные данные из Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-104">This topic describes how to provision Microsoft Teams by using organizational data from Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1cb1d-105">Dynamics 365 Commerce предлагает простой способ подготовки Teams, если вы еще не настроили Teams для магазинов розничной торговли там.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-105">Dynamics 365 Commerce offers an easy way to provision Teams if you haven't yet set up teams for your retail stores there.</span></span> <span data-ttu-id="1cb1d-106">Используя хорошо определенную информацию из Commerce, которую вы хотите использовать в Teams, вы можете помочь сотрудникам магазина начать работу в Teams.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-106">By taking advantage of well-defined information from Commerce that you want to use in Teams, you can help your store employees get started in Teams.</span></span> <span data-ttu-id="1cb1d-107">Эти сведения включают организационную иерархию, названия магазинов, сведения о сотрудниках и учетные записи Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="1cb1d-107">This information includes the organizational hierarchy, store names, employee information, and Azure Active Directory (Azure AD) accounts.</span></span> 

<span data-ttu-id="1cb1d-108">Процесс подготовки Teams включает в себя два основных этапа:</span><span class="sxs-lookup"><span data-stu-id="1cb1d-108">The process of provisioning Teams has two main steps:</span></span>

1. <span data-ttu-id="1cb1d-109">В Teams создайте группу для каждого розничного магазина и добавьте сотрудников магазина в качестве участников соответствующей группы.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-109">In Teams, create a team for each retail store, and add store workers as members of the appropriate team.</span></span> <span data-ttu-id="1cb1d-110">Если сотрудник связан более чем с одним розничным магазином, то этот факт будет отражен в участии в группах.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-110">If an employee is associated with more than one retail store, team membership will reflect that fact.</span></span> <span data-ttu-id="1cb1d-111">Группа взаимодействия, которая включает в себя региональных руководителей в качестве участников, будет создана, чтобы помочь публиковать задачи из Teams.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-111">A communications team that includes regional managers as members will be created to help publish tasks from Teams.</span></span>
1. <span data-ttu-id="1cb1d-112">Отправьте организационную иерархию из Commerce в Teams.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-112">Upload your organizational hierarchy from Commerce to Teams.</span></span>

## <a name="provision-teams-in-commerce-headquarters"></a><span data-ttu-id="1cb1d-113">Подготовка Teams в Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="1cb1d-113">Provision Teams in Commerce headquarters</span></span>

<span data-ttu-id="1cb1d-114">Прежде чем подготавливать Microsoft Teams, выполните следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="1cb1d-114">Before you provision Microsoft Teams, complete these tasks:</span></span>

- <span data-ttu-id="1cb1d-115">Убедитесь, что все региональные менеджеры были сделаны менеджерами по связи.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-115">Confirm that all regional managers have been made communications managers.</span></span>
- <span data-ttu-id="1cb1d-116">Убедитесь, что учетная запись Azure каждого менеджера и работника магазина связана с записью работника этого менеджера или работника в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-116">Confirm that the Azure account of every store manager and worker has been associated with that manager's or worker's worker record in Commerce headquarters.</span></span>

<span data-ttu-id="1cb1d-117">Чтобы подготовить Teams в Commerce Headquarters, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-117">To provision Teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="1cb1d-118">Выберите **Retail и Commerce \> Настройка канала \> Конфигурация интеграции Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-118">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="1cb1d-119">На панели операций выберите **Подготовка Teams**.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-119">On the Action Pane, select **Provision teams**.</span></span> <span data-ttu-id="1cb1d-120">Создается пакетное задание с именем **Подготовка Teams**.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-120">A batch job that is named **Teams provision** is created.</span></span>
1. <span data-ttu-id="1cb1d-121">Перейдите в раздел **Администрирование системы \> Запросы \> Пакетные задания** и найдите самое последнее задание, которое имеет описание **Подготовка Teams**.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-121">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="1cb1d-122">Дождитесь завершения выполнения этого задания.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-122">Wait until this job has finished running.</span></span>

> [!TIP]
> <span data-ttu-id="1cb1d-123">Если ни один из региональных руководителей, менеджеров магазинов и сотрудников магазина не связаны с лицензией на Teams, возможно появление следующего сообщения об ошибке: "Не удалось получить применимые категории SKU для пользователя".</span><span class="sxs-lookup"><span data-stu-id="1cb1d-123">If none of your regional managers, store managers, and store workers have been associated with a Teams license, you might receive the following error message: "Failed to retrieve appliable Sku categories for the user."</span></span> <span data-ttu-id="1cb1d-124">Чтобы исправить эту ошибку, выберите **Синхронизировать группы и участников** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-124">To correct the issue, select **Sync teams and members** on the Action Pane.</span></span>

<!-- ![Dynamics 365 Commerce - Teams integration configuration](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a><span data-ttu-id="1cb1d-125">Проверка подготовки Teams в центре администрирования Teams</span><span class="sxs-lookup"><span data-stu-id="1cb1d-125">Validate Teams provisioning in the Teams admin center</span></span>

<span data-ttu-id="1cb1d-126">Чтобы проверить подготовку Microsoft Teams в центре администрирования Microsoft Teams, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-126">To validate Microsoft Teams provisioning in the Microsoft Teams admin center, follow these steps.</span></span>
    
1. <span data-ttu-id="1cb1d-127">Перейдите в [центр администрирования Teams](https://admin.teams.microsoft.com/) и войдите в систему как администратор вашего клиента электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-127">Go to the [Teams admin center](https://admin.teams.microsoft.com/), and sign in as the administrator of your e-commerce tenant.</span></span>
1. <span data-ttu-id="1cb1d-128">В левой области навигации выберите **Teams**, чтобы развернуть его, затем выберите **Управление группами**.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-128">In the left navigation pane, select **Teams** to expand it, and then select **Manage teams**.</span></span>
1. <span data-ttu-id="1cb1d-129">Убедитесь, что одна группа была создана для каждого розничного магазина Commerce.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-129">Confirm that one team has been created for each Commerce retail store.</span></span>
1. <span data-ttu-id="1cb1d-130">Выберите группу и подтвердите, что сотрудники магазина были добавлены в нее в качестве участников.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-130">Select a team, and confirm that store workers have been added to it as members.</span></span>
1. <span data-ttu-id="1cb1d-131">В левой области навигации выберите **Пользователи** и убедитесь, что все сотрудники магазина во всех магазинах были добавлены в качестве пользователей.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-131">In the left navigation pane, select **Users**, and confirm that all store employees in all stores have been added as users.</span></span>

<span data-ttu-id="1cb1d-132">На следующем рисунке показан пример страницы **Управление группами** в центре администрирования Teams.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-132">The following illustration shows an example of the **Manage teams** page in the Teams admin center.</span></span>

![Пример страницы управления группами в центре администрирования Teams](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a><span data-ttu-id="1cb1d-134">Отправка организационной иерархии Commerce в Teams</span><span class="sxs-lookup"><span data-stu-id="1cb1d-134">Upload a Commerce organizational hierarchy to Teams</span></span>
    
<span data-ttu-id="1cb1d-135">Организационную иерархию Commerce можно использовать в Microsoft Teams для публикации задач во всех или в выбранных магазинах, использующих одну и ту же структуру иерархии.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-135">The Commerce organizational hierarchy can be used in Microsoft Teams to publish tasks to all or selected stores that use the same hierarchy structure.</span></span>

<span data-ttu-id="1cb1d-136">Чтобы отправить организационную иерархию Commerce в Teams, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-136">To upload a Commerce organizational hierarchy to Teams, follow these steps.</span></span>
    
1. <span data-ttu-id="1cb1d-137">В Commerce Headquarter перейдите в раздел **Розничная торговля и коммерция \> Настройка канала \> Конфигурация интеграции Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-137">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="1cb1d-138">Выберите **Загрузить иерархию таргетирования**, затем выберите **Розничные магазины по регионам**, чтобы загрузить файл значений с разделителями-запятыми (CSV) организационной иерархии.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-138">Select **Download targeting hierarchy**, and then select **Retail Stores by Region** to download a comma-separated values (CSV) file of the organizational hierarchy.</span></span>
1. <span data-ttu-id="1cb1d-139">Установите модуль Microsoft Teams PowerShell, выполнив шаги, описанные в разделе [Установка Microsoft Teams PowerShell](https://docs.microsoft.com/microsoftteams/teams-powershell-install).</span><span class="sxs-lookup"><span data-stu-id="1cb1d-139">Install the Microsoft Teams PowerShell module by following the steps in [Install Microsoft Teams PowerShell](https://docs.microsoft.com/microsoftteams/teams-powershell-install).</span></span>
1. <span data-ttu-id="1cb1d-140">При появлении запроса в окне Teams PowerShell выполните вход с учетной записью администратора для своего клиента Azure AD.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-140">When you're prompted in the Teams PowerShell window, sign in by using the administrator account for your Azure AD tenant.</span></span>
1. <span data-ttu-id="1cb1d-141">Следуйте шагам в разделе [Настройка иерархии таргетирования рабочей группы](https://docs.microsoft.com/microsoftteams/set-up-your-team-hierarchy) для отправки CSV-файла для иерархии таргетирования.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-141">Follow the steps in [Set up your team targeting hierarchy](https://docs.microsoft.com/microsoftteams/set-up-your-team-hierarchy) to upload the CSV file for the targeting hierarchy.</span></span>

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a><span data-ttu-id="1cb1d-142">Проверка, что организационная иерархия была отправлена в Teams</span><span class="sxs-lookup"><span data-stu-id="1cb1d-142">Verify that the organizational hierarchy was uploaded to Teams</span></span>

<span data-ttu-id="1cb1d-143">Чтобы проверить, что организационная иерархия была отправлена в Microsoft Teams, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-143">To verify that the organizational hierarchy was uploaded to Microsoft Teams, follow these steps.</span></span>

1. <span data-ttu-id="1cb1d-144">Выполните вход в Teams в качестве менеджера по связям.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-144">Sign in to Teams as a communications manager.</span></span>
1. <span data-ttu-id="1cb1d-145">В левой области навигации выберите **Задачи по планировщику**.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-145">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="1cb1d-146">На вкладке **Опубликованные списки** создайте новый список, содержащий фиктивную задачу.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-146">On the **Published lists** tab, create a new list that has a dummy task.</span></span>
1. <span data-ttu-id="1cb1d-147">Выберите **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-147">Select **Publish**.</span></span> <span data-ttu-id="1cb1d-148">Организационная иерархия должна появиться в диалоговом окне **Выберите, для кого предназначена публикация**, как показано в примере на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="1cb1d-148">The organizational hierarchy should appear in the **Select who to publish to** dialog box, as shown in the example in the following illustration.</span></span>

![Пример организационной иерархии в диалоговом окне "Выберите, для кого предназначена публикация"](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a><span data-ttu-id="1cb1d-150">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1cb1d-150">Additional resources</span></span>

[<span data-ttu-id="1cb1d-151">Обзор интеграции Dynamics 365 Commerce и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="1cb1d-151">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="1cb1d-152">Включение интеграции Dynamics 365 Commerce и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="1cb1d-152">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="1cb1d-153">Синхронизация управления задачами между Microsoft Teams и Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="1cb1d-153">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="1cb1d-154">Управление ролями пользователей в Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="1cb1d-154">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="1cb1d-155">Сопоставление магазинов и рабочих групп, если имеются готовые рабочие группы в Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="1cb1d-155">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="1cb1d-156">Вопросы и ответы по интеграции Dynamics 365 Commerce и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="1cb1d-156">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
