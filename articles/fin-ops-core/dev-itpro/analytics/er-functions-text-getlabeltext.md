---
title: Функция ER GETLABELTEXT
description: В этой статье представлена информация о том, как используется функция электронной отчетности (ER) GETLABELTEXT.
author: NickSelin
ms.date: 03/18/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: cb3af10d4725e87190f901aa99378e10bdf05bee
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877077"
---
# <a name="getlabeltext-er-function"></a>Функция ER GETLABELTEXT

[!include [banner](../includes/banner.md)]

Функция `GETLABELTEXT` выполняет поиск конкретной метки для возврата значения *[Строка](er-formula-supported-data-types-primitive.md#string)*, представляющего преобразование указанной метки на указанном языке.

## <a name="syntax"></a>Синтаксис

```vb
GETLABELTEXT (label id, language)
```

## <a name="arguments"></a>Аргументы

### <a name="label-id"></a>Код метки

`label id`: *Строка* или *Код метки*

Допустимый идентификатор одного из следующих типов метки:

- Метка [электронной отчетности (ER)](general-electronic-reporting.md)
- Метка Microsoft Dynamics 365 Finance

#### <a name="usage-notes"></a>Примечания по использованию

Этот аргумент может быть определен только как константа с помощью одного из следующих поддерживаемых шаблонов:

- Для меток ER:

    - `@"GER_LABEL:<LABEL ID>"`
    - `"GER_LABEL:<LABEL ID>"`

- Для меток Finance:

    - `@"<LABEL ID>"`
    - `"<LABEL ID>"`

> [!NOTE]
> Во время разработки сообщение об ошибке проверки отображается на странице **[Конструктор формул](er-advanced-formula-editor.md)**, если не удается найти метку, используя предоставленный идентификатор метки.

### <a name="language"></a>Язык

`language`: *Строка*

Строка, представляющая код языка.

#### <a name="usage-notes"></a>Примечания по использованию

Этот аргумент может быть определен либо как текстовая константа, либо как путь к полю источника данных, который возвращает *строковое* значение.

> [!NOTE]
> Во время разработки выводится сообщение об ошибке проверки, если не удается найти код языка с помощью предоставленного аргумента `language`, если он был определен как текстовая константа.
>
> Во время выполнения перевод для системного языка `EN-US` возвращается для указанной метки, если не найден код языка с помощью предоставленного аргумента `language`.

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее текстовое значение.

## <a name="example-1-system-label"></a><a name=example-1></a>Пример 1. Метка системы

Выражения `GETLABELTEXT (@"SYS70894", "en-us")` и `GETLABELTEXT ("SYS70894", "en-us")` возвращают английский перевод для метки приложения `@SYS70894` "Nothing to print".

## <a name="example-2-er-label"></a><a name=example-2></a>Пример 2. Метка ER

Пользователь начинает редактировать [конфигурацию](general-electronic-reporting.md#Configuration) ER, которая была [унаследована](er-quick-start2-customize-report.md#DeriveProvidedFormat) из конфигурации **Перенос кредита ISO20022 (DE)**, введите новый источник данных типа *[Вычисляемое поле](er-calculated-field-ds-performance.md)* и настройте выражение `GETLABELTEXT(@"GER_LABEL:VendorName", "de")` для этого источника данных. В этом случае, при выполнении источник данных возвращает немецкий перевод "Kreditorenname" для метки ER `@GER_LABEL:VendorName`, которая первоначально была настроена в базовой конфигурации ER **Перенос кредита ISO20022 (DE)**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Текстовые функции](er-functions-category-text.md)

[Разработка многоязычных отчетов в электронной отчетности](er-design-multilingual-reports.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
