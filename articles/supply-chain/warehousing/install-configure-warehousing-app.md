---
title: Обзор установки и настройки складского приложения
description: В этом разделе описывается, как установить и настроить приложение Dynamics 365 Supply Chain Management — Warehousing.
author: MarkusFogelberg
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b8eb8dee88d8664391d2dcf485dff9dee4722cac
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251508"
---
# <a name="install-and-configure-the-warehousing-app-overview"></a>Обзор установки и настройки складского приложения

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 
> В этом разделе описывается, как настроить складские операции для размещения в облаке. Если требуется информация о настройке складских операций для локальных развертываний, см. раздел [Складские операции для локальных развертываний](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).


В этом разделе описывается, как установить и настроить приложение Dynamics 365 Supply Chain Management — Warehousing.

Приложение Warehousing доступно в магазине Google Play и Магазин Windows. Для текущей версии Dynamics 365 Supply Chain Management это приложение предоставляется в качестве отдельного компонента, что означает самостоятельное развертывание на устройствах, используемые для складских задач. Чтобы использовать это, необходимо загрузить приложение на каждое устройство и настроить его для подключения к среде Supply Chain Management. В этом разделе описывается, как установить приложение на устройствах. Также объясняется, как настроить приложение для подключения к среде Supply Chain Management.

## <a name="prerequisites"></a>Необходимые условия
Приложение доступно в операционных системах Android и Windows. Чтобы использовать это приложение, на устройстве должна быть установлена одна из следующих поддерживаемых операционных систем. Необходимо также иметь одну из следующих поддерживаемых версий. Используйте сведения из следующей таблицы для оценки, готовы ли ваши аппаратная и программная среды для поддержки установки.

| Платформа                    | Версия                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Android                     | 4.4, 5.0, 6.0, 7.0, 8.0, 9.0                                                                                                                                                     |
| Windows (UWP)               | Windows 10 (все версии)                                                                                                                                                   |
| Finance and Operations | Microsoft Dynamics 365 for Operations, версия 1611 <br>–или– <br>Microsoft Dynamics AX версии 7.0/7.0.1 и Microsoft Dynamics AX, обновление платформы 2 с исправлением KB 3210014 |

## <a name="get-the-app"></a>Получение приложения
-   Windows (UWP)
     - [Finance and Operations - Warehousing в Магазине Windows](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   Android
    - [Finance and Operations — Warehousing в магазине Google Play](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

> [!NOTE]
> Zebra App Gallery была удалена, что означает, что приложение Warehousing больше не будет доступно для загрузки из этого расположения.

## <a name="create-a-web-service-application-in-azure-active-directory"></a>Создание приложения веб-службы в Azure Active Directory
Чтобы приложение могло взаимодействовать с определенным сервером Supply Chain Management, необходимо зарегистрировать приложение веб-службы в Azure Active Directory для владельца Supply Chain Management. По соображениям безопасности рекомендуется создавать приложения веб-службы для каждого устройства, которое используется. Чтобы создать приложение веб-службы в Azure Active Directory (Azure AD), выполните следующие действия:

1.  В веб-браузере перейдите к <https://portal.azure.com>.
2.  Введите имя и пароль пользователя, который имеет доступ к подписке Azure.
3.  На портале Azure в левой области навигации щелкните **Azure Active Directory**.[](./media/WMA-01-active-directory-example.png)[![WMA-01-пример-активного-каталога](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)
4.  Убедитесь, что экземпляр службы каталогов Active Directory — это экземпляр, используемый Supply Chain Management.
5.  В списке щелкните **Регистрации приложений**. [![WMA-02-регистрации-приложений-active-directory](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)
6.  В верхней области щелкните **Создать регистрацию**. Запускается **Мастер регистрации приложения**.
7.  Введите имя приложения и выберите **Только организации в этом организационном каталоге**. Щелкните **Регистрация**.  [![WMA-03-добавить-приложение-active-directory](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)
8.  Будет открыта новая регистрация приложения. [![WMA-04-настройка-приложения-active-directory](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)
9.  Запомните **Код приложения**, он понадобится позже. **Код приложения** далее будет называться **Код клиента**.
10. Щелкните **Сертификат и секреты** на панели **Управление**. Щелкните **Создать секрет клиента**. [![WMA-05-создание-ключа-active-directory](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)
11. Создайте ключ, введя описание ключа и срок действия в разделе **Пароли**. Щелкните **Добавить** и скопируйте ключ. Этот ключ будет позже называется **Секрет клиента**. [![WMA-06-сохранение-ключа-active-directory](./media/WMA-06-active-directory-save-key.png)](./media/WMA-06-active-directory-save-key.png)

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a>Создание и настройка учетной записи пользователя в Supply Chain Management
Чтобы включить Supply Chain Management для использования приложения Azure AD, необходимо выполнить следующие шаги по настройке:

1.  Создайте пользователя, который соответствует учетным данным пользователя складского приложения.
    1.  Перейдите в раздел **Администрирование системы** &gt; **Общее** &gt; **Пользователи**.
    2.  Создайте нового пользователя.
    3.  Назначьте пользователя складского мобильного устройства, как показано на следующем рисунке. [![wh-09-добавление-роли-безопасности-пользователя](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)

2.  Свяжите приложение Azure Active Directory с пользователем складского приложения.
    1.  В Supply Chain Management перейдите к **Администрирование системы** &gt; **Настройка** &gt; **Приложения Azure Active Directory**.
    2.  Создайте новую строку.
    3.  Введите **Код клиента** (полученный в предыдущем разделе), присвойте ему имя, затем выберите ранее созданного пользователя. Рекомендуется пометить все устройства, чтобы можно было легко удалять их доступ к Supply Chain Management, с этой страницы в случае, если они будут потеряны. [![wh-10-форма-приложений-ad](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)

## <a name="configure-the-application"></a>Настройка приложения
Необходимо настроить приложение на устройстве для подключения к серверу Supply Chain Management через приложение Azure AD. Для этого необходимо выполнить следующие шаги.

1.  В приложении перейдите к пункту **Параметры подключения**.
2.  Очистите поле **Демонстрационный режим**. <br>[![wh-11-демо-режим-в-настройках-подключения-приложения](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)
3.  Введите следующую информацию: 
    + **Код клиента Azure Active Directory** — код клиента, который получен на шаге 9 в разделе "Создание приложения веб-службы в Active Directory". 
    + **Секрет клиента Azure Active Directory** — секрет клиента, который получен на шаге 11 в разделе "Создание приложения веб-службы в Active Directory". 
    + **Ресурс Azure Active Directory** — ресурс каталога Azure AD описывает корневой URL-адрес Supply Chain Management. **Примечание**. Не завершайте это поле символом прямой косой черты (/). 
    + **Владелец Azure Active Directory** — владелец каталога Azure AD, используемый с сервером Supply Chain Management: `https://login.windows.net/your-AD-tenant-ID`. Пример: `https://login.windows.net/contosooperations.onmicrosoft.com.` 
    <br>**Примечание**. Не завершайте это поле символом прямой косой черты (/). 
    + **Компания** — введите юридическое лицо в Supply Chain Management, к которому должно подключаться приложение. <br>[![wh-12-настройки-подключения-приложения](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)
4.  Нажмите кнопку **Назад** в левом верхнем углу приложения. Теперь приложение подключится к серверу Supply Chain Management, и на дисплее появится экран входа для работника склада. <br>[![wh-13-экран-входа](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)

Сведения о том, как настроить приложение Warehousing для сканирование штрих-кодов с помощью камеры на мобильном устройстве см. в разделе [Сканирование штрих-кодов с помощью камеры в Dynamics 365 for Finance and Operations — Warehousing](scan-bar-codes-using-a-camera.md)

## <a name="remove-access-for-a-device"></a>Удаление доступа для устройства
Если устройство было потеряно или взломано, необходимо удалить доступ к Supply Chain Management для устройства. Следующие шаги описывают рекомендуемый процесс удаления доступа.

1.  Перейдите в раздел **Администрирование системы** &gt; **Настройка** &gt; **Приложения Azure Active Directory**.
2.  Удалите строку, которая соответствует устройству, для которого необходимо удалить доступ. Запомните **Код клиента**, использованный для удаленного устройства, он понадобится позже.
3.  Выполните вход на портал Azure по адресу <https://portal.azure.com>.
4.  Щелкните значок **Active Directory** в левом меню и убедитесь, что вы находитесь в правильном каталоге.
5.  В списке щелкните **Регистрации приложений**, затем щелкните приложение, которое требуется настроить. Открывается страница **Параметры** со сведениями о конфигурации.
6.  Убедитесь, что **Код клиента** приложения совпадает с кодом из шага 2 в этом разделе.
7.  Нажмите кнопку **Удалить** в верхней области.
8.  Нажмите **Да** в сообщение с запросом подтверждения.
