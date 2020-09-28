---
title: Функция ER CH_BANK_MOD_10
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности CH_BANK_MOD_10.
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
ms.openlocfilehash: c18a7f96096fbc6bbc7b6d15135c11bd70960d26
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744478"
---
# <a name="ch_bank_mod_10-er-function"></a>Функция ER CH_BANK_MOD_10

[!include [banner](../includes/banner.md)]

Функция `CH_BANK_MOD_10` возвращает *строковое* значение, представляющее ссылку кредитора в качестве выражения MOD10, на основе цифр указанного номера счета-фактуры.

## <a name="syntax"></a>Синтаксис

```vb
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a>Аргументы

`invoice number digits`: *Строка*

Текстовое значение, представляющее цифры номера счета-фактуры.

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее текстовое значение.

## <a name="example"></a>Пример

`CH_BANK_MOD_10 ("VEND-200002")` возвращает **3**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Другие функции (характерные для конкретных бизнес-доменов)](er-functions-category-other.md)
