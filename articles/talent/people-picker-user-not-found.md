---
title: Пользователь не найден в средстве выбора пользователей в Attract или Onboard
description: В этом разделе объясняется, что делать, когда пользователи в клиенте организации не видны в средстве выбора пользователей в приложениях Dynamics 365 for Talent Attract или Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d5a2c61fc21578d1db4c1bf0c3dfaf0c7a93298c
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2019
ms.locfileid: "859513"
---
# <a name="azure-active-directory-users-not-found-in-people-picker"></a>Пользователи Azure Active Directory отсутствуют в средстве выбора пользователей

[!include [banner](includes/banner.md)]

## <a name="issue"></a>Выдать

Некоторые допустимые пользователи в Microsoft Azure Active Directory (Azure AD) для клиента не отображаются при поиске имени в средстве выбора пользователей в приложениях Dynamics 365 for Talent Attract или Onboard.

## <a name="cause"></a>Причина

Определенные пользователем в настоящее время не поддерживаются в приложениях Attract и Onboard. Убедитесь, что пользователь не является гостевым пользователем Azure AD B2B. Сведения "Тип пользователя" можно найти в колонке Azure Active Directory на портале Azure.

Дополнительные сведения об Azure B2B см. в разделе [Что такое доступ гостевого пользователя в Azure Active Directory B2B](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b).

Для пользователей, не являющихся пользователями B2B, имеются отдельные пользователи, которые могут иметь неполные свойства "Тип пользователя" в объекте **Пользователь**. Это можно проверить и исправить с помощью модуля Azure AD Powershell. Дополнительные сведения см. в разделе [Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0).

## <a name="resolution"></a>Приказ

Чтобы выполнить следующие действия для устранения проблемы, необходимо иметь разрешения "Глобальный администратор" в клиенте Azure Active Directory или разрешения для **User.ReadWrite.All**.

Чтобы проверить "Тип пользователя" для затронутого пользователя.

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
Команда возвращает следующую информацию.
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
Отметьте свойство **UserType** для пользователя. Если свойство **UserType** не заполнено, например не имеет значение "Участник" или "Гость", обновите свойство **UserType** с помощью следующей команды.

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```
