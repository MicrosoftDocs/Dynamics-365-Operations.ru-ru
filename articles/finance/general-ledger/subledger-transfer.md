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
# <a name="subledger-transfer-to-the-general-ledger"></a><span data-ttu-id="6563d-103">Перенос субкниги в главную книгу</span><span class="sxs-lookup"><span data-stu-id="6563d-103">Subledger transfer to the General ledger</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6563d-104">В этой теме описываются возможности Microsoft Dynamics 365 Finance, которые относятся к правилам переноса партий записей журнала субкниги.</span><span class="sxs-lookup"><span data-stu-id="6563d-104">This topic describes capabilities in Microsoft Dynamics 365 Finance that are related to the rules for transferring batches of subledger journal entries.</span></span>

<span data-ttu-id="6563d-105">В версии 8.1 были сделаны изменения, разрешающие перенос правил, поэтому параметр "Синхронный" устарел.</span><span class="sxs-lookup"><span data-stu-id="6563d-105">In version 8.1, changes were made to allow the transfer of rules, which deprecated the Synchronous option.</span></span> <span data-ttu-id="6563d-106">Подробнее см. в разделе [Удаленные или устаревшие функции для Finance and Operations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).</span><span class="sxs-lookup"><span data-stu-id="6563d-106">For more information, see [Removed or deprecated features for Finance and Operations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).</span></span>

<span data-ttu-id="6563d-107">Для переноса партий субкниги доступны следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="6563d-107">The following options are available for transferring subledger batches.</span></span> 

 - <span data-ttu-id="6563d-108">Асинхронно — этот параметр позволяет сразу запланировать перенос записей учета субкниги в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="6563d-108">Asynchronous – This option will immediately schedule the transfer of the subledger accounting entries to the general ledger.</span></span> <span data-ttu-id="6563d-109">Ваучер ГК будет записан, как только освободятся ресурсы, чтобы обработать этот запрос на сервере.</span><span class="sxs-lookup"><span data-stu-id="6563d-109">The general ledger voucher will be recorded as soon as resources are free to process this request on the server.</span></span> 

- <span data-ttu-id="6563d-110">Запланированная партия — этот параметр добавляет записи учета субкниги, перемещаемые в очередь обработки в главной книге, где записи будут обрабатываться в порядке получения.</span><span class="sxs-lookup"><span data-stu-id="6563d-110">Scheduled batch – This option will add the subledger accounting entries that are being transferred to the processing queue in the general ledger, where the entries will be processed in order received.</span></span> <span data-ttu-id="6563d-111">Ваучер ГК будет записан в запланированное время, как только освободятся ресурсы, чтобы обработать это пакетное задание на сервере.</span><span class="sxs-lookup"><span data-stu-id="6563d-111">The general ledger voucher will be recorded at the scheduled time if resources are free to process this batch job on the server.</span></span> 
 
<span data-ttu-id="6563d-112">В версии 10.0.8 были сделаны усовершенствования, повышающие производительность параметра "Асинхронно".</span><span class="sxs-lookup"><span data-stu-id="6563d-112">In version 10.0.8, improvements were made to enhance the performance of the Asynchrounous option.</span></span> <span data-ttu-id="6563d-113">Эта функция включается в рамках функции **Оптимизация производительности переноса субкниги в главную книгу**.</span><span class="sxs-lookup"><span data-stu-id="6563d-113">This feature is enabled under the feature name **Subledger transfer to General Ledger performance optimization**.</span></span> 
 
<span data-ttu-id="6563d-114">Эта функция улучшает перенос данных из субкниги в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="6563d-114">This functionality improves the transfer of data from the subledger to the general ledger.</span></span> <span data-ttu-id="6563d-115">Это позволяет повысить эффективность процесса и группирует совокупные наборы более мелких проводок для передачи.</span><span class="sxs-lookup"><span data-stu-id="6563d-115">It allows the process to be more efficient, and it groups together sets of smaller transactions to transfer.</span></span> <span data-ttu-id="6563d-116">Это позволяет более эффективно использовать сервер пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="6563d-116">This allows for a more efficient use of the batch server.</span></span> <span data-ttu-id="6563d-117">Для этой функции требуется, чтобы сервер пакетной обработки был настроен, подключен и работал, чтобы можно было работать с параметром переноса "Асинхронно".</span><span class="sxs-lookup"><span data-stu-id="6563d-117">This functionality requires that the batch server be set up, online, and functioning in order for the Asynchrounous transfer option to work.</span></span> 
