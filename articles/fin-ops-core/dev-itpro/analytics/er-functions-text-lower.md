---
title: Функция ER LOWER
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) LOWER.
author: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 7a633c8cf68b611fcaa3f216823ef9b19cac16f5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288029"
---
# <a name="lower-er-function"></a>Функция ER LOWER

[!include [banner](../includes/banner.md)]

Функция `LOWER` возвращает указанную строку текста в качестве *строкового* значения после того, как она была преобразована в буквы нижнего регистра.

## <a name="syntax"></a>Синтаксис

```vb
LOWER (text)
```

## <a name="arguments"></a>Аргументы

`text`: *Строка*

*Строковое* значение, задающее текст.

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее текстовое значение.

## <a name="example"></a>Пример

`LOWER ("Sample")` возвращает **"sample"**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Текстовые функции](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
