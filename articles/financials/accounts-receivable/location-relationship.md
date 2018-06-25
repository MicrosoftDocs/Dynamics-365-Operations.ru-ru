---
title: "Добавить расположение и типы отношений субъектов"
description: "В этом теме объясняется, как добавить новый тип местоположения и отношения субъектов."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8435389a523d8393e9d4daa0cb1244203c0dbb12
ms.openlocfilehash: bd8c5a18d69e1952d32675d759b8b2a997844822
ms.contentlocale: ru-ru
ms.lasthandoff: 05/21/2018

---

# <a name="add-new-location-roles-and-party-relationship-types"></a>Добавить новые роли местоположения и типы отношения субъектов 

## <a name="add-new-location-roles"></a>Добавление ролей местоположения

Существует два способа добавить новые роли местоположения для адреса и контактной информации:

-  Добавить посредством страницы **Адрес и контактная информация**. Новая роль будет сохранена в таблице **LogisticsLocationRole** под типом = 0, что означает, что роль не является системной ролью, определенной в перечислении **LogisticsLocationRoleType** и ее расширениях. Пользователь будет иметь возможность использовать эту роль при создании адреса или контактной информации.

    ![Цель адреса и контактной информации](media/Address-Contact.PNG)

-  Добавьте его в расширение перечисления **LogisticsLocationRoleType** и задайте его заполнение во время синхронизации базы данных.

    1.  Создайте расширение для перечисления **LogisticsLocationRoleType** и добавьте новую роль в расширении. 
  
        ![LogisticsLocationRoleType](media/Logistics.PNG)

    2. Создание нового файла ресурса для новой роли, а затем назначение значения для его свойств.
     
     ![Новый файл ресурса](media/Resource.PNG)
        
    3.  Создайте класс совокупности данных и обеспечьте метод обработчика для заполнения новой роли. 

        ![Заполнение данными](media/Dirdata.PNG)

    4.  Чтобы проверить заполнение новой роли местоположения, можно создать исполнимый класс, готовый к выполнению и вызвать DirDataPopulation::insertLogisticsLocationRoles() в Main(). После завершения этого процесса должна появиться новая роль, заполняемая в таблице **LogisticsLocationRole** символом \> 0. Новая роль в отобразится на странице **адреса и контактной информации цели**.

        ![Вставить новое местонахождение](media/InsertNewLocation.PNG)

## <a name="add-new-party-relationship-types"></a>Добавить новые типы отношений субъектов 

Добавить новый тип отношений можно двумя способами:

-   Добавить через страницу **типы отношений**. Новое отношение будет сохранен в **DirRelationshipTypeTable** с типом системы = 0.

    ![Типы отношений](media/Relationship.PNG)

-  Добавьте его в расширение перечисления **DirSystemRelationshipType** и задайте его заполнение во время синхронизации базы данных.

    1.  Создайте расширение для перечисления **DirSystemRelationshipType** и добавьте новый тип связи.

    2. Создайте инициализатор для этого нового типа. Несколько примеров можно найти в коде ядра, один из них —**DirRelationshipTypeChildInitialize**. Это класс инициализации для типа отношения субъектов «дочерний». Можно начать с инициализатора путем копирования и вставки этого кода и последующего обновления выделенной области.
    
    ![DirRelationshipChild](media/DirRelationship.PNG)

    3.  Чтобы проверить заполнение нового типа связи, можно создать исполнимый класс, готовый к выполнению и вызвать DirDataPopulation::insertDirRelationshipTypes() в Main(). Должен появиться новый тип отношения **DirRelationshipTypeTable**, и новый тип отношения будет доступен на странице **Типы отношений**.

        ![Исполняемый класс](media/Runnable.PNG)
