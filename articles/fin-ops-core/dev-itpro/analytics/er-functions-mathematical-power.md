---
title: Функция ER POWER
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) POWER.
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
ms.openlocfilehash: 9b6693d7c1afebcf9c30d1bf8d72950053c305bd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274007"
---
# <a name="power-er-function"></a>Функция ER POWER

[!include [banner](../includes/banner.md)]

Функция `POWER` возвращает *вещественное* значение, которое представляет собой результат увеличения указанного положительного числа до указанной степени.

## <a name="syntax"></a>Синтаксис

```vb
POWER (number, power)
```

## <a name="arguments"></a>Аргументы

`number`: *Вещественный* или *Целочисленный*

Числовое значение, которое должно быть возведено в указанную степень.

`power`: *Вещественный* или *Целочисленный*

Числовое значение, представляющее определенную степень.

## <a name="return-values"></a>Возвращаемые значения

*Действующий*

Результирующее числовое значение.

## <a name="example-1"></a>Пример 1

`POWER (10, 2)` возвращает **100**.

## <a name="example-2"></a>Пример 2

`POWER (4, 0.5)` возвращает **2**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Математические функции](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
