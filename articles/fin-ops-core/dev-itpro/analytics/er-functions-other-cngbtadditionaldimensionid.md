---
title: Функция ER CN_GBT_ADDITIONALDIMENSIONID
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) CN_GBT_ADDITIONALDIMENSIONID.
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
ms.openlocfilehash: 0ed2593f865a4764b1c6172722d701a0a10ba5f8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281763"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a>Функция ER CN_GBT_ADDITIONALDIMENSIONID

[!include [banner](../includes/banner.md)]

Функция `CN_GBT_ADDITIONALDIMENSIONID` возвращает *строковое* значение, представляющее один идентификатор финансовой аналитики, взятый из указанной строки. Указанная строка представляет все аналитики в виде списка идентификаторов, разделенных запятой.

## <a name="syntax"></a>Синтаксис

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a>Аргументы

`text`: *Строка*

Значение *строка* представляет все аналитики в виде списка идентификаторов, разделенных запятой.

`number`: Целочисленное

*Целочисленное* значение определяет код серии запрошенной аналитики в указанной строке.

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее текстовое значение.

## <a name="example"></a>Пример

`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` возвращает **"CC"**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Другие функции (характерные для конкретных бизнес-доменов)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
