---
title: Настройка параллельных действий в workflow-процессе
description: Чтобы настроить параллельное мероприятие, необходимо выполнить следующие действия в редакторе workflow-процессов.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8043e2854ccc8db0128969ffe36a5517a12c37ac
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693362"
---
# <a name="configure-parallel-activities-in-a-workflow"></a>Настройка параллельных действий в workflow-процессе

[!include [banner](../includes/banner.md)]

Чтобы настроить параллельное мероприятие, необходимо выполнить следующие действия в редакторе workflow-процессов.

Параллельное мероприятие состоит из ветвей workflow-процесса, которые выполняются одновременно.

## <a name="name-a-parallel-activity"></a>Наименование параллельного действия

Чтобы ввести название параллельного мероприятия, необходимо выполнить следующие действия.

1. Щелкните правой кнопкой мыши параллельное мероприятие, затем щелкните **Свойства**, чтобы открыть форму **Свойства**.
2. В левой области нажмите **Основные настройки**.
3. В поле **Имя** введите уникальное имя для параллельного мероприятия.
4. Нажмите кнопку **Закрыть**.

## <a name="configure-the-branches-of-a-parallel-activity"></a>Настройте ветви параллельного мероприятия

Выполните следующие действия, чтобы добавить и настроить ветви данного параллельного мероприятия.

1. Дважды щелкните параллельное мероприятие для отображения ветвей параллельного мероприятия.
2. Для добавления ветви, перетащите элемент **Ветвь** из зоны **Элементы workflow-процесса** в точку вставки на холст. На следующем рисунке показана точка вставки.

    ![Точка вставки](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > Порядок ветвлений не важен, поскольку все ветви параллельного мероприятия выполняются одновременно.

3. Для настройки каждой ветви см. раздел [Настройка параллельных ветвей в workflow-процессе](configure-parallel-branch-workflow.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]