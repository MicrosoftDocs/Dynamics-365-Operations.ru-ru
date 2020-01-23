---
title: Функция ER GUIDVALUE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности GUIDVALUE.
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
ms.openlocfilehash: be5e8e7625d0226c9eb59efd3217fce7b8eba086
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915702"
---
# <a name="GUIDVALUE">Функция ER GUIDVALUE</a>

[!include [banner](../includes/banner.md)]

Функция `GUIDVALUE` преобразует заданный ввод типа *Строка* в элемент данных типа *GUID*.

## <a name="syntax"></a>Синтаксис

```
GUIDVALUE (input)
```

## <a name="arguments"></a>Аргументы

`input`: *Строка*

Действительный путь источника данных типа *Строка*.

## <a name="return-values"></a>Возвращаемые значения

*GUID*

Результирующе значение глобально уникального кода (GUID).

## <a name="usage-notes"></a>Примечания по использованию

Чтобы выполнить преобразование в обратном направлении (то есть, для преобразования указанного ввода с типом данных *GUID* в элемент данных с типом данных *Строка*), можно использовать функцию [TEXT](er-functions-text-text.md).

## <a name="example"></a>Пример

Определите следующие источники данных в соответствии вашей модели:

- Источник данных **myID** типа *Вычисляемое поле*, содержащий выражение `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`
- Источник данных **Users** типа *Записи таблицы*, который относится к таблице UserInfo

Затем можно использовать такое выражение, как `FILTER (Users, Users.objectId = myID)` для фильтрации таблицы UserInfo по полю **objectId** типа данных *GUID*.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Текстовые функции](er-functions-category-text.md)
