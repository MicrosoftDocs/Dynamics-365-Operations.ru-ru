---
title: Функция ER ISEMPTY
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) ISEMPTY.
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
ms.openlocfilehash: e1f1ac1cc1729ef6d0f0301f12cc3f4b07fc6110
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273229"
---
# <a name="isempty-er-function"></a>Функция ER ISEMPTY

[!include [banner](../includes/banner.md)]

Функция `ISEMPTY` возвращает *логическое* значение **TRUE**, если указанный список не содержит записей. В противном случае возвращает *логическое* значение **FALSE**.

## <a name="syntax"></a>Синтаксис

```vb
ISEMPTY (list)
```

## <a name="arguments"></a>Аргументы

`list`: *Список записей*

Действительный путь источника данных типа данных *Список записей*.

## <a name="return-values"></a>Возвращаемые значения

*Логический*

Результирующее *логическое* значение.

## <a name="example-1"></a>Пример 1

Если вы введете источник данных **DS** типа *Вычисляемое поле* и он содержит выражение `SPLIT ("A|B|C", "|")`, выражение `ISEMPTY(DS)` возвращает **FALSE**.

## <a name="example-2"></a>Пример 2

Выражение `ISEMPTY (SPLIT ("",1))` возвращает **TRUE**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции для работы со списками](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
