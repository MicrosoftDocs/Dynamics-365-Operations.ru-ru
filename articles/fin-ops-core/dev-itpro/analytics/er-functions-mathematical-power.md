---
title: Функция ER POWER
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности POWER.
author: NickSelin
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
ms.openlocfilehash: ce1f4c735f815c46003ded35156bb47febf177a3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750164"
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