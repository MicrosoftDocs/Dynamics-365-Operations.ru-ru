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
ms.openlocfilehash: c7e9917dcdc45a52e0ad490f5fa194d5390cc437
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917427"
---
# <a name="TODAY">Функция ER TODAY</a>

[!include [banner](../includes/banner.md)]

Функция `TODAY` возвращает значение *Date*, которое представляет текущую дату сервера приложения.

## <a name="syntax"></a>Синтаксис

```
TODAY ()
```

## <a name="return-values"></a>Возвращаемые значения

*Дата*

Результирующее значение даты.

## <a name="example"></a>Пример

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` возвращает текущую дату сервера приложений, 24 декабря 2015, как строку **"24-12-2015"**, на основе указанного настраиваемого формата.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции даты и времени](er-functions-category-datetime.md)
