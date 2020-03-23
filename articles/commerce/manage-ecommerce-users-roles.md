---
title: Управление пользователями и ролями электронной коммерции
description: В этой теме объясняется, как предоставить пользователям доступ к среде разработки для сайта Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9a1f9abae20d0f2e71790a3b27337338dc042b52
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003541"
---
# <a name="manage-e-commerce-users-and-roles"></a>Управление пользователями и ролями электронной коммерции


[!include [banner](includes/banner.md)]

В этой теме объясняется, как предоставить пользователям доступ к среде разработки для сайта Microsoft Dynamics 365 Commerce.

Чтобы помочь управлять доступом пользователей и предоставлять пользователям разрешения на выполнение определенных задач, в среде разработки сайтов используются группы безопасности, создаваемые в Microsoft Azure Active Directory (Azure AD). Прежде всего, назначьте новую или существующую группу безопасности из Azure AD каждой роли в среде разработки. Затем вы предоставляете или отменяет разрешения для отдельных пользователей, добавляя этих пользователей в соответствующую группу безопасности или удаляя их из группы безопасности.

## <a name="overview-of-roles-in-the-authoring-environment"></a>Обзор ролей в среде разработки

Среда разработки Dynamics 365 for Commerce поддерживает следующие роли.

| Роль                 | Описание |
|----------------------|-------------|
| Системный администратор | Пользователи, имеющие эту роль, имеют все привилегии для всех инструментов и для всех оценок и отзывов. Они также могут создавать сайты. |
| Администратор   | Пользователи, имеющие эту роль, имеют все привилегии для всех инструментов, оценок и отзывов в определенной структуре сайта. |
| Веб-производитель         | Пользователи, имеющие эту роль, могут создавать страницы, фрагменты и шаблоны, отправлять активы и управлять ими, а также расширять продукты и категории. |
| Читатель               | Пользователи, имеющие эту роль, могут просматривать страницы, шаблоны, активы, фрагменты, макеты и параметры, но не могут вносить изменения. |
| Модератор оценок и отзывов        | Пользователи, имеющие эту роль, могут модерировать отзывы по продукту. |

## <a name="system-administrator-role"></a>Роль системного администратора

При подготовке Dynamics 365 Commerce в среде Microsoft Dynamics Lifecycle Services (LCS) необходимо предоставить группу безопасности для роли **Системный администратор**. Эта роль затем автоматически применяется ко всем сайтам, созданным в настраиваемой среде. Группу безопасности для этой роли можно обновить только в LCS. На странице **Администрирование сайта** для всех сайтов она доступна только для чтения и предназначена только для информационных целей.

## <a name="administrator-role"></a>Роль администратора

При создании нового сайта в Commerce вам будет предложено предоставить группу безопасности для роли **Администратор**. Сведения о разрешениях, предоставляемых данной ролью, см. в таблице выше в этом разделе.

## <a name="add-or-update-security-groups"></a>Добавление и обновление групп безопасности

После создания сайта только пользователи, которые находятся в группах безопасности, связанных с ролями **Системный администратор** и **Администратор**, могут получить доступ к среде разработки для этого сайта. Чтобы назначить пользователей для ролей **Веб-производитель**, **Модератор оценок и отзывов** и **Читатель**, необходимо назначить этим ролям группы безопасности. Чтобы добавить группу безопасности к роли или обновить группу безопасности, которая в настоящее время назначена роли, выполните следующие действия.

1. Перейдите на сайт, который требуется обновить.
1. В области **Управление сайтом** откройте страницу **Безопасность**.
1. Выберите роль для изменения.
1. Добавьте группы безопасности в роли или удалите группы безопасности из ролей.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Добавление кода скрипта на страницы сайта для поддержки телеметрии](add-telemetry.md)

[Особенности поисковой оптимизации (SEO) для вашего сайта](search-engine-optimization-considerations.md)

[Управление политикой безопасности содержимого (CSP)](manage-csp.md)