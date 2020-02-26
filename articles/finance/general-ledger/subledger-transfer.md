---
title: Перенос субкниги в главную книгу
description: В этой теме описываются возможности Microsoft Dynamics 365 Finance для процесса субкниги в главную книгу.
author: roschlom
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 1ae10f406148e213fd0272d1387f15606233be27
ms.sourcegitcommit: 9168621ca9b5061c65f3e05dbc5918b6a11d53d5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/31/2020
ms.locfileid: "3000455"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Перенос субкниги в главную книгу

[!include [banner](../includes/banner.md)]

В этой теме описываются возможности Microsoft Dynamics 365 Finance, которые относятся к правилам переноса партий записей журнала субкниги.

В версии 8.1 были сделаны изменения, разрешающие перенос правил, поэтому параметр "Синхронный" устарел. Подробнее см. в разделе [Удаленные или устаревшие функции для Finance and Operations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).

Для переноса партий субкниги доступны следующие параметры. 

 - Асинхронно — этот параметр позволяет сразу запланировать перенос записей учета субкниги в главную книгу. Ваучер ГК будет записан, как только освободятся ресурсы, чтобы обработать этот запрос на сервере. 

- Запланированная партия — этот параметр добавляет записи учета субкниги, перемещаемые в очередь обработки в главной книге, где записи будут обрабатываться в порядке получения. Ваучер ГК будет записан в запланированное время, как только освободятся ресурсы, чтобы обработать это пакетное задание на сервере. 
 
В версии 10.0.8 были сделаны усовершенствования, повышающие производительность параметра "Асинхронно". Эта функция включается в рамках функции **Оптимизация производительности переноса субкниги в главную книгу**. 
 
Эта функция улучшает перенос данных из субкниги в главную книгу. Это позволяет повысить эффективность процесса и группирует совокупные наборы более мелких проводок для передачи. Это позволяет более эффективно использовать сервер пакетной обработки. Для этой функции требуется, чтобы сервер пакетной обработки был настроен, подключен и работал, чтобы можно было работать с параметром переноса "Асинхронно". 
