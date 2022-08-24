---
title: Функция ER LISTOFFIRSTITEM
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) LISTOFFIRSTITEM.
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
ms.openlocfilehash: dede32c58ef8dc67028ea17b8a26189f62f73593
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275596"
---
# <a name="listoffirstitem-er-function"></a>Функция ER LISTOFFIRSTITEM

[!include [banner](../includes/banner.md)]

Функция `LISTOFFIRSTITEM` возвращает значение *Список записей*, состоящее только из первой записи указанного списка.

## <a name="syntax"></a>Синтаксис

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a>Аргументы

`list`: *Список записей*

Действительный путь источника данных типа данных *Список записей*.

## <a name="return-values"></a>Возвращаемые значения

*Список записей*

Полученный список записей.

## <a name="example"></a>Пример

Выражение `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` возвращает значение текста **"A"**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции для работы со списками](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
