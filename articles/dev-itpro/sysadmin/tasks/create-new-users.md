---
title: Создание новых пользователей
description: Пользователи — это сотрудники внутри вашей организации либо внешние клиенты или поставщики, которым требуется доступ к системе для выполнения своей работы.
author: maertenm
manager: AnnBe
ms.date: 07/01/2019
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
ms.openlocfilehash: a542ece226750330262e0c44427e5654fa4f6369
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916492"
---
# <a name="create-new-users"></a><span data-ttu-id="e002c-103">Создание новых пользователей</span><span class="sxs-lookup"><span data-stu-id="e002c-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e002c-104">Пользователи — это сотрудники внутри вашей организации либо внешние клиенты или поставщики, которым требуется доступ к системе для выполнения своей работы.</span><span class="sxs-lookup"><span data-stu-id="e002c-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="e002c-105">Системные администраторы могут выполнить эту процедуру для добавления пользователей в систему.</span><span class="sxs-lookup"><span data-stu-id="e002c-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="e002c-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="e002c-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="e002c-107">Добавление нового пользователя</span><span class="sxs-lookup"><span data-stu-id="e002c-107">Add a new user</span></span>
1. <span data-ttu-id="e002c-108">Перейдите в раздел **Область перехода > Модули > Администрирование системы > Пользователи > Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="e002c-108">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="e002c-109">В области **Панель операций** щелкните **Создать**.</span><span class="sxs-lookup"><span data-stu-id="e002c-109">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="e002c-110">В поле **Код пользователя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="e002c-110">In the **User ID** field, type a value.</span></span> <span data-ttu-id="e002c-111">Введите уникальный код пользователя.</span><span class="sxs-lookup"><span data-stu-id="e002c-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="e002c-112">Код пользователя — обязательное поле.</span><span class="sxs-lookup"><span data-stu-id="e002c-112">A user ID is required.</span></span>  
4. <span data-ttu-id="e002c-113">В поле **Имя пользователя** введите значение.</span><span class="sxs-lookup"><span data-stu-id="e002c-113">In the **User name** field, type a value.</span></span> <span data-ttu-id="e002c-114">Введите имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="e002c-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="e002c-115">В поле **Домен** введите значение.</span><span class="sxs-lookup"><span data-stu-id="e002c-115">In the **Domain** field, type a value.</span></span> <span data-ttu-id="e002c-116">Введите домен пользователя.</span><span class="sxs-lookup"><span data-stu-id="e002c-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="e002c-117">В поле **Псевдоним** введите значение.</span><span class="sxs-lookup"><span data-stu-id="e002c-117">In the **Alias** field, type a value.</span></span> <span data-ttu-id="e002c-118">Введите псевдоним пользователя.</span><span class="sxs-lookup"><span data-stu-id="e002c-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="e002c-119">В поле **Компания** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="e002c-119">In the **Company** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="e002c-120">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="e002c-120">In the list, find and select the desired record.</span></span> 
9. <span data-ttu-id="e002c-121">В разделе **Роли пользователя** щелкните **Назначить роли**.</span><span class="sxs-lookup"><span data-stu-id="e002c-121">In the **User's roles** section, click **Assign roles**.</span></span>
10. <span data-ttu-id="e002c-122">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="e002c-122">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="e002c-123">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="e002c-123">Click **OK**.</span></span>
12. <span data-ttu-id="e002c-124">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="e002c-124">Click **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="e002c-125">Импорт пользователей</span><span class="sxs-lookup"><span data-stu-id="e002c-125">Import users</span></span>
1. <span data-ttu-id="e002c-126">В области **Панель операций** щелкните **Импорт пользователей**.</span><span class="sxs-lookup"><span data-stu-id="e002c-126">On the **Action pane**, click **Import users**.</span></span>
2. <span data-ttu-id="e002c-127">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="e002c-127">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="e002c-128">Щелкните **Импорт пользователей**.</span><span class="sxs-lookup"><span data-stu-id="e002c-128">Click **Import users**.</span></span>
4. <span data-ttu-id="e002c-129">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="e002c-129">Click **Close**.</span></span>

