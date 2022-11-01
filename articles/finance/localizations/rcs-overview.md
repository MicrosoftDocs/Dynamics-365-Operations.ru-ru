---
title: Regulatory Configuration Service
description: В этой статье представлен обзор возможностей службы Regulatory Configuration Service (RCS) и объясняется, как получить доступ к этой службе.
author: kfend
ms.date: 06/04/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
ms.openlocfilehash: c04b13ef05424b27b5abcc2ac7490a7b75797bf5
ms.sourcegitcommit: c6c2486be2359bd30106f7f52bda788239147d8c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/22/2022
ms.locfileid: "9713931"
---
# <a name="regulatory-configuration-service"></a>Regulatory Configuration Service

[!include [banner](../includes/banner.md)]

Служба Regulatory Configuration Service (RCS) — это изолированный конструктор и служба управления жизненным циклом для функций глобализации без кода/мало кода. RCS позволяет заинтересованным сторонам глобализации расширять и настраивать ключевые области глобализации, такие как налогообложение, электронное выставление накладных, нормативная отчетность, банковские операции и бизнес-документы, без необходимости привлечения разработчиков. Такой подход к глобализации без кода/мало кода упрощает работу с глобализацией и повышает эффективность создания и расширения.

RCS обеспечивает следующие возможности:

- Поддержка всех функций, предоставляемых электронной отчетностью (ER).
- Необходимое условие для настройки новых микрослужб глобализации.
- Поддержка электронного выставления накладных. Дополнительные сведения см. в [Электронное выставление накладных](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).
- Поддержка расчета налогов. Дополнительные сведения см. в [Служба налогообложения](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).
- Поддержка новых функциональных возможностей глобализации, которая упрощает управление многокомпонентными возможностями и предоставляет дополнительные возможности для настройки действий и настройки параметров функций. Дополнительные сведения см. в [Служба Regulatory Configuration Service — упрощенное управление функциями глобализации для служб глобализации](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).
- Поддержка централизованной публикации, хранения и совместного использования пользовательских конфигураций в глобальном репозитории для упрощения управления конфигурацией без необходимости использования Microsoft Dynamics Lifecycle Services (LCS).

## <a name="access-rcs"></a>Доступ к RCS

Вы можете зарегистрироваться или войти в RCS на [странице Служба Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).

![Регистрация/вход в RCS.](media/202103_RCS%20Marketing%20page_updated_1.jpg)

На странице **Служба Regulatory Configuration Service** проверьте и примите дополнительные условия использования службы, а затем выберите одну из следующих кнопок:

- **Регистрация**, если вы впервые пользуетесь службой и используете рабочий адрес электронной почты для предоставления вашей организации среды службы
- **Вход**, если вы ранее зарегистрировались в службе, и вам необходимо получить доступ к корпоративной среде

> [!NOTE] 
> После регистрации рекомендуется добавить в среду RCS нового пользователя-системного администратора. Этот пользователь будет подготовлен для совместного администрирования среды. Это поможет обеспечить стабильность доступа к среде RCS, так как роль системного администратора используется для управления пользователями этой среды. Можно добавлять пользователей с помощью **Рабочая область RCS > Администрирование системы**.

## <a name="regional-availability"></a>Региональная доступность

RCS обычно доступен в следующих регионах:

- США
- Индия
- Франция
- Европа

Полный список регионов см. в [Dynamics 365 и Power Platform: доступность, расположение данных, язык и локализация](https://aka.ms/dynamics_365_international_availability_deck).

> [!NOTE] 
> RCS в настоящее время недоступен для облака сообщества для государственных организаций (GCC).

## <a name="rcs-default-company"></a>Компания по умолчанию RCS

Функция времени разработки, используемая в RCS, используется совместно всеми компаниями. Нет функциональности, специфической для компании. Поэтому рекомендуется использовать одну компанию, **DAT**, со средой RCS.

Однако в некоторых сценариях можно задать, чтобы форматы электронной отчетности использовали параметры, связанные с определенным юридическим лицом. Только в этих сценариях следует использовать переключатель компании по умолчанию. Например, см. раздел [Настройка формата электронной отчетности для использования параметров, указанных для юридического лица](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).

## <a name="related-rcs-documentation"></a>Документация, связанная с RCS

Дополнительные сведения о связанных компонентах см. в следующих темах:

- **RCS:**

    - [Создание конфигураций электронной отчетности в RCS и их отправка в глобальный репозиторий](rcs-global-repo-upload.md)

- **Глобальный репозиторий:**

    - [Создание конфигурации электронной отчетности и загрузка в глобальный репозиторий](rcs-global-repo-upload.md)
    - [Общая конфигурация в глобальном репозитории](rcs-global-repo-share-configuration.md)
    - [Улучшенная фильтрация в глобальном репозитории](enhanced-filtering-global-repo.md)
    - [Загрузка конфигураций электронной отчетности из глобального репозитория](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [Прекращение использования конфигураций в глобальном репозитории](discontinuing-configurations-rcs-global-repo.md)
    - [Regulatory Configuration Service (RCS) — устаревание хранилища Lifecycle Services (LCS)](rcs-lcs-repo-dep-faq.md)

- **Функция глобализации:**

    - [Regulatory Configuration Service (RCS) — функции глобализации](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)


## <a name="troubleshooting-rcs-sign-up"></a>Устранение неполадок регистрации в RCS

При регистрации на RCS со страницы обслуживания может возникнуть проблема, связанная с Azure Active Directory (Azure AD). Полученное сообщение об ошибке указывает на то, что регистрация на RCS в данный момент отключена и должна быть включена, прежде чем можно будет завершить процесс регистрации.

![Сообщение об ошибке при регистрации RCS.](media/01_RCSSignUpError.jpg)

Проблема возникает из-за того, что вы не можете регистрироваться на нерегламентированные подписки, и свойство `AllowAdHocSubscriptions` должно быть включено в клиенте. 

- Если ИТ-отдел управляет клиентами Azure вашей организации, свяжитесь с этим подразделением, чтобы сообщить о проблеме.
- Если вы отвечаете за управление вашими клиентами Azure, вы можете решить эти проблемы, выполнив шаги, указанные в разделе [Что такое регистрация самообслуживания для Azure Active Directory](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).
