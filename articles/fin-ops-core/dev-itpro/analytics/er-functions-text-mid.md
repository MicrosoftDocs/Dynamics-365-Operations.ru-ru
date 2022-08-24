---
title: Функция ER MID
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) MID.
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
ms.openlocfilehash: c53963876db92bb07ed5ac49f009ed4f9bc5e8c4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285920"
---
# <a name="mid-er-function"></a>Функция ER MID

[!include [banner](../includes/banner.md)]

Функция `MID` возвращает *строковое* значение, которое представляет указанное число символов из указанной строки, начиная с указанного положения.

## <a name="syntax"></a>Синтаксис

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a>Аргументы

`text`: *Строка*

Строковое *значение*, которое определяет текст, из которого возвращаются символы.

`starting position`: *Целочисленный*

*Целочисленное* значение, определяющее положение первого символа, который должен быть возвращен из указанного текста.

`number of characters`: *Целочисленный*

*Целочисленное* значение, определяющее число символов, которые должны быть возвращены, начиная с указанного места.

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее текстовое значение.

## <a name="usage-notes"></a>Примечания по использованию

Если значение аргумента `starting position` меньше 0 (ноль), символы, которые возвращаются, учитываются из первой позиции в указанной строке.

Если значение аргумента `starting position` превышает длину указанной строки, возвращается пустая строка.

## <a name="example"></a>Пример

`MID ("Sample", 2, 3)` возвращает **"amp"**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Текстовые функции](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
