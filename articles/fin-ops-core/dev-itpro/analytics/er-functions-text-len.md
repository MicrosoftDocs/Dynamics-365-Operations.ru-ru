---
title: Функция ER LEN
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) LEN.
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
ms.openlocfilehash: b181c6b548137b997b9a64ba20391d1f5ad2ffa4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876757"
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