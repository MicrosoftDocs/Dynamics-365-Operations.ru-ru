---
title: Функция ER ABS
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ABS.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: b53535d1a000b72577be5c6284cc4676c43d591b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744607"
---
# <a name="abs-er-function"></a>Функция ER ABS

[!include [banner](../includes/banner.md)]

Функция `ABS` возвращает абсолютное значение (модуль) указанного числа в качестве *вещественного* значения. Другими словами, возвращает число без знака.

## <a name="syntax"></a>Синтаксис

```vb
ABS (number)
```

## <a name="arguments"></a>Аргументы

`number`: *Вещественный*

Числовое значение, модуль которого вам нужен.

## <a name="return-values"></a>Возвращаемые значения

*Действующий*

Результирующее числовое значение.

## <a name="example"></a>Пример

`ABS (-1)` возвращает **1**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Математические функции](er-functions-category-mathematical.md)
