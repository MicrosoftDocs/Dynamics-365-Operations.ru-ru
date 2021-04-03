---
title: Функция электронной отчетности STARTSWITH
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности STARTSWITH.
author: NickSelin
manager: kfend
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 22e99d9e131410820abd12536b8d4f3e868c6863
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557549"
---
# <a name="startswith-er-function"></a>Функция электронной отчетности STARTSWITH

[!include [banner](../includes/banner.md)]

Функция `STARTSWITH` определяет, содержит ли заданный ввод начинается заданным текстом. Это возвращает *логическое* значение **TRUE**, если заданный ввод начинается заданным текстом. В противном случае возвращает *логическое* значение **FALSE**.

## <a name="syntax"></a>Синтаксис

```vb
STARTSWITH (input, start text)
```

## <a name="arguments"></a>Аргументы

`input`: *Строка*

Допустимый путь к номенклатуре в источнике данных типа *Строка* или строковой константы, значение которого может начинаться с второго аргумента.

`start text`: *Строка*

Допустимый путь к источнику данных типа данных *Строка* или строковой константы, значение которого может быть в начале первого аргумента.

## <a name="return-values"></a>Возвращаемые значения

*Логический*

Результирующее *логическое* значение.

## <a name="usage-notes"></a>Примечания по использованию

Эта функция может использоваться для указания выражения условия функции [FILTER](er-functions-list-filter.md) только в том случае, если соответствующее сопоставление настроено в [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) для доступа к [Microsoft Dataverse](../data-entities/data-integration-cds.md). В противном случае исключение создается во время разработки. Полученное сообщение рекомендует использовать функцию [WHERE](er-functions-list-where.md) вместо функции `FILTER`.

## <a name="example-1"></a>Пример 1

Выражение `STARTSWITH ("abc", "d")` возвращает значение **FALSE**, в то время как выражение `STARTSWITH ("abc", "A")` возвращает значение **TRUE**.

## <a name="example-2"></a>Пример 2

Выражение `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` возвращает значение **TRUE**, если значение поля **адрес** в источнике данных **модель** начинается со строки **123 Coffee Street**. В противном случае возвращает **FALSE**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Логические функции](er-functions-category-logical.md)
