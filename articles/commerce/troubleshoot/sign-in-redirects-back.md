---
title: Ссылка для входа перенаправляет обратно на сайт электронной коммерции
description: В этой статье содержатся указания по устранению неполадок, которые могут помочь при переадресации ссылки входа на сайт электронной коммерции вместо перехода на страницу входа.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5274599ee5ea23c18648d95431b2e79ebca12dea
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860226"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a>Ссылка для входа перенаправляет обратно на сайт электронной коммерции

[!include [banner](../../includes/banner.md)]

В этой статье содержатся указания по устранению неполадок, которые могут помочь при переадресации ссылки входа на сайт электронной коммерции вместо перехода на страницу входа.

## <a name="description"></a>описание

После того, как вы настроили новый клиент B2C Microsoft Azure Active Directory (Azure AD B2C) в конструкторе сайтов Commerce, пользователи, выбравшие ссылку **Войти**, перенаправляются назад на основную целевую страницу электронной коммерции без перехода на страницу входа.

## <a name="resolution"></a>Приказ

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a>Убедитесь, что URL-адрес ответа правильно настроен в приложении Azure AD B2C

Чтобы убедиться, что URL-адрес ответа правильно настроен в приложении Azure AD B2C, выполните следующие действия.

1. Перейдите в раздел [порталу Azure](https://portal.azure.com/).
1. Выберите приложение Azure AD B2C, созданное для доступа к сайту.
1. Выберите приложение, которое было создано во время настройки Azure AD B2C.
1. В разделе **URL-адрес ответа** убедитесь, что в списке имеются записи как для URL-адреса домена сайта, так и для URL-адреса, созданного в электронной коммерции, как показано в примере на следующем рисунке.

    ![Записи URL-адресов ответа Azure AD B2C.](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> URL-адрес домена сайта и созданный в электронной коммерции URL-адрес должны иметь допустимый формат URL-адреса, не включающий начальную и заключительную косую черту.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Регистрация веб-приложения в Azure Active Directory B2C](/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[Настройка клиента B2C в модуле Commerce](../set-up-b2c-tenant.md)