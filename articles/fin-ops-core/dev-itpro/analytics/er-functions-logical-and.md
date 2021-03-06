---
title: Функция ER AND
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности AND
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 9851321137b4c7744634df30f85aa3a0b1a0a588
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745481"
---
# <a name="and-er-function"></a>Функция ER AND

[!include [banner](../includes/banner.md)]

Функция `AND` возвращает *логическое* значение **TRUE**, если все указанные условия — true. В противном случае возвращает *логическое* значение **FALSE**.

## <a name="syntax"></a>Синтаксис

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>Аргументы

`condition 1`: *Логический*

Действительное условное выражение, которое должно быть протестировано. Этот аргумент обязательный.

`condition N`: *Логический*

Действительное условное выражение, которое должно быть протестировано. Эти дополнительные аргументы являются необязательными.

## <a name="return-values"></a>Возвращаемые значения

*Логический*

Результирующее *логическое* значение.

## <a name="usage-notes"></a>Примечания по использованию

В аргументах логических функций можно использовать ссылки на источники данных, числовые и текстовые значения, логические значения, операторы сравнения и другие функции электронной отчетности (ER). Тем не менее, все аргументы должны быть оценены как *логическое* значение **TRUE** или **FALSE**.

## <a name="example"></a>Пример

`AND (1=1, "a"="a")` возвращает **TRUE**.

`AND (1=2, "a"="a")` возвращает **FALSE**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Логические функции](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]