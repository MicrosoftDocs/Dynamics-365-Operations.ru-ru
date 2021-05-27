---
title: Включение интеграции Dynamics 365 Commerce и Microsoft Teams
description: В этом разделе описывается, как включить интеграцию Microsoft Dynamics 365 Commerce и Microsoft Teams.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eb0b8b419b302fbd0bc107bca22f8b26774ba3c7
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019843"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a>Включение интеграции Dynamics 365 Commerce и Microsoft Teams

[!include [banner](includes/banner.md)]

В этом разделе описывается, как включить интеграцию Microsoft Dynamics 365 Commerce и Microsoft Teams.

Чтобы подготовить в Teams сведения из Dynamics 365 Commerce и синхронизировать функции управления задачами между Teams и приложением POS-терминала, необходимо включить функции интеграции в Commerce Headquarters.

> [!NOTE]
> При включении интеграции Teams вы соглашаетесь с предоставлением общего доступа к данным с Teams. Данные, которые совместно используются с Teams, могут находиться не в той стране, в которой находятся ваши данные Commerce, и к ним могут применяться другие стандарты соответствия нормативам. Дополнительные сведения см. в [Центре управления безопасностью Майкрософт](https://www.microsoft.com/trust-center). Сведения о политиках конфиденциальности корпорации Майкрософт см. в [заявлении о конфиденциальности Майкрософт](https://aka.ms/privacy).

## <a name="enable-teams-integration"></a>Включение интеграции Teams

Прежде чем можно будет включить интеграцию Microsoft Teams с Commerce, необходимо зарегистрировать приложение Teams с вашим клиентом на портале Azure.

Чтобы зарегистрировать приложение Teams с вашим клиентом на портале Azure, выполните следующие действия.

1. Следуйте указаниям из раздела [Краткое руководство: регистрация приложения на платформе удостоверений Майкрософт](/azure/active-directory/develop/quickstart-register-app), чтобы зарегистрировать приложение Teams с вашим клиентом на портале Azure.
1. Скопируйте значение **ИД приложения (клиента)** со страницы **Обзор** для зарегистрированного приложения. Это значение будет использоваться, чтобы включить интеграцию Teams в Commerce Headquarters.
1. Скопируйте значение сертификата, которое был введено при [добавлении сертификата](/azure/active-directory/develop/quickstart-register-app#add-a-certificate) на шаге 1. Этот сертификат называется также открытым ключом или ключом приложения. Это значение будет использоваться, чтобы включить интеграцию Teams в Commerce Headquarters.

Чтобы включить интеграцию Teams в Commerce Headquarters, выполните следующие действия.

1. Выберите **Retail и Commerce \> Настройка канала \> Конфигурация интеграции Microsoft Teams**.
1. На панели операций выберите **Правка**.
1. Для параметра **Включить интеграцию Microsoft Teams** задайте значение **Да**.
1. В полях **Код приложения** и **Ключ приложения** введите значения, полученные при регистрации приложения Teams на портале Azure.
1. На панели операций выберите **Сохранить**.

На следующем рисунке показан пример настройки интеграции Teams в Commerce Headquarters.

![Настройка интеграции Teams в Commerce Headquarters](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

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