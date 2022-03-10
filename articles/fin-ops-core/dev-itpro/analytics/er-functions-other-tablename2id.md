---
title: Функция ER TABLENAME2ID
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности TABLENAME2ID
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: a500eda75fbb5867f74b56753ee45016c60803b06f508340540764a6cd0399cc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725242"
---
# <a name="tablename2id-er-function"></a>Функция ER TABLENAME2ID

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]