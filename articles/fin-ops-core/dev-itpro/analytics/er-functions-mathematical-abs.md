---
title: Функция ER ABS
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) ABS.
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: a8d0fe68232d9dd27d9ba0cc6b81c7708d22711e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272569"
---
# <a name="abs-er-function"></a>Функция ER ABS

[!include [banner](../includes/banner.md)]

Функция `ABS` возвращает абсолютное значение (модуль) указанного числа в качестве *вещественного* значения. Другими словами, возвращает число без знака.

## <a name="syntax"></a>Синтаксис

```vb
ABS (number)
```

## <a name="arguments"></a>Аргументы

`number`: *Вещественный*

Числовое значение, модуль которого вам нужен.

## <a name="return-values"></a>Возвращаемые значения

*Действующий*

Результирующее числовое значение.

## <a name="example"></a>Пример

`ABS (-1)` возвращает **1**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Математические функции](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
