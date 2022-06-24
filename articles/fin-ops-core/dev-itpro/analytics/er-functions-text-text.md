---
title: Функция ER TEXT
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) TEXT.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: bf9049463ca905952cab512884afad380b7b3d52
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900174"
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

Если для экземпляра Microsoft Dynamics 365 Finance определен языковой стандарт сервера **EN-US**, `TEXT (NOW ())` возвращает текущую дату сеанса Finance, 17 декабря 2015, как текстовую строку **"12/17/2015 07:59:23 AM"**. `TEXT (1/3)` возвращает **"0,33"**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Текстовые функции](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]