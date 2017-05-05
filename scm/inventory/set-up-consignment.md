---
title: "Настройка коносамента"
description: "В этом разделе описаны способы настройки входящих операций консигнационных запасов."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: afa59439e06aad9d669eb352a9837a013f447249
ms.openlocfilehash: 48e3f7f33bedf33bee5a7c2882e90743feac8687
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-consignment"></a>Настройка коносамента

[!include[banner](../includes/banner.md)]


В этом разделе описаны способы настройки входящих операций консигнационных запасов. 

Консигнационные запасы — это запасы, принадлежащие поставщику, но хранящиеся на вашем сайте. Когда вы готовы потребить или использовать запасы, вы принимаете на себя владение запасами. В этом разделе описывается настройка, необходимая для включения процессов коносамента. Дополнительные сведения о процессах коносамента см. в разделе [Коносамент](consignment.md).

## <a name="inventory-owners"></a>Владельцы запасов
Для записи физических входящих консигнационных запасов необходимо указать владельца поставщика. Это выполняется на странице **Владелец запасов**. При выборе параметра **Счет поставщика** это создает значения по умолчанию для полей **Наименование** и **Владелец**. Значение в поле **Владелец** будет отображаться поставщику, поэтому возможно, потребуется изменить его, если ваши названия счетов поставщика непонятны внешним лицам. Можно изменить поле **Владелец**, но только до момента, когда вы сохраняете запись **Владелец запасов**. Поле **Наименование** заполняется именем субъекта, с которым связан счет поставщика, и это невозможно изменить. 

[![владельцы-запасов](./media/inventory-owners.png)](./media/inventory-owners.png)

## <a name="tracking-dimension-group"></a>Группа аналитик отслеживания
Номенклатуры, которые будут использоваться в процессе коносамента, необходимо связать с параметром **Группа аналитик отслеживания**, в которой для аналитики **Владелец** задано значение **Активна**. У аналитики "Владелец" всегда выбраны параметры **Физические запасы** и **Финансовые запасы**. Параметр **План покрытия по аналитикам** никогда не выбран. 

[![группа-аналитик-отслеживания](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)

## <a name="inventory-ownership-change-journal"></a>Журнал изменения владельца запасов
Журнал **Изменение владельца запасов** используется для регистрации передачи прав собственности на запасы коносамента от поставщика юридическому лицу, которое потребляет их. Как и любой журнал запасов, его необходимо определить с именем журнала запасов. Эти имена создаются на странице **Имена журналов запасов**, а для параметра **Тип журнала** должно быть установлено значение **Изменение владельца**. 

[![журнал-изменения-владельца-запасов](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Совместная работа с поставщиками в процессах коносамента
Если поставщики используют интерфейс совместной работы с поставщиками, они могут использовать его, чтобы контролировать потребление запасов на вашем сайте. Дополнительные сведения о настройке поставщиков для использования совместной работы с поставщиками см. в разделе [Настройка безопасности для пользователей совместной работы с поставщиками](../procurement/configure-security-vendor-portal-users.md).



