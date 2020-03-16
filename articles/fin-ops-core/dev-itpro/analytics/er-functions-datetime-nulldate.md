---
title: Функция ER NULLDATE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности NULLDATE.
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
ms.openlocfilehash: 24a295a6ad8aca7718e60dd351248c9fbfdafee8
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042328"
---
# <a name="NULLDATE">Функция ER NULLDATE</a>

[!include [banner](../includes/banner.md)]

Функция `NULLDATE` возвращает значение *Date*, которое представляет **нулевую** дату (1 января 1900 года).

## <a name="syntax"></a>Синтаксис

```vb
NULLDATE () as 
```

## <a name="return-values"></a>Возвращаемые значения

*Дата*

Результирующее значение даты.

## <a name="example-1"></a>Пример 1

`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` возвращает **нулевую** дату, 1 января 1900 года, как **"1900-01-01"**, на основе указанного пользовательского формата.

## <a name="example-2"></a>Пример 2

Выражение `IF( Invoice.DocumentDate = NULLDATE(), true, false)` возвращает **True**, когда значение поля **DocumentDate** равняется **нулевой** дате. В этом примере **Invoice** представляет собой источник данных электронной отчетности (ER) типа **Записи Finance/Table** и ссылается на таблицу CustInvoiceJour.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции даты и времени](er-functions-category-datetime.md)
