---
title: Функция ER NUMBERFORMAT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности NUMBERFORMAT.
author: NickSelin
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8de57d8b0a45b8b58849a24f2d8f0cde41e0ea3a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746226"
---
# <a name="numberformat-er-function"></a>Функция ER NUMBERFORMAT

[!include [banner](../includes/banner.md)]

Функция `NUMBERFORMAT` возвращает значение *строки*, которое представляет заданное число в указанном формате и в дополнительно указанной [культуре](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Сведения о поддерживаемых форматах см. в разделах [стандартный](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) и [настраиваемый](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).

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