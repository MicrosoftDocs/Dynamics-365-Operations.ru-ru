---
title: Финансовые отчеты по балансовому отчету
description: В этой статье описываются отчеты по умолчанию для балансовых отчетов. Здесь также описываются строительные блоки, связанные с этими отчетами.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinanicalReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e96552447182f3692a19d4cfd962afbcb28e5508
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771877"
---
# <a name="balance-sheet-financial-reports"></a>Финансовые отчеты по балансовому отчету

[!include [banner](../includes/banner.md)]

В этой статье описываются отчеты по умолчанию для балансовых отчетов. Здесь также описываются строительные блоки, связанные с этими отчетами. 

<a name="default-balance-sheet-reports"></a>Отчеты по балансовому отчету по умолчанию
-----------------------------

Есть два отчета по балансовому отчету по умолчанию. На одном отчете, разделы составлены друг над другом На другом отчете, разделы расположены рядом по сторонам друг от друга.

| Отчет по умолчанию                       | Что он делает                                                                                                                           |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Балансовый отчет — по умолчанию              | Предоставляет Просмотр финансового положения организации за год.                                                                 |
| Сравнительный балансовый отчет — по умолчанию | Предоставляет Просмотр финансового положения организации за год. Сравнение основных средств, задолженности и собственного капитала акционеров. |

## <a name="building-blocks"></a>Строительные блоки
Финансовые отчеты по балансовому отчету ведомости используют следующие строительные блоки.

| Отчет по умолчанию                       | Определение строки                       | Определение столбца             |
|--------------------------------------|--------------------------------------|-------------------------------|
| Балансовый отчет — по умолчанию              | Балансовый отчет — по умолчанию              | С начала года и отклонение — по умолчанию    |
| Сравнительный балансовый отчет — по умолчанию | Сравнительный балансовый отчет — по умолчанию | Столбец С начала года — по умолчанию |

### <a name="row-definition"></a>Определение строки

Определения строки для обоих балансовых отчетов содержит разделы для каждой части традиционного балансового отчета. Отчет бок о бок включает перенос столбца так, что задолженность и собственный капитал владельца находятся рядом с активами. Аналитика Категория счета ГК используется для того, чтобы построить оба определения строки. Поэтому, кто угодно может создать отчеты, не делая изменений.

### <a name="column-definition"></a>Определение столбца

Определения столбца содержат разные типы столбцов, чтобы обеспечить различные уровни детализации и финансовые данные.

-   **С начала года и отклонение — типы столбца по умолчанию:**
    -   **DESC** – Описание из определения строки
    -   **FD** — Финансовые данные с начала года на текущий год
    -   **FD** — Финансовые данные с начала года за прошлый год
    -   **CALC** — Отклонение от вычитания прошлого года из этого года

<!-- -->

-   **Столбец С начала года — по умолчанию:**
    -   **DESC** – Описание из определения строки
    -   **FD** — Финансовые данные с начала года на текущий год



<a name="additional-resources"></a>Дополнительные ресурсы
--------

[Обзор финансовой отчетности](financial-reporting-getting-started.md)

[Просмотр финансовых отчетов](view-financial-reports.md)

[Блог финансовой отчетности Dynamics](https://blogs.msdn.com/b/dynamics_financial_reporting/)


