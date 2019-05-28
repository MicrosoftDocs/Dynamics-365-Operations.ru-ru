---
title: Создание пакетного задания
description: Пакетное задание — это группа задач, отправляемых в экземпляр AOS для автоматической обработки.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fbb844ebcf8d4b47b127132a5bf0ea45fa40f747
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562889"
---
# <a name="create-a-batch-job"></a>Создание пакетного задания

[!include [task guide banner](../../includes/task-guide-banner.md)]

Пакетное задание — это группа задач, отправляемых в экземпляр AOS для автоматической обработки. Пакетные задания выполняются с использованием параметров доступа пользователя, создавшего задание. Следующая процедура используется для создания пакетного задания. В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.


## <a name="create-the-batch-job"></a>Создание пакетного задания
1. Перейдите в раздел "Администрирование системы" > "Запросы" > "Пакетные задания".
2. Щелкните "Создать".
3. В поле "Описание задания" введите значение.
4. В поле "Запланированные дата/время начала" введите дату и время.
5. Нажмите кнопку "Сохранить".

## <a name="create-a-recurrence"></a>Создание повторения
1. В области действий щелкните "Пакетное задание".
2. Щелкните "Повторение".
    * Эти параметры используются для ввода диапазона и схемы повторения.  
3. Нажмите кнопку "OК".

## <a name="add-alerts"></a>Добавление оповещений
1. В области действий щелкните "Пакетное задание".
2. Щелкните "Оповещения".
    * Укажите, требуется ли отправлять оповещения по завершении пакетного задания, в случае ошибки или отмены. Затем укажите, требуется ли отображать оповещения в виде всплывающих сообщений.   
3. Нажмите кнопку "OК".

