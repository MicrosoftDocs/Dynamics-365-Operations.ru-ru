---
title: Функция ER REPLACE
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) REPLACE.
author: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: e7a27b5015615d9b0f26e8fcddd812b3f51fb945
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278482"
---
# <a name="replace-er-function"></a>Функция ER REPLACE

[!include [banner](../includes/banner.md)]

Функция `REPLACE` возвращает указанную строку текста в качестве значения *Строка* после того, как все или ее часть была заменена другой строкой.

## <a name="syntax"></a>Синтаксис

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a>Аргументы

`text`: *Строка*

Действительный путь источника данных типа *Строка*.

`pattern`: *Строка*

Если аргумент `regular expression flag` — **FALSE**, этот аргумент содержит текст, который должен быть заменен.

Если аргумент `regular expression flag` — **TRUE**, этот аргумент содержит регулярное выражение, которое определяет как шаблон поиска, так и текст замены.

`replacement`: *Строка*

Если аргумент `regular expression flag` — **FALSE**, этот аргумент содержит текст, который используется в качестве замены.

Если аргумент `regular expression flag` — **TRUE**, этот аргумент не используется.

`regular expression flag`: *Логический*

*Логическое* значение, которое указывает, используется ли регулярное выражение для замены.

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее текстовое значение.

## <a name="usage-notes"></a>Примечания по использованию

Если аргумент `regular expression flag` — **TRUE**, эта функция возвращает указанную строку после того, как она была изменена в результате использования регулярного выражения, заданного аргументом `pattern`. Регулярное выражение используется для обнаружения символов, которые необходимо заменить.

Если аргумент `regular expression flag` имеет значение **FALSE**, эта функция возвращает указанную строку после того, как набор символов, определенных в аргументе `pattern`, был заменен символами из аргумента `replacement`. 

## <a name="example-1"></a>Пример 1

`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` применяет регулярное выражение, которое удаляет все нечисловые символы и возвращает **"19234564971"**. 

## <a name="example-2"></a>Пример 2

`REPLACE ("abcdef", "cd", "GH", false)` заменяет шаблон **"cd"** строкой **"GH"** и возвращает **"abGHef"**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Текстовые функции](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
