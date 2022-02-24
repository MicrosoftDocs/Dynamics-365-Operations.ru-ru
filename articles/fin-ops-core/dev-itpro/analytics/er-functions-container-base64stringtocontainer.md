---
title: Функция электронной отчетности Base64StringToContainer
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности Base64StringToContainer.
author: NickSelin
manager: kfend
ms.date: 12/14/2020
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
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 0e92ae41a3e0f03cb14d4791ab768f096f2a0523
ms.sourcegitcommit: e8a46e127d70986539c138b27a641bff6f6874d0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/15/2020
ms.locfileid: "4739107"
---
# <a name="base64stringtocontainer-er-function"></a>Функция электронной отчетности Base64StringToContainer

[!include [banner](../includes/banner.md)]

[Функция](er-formula-language.md#functions) `BASE64STRINGTOCONTAINER` преобразует заданный ввод типа *Строка* в элемент данных типа *[Контейнер](er-functions-category-container.md)*.

## <a name="syntax"></a>Синтаксис

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a>Аргументы

`input`: *Строка*

Действительный путь источника данных типа *Строка*.

## <a name="return-values"></a>Возвращаемые значения

*Тара*

Результирующее двоичное значение в формате больших двоичных объектов (BLOB).

## <a name="usage-notes"></a>Примечания по использованию

Исключение "Недопустимый параметр" генерируется, если входная строка не предоставляет правильную группу Base64 для схем кодирования двоичного кода в текст.

## <a name="example"></a>Пример

Определите следующие источники данных в соответствии вашей модели:

- Корневой источник данных **DocuTypeGroupEnum** типа *Dynamics 365 for Operations/перечисление*, относящийся к перечислению приложения **DocuTypeGroup**.
- Корневой источник данных **Customer** типа *Dynamics 365 for Operations / Записи таблицы*, который ссылается на таблицу приложения **CustTable**.
- Источник данных **\#Media** типа *Вычисляемое поле*, сконфигурированного следующим образом:

    - Он добавляется как дочерний источник данных для источника данных **Customer**.
    - Он содержит выражение `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.

- Источник данных **\#MediaAsBase64String** типа *Вычисляемое поле*, сконфигурированного следующим образом:

    - Он добавляется как дочерний источник данных для источника данных **Customer.'\#Media'**.
    - Он содержит выражение `Customer.'#Media'.'getFileContentAsBase64String()'`.

- Источник данных **\#BlobFomBase64** типа *Вычисляемое поле*, сконфигурированного следующим образом:

    - Он добавляется как дочерний источник данных для источника данных **Customer.'\#Media'**.
    - Он содержит выражение `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.

В этом примере источник данных **\#MediaAsBase64String** кодирует двоичное содержимое текущего вложения мультимедиа в виде текста, представляющего группу Base64 схем кодирования двоичных значений в текст. Источник данных **\#BlobFomBase64** декодирует строку Base64 и возвращает двоичное значение в формате BLOB.

![Пример источников данных на странице конструктора сопоставления модели электронной отчетности](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a>Дополнительные ресурсы

[Контейнерные функции](er-functions-category-container.md)
