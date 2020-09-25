---
title: Функция ER CURCREDREF
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности CURCREDREF.
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
ms.openlocfilehash: 95e90289f43896b83ba98a6edefe0cd6028f4043
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744199"
---
# <a name="curcredref-er-function"></a>Функция ER CURCREDREF

[!include [banner](../includes/banner.md)]

Функция `CURCREDREF` возвращает *строковое* значение, представляющее ссылку кредитора на основе цифр указанного номера счета-фактуры.

## <a name="syntax"></a>Синтаксис

```vb
CURCREDREF (invoice number digits)
```

## <a name="arguments"></a>Аргументы

`invoice number digits`: *Строка*

Текстовое значение, представляющее цифры номера счета-фактуры.

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее текстовое значение.

## <a name="example"></a>Пример

`CURCredRef ("VEND-200002")` возвращает **"2200002"**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Другие функции (характерные для конкретных бизнес-доменов)](er-functions-category-other.md)
