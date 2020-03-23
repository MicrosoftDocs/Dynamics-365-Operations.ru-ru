---
title: Создание новых пользователей
description: Пользователи — это сотрудники внутри вашей организации либо внешние клиенты или поставщики, которым требуется доступ к системе для выполнения своей работы.
author: maertenm
manager: AnnBe
ms.date: 02/06/2020
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
ms.openlocfilehash: 6d884dfe30be5684a90925d4d2d9ab7eebca5b44
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029817"
---
# <a name="create-new-users"></a>Создание новых пользователей

[!include [task guide banner](../../includes/task-guide-banner.md)]

Пользователи — это сотрудники внутри вашей организации либо внешние клиенты или поставщики, которым требуется доступ к системе для выполнения своей работы.

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>Связывание пользователя с лицензией (только новые типы лицензий)
Для клиентов, для которых используется один из новых типов лицензий, которые были добавлены в октябре 2019 года, пользователи должны быть связаны с лицензией. Пользователи, связанные с лицензией, автоматически добавляются в качестве системных пользователей, не имеющих ролей при первом входе в систему.

Администраторы системы могут [назначать лицензии пользователям](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) из [центра администрирования Microsoft 365](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a>Связывание внешнего пользователя с лицензией (только новые типы лицензий)
Пользователи, внешние по отношению к клиенту, для которого была выполнено развертывание среды, должны быть представлены в каталоге клиента узла (Azure Active Directory (Azure AD)), чтобы им можно было назначить лицензии. Эти внешние пользователи должны быть добавлены к клиенту в Azure AD в качестве гостевых пользователей, а затем им назначаются соответствующие лицензии. Дополнительные сведения см. в разделе [Добавление пользователей сотрудничества Azure Active Directory B2B на портале Azure](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).

## <a name="add-a-new-user"></a>Добавление нового пользователя
1. Перейдите в раздел **Администрирование системы \> Пользователи \> Пользователи**.
2. В области действий выберите **Создать**.
3. В поле **Код пользователя** введите уникальный код для пользователя. Код пользователя — обязательное поле.  
4. В поле **Имя пользователя** введите имя пользователя.  
5. В поле **Домен** введите домен пользователя.  
6. В поле **Псевдоним** введите псевдоним пользователя.  
7. В поле **Компания** выберите требуемую компанию. 
8. На экспресс-вкладке **Роли пользователя** выберите **Назначить роли**, чтобы назначить пользователям роли безопасности. Дополнительные сведения см. в разделе [Назначение пользователей для ролей безопасности](assign-users-security-roles.md).
9. Нажмите **ОК**.
10. Нажмите **Сохранить**.

## <a name="import-users"></a>Импорт пользователей
1. На панели операций выберите **Импорт пользователей**.
2. В списке пометьте выбранную строку.
3. Выберите **Импорт пользователей**.
4. Выберите **Закрыть**.
