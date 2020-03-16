---
title: Функция ER ISVALIDCHARACTERISO7064
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ISVALIDCHARACTERISO7064
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: c858ad72db7afe63baca8288f312548c4fc37d5c
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041408"
---
# <a name="ISVALIDCHARACTERISO7064">Функция ER ISVALIDCHARACTERISO7064</a>

[!include [banner](../includes/banner.md)]

Функция `ISVALIDCHARACTERISO7064` возвращает *логическое* значение **TRUE**, если указанная строка представляет допустимый международный номер банковского счета (IBAN). В противном случае возвращает *логическое* значение **FALSE**.

## <a name="syntax"></a>Синтаксис

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a>Аргументы

`text`: *Строка*

Текстовое значение, представляющее IBAN.

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее текстовое значение.

## <a name="example"></a>Пример

`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` возвращает **TRUE**. 

`ISVALIDCHARACTERISO7064 ("AT61")` возвращает **FALSE**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Другие функции (характерные для конкретных бизнес-доменов)](er-functions-category-other.md)
