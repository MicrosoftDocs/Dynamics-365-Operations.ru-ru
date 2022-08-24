---
title: Функция ER SESSIONTODAY
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) SESSIONTODAY.
author: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 0eeb4fcc449b565774cc79b767a2d157557d5b98
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274900"
---
# <a name="sessiontoday-er-function"></a>Функция ER SESSIONTODAY

[!include [banner](../includes/banner.md)]

Функция `SESSIONTODAY` возвращает значение *Date*, которое представляет текущую дату сеанса приложения.

## <a name="syntax"></a>Синтаксис

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a>Возвращаемые значения

*Дата*

Результирующее значение даты.

## <a name="example"></a>Пример

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` возвращает текущую дату сеанса приложения, 24 декабря 2015 года, как строку **"24-12-2015"** на основе выбранной немецкой культуры и указанного формата.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции даты и времени](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
