---
title: Функция ER CHAR
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности CHAR
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d42afcf97690351763138fd9e16265aa104a6bc4
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915748"
---
# <a name="CHAR">Функция ER CHAR</a>

[!include [banner](../includes/banner.md)]

Функция `CHAR` возвращает *строковое* значение, которое представляет один символ, на который ссылается указанный номер Unicode.

## <a name="syntax"></a>Синтаксис

```
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
