---
title: Функция ER NOT
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) NOT.
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
ms.openlocfilehash: 032cdaa2c71f6fab8c15780594d5a26d73600e74
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278987"
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
