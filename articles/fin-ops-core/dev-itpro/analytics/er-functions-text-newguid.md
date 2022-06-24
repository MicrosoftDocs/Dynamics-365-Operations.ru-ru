---
title: Функция ER NEWGUID
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) NEWGUID.
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
ms.openlocfilehash: 321e2eda4accf9c8fe33b5a4c092c7be55276f26
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861826"
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
