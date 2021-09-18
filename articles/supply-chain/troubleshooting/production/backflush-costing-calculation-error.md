---
title: Ошибка backflush-расчета себестоимости при закрытии склада
description: В предыдущих выпусках могла быть получена ошибка backflush-расчета себестоимости в процессе закрытия склада. Эта проблема была устранена.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ae92b7121998d6b1ba2f08ea5736c55637867fbf
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477401"
---
# <a name="backflush-costing-calculation-error-during-inventory-closing"></a>Ошибка backflush-расчета себестоимости при закрытии склада

## <a name="symptoms"></a>Симптомы

В выпусках до выпуска 10.0.13 если не используется поток расчета себестоимости бережливого производства, при закрытии запасов выводится следующее сообщение об ошибке:

> Вы собираетесь выполнить закрытие запасов с датой %1. Не было зарегистрировано выполнение вычисления backflush-расчета себестоимости с датой %1, соответствующее концу периода. Не забудьте выполнить вычисление backflush-расчета себестоимости с датой %1, соответствующее концу периода. Оценка стоимости запасов, себестоимости проданных товаров и отклонений может быть неверна в субкниге или в главной книге до тех пор, пока оно не будет выполнено.

## <a name="resolution"></a>Решение

Эта проблема исправлена в версии 10.0.13 и более поздних версиях. Дополнительные сведения см. в статье базы знаний [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).
