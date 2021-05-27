---
title: Regulatory Configuration Service
description: В этом разделе представлен обзор возможностей службы Regulatory Configuration Service (RCS) и объясняется, как получить доступ к службе.
author: JaneA07
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 1eeac7217290e0583fcecdf5b4b5b9153d266240
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019402"
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

![Регистрация/вход в RCS](media/202103_RCS%20Marketing%20page_updated_1.jpg)

На странице **Служба Regulatory Configuration Service** проверьте и примите дополнительные условия использования службы, а затем выберите одну из следующих кнопок:

- **Регистрация**, если вы впервые пользуетесь службой и используете рабочий адрес электронной почты для предоставления вашей организации среды службы
- **Вход**, если вы ранее зарегистрировались в службе, и вам необходимо получить доступ к корпоративной среде

## <a name="regional-availability"></a>Региональная доступность

RCS обычно доступен в следующих регионах:

- США
- Индия
- Франция
- Европа

Полный список регионов см. в [Dynamics 365 и Power Platform: доступность, расположение данных, язык и локализация](https://aka.ms/dynamics_365_international_availability_deck).

## <a name="related-rcs-documentation"></a>Документация, связанная с RCS

Дополнительные сведения о связанных компонентах см. в следующей документации:

- **Глобальный репозиторий:**

    - [Создание конфигурации электронной отчетности и загрузка в глобальный репозиторий](rcs-global-repo-upload.md)
    - [Общая конфигурация в глобальном репозитории](rcs-global-repo-share-configuration.md)
    - [Улучшенная фильтрация в глобальном репозитории](enhanced-filtering-global-repo.md)
    - [Загрузка конфигураций электронной отчетности из глобального репозитория](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [Прекращение использования конфигураций в глобальном репозитории](discontinuing-configurations-rcs-global-repo.md)

- **Функция глобализации:**

    - [Regulatory Configuration Service (RCS) — функции глобализации](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)