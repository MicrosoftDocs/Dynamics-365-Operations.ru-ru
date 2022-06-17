---
title: Отключение правил, используемых в процессе проверки проводок
description: В этой статье описывается функция отключения правил проверки проводок в Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 12/11/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7d566aa3b829dad281528925a341382f9637fdba
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884886"
---
# <a name="disable-rules-used-in-the-transaction-validation-process"></a>Отключение правил, используемых в процессе проверки проводок

[!include [banner](../includes/banner.md)]

Многие розничные компании используют уникальные бизнес-сценарии и процессы. Поэтому не все правила, включенные в процесс проверки проводок Commerce, применимы ко всем предприятиям розничной торговли. Для учета этих различий в Microsoft Dynamics 365 Commerce предусмотрена возможность отключения неприменимых правил.

Чтобы просмотреть список правил, доступных в процессе проверки проводок в среде, и статус каждого правила, перейдите в раздел **Retail и Commerce \> Настройка центрального офиса \> Параметры \> Параметры Commerce** и выберите вкладку **Проверка проводок**. Все включенные правила используются для проверки проводок в процессе **Проверить проводки магазина** и должны быть соблюдены, чтобы проводки были собраны и разнесены в журнал проводок.

По умолчанию каждое правило имеет статус **Включено**. Поэтому для проверки проводок перед их передачей в журналы проводок Commerce используются все правила. Чтобы отключить правило, измените его статус на **Отключено**. Отключенные правила не используются при проверке проводок в процессе **Проверить проводки магазина**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
