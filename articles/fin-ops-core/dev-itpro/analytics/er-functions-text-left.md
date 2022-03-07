---
title: Функция ER LEFT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности LEFT
author: NickSelin
ms.date: 12/11/2019
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
ms.openlocfilehash: 5d0056dbe46b20432aacb35a971895b987fdbf1b8ebc0d2679bb1e52eb3c4cc2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762484"
---
# <a name="left-er-function"></a>Функция ER LEFT

[!include [banner](../includes/banner.md)]

Функция `LEFT` возвращает *строковое* значение, которое представляет указанное число символов от начала указанной строки.

## <a name="syntax"></a>Синтаксис

```vb
LEFT (text, number)
```

## <a name="arguments"></a>Аргументы

`text`: *Строка*

*Строковое* значение, представляющее исходный текст.

`number`: *Целочисленный*

Количество символов, которые должны быть возвращены с начала исходного текста.

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее текстовое значение.

## <a name="example"></a>Пример

`LEFT ("Sample", 3)` возвращает **"Sam"**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Текстовые функции](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]