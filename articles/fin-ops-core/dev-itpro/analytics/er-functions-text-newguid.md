---
title: Функция ER NEWGUID
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) NEWGUID.
author: kfend
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-09-08
ms.dyn365.ops.version: AX 10.0.23
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 381dbcbe816c189c1966ffe962020d5aa2b1f3eb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274783"
---
# <a name="newguid-er-function"></a>Функция ER NEWGUID

[!include [banner](../includes/banner.md)]

Функция `NEWGUID` создает новый глобальный уникальный идентификатор (GUID) и возвращает его в виде значения *[GUID](er-formula-supported-data-types-primitive.md#guid)*.

## <a name="syntax"></a>Синтаксис

```vb
NEWGUID ()
```

## <a name="return-values"></a>Возвращаемые значения

*GUID*

Результирующее значение GUID.

## <a name="example"></a>Пример

`NEWGUID()` всегда возвращает новое значение *GUID*, например **3afcf7ff-af10-ec11-b6e6-000d3a13209e**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Текстовые функции](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
