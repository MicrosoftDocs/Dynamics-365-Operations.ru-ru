---
title: Функция ER REPLACE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности REPLACE.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: ba2590635ba465dae9ea50d3e4da989365548f3b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040994"
---
# <a name="REPLACE">Функция ER REPLACE</a>

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

Если аргумент `regular expression flag` — **FALSE**, эта функция ведет себя как [TRANSLATE](er-functions-text-translate.md). Символы, заданные аргументом `replacement` используются для замены найденных символов. 

## <a name="example-1"></a>Пример 1

`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` применяет регулярное выражение, которое удаляет все нечисловые символы и возвращает **"19234564971"**. 

## <a name="example-2"></a>Пример 2

`REPLACE ("abcdef", "cd", "GH", false)` заменяет шаблон **"cd"** строкой **"GH"** и возвращает **"abGHef"**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Текстовые функции](er-functions-category-text.md)
