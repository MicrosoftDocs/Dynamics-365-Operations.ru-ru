---
title: Функция ER REPEAT
description: В этой статье представлена информация об использовании функции электронной отчетности (ER) REPEAT.
author: NickSelin
ms.date: 08/01/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-06-01
ms.dyn365.ops.version: AX 10.0.29
ms.openlocfilehash: c56139a3c63b03f907b1dcbf4365990d2a13c35a
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220698"
---
# <a name="repeat-er-function"></a>Функция ER REPEAT

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Функция `REPEAT` создает запись, которая содержит поле со значением, соответствующим указанному вводу. Затем возвращается новый *Список записей* для записи, повторяемый указанное число раз.

## <a name="syntax"></a>Синтаксис

```vb
REPEAT (item, number)
```

## <a name="arguments"></a>Аргументы

`item`: Любой поддерживаемый [простой](er-formula-supported-data-types-primitive.md) или [составной](er-formula-supported-data-types-composite.md) тип данных

Повторяемое значение.

`number`: *Целочисленный*

Число повторов.

## <a name="return-values"></a>Возвращаемые значения

*Список записей*

Полученный список записей.

## <a name="usage-notes"></a>Примечания по использованию

Возвращаемый список повторяемых записей содержит следующие поля:

- Указанное значение (поле `Item`)
- Индекс текущей записи (поле `Number`)

> [!NOTE]
> Так как для этой функции используется нумерация, начинающаяся с единицы, поле `Number` имеет значение **1** для первой записи в полученном списке.

Эту функцию можно использовать для умножения существующих данных таким образом, чтобы можно было протестировать производительность и объем решений для [электронной отчетности (ER)](general-electronic-reporting.md) с помощью [Regression suite automation tool (RSAT)](../perf-test/rsat/rsat-overview.md).

## <a name="example"></a>Пример

Необходимо создать документ в формате XML, который должен содержать столько XML-элементов `Party`, сколько вы укажете в поле ввода данных в диалоговом окне в среде выполнения, прежде чем начнется выполнение формата ER.

На следующем рисунке показан [формат](er-overview-components.md#format-component) ER. В этом формате добавляется единственный XML-элемент `Party`, чтобы раскрыть свойства одной стороны.

<a href="./media/er-repeat-function-1.png"><img src="./media/er-repeat-function-1.png" alt="Format structure on the Format tab of the Format designer page." class="alignnone size-full" width="929" height="548" /></a>

На приведенном ниже рисунке показаны следующие настроенные источники данных:

- Источник данных `Party`, представляющий одну сторону. Поле `Party.Value` используется для вывода единого текстового значения.
- `NumberOfRepeats` — [источник данных](er-user-input-parameter-data-sources.md), используемый для предложения поля ввода данных в диалоговом окне в среде выполнения, чтобы можно было указать число сторон, которые должны быть введены в созданный документ.
- Источник данных `Party2` повторяет запись `Party` столько раз, сколько раз было указано в источнике данных `NumberOfRepeats`.

<a href="./media/er-repeat-function-2.png"><img src="./media/er-repeat-function-2.png" alt="Configured data sources on the Mapping tab of the Format designer page." class="alignnone size-full" width="1044" height="411" /></a>

На следующем рисунке показаны привязки данных для редактируемого формата ER, которые создаются для создания выходных данных в формате XML. Эти выходные данные представляют отдельные стороны как перечислимые узлы.

<a href="./media/er-repeat-function-3.png"><img src="./media/er-repeat-function-3.png" alt="Configured data bindings on the Mapping tab of the Format designer page." class="alignnone size-full" width="1051" height="417" /></a>

На следующем рисунке показан результат выполнения спроектированного формата, а значение `NumberOfRepeats` источника данных указывается как **5**.

<a href="./media/er-repeat-function-4.png"><img src="./media/er-repeat-function-4.png" alt="Result of running the format on a new web browser tab." class="alignnone wp-image-290711 size-full" width="400" height="380" /></a>

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции для работы со списками](er-functions-category-list.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
