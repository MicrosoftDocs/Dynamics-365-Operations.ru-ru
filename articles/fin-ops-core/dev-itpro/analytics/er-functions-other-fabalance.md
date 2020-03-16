---
title: Функция ER FA_BALANCE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности FA_BALANCE.
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
ms.openlocfilehash: 76a087157ae53e2c571654ade7383d7bd7a005c3
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041454"
---
# <a name="FA_BALANCE">Функция ER FA_BALANCE</a>

[!include [banner](../includes/banner.md)]

Функция `FA_BALANCE` возвращает значение *Контейнер (запись)*, которое состоит из данных баланса основных средств для указанного элемента основных средств, кода модели стоимости, отчетного года и даты отчетности.

## <a name="syntax"></a>Синтаксис

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a>Аргументы

`fixed asset code`: *Строка*

Значение *строка*, представляющее код элемента основного средства, для которого рассчитывается сальдо.

`value model code`: *Строка*

Значение *строка*, представляющее код модели стоимости, для которого рассчитывается сальдо.

`reporting year`: *Значение перечисления*

Значения перечисления приложения **AssetYear**, определяющее период для расчета сальдо.

`reporting date`: *Дата*

Значение *Дата*, определяющее дату расчета сальдо.

## <a name="return-values"></a>Возвращаемые значения

*Контейнер (запись)*

Результирующее значение записи.

## <a name="example"></a>Пример

`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` возвращает подготовленный контейнер данных сальдо для основного средства **COMP-000001**, подготовленного с моделью стоимости **Current** для даты текущего сеанса приложения.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Другие функции (характерные для конкретных бизнес-доменов)](er-functions-category-other.md)
