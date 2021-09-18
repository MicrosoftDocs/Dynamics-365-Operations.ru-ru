---
title: Журнал запасов заблокирован, и пакетное задание рабочего процесса не работает
description: Один из журналов запасов заблокирован какой-либо операцией и не освобождается
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8b21ec2e2b3b8546dcb138422c5540053392c179
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477389"
---
# <a name="your-inventory-journal-is-locked-and-the-workflow-batch-job-doesnt-work"></a>Журнал запасов заблокирован, и пакетное задание рабочего процесса не работает

## <a name="symptoms"></a>Симптомы

Один из журналов запасов заблокирован какой-либо операцией и не освобождается. Например, если во время разноски (которая является операцией с системной блокировкой) произошла неизвестная ошибка, журнал может остаться в статусе заблокированного системой. В этом случае обработчик рабочего элемента рабочего процесса вызовет ошибку, когда он выполняет проверку блокировки.

## <a name="resolution"></a>Решение

Выполните вход в экземпляр SQL Server для Supply Chain Management и проверьте, установлено ли для параметра **InventJournalTable.SystemBlocked** значение *1*. Если это так, убедитесь, что журнал не должен находиться в состоянии блокировки, затем сбросьте параметр **InventJournalTable.SystemBlocked** на значение *0*.
