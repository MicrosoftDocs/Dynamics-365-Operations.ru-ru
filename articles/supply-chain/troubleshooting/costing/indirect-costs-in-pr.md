---
title: В отчете "косвенные затраты в процессе" содержатся удаленные производственные заказы
description: В отчете "косвенные затраты в процессе" представлены сведения о производственных заказах, которые были частично обработаны и позднее удалены.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdIndirectCostInProgress
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 707fa9bb30129c3656e10c6756dee770a7712e65
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026848"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a><span data-ttu-id="ffe90-103">В отчете "косвенные затраты в процессе" содержатся удаленные производственные заказы</span><span class="sxs-lookup"><span data-stu-id="ffe90-103">The Indirect costs in process report includes deleted production orders</span></span>

<span data-ttu-id="ffe90-104">Номер статьи базы знаний: 4612748</span><span class="sxs-lookup"><span data-stu-id="ffe90-104">KB number: 4612748</span></span>

## <a name="symptoms"></a><span data-ttu-id="ffe90-105">Симптомы</span><span class="sxs-lookup"><span data-stu-id="ffe90-105">Symptoms</span></span>

<span data-ttu-id="ffe90-106">В отчете **Косвенные затраты в процессе** представлены сведения о производственных заказах, которые были частично обработаны и позднее удалены.</span><span class="sxs-lookup"><span data-stu-id="ffe90-106">The **Indirect costs in process** report presents information about production orders that were partially processed and later deleted.</span></span>

## <a name="resolution"></a><span data-ttu-id="ffe90-107">Приказ</span><span class="sxs-lookup"><span data-stu-id="ffe90-107">Resolution</span></span>

<span data-ttu-id="ffe90-108">При сторнировании производственного заказа также сторнируются все проводки этого производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="ffe90-108">When you reverse a production order, you also reverse all the transactions of that production order.</span></span> <span data-ttu-id="ffe90-109">При удалении производственного заказа таблицы субкниги и главной книги сохраняют все связанные друг с другом проводки.</span><span class="sxs-lookup"><span data-stu-id="ffe90-109">When you delete the production order, the subledger tables and general ledger persist all transactions that are related to it.</span></span> <span data-ttu-id="ffe90-110">В отчетах отображаются проводки в таблицах субкниги.</span><span class="sxs-lookup"><span data-stu-id="ffe90-110">The reports will show the transactions in the subledger tables.</span></span> <span data-ttu-id="ffe90-111">Для конкретного производственного заказа чистая стоимость должна быть 0,00.</span><span class="sxs-lookup"><span data-stu-id="ffe90-111">For the specific production order, the net value should be 0.00.</span></span>
