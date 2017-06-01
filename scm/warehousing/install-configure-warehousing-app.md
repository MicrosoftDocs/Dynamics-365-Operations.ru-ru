---
title: "Установка и настройка Microsoft Dynamics 365 for Operations &#8211; Warehousing"
description: "В этом разделе описывается, как установить и настроить Microsoft Dynamics 365 for Operations - Warehousing."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 46b4809ae89f90295766e95ce78a8f019de0cdae
ms.contentlocale: ru-ru
ms.lasthandoff: 05/25/2017


---

# <a name="install-and-configure-microsoft-dynamics-365-for-operations-8211-warehousing"></a>Установка и настройка Microsoft Dynamics 365 for Operations &#8211; Warehousing

[!include[banner](../includes/banner.md)]


В этом разделе описывается, как установить и настроить Microsoft Dynamics 365 for Operations - Warehousing.

Dynamics 365 for Operations - Warehousing представляет собой приложение, доступное в магазине Google Play и в Магазине Windows. Для текущей версии Microsoft Dynamics 365 for Operations это приложение предоставляется в качестве отдельного компонента, что означает самостоятельное развертывание на устройствах, используемые для складских задач. Чтобы использовать приложение в среде Dynamics 365 for Operations, необходимо загрузить приложение на каждое устройство и настроить его для подключения к среде Dynamics 365 for Operations. В этом разделе описывается, как установить приложение на устройствах. Также объясняется, как настроить приложение для подключения к среде Dynamics 365 for Operations.

## <a name="prerequisites"></a>Необходимые условия
Приложение доступно в операционных системах Android и Windows. Чтобы использовать это приложение, на устройстве должна быть установлена одна из следующих поддерживаемых операционных систем. Также необходимо иметь одну из следующих поддерживаемых версий Dynamics 365 for Operations. Используйте сведения из следующей таблицы для оценки, готовы ли ваши аппаратная и программная среды для поддержки установки.

| Платформа                    | Версия                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0                                                                                                                                                               |
| Windows (UWP)               | Windows 10 (все версии)                                                                                                                                                   |
| Dynamics 365 for Operations | Microsoft Dynamics 365 for Operations версии 1611 -или- Microsoft Dynamics AX версии 7.0/7.0.1 и платформа Microsoft Dynamics AX, обновление 2, с пакетом обновления KB 3210014 |

## <a name="get-the-app"></a>Получение приложения
-   Windows (UWP) - [Dynamics 365 for Operations - Warehousing в Магазине Windows](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android - [Dynamics 365 for Operations - Warehousing в магазине Google Play](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

## <a name="create-a-web-service-application-in-active-directory"></a>Создание приложения веб-службы в Active Directory
Чтобы приложение могло взаимодействовать с определенным сервером Dynamics 365 for Operations, необходимо зарегистрировать приложение веб-службы в Azure Active Directory для владельца Dynamics 365 for Operations. По соображениям безопасности рекомендуется создавать приложения веб-службы для каждого устройства, которое используется. Чтобы создать приложение веб-службы в Azure Active Directory (Azure AD), выполните следующие действия:

1.  В веб-браузере перейдите к <https://manage.windowsazure.com>.
2.  Введите имя и пароль пользователя, который имеет доступ к подписке Azure.
3.  На портале Azure в левой области навигации щелкните **Active Directory**.[](./media/wh-01-active-directory-example.png)[![wh-01-пример-active-directory](./media/wh-01-active-directory-example.png)](./media/wh-01-active-directory-example.png)
4.  В сетке выберите экземпляр службы каталогов Active Directory, используемый Dynamics 365 for Operations.
5.  На верхней панели инструментов щелкните **Приложения**. [![wh-02-приложения-active-directory](./media/wh-02-active-directory-applications-1024x197.png)](./media/wh-02-active-directory-applications.png)
6.  В нижней области нажмите **Добавить**. Запускается мастер **Добавление приложения**.
7.  Введите имя приложения и выберите **Веб-приложение и/или веб-интерфейс API**. [![wh-03-добавить-приложение-active-directory](./media/wh-03-active-directory-add-application.png)](./media/wh-03-active-directory-add-application.png)
8.  Введите URL-адрес входа, который является URL-адресом приложения в вашем владении, корневом URL-адресе Operations. URL-адрес входа в данный момент не используется активно при проверке подлинности приложения, но является обязательным полем. Введите этот же URL-адрес в поле URI кода приложения. [![wh-04-добавить-свойства-ad](./media/wh-04-ad-add-properties.png)](./media/wh-04-ad-add-properties.png)
9.  Перейдите на вкладку **Настройка**. [![wh-05-настройка-приложения-ad](./media/wh-05-ad-configure-app.png)](./media/wh-05-ad-configure-app.png)
10. Прокрутите экран вниз до раздела **Разрешения для других приложений**. Щелкните **Добавить приложение**. [![wh-06-добавление-разрешений-приложения-ad](./media/wh-06-ad-app-add-permissions.png)](./media/wh-06-ad-app-add-permissions.png)
11. Выберите **Microsoft Dynamics ERP** в списке. Нажмите кнопку **Полная проверка** в правом углу страницы. [![wh-07-выбор-разрешений-ad](./media/wh-07-ad-select-permissions.png)](./media/wh-07-ad-select-permissions.png)
12. В списке **Делегирование разрешений** установите все флажки. Нажмите кнопку **Сохранить**. [![wh-08-делегирование-разрешений-ad](./media/wh-08-ad-delegate-permissions.png)](./media/wh-08-ad-delegate-permissions.png)
13. Запишите следующую информацию:
    -   **Код клиента** — при прокрутке страницы вверх вы увидите **Код клиента**.
    -   **Ключ** — в разделе **Ключи** создайте ключ, выбрав продолжительность, и скопируйте ключ. Этот ключ будет позже называется **Секрет клиента**.

## <a name="create-and-configure-a-user-account-in-dynamics-365-for-operations"></a>Создание и настройка учетной записи пользователя в Dynamics 365 for Operations
Чтобы включить Dynamics 365 for Operations для использования приложения Azure AD, необходимо выполнить следующие шаги по настройке:

1.  Создайте новую учетную запись пользователя в Azure Active Directory для владельца Dynamics 365 for Operations. Эта учетная запись пользователя предназначена для доступа к определенной пользовательской службе складского приложения, которую предоставляет сервер Dynamics 365 for Operations. После выполнения этого шага у вас будут учетные данные пользователя WMDP, состоящие из адреса электронной почты WMDP и пароля WMDP. Чтобы получить сведения об основных шагах для добавления пользователей в Azure AD и Dynamics 365 for Operations, см. в этом учебнике: [Оформление подписки на Microsoft Dynamics 365 for Operations](/dynamics365/operations/dev-itpro/dev-tools/sign-up-preview-subscription).
2.  Создайте пользователя Dynamics 365 for Operations, который соответствует учетным данным пользователя складского приложения.
    1.  В Dynamics 365 for Operations перейдите к **Администрирование системы** &gt; **Общее** &gt; **Пользователи**.
    2.  Создайте нового пользователя.
    3.  Назначьте пользователя складского мобильного устройства, как показано на следующем рисунке. [![wh-09-добавление-роли-безопасности-пользователя](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

3.  Свяжите приложения Azure Active Directory с пользователем складского приложения.
    1.  В Dynamics 365 for Operations перейдите к **Администрирование системы** &gt; **Настройка** &gt; **Приложения Azure Active Directory**.
    2.  Создайте новую строку.
    3.  Введите **Код клиента** (полученный в предыдущем разделе), присвойте ему имя, затем выберите ранее созданного пользователя. Рекомендуется пометить все устройства, чтобы можно было легко удалять их доступ к Dynamics 365 for Operations, с этой страницы в случае, если они будут потеряны. [![wh-10-форма-приложений-ad](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Настройка приложения
Необходимо настроить приложение на устройстве для подключения к серверу Dynamics 365 for Operations через приложение Azure AD. Для этого необходимо выполнить следующие шаги.

1.  В приложении перейдите к пункту **Параметры подключения**.
2.  Очистите поле **Демонстрационный режим**. [![wh-11-демо-режим-в-настройках-подключения-приложения](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Введите следующие сведения: - **Код клиента Azure Active Directory** - код клиента, который получен на шаге 13 в разделе "Создание приложения веб-службы в Active Directory". - **Секрет клиента Azure Active Directory** — секрет клиента, который получен на шаге 13 в разделе "Создание приложения веб-службы в Active Directory". - **Ресурс Azure Active Directory** — ресурс Azure AD Directory описывает корневой URL-адрес Dynamics 365 for Operations. **Примечание**. Не завершайте это поле символом прямой косой черты (/). - **Владелец Azure Active Directory** – владелец Azure AD Directory, используемый с сервером Dynamics 365 for Operations: https://login.windows.net/&lt;код-вашего-владельца-AD&gt;. Например: https://login.windows.net/contosooperations.onmicrosoft.com. 
**Примечание**. Не завершайте это поле символом прямой косой черты (/). - **Компания** — введите юридическое лицо в Dynamics 365 for Operations, к которому должно подключаться приложение. [![wh-12-настройки-подключения-приложения](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Нажмите кнопку **Назад** в левом верхнем углу приложения. Теперь приложение подключится к серверу Dynamics 365 for Operations, и на дисплее появится экран входа для работника склада. [![wh-13-экран-входа](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

## <a name="remove-access-for-a-device"></a>Удаление доступа для устройства
Если устройство было потеряно или взломано, необходимо удалить доступ к Dynamics 365 for Operations для устройства. Следующие шаги описывают рекомендуемый процесс удаления доступа.

1.  В Dynamics 365 for Operations перейдите к **Администрирование системы** &gt; **Настройка** &gt; **Приложения Azure Active Directory**.
2.  Удалите строку, которая соответствует устройству, для которого необходимо удалить доступ. Запишите **Код клиента**, используемый для удаленного устройства.
3.  Войдите на классический портал Azure по адресу <https://manage.windowsazure.com>.
4.  Щелкните значок **Active Directory** в левом меню, затем щелкните нужный каталог.
5.  В верхнем меню щелкните **Приложения**, затем щелкните приложение, которое требуется настроить. Откроется страница **Быстрый запуск** с единым входом и другими сведениями о конфигурации.
6.  Щелкните вкладку **Конфигурация**, прокрутите экран вниз и убедитесь, что **Код клиента** приложения совпадает с указанным на шаге 2 в этом разделе.
7.  Щелкните кнопку **Удалить** на панели команд.
8.  Нажмите **Да** в сообщение с запросом подтверждения.





