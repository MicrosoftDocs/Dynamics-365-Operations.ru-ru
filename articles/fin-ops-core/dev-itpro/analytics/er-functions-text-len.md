---
title: Функция ER LEN
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) LEN.
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
ms.openlocfilehash: 5a8e672e0308a58dca28c73ce01c7307abec60ed
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280136"
---
# <a name="len-er-function"></a>Функция ER LEN

[!include [banner](../includes/banner.md)]

Функция `LEN` возвращает целочисленное значение, которое представляет число символов в указанной строке как *целочисленное* значение.

## <a name="syntax"></a>Синтаксис

```vb
LEN (text)
```

## <a name="arguments"></a>Аргументы

`text`: *Строка*

*Строковое* значение, задающее текст.

## <a name="return-values"></a>Возвращаемые значения

*Целочисленный*

Результирующее числовое значение.

## <a name="example"></a>Пример

`LEN ("Sample")` возвращает **6**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Текстовые функции](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
