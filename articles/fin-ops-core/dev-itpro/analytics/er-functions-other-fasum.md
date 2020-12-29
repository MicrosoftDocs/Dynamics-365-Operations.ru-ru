---
title: Функция ER FA_SUM
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности FA_SUM
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c46f945a9caae2836886d051da820658e8be9af
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687704"
---
# <a name="fa_sum-er-function"></a>Функция ER FA_SUM

[!include [banner](../includes/banner.md)]

Функция `FA_SUM` возвращает значение *Контейнер (запись)*, которое состоит из данных сумм основных средств для указанного элемента основных средств, кода модели стоимости и периода дат.

## <a name="syntax"></a>Синтаксис

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a>Аргументы

`fixed asset code`: *Строка*

Значение *строка*, представляющее код элемента основного средства, для которого рассчитывается сальдо.

`value model code`: *Строка*

Значение *строка*, представляющее код модели стоимости, для которого рассчитывается сальдо.

`start date`: *Дата*

Значение *Дата*, представляющее дату начала периода, для которого рассчитываются суммы основного средства.

`end date`: *Дата*

Значение *Дата*, представляющее дату окончания периода, для которого рассчитываются суммы основного средства.

## <a name="return-values"></a>Возвращаемые значения

*Контейнер (запись)*

Результирующее значение записи.

## <a name="example"></a>Пример

`FA_SUM ("COMP-000001", "Current", Date1, Date2)` возвращает контейнер данных для основного средства **COMP-000001**, которое было подготовлено для модели стоимости **Current** и за период с **Date1** по **Date2**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Другие функции (характерные для конкретных бизнес-доменов)](er-functions-category-other.md)
