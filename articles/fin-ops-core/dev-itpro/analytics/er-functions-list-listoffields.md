---
title: Функция ER LISTOFFIELDS
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности LISTOFFIELDS.
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
ms.openlocfilehash: 0d51b59c437bd216c6d229546136bb604239fa92
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042006"
---
# <a name="LISTOFFIELDS">Функция ER LISTOFFIELDS</a>

[!include [banner](../includes/banner.md)]

Функция `LISTOFFIELDS` возвращает значение *Список записей*, созданное на основе структуры указанного аргумента типа *Перечисление* или *Контейнер (запись)*.

## <a name="syntax-1"></a>Синтаксис 1

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a>Синтаксис 2

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a>Аргументы

`path`: Ссылка на источник данных

Действительный путь ссылки источника данных одного из следующих типов данных:

- Перечисление модели
- Перечисление форматов
- Перечисление приложений
- Контейнер (запись)

`language`: *Строка*

Текст, представляющий код языка.

## <a name="return-values"></a>Возвращаемые значения

*Список записей*

Полученный список записей.

## <a name="usage-notes"></a>Примечания по использованию

Созданный список состоит из записей, которые имеют следующие поля:

- **Имя** (тип данных *Строка*)
- **Метка** (тип данных *Строка*)
- **Описание** (тип данных *Строка*)
- **IsTranslated** (тип данных *Логический*)

Если аргумент `path` относится к источнику данных типа *Контейнер (запись)*, для каждого поля записи контейнера, на которую есть ссылка , новая запись добавляется в созданный список. Для каждой созданной записи поле **Имя** возвращает имя поля записи контейнера, на которую ест ссылка, для которого была создана текущая запись.

Если аргумент `path` относится к источнику данных одного из типов *Перечисление*, для каждого значения перечисления, для которого есть ссылка , новая запись добавляется в созданный список. Для каждой созданной записи поле **Имя** возвращает значение перечисления, на которое есть ссылка, для которого была создана текущая запись, поле **Описание** возвращает описание этого перечисления, а поле **Метка** возвращает метку этого перечисления.

Во время выполнения, когда используется синтаксис 1, поля **Метка** и **Описание** должны возвращать значения, основанные на настройках языка формата электронной отчетности (ER), который используется:

- Если доступны метки и описания для запрашиваемого языка, поля **Метка** и **Описание** возвращают значения, основанные на этом языке, и поле **IsTranslated** возвращает **True**.
- Если метки и описания для запрашиваемого языка недоступны, поля **Метка** и **Описание** возвращают значения, основанные на языке по умолчанию **EN-US**, и поле **IsTranslated** возвращает **False**.

Во время выполнения, когда используется синтаксис 2, поля **Метка** и **Описание** должны возвращать значения, основанные на языке, который задан как второй аргумент вызываемой функции:

- Если доступны метки и описания для запрашиваемого языка, поля **Метка** и **Описание** возвращают значения, основанные на этом языке, и поле **IsTranslated** возвращает **True**.
- Если метки и описания для запрашиваемого языка недоступны, поля **Метка** и **Описание** возвращают значения, основанные на языке **EN-US**, и поле **IsTranslated** возвращает **False**.

## <a name="example-1"></a>Пример 1

На следующем рисунке показано перечисление, введенное в модели данных ER.

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

Следующая иллюстрация показывает эти детали:

- Перечисление модели, вставленное в отчет в качестве источника данных.
- Выражение ER использует перечисление модели как параметр функции `LISTOFFIELDS`.
- Источник данных типа *Список записей* вставляется в отчет с помощью созданного выражения ER.

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

В следующем примере показано элементы формата электронной отчетности, которые привязаны к источнику данных типа *Список записей*, который был создан с помощью функции `LISTOFFIELDS`.

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

На следующем рисунке показан результат выполнения созданного формата.

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> На основе параметров языка родительских элементов формата **FILE** и **FOLDER** переведенный текст для меток и описаний вводится в выходные данные формата электронной отчетности.

## <a name="example-2"></a>Пример 2

Можно использовать тип источника данных *Вычисляемое поле* для настройки источников данных **enumType\_de** и **enumType\_deCH** для перечисления модели данных **enumType**.

- **enumType\_de** = `LISTOFFIELDS (enumType, "de")`
- **enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`

В этом случае можно использовать следующее выражение для получения метки значения перечисления на немецком языке (Швейцария), если этот перевод доступен. Если перевод со швейцарского на немецкий не поддерживается, подпись появляется на немецком языке.

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции для работы со списками](er-functions-category-list.md)
