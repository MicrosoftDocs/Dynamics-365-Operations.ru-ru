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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 20313133ce29b8d5048814ff78ce4ea4f5c54d4a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743696"
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
