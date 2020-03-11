---
title: Функция ER OR
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности OR.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 2a850b1cbe7224ab1a7b2bd39ac4667304781cbb
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041684"
---
# <a name="OR">Функция ER OR</a>

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
