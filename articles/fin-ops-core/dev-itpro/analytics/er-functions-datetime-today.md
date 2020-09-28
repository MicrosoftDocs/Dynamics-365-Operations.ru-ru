---
title: Функция ER TODAY
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности TODAY.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: e2ee153c1dde99810a78ed15c7505fa705088797
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745449"
---
# <a name="today-er-function"></a>Функция ER TODAY

[!include [banner](../includes/banner.md)]

Функция `TODAY` возвращает значение *Date*, которое представляет текущую дату сервера приложения.

## <a name="syntax"></a>Синтаксис

```xpp
TODAY ()
```

## <a name="return-values"></a>Возвращаемые значения

*Дата*

Результирующее значение даты.

## <a name="example"></a>Пример

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` возвращает текущую дату сервера приложений, 24 декабря 2015, как строку **"24-12-2015"**, на основе указанного настраиваемого формата.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции даты и времени](er-functions-category-datetime.md)
