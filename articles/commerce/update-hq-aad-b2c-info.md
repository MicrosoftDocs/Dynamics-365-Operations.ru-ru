---
title: Обновление центрального офиса Commerce с учетом новой информации Azure AD B2C
description: В этой статье описывается, как обновить Microsoft Dynamics 365 Commerce headquarters с новой информацией Azure Active Directory (Azure AD) "бизнес-клиент" (B2C).
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: c65949ff97182d2692319ac2af00e3ef35a79580
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785326"
---
# <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a>Обновление центрального офиса Commerce с учетом новой информации Azure AD B2C

[!include [banner](includes/banner.md)]

В этой статье описывается, как обновить Microsoft Dynamics 365 Commerce headquarters с новой информацией Azure Active Directory (Azure AD) "бизнес-клиент" (B2C).

После завершения приведенных выше шагов по подготовке Azure AD B2C, приложение Azure AD B2C должно быть зарегистрировано в вашей среде Dynamics 365 Commerce.

Чтобы обновить штаб-квартиру с новыми сведениями Azure AD B2C, выполните следующие действия.

1. В модуле Commerce перейдите на страницу **Общие параметры Commerce** и выберите пункт **Поставщики удостоверений** в меню слева.
1. В разделе **Поставщики удостоверений** выполните следующие действия:
    1. В поле **Издатель** введите строку издателя поставщика удостоверений. Чтобы найти строку издателя, см. раздел [Получение строки издателя для настройки центрального офиса](#obtain-issuer-string-for-headquarters-setup) ниже.
    1. В поле **Имя** введите имя для записи издателя.
    1. В поле **Тип** введите **Azure AD B2C (id_token)**.
1. В разделе **Зависимые стороны** с выбранным выше пунктом поставщика удостоверений B2C выполните следующие действия:
    1. В поле **ClientID** введите код приложения B2C, который можно найти в поле **Код приложения** на странице свойств приложения B2C.
    1. В поле **Тип** введите **Общий**.
    1. В поле **Тип пользователя** введите **Клиент**.
1. На панели операций выберите **Сохранить**.
1. В поле поиска Commerce выполните поиск **График распределения**
1. В левом меню навигации на странице **Графики распределения** выберите задание **1110 Глобальная конфигурация**.
1. В области действий выберите **Выполнить сейчас**.

### <a name="obtain-issuer-string-for-headquarters-setup"></a>Получение строки издателя для настройки центрального офиса

Чтобы получить строку издателя поставщика удостоверений, выполните следующие действия.

1. На странице Azure AD B2C портала Azure перейдите к потоку пользователей **Регистрация и вход**.
1. Выберите **Макеты страниц** в левом меню переходов, в разделе **Имя макета** выберите **Унифицированная страница регистрации или входа**, затем выберите **Выполнить поток пользователей**.
1. Убедитесь, что ваше приложение настроено на требуемое приложение Azure AD B2C, созданное выше, затем выберите ссылку потока пользователей, которая отображается в заголовке **Выполнить поток пользователей**, которая включает ``.../.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``. (Не выбирайте **Выполнение потока пользователей**.) Откроется новая вкладка, в которой будут отображены метаданные для политики для сбора строки издателя.
1. На странице метаданных, отображаемой на вкладке обозревателя, скопируйте строку издателя поставщика удостоверений (значение для **издателя**, начинающееся с "https://" и заканчивающееся на "/v2.0/"), которая выглядит примерно следующим образом:
   - ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.
 
**ИЛИ**: чтобы создать тот же URL-адрес метаданных вручную, выполните следующие действия.

1. Создайте URL-адрес метаданных в следующем формате, используя клиент B2C и политику: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``
    - Пример: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.
1. Введите URL-адрес метаданных в адресную строку браузера.
1. В метаданных скопируйте URL-адрес издателя поставщика удостоверений (значение для **"издатель"**).
    - Пример: ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.

## <a name="next-steps"></a>Далее

Чтобы продолжить процесс настройки клиента B2C в модуле Commerce, переходите к разделу [Настройка клиента B2C в конфигураторе сайта Commerce](config-b2c-tenant-site-builder.md).

## <a name="additional-resources"></a>Дополнительные ресурсы

[Настройка клиента B2C в Commerce](set-up-b2c-tenant.md)

[Создание или связывание существующего клиента Azure AD B2C с порталом Azure](create-link-aad-b2c-tenant.md)

[Создание приложения B2C](create-b2c-app.md)

[Создание политик потока пользователей](create-user-flow-policies.md)

[Добавление поставщиков удостоверений в социальных сетях (дополнительно)](add-social-identity-providers.md)

[Настройка клиента B2C в конфигураторе сайта Commerce](config-b2c-tenant-site-builder.md)

[Дополнительные сведения B2C](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
