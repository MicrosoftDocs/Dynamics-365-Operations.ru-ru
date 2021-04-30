---
title: Перенос субкниги в главную книгу
description: В этой теме описываются возможности Microsoft Dynamics 365 Finance для процесса субкниги в главную книгу.
author: roschlom
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 1efdf095e379b73d553ca3525abbeee8ca35bcbb
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897512"
---
# <a name="subledger-transfer-to-the-general-ledger"></a><span data-ttu-id="0bd09-103">Перенос субкниги в главную книгу</span><span class="sxs-lookup"><span data-stu-id="0bd09-103">Subledger transfer to the General ledger</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0bd09-104">В этой теме описываются возможности Microsoft Dynamics 365 Finance, которые относятся к правилам переноса партий записей журнала субкниги.</span><span class="sxs-lookup"><span data-stu-id="0bd09-104">This topic describes capabilities in Microsoft Dynamics 365 Finance that are related to the rules for transferring batches of subledger journal entries.</span></span>

<span data-ttu-id="0bd09-105">В версии 8.1 были сделаны изменения, разрешающие перенос правил, поэтому параметр **Синхронный** устарел.</span><span class="sxs-lookup"><span data-stu-id="0bd09-105">In version 8.1, changes were made to allow the transfer of rules, which deprecated the **Synchronous** option.</span></span> <span data-ttu-id="0bd09-106">Подробнее см. в разделе [Удаленные или устаревшие функции для Finance and Operations](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).</span><span class="sxs-lookup"><span data-stu-id="0bd09-106">For more information, see [Removed or deprecated features for Finance and Operations](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).</span></span>

<span data-ttu-id="0bd09-107">Для переноса партий субкниги доступны следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="0bd09-107">The following options are available for transferring subledger batches.</span></span> 

 - <span data-ttu-id="0bd09-108">Асинхронно — этот параметр позволяет сразу запланировать перенос записей учета субкниги в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="0bd09-108">Asynchronous – This option will immediately schedule the transfer of the subledger accounting entries to the general ledger.</span></span> <span data-ttu-id="0bd09-109">Ваучер ГК будет записан, как только освободятся ресурсы, чтобы обработать этот запрос на сервере.</span><span class="sxs-lookup"><span data-stu-id="0bd09-109">The general ledger voucher will be recorded as soon as resources are free to process this request on the server.</span></span> 

- <span data-ttu-id="0bd09-110">Запланированная партия — этот параметр добавляет записи учета субкниги, перемещаемые в очередь обработки в главной книге, где записи будут обрабатываться в порядке получения.</span><span class="sxs-lookup"><span data-stu-id="0bd09-110">Scheduled batch – This option will add the subledger accounting entries that are being transferred to the processing queue in the general ledger, where the entries will be processed in order received.</span></span> <span data-ttu-id="0bd09-111">Ваучер ГК будет записан в запланированное время, как только освободятся ресурсы, чтобы обработать это пакетное задание на сервере.</span><span class="sxs-lookup"><span data-stu-id="0bd09-111">The general ledger voucher will be recorded at the scheduled time if resources are free to process this batch job on the server.</span></span> 
 
<span data-ttu-id="0bd09-112">В версии 10.0.8 были сделаны усовершенствования, повышающие производительность параметра "Асинхронно".</span><span class="sxs-lookup"><span data-stu-id="0bd09-112">In version 10.0.8, improvements were made to enhance the performance of the Asynchronous option.</span></span> <span data-ttu-id="0bd09-113">Эта функция включается в рамках функции **Оптимизация производительности переноса субкниги в главную книгу**.</span><span class="sxs-lookup"><span data-stu-id="0bd09-113">This feature is enabled under the feature name **Subledger transfer to General Ledger performance optimization**.</span></span> 
 
<span data-ttu-id="0bd09-114">Эта функция улучшает перенос данных из субкниги в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="0bd09-114">This functionality improves the transfer of data from the subledger to the general ledger.</span></span> <span data-ttu-id="0bd09-115">Это позволяет повысить эффективность процесса и группирует совокупные наборы более мелких проводок для передачи.</span><span class="sxs-lookup"><span data-stu-id="0bd09-115">It allows the process to be more efficient, and it groups together sets of smaller transactions to transfer.</span></span> <span data-ttu-id="0bd09-116">Это позволяет более эффективно использовать сервер пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="0bd09-116">This allows for a more efficient use of the batch server.</span></span> <span data-ttu-id="0bd09-117">Для этой функции требуется, чтобы сервер пакетной обработки был настроен, подключен и работал, чтобы можно было работать с параметром переноса "Асинхронно".</span><span class="sxs-lookup"><span data-stu-id="0bd09-117">This functionality requires that the batch server be set up, online, and functioning in order for the Asynchronous transfer option to work.</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]