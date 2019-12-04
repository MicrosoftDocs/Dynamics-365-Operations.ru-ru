---
title: Добавить расположение и типы отношений субъектов
description: В этом теме объясняется, как добавить новый тип местоположения и отношения субъектов.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: e38d0bd75ad865b7885182f798beb43551576beb
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770904"
---
# <a name="add-location-and-party-relationship-types"></a><span data-ttu-id="cdb8c-103">Добавить расположение и типы отношений субъектов</span><span class="sxs-lookup"><span data-stu-id="cdb8c-103">Add location and party relationship types</span></span> 

[!include [banner](../includes/banner.md)]

## <a name="add-location-roles"></a><span data-ttu-id="cdb8c-104">Добавить роли местонахождения</span><span class="sxs-lookup"><span data-stu-id="cdb8c-104">Add location roles</span></span>

<span data-ttu-id="cdb8c-105">Существует два способа добавить новые роли местоположения для адреса и контактной информации:</span><span class="sxs-lookup"><span data-stu-id="cdb8c-105">There are two ways to add a new location roles for address and contact information:</span></span>

-  <span data-ttu-id="cdb8c-106">Добавить посредством страницы **Адрес и контактная информация**.</span><span class="sxs-lookup"><span data-stu-id="cdb8c-106">Add it through the **Address and contact information purpose** page.</span></span> <span data-ttu-id="cdb8c-107">Новая роль будет сохранена в таблице **LogisticsLocationRole** под типом = 0, что означает, что роль не является системной ролью, определенной в перечислении **LogisticsLocationRoleType** и ее расширениях.</span><span class="sxs-lookup"><span data-stu-id="cdb8c-107">The new role will be saved to the **LogisticsLocationRole** table with type = 0, which indicates that the role is not a system role defined in the **LogisticsLocationRoleType** enum and its extensions.</span></span> <span data-ttu-id="cdb8c-108">Пользователь будет иметь возможность использовать эту роль при создании адреса или контактной информации.</span><span class="sxs-lookup"><span data-stu-id="cdb8c-108">A user will be able to use this role when creating address or contact information.</span></span>

    ![Цель адреса и контактной информации](media/Address-Contact.PNG)

-  <span data-ttu-id="cdb8c-110">Добавьте его в расширение перечисления **LogisticsLocationRoleType** и задайте его заполнение во время синхронизации базы данных.</span><span class="sxs-lookup"><span data-stu-id="cdb8c-110">Add it to the **LogisticsLocationRoleType** enum extension, and let it populate through the database sync process.</span></span>

    1.  <span data-ttu-id="cdb8c-111">Создайте расширение для перечисления **LogisticsLocationRoleType** и добавьте новую роль в расширении.</span><span class="sxs-lookup"><span data-stu-id="cdb8c-111">Create an extension to the **LogisticsLocationRoleType** enum and add the new role in the extension.</span></span> 
  
        ![Расширение для перечисления LogisticsLocationRoleType](media/Logistics.PNG)

    2. <span data-ttu-id="cdb8c-113">Создание нового файла ресурса для новой роли, а затем назначение значения для его свойств.</span><span class="sxs-lookup"><span data-stu-id="cdb8c-113">Create a new resource file for the new role, and then assign a value for its properties.</span></span>
     
     ![Новый файл ресурса](media/Resource.PNG)
        
    3.  <span data-ttu-id="cdb8c-115">Создайте класс совокупности данных и обеспечьте метод обработчика для заполнения новой роли.</span><span class="sxs-lookup"><span data-stu-id="cdb8c-115">Create a data population class and provide a handler method to populate the new role.</span></span> 

        ![Заполнение данными](media/Dirdata.PNG)

    4.  <span data-ttu-id="cdb8c-117">Чтобы проверить заполнение новой роли местоположения, можно создать исполнимый класс, готовый к выполнению и вызвать DirDataPopulation::insertLogisticsLocationRoles() в Main().</span><span class="sxs-lookup"><span data-stu-id="cdb8c-117">To test populating the new location role, you can create a runnable class, and call DirDataPopulation::insertLogisticsLocationRoles() in Main().</span></span> <span data-ttu-id="cdb8c-118">После завершения этого процесса должна появиться новая роль, заполняемая в таблице **LogisticsLocationRole** символом \> 0.</span><span class="sxs-lookup"><span data-stu-id="cdb8c-118">After this process is complete, you should see the new role populated in the **LogisticsLocationRole** table with type \> 0.</span></span> <span data-ttu-id="cdb8c-119">Новая роль в отобразится на странице **адреса и контактной информации цели**.</span><span class="sxs-lookup"><span data-stu-id="cdb8c-119">The new role will display on the **Address and contact information purpose** page.</span></span>

        ![Вставить новое местонахождение](media/InsertNewLocation.PNG)

## <a name="add-party-relationship-types"></a><span data-ttu-id="cdb8c-121">Добавить типы отношений субъектов</span><span class="sxs-lookup"><span data-stu-id="cdb8c-121">Add party relationship types</span></span> 

<span data-ttu-id="cdb8c-122">Добавить новый тип отношений можно двумя способами:</span><span class="sxs-lookup"><span data-stu-id="cdb8c-122">There are two ways to add a new relationship type:</span></span>

-   <span data-ttu-id="cdb8c-123">Добавить через страницу **типы отношений**.</span><span class="sxs-lookup"><span data-stu-id="cdb8c-123">Add it through the **Relationship types** page.</span></span> <span data-ttu-id="cdb8c-124">Новое отношение будет сохранен в **DirRelationshipTypeTable** с типом системы = 0.</span><span class="sxs-lookup"><span data-stu-id="cdb8c-124">The new relationship will be saved to **DirRelationshipTypeTable** with systemtype = 0.</span></span>

    ![Типы отношений](media/Relationship.PNG)

-  <span data-ttu-id="cdb8c-126">Добавьте его в расширение перечисления **DirSystemRelationshipType** и задайте его заполнение во время синхронизации базы данных.</span><span class="sxs-lookup"><span data-stu-id="cdb8c-126">Add it to the extension of the **DirSystemRelationshipType** enum, and let it populate through database sync process.</span></span>

    1.  <span data-ttu-id="cdb8c-127">Создайте расширение для перечисления **DirSystemRelationshipType** и добавьте новый тип связи.</span><span class="sxs-lookup"><span data-stu-id="cdb8c-127">Create an extension to the **DirSystemRelationshipType** enum and add the new relationship type.</span></span>

    2. <span data-ttu-id="cdb8c-128">Создайте инициализатор для этого нового типа.</span><span class="sxs-lookup"><span data-stu-id="cdb8c-128">Create an initializer for this new type.</span></span> <span data-ttu-id="cdb8c-129">Несколько примеров можно найти в коде ядра, один из них —**DirRelationshipTypeChildInitialize**.</span><span class="sxs-lookup"><span data-stu-id="cdb8c-129">You can find several examples in the core code, one of them is  **DirRelationshipTypeChildInitialize**.</span></span> <span data-ttu-id="cdb8c-130">Это класс инициализации для типа отношения субъектов «дочерний».</span><span class="sxs-lookup"><span data-stu-id="cdb8c-130">This is an initializer class for party relationship type “Child”.</span></span> <span data-ttu-id="cdb8c-131">Можно начать с инициализатора путем копирования и вставки этого кода и последующего обновления выделенной области.</span><span class="sxs-lookup"><span data-stu-id="cdb8c-131">You can start with your initializer by copying and pasting this code and then update the highlighted areas.</span></span>
    
    ![Инициализатор DirRelationshipChild](media/DirRelationship.PNG)

    3.  <span data-ttu-id="cdb8c-133">Чтобы проверить заполнение нового типа связи, можно создать исполнимый класс, готовый к выполнению и вызвать DirDataPopulation::insertDirRelationshipTypes() в Main().</span><span class="sxs-lookup"><span data-stu-id="cdb8c-133">To test populating the new relationship type, you can create a runnable class, and call DirDataPopulation::insertDirRelationshipTypes() in Main().</span></span> <span data-ttu-id="cdb8c-134">Должен появиться новый тип отношения **DirRelationshipTypeTable**, и новый тип отношения будет доступен на странице **Типы отношений**.</span><span class="sxs-lookup"><span data-stu-id="cdb8c-134">You should see the new relationship type in the **DirRelationshipTypeTable**, and the new relationship type will be available on the **Relationship types** page.</span></span>

        ![Исполняемый класс](media/Runnable.PNG)
