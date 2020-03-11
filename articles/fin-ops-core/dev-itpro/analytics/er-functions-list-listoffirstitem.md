---
title: Функция ER LISTOFFIRSTITEM
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности LISTOFFIRSTITEM.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8cd48732280c9af0b89129a32b42285207f97fb7
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041983"
---
# <a name="LISTOFFIRSTITEM">Функция ER LISTOFFIRSTITEM</a>

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
