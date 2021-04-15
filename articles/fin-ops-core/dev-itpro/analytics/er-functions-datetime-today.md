---
title: Функция ER TODAY
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности TODAY.
author: NickSelin
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
ms.openlocfilehash: 45ee4282acf4d6a5febe4b74b6955410e73e86a3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746755"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]