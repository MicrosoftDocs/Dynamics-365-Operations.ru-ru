---
title: Функция ER NEWGUID
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности NEWGUID.
author: NickSelin
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-09-08
ms.dyn365.ops.version: AX 10.0.23
ms.openlocfilehash: 5856a4d765f5136ecb11a34e0255c1ba88818f2c
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647954"
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
