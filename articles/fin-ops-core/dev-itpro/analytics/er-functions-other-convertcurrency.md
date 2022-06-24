---
title: Функция ER CONVERTCURRENCY
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) CONVERTCURRENCY.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: e51086d977652e4be4c19390a824d4f4507b60d3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898472"
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