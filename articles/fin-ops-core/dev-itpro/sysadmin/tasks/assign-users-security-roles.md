---
title: Назначение пользователей для ролей безопасности
description: Для получения доступа к приложениям Finance and Operations пользователи должны быть назначены ролям безопасности.
author: ChrisGarty
manager: AnnBe
ms.date: 11/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0744f45ac91dfb9b5aae35091e3675202c9144f9
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143569"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="7f21c-103">Назначение пользователей для ролей безопасности</span><span class="sxs-lookup"><span data-stu-id="7f21c-103">Assign users to security roles</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7f21c-104">Для использования каких-либо других возможностей, кроме общих, пользователям необходимо назначить роли безопасности.</span><span class="sxs-lookup"><span data-stu-id="7f21c-104">To use anything other than common capabilities, users must be assigned to security roles.</span></span> <span data-ttu-id="7f21c-105">В этой процедуре описывается, как системные администраторы могут автоматически назначить пользователей ролям на основе бизнес-данных.</span><span class="sxs-lookup"><span data-stu-id="7f21c-105">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="7f21c-106">Автоматическое назначение пользователей ролям</span><span class="sxs-lookup"><span data-stu-id="7f21c-106">Automatically assign users to roles</span></span>
1. <span data-ttu-id="7f21c-107">Перейдите в раздел **Область переходов > Модули > Администрирование системы > Безопасность > Назначить пользователей ролям**.</span><span class="sxs-lookup"><span data-stu-id="7f21c-107">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="7f21c-108">В этом дереве выберите роль "Супервизор по учету".</span><span class="sxs-lookup"><span data-stu-id="7f21c-108">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="7f21c-109">Выберите роль, для которой необходимо настроить правило.</span><span class="sxs-lookup"><span data-stu-id="7f21c-109">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="7f21c-110">В этом примере выберите роль "Супервизор по учету".</span><span class="sxs-lookup"><span data-stu-id="7f21c-110">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="7f21c-111">Щелкните **Добавить правило**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="7f21c-111">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="7f21c-112">В списке **Выбрать запрос** найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="7f21c-112">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="7f21c-113">Выберите запрос, который требуется использовать для этого правила.</span><span class="sxs-lookup"><span data-stu-id="7f21c-113">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="7f21c-114">В списке **Имя правила членства** перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="7f21c-114">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="7f21c-115">Щелкните **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="7f21c-115">Click **Edit query**.</span></span> <span data-ttu-id="7f21c-116">При необходимости измените запрос.</span><span class="sxs-lookup"><span data-stu-id="7f21c-116">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="7f21c-117">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="7f21c-117">Click **OK**.</span></span>
8. <span data-ttu-id="7f21c-118">Нажмите **Выполнить автоматическое назначение роли**.</span><span class="sxs-lookup"><span data-stu-id="7f21c-118">Click **Run automatic role assignment**.</span></span>
9. <span data-ttu-id="7f21c-119">Перейдите **Область перехода > Модули > Администрирование системы > Пользователи > Пользователи** (в идеале на отдельной вкладке браузера).</span><span class="sxs-lookup"><span data-stu-id="7f21c-119">Go to **Navigation pane > Modules > System administration > Users > Users** (ideally in a separate browser tab).</span></span>
10. <span data-ttu-id="7f21c-120">Просмотрите роли, назначенные различным пользователям, чтобы подтвердить правильность запроса на назначение ролей.</span><span class="sxs-lookup"><span data-stu-id="7f21c-120">Review the roles assigned to various users to confirm that the role assignment query was correct.</span></span> <span data-ttu-id="7f21c-121">Скорректируйте и повторно запустите, если необходимо.</span><span class="sxs-lookup"><span data-stu-id="7f21c-121">Adjust and re-run if needed.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="7f21c-122">Исключение пользователей из автоматического назначения ролей</span><span class="sxs-lookup"><span data-stu-id="7f21c-122">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="7f21c-123">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="7f21c-123">Close the page.</span></span>
2. <span data-ttu-id="7f21c-124">Перейдите в раздел **Область переходов > Модули > Администрирование системы > Безопасность > Назначить пользователей ролям**.</span><span class="sxs-lookup"><span data-stu-id="7f21c-124">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="7f21c-125">В этом дереве выберите роль "Супервизор по учету".</span><span class="sxs-lookup"><span data-stu-id="7f21c-125">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="7f21c-126">Выбор роли.</span><span class="sxs-lookup"><span data-stu-id="7f21c-126">Select a role.</span></span> <span data-ttu-id="7f21c-127">В этом примере выберите роль "Супервизор по учету".</span><span class="sxs-lookup"><span data-stu-id="7f21c-127">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="7f21c-128">В меню **Пользователи, назначенные ролям** выберите **Назначить / исключить пользователей вручную**.</span><span class="sxs-lookup"><span data-stu-id="7f21c-128">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="7f21c-129">В списке **Назначить пользователей роли или исключить их из нее** отмерьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="7f21c-129">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="7f21c-130">Выберите пользователя.</span><span class="sxs-lookup"><span data-stu-id="7f21c-130">Select a user.</span></span>  
6. <span data-ttu-id="7f21c-131">В область **Панель операций** выберите **Исключить из роли**.</span><span class="sxs-lookup"><span data-stu-id="7f21c-131">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="7f21c-132">Щелкните **Исключить из роли**, чтобы исключить выбранных пользователей из роли.</span><span class="sxs-lookup"><span data-stu-id="7f21c-132">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="7f21c-133">Чтобы удалить исключения, выберите пользователей, для которых требуется удалить исключения, а затем щелкните **Сброс статуса**.</span><span class="sxs-lookup"><span data-stu-id="7f21c-133">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="7f21c-134">При удалении исключения путем сброса статуса пользователя роль пользователя назначается снова автоматически.</span><span class="sxs-lookup"><span data-stu-id="7f21c-134">When you remove an exclusion by resetting the user's status, the user's role is again assigned automatically.</span></span> <span data-ttu-id="7f21c-135">Однако пользователь не сразу назначается роли и не исключается из роли при сбросе статуса.</span><span class="sxs-lookup"><span data-stu-id="7f21c-135">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="7f21c-136">Вместо этого пользователь либо назначается роли, либо удаляется из роли при следующем выполнении правил для автоматического назначения ролей.</span><span class="sxs-lookup"><span data-stu-id="7f21c-136">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
