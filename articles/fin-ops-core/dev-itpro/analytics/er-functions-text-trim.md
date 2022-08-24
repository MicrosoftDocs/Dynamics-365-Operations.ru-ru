---
title: Функция ER TRIM
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) TRIM.
author: kfend
ms.date: 02/28/2022
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
ms.openlocfilehash: 95b8d2989d705c4998da0af8e683adf567edfe92
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273109"
---
# <a name="trim-er-function"></a>Функция ER TRIM

[!include [banner](../includes/banner.md)]

Функция `TRIM` возвращает указанную текстовую строку в виде значения *Строка* после замены знаков табуляции, возврата каретки, перевода строки и перевода форм на один символ пробела, после удаления ведущих и замыкающих пробелов и после удаления повторяющихся пробелов между словами.

## <a name="syntax"></a>Синтаксис

```vb
TRIM (text)
```

## <a name="arguments"></a>Аргументы

`text`: *Строка*

Действительный путь источника данных типа *Строка*.

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее текстовое значение.

## <a name="usage-notes"></a>Примечания по использованию

В некоторых случаях бывает необходимо удалить начальные и конечные пробелы, но желательно сохранить форматирование для указанного текста. Например, если этот текст представляет адрес, который можно ввести в многострочное текстовое поле и он может содержать символы перевода строки и возврата каретки. В этом случае используется следующее выражение: `REPLACE(text,"^[ \t]+|[ \t]+$","", true)`, где `text` — это аргумент, обозначающий указанную текстовую строку.

## <a name="example-1"></a>Пример 1

`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` возвращает **"Sample text"**.

## <a name="example-2"></a>Пример 2

`TRIM (CONCATENATE (CHAR(10), "`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(9),"`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(13)))` возвращает **"Образец текста"**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Текстовые функции](er-functions-category-text.md)

[Функция ER REPLACE](er-functions-text-replace.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
