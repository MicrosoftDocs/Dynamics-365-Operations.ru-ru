---
title: Функция ER LISTOFFIRSTITEM
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) LISTOFFIRSTITEM.
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
ms.openlocfilehash: f4715becfb158826a2b5678aac6a58c987433192
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881169"
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