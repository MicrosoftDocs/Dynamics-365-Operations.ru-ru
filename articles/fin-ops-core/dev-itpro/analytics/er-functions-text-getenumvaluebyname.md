---
title: Функция ER GETENUMVALUEBYNAME
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности GETENUMVALUEBYNAME.
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
ms.openlocfilehash: 33ccf358dc5355cd00d5ff41ebd8148a334cba38
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743863"
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

## <a name="example"></a>Пример

На следующем рисунке показано перечисление **ReportDirection** введенное в модели данных. Обратите внимание, что метки определены для значений перечисления.

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

Следующая иллюстрация показывает эти детали:

- Источник данных **$Direction** настроен в отчете ER. Этот источник данных настроен на основе перечисления модели **ReportDirection**.
- Выражение `$IsArrivals` разработано для использования модели на основе перечисления для источника данных **$Direction** в качестве параметра этой функции.
- Значение этого выражения сравнения — **TRUE**.

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a>Дополнительные ресурсы

[Текстовые функции](er-functions-category-text.md)
