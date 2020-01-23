---
title: Функция ER LEFT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности LEFT
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 8280a05ea180d9de499d87efa53eca8ca912b0e3
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915656"
---
# <a name="LEFT">Функция ER LEFT</a>

[!include [banner](../includes/banner.md)]

Функция `LEFT` возвращает *строковое* значение, которое представляет указанное число символов от начала указанной строки.

## <a name="syntax"></a>Синтаксис

```
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
