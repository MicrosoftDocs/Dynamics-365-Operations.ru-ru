--- 
title: "Назначение пользователей ролям безопасности"
description: "Для доступа к Microsoft Dynamics 365 for Finance and Operations, Enterprise edition пользователи должны быть назначены ролям безопасности."
author: maertenm
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: b951bbf935645460f7be1df656ca2c5269a020ec
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="assign-users-to-security-roles"></a>Назначение пользователей ролям безопасности

[!include[task guide banner](../../includes/task-guide-banner.md)]

Для доступа к Microsoft Dynamics 365 for Finance and Operations, Enterprise edition пользователи должны быть назначены ролям безопасности. В этой процедуре описывается, как системные администраторы могут назначить пользователей ролям автоматически на основе бизнес-данных. В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.


## <a name="automatically-assign-users-to-roles"></a>Автоматическое назначение пользователей ролям
1. Перейдите в раздел "Администрирование системы" > "Контроль доступа" > "Назначить пользователей ролям".
2. В этом дереве выберите роль "Супервизор по учету".
    * Выберите роль, для которой необходимо настроить правило. В этом примере выберите роль "Супервизор по учету".  
3. Щелкните "Добавить правило", чтобы открыть раскрывающееся диалоговое окно.
4. В списке найдите и выберите требуемую запись.
    * Выберите запрос, который требуется использовать для этого правила.  
5. В списке перейдите по ссылке в выбранной строке.
6. Щелкните "Изменить запрос".
    * При необходимости измените запрос.  
7. Нажмите кнопку "OК".

## <a name="exclude-users-from-automatic-role-assignment"></a>Исключение пользователей из автоматического назначения ролей
1. Закройте страницу.
2. Перейдите в раздел "Администрирование системы" > "Контроль доступа" > "Назначить пользователей ролям".
3. В этом дереве выберите роль "Супервизор по учету".
    * Выбор роли. В этом примере выберите роль "Супервизор по учету".  
4. Щелкните "Назначить/исключить пользователей вручную".
5. В списке пометьте выбранную строку.
    * Выберите пользователя.  
6. Щелкните "Исключить из роли".
    * Щелкните "Исключить из роли", чтобы исключить выбранных пользователей из роли. Чтобы удалить исключения, выберите пользователей, для которых требуется удалить исключения, а затем щелкните "Сброс статуса". При удалении исключения путем сброса статуса пользователя роль пользователя назначается снова автоматически. Однако пользователь не сразу назначается роли и не исключается из роли при сбросе статуса. Вместо этого пользователь либо назначается роли, либо удаляется из роли при следующем выполнении правил для автоматического назначения ролей.  

