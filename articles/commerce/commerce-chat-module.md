---
title: Модуль чата Commerce с многоканальным взаимодействием для Customer Service
description: В этой статье описывается модуль чата Commerce с многоканальным взаимодействием для Customer Service в Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-07-20
ms.openlocfilehash: 99e8b9d66a04390ab70fd1deff9f95fe28bdfae3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690325"
---
# <a name="commerce-chat-with-omnichannel-for-customer-service-module"></a>Модуль чата Commerce с многоканальным взаимодействием для Customer Service

[!include [banner](includes/banner.md)]

В этой статье описывается модуль *Чат Commerce с многоканальным взаимодействием для Customer Service* в Microsoft Dynamics 365 Commerce.

В выпуске Commerce версии 10.0.29 в библиотеку модулей Commerce добавлен новый модуль чата Commerce с многоканальным взаимодействием для Customer Service. Функция чата Commerce предоставляет клиентам электронной коммерции возможности чата Многоканального взаимодействия для Dynamics 365 Customer Service, которые включают в себя поддержку агента службы поддержки, чтобы помогать отвечать на запросы клиентов, предоставлять обслуживание клиентов, а также способствовать продажам для клиентов Commerce.

Функция чата Commerce позволяет предприятиям розничной торговли достигать следующих целей:

- Повышение персонализированного взаимодействия с клиентами, чтобы помочь улучшить удержание клиентов.
- Совершенствование обслуживания клиентов посредством интеграции человеческого агента и чат-ботов самообслуживания.
- Помощь агентам в получении опыта с помощью данных о профиле клиентов в реальном времени, заказе и покупках, что обеспечивает операционные усовершенствования и взаимодействие.
- Повышайте уровень удовлетворенности клиентов, чтобы повысить эффективность продаж.

В функции чата Commerce доступны следующие возможности:

- Чат Commerce с многоканальным взаимодействием для Customer Service
- Добавление **Центра обработки вызовов Commerce** в качестве вкладки приложения в интерфейсе агента многоканального взаимодействия Dynamics 365 для Customer Service

## <a name="prerequisites-for-omnichannel-for-customer-service"></a>Необходимые условия для многоканального взаимодействия для Customer Service

В качестве необходимого условия необходимо настроить чат в мини-приложении администрирования многоканального взаимодействия для Customer Service и получить некоторые параметры для настройки взаимодействия с чатом Commerce. Инструкции см. в разделе [Настройка канала чата](/dynamics365/customer-service/set-up-chat-widget).

После настройки чата в мини-приложении администрирования многоканального взаимодействия для Customer Service вы получите сценарий, аналогичный следующему примеру.

`<script id="Microsoft_Omnichannel_LCWidget" src="https://oc-cdn-ocprod.azureedge.net/livechatwidget/scripts/LiveChatBootstrapper.js" data-app-id="xxxx-xxx-4be7-bcd5-1d118ecffe1f" data-org-id="5a0e73c0-xxxx-xxxxx-xxx- 76df135f375d" data-org-url="https://xxsxxxxssdb348f-crm.omnichannelengagementhub.com"></script>`

Скопируйте этот сценарий, поскольку для настройки модуля чата потребуются значения из него.

### <a name="commerce-chat-with-omnichannel-for-customer-service-mandatory-fields"></a>Обязательные поля чата Commerce с многоканальным взаимодействием для Customer Service

В следующей таблице показаны значения сценария из мини-приложения администрирования многоканального взаимодействия для Customer Service, которые необходимы для настройки модуля чата Commerce с многоканальным взаимодействием для Customer Service.

| Свойство мини-приложения | Описание |
| ------------- |--------------|
| Источник сценария | Значение **src** в сценарии мини-приложения чата. |
| Идентификатор приложения данных | Значение **data-app-id** в сценарии мини-приложения чата. |
| ИД организации данных | Значение **data-org-id** в сценарии мини-приложения чата. |
| URL-адрес организации данных | Значение **data-org-url** в сценарии мини-приложения чата. |

## <a name="configure-the-commerce-chat-experience-for-your-e-commerce-site"></a>Настройка взаимодействия чата Commerce для сайта электронной коммерции

Одним из рекомендуемых способов внедрения чата для сайта электронной коммерции является добавление модуля чата Commerce с многоканальным взаимодействием для Customer Service в общий фрагмент заголовка, который используется на страницах сайта электронной коммерции.

Чтобы добавить модуль чата в фрагмент заголовка сайта в конструкторе сайтов Commerce, выполните следующие действия.

1. В конструкторе сайтов для вашего сайта перейдите к пункту **Фрагменты**.
1. Выберите **Создать**.
1. В диалоговом окне **Выбор фрагмента** выберите модуль **Чат Commerce с многоканальным взаимодействием для Customer Service**, введите имя для фрагмента, затем выберите **ОК**.
1. В представлении структуры выберите гнездо **Соединитель чата Msdyn365 cs**.
1. В области **Свойства чата** с правой стороны выполните следующие действия:

    1. В поле **Источник сценария** введите значение **src**, полученное из сценария Многоканального взаимодействия для Customer Service.
    1. В поле **ИД приложения данных** введите значение **data-app-id**, полученное из сценария Многоканального взаимодействия для Customer Service.
    1. В поле **ИД организации данных** введите значение **data-org-id**, полученное из сценария Многоканального взаимодействия для Customer Service.
    1. В поле **URL-адрес организации данных** введите значение **data-org-url**, полученное из сценария Многоканального взаимодействия для Customer Service.

    ![Создание фрагмента модуля чата Commerce в конструкторе сайтов Commerce.](media/Commerce-chat-creating-new-fragment.png)

1. Выберите **Сохранить**, выберите **Завершить редактирование** для возврата фрагмента, затем нажмите кнопку **Опубликовать**, чтобы опубликовать его.
1. Перейдите в раздел **Фрагменты** и откройте фрагмент заголовка для вашего сайта.
1. В ячейке **Контейнер по умолчанию** выберите многоточие (**...**), затем выберите **Добавить фрагмент**.
1. В диалоговом окне **Выбор модулей** выберите созданный ранее фрагмент чата и нажмите **ОК**.
1. Выберите **Сохранить**, выберите **Завершить редактирование** для возврата фрагмента, затем нажмите кнопку **Опубликовать**, чтобы опубликовать его.

> [!NOTE]
> Чтобы получить полный список параметров настройки, см. раздел [Параметры упреждающего чата модуля чата Commerce](chat-proactive-chat-parameters.md).

## <a name="add-commerce-headquarters-as-an-application-tab-for-omnichannel-for-customer-service"></a>Добавьте Commerce headquarters в качестве вкладки приложения для Многоканального взаимодействия для Customer Service

Вы можете добавить вкладку приложения для Commerce headquarters в Многоканальное взаимодействие для Customer Service. Агенты могут затем использовать интерфейс пользователя для интерфейса агента Многоканального взаимодействия для Customer Service, чтобы легко получить доступ к модулю Dynamics 365 Commerce Customer Service, содержащему контекстные сведения о клиенте вместе со сведениями о его заказах на продажу. Кроме того, агенты обслуживания клиентов могут размещать новые заказы, запускать возвраты и проверять сведения о статусе заказа.

### <a name="create-a-new-application-tab-that-loads-commerce-headquarters-in-an-iframe-module"></a>Создание новой вкладки приложения, в которой загружается Commerce headquarters в модуле iFrame 

Чтобы создать новую вкладку приложения, в которой загружается Commerce headquarters в модуле iFrame, выполните следующие шаги.

1. Откройте портал [Power Apps Maker Portal](https://make.powerapps.com).
1. В области переходов слева выберите **Приложения**.
1. Выберите **Центр администрирования обслуживания клиентов**.
1. Перейдите в раздел **Интерфейс агента**.
1. Для параметра **Шаблоны вкладок приложения** выберите **Управление**.
1. Создайте новую вкладку приложения типа **Веб-сайт стороннего производителя**. Инструкции см. в разделе [Управление шаблонами вкладки приложения](/dynamics365/app-profile-manager/application-tab-templates?tabs=customerserviceadmincenter).
1. В области **Параметры** в поле **Значение** параметра **url** введите следующий URL-адрес, где `<YourOrganizationHeadquartersURL>` и `<LegalEntityname>` заменяются соответствующими значениями. Многоканальное взаимодействие для Customer Service считывает **{AccountNumber}** из контекста чата. Поэтому оставьте **{AccountNumber}** без изменений.

    `https://<YourOrganizationHeadquartersURL>/?mi=MCRCustomerService&cmp=<LegalEntityName>&embedded=true&customerId={AccountNumber}`

1. Оставьте значение поля **Значение** параметра **данные** пустым.

![Создание вкладки приложения в Многоканальном взаимодействии для Dynamics 365 Customer Service.](media/OC-CS-Admin-Application-Tab-Parameters.png)

## <a name="enable-a-new-application-tab-for-customer-agents-in-dynamics-365-omnichannel-for-customer-service"></a>Включение новой вкладки приложения для агентов клиентов в Многоканальном взаимодействии для Dynamics 365 Customer Service

Чтобы включить новую вкладку приложения для агентов клиентов в Многоканальном взаимодействии для Dynamics 365 Customer Service, выполните следующие шаги.
    
1. Откройте портал [Power Apps Maker Portal](https://make.powerapps.com).
1. В области переходов слева выберите **Приложения**.
1. Выберите **Центр администрирования обслуживания клиентов**.
1. Перейдите в раздел **Служба поддержки клиентов \> Рабочие потоки**.
1. Откройте рабочий поток, созданный для агентов, затем в разделе **Дополнительные параметры** выберите **По умолчанию для сеансов**.
1. В разделе **Вкладки приложений** выберите **Добавить существующую вкладку приложения**, затем добавьте созданную ранее вкладку приложения. Этот шаг гарантирует, что вкладка приложения, которая загружает Commerce headquarters в модуль iFrame, появится, когда агент получит входящий вызов чата с веб-сайта электронной коммерции.

> [!NOTE]
> Невозможно изменить шаблон сеанса чата по умолчанию в рабочем потоке. Таким образом, может потребоваться создание нового шаблона или дублирование существующего шаблона для его обновления. Дополнительные сведения см. в разделе [Связывание шаблонов с рабочим потоком](/dynamics365/app-profile-manager/associate-templates).

## <a name="add-context-variables-in-dynamics-365-omnichannel-for-customer-service"></a>Добавление контекстных переменных в Многоканальное взаимодействие для Dynamics 365 Customer Service

Чтобы добавить контекстные переменные в Многоканальное взаимодействие для Dynamics 365 Customer Service, выполните следующие шаги.

1. Откройте портал [Power Apps Maker Portal](https://make.powerapps.com).
1. В области переходов слева выберите **Приложения**.
1. Выберите **Центр администрирования обслуживания клиентов**.
1. Перейдите в раздел **Служба поддержки клиентов \> Рабочие потоки**.
1. Откройте рабочий поток, созданный для агентов, затем в разделе **Дополнительные параметры** перейдите в раздел **Контекстные переменные**.
1. Выберите **Изменить**, затем добавьте **AccountNumber** в качестве переменной контекста типа **текст**. Эта переменная поможет Commerce headquarters загрузить сведения о клиенте с соответствующими номерами счетов.

> [!NOTE]
> Если необходимо прочитать адреса электронной почты и имена вошедших пользователей из канала электронной коммерции, можно добавить **Адрес электронной почты** и **Имя** в качестве переменных контекста типа **текст**, в дополнение к переменной контекста **AccountNumber**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор функций чата Commerce](commerce-chat-overview.md)

[Модуль чата Commerce с Power Virtual Agents](chat-module-pva.md)

[Параметры упреждающего чата модуля чата Commerce](chat-proactive-chat-parameters.md)
