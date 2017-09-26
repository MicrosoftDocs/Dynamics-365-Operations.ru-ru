--- 
title: "Разрешение пользователям получать сообщения электронной почты, связанные с workflow-процессом"
description: "Систему можно настроить для отправки сообщений электронной почты пользователям при возникновении событий, связанных с workflow-процессами."
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 76ae3b1f479733f7e3a738fd43e52134bda7069a
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a>Разрешение пользователям получать сообщения электронной почты, связанные с workflow-процессом

[!include[task guide banner](../../includes/task-guide-banner.md)]

Систему можно настроить для отправки сообщений электронной почты пользователям при возникновении событий, связанных с workflow-процессами. Например, сообщения электронной почты можно отправлять пользователям, когда им назначаются документы для утверждения. В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.

1. Перейдите в раздел "Администрирование системы" > "Пользователи" > "Пользователи".
2. В списке найдите и выберите требуемую запись.
3. Щелкните "Параметры пользователя".
4. Щелкните вкладку "Workflow-процесс".
    * Убедитесь, что раздел "Уведомления" развернут.     В разделе "Уведомления" можно указать способ уведомления пользователя о событиях, связанных с workflow-процессами.  
5. В поле "Тип уведомления workflow-процесса по строке" выберите параметр.
    * Сгруппированные — уведомления для номенклатур строки сгруппированы в одно сообщение электронной почты.    Индивидуальные — сообщение электронной почты отправляется для каждой номенклатуры строки.  
    * Если требуется, чтобы пользователь получал уведомления в клиенте, установите флажок "Отправлять уведомления в электронной почте".  
6. Нажмите кнопку "Сохранить".
7. Закройте страницу.

