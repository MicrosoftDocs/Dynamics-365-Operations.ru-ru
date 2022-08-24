---
title: Функция ER NUMERALSTOTEXT
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) NUMERALSTOTEXT.
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
ms.openlocfilehash: 172693583699edfad7deeb16f8fc081abb6119d5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287999"
---
# <a name="numeralstotext-er-function"></a>Функция ER NUMERALSTOTEXT

[!include [banner](../includes/banner.md)]

Функция `NUMERALSTOTEXT` возвращает указанное число в качестве *строкового* значения после того, как оно было преобразовано в текст (т.е. преобразовано в строки текста) на указанном языке.

## <a name="syntax"></a>Синтаксис

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a>Аргументы

`number`: *Целочисленный* или *Вещественный*

Числовое значение, которое определяет число, которое должно быть преобразовано в текст.

`language`: *Строка*

*Строковое* значение, представляющее код языка.

`currency`: *Строка*

*Строковое* значение, представляющее код валюты.

`print currency name flag`: *Логический*

*Логическое* значение, указывающее, следует ли добавить название валюты в написанный текст.

`decimal points`: *Целочисленный*

*Целочисленное* значение, которое указывает число десятичных знаков для написанного текста.

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее текстовое значение.

## <a name="usage-notes"></a>Примечания по использованию

Код языка указывать необязательно. Если он определен как пустая строка, вместо него используется код языка для контекста выполнения. Код языка по умолчанию — **EN-US**. Код языка для выполняющегося контекста определяется в элементе **Папка** или **Файл** в выполняющемся формате электронной отчетности (ER).

Код валюты указывать необязательно. Если он определен как пустая строка, вместо него используется валюта компании для контекста выполнения.

> [!NOTE] 
> Аргументы `print currency name flag` и `decimal points` анализируются только для следующих кодов языка: **CS**, **ET**, **HU**, **LT**, **LV**, **PL** и **RU**. Кроме того, аргумент `print currency name flag` анализируется только для компаний, в которых контекст страны или региона поддерживает склонение названий валюты.

## <a name="example-1"></a>Пример 1

`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` возвращает **"One Thousand Two Hundred Thirty Four and 56"**.

## <a name="example-2"></a>Пример 2

`NUMERALSTOTEXT (120, "PL", "", false, 0)` возвращает **"Sto dwadzieścia"**. 

## <a name="example-3"></a>Пример 3

`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` возвращает **"Сто двадцать евро 21 евроцент"**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Текстовые функции](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
