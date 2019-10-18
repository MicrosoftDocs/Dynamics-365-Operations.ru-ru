---
title: Назначение пользователей для ролей безопасности
description: Для доступа к приложениям Finance and Operations пользователи должны быть назначены ролям безопасности.
author: ChrisGarty
manager: AnnBe
ms.date: 09/16/2019
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
ms.openlocfilehash: a4daecc1acd589cd1656402244e5325382a407e7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180975"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="1b419-103">Назначение пользователей для ролей безопасности</span><span class="sxs-lookup"><span data-stu-id="1b419-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1b419-104">Для использования каких-либо других возможностей, кроме общих, пользователям необходимо назначить роли безопасности.</span><span class="sxs-lookup"><span data-stu-id="1b419-104">To use anything other than common capabilities, users must be assigned to security roles.</span></span> <span data-ttu-id="1b419-105">В этой процедуре описывается, как системные администраторы могут автоматически назначить пользователей ролям на основе бизнес-данных.</span><span class="sxs-lookup"><span data-stu-id="1b419-105">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="1b419-106">Автоматическое назначение пользователей ролям</span><span class="sxs-lookup"><span data-stu-id="1b419-106">Automatically assign users to roles</span></span>
1. <span data-ttu-id="1b419-107">Перейдите в раздел **Область переходов > Модули > Администрирование системы > Безопасность > Назначить пользователей ролям**.</span><span class="sxs-lookup"><span data-stu-id="1b419-107">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="1b419-108">В этом дереве выберите роль "Супервизор по учету".</span><span class="sxs-lookup"><span data-stu-id="1b419-108">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="1b419-109">Выберите роль, для которой необходимо настроить правило.</span><span class="sxs-lookup"><span data-stu-id="1b419-109">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="1b419-110">В этом примере выберите роль "Супервизор по учету".</span><span class="sxs-lookup"><span data-stu-id="1b419-110">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="1b419-111">Щелкните **Добавить правило**, чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="1b419-111">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="1b419-112">В списке **Выбрать запрос** найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="1b419-112">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="1b419-113">Выберите запрос, который требуется использовать для этого правила.</span><span class="sxs-lookup"><span data-stu-id="1b419-113">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="1b419-114">В списке **Имя правила членства** перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="1b419-114">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="1b419-115">Щелкните **Изменить запрос**.</span><span class="sxs-lookup"><span data-stu-id="1b419-115">Click **Edit query**.</span></span> <span data-ttu-id="1b419-116">При необходимости измените запрос.</span><span class="sxs-lookup"><span data-stu-id="1b419-116">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="1b419-117">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="1b419-117">Click **OK**.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="1b419-118">Исключение пользователей из автоматического назначения ролей</span><span class="sxs-lookup"><span data-stu-id="1b419-118">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="1b419-119">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="1b419-119">Close the page.</span></span>
2. <span data-ttu-id="1b419-120">Перейдите в раздел **Область переходов > Модули > Администрирование системы > Безопасность > Назначить пользователей ролям**.</span><span class="sxs-lookup"><span data-stu-id="1b419-120">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="1b419-121">В этом дереве выберите роль "Супервизор по учету".</span><span class="sxs-lookup"><span data-stu-id="1b419-121">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="1b419-122">Выбор роли.</span><span class="sxs-lookup"><span data-stu-id="1b419-122">Select a role.</span></span> <span data-ttu-id="1b419-123">В этом примере выберите роль "Супервизор по учету".</span><span class="sxs-lookup"><span data-stu-id="1b419-123">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="1b419-124">В меню **Пользователи, назначенные ролям** выберите **Назначить / исключить пользователей вручную**.</span><span class="sxs-lookup"><span data-stu-id="1b419-124">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="1b419-125">В списке **Назначить пользователей роли или исключить их из нее** отмерьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="1b419-125">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="1b419-126">Выберите пользователя.</span><span class="sxs-lookup"><span data-stu-id="1b419-126">Select a user.</span></span>  
6. <span data-ttu-id="1b419-127">В область **Панель операций** выберите **Исключить из роли**.</span><span class="sxs-lookup"><span data-stu-id="1b419-127">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="1b419-128">Щелкните **Исключить из роли**, чтобы исключить выбранных пользователей из роли.</span><span class="sxs-lookup"><span data-stu-id="1b419-128">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="1b419-129">Чтобы удалить исключения, выберите пользователей, для которых требуется удалить исключения, а затем щелкните **Сброс статуса**.</span><span class="sxs-lookup"><span data-stu-id="1b419-129">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="1b419-130">При удалении исключения путем сброса статуса пользователя роль пользователя назначается снова автоматически.</span><span class="sxs-lookup"><span data-stu-id="1b419-130">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="1b419-131">Однако пользователь не сразу назначается роли и не исключается из роли при сбросе статуса.</span><span class="sxs-lookup"><span data-stu-id="1b419-131">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="1b419-132">Вместо этого пользователь либо назначается роли, либо удаляется из роли при следующем выполнении правил для автоматического назначения ролей.</span><span class="sxs-lookup"><span data-stu-id="1b419-132">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
