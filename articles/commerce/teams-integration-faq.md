---
title: Вопросы и ответы по интеграции Dynamics 365 Commerce и Microsoft Teams
description: В этом разделе содержатся ответы на часто задаваемые вопросы по интеграции Microsoft Dynamics 365 Commerce и Microsoft Teams.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 16ad6cec0fb852d863039740e9f2c3406467e899
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692517"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a>Вопросы и ответы по интеграции Dynamics 365 Commerce и Microsoft Teams

[!include [banner](includes/banner.md)]

В этом разделе содержатся ответы на часто задаваемые вопросы по интеграции Microsoft Dynamics 365 Commerce и Microsoft Teams.

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a>Кто в магазине становится владельцем рабочей группы при подготовке Teams из Commerce? 

Все менеджеры магазинов автоматически добавляются в качестве владельцев в соответствующую группу Teams, чтобы они могли выполнять такие операции, как добавление личного канала и добавление или удаление участников. 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a>Как назначить роль "Менеджер взаимодействия" сотруднику в модуле Commerce Headquarters? 

Менеджеры взаимодействия в Microsoft Teams имеют возможность создавать и публиковать списки задач. Сотрудникам организации, которым необходимо стать менеджерам взаимодействия, необходима роль "менеджер задач розничной торговли", назначенная им в Commerce Headquarters.

Чтобы назначить роль менеджера задач розничной торговли для сотрудника в Commerce Headquarters, выполните следующие действия.

1. Перейдите в раздел **Retail и Commerce \> Сотрудники \> Пользователи**.
1. Выберите сотрудника.
1. На экспресс-вкладке **Роли пользователя** выберите **Назначить роли**.
1. В диалоговом окне **Назначение ролей пользователю** выберите роль **Руководителя задачи Retail** и нажмите кнопку **ОК**.

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a>Как сделать конкретную организационную иерархию доступной для отправки в Microsoft Teams?

В Commerce Headquarters иерархия каждой организации связана с одной или несколькими целями. Убедитесь, что иерархия, которую вы хотите подготовить в Microsoft Teams, имеет связанную с ней цель **Отчетность розничной торговли**, как показано в следующем примере изображения. 

![Пример цели организационной иерархии в центральном офисе Commerce.](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a>Как разрешить работникам розничного магазина входить в Commerce POS, используя Azure Active Directory (Azure AD)?

Сведения о настройке использования проверки подлинности Azure AD в Commerce POS см. в разделе [Включение проверки подлинности Azure Active Directory для входа в POS-терминал](aad-pos-logon.md).

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a>Как сопоставить магазины и соответствующие рабочие группы в Commerce Headquarters, если в организации уже созданы рабочие группы в Microsoft Teams?

Сведения о сопоставлении магазинов и рабочих групп при наличии готовых групп см. в разделе [Сопоставление магазинов и соответствующих рабочих групп, если в организации имеются готовые рабочие группы в Microsoft Teams](map-stores-existing-teams.md).

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a>Как удалить токен API Microsoft Graph, хранящийся в хранилище сеанса?

Пользователь, вошедший в POS-терминал с учетной записью Azure Active Directory (Azure AD), должен выйти из POS-терминала или закрыть приложение, чтобы стереть хранилище сеанса. 

> [!TIP]
> Рекомендуется, чтобы работники магазина всегда запирали POS-терминал или выходили из сеанса, когда они не используют терминал. 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a>Что произойдет, если у магазина нет менеджеров магазина?

Если в магазине нет менеджеров, группа рабочей группы не будет создана для магазина или в Teams. 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a>Что произойдет, если менеджер магазина покидает компанию?

Любой пользователь, имеющий роль владельца, может добавить нового менеджера магазина в Commerce Headquarters и повторно подготовить Teams, чтобы новый менеджер имел необходимые привилегии в Teams для этой группы. 

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор интеграции Dynamics 365 Commerce и Microsoft Teams](commerce-teams-integration.md)

[Включение интеграции Dynamics 365 Commerce и Microsoft Teams](enable-teams-integration.md)

[Подготовка Microsoft Teams из Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Синхронизация управления задачами между Microsoft Teams и Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Управление ролями пользователей в Microsoft Teams](manage-user-roles-teams.md)

[Сопоставление магазинов и рабочих групп, если имеются готовые рабочие группы в Microsoft Teams](map-stores-existing-teams.md)
