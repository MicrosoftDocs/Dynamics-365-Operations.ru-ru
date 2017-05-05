---
title: "Финансовый отчет по отчету о прибылях"
description: "В этой статье описывается отчет по умолчанию для отчетов о прибыли. Здесь также описываются строительные блоки, связанные с этим отчетом."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 8dd289c1943afb55373ba682afcc3cd107cb67a7
ms.lasthandoff: 03/31/2017


---

# <a name="income-statement-financial-report"></a>Финансовый отчет по отчету о прибылях

[!include[banner](../includes/banner.md)]


В этой статье описывается отчет по умолчанию для отчетов о прибыли. Здесь также описываются строительные блоки, связанные с этим отчетом. 

<a name="default-income-statement-report"></a>Отчет о прибылях по умолчанию
-------------------------------

| Отчет по умолчанию             | Что он делает                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| Отчет о доходах — по умолчанию | Предоставляет просмотр доходности организации за текущий период и также с начала года. |

## <a name="building-blocks"></a>Строительные блоки
Финансовый отчет по отчету о прибылях использует следующие строительные блоки.

| Отчет по умолчанию             | Определение строки                     | Определение столбца          |
|----------------------------|------------------------------------|----------------------------|
| Отчет о доходах — по умолчанию | Сводный отчет о доходах — по умолчанию | Периодически и с начала года — по умолчанию |

### <a name="row-definition"></a>Определение строки

Определение строки, Сводный отчет о доходах — по умолчанию, содержит раздел для каждой из частей традиционного отчета о доходах. Аналитика Категория счета ГК используется для того, чтобы построить это определение строки. Поэтому, кто угодно может создать отчет, не делая изменений.

### <a name="column-definition"></a>Определение столбца

Определения столбца содержат разные типы столбцов, чтобы обеспечить различные уровни детализации и финансовые данные.

-   **Периодически и с начала года — типы столбца по умолчанию:**
    -   **DESC** – Описание из определения строки
    -   **FD** — Финансовые данные на текущий период
    -   **FD** — Финансовые данные с начала года

 

<a name="see-also"></a>См. также
--------

[Финансовая отчетность](financial-reporting-getting-started.md)

[Просмотр финансовых отчетов](view-financial-reports.md)

[Блог финансовой отчетности Dynamics](http://blogs.msdn.com/b/dynamics_financial_reporting/)



