---
title: Создание новых пользователей
description: Пользователи — это сотрудники внутри вашей организации либо внешние клиенты или поставщики, которым требуется доступ к системе для выполнения своей работы.
author: maertenm
manager: AnnBe
ms.date: 06/08/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d126b449074663772549b96b86acb53db971a5d4
ms.sourcegitcommit: 7d943499f302298c6ff127f56cecc34af6cee289
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "3435592"
---
# <a name="create-new-users"></a><span data-ttu-id="8dd90-103">Создание новых пользователей</span><span class="sxs-lookup"><span data-stu-id="8dd90-103">Create new users</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8dd90-104">Пользователи — это сотрудники внутри вашей организации либо внешние клиенты или поставщики, которым требуется доступ к системе для выполнения своей работы.</span><span class="sxs-lookup"><span data-stu-id="8dd90-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="8dd90-105">Связывание пользователя с лицензией (только новые типы лицензий)</span><span class="sxs-lookup"><span data-stu-id="8dd90-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="8dd90-106">Для клиентов, для которых используется один из новых типов лицензий, которые были добавлены в октябре 2019 года, пользователи должны быть связаны с лицензией.</span><span class="sxs-lookup"><span data-stu-id="8dd90-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="8dd90-107">Пользователи, связанные с лицензией, автоматически добавляются в качестве системных пользователей, не имеющих ролей при первом входе в систему.</span><span class="sxs-lookup"><span data-stu-id="8dd90-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span>

<span data-ttu-id="8dd90-108">Администраторы системы могут [назначать лицензии пользователям](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) из [центра администрирования Microsoft 365](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="8dd90-108">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a><span data-ttu-id="8dd90-109">Связывание внешнего пользователя с лицензией (только новые типы лицензий)</span><span class="sxs-lookup"><span data-stu-id="8dd90-109">Associate an external user with a license (new license types only)</span></span>
<span data-ttu-id="8dd90-110">Пользователи, внешние по отношению к клиенту, для которого была выполнено развертывание среды, должны быть представлены в каталоге клиента узла (Azure Active Directory (Azure AD)), чтобы им можно было назначить лицензии.</span><span class="sxs-lookup"><span data-stu-id="8dd90-110">Users external to the tenant that the environment was deployed into need to be represented in the host tenant directory (Azure Active Directory (Azure AD)) so that they can be assigned licenses.</span></span> <span data-ttu-id="8dd90-111">Эти внешние пользователи должны быть добавлены к клиенту в Azure AD в качестве гостевых пользователей, а затем им назначаются соответствующие лицензии.</span><span class="sxs-lookup"><span data-stu-id="8dd90-111">Those external users should be added to the tenant in Azure AD as guest users and then assigned the appropriate licenses.</span></span> <span data-ttu-id="8dd90-112">Дополнительные сведения см. в разделе [Добавление пользователей сотрудничества Azure Active Directory B2B на портале Azure](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span><span class="sxs-lookup"><span data-stu-id="8dd90-112">For more information, see [Add Azure Active Directory B2B collaboration users in the Azure portal](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="8dd90-113">Добавление нового пользователя</span><span class="sxs-lookup"><span data-stu-id="8dd90-113">Add a new user</span></span>
1. <span data-ttu-id="8dd90-114">Перейдите в раздел **Администрирование системы \> Пользователи \> Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="8dd90-114">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="8dd90-115">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="8dd90-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="8dd90-116">В поле **Код пользователя** введите уникальный код для пользователя.</span><span class="sxs-lookup"><span data-stu-id="8dd90-116">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="8dd90-117">Код пользователя — обязательное поле.</span><span class="sxs-lookup"><span data-stu-id="8dd90-117">A user ID is required.</span></span>  
4. <span data-ttu-id="8dd90-118">В поле **Имя пользователя** введите имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="8dd90-118">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="8dd90-119">В поле **Домен** введите домен пользователя.</span><span class="sxs-lookup"><span data-stu-id="8dd90-119">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="8dd90-120">В поле **Псевдоним** введите псевдоним пользователя.</span><span class="sxs-lookup"><span data-stu-id="8dd90-120">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="8dd90-121">В поле **Компания** выберите требуемую компанию.</span><span class="sxs-lookup"><span data-stu-id="8dd90-121">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="8dd90-122">На экспресс-вкладке **Роли пользователя** выберите **Назначить роли**, чтобы назначить пользователям роли безопасности.</span><span class="sxs-lookup"><span data-stu-id="8dd90-122">On the **User's roles** FastTab, select **Assign roles** to assign users to security roles.</span></span> <span data-ttu-id="8dd90-123">Дополнительные сведения см. в разделе [Назначение пользователей для ролей безопасности](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="8dd90-123">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span>
9. <span data-ttu-id="8dd90-124">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="8dd90-124">Select **OK**.</span></span>
10. <span data-ttu-id="8dd90-125">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="8dd90-125">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="8dd90-126">Импорт пользователей</span><span class="sxs-lookup"><span data-stu-id="8dd90-126">Import users</span></span>
1. <span data-ttu-id="8dd90-127">Перейдите в раздел **Администрирование системы \> Пользователи \> Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="8dd90-127">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="8dd90-128">На панели операций выберите **Импорт пользователей**.</span><span class="sxs-lookup"><span data-stu-id="8dd90-128">On the Action Pane, select **Import users**.</span></span>
3. <span data-ttu-id="8dd90-129">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="8dd90-129">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="8dd90-130">Выберите **Импорт пользователей**.</span><span class="sxs-lookup"><span data-stu-id="8dd90-130">Select **Import users**.</span></span>
5. <span data-ttu-id="8dd90-131">Выберите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="8dd90-131">Select **Close**.</span></span>

