---
title: Регистрация и установка службы электронного выставления накладных
description: В этой статье содержится информация о том, как зарегистрироваться и установить службу "Электронное выставление накладных".
author: gionoder
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 99f484e5ab8821c78fde776a9d3195dade2a09d5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283968"
---
# <a name="sign-up-for-and-install-the-electronic-invoicing-service"></a>Регистрация и установка службы электронного выставления накладных

[!include [banner](../includes/banner.md)]

В этой статье содержится информация о том, как зарегистрироваться и установить службу "Электронное выставление накладных". Для этого процесса необходимо выполнить четыре шага. Шаги с 1 по 3 являются обязательными, а шаг 4 — необязательным.

### <a name="step-1-sign-up-for-regulatory-configuration-service"></a>Шаг 1. Регистрация на службу Regulatory Configuration Service

Служба Regulatory Configuration Service (RCS) предоставляет интерфейс конфигурации и разработки, который используется для настройки электронного выставления счетов. Ресурсы, такие как среды и функции электронного выставления накладных, создаются, поддерживаются и управляются в RCS. Когда ресурсы готовы, они публикуются в службе электронного выставления накладных.

Дополнительные сведения об RCS см. в разделе [Regulatory Configuration Services (RCS) — функции глобализации](rcs-globalization-feature.md).

Чтобы зарегистрироваться на RCS, перейдите на страницу [Служба Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).

### <a name="step-2-install-the-add-in-for-microservices-in-microsoft-dynamics-lifecycle-services"></a>Шаг 2. Установка надстройки для микрослужб в Microsoft Dynamics Lifecycle Services

Служба электронного выставления накладных — это набор микрослужб, размещенных в центрах обработки данных Microsoft. По умолчанию клиенты Dynamics 365 Finance и Dynamics 365 Supply Chain Management не имеют доступа к службе электронного выставления накладных. Необходимо установить его в качестве надстройки в службы Microsoft Dynamics Lifecycle Services (LCS). При установке надстройки среда Finance или Supply Chain Management регистрируется в регистре приложений, которые могут подключиться к службе электронного выставления накладных.

Чтобы выполнить этот шаг, см. раздел [Установка надстройки для микрослужб в Lifecycle Services](e-invoicing-install-add-in-microservices-lcs.md).

### <a name="step-3-set-up-rcs"></a>Шаг 3. Настройка RCS

Необходимо настроить интеграцию между RCS и службой электронного выставления накладных. Также необходимо настроить основные компоненты.

Чтобы выполнить этот шаг, см. раздел [Настройка службы Regulatory Configuration Service (RCS)](e-invoicing-set-up-rcs.md).

### <a name="step-4-microsoft-power-platform-plug-in-admin-reference"></a>Шаг 4. Ссылка администратора подключаемого модуля Microsoft Power Platform

Для некоторых сценариев требуется интеграция с Dataverse в области Microsoft Power Platform.

В настоящее время эта настройка является обязательной, если используются решения электронного выставления накладных для сценариев выставления электронных накладных для Индонезии. Однако это необязательно для сценариев выставления электронных накладных для Саудовской Аравии. Дополнительные сведения см. в разделе [Доступность функций электронного выставления накладных по странам или регионам](e-invoicing-country-specific-availability.md).

Для выполнения этого шага см. раздел [Справочник администратора подключаемого модуля Microsoft Power Platform](e-invoicing-power-platform-plug-in.md).
