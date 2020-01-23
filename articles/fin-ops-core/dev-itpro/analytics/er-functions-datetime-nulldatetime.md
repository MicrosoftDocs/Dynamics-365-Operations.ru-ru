---
title: Функция ER NULLDATETIME
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности NULLDATETIME.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 4165f6e064d12200907ac76b6779d35bc578daba
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917496"
---
# <a name="NULLDATETIME">Функция ER NULLDATETIME</a>

[!include [banner](../includes/banner.md)]

Функция `NULLDATETIME` возвращает значение *DateTime*, которое представляет значение **нулевой** даты/времени (1 января 1900 года) в формате UTC (Greenwich Mean Time \[GMT\]).

## <a name="syntax"></a>Синтаксис

```
NULLDATETIME ()
```

## <a name="return-values"></a>Возвращаемые значения

*DateTime*

Результирующее значение даты/времени.

## <a name="example"></a>Пример

`DATETIMEFORMAT( NULLDATETIME(), "O")` возвращает значение строки **1900-01-01T00:00:00.0000000+00:00**, когда оно называется во время процесса, инициированного пользователем приложения со значением часового пояса **(GMT) UTC** в разделе **Настройки языка и страны/региона**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции даты и времени](er-functions-category-datetime.md)
