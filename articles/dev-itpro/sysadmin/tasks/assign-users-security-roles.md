---
title: Назначение пользователей для ролей безопасности
description: Для получения доступа к Microsoft Dynamics 365 for Finance and Operations, Enterprise edition пользователи должны быть назначены ролям безопасности.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55cb085bb5170aa4894a2240a12f6ca451b922fb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556717"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="8045b-103">Назначение пользователей для ролей безопасности</span><span class="sxs-lookup"><span data-stu-id="8045b-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8045b-104">Для получения доступа к Microsoft Dynamics 365 for Finance and Operations, Enterprise edition пользователи должны быть назначены ролям безопасности.</span><span class="sxs-lookup"><span data-stu-id="8045b-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="8045b-105">В этой процедуре описывается, как системные администраторы могут назначить пользователей ролям автоматически на основе бизнес-данных.</span><span class="sxs-lookup"><span data-stu-id="8045b-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="8045b-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="8045b-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="8045b-107">Автоматическое назначение пользователей ролям</span><span class="sxs-lookup"><span data-stu-id="8045b-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="8045b-108">Перейдите в раздел "Администрирование системы" > "Контроль доступа" > "Назначить пользователей ролям".</span><span class="sxs-lookup"><span data-stu-id="8045b-108">Go to System administration > Security > Assign users to roles.</span></span>
2. <span data-ttu-id="8045b-109">В этом дереве выберите роль "Супервизор по учету".</span><span class="sxs-lookup"><span data-stu-id="8045b-109">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="8045b-110">Выберите роль, для которой необходимо настроить правило.</span><span class="sxs-lookup"><span data-stu-id="8045b-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="8045b-111">В этом примере выберите роль "Супервизор по учету".</span><span class="sxs-lookup"><span data-stu-id="8045b-111">In this example, select Accounting supervisor.</span></span>  
3. <span data-ttu-id="8045b-112">Щелкните "Добавить правило", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="8045b-112">Click Add rule to open the drop dialog.</span></span>
4. <span data-ttu-id="8045b-113">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="8045b-113">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8045b-114">Выберите запрос, который требуется использовать для этого правила.</span><span class="sxs-lookup"><span data-stu-id="8045b-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="8045b-115">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="8045b-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="8045b-116">Щелкните "Изменить запрос".</span><span class="sxs-lookup"><span data-stu-id="8045b-116">Click Edit query.</span></span>
    * <span data-ttu-id="8045b-117">При необходимости измените запрос.</span><span class="sxs-lookup"><span data-stu-id="8045b-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="8045b-118">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="8045b-118">Click OK.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="8045b-119">Исключение пользователей из автоматического назначения ролей</span><span class="sxs-lookup"><span data-stu-id="8045b-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="8045b-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="8045b-120">Close the page.</span></span>
2. <span data-ttu-id="8045b-121">Перейдите в раздел "Администрирование системы" > "Контроль доступа" > "Назначить пользователей ролям".</span><span class="sxs-lookup"><span data-stu-id="8045b-121">Go to System administration > Security > Assign users to roles.</span></span>
3. <span data-ttu-id="8045b-122">В этом дереве выберите роль "Супервизор по учету".</span><span class="sxs-lookup"><span data-stu-id="8045b-122">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="8045b-123">Выбор роли.</span><span class="sxs-lookup"><span data-stu-id="8045b-123">Select a role.</span></span> <span data-ttu-id="8045b-124">В этом примере выберите роль "Супервизор по учету".</span><span class="sxs-lookup"><span data-stu-id="8045b-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="8045b-125">Щелкните "Назначить/исключить пользователей вручную".</span><span class="sxs-lookup"><span data-stu-id="8045b-125">Click Manually assign / exclude users.</span></span>
5. <span data-ttu-id="8045b-126">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="8045b-126">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="8045b-127">Выберите пользователя.</span><span class="sxs-lookup"><span data-stu-id="8045b-127">Select a user.</span></span>  
6. <span data-ttu-id="8045b-128">Щелкните "Исключить из роли".</span><span class="sxs-lookup"><span data-stu-id="8045b-128">Click Exclude from role.</span></span>
    * <span data-ttu-id="8045b-129">Щелкните "Исключить из роли", чтобы исключить выбранных пользователей из роли.</span><span class="sxs-lookup"><span data-stu-id="8045b-129">Click Exclude from role to exclude the selected users from the role.</span></span> <span data-ttu-id="8045b-130">Чтобы удалить исключения, выберите пользователей, для которых требуется удалить исключения, а затем щелкните "Сброс статуса".</span><span class="sxs-lookup"><span data-stu-id="8045b-130">To remove exclusions, select the users that you want to remove exclusions for, and then click Reset status.</span></span> <span data-ttu-id="8045b-131">При удалении исключения путем сброса статуса пользователя роль пользователя назначается снова автоматически.</span><span class="sxs-lookup"><span data-stu-id="8045b-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="8045b-132">Однако пользователь не сразу назначается роли и не исключается из роли при сбросе статуса.</span><span class="sxs-lookup"><span data-stu-id="8045b-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="8045b-133">Вместо этого пользователь либо назначается роли, либо удаляется из роли при следующем выполнении правил для автоматического назначения ролей.</span><span class="sxs-lookup"><span data-stu-id="8045b-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  

