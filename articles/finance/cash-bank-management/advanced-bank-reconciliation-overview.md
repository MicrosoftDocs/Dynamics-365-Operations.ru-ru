---
title: Обзор расширенной банковской выверки
description: Эта статья описывает поток для предварительного процесса банковской выверки. Функция расширенной банковской выверки позволяет импортировать банковские выписки, которые можно автоматически выверять из банковских проводок.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 39ddfde74aaff8bf5d8f22861b7595be1f9b89a9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179623"
---
# <a name="advanced-bank-reconciliation-overview"></a>Обзор расширенной банковской выверки

[!include [banner](../includes/banner.md)]

Эта статья описывает поток для предварительного процесса банковской выверки. Функция расширенной банковской выверки позволяет импортировать банковские выписки, которые можно автоматически выверять из банковских проводок.

Функция расширенной банковской выверки позволяет вам импортировать банковские выписки. Импортированную банковскую выписку можно после этого автоматически выверить их банковских проводок. Вот шаги процесса расширенной банковской выверки.

1.  Настройка импорта банковской выписки.
    -   Импортируйте банковские выписки через структуру информационного объекта.
    -   Встроены три типичных формата банковской выписки: ISO20022, BAI2 и MT940.
    -   Функциональность можно расширить до любого формата.

2.  Настройте номерную серию для использования для расширенной банковской выверки, и определите правила сопоставления банковской выверки.
    -   Правило сопоставления выверки — это набор критериев, используемых при фильтрации строк банковской выписки и строк банковской проводки Microsoft Dynamics 365 Finance во время процесса выверки. В зависимости от вашей методики ведения бизнеса можно настроить более одного правила сопоставления, чтобы автоматизировать и оптимизировать процесс сверки.

3.  Выверите банковские выписки с банковскими проводками Finance.
    -   Выполните автоматические сопоставление и создание журналов выверки.
    -   Просмотр банковских выписок с банковскими проводками Finance друг рядом с другом.
    -   Автоматическая разноска банковских проводок Finance, если они появляются в банковской выписке, но не появились в приложении Finance.
    -   Создать выписку выверки.




