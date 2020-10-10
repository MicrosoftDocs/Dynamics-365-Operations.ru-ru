---
title: Функция ER GETENUMVALUEBYNAME
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности GETENUMVALUEBYNAME.
author: NickSelin
manager: kfend
ms.date: 09/23/2020
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
ms.openlocfilehash: 722ea8ea233d617b0584e21e98073428f16c0801
ms.sourcegitcommit: ad5b7676fc1213316e478afcffbfaee7d813f3bb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/24/2020
ms.locfileid: "3885235"
---
# <a name="getenumvaluebyname-er-function"></a>Функция ER GETENUMVALUEBYNAME

[!include [banner](../includes/banner.md)]

Функция `GETENUMVALUEBYNAME` выполняет поиск определенного значения *Enum* в указанном источнике данных перечисления, используя имя перечисления, указанное как значение *строка*. При обнаружении значения *Enum* функция возвращает его. В противном случае функция возвращает значение перечисления **null**.

## <a name="syntax"></a>Синтаксис

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a>Аргументы

`enumeration data source path`: *Перечисление*

Действительный путь источника данных одного из следующих типов перечисления:

- Перечисление модели электронной отчетности (ER)
- Перечисление формата ER
- Перечисление Microsoft Dynamics 365 Finance

`enumeration value text`: *Строка*

Строковое значение, представляющее имя одного значения перечисления.

## <a name="return-values"></a>Возвращаемые значения

Обнуляемый *Enum*

Результирующее значение перечисления.

## <a name="usage-notes"></a>Примечания по использованию

Исключение не выдается, если значение *Enum* не найдено с помощью имени значения перечисления, указанного как значение *строки*.

## <a name="example-1"></a>Пример 1

На следующем рисунке показано перечисление **ReportDirection** введенное в модели данных. Обратите внимание, что метки определены для значений перечисления.

![Доступные значения для перечисления модели данных](./media/ER-data-model-enumeration-values.PNG)

Следующая иллюстрация показывает эти детали:

- Источник данных **$Direction** настроен в отчете ER. Этот источник данных настроен на основе перечисления модели **ReportDirection**.
- Выражение `$IsArrivals` разработано для использования модели на основе перечисления для источника данных **$Direction** в качестве параметра этой функции.
- Значение этого выражения сравнения — **TRUE**.

![Пример перечисления модели данных](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a>Пример 2

Функции `GETENUMVALUEBYNAME` и [`LISTOFFIELDS`](er-functions-list-listoffields.md) позволяют выбирать значения и метки поддерживаемых перечислений как текстовые значения. (Поддерживаемые перечисления: перечисления приложений, перечисления моделей данных и перечисления форматов.)

На следующем рисунке источник данных **TransType** вводится в сопоставлении модели. Этот источник данных относится к перечислению приложения **LedgerTransType**.

![Источник данных сопоставления модели, ссылающийся на перечисление приложения](./media/er-functions-text-getenumvaluebyname-example2-1.png)

На следующем рисунке показан источник данных **TransTypeList**, настроенный в сопоставлении модели. Этот источник данных настроен на основе перечисления приложения **TransType**. Функция `LISTOFFIELDS` используется для того, чтобы вернуть все значения перечисления в виде списка записей, содержащих поля. Таким образом предоставляются сведения о каждом значении перечисления.

> [!NOTE]
> Поле **EnumValue** настроено для источника данных **TransTypeList** с помощью выражения `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)`. Это поле возвращает значение перечисления для каждой записи в данном списке.

![Источник данных сопоставления модели, который возвращает все значения перечисления выбранного перечисления в виде списка записей](./media/er-functions-text-getenumvaluebyname-example2-2.png)

На следующем рисунке показан источник данных **VendTrans**, настроенный в сопоставлении модели. Этот источник данных возвращает записи проводок поставщика из таблицы приложения **VendTrans**. Тип книги учета каждой проводки определяется значением поля **TransType**.

> [!NOTE]
> Поле **TransTypeTitle** настроено для источника данных **VendTrans** с помощью выражения `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label`. Это поле возвращает метку значения перечисления текущей проводки в виде текста, если это значение перечисления доступно. В противном случае оно возвращает пустое значение.
>
> Поле **TransTypeTitle** связано с полем **LedgerType** модели данных, которое позволяет использовать эту информацию в любом формате электронной отчетности, который использует модель данных в качестве источника данных.

![Источник данных сопоставления модели, который возвращает проводки поставщика](./media/er-functions-text-getenumvaluebyname-example2-3.png)

На следующем рисунке показано, как можно использовать [отладчик источников данных](er-debug-data-sources.md) для проверки настроенного сопоставления модели.

![Проверка настроенного сопоставления модели с помощью отладчика источника данных](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

Поле **LedgerType** модели данных предоставляет метки типов проводок, как и ожидается.

Если планируется использовать этот подход для больших объемов данных по проводкам, следует рассмотреть производительность выполнения. Дополнительные сведения см. в разделе [Трассировка выполнения форматов электронной отчетности для устранения неполадок, связанных с производительностью](trace-execution-er-troubleshoot-perf.md).

## <a name="additional-resources"></a>Дополнительные ресурсы

[Текстовые функции](er-functions-category-text.md)

[Трассировка выполнения форматов электронной отчетности для устранения неполадок, связанных с производительностью](trace-execution-er-troubleshoot-perf.md)

[Функция ER LISTOFFIELDS](er-functions-list-listoffields.md)

[Функция ER FIRSTORNULL](er-functions-list-firstornull.md)

[Функция ER WHERE](er-functions-list-where.md)
