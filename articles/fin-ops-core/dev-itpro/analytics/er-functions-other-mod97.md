---
title: Функция ER MOD_97
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) MOD_97.
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
ms.openlocfilehash: f57b55a9c4182b411e098ebce2f36b78ef03b6f8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898443"
---
# <a name="mod_97-er-function"></a>Функция ER MOD_97

[!include [banner](../includes/banner.md)]

Функция `MOD_97` возвращает *строковое* значение, представляющее ссылку кредитора в качестве выражения MOD97, на основе цифр указанного номера счета-фактуры.

## <a name="syntax"></a>Синтаксис

```vb
MOD_97 (invoice number digits)
```

## <a name="arguments"></a>Аргументы

`invoice number digits`: *Строка*

Текстовое значение, представляющее цифры номера счета-фактуры.

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее текстовое значение.

## <a name="example"></a>Пример

`MOD_97 ("VEND-200002")` возвращает **"20000285"**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Другие функции (характерные для конкретных бизнес-доменов)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]