---
title: Функция ER CN_GBT_ADDITIONALDIMENSIONID
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности CN_GBT_ADDITIONALDIMENSIONID.
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
ms.openlocfilehash: 7fdc4527bc6115bdb3fca9d6a92d3d77a7c264c2
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744439"
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
