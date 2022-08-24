---
title: Функция ER SESSIONNOW
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) SESSIONNOW.
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
ms.openlocfilehash: 1cf092d55728f23cb10070324abc4458004946c3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272633"
---
# <a name="sessionnow-er-function"></a>Функция ER SESSIONNOW

[!include [banner](../includes/banner.md)]

Функция `SESSIONNOW` возвращает значение *DateTime*, которое представляет текущую дату и время сеанса приложения.

## <a name="syntax"></a>Синтаксис

```vb
SESSIONNOW ()
```

## <a name="return-values"></a>Возвращаемые значения

*DateTime*

Результирующее значение даты/времени.

## <a name="example"></a>Пример

`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` возвращает значение текущей даты/времени сеанса приложения, 24 декабря 2015 года, как строку **"24.12.2015"** на основе выбранной немецкой культуры и указанного формата.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции даты и времени](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
