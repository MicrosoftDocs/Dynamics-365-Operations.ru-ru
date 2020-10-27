---
title: Проверка пользовательского сертификата NF-e
description: В этой теме приводятся сведения о включении и использовании пользовательского сертификата NF-e.
author: gionoder
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 26ffed1f49d9087ca767aab1b8cac41b099f73cb
ms.sourcegitcommit: 3c88c4adafb78b807842b0b41c69b19cf2b7aa23
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2020
ms.locfileid: "3973100"
---
# <a name="nf-e-custom-certificate-validation"></a>Проверка пользовательского сертификата NF-e

[!include [banner](../includes/banner.md)]

При включении функции проверки пользовательских сертификатов NF-e пользовательская проверка разрешает подключение к веб-службам. Это подключение требуется для передачи NF-e и получения авторизации от SEFAZ.

Свойство **Цель проверки подлинности сервера** из сертификата V5 выдается корневым центром сертификации Бразилии. По умолчанию это свойство отключено, и оно должно быть включено вручную. В некоторых обстоятельствах автоматическое обновление сертификатов может переключать это свойство, чтобы оно больше не было включено. В этом случае виновато TLS-подключение, и оно больше не является доверенным. Также затрагивается возможность выпуска NF-e в производственных средах для штатов Minas Gerais (MG) и Paraná (PR).

Это обновление предоставляет альтернативное решение для проверки сертификатов, что означает возможность установления безопасного подключения.


