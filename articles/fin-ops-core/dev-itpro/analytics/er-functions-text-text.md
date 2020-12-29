---
title: Функция ER TEXT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности TEXT
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: d489da24d0589549153913bbc6db699e3c217e72
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682903"
---
# <a name="text-er-function"></a>Функция ER TEXT

[!include [banner](../includes/banner.md)]

Функция `TEXT` возвращает указанное число в качестве *строкового* значения после его преобразования в текстовую строку, которая отформатирована в соответствии с параметрами языкового стандарта сервера текущего экземпляра приложения.

## <a name="syntax"></a>Синтаксис

```vb
TEXT (number)
```

## <a name="arguments"></a>Аргументы

`number`: *Целочисленный* или *Вещественный*

Число, которое должно быть преобразовано в текстовую строку.

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее текстовое значение.

## <a name="usage-notes"></a>Примечания по использованию

Для значений типа *Вещественный* преобразование строки ограничено до двух десятичных знаков.

## <a name="example"></a>Пример

Если языковой стандарт экземпляра сервера Microsoft Dynamics 365 Finance определен как **EN-US**, `TEXT (NOW ())` возвращает текущую дату сеанса Finance, 17 декабря 2015, как текстовую строку **"12/17/2015 07:59:23 AM"**. `TEXT (1/3)` возвращает **"0,33"**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Текстовые функции](er-functions-category-text.md)
