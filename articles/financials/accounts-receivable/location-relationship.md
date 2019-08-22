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
ms.openlocfilehash: 8c359c5c33bed5b5abe7fc0c8e362c3399e9051a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836684"
---
# <a name="add-location-roles-and-party-relationship-types"></a>Добавить роли местоположения и типы отношения субъектов 

[!include [banner](../includes/banner.md)]

## <a name="add-location-roles"></a>Добавить роли местонахождения

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

## <a name="add-party-relationship-types"></a>Добавить типы отношений субъектов 

Добавить новый тип отношений можно двумя способами:

-   Добавить через страницу **типы отношений**. Новое отношение будет сохранен в **DirRelationshipTypeTable** с типом системы = 0.

    ![Типы отношений](media/Relationship.PNG)

-  Добавьте его в расширение перечисления **DirSystemRelationshipType** и задайте его заполнение во время синхронизации базы данных.

    1.  Создайте расширение для перечисления **DirSystemRelationshipType** и добавьте новый тип связи.

    2. Создайте инициализатор для этого нового типа. Несколько примеров можно найти в коде ядра, один из них —**DirRelationshipTypeChildInitialize**. Это класс инициализации для типа отношения субъектов «дочерний». Можно начать с инициализатора путем копирования и вставки этого кода и последующего обновления выделенной области.
    
    ![DirRelationshipChild](media/DirRelationship.PNG)

    3.  Чтобы проверить заполнение нового типа связи, можно создать исполнимый класс, готовый к выполнению и вызвать DirDataPopulation::insertDirRelationshipTypes() в Main(). Должен появиться новый тип отношения **DirRelationshipTypeTable**, и новый тип отношения будет доступен на странице **Типы отношений**.

        ![Исполняемый класс](media/Runnable.PNG)
