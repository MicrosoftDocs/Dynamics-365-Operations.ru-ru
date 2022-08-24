---
title: Функция ER LEFT
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) LEFT.
author: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 866c1b59fee9aa58afafbd82a83cff57e4cadeeb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268007"
---
# <a name="left-er-function"></a>Функция ER LEFT

[!include [banner](../includes/banner.md)]

Функция `LEFT` возвращает *строковое* значение, которое представляет указанное число символов от начала указанной строки.

## <a name="syntax"></a>Синтаксис

```vb
LEFT (text, number)
```

## <a name="arguments"></a>Аргументы

`text`: *Строка*

*Строковое* значение, представляющее исходный текст.

`number`: *Целочисленный*

Количество символов, которые должны быть возвращены с начала исходного текста.

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее текстовое значение.

## <a name="example"></a>Пример

`LEFT ("Sample", 3)` возвращает **"Sam"**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Текстовые функции](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
