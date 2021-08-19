---
title: Невозможно обновить прогнозируемые затраты на единицу измерения при импорте записей прогноза спроса
description: При использовании сущностей данных для импорта записей прогноза спроса себестоимость для существующих записей не обновляется, чтобы они соответствовали импортируемым данным.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: de471da861785f283eeaa78f97b5d1e1a6b023d71de6fff72ae39edd6bb124cc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765378"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a>Невозможно обновить прогнозируемые затраты на единицу измерения при импорте записей прогноза спроса

Номер статьи базы знаний: 4614109

## <a name="symptoms"></a>Симптомы

При использовании сущностей данных для импорта записей прогноза спроса значение **Прогнозируемые затраты на единицу измерения** для существующих записей не обновляется, чтобы они соответствовали импортируемым данным.

## <a name="cause"></a>Причина

**Прогнозируемые затраты на единицу измерения** является полем только для чтения. Значение основано на затраты на единицу измерения продукта и не может быть задано непосредственно при импорте.

## <a name="resolution"></a>Приказ

Так как поле доступно только для чтения, для него нельзя импортировать значения. Значение будет вычисляться в соответствии с существующей бизнес-логикой.
