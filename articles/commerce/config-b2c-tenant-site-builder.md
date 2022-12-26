---
title: Настройка клиента B2C в конфигураторе сайта Commerce
description: В этой статье описывается, как настроить клиент "бизнес-потребитель" (B2C) в конструкторе сайтов Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 181edf1570f1a9d071a7fae38ff9d73ff3c068fa
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785315"
---
# <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a>Настройка клиента B2C в конфигураторе сайта Commerce

[!include [banner](includes/banner.md)]

В этой статье описывается, как настроить клиент "бизнес-потребитель" (B2C) в конструкторе сайтов Microsoft Dynamics 365 Commerce.

После завершения настройки клиента Azure AD B2C необходимо настроить клиент B2C в конфигураторе сайта Commerce. Этапы настройки включают сбор информации о приложении B2C с портала Azure, ввод этих сведений о приложении B2C в конфигуратор сайта, затем связывание приложения B2C с сайтом и каналом.

### <a name="collect-the-required-application-information"></a>Сбор необходимой информации о приложении

Чтобы собрать необходимые сведения о приложении, выполните следующие действия.

1. На портале Azure перейдите к пункту **Домашняя страница \> Azure AD B2C — Регистрации приложений**.
1. Выберите приложение, затем в левой области навигации выберите **Обзор** для получения сведений о приложении.
1. В ссылке **Код приложения (клиент)** соберите идентификатор приложения B2C, созданный в вашем клиенте B2C. Впоследствии он будет введено как идентификатор **GUID клиента** в конфигураторе сайта.
1. Выберите **URI перенаправления** и соберите URL-адреса ответа, отображаемые для вашего сайта (URL-адрес ответа, введенный при установке).
1. Перейдите в пункт **Домашняя страница \> Azure AD B2C — потоки пользователей**, затем соберите полные имена каждой политики потока пользователей.

На следующем рисунке показан пример страницы обзора **Azure AD B2C — Регистрация приложений**.

![Azure AD B2C — страница обзора регистраций приложений с выделенным кодом приложения (клиент)](./media/ClientGUID_Application_AzurePortal.png)

На следующем рисунке показан пример политик потока пользователей на странице **Azure AD B2C — потоки пользователей (политики)**.

![Сбор имен каждого потока политик B2C.](./media/B2CImage_22.png)

### <a name="enter-your-azure-ad-b2c-tenant-application-information-into-commerce"></a>Ввод данных приложения клиента Azure AD B2C в Commerce

Перед сопоставлением клиента B2C с вашими сайтами необходимо ввести сведения о клиенте Azure AD B2C в конфигураторе сайта Commerce.

Чтобы добавить данные приложения клиента Azure AD B2C в Commerce, выполните следующие действия.

1. Войдите в систему в качестве администратора конфигуратора сайта Commerce для вашей среды.
1. На левом панели навигации выберите **Настройки клиента**, чтобы развернуть их.
1. В разделе **Настройки клиента** выберите **Настройка аутентификации сайта**. 
1. В главном окне рядом с элементом **Профили аутентификации сайтов** выберите **Управление**. (Если клиент отображается в списке профилей аутентификации сайтов, то он уже добавлен администратором. Убедитесь, что элементы на шаге 6 ниже соответствуют элементам для вашей желаемой установки приложения B2C. Новый профиль также может быть создан с помощью аналогичных клиентов Azure AD B2C или приложений для учета небольших отличий, например, различных идентификаторов политик пользователя).
1. Выберите **Добавить профиль аутентификации сайта**.
1. Введите следующие необходимые пункты в отображаемой форме, используя значения из клиента B2C и приложения. Поля, которые не являются обязательными (без звездочки), могут быть оставлены пустыми.

    - **Имя приложения**: имя вашего приложения B2C, например "Fabrikam B2C".
    - **Имя клиента**: имя вашего B2C-клиента (например, "Fabrikam", если домен отображается как "fabrikam.onmicrosoft.com" для клиента B2C). 
    - **Код политики сброса пароля**: идентификатор политики потока пользователей для сброса пароля, например "B2C_1_PasswordReset".
    - **Идентификатор политики регистрации или входа**: идентификатор политики потока пользователей для входа и регистрации, например "B2C_1_signup_signin".
    - **Идентификатор GUID клиента**: идентификатор приложения B2C, например "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".
    - **Идентификатор политики изменения профиля**: идентификатор политики потока пользователя для редактирования профиля, например "B2C_1A_ProfileEdit".

1. Нажмите **ОК**. Теперь в списке должно отображаться имя приложения B2C.
1. Выберите **Сохранить** для сохранения изменений.

Необязательное поле **Пользовательский домен для входа** должно использоваться только при настройке пользовательского домена для клиента Azure AD B2C. Дополнительные сведения и замечания, касающиеся использования поля **Пользовательский домен для входа**, см. в разделе [Дополнительные сведения о B2C](additional-b2c-info.md).

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a>Связь приложения B2C с сайтом и каналом

> [!WARNING]
> - Если сайт уже связан с приложением B2C, при переходе к другому приложению B2C будут удалены текущие ссылки, установленные для пользователей, уже зарегистрированных в этой среде. При изменении все учетные данные, связанные с назначенным в данный момент приложением B2C, будут недоступны пользователям. 
> - Обновляйте приложение B2C только в том случае, если выполняется первая настройка приложения B2C канала или если требуется, чтобы пользователи повторно зарегистрировались с новыми учетными данными в этом канале с новым приложением B2C. Соблюдайте осторожность при связывании каналов с приложениями B2C и давайте приложениям понятные названия. Если канал не связан с приложением B2C в приведенных ниже шагах, пользователи, вошедшие в этот канал для вашего сайта, будут входить в приложение B2C, которое отображается как **по умолчанию** в списке **Параметры клиента \> Параметры B2C** приложений B2C.

Чтобы связать приложение B2C с сайтом и каналом, выполните следующие действия.

1. Перейдите на свой сайт в конфигураторе сайта Commerce.
1. На левом панели навигации выберите **Настройки сайта**, чтобы развернуть.
1. В разделе **Параметры сайта** выберите **Каналы**.
1. В главном окне в разделе **Каналы** выберите свой канал.
1. В правой панели свойств канала выберите имя приложения B2C в раскрывающемся меню **Выбор приложения B2C**.
1. Выберите **Закрыть**, затем выберите **Сохранить и опубликовать**.

## <a name="next-steps"></a>Далее

Чтобы продолжить процесс настройки клиента B2C в Commerce, переходите к разделу [Дополнительные сведения B2C](additional-b2c-info.md).

## <a name="additional-resources"></a>Дополнительные ресурсы

[Настройка клиента B2C в Commerce](set-up-b2c-tenant.md)

[Создание или связывание существующего клиента Azure AD B2C с порталом Azure](create-link-aad-b2c-tenant.md)

[Создание приложения B2C](create-b2c-app.md)

[Создание политик потока пользователей](create-user-flow-policies.md)

[Добавление поставщиков удостоверений в социальных сетях (дополнительно)](add-social-identity-providers.md)

[Обновление Commerce headquarters с учетом новой информации Azure AD B2C](update-hq-aad-b2c-info.md)

[Дополнительные сведения B2C](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]