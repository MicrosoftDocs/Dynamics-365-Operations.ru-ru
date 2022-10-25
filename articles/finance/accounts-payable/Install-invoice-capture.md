---
title: Установка решения Invoice Capture
description: В этой статье приводятся сведения о том, как установить решение Invoice Capture и интегрировать его с Microsoft Dynamics 365 Finance.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: d853e347c833345f34b65760fd7ee35cbb38c9a3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691227"
---
# <a name="install-the-invoice-capture-solution"></a>Установка решения Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Если решение было установлено на этапе предварительной версии, перед продолжением необходимо удалить старое решение.

## <a name="prerequisites"></a>Необходимые условия

Перед установкой решения Invoice Capture необходимо выполнить следующие требования:

1. Зарегистрируйте приложение и добавьте секрет клиента в Microsoft Azure Active Directory (Azure AD) в своей подписке Azure. Дополнительные сведения см. в разделе [Регистрация веб-приложения в AAD](../../dev-itpro/data-entities/services-home-page.md#register-a-web-application-with-aad).

    > [!NOTE]
    > Запишите значения **Идентификатор приложения (клиента)**, **Секрет клиента** и **Идентификатора арендатора**, так как они понадобятся позже.

2. Зарегистрируйте приложение Azure в среде Dynamics 365 Finance. Дополнительные сведения см. в разделе [Регистрация внешнего приложения](../../dev-itpro/data-entities/services-home-page.md#register-your-external-application).

## <a name="install-and-set-up-the-solution"></a>Установка и настройка решения

Чтобы установить решение Invoice Capture, перейдите в AppSource и выберите ссылку для предварительной версии [Dynamics 365 Invoice Capture](https://appsource.microsoft.com/product/dynamics-365/mscrm.dynamics365-invoice-capture-preview?flightCodes=invoicecapture). После завершения установки будет отображено решение, установленное в выбранной среде в Power Apps.

Чтобы завершить настройку, выполните следующие действия.

1. Загрузите [решение помощника](https://github.com/InvoiceCapture/InstallationTools/releases/download/latest/msdyn_InvoiceCaptureIntallationTools.zip), чтобы настроить следующие сведения:

    - Связь между Microsoft Power Platform и средой Finance
    - Ссылка на подключение для Dataverse и Office 365 Outlook, которое будет использоваться в канале

2. В Power Apps откройте среду и выберите **Импорт решения**.
3. Выберите **Обзор**, выберите загруженный пакет решения помощника и затем выберите **Далее**.
4. Выберите **Далее**.
5. Назначьте существующее подключение или создайте новое путем выбора **Создать подключение**.
6. После успешного импорта пакета откройте **Dynamics 365 Invoice Capture — инструменты установки**.
7. Выполните облачный поток для настройки подключения между решением Invoice Capture в Microsoft Power Platform и Finance.
8. Выберите **Выполнить** и укажите следующие параметры:

    - **URL-адрес Dynamics 365 Finance** — URL-адрес среды Finance, с которой требуется выполнить интеграцию.
    - **Код арендатора** — код арендатора для среды Finance.
    - **Код клиента** — зарегистрированный идентификатор приложения Azure.
    - **Секрет клиента** — секрет клиента, созданный для приложения Azure.
