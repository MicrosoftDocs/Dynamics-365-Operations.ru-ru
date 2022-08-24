---
title: Функция ER CHAR
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) CHAR.
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 61e402718723325fc975d577ab76039e3e59691e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288059"
---
# <a name="char-er-function"></a>Функция ER CHAR

[!include [banner](../includes/banner.md)]

Функция `CHAR` возвращает *строковое* значение, которое представляет один символ, на который ссылается указанный номер Unicode.

## <a name="syntax"></a>Синтаксис

```vb
CHAR (number)
```

## <a name="arguments"></a>Аргументы

`number`: *Целочисленный*

Номер, соответствующий ожидаемому одному символу.

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее текстовое значение.

## <a name="usage-notes"></a>Примечания по использованию

Строка, возвращаемая этой функцией, зависит от кодировки, выбранной в родительском элементе формата **FILE**. Список поддерживаемых кодировок см. в разделе [Класс кодировки](/dotnet/api/system.text.encoding).

## <a name="example"></a>Пример

`CHAR (255)` возвращает **"ÿ"**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Текстовые функции](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
