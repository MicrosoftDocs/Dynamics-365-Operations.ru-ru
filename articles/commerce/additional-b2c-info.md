---
title: Дополнительные сведения B2C
description: В этой статье приводятся дополнительные сведения о том, как настроить клиент "бизнес-клиент" (B2C) в Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/14/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: b60ef15544cd30c44968ee7a588a8a9fb08e8223
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785272"
---
# <a name="additional-b2c-information"></a>Дополнительные сведения B2C

[!include [banner](includes/banner.md)]

В этой статье приводятся дополнительные сведения о том, как настроить клиент "бизнес-клиент" (B2C) в Microsoft Dynamics 365 Commerce.

### <a name="customer-migration"></a>Миграция клиентов

Если вы собираетесь выполнить миграцию записей клиентов из предыдущей платформы поставщика удостоверений, работайте с рабочей группой Dynamics 365 Commerce, чтобы проверить свои потребности по миграции клиентов.

Дополнительную документацию Azure AD B2C по миграции клиентов см. в разделе [Миграция пользователей в Azure Active Directory B2C](/azure/active-directory-b2c/active-directory-b2c-user-migration).

### <a name="custom-policies"></a>Пользовательские политики

Дополнительные сведения о настройке взаимодействий Azure AD B2C и лежащих в основе потоках политик, предлагаемых стандартными политиками B2C, см. раздел [Пользовательские политики в Azure Active Directory B2C](/azure/active-directory-b2c/active-directory-b2c-overview-custom). 

### <a name="secondary-admin"></a>Дополнительный администратор

При необходимости учетная запись дополнительного администратора может быть добавлена в разделе **Пользователи** вашего клиента B2C. Это может быть прямая учетная запись или общая учетная запись. Если необходимо сделать учетную запись общей для нескольких ресурсов группы, также может быть создана общая учетная запись. В связи с чувствительностью данных, хранящихся в Azure AD B2C, следует внимательно отслеживать общую учетную запись в соответствии с политиками безопасности компании.

### <a name="set-up-a-custom-sign-in-domain"></a>Настройка пользовательского домена для входа

Azure AD B2C позволяет настроить пользовательский домен для входа для клиента Azure AD B2C. Инструкции см. в разделе [Включение пользовательских доменов для Azure Active Directory B2C](/azure/active-directory-b2c/custom-domain). 

При использовании настраиваемого домена для входа домен должен быть введен в построитель сайтов Commerce.

Чтобы ввести настраиваемый домен для входа в построителе сайтов, выполните следующие действия.

1. В верхнем правом углу построителя сайтов выберите переключатель сайтов, а затем выберите **Управление сайтами**.
1. В левой области навигации выберите **Настройки клиента \> Настройка аутентификации сайта**.
1. В разделе **Профили аутентификации сайта** выберите **Управление**.
1. В раскрывающемся меню справа нажмите кнопку **Изменить** (символ карандаша) рядом с профилем аутентификации сайта, для которого необходимо ввести пользовательский домен.
1. В диалоговом окне **Изменить профиль аутентификации сайта** в разделе **Пользовательский домен для входа** введите свой пользовательский домен для входа (например, "login.fabrikam.com").

> [!WARNING]
> При обновлении личного домена для клиента Azure AD B2C это изменение повлияет на сведения о поставщике клиента для созданного маркера. Затем в сведения о поставщике будет включен личный домен, а не домен по умолчанию, предоставляемый службой Azure AD B2C. Другая конфигурация **Поставщик** в Commerce headquarters (**Розничная торговля и коммерция \> Настройка Headquarters \> Параметры \> Общие параметры Commerce \> Поставщики удостоверений**) изменяет взаимодействие системы с пользователями сайта, потенциально создавая новую запись клиента, если пользователь выполняет аутентификацию для нового поставщика. Любые изменения личного домена следует тщательно протестировать, прежде чем переходить на личный домен в рабочей среде B2C Azure AD.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Настройка клиента B2C в Commerce](set-up-b2c-tenant.md)

[Создание или связывание существующего клиента Azure AD B2C с порталом Azure](create-link-aad-b2c-tenant.md)

[Создание приложения B2C](create-b2c-app.md)

[Создание политик потока пользователей](create-user-flow-policies.md)

[Добавление поставщиков удостоверений в социальных сетях (дополнительно)](add-social-identity-providers.md)

[Обновление Commerce headquarters с учетом новой информации Azure AD B2C](update-hq-aad-b2c-info.md)

[Настройка клиента B2C в конфигураторе сайта Commerce](config-b2c-tenant-site-builder.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]