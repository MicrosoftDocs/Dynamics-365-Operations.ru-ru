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
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a>В отчете "косвенные затраты в процессе" содержатся удаленные производственные заказы

Номер статьи базы знаний: 4612748

## <a name="symptoms"></a>Симптомы

В отчете **Косвенные затраты в процессе** представлены сведения о производственных заказах, которые были частично обработаны и позднее удалены.

## <a name="resolution"></a>Приказ

При сторнировании производственного заказа также сторнируются все проводки этого производственного заказа. При удалении производственного заказа таблицы субкниги и главной книги сохраняют все связанные друг с другом проводки. В отчетах отображаются проводки в таблицах субкниги. Для конкретного производственного заказа чистая стоимость должна быть 0,00.
