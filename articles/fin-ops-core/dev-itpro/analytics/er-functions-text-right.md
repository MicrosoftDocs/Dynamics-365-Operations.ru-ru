---
title: Функция ER RIGHT
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) RIGHT.
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
ms.openlocfilehash: fc3e5fed67ecc67bf0673f7d8322b7c151c4d50c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287165"
---
# <a name="right-er-function"></a>Функция ER RIGHT

[!include [banner](../includes/banner.md)]

Функция `RIGHT` возвращает *строковое* значение, которое представляет указанное число символов от конца указанной строки.

## <a name="syntax"></a>Синтаксис

```vb
RIGHT (text, number)
```

## <a name="arguments"></a>Аргументы

`text`: *Строка*

*Строковое* значение, представляющее исходный текст.

`number`: *Целочисленный*

Количество символов, которые должны быть возвращены с конца исходного текста.

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее текстовое значение.

## <a name="example"></a>Пример

`RIGHT ("Sample", 3)` возвращает **"ple"**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Текстовые функции](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
