---
title: Настройка сред службы и подключенных приложений
description: В этой теме приводятся сведения о настройке сред служб и подключенных приложений.
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c3366e75b4a6d3f33a1aac9e444236d9ae57c829
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371734"
---
# <a name="configure-service-environments-and-connected-applications"></a>Настройка сред службы и подключенных приложений

[!include [banner](../includes/banner.md)]

В этой теме приводятся сведения о настройке сред служб и подключенных приложений. Для этого процесса необходимо выполнить три шага. Шаг 1 является обязательным, а шаги 2 и 3 необязательны.

## <a name="step-1-create-a-service-environment"></a>Шаг 1. Создание среды службы

При создании среды службы необходимо определить список пользователей, которые могут развертывать в ней функции глобализации. Дополнительно, для некоторых сценариев необходимо определить список внешних приложений, которые могут взаимодействовать со службой электронного выставления накладных. Настройте номерные серии, если они будут использоваться в сценариях.

Чтобы выполнить этот шаг, см. раздел [Среды служб](e-invoicing-service-environments.md).

## <a name="step-2-add-certificates-and-secrets"></a>Шаг 2. Добавление сертификатов и секретов

Добавьте ссылку на хранилище ключей и секреты Microsoft Azure, чтобы использовать их в ваших сценариях. Этот шаг является обязательным, если действия в конвейерах обработки используют сертификаты и секреты для цифровой подписи или для связи с внешними веб-службами.

Чтобы выполнить этот шаг, см. раздел [Сертификаты и секреты клиентов](e-invoicing-customer-certificates-secrets.md).

## <a name="step-3-configure-connected-applications"></a>Шаг 3. Настройка связанных приложений

Для настройки обмена данными между приложениями Dynamics 365 Finance или Dynamics 365 Supply Chain Management и электронным выставлением накладных необходимо настроить Finance или Supply Chain Management для создания вызова службы электронного выставления накладных и подготовки деловых данных в единой структуре, которая может быть преобразована в нужный электронный формат. Кроме того, приложения должны правильно обрабатывать отклики от службы. Эту конфигурацию можно выполнить непосредственно в среде Finance или Supply Chain Management, либо можно выполнить ее в службе Regulatory Configuration Service (RCS). В случае выполнения конфигурации в RCS можно затем развернуть ее в среде Finance или Supply Chain Management. На этом шаге выполняется регистрация подключенного приложения для развертывания параметров.

Чтобы выполнить этот шаг, см. раздел [Подключенные приложения](e-invoicing-connected-applications.md).
