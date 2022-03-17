---
title: Пустой список налоговых функций в параметрах налогового расчета
description: В этой теме описывается, как устранять неполадки, когда список налоговых функций на странице параметров расчета налогов пуст.
author: wangchen
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 5b87499042c9c4bfe76e182b170adf4f1cfeac4b
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388564"
---
# <a name="empty-tax-feature-list-in-tax-calculation-parameters"></a>Пустой список налоговых функций в параметрах налогового расчета

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="symptom"></a>Проблема

Вы опубликовали функцию в службе Regulatory Configuration Service (RCS), чтобы можно было использовать ее в Microsoft Dynamics 365 Finance. Однако, когда вы откроете Finance, перейдете в раздел **Налог** \> **Настройка** \> **Конфигурация налогов** \> **Конфигурация налогов** и попробуете выбрать значение в поле **Имя настройки функции**, список значений будет пустым.

## <a name="reason"></a>Основание

Эта проблема обычно возникает, потому что среда Finance и среда RCS не находятся в одном и том же клиенте.

### <a name="rcs-tenant"></a>Клиент RCS

Выполните следующие действия, чтобы найти идентификатор клиента RCS.

1. Скопируйте полный URL-адрес RCS. Например, может быть указан URL-адрес `https://rcs-rts-sf-ed22b5aeea8-int-westus2.configure.global.int.dynamics.com/namespaces/817ff7a0-0d77-4aba-9360-3c9749e2c5de/?cmp=dat&mi=RCSFeatureDomainsWorkspace`.
2. Откройте окно браузера в режиме InPrivate, вставьте URL-адрес RCS в адресную строку и выберите **Ввод**. Вы направляетесь на страницу входа, где можно найти идентификатор клиента RCS. Например, если URL-адрес страницы входа имеет значение `https://login.microsoftonline.com/d335a570-a05b-4bc5-8eb3-c42c65f9560d`, идентификатор клиента — это информация, которая появляется после `https://login.microsoftonline.com/` или **d335a570-a05b-4bc5-8eb3-c42c65f9560d**.

### <a name="finance-environment-tenant-id"></a>Код клиента среды Finance

Чтобы найти идентификатор клиента для среды Finance, выполните те же действия, которые были выполнены при поиске клиента RCS. Однако необходимо скопировать и вставить полный URL-адрес среды Finance вместо полного URL-адреса RCS.

## <a name="resolution"></a>Решение

Если два идентификатора клиентов различаются, то вы столкнулись с проблемой, описанной в этой теме. Если они одинаковы, вы столкнулись с другой проблемой, не связанной с этой. В этом случае рекомендуется обратиться в службу поддержки Майкрософт.

### <a name="solution-1"></a>Решение 1

Войдите в вашу среду RCS в том же клиенте, на котором выполняется вход в среду Finance. Затем создайте и опубликуйте функцию налога.

### <a name="solution-2"></a>Решение 2

Поделитесь функцией налогообложения с клиентом Finance в RCS.

1. В RCS перейдите в **Функции глобализации** \> **Расчета налога**.
2. Выберите функцию, к которой необходимо предоставить общий доступ, затем на вкладке **Организации** выберите **Поделиться**.
3. В поле **Имя домена организации** введите имя. Например, введите **contoso.onmicrosoft.com**.
4. Выберите **Поделиться**.

![Раскрывающееся диалоговое окно общего доступа для внешней организации.](media/ShareTaxFeature.png)
