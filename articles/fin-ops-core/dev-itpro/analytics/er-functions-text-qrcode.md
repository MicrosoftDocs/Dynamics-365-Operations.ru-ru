---
title: Функция ER QRCODE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности QRCODE.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 92665936decc87b29f2fabb346f4d16745d0a30b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562669"
---
# <a name="qrcode-er-function"></a>Функция ER QRCODE

[!include [banner](../includes/banner.md)]

Функция `QRCODE` возвращает значение *Контейнер*, которое представляет изображение Quick Response (QR) для указанной строки в двоичном формате.

## <a name="syntax"></a>Синтаксис

```vb
QRCODE (text)
```

## <a name="arguments"></a>Аргументы

`text`: *Строка*

*Строковое* значение, представляющее исходный текст.

## <a name="return-values"></a>Возвращаемые значения

*Тара*

Полученный двоичный поток.

## <a name="example"></a>Пример

Вы можете настроить формат электронной отчетности (ER) для создания исходящего документа в формате Microsoft Office (рабочие книги Excel или документы Word) с помощью предварительно заданного шаблона. Этот шаблон может содержать объект **Изображение** (книга Excel) или **Элемент управления изображения** (документ Word) в качестве заполнителя для изображения кода QR. Необходимо добавить в настроенный формат ER элемент **Ячейка**, который будет использоваться для заполнения этого заполнителя. Чтобы указать, какая информация будет храниться в коде QR, необходимо определить привязку для этого элемента **Ячейка**. Например, можно настроить такую привязку как содержащую следующие выражения:

```vb
QRCODE (model.ListOfShelfLabels.LabelText)`
```

При запуске настроенного формата ER текстовое значение поля **LabelText** источника данных **model.ListOfShelfLabels** будет использовано для создания изображения кода QR. Это изображение заменит заполнитель изображения кода QR в шаблоне документа, используемого для создания исходящего документа. Когда это изображение созданного документа сканируется, оно возвращает текст, взятый из поля **LabelText** источника данных **model.ListOfShelfLabels**. Дополнительные сведения см. в разделе [Внедрение изображений и фигур в документы, создаваемые с помощью электронной отчетности](electronic-reporting-embed-images-shapes.md).

## <a name="additional-resources"></a>Дополнительные ресурсы

[Текстовые функции](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]