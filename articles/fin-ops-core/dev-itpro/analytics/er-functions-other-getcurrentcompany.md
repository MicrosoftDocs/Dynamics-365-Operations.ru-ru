---
title: Функция ER GETCURRENTCOMPANY
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) GETCURRENTCOMPANY.
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
ms.openlocfilehash: 06d552a0e8241d416fc49c4377b02f90fdf63d29
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872752"
---
# <a name="getcurrentcompany-er-function"></a>Функция ER GETCURRENTCOMPANY

[!include [banner](../includes/banner.md)]

Функция `GETCURRENTCOMPANY` возвращает *строковое* значение, представляющее код для юридического лица (компании), в которую выполнил вход пользователь.

## <a name="syntax"></a>Синтаксис

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее текстовое значение.

## <a name="example"></a>Пример

`GETCURRENTCOMPANY ()` возвращает **USMF** для пользователя, выполнившего вход в компанию **Contoso Entertainment System USA**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Другие функции (характерные для конкретных бизнес-доменов)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]