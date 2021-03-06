---
title: Создание пакетного задания
description: Пакетное задание — это группа задач, отправляемых в экземпляр AOS для автоматической обработки.
author: maertenm
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f498014555e0beccbc8965dd43e5162944867978
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745869"
---
# <a name="create-a-batch-job"></a>Создание пакетного задания

[!include [banner](../../includes/banner.md)]

Пакетное задание — это группа задач, отправляемых в экземпляр AOS для автоматической обработки. Пакетные задания выполняются с использованием параметров доступа пользователя, создавшего задание. Следующая процедура используется для создания пакетного задания. В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.


## <a name="create-the-batch-job"></a>Создание пакетного задания
1. Перейдите в раздел **Область переходов > Модули > Администрирование системы > Запросы > Пакетные задания**.
2. Нажмите кнопку **Создать**.
3. В поле **Описание задания** введите значение.
4. В поле **Запланированные дата/время начала** введите дату и время.
5. Нажмите кнопку **Сохранить**.

## <a name="create-a-recurrence"></a>Создание повторения
1. В области действий щелкните **Пакетное задание**.
2. Щелкните **Повторение**. Эти параметры используются для ввода диапазона и схемы повторения.  
3. Щелкните **OK**.

## <a name="add-alerts"></a>Добавление оповещений
1. В области действий щелкните **Пакетное задание**.
2. Щелкните **Оповещения**. Укажите, требуется ли отправлять оповещения по завершении пакетного задания, в случае ошибки или отмены. Затем укажите, требуется ли отображать оповещения в виде всплывающих сообщений.   
3. Щелкните **OK**.

## <a name="adjust-batch-job-status"></a>Настройка статуса пакетного задания
1. Перейдите в раздел **Администрирование системы > Запросы > Пакетные задания**.
2. Выберите соответствующее пакетное задание.
3. В области действий щелкните **Пакетное задание > Функции > Изменить статус**.
4. Выберите соответствующий статус.
    - **Отложено**: задавайте пакетное задание как **отложено**, чтобы оно откладывалось планировщиком пакетного задания. Эквивалентно *остановке*.
    - **Ожидание**: установите пакетное задание как **ожидание**, чтобы оно ожидало обработки планировщиком пакетных заданий. Эквивалентно *запуску*.
5. Щелкните **OK**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]