---
title: Функция ER REPLACE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности REPLACE.
author: NickSelin
ms.date: 04/02/2020
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
ms.openlocfilehash: 21cdd8532730925b7d5c6f5b3bb565dcd365dd6d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746213"
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