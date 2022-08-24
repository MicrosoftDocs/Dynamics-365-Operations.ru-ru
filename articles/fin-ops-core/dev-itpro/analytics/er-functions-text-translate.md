---
title: Функция ER TRANSLATE
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) TRANSLATE.
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
ms.openlocfilehash: 7a15a28f6efa5333b54aa34938d22a9d6e404cec
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278452"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
