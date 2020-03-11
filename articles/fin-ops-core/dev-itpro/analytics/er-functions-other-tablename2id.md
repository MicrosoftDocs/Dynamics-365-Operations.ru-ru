---
title: Функция ER TABLENAME2ID
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности TABLENAME2ID
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 951de1d1505508ebb6abeff5b80ecef10573e117
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041280"
---
# <a name="TABLENAME2ID">Функция ER TABLENAME2ID</a>

[!include [banner](../includes/banner.md)]

Функция `TABLENAME2ID` возвращает числовое представление идентификатора таблицы для указанного имени таблицы в качестве *целочисленного* значения.

## <a name="syntax"></a>Синтаксис

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a>Аргументы

`text`: *Строка*

Текстовое значение, представляющее действительное имя таблицы.

## <a name="return-values"></a>Возвращаемые значения

*Целочисленный*

Результирующее числовое значение.

## <a name="usage-notes"></a>Примечания по использованию

Выполнение этой функции может привести к различным результатам в разных экземплярах Microsoft Dynamics 365 Finance, даже если используется одно и то же название компании.

## <a name="example"></a>Пример

`TABLENAME2ID ("Intrastat")` возвращает **1510**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Другие функции (характерные для конкретных бизнес-доменов)](er-functions-category-other.md)
