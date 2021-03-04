---
title: Функция ER LIST
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности LIST
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7f8e701ec2836206d2299abba5e5b8542b4cf92
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683095"
---
# <a name="list-er-function"></a>Функция ER LIST

[!include [banner](../includes/banner.md)]

Функция `LIST` возвращает значение *Список записей*, состоящее из нового списка записей, созданного из указанных аргументов.

## <a name="syntax"></a>Синтаксис

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a>Аргументы

`record 1`: *Контейнер (запись)*

Ссылка на источник данных типа данных *Запись*. Этот аргумент обязательный.

`record N`: *Контейнер (запись)*

Ссылка на источник данных типа данных *Запись*. Эти дополнительные аргументы являются необязательными.

## <a name="return-values"></a>Возвращаемые значения

*Список записей*

Полученный список записей.

## <a name="usage-notes"></a>Примечания по использованию

Структура создаваемого списка содержит только поля, представленные в структуре каждой записи, упомянутой в аргументах.

## <a name="example"></a>Пример

Вы вводите источник данных **Запись 1** типа *Контейнер*. Этот источник данных содержит следующие вложенные поля типа *Вычисляемое поле*:

- **Код**: это поле содержит выражение, возвращающее значение типа *Строка*.
- **Сумма**: это поле содержит выражение, возвращающее значение типа *вещественное*.

Затем вы вводите источник данных **Запись 2** типа *Контейнер*. Этот источник данных содержит следующие вложенные поля типа *Вычисляемое поле*:

- **Сумма**: это поле содержит выражение, возвращающее значение типа *вещественное*.
- **IsValid**: это поле содержит выражение, возвращающее значение типа *логическое*.

В этом случае выражение `LIST('Record 1', 'Record 2')` возвращает новый список, содержащий две записи. Структура этого списка состоит из единого поля **Сумма** типа *Вещественное*, потому что это поле является единственным полем, которое представлено в каждом аргументе вызываемой функции.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции для работы со списками](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]