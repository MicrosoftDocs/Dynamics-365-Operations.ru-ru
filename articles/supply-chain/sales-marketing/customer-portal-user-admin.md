---
title: Создание пользователей клиентского портала и управление ими (содержит видео)
description: В этой статье объясняется, как создавать учетные записи пользователей клиентского портала и задавать для них разрешения.
author: Henrikan
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ec4f20daac39e1728ab46db159059e51a0cae0a6
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103782"
---
# <a name="create-and-manage-customer-portal-users"></a>Создание пользователей клиентского портала и управление ими

[!include [banner](../includes/banner.md)]


При использовании готовой реализации пользователи не могут самостоятельно регистрироваться для сайтов, созданных с помощью клиентского портала. Чтобы войти в систему и использовать сайт, пользователи должны быть приглашены администратором. Корпорация Майкрософт преднамеренно запретила пользователям выполнять самостоятельную регистрацию.

Прежде чем пользователь сможет использовать веб-сайт, необходимо создать запись контакта для этого пользователя. В этой записи указан счет клиента и юридическое лицо, к которому относится пользователь. Эта информация важна для обеспечения возможности создания и просмотра пользователем заказов на продажу.

При самостоятельной регистрации пользователей для них автоматически создаются записи контактов. Поэтому нельзя гарантировать, что пользователь выбрал правильный счет клиента и юридическое лицо. С другой стороны, процесс приглашения позволяет администратору назначить для записи контакта правильный счет клиента и юридическое лицо перед отправкой приглашения. Если вы думаете о настройке решения, чтобы пользователи могли самостоятельно регистрироваться, примите во внимание возможные последствия.

## <a name="video"></a>Видео
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ADkI]

Видео [Приглашение клиентов для регистрации и использование портала клиента](https://youtu.be/drGUYHX9QIQ) (см. выше) включено в [список воспроизведения по приложениям для управления финансами и операциями](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), доступный в YouTube.

## <a name="prerequisite-setup"></a>Необходимые условия настройки

Контакты на порталах Power Apps хранятся в виде записей в таблице **Контакты** в Microsoft Dataverse. Затем двойная запись синхронизирует эти записи в Microsoft Dynamics 365 Supply Chain Management в соответствии с требованиями.

![Диаграмма системы для контактов клиентского портала.](media/customer-portal-contacts.png "Диаграмма системы для контактов клиентского портала")

Прежде чем приступить к приглашению новых клиентов, убедитесь, что вы включили сопоставление таблицы **Контакт** в двойной записи.

## <a name="the-invitation-process"></a>Процесс приглашения

Чтобы пригласить существующего контакта на клиентский портал, выполните шаги, указанные в разделе [Приглашение контактов на свои порталы](/powerapps/maker/portals/configure/invite-contacts) в документации по порталам Power Apps.

Прежде чем пригласить клиента на присоединение к клиентскому порталу, убедитесь, что [запись контакта](/powerapps/maker/portals/configure/configure-contacts) клиента доступна и настроена следующим образом:

1. В поле **Компания** укажите юридическое лицо, к которому должен относиться клиент в Supply Chain Management.
2. В поле **Счет клиента** укажите номер счета клиента в Supply Chain Management.

После создания контакта его можно просмотреть в Supply Chain Management.

Дополнительные сведения см. в разделе [Настройка контакта для использования на портале](/powerapps/maker/portals/configure/configure-contacts) в документации по порталам Power Apps.

## <a name="out-of-box-web-roles-and-table-permissions"></a>Готовые веб-роли и разрешения таблиц

Роли пользователей на порталах Power Apps определяются [веб-ролями](/powerapps/maker/portals/configure/create-web-roles) и [разрешениями таблиц](/powerapps/maker/portals/configure/assign-entity-permissions). Клиентский портал содержит несколько готовых веб-ролей. Можно создавать новые роли, а также изменять или удалять существующие роли.

### <a name="out-of-box-web-roles"></a>Готовые веб-роли

В этом разделе описываются веб-роли, обеспечиваемые с помощью клиентского портала.

Дополнительные сведения об изменении готовых пользовательских ролей см. в разделе [Создание веб-ролей для порталов](/powerapps/maker/portals/configure/create-web-roles) и [Добавление безопасности на основе записей с помощью разрешений таблиц для порталов](/powerapps/maker/portals/configure/assign-entity-permissions) в документации по порталам Power Apps.

#### <a name="administrator"></a>Администратор

Администратор контролирует и поддерживает веб-сайт. Этот сотрудник выполнит подготовку и настройку клиентского портала. Администратор поддерживает системы ИТ и безопасности портала и гарантирует бесперебойную работу всего процесса. Администратор может также настраивать и/или изменять портал путем добавления новых функций, создания новых ролей и т. д.

#### <a name="customer-representative"></a>Представитель клиента

Представитель клиента работает на компанию клиента и отвечает за управление заказами, размещаемыми компанией. Представитель клиента может просматривать все заказы, которые были размещены для компании, и пользователей, которые их разместили. Кроме того, представитель клиента может просматривать сведения об общем счете и о том, какие контакты могут размещать заказы от имени этого счета.

#### <a name="authorized-users"></a>Авторизованные пользователи

Авторизованные пользователи могут размещать заказы и просматривать статус заказов, которые они разместили. Однако они не могут просматривать статус заказов, размещенных другими пользователями компании.

#### <a name="unauthorized-users"></a>Неавторизованный пользователь

Неавторизованные пользователи не могут просматривать какие-либо данные. Они могут просматривать только общие (публичные) сведения, такие как условия и положения, сведения о компании, где работает клиентский портал.

#### <a name="example"></a>Пример

В следующей таблице показано, какие заказы на продажу могут просматривать пользователи каждой веб-роли в системе.

| Заказ на продажу | Администратор | Представитель клиента для клиента&nbsp;X | Авторизованный пользователь: Jane | Авторизованный пользователь: Sam | Неавторизованный пользователь: May |
|---|---|---|---|---|---|
| Клиент&nbsp;X Приемщик заказа:&nbsp;Jane | Да | Да | Да | Нет | Нет |
| Клиент&nbsp;X Приемщик заказа:&nbsp;Sam | Да | Да | Нет | Да | Нет |
| Клиент&nbsp;Y Приемщик заказа:&nbsp;May | Да | Нет | Нет | Нет | Нет |

> [!NOTE]
> Даже если Sam и Jane являются контактами, работающими у клиента X, они могут видеть только те заказы, которые разместили они, и ничего другого. Хотя у May в системе может быть заказ, она не видит этот заказ на клиентском портале, поскольку она является неавторизованным пользователем. (Кроме того, ей необходимо разместить заказ через другой канал, отличный от клиентского портала.)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
