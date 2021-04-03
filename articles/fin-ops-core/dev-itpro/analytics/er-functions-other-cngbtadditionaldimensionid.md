---
title: Функция ER CN_GBT_ADDITIONALDIMENSIONID
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности CN_GBT_ADDITIONALDIMENSIONID.
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
ms.openlocfilehash: 5774bb6928ae321af923819d6b2cc609dbf35b99
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564150"
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