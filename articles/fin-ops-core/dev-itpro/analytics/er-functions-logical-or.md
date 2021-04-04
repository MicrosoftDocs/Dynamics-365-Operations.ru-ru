---
title: Функция ER OR
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности OR.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 7c2f110185330ee1e0cc6dc9ac534ae697e4b19b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565864"
---
# <a name="or-er-function"></a>Функция ER OR

[!include [banner](../includes/banner.md)]

Функция `OR` возвращает *логическое* значение **FALSE**, если все указанные условия — false. Если какое-либо указанное условие — true, эта функция возвращает *логическое* значение **TRUE**.

## <a name="syntax"></a>Синтаксис

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>Аргументы

`condition 1`: *Логический*

Действительное условное выражение, которое должно быть протестировано. Этот аргумент обязательный.

`condition N`: *Логический*

Действительное условное выражение, которое должно быть протестировано. Эти дополнительные аргументы являются необязательными.

## <a name="return-values"></a>Возвращаемые значения

*Логический*

Результирующее *логическое* значение.

## <a name="example"></a>Пример

`OR (1=2, "a"="a")` возвращает **TRUE**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Логические функции](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]