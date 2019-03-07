---
title: Создание новых пользователей
description: Пользователи — это сотрудники внутри вашей организации либо внешние клиенты или поставщики, которым требуется доступ к системе для выполнения своей работы.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 12cf223d262c4e0f2a195e95c83a00fc1a3f07e5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "361966"
---
# <a name="create-new-users"></a><span data-ttu-id="66746-103">Создание новых пользователей</span><span class="sxs-lookup"><span data-stu-id="66746-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="66746-104">Пользователи — это сотрудники внутри вашей организации либо внешние клиенты или поставщики, которым требуется доступ к системе для выполнения своей работы.</span><span class="sxs-lookup"><span data-stu-id="66746-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="66746-105">Системные администраторы могут выполнить эту процедуру для добавления пользователей в систему.</span><span class="sxs-lookup"><span data-stu-id="66746-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="66746-106">В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.</span><span class="sxs-lookup"><span data-stu-id="66746-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="66746-107">Добавление нового пользователя</span><span class="sxs-lookup"><span data-stu-id="66746-107">Add a new user</span></span>
1. <span data-ttu-id="66746-108">Перейдите в раздел "Администрирование системы" > "Пользователи" > "Пользователи".</span><span class="sxs-lookup"><span data-stu-id="66746-108">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="66746-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="66746-109">Click New.</span></span>
3. <span data-ttu-id="66746-110">В поле "Код пользователя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="66746-110">In the User ID field, type a value.</span></span>
    * <span data-ttu-id="66746-111">Введите уникальный код пользователя.</span><span class="sxs-lookup"><span data-stu-id="66746-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="66746-112">Код пользователя — обязательное поле.</span><span class="sxs-lookup"><span data-stu-id="66746-112">A user ID is required.</span></span>  
4. <span data-ttu-id="66746-113">В поле "Имя пользователя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="66746-113">In the User name field, type a value.</span></span>
    * <span data-ttu-id="66746-114">Введите имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="66746-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="66746-115">В поле "Домен" введите значение.</span><span class="sxs-lookup"><span data-stu-id="66746-115">In the Domain field, type a value.</span></span>
    * <span data-ttu-id="66746-116">Введите домен пользователя.</span><span class="sxs-lookup"><span data-stu-id="66746-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="66746-117">В поле "Псевдоним" введите значение.</span><span class="sxs-lookup"><span data-stu-id="66746-117">In the Alias field, type a value.</span></span>
    * <span data-ttu-id="66746-118">Введите псевдоним пользователя.</span><span class="sxs-lookup"><span data-stu-id="66746-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="66746-119">В поле "Компания" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="66746-119">In the Company field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="66746-120">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="66746-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="66746-121">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="66746-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="66746-122">Выберите компанию пользователя</span><span class="sxs-lookup"><span data-stu-id="66746-122">Select the user's company</span></span>  
10. <span data-ttu-id="66746-123">Щелкните "Назначить роли".</span><span class="sxs-lookup"><span data-stu-id="66746-123">Click Assign roles.</span></span>
11. <span data-ttu-id="66746-124">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="66746-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="66746-125">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="66746-125">Click OK.</span></span>
13. <span data-ttu-id="66746-126">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="66746-126">Click Save.</span></span>

## <a name="import-users"></a><span data-ttu-id="66746-127">Импорт пользователей</span><span class="sxs-lookup"><span data-stu-id="66746-127">Import users</span></span>
1. <span data-ttu-id="66746-128">Щелкните "Импорт пользователей".</span><span class="sxs-lookup"><span data-stu-id="66746-128">Click Import users.</span></span>
2. <span data-ttu-id="66746-129">В списке пометьте выбранную строку.</span><span class="sxs-lookup"><span data-stu-id="66746-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="66746-130">Щелкните "Импорт пользователей".</span><span class="sxs-lookup"><span data-stu-id="66746-130">Click Import users.</span></span>
4. <span data-ttu-id="66746-131">Щелкните "Закрыть".</span><span class="sxs-lookup"><span data-stu-id="66746-131">Click Close.</span></span>

