---
title: Функция ER NUMBERFORMAT
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) NUMBERFORMAT.
author: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 5519f549c10ba5c02e249592d040582c3f8dc44f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274806"
---
# <a name="numberformat-er-function"></a>Функция ER NUMBERFORMAT

[!include [banner](../includes/banner.md)]

Функция `NUMBERFORMAT` возвращает значение *строки*, которое представляет заданное число в указанном формате и в дополнительно указанной [культуре](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Сведения о поддерживаемых форматах см. в разделах [стандартный](/dotnet/standard/base-types/standard-numeric-format-strings) и [настраиваемый](/dotnet/standard/base-types/custom-numeric-format-strings).

## <a name="syntax-1"></a>Синтаксис 1

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a>Синтаксис 2

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a>Аргументы

`number`: *Целочисленный* или *Вещественный*

Числовое значение, которое определяет число, которое должно быть отформатировано.

`format`: *Строка*

*Строковое* значение, представляющее формат.

`culture`: *Строка*

*Строковое* значение строки, которое представляет культуру для форматирования.

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее текстовое значение.

## <a name="usage-notes"></a>Примечания по использованию

Если культура не определена как аргумент вызываемо функции, контекст, в который работает эта функция, определяет культуру, используемую для форматирования чисел.

## <a name="example-1"></a>Пример 1

Для культуры **EN-US**, `NUMBERFORMAT (0.45, "p")` возвращает **"45.00 %"**, а `NUMBERFORMAT (10.45, "#")`возвращает **"10"**.

## <a name="example-2"></a>Пример 2

`NUMBERFORMAT (10/3, "F2", "de")` возвращает **3,33**, в то время как `NUMBERFORMAT (10/3, "F2", "en-us")` возвращает **3,33**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Текстовые функции](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
