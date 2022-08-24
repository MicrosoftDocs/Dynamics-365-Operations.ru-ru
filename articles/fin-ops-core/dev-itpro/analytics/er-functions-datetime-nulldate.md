---
title: Функция ER NULLDATE
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) NULLDATE.
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
ms.openlocfilehash: 276ad99303a4e88ecb1c83e9518e06bfd7afaa45
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272663"
---
# <a name="nulldate-er-function"></a>Функция ER NULLDATE

[!include [banner](../includes/banner.md)]

Функция `NULLDATE` возвращает значение *Date*, которое представляет **нулевую** дату (1 января 1900 года).

## <a name="syntax"></a>Синтаксис

```vb
NULLDATE () as 
```

## <a name="return-values"></a>Возвращаемые значения

*Дата*

Результирующее значение даты.

## <a name="example-1"></a>Пример 1

`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` возвращает **нулевую** дату, 1 января 1900 года, как **"1900-01-01"**, на основе указанного пользовательского формата.

## <a name="example-2"></a>Пример 2

Выражение `IF( Invoice.DocumentDate = NULLDATE(), true, false)` возвращает **True**, когда значение поля **DocumentDate** равняется **нулевой** дате. В этом примере **Invoice** представляет собой источник данных электронной отчетности (ER) типа **Записи Finance/Table** и ссылается на таблицу CustInvoiceJour.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции даты и времени](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
