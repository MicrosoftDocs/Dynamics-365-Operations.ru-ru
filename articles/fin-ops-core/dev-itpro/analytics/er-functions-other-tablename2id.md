---
title: Функция ER TABLENAME2ID
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) TABLENAME2ID.
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: fe7ed336f2264e15e0a8a7305e1bcebb75b2cd07
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268067"
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

Выполнение этой функции может давать разные результаты в разных экземплярах Microsoft Dynamics 365 Finance, даже если используется одно и то же название компании.

## <a name="example"></a>Пример

`TABLENAME2ID ("Intrastat")` возвращает **1510**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Другие функции (характерные для конкретных бизнес-доменов)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
