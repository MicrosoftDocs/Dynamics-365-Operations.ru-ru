---
title: Функция ER TRANSLATE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности TRANSLATE.
author: NickSelin
manager: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: c5d192b8679d6df2c44a0038fe4ffc181a6a54df
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685311"
---
# <a name="translate-er-function"></a>Функция ER TRANSLATE

[!include [banner](../includes/banner.md)]

Функция `TRANSLATE` возвращает значение *Строка*, которое содержит результат замены символов указанного текста символами другого предоставленного набора.

## <a name="syntax"></a>Синтаксис

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a>Аргументы

`text`: *Строка*

Действительный путь источника данных типа *Строка*.

`pattern`: *Строка*

Текст, который должен быть заменен.

`replacement`: *Строка*

Текст для использования в качестве замены.

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее текстовое значение.

## <a name="usage-notes"></a>Примечания по использованию

Функция `TRANSLATE` заменяет один символ за раз. Функция заменяет первый символ аргумента `text` с первым символом аргумента `pattern`, затем второй символ, и действует таким образом до завершения операции. Когда символ из аргументов `text` и `pattern` совпадает, он замещается символом из аргумента `replacement`, расположенным в той же позиции, что и символ из аргумента `pattern`. Если символ появляется в аргументе `pattern` несколько раз, используется сопоставление аргумента `replacement`, соответствующее первому вхождению данного символа.

## <a name="example-1"></a>Пример 1

`TRANSLATE ("abcdef", "cd", "GH")` заменяет символ **"c"** указанного текста **"abcdef"** символом **"G"** аргумента `replacement`, выполняя следующие действия:
-   Символ **"c"** представлен в тексте `pattern` в первом положении.
-   Первая позиция текста `replacement` содержит символ **"G"**.

## <a name="example-2"></a>Пример 2

`TRANSLATE ("abcdef", "ccd", "GH")` возвращает **"abGdef"**.

## <a name="example-3"></a>Пример 3

`TRANSLATE ("abccba", "abc", "123")` возвращает **"123321"**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Текстовые функции](er-functions-category-text.md)
