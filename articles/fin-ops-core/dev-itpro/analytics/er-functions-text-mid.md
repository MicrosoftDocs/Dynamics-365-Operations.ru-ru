---
title: Функция ER MID
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности MID
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 33a8d02e937b3d88d98cac96ae28a30345ccffb23be37d7add67f721dfb9cc70
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742370"
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