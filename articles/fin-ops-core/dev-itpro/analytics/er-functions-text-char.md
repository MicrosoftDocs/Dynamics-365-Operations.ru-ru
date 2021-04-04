---
title: Функция ER CHAR
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности CHAR
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
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
ms.openlocfilehash: b008cf6ddf51d816a17e0fae1fa0db464adeabde
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563206"
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

Строка, возвращаемая этой функцией, зависит от кодировки, выбранной в родительском элементе формата **FILE**. Список поддерживаемых кодировок см. в разделе [Класс кодировки](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).

## <a name="example"></a>Пример

`CHAR (255)` возвращает **"ÿ"**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Текстовые функции](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]