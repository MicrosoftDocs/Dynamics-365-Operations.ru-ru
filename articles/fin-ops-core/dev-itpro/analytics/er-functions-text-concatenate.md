---
title: Функция ER CONCATENATE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности CONCATENATE.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 1507e1b8a31ed45e7c540e4e2ff31b79e8de3b866ffbace9de17d7b3e169e877
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762508"
---
# <a name="concatenate-er-function"></a>Функция ER CONCATENATE

[!include [banner](../includes/banner.md)]

Функция `CONCATENATE` возвращает все указанные строки текста как значение *Строка* после того, как они были объединены в одну строку.

## <a name="syntax"></a>Синтаксис

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a>Аргументы

`text 1`: *Строка*

Ссылка на источник данных типа данных *Строка*. Этот аргумент обязательный.

`text N`: *Строка*

Ссылка на источник данных типа данных *Строка*. Эти дополнительные аргументы являются необязательными.

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее текстовое значение.

## <a name="example"></a>Пример

`CONCATENATE ("abc", "def")` возвращает **"abcdef"**.

## <a name="usage-notes"></a>Примечания по использованию

Выражение `"abc" & "def"` также возвращает **"abcdef"**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Текстовые функции](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]