---
title: Функция ER DATETODATETIME
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) DATETODATETIME.
author: kfend
ms.date: 12/04/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 30fe75c7fd68edfff3e3778192723792d0f342ab
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287319"
---
# <a name="datetodatetime-er-function"></a>Функция ER DATETODATETIME

[!include [banner](../includes/banner.md)]

Функция `DATETODATETIME` возвращает значение *DateTime*, которое преобразуется из заданного значения даты в значение даты/времени в формате UTC (Greenwich Mean Time \[GMT\]).

## <a name="syntax"></a>Синтаксис

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a>Аргументы

`date`: *Дата*

Значение даты, представляющее дату для преобразования.

## <a name="return-values"></a>Возвращаемые значения

*DateTime*

Результирующее значение даты/времени.

## <a name="example-1"></a>Пример 1

`DATETODATETIME (CompInfo. 'getCurrentDate()')` возвращает дату текущего сеанса Microsoft Dynamics 365 Finance, 24 декабря 2015, как **12/24/2015 12:00:00 AM**. В этом примере **CompInfo** представляет собой источник данных электронной отчетности (ER) типа **Финансы и операции/Table** и ссылается на таблицу CompanyInfo.

## <a name="example-2"></a>Пример 2

`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` возвращает значение даты/времени **11/12/2019 12:00:00 AM**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции даты и времени](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
