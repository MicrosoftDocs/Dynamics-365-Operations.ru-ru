---
title: Функция ER SPLIT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности SPLIT.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: e1f11d68b697fdd363f429e60a79f1e1f97bab5b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686400"
---
# <a name="split-er-function"></a>Функция ER SPLIT

[!include [banner](../includes/banner.md)]

Функция `SPLIT` разделяет указанную строку ввода на подстроки и возвращает результат в виде нового значения *Список записей*.

## <a name="syntax-1"></a>Синтаксис 1

```vb
SPLIT (input, length)
```

Этот синтаксис используется для разделения указанной строки ввода на подстроки, каждая из которых имеет заданную длину.

## <a name="syntax-2"></a>Синтаксис 2

```vb
SPLIT (input, delimiter)
```

Этот синтаксис используется для разделения указанной строки ввода на подстроки на основе указанного разделителя.

## <a name="arguments"></a>Аргументы

`input`: *Строка*

Текст для разделения.

`length`: *Целочисленный*

Максимальная длина одной подстроки.

`delimiter`: *Строка*

Разделитель, который используется для разделения подстрок.

## <a name="return-values"></a>Возвращаемые значения

*Список записей*

Полученный список записей.

## <a name="usage-notes"></a>Примечания по использованию

Структура записи возвращенного списка состоит из поля **Значение** типа *Строка*. Каждая запись возвращаемого списка содержит созданные подстроки в этом поле.

Если аргумент `delimiter` пуст, новый возвращаемый список состоит из одной записи с полем **Значение** типа *Строка*. Это поле содержит введенный текст.

Если аргумент `input` пуст, возвращается новый пустой список. Если аргумент `input` или `delimiter` не указан (null), возникает исключение приложения.

## <a name="example-1"></a>Пример 1

`SPLIT ("abcd", 3)` возвращает новый список, который состоит из двух записей с полем **Значение** типа *Строка*. Поле **Значение** в первой записи содержит текст **"abc"**, и поле **Значение** во второй записи содержит текст **"d"**.

## <a name="example-2"></a>Пример 2

`SPLIT ("XAb aBy", "aB")` возвращает новый список, который состоит из трех записей с полем **Значение** типа *Строка*. Поле **Значение** в первой записи содержит текст **"X"**, поле **Значение** во второй записи содержит текст **"&nbsp;"**, и поле **Значение** в третьей записи содержит текст **"y"**. 

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции для работы со списками](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]