---
title: Создание новых пользователей
description: Пользователи — это сотрудники внутри вашей организации либо внешние клиенты или поставщики, которым требуется доступ к системе для выполнения своей работы.
author: maertenm
manager: AnnBe
ms.date: 10/08/2019
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
ms.openlocfilehash: 3c347a34a389c32d005cc8086c4a1349ecb8a698
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570529"
---
# <a name="create-new-users"></a><span data-ttu-id="f00cd-103">Создание новых пользователей</span><span class="sxs-lookup"><span data-stu-id="f00cd-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f00cd-104">Пользователи — это сотрудники внутри вашей организации либо внешние клиенты или поставщики, которым требуется доступ к системе для выполнения своей работы.</span><span class="sxs-lookup"><span data-stu-id="f00cd-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="f00cd-105">Связывание пользователя с лицензией (только новые типы лицензий)</span><span class="sxs-lookup"><span data-stu-id="f00cd-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="f00cd-106">Для клиентов, для которых используется один из новых типов лицензий, которые были добавлены в октябре 2019 года, пользователи должны быть связаны с лицензией.</span><span class="sxs-lookup"><span data-stu-id="f00cd-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="f00cd-107">Пользователи, связанные с лицензией, автоматически добавляются в качестве системных пользователей, не имеющих ролей при первом входе в систему.</span><span class="sxs-lookup"><span data-stu-id="f00cd-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span> <span data-ttu-id="f00cd-108">Пользователи, не связанные с лицензией, получают предупреждающее сообщение.</span><span class="sxs-lookup"><span data-stu-id="f00cd-108">Users who aren't associated with a licence receive a warning message.</span></span>

<span data-ttu-id="f00cd-109">Администраторы системы могут [назначать лицензии пользователям](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) из [центра администрирования Microsoft 365](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="f00cd-109">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="f00cd-110">Добавление нового пользователя</span><span class="sxs-lookup"><span data-stu-id="f00cd-110">Add a new user</span></span>
1. <span data-ttu-id="f00cd-111">Перейдите в раздел **Администрирование системы \> Пользователи \> Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="f00cd-111">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="f00cd-112">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="f00cd-112">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="f00cd-113">В поле **Код пользователя** введите уникальный код для пользователя.</span><span class="sxs-lookup"><span data-stu-id="f00cd-113">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="f00cd-114">Код пользователя — обязательное поле.</span><span class="sxs-lookup"><span data-stu-id="f00cd-114">A user ID is required.</span></span>  
4. <span data-ttu-id="f00cd-115">В поле **Имя пользователя** введите имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="f00cd-115">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="f00cd-116">В поле **Домен** введите домен пользователя.</span><span class="sxs-lookup"><span data-stu-id="f00cd-116">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="f00cd-117">В поле **Псевдоним** введите псевдоним пользователя.</span><span class="sxs-lookup"><span data-stu-id="f00cd-117">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="f00cd-118">В поле **Компания** выберите требуемую компанию.</span><span class="sxs-lookup"><span data-stu-id="f00cd-118">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="f00cd-119">На экспресс-вкладке **Роли пользователя** выберите **Назначить роли**, чтобы [назначить пользователям роли безопасности](assign-users-security-roles.md)</span><span class="sxs-lookup"><span data-stu-id="f00cd-119">On the **User's roles** FastTab, select **Assign roles** to [assign users to security roles](assign-users-security-roles.md)</span></span>
9. <span data-ttu-id="f00cd-120">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f00cd-120">Select **OK**.</span></span>
10. <span data-ttu-id="f00cd-121">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="f00cd-121">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="f00cd-122">Импорт пользователей</span><span class="sxs-lookup"><span data-stu-id="f00cd-122">Import users</span></span>
1. <span data-ttu-id="f00cd-123">На панели операций выберите **Импорт пользователей**.</span><span class="sxs-lookup"><span data-stu-id="f00cd-123">On the Action Pane, select **Import users**.</span></span>
2. <span data-ttu-id="f00cd-124">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="f00cd-124">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="f00cd-125">Выберите **Импорт пользователей**.</span><span class="sxs-lookup"><span data-stu-id="f00cd-125">Select **Import users**.</span></span>
4. <span data-ttu-id="f00cd-126">Выберите **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="f00cd-126">Select **Close**.</span></span>

