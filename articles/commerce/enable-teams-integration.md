---
title: Включение интеграции Dynamics 365 Commerce и Microsoft Teams
description: В этой статье описывается, как включить интеграцию Microsoft Dynamics 365 Commerce и Microsoft Teams.
author: gvrmohanreddy
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f8b84938c2047ab1102864cc203e0ec853160bb1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274322"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a>Включение интеграции Dynamics 365 Commerce и Microsoft Teams

[!include [banner](includes/banner.md)]

В этой статье описывается, как включить интеграцию Microsoft Dynamics 365 Commerce и Microsoft Teams.

Чтобы подготовить в Teams сведения из Dynamics 365 Commerce и синхронизировать функции управления задачами между Teams и приложением POS-терминала, необходимо включить функции интеграции в Commerce Headquarters.

> [!NOTE]
> При включении интеграции Teams вы соглашаетесь с предоставлением общего доступа к данным с Teams. Данные, которые совместно используются с Teams, могут находиться не в той стране, в которой находятся ваши данные Commerce, и к ним могут применяться другие стандарты соответствия нормативам. Дополнительные сведения см. в [Центре управления безопасностью Майкрософт](https://www.microsoft.com/trust-center). Сведения о политиках конфиденциальности корпорации Майкрософт см. в [заявлении о конфиденциальности Майкрософт](https://aka.ms/privacy).

## <a name="enable-teams-integration"></a>Включение интеграции Teams

Прежде чем можно будет включить интеграцию Microsoft Teams с Commerce, необходимо зарегистрировать приложение Teams с вашим клиентом на портале Azure.

Чтобы зарегистрировать приложение Teams с вашим клиентом на портале Azure, выполните следующие действия.

1. Следуйте указаниям из раздела [Краткое руководство: регистрация приложения на платформе удостоверений Майкрософт](/azure/active-directory/develop/quickstart-register-app), чтобы зарегистрировать приложение Teams с вашим клиентом на портале Azure.
1. На вкладке **Регистрация приложения** выберите приложение, которое было создано на предыдущем шаге. Затем на вкладке **Проверка подлинности** выберите **Добавить платформу**.
1. В диалоговом окне выберите **Интернет**. Затем в поле **URL-адреса перенаправления** введите URL-адрес в формате **\<HQUrl\>/oauth**. Замените **\<HQUrl\>** URL-адресом Commerce headquarters (например, `https://hxennugbjtweufmdeo385f47fadb6aa9a0aos.cloudax.int.dynamics.com/oauth`).
1. На странице **Обзор** зарегистрированного приложения скопируйте значение **ИД приложения (клиента)**. Вам потребуется указать это значение, чтобы включить интеграцию Teams в Commerce Headquarters в следующем разделе.
1. Следуйте инструкциям в разделе [Добавление секрета клиента](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret), чтобы добавить секрет клиента. Затем скопируйте значение **Значение секрета** для клиента. Вам потребуется указать это значение, чтобы включить интеграцию Teams в Commerce Headquarters в следующем разделе.
1. Выберите **Разрешения API**, затем выберите **Добавить разрешение**.
1. В диалоговом окне **Разрешения запроса API** выберите **Microsoft Graph**, выберите **Делегированные разрешения**, разверните пункт **Группа**, выберите **Group.ReadWrite.All**, затем выберите **Добавить разрешения**.
1. В диалоговом окне **Разрешения запроса API** выберите **Добавить разрешение**, выберите **Microsoft Graph**, выберите **Разрешения приложения**, разверните пункт **Группа**, выберите **Group.ReadWrite.All**, затем выберите **Добавить разрешения**.
1. В диалоговом окне **Разрешения запроса API** выберите **Добавить разрешение**. На вкладке **Используемые в моей организации API** найдите пункт **Microsoft Teams Retail Service** и выберите его.
1. Выберите **Делегированные разрешения**, разверните **TaskPublishing**, выберите **TaskPublising.ReadWrite.All**, затем выберите **Добавить разрешения**. Дополнительные сведения см. в разделе [Настройка клиентского приложения для доступа к веб-API](/azure/active-directory/develop/quickstart-configure-app-access-web-apis).

Чтобы включить интеграцию Teams в Commerce Headquarters, выполните следующие действия.

1. Выберите **Retail и Commerce \> Настройка канала \> Конфигурация интеграции Microsoft Teams**.
1. На панели операций выберите **Правка**.
1. Для параметра **Включить интеграцию Microsoft Teams** задайте значение **Да**.
1. В поле **Код приложения** и введите значение **Код приложения (клиента)**, полученное при регистрации приложения Teams на портале Azure.
1. В поле **Ключ приложения** и введите значение **Значение секрета**, полученное при добавлении секрета клиента на портал Azure.
1. На панели операций выберите **Сохранить**.

На следующем рисунке показан пример настройки интеграции Teams в Commerce Headquarters.

![Настройка интеграции Teams в центральном офисе Commerce.](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a>Отключение интеграции Teams

Чтобы отключить интеграцию Microsoft Teams в Commerce Headquarters, выполните следующие действия.

1. Выберите **Retail и Commerce \> Настройка канала \> Конфигурация интеграции Microsoft Teams**.
1. На панели операций выберите **Правка**.
3. Для параметра **Включить интеграцию Microsoft Teams** задайте значение **Нет**.
4. Удалите значения из полей **Код приложения** и **Ключ приложения**.
1. На панели операций выберите **Сохранить**.

> [!NOTE]
> После отключения интеграции Teams с Commerce POS-терминалы больше не будут показывать задачи, опубликованные из приложения Teams.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор интеграции Dynamics 365 Commerce и Microsoft Teams](commerce-teams-integration.md)

[Подготовка Microsoft Teams из Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Синхронизация управления задачами между Microsoft Teams и Dynamics 365 Commerce POS](synchronize-tasks-teams-pos.md)

[Управление ролями пользователей в Microsoft Teams](manage-user-roles-teams.md)

[Сопоставление магазинов и рабочих групп, если имеются готовые рабочие группы в Microsoft Teams](map-stores-existing-teams.md)

[Вопросы и ответы по интеграции Dynamics 365 Commerce и Microsoft Teams](teams-integration-faq.md)
