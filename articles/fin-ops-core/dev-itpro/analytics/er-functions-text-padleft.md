---
title: Функция ER PADLEFT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности PADLEFT.
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
ms.openlocfilehash: 3f8a8e2006fe279b25bbf154c6e1802babf51117
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744367"
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
