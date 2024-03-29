---
title: Финансовые отчеты по балансовому отчету
description: В этой статье описываются отчеты по умолчанию для балансовых отчетов. Здесь также описываются строительные блоки, связанные с этими отчетами.
author: jinniew
ms.date: 10/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinanicalReports
audience: Application User
ms.reviewer: twheeloc
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4aad297f401143388d682da175a6b14727a8f2f0
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643832"
---
# <a name="balance-sheet-financial-reports"></a>Финансовые отчеты по балансовому отчету

[!include [banner](../includes/banner.md)]

В этой статье описываются отчеты по умолчанию для балансовых отчетов. Здесь также описываются строительные блоки, связанные с этими отчетами. 

## <a name="default-balance-sheet-reports"></a>Отчеты по балансовому отчету по умолчанию

Есть два отчета по балансовому отчету по умолчанию. На одном отчете, разделы составлены друг над другом На другом отчете, разделы расположены рядом по сторонам друг от друга.

| Отчет по умолчанию                       | Что он делает                                                                                                                           |
|--------------------------------------|--------------------------------------------------------------------------------------|
| Балансовый отчет — по умолчанию              | Предоставляет Просмотр финансового положения организации за год.                    |
| Балансовый отчет и отчет о прибылях и убытках рядом – по умолчанию | Обеспечивает представление финансового положения организации за год в режиме параллельного просмотра. |

## <a name="building-blocks"></a>Шаблоны
Финансовые отчеты по балансовому отчету ведомости используют следующие строительные блоки.

| Отчет по умолчанию                       | Определение строки                       | Определение столбца             |
|--------------------------------------|--------------------------------------|-------------------------------|
| Балансовый отчет — по умолчанию              | Балансовый отчет — по умолчанию              | С начала года и отклонение — по умолчанию    |
| Балансовый отчет и отчет о прибылях и убытках рядом – по умолчанию | Балансовый отчет и отчет о прибылях и убытках рядом – по умолчанию | Столбец С начала года — по умолчанию |

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



## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор финансовой отчетности](financial-reporting-getting-started.md)

[Просмотр финансовых отчетов](view-financial-reports.md)

[Блог финансовой отчетности Dynamics](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
