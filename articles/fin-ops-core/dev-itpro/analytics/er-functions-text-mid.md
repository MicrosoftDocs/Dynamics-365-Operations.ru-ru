---
title: Функция ER MID
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности MID
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: e178b01740954b46e2afbd2a2be6200a652a18c0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915610"
---
# <a name="MID">Функция ER MID</a>

[!include [banner](../includes/banner.md)]

Функция `MID` возвращает *строковое* значение, которое представляет указанное число символов из указанной строки, начиная с указанного положения.

## <a name="syntax"></a>Синтаксис

```
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
