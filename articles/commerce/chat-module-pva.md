---
title: Модуль чата Commerce с Power Virtual Agents
description: В этой статье описывается модуль чата Commerce с Power Virtual Agents, который интегрирует Microsoft Power Virtual Agents с веб-сайтами Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-09-07
ms.openlocfilehash: 838990cb638479c9c90ba0e38794ecedd55e95b3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691080"
---
# <a name="commerce-chat-with-power-virtual-agents-module"></a>Модуль чата Commerce с Power Virtual Agents

[!include [banner](includes/banner.md)]

В этой статье описывается модуль чата Commerce с Power Virtual Agents, который интегрирует Microsoft Power Virtual Agents с веб-сайтами Dynamics 365 Commerce.

Функция чата Commerce с Power Virtual Agents позволяет клиентам электронной коммерции Dynamics 365 использовать возможности чат-бота Power Virtual Agents для обработки своих запросов. В выпуске Dynamics 365 Commerce 10.0.30 эту функцию можно встроить в веб-сайты электронной коммерции, используя модуль чата Commerce с Power Virtual Agents, который является частью библиотеки модуля Commerce.

Функция чата Commerce с Power Virtual Agents помогает предприятиям достичь следующих целей:

- Повышение персонализированного взаимодействия с их клиентами и улучшение удержания.
- Улучшение обслуживания клиентов посредством интеграции чат-ботов самообслуживания.
- Повышение уровня удовлетворенности клиентов и, таким образом, повышение эффективности продаж.

> [!NOTE]
> Сведения о различиях между приложениями многоканального взаимодействия Dynamics 365 для Customer Service и Power Virtual Agents см. в разделе [Обзор модулей чата Commerce](/commerce-chat-modules-overview.md).

## <a name="prerequisites-for-using-power-virtual-agents"></a><a id="prereq"></a>Необходимые условия для использования Power Virtual Agents

Чтобы использовать функцию чата Commerce с Power Virtual Agents, необходимо сначала создать чат-бот Power Virtual Agents для веб-узла электронной коммерции. Инструкции см. в разделе [Создание бота Power Virtual Agent](/power-virtual-agents/authoring-first-bot).

После настройки чат-бота необходимо скопировать значения параметров чатбота **Код бота** и **Код клиента**, чтобы настроить интерфейс чата Commerce. Сведения о порядке копирования этих значений см. в разделе [Получение параметров бота Power Virtual Agents](/power-virtual-agents/publication-connect-bot-to-custom-application#retrieve-your-power-virtual-agents-bot-parameters).

## <a name="configure-your-e-commerce-site"></a>Настройка сайта электронной коммерции 

Одним из рекомендуемых способов внедрения чата для сайта электронной коммерции является добавление модуля чата Commerce с Power Virtual Agents в общий фрагмент заголовка, который используется на страницах сайта.

Чтобы добавить модуль чата в фрагмент заголовка сайта в конструкторе сайтов Commerce, выполните следующие действия.

1. В конструкторе сайтов Commerce для вашего сайта перейдите к пункту **Фрагменты**.
1. Выберите **Создать**.
1. В диалоговом окне **Выбор фрагмента** выберите модуль **Чат Commerce с Power Virtual Agents**, введите имя для фрагмента, затем выберите **ОК**.
1. В представлении структуры выберите гнездо **Соединитель чата Msdyn365 pva**.
1. В области свойств с правой стороны выполните следующие действия:

    1. В разделе **Параметры бота** в поле **URL-адрес CDN чата веб-чата Bot Framework** оставьте значение по умолчанию (например, `https://cdn.botframework.com/botframework-webchat/latest/webchat.js`).
    1. В поле **URL-адрес аутентификации Bot Framework Direct Line** оставьте значение по умолчанию (например, `https://powerva.microsoft.com/api/botmanagement/v1/directline/directlinetoken`).
    1. В поле **Код бота** введите значение **Код бота** Power Virtual Agents, скопированное в разделе [Необходимые условия использования Power Virtual Agents](#prereq).
    1. В поле **Код клиента** введите значение **Код клиента**, которое было скопировано.

1. Выберите **Сохранить**, выберите **Завершить редактирование** для возврата фрагмента, затем нажмите кнопку **Опубликовать**, чтобы опубликовать его.
1. Перейдите в раздел **Фрагменты** и откройте фрагмент заголовка для вашего сайта.
1. В ячейке **Контейнер по умолчанию** выберите многоточие (**...**), затем выберите **Добавить фрагмент**.
1. В диалоговом окне **Выбор модулей** выберите созданный ранее фрагмент чата и нажмите **ОК**.
1. Выберите **Сохранить**, выберите **Завершить редактирование** для возврата фрагмента, затем нажмите кнопку **Опубликовать**, чтобы опубликовать его.

## <a name="proactive-chat-parameters"></a>Параметры упреждающего чата

Чтобы получить полный список параметров настройки упреждающего чата, см. раздел [Параметры упреждающего чата модуля чата Commerce](chat-proactive-chat-parameters.md).

> [!NOTE]
> В настоящее время Power Virtual Agents не поддерживает аутентификацию Azure Active Directory B2C (Azure AD B2C). Он поддерживает только анонимные вызовы Retail Cloud Scale Unit (RCSU), чтобы получить доступность продукта или взаимодействовать с другими анонимными интерфейсами API. Вызовы прошедших проверку подлинности API через чет-ботов Power Virtual Agents требуют явного входа клиента.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор функций чата Commerce](commerce-chat-overview.md)

[Модуль чата Commerce с многоканальным взаимодействием для Customer Service](commerce-chat-module.md)

[Параметры упреждающего чата модуля чата Commerce](chat-proactive-chat-parameters.md)
