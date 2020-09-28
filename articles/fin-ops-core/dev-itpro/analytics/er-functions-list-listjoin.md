---
title: Функция STRINGJOIN электронной отчетности
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности LISTJOIN.
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 035bf720a892e987ff9fc073ab8ed6f6cc6ea18e
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745113"
---
# <a name="listjoin-er-function"></a>Функция STRINGJOIN электронной отчетности

[!include [banner](../includes/banner.md)]

Функция `LISTJOIN` возвращает значение *Список записей*, представляющее новый объединенный список записей, созданный из указанных аргументов.

## <a name="syntax"></a>Синтаксис

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a>Аргументы

`list 1`: *Список записей*

Ссылка на источник данных типа данных *Список записей*. Этот аргумент является обязательным.

`list N`: *Список записей*

Ссылка на источник данных типа данных *Список записей*. Эти дополнительные аргументы являются необязательными.

## <a name="return-values"></a>Возвращаемые значения

*Список записей*

Полученный список записей.

## <a name="usage-notes"></a>Примечания по использованию

Структура создаваемого списка содержит только поля, представленные в структуре каждого списка записей, указанных в аргументах.

## <a name="example"></a>Пример

Вы вводите источник данных **Запись 1** типа `Container`. Этот источник данных содержит следующие вложенные поля типа `Calculated field`:

- **Код:** это поле содержит выражение, возвращающее значение типа `String`.
- **Сумма**: это поле содержит выражение, возвращающее значение типа `Real`.

Вы затем вводите источник данных **Запись 2** типа `Container`. Этот источник данных содержит следующие вложенные поля типа `Calculated field`:

- **Сумма**: это поле содержит выражение, возвращающее значение типа `Real`.
- **IsValid**: это поле содержит выражение, возвращающее значение типа `Boolean`.

![Страница конструктора сопоставления модели электронной отчетности](./media/er-functions-list-listjoin-image1.gif)

В этом случае выражение `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` возвращает новый список, содержащий две записи.

![Страница конструктора сопоставления моделей электронной отчетности с двумя записями](./media/er-functions-list-listjoin-image2.gif)

Структура этого списка состоит из одного поля **Сумма** типа `Real`, потому что это поле является единственным полем, которое представлено в каждом аргументе вызываемой функции.

![Поле суммы страницы конструктора сопоставления модели электронной отчетности](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции для работы со списками](er-functions-category-list.md)

[Отладка источников данных для выполняемого формата электронной отчетности для анализа потока и преобразования данных](er-debug-data-sources.md)
