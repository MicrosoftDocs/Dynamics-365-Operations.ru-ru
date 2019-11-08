---
title: Создание новых пользователей
description: Пользователи — это сотрудники внутри вашей организации либо внешние клиенты или поставщики, которым требуется доступ к системе для выполнения своей работы.
author: maertenm
manager: AnnBe
ms.date: 10/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c347a34a389c32d005cc8086c4a1349ecb8a698
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570529"
---
# <a name="create-new-users"></a>Создание новых пользователей

[!include [task guide banner](../../includes/task-guide-banner.md)]

Пользователи — это сотрудники внутри вашей организации либо внешние клиенты или поставщики, которым требуется доступ к системе для выполнения своей работы.

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>Связывание пользователя с лицензией (только новые типы лицензий)
Для клиентов, для которых используется один из новых типов лицензий, которые были добавлены в октябре 2019 года, пользователи должны быть связаны с лицензией. Пользователи, связанные с лицензией, автоматически добавляются в качестве системных пользователей, не имеющих ролей при первом входе в систему. Пользователи, не связанные с лицензией, получают предупреждающее сообщение.

Администраторы системы могут [назначать лицензии пользователям](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) из [центра администрирования Microsoft 365](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).

## <a name="add-a-new-user"></a>Добавление нового пользователя
1. Перейдите в раздел **Администрирование системы \> Пользователи \> Пользователи**.
2. В области действий выберите **Создать**.
3. В поле **Код пользователя** введите уникальный код для пользователя. Код пользователя — обязательное поле.  
4. В поле **Имя пользователя** введите имя пользователя.  
5. В поле **Домен** введите домен пользователя.  
6. В поле **Псевдоним** введите псевдоним пользователя.  
7. В поле **Компания** выберите требуемую компанию. 
8. На экспресс-вкладке **Роли пользователя** выберите **Назначить роли**, чтобы [назначить пользователям роли безопасности](assign-users-security-roles.md)
9. Нажмите **ОК**.
10. Нажмите **Сохранить**.

## <a name="import-users"></a>Импорт пользователей
1. На панели операций выберите **Импорт пользователей**.
2. В списке пометьте выбранную строку.
3. Выберите **Импорт пользователей**.
4. Выберите **Закрыть**.

