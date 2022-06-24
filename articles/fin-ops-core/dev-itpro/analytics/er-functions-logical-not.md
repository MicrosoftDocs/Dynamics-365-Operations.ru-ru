---
title: Функция ER NOT
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) NOT.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: da30e9a0092f594da7cef7b425e2b89af7bda491
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890495"
---
# <a name="not-er-function"></a>Функция ER NOT

[!include [banner](../includes/banner.md)]

Функция `NOT` возвращает обратное логическое значение указанного условия в качестве *логического* значения.

## <a name="syntax"></a>Синтаксис

```vb
NOT (condition)
```

## <a name="arguments"></a>Аргументы

`condition`: *Логический*

Действительное условное выражение, которое должно быть реверсировано.

## <a name="return-values"></a>Возвращаемые значения

*Логический*

Результирующее *логическое* значение.

## <a name="example"></a>Пример

`NOT (TRUE)` возвращает **FALSE**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Логические функции](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]