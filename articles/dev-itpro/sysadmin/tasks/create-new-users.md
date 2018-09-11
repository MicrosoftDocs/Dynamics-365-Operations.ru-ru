--- 
title: "Создание новых пользователей"
description: "Пользователи — это сотрудники внутри вашей организации либо внешние клиенты или поставщики, которым требуется доступ к системе для выполнения своей работы."
author: maertenm
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 295c355286b3d2df39cf1144ba7bfecdca25f9cb
ms.contentlocale: ru-ru
ms.lasthandoff: 09/11/2018

---
# <a name="create-new-users"></a><span data-ttu-id="b0fa2-103">Создание новых пользователей</span><span class="sxs-lookup"><span data-stu-id="b0fa2-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b0fa2-104">Пользователи — это сотрудники внутри вашей организации либо внешние клиенты или поставщики, которым требуется доступ к системе для выполнения своей работы.</span><span class="sxs-lookup"><span data-stu-id="b0fa2-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="b0fa2-105">Системные администраторы могут выполнить эту процедуру для добавления пользователей в систему.</span><span class="sxs-lookup"><span data-stu-id="b0fa2-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="b0fa2-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="b0fa2-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="b0fa2-107">Добавление нового пользователя</span><span class="sxs-lookup"><span data-stu-id="b0fa2-107">Add a new user</span></span>
1. <span data-ttu-id="b0fa2-108">Перейдите в раздел "Администрирование системы" > "Пользователи" > "Пользователи".</span><span class="sxs-lookup"><span data-stu-id="b0fa2-108">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="b0fa2-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="b0fa2-109">Click New.</span></span>
3. <span data-ttu-id="b0fa2-110">В поле "Код пользователя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b0fa2-110">In the User ID field, type a value.</span></span>
    * <span data-ttu-id="b0fa2-111">Введите уникальный код пользователя.</span><span class="sxs-lookup"><span data-stu-id="b0fa2-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="b0fa2-112">Код пользователя — обязательное поле.</span><span class="sxs-lookup"><span data-stu-id="b0fa2-112">A user ID is required.</span></span>  
4. <span data-ttu-id="b0fa2-113">В поле "Имя пользователя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b0fa2-113">In the User name field, type a value.</span></span>
    * <span data-ttu-id="b0fa2-114">Введите имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="b0fa2-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="b0fa2-115">В поле "Домен" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b0fa2-115">In the Domain field, type a value.</span></span>
    * <span data-ttu-id="b0fa2-116">Введите домен пользователя.</span><span class="sxs-lookup"><span data-stu-id="b0fa2-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="b0fa2-117">В поле "Псевдоним" введите значение.</span><span class="sxs-lookup"><span data-stu-id="b0fa2-117">In the Alias field, type a value.</span></span>
    * <span data-ttu-id="b0fa2-118">Введите псевдоним пользователя.</span><span class="sxs-lookup"><span data-stu-id="b0fa2-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="b0fa2-119">В поле "Компания" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="b0fa2-119">In the Company field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="b0fa2-120">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="b0fa2-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="b0fa2-121">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="b0fa2-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b0fa2-122">Выберите компанию пользователя</span><span class="sxs-lookup"><span data-stu-id="b0fa2-122">Select the user's company</span></span>  
10. <span data-ttu-id="b0fa2-123">Щелкните "Назначить роли".</span><span class="sxs-lookup"><span data-stu-id="b0fa2-123">Click Assign roles.</span></span>
11. <span data-ttu-id="b0fa2-124">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="b0fa2-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="b0fa2-125">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="b0fa2-125">Click OK.</span></span>
13. <span data-ttu-id="b0fa2-126">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="b0fa2-126">Click Save.</span></span>

## <a name="import-users"></a><span data-ttu-id="b0fa2-127">Импорт пользователей</span><span class="sxs-lookup"><span data-stu-id="b0fa2-127">Import users</span></span>
1. <span data-ttu-id="b0fa2-128">Щелкните "Импорт пользователей".</span><span class="sxs-lookup"><span data-stu-id="b0fa2-128">Click Import users.</span></span>
2. <span data-ttu-id="b0fa2-129">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="b0fa2-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="b0fa2-130">Щелкните "Импорт пользователей".</span><span class="sxs-lookup"><span data-stu-id="b0fa2-130">Click Import users.</span></span>
4. <span data-ttu-id="b0fa2-131">Щелкните "Закрыть".</span><span class="sxs-lookup"><span data-stu-id="b0fa2-131">Click Close.</span></span>


