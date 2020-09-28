---
title: Функция ER DATETODATETIME
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности DATETODATETIME.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eac09c9b410815ad9ae71dec53fc0416b020ca1e
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744823"
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

`DATETODATETIME (CompInfo. 'getCurrentDate()')` возвращает дату текущего сеанса Microsoft Dynamics 365 Finance, 24 декабря 2015, как **12/24/2015 12:00:00 AM**. В этом примере **CompInfo** представляет собой источник данных электронной отчетности (ER) типа **Finance and Operations/Table** и ссылается на таблицу CompanyInfo.

## <a name="example-2"></a>Пример 2

`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` возвращает значение даты/времени **11/12/2019 12:00:00 AM**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции даты и времени](er-functions-category-datetime.md)
