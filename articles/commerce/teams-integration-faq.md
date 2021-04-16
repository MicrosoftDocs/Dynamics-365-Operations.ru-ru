---
title: Вопросы и ответы по интеграции Dynamics 365 Commerce и Microsoft Teams
description: В этом разделе содержатся ответы на часто задаваемые вопросы по интеграции Microsoft Dynamics 365 Commerce и Microsoft Teams.
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
ms.openlocfilehash: 26e1dc53126c0615332457aa785415c4c7112bbd
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842735"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a><span data-ttu-id="bd54c-103">Вопросы и ответы по интеграции Dynamics 365 Commerce и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="bd54c-103">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="bd54c-104">В этом разделе содержатся ответы на часто задаваемые вопросы по интеграции Microsoft Dynamics 365 Commerce и Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="bd54c-104">This topic provides answers to frequently asked questions regarding Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a><span data-ttu-id="bd54c-105">Кто в магазине становится владельцем рабочей группы при подготовке Teams из Commerce?</span><span class="sxs-lookup"><span data-stu-id="bd54c-105">Who in the store becomes an owner of a team while provisioning Teams from Commerce?</span></span> 

<span data-ttu-id="bd54c-106">Все менеджеры магазинов автоматически добавляются в качестве владельцев в соответствующую группу Teams, чтобы они могли выполнять такие операции, как добавление личного канала и добавление или удаление участников.</span><span class="sxs-lookup"><span data-stu-id="bd54c-106">All store managers are automatically added as owners to the corresponding team group so that they can perform operations such as adding a private channel and adding or deleting members.</span></span> 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a><span data-ttu-id="bd54c-107">Как назначить роль "Менеджер взаимодействия" сотруднику в модуле Commerce Headquarters?</span><span class="sxs-lookup"><span data-stu-id="bd54c-107">How do I assign the "communications manager" role to an employee in Commerce headquarters?</span></span> 

<span data-ttu-id="bd54c-108">Менеджеры взаимодействия в Microsoft Teams имеют возможность создавать и публиковать списки задач.</span><span class="sxs-lookup"><span data-stu-id="bd54c-108">Communication managers in Microsoft Teams have the ability to create and publish task lists.</span></span> <span data-ttu-id="bd54c-109">Сотрудникам организации, которым необходимо стать менеджерам взаимодействия, необходима роль "менеджер задач розничной торговли", назначенная им в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="bd54c-109">Organization employees who need to become communication managers must have the "retail task manager" role assigned to them in Commerce headquarters.</span></span>

<span data-ttu-id="bd54c-110">Чтобы назначить роль менеджера задач розничной торговли для сотрудника в Commerce Headquarters, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="bd54c-110">To assign the retail task manager role to an employee in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="bd54c-111">Перейдите в раздел **Retail и Commerce \> Сотрудники \> Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="bd54c-111">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="bd54c-112">Выберите сотрудника.</span><span class="sxs-lookup"><span data-stu-id="bd54c-112">Select an employee.</span></span>
1. <span data-ttu-id="bd54c-113">На экспресс-вкладке **Роли пользователя** выберите **Назначить роли**.</span><span class="sxs-lookup"><span data-stu-id="bd54c-113">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="bd54c-114">В диалоговом окне **Назначение ролей пользователю** выберите роль **Руководителя задачи Retail** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="bd54c-114">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a><span data-ttu-id="bd54c-115">Как сделать конкретную организационную иерархию доступной для отправки в Microsoft Teams?</span><span class="sxs-lookup"><span data-stu-id="bd54c-115">How do I make a specific organization hierarchy available to upload into Microsoft Teams?</span></span>

<span data-ttu-id="bd54c-116">В Commerce Headquarters иерархия каждой организации связана с одной или несколькими целями.</span><span class="sxs-lookup"><span data-stu-id="bd54c-116">In Commerce headquarters, every organization's hierarchy is associated with one or more purposes.</span></span> <span data-ttu-id="bd54c-117">Убедитесь, что иерархия, которую вы хотите подготовить в Microsoft Teams, имеет связанную с ней цель **Отчетность розничной торговли**, как показано в следующем примере изображения.</span><span class="sxs-lookup"><span data-stu-id="bd54c-117">Make sure the hierarchy that you want to provision into Microsoft Teams has the **Retail reporting** purpose associated with it, as shown in the following example image.</span></span> 

![Пример цели организационной иерархии в Commerce Headquarters](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a><span data-ttu-id="bd54c-119">Как разрешить работникам розничного магазина входить в Commerce POS, используя Azure Active Directory (Azure AD)?</span><span class="sxs-lookup"><span data-stu-id="bd54c-119">How do I enable retail store workers to sign in to Commerce point of sale (POS) using Azure Active Directory (Azure AD)?</span></span>

<span data-ttu-id="bd54c-120">Сведения о настройке использования проверки подлинности Azure AD в Commerce POS см. в разделе [Включение проверки подлинности Azure Active Directory для входа в POS-терминал](aad-pos-logon.md).</span><span class="sxs-lookup"><span data-stu-id="bd54c-120">For information about how to configure the Commerce POS sign-in experience to use Azure AD authentication, see [Enable Azure Active Directory authentication for POS sign-in](aad-pos-logon.md).</span></span>

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a><span data-ttu-id="bd54c-121">Как сопоставить магазины и соответствующие рабочие группы в Commerce Headquarters, если в организации уже созданы рабочие группы в Microsoft Teams?</span><span class="sxs-lookup"><span data-stu-id="bd54c-121">How do I map stores and corresponding teams in Commerce headquarters if my organization has already created teams in Microsoft Teams?</span></span>

<span data-ttu-id="bd54c-122">Сведения о сопоставлении магазинов и рабочих групп при наличии готовых групп см. в разделе [Сопоставление магазинов и соответствующих рабочих групп, если в организации имеются готовые рабочие группы в Microsoft Teams](map-stores-existing-teams.md).</span><span class="sxs-lookup"><span data-stu-id="bd54c-122">For information on how to map stores and teams if there are pre-existing teams, see [Map stores and corresponding teams if your organization has pre-existing teams in Microsoft Teams](map-stores-existing-teams.md).</span></span>

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a><span data-ttu-id="bd54c-123">Как удалить токен API Microsoft Graph, хранящийся в хранилище сеанса?</span><span class="sxs-lookup"><span data-stu-id="bd54c-123">How do I clear the Microsoft Graph API token stored in the session storage?</span></span>

<span data-ttu-id="bd54c-124">Пользователь, вошедший в POS-терминал с учетной записью Azure Active Directory (Azure AD), должен выйти из POS-терминала или закрыть приложение, чтобы стереть хранилище сеанса.</span><span class="sxs-lookup"><span data-stu-id="bd54c-124">A user who has signed in to the point of sale (POS) with an Azure Active Directory (Azure AD) account should sign out from the POS or close the application to clear the session storage.</span></span> 

> [!TIP]
> <span data-ttu-id="bd54c-125">Рекомендуется, чтобы работники магазина всегда запирали POS-терминал или выходили из сеанса, когда они не используют терминал.</span><span class="sxs-lookup"><span data-stu-id="bd54c-125">A recommended best practice is to always have store workers lock the POS terminal or sign out from a session when not using the terminal.</span></span> 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a><span data-ttu-id="bd54c-126">Что произойдет, если у магазина нет менеджеров магазина?</span><span class="sxs-lookup"><span data-stu-id="bd54c-126">What happens if a store doesn't have store managers?</span></span>

<span data-ttu-id="bd54c-127">Если в магазине нет менеджеров, группа рабочей группы не будет создана для магазина или в Teams.</span><span class="sxs-lookup"><span data-stu-id="bd54c-127">If a store doesn't have managers, a team group will not be created for the store or in Teams.</span></span> 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a><span data-ttu-id="bd54c-128">Что произойдет, если менеджер магазина покидает компанию?</span><span class="sxs-lookup"><span data-stu-id="bd54c-128">What happens if a store manager leaves the company?</span></span>

<span data-ttu-id="bd54c-129">Любой пользователь, имеющий роль владельца, может добавить нового менеджера магазина в Commerce Headquarters и повторно подготовить Teams, чтобы новый менеджер имел необходимые привилегии в Teams для этой группы.</span><span class="sxs-lookup"><span data-stu-id="bd54c-129">Anyone with the owner role can add a new store manager in Commerce headquarters and reprovision Teams so that the new manager will have the necessary privileges in Teams for the group.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="bd54c-130">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bd54c-130">Additional resources</span></span>

[<span data-ttu-id="bd54c-131">Обзор интеграции Dynamics 365 Commerce и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="bd54c-131">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="bd54c-132">Включение интеграции Dynamics 365 Commerce и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="bd54c-132">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="bd54c-133">Подготовка Microsoft Teams из Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="bd54c-133">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="bd54c-134">Синхронизация управления задачами между Microsoft Teams и Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="bd54c-134">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="bd54c-135">Управление ролями пользователей в Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="bd54c-135">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="bd54c-136">Сопоставление магазинов и рабочих групп, если имеются готовые рабочие группы в Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="bd54c-136">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)
