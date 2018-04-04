--- 
title: "Назначение пользователей ролям безопасности"
description: "Для доступа к Microsoft Dynamics 365 for Finance and Operations пользователи должны быть назначены ролям безопасности."
author: maertenm
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: da96ec8357ea209fd958e32ab438b13e668735df
ms.contentlocale: ru-ru
ms.lasthandoff: 03/26/2018

---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="5cc02-103">Назначение пользователей для ролей безопасности</span><span class="sxs-lookup"><span data-stu-id="5cc02-103">Assign users to security roles</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5cc02-104">Для доступа к Microsoft Dynamics 365 for Finance and Operations пользователи должны быть назначены ролям безопасности.</span><span class="sxs-lookup"><span data-stu-id="5cc02-104">To access Microsoft Dynamics 365 for Finance and Operations, users must be assigned to security roles.</span></span> <span data-ttu-id="5cc02-105">В этой процедуре описывается, как системные администраторы могут назначить пользователей ролям автоматически на основе бизнес-данных.</span><span class="sxs-lookup"><span data-stu-id="5cc02-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="5cc02-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="5cc02-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="5cc02-107">Автоматическое назначение пользователей ролям</span><span class="sxs-lookup"><span data-stu-id="5cc02-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="5cc02-108">Перейдите в раздел "Администрирование системы" > "Контроль доступа" > "Назначить пользователей ролям".</span><span class="sxs-lookup"><span data-stu-id="5cc02-108">Go to System administration > Security > Assign users to roles.</span></span>
2. <span data-ttu-id="5cc02-109">В этом дереве выберите роль "Супервизор по учету".</span><span class="sxs-lookup"><span data-stu-id="5cc02-109">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="5cc02-110">Выберите роль, для которой необходимо настроить правило.</span><span class="sxs-lookup"><span data-stu-id="5cc02-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="5cc02-111">В этом примере выберите роль "Супервизор по учету".</span><span class="sxs-lookup"><span data-stu-id="5cc02-111">In this example, select Accounting supervisor.</span></span>  
3. <span data-ttu-id="5cc02-112">Щелкните "Добавить правило", чтобы открыть раскрывающееся диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5cc02-112">Click Add rule to open the drop dialog.</span></span>
4. <span data-ttu-id="5cc02-113">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="5cc02-113">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5cc02-114">Выберите запрос, который требуется использовать для этого правила.</span><span class="sxs-lookup"><span data-stu-id="5cc02-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="5cc02-115">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="5cc02-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="5cc02-116">Щелкните "Изменить запрос".</span><span class="sxs-lookup"><span data-stu-id="5cc02-116">Click Edit query.</span></span>
    * <span data-ttu-id="5cc02-117">При необходимости измените запрос.</span><span class="sxs-lookup"><span data-stu-id="5cc02-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="5cc02-118">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="5cc02-118">Click OK.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="5cc02-119">Исключение пользователей из автоматического назначения ролей</span><span class="sxs-lookup"><span data-stu-id="5cc02-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="5cc02-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="5cc02-120">Close the page.</span></span>
2. <span data-ttu-id="5cc02-121">Перейдите в раздел "Администрирование системы" > "Контроль доступа" > "Назначить пользователей ролям".</span><span class="sxs-lookup"><span data-stu-id="5cc02-121">Go to System administration > Security > Assign users to roles.</span></span>
3. <span data-ttu-id="5cc02-122">В этом дереве выберите роль "Супервизор по учету".</span><span class="sxs-lookup"><span data-stu-id="5cc02-122">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="5cc02-123">Выбор роли.</span><span class="sxs-lookup"><span data-stu-id="5cc02-123">Select a role.</span></span> <span data-ttu-id="5cc02-124">В этом примере выберите роль "Супервизор по учету".</span><span class="sxs-lookup"><span data-stu-id="5cc02-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="5cc02-125">Щелкните "Назначить/исключить пользователей вручную".</span><span class="sxs-lookup"><span data-stu-id="5cc02-125">Click Manually assign / exclude users.</span></span>
5. <span data-ttu-id="5cc02-126">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="5cc02-126">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="5cc02-127">Выберите пользователя.</span><span class="sxs-lookup"><span data-stu-id="5cc02-127">Select a user.</span></span>  
6. <span data-ttu-id="5cc02-128">Щелкните "Исключить из роли".</span><span class="sxs-lookup"><span data-stu-id="5cc02-128">Click Exclude from role.</span></span>
    * <span data-ttu-id="5cc02-129">Щелкните "Исключить из роли", чтобы исключить выбранных пользователей из роли.</span><span class="sxs-lookup"><span data-stu-id="5cc02-129">Click Exclude from role to exclude the selected users from the role.</span></span> <span data-ttu-id="5cc02-130">Чтобы удалить исключения, выберите пользователей, для которых требуется удалить исключения, а затем щелкните "Сброс статуса".</span><span class="sxs-lookup"><span data-stu-id="5cc02-130">To remove exclusions, select the users that you want to remove exclusions for, and then click Reset status.</span></span> <span data-ttu-id="5cc02-131">При удалении исключения путем сброса статуса пользователя роль пользователя назначается снова автоматически.</span><span class="sxs-lookup"><span data-stu-id="5cc02-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="5cc02-132">Однако пользователь не сразу назначается роли и не исключается из роли при сбросе статуса.</span><span class="sxs-lookup"><span data-stu-id="5cc02-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="5cc02-133">Вместо этого пользователь либо назначается роли, либо удаляется из роли при следующем выполнении правил для автоматического назначения ролей.</span><span class="sxs-lookup"><span data-stu-id="5cc02-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  


