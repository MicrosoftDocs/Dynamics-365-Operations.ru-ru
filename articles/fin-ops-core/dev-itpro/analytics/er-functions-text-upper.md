---
title: Функция ER UPPER
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) UPPER.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 539c9c0d225f4daf53038ce0f26e641ee94ae790
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877048"
---
# <a name="upper-er-function"></a>Функция ER UPPER

[!include [banner](../includes/banner.md)]

Функция `UPPER` возвращает указанную строку текста в качестве *строкового* значения после того, как она была преобразована в буквы верхнего регистра.

## <a name="syntax"></a>Синтаксис

```vb
UPPER (text )
```

## <a name="arguments"></a>Аргументы

`text`: *Строка*

Действительный путь источника данных типа *Строка*.

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее текстовое значение.

## <a name="example"></a>Пример

`UPPER ("Sample")` возвращает **"SAMPLE"**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Текстовые функции](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]