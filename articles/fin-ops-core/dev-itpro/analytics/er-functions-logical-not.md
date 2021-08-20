---
title: Функция ER NOT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности NOT.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 094c60157d3ac4091fb02b24dcc00dddba2397abe87510952371a779eb3a2f4a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725292"
---
# <a name="not-er-function"></a>Функция ER NOT

[!include [banner](../includes/banner.md)]

Функция `NOT` возвращает обратное логическое значение указанного условия в качестве *логического* значения.

## <a name="syntax"></a>Синтаксис

```vb
NOT (condition)
```

## <a name="arguments"></a>Аргументы

`condition`: *Логический*

Действительное условное выражение, которое должно быть реверсировано.

## <a name="return-values"></a>Возвращаемые значения

*Логический*

Результирующее *логическое* значение.

## <a name="example"></a>Пример

`NOT (TRUE)` возвращает **FALSE**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Логические функции](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]