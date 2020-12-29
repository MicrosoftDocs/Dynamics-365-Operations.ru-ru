---
title: Функция ER TRIM
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности TRIM
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 908da840ffcb94f4a60bb41ce041f5f263c921eb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688378"
---
# <a name="trim-er-function"></a>Функция ER TRIM

[!include [banner](../includes/banner.md)]

Функция `TRIM` возвращает указанную текстовую строку в качестве *строкового* значения после удаления начальных и конечных пробелов и после преобразования нескольких пробелов между словами в одинарные пробелы.

## <a name="syntax"></a>Синтаксис

```vb
TRIM (text )
```

## <a name="arguments"></a>Аргументы

`text`: *Строка*

Действительный путь источника данных типа *Строка*.

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее текстовое значение.

## <a name="example"></a>Пример

`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` возвращает **"Sample text"**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Текстовые функции](er-functions-category-text.md)
