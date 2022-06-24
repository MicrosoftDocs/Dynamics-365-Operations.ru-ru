---
title: Функция ER TRIM
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) TRIM.
author: NickSelin
ms.date: 02/28/2022
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
ms.openlocfilehash: deadf89641771efa864e701af9dad57c5e62ea37
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864669"
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
