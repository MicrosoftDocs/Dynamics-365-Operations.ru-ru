---
title: Функция ER PADLEFT
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) PADLEFT.
author: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: dac1f9142a381238bf116c4bce65958da8afc4db
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278899"
---
# <a name="padleft-er-function"></a>Функция ER PADLEFT

[!include [banner](../includes/banner.md)]

Функция `PADLEFT` возвращает *строковое* значение указанной длины, в котором в начало указанной строки добавлены указанные символы.

## <a name="syntax"></a>Синтаксис

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a>Аргументы

`text`: *Строка*

*Строковое* значение, представляющее исходный текст.

`length`: *Целочисленный*

*Целочисленное* значение, представляющее окончательное число символов в строке с отступами.

`padding chars`: *Строка*

Символы для использования для отступа.

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее текстовое значение.

## <a name="example"></a>Пример

`PADLEFT ("1234", 10, "`&nbsp;`")` возвращает текстовую строку **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Текстовые функции](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
