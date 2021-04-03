---
title: Функция ER SESSIONTODAY
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности SESSIONTODAY.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: e6ad28e642fcfae3cfa2692a4e41b99fae7fc9df
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561358"
---
# <a name="sessiontoday-er-function"></a>Функция ER SESSIONTODAY

[!include [banner](../includes/banner.md)]

Функция `SESSIONTODAY` возвращает значение *Date*, которое представляет текущую дату сеанса приложения.

## <a name="syntax"></a>Синтаксис

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a>Возвращаемые значения

*Дата*

Результирующее значение даты.

## <a name="example"></a>Пример

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` возвращает текущую дату сеанса приложения, 24 декабря 2015 года, как строку **"24-12-2015"** на основе выбранной немецкой культуры и указанного формата.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции даты и времени](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]