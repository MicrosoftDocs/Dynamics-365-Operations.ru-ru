---
title: Функция ER CONVERTCURRENCY
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности CONVERTCURRENCY.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 0f0d5bace9b62cf6f0d7576744a6cc271666bf73
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567648"
---
# <a name="convertcurrency-er-function"></a>Функция ER CONVERTCURRENCY

[!include [banner](../includes/banner.md)]

Функция `CONVERTCURRENCY` возвращает *вещественное* значение, представляющее результат преобразования указанной денежной суммы от указанной валюты источника в указанную целевую валюту, используя настройки определенной компании на указанную дату.

## <a name="syntax"></a>Синтаксис

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a>Аргументы

`amount`: *Целочисленный* или *Вещественный*

Числовое значение, представляющее денежную сумму, которая должна быть конвертирована.

`source currency`: *Строка*

Код исходной валюты.

`target currency`: *Строка*

Код целевой валюты.

`date`: *Дата*

Значение *Дата*, представляющее дату, используемую для определения валютного курса для конвертации.

`company`: *Строка*

Значение *строка*, представляющее код компании, которая представляет параметры, используемые для конвертации.

## <a name="return-values"></a>Возвращаемые значения

*Действующий*

Результирующее числовое значение.

## <a name="example"></a>Пример

`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` возвращает эквивалент одного евро в долларах США на текущую дату сеанса на основе настроек для компании **DEMF**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Другие функции (характерные для конкретных бизнес-доменов)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]