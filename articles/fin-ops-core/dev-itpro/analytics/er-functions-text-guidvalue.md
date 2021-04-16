---
title: Функция ER GUIDVALUE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности GUIDVALUE.
author: NickSelin
ms.date: 12/12/2019
ms.topic: article
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
ms.openlocfilehash: ec8222708b999a17794a396b5bf807dab037799d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746395"
---
# <a name="guidvalue-er-function"></a>Функция ER GUIDVALUE

[!include [banner](../includes/banner.md)]

Функция `GUIDVALUE` преобразует заданный ввод типа *Строка* в элемент данных типа *GUID*.

## <a name="syntax"></a>Синтаксис

```vb
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]