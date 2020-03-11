---
title: Функция ER ISOCREDREF
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ISOCREDREF.
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
ms.openlocfilehash: dd692720872314d533274f392f84e5ac7d36c7c1
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041385"
---
# <a name="ISOCREDREF">Функция ER ISOCREDREF</a>

[!include [banner](../includes/banner.md)]

Функция `ISOCREDREF` возвращает *строковое* значение, представляющее ссылку кредитора международной организации по стандартизации (ISO) на основе цифр и алфавитных символов определенного номера счета-фактуры.

## <a name="syntax"></a>Синтаксис

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a>Аргументы

`invoice number digits`: *Строка*

Текстовое значение, представляющее цифры номера счета-фактуры.

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее текстовое значение.

## <a name="usage-notes"></a>Примечания по использованию

> [!NOTE] 
> Чтобы исключить символы из алфавитов, не совместимых с ISO, аргумент `invoice number digits` необходимо перевести до передачи к этой функции.

## <a name="example"></a>Пример

`ISOCredRef ("VEND-200002")` возвращает **"RF23VEND-200002"**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Другие функции (характерные для конкретных бизнес-доменов)](er-functions-category-other.md)
