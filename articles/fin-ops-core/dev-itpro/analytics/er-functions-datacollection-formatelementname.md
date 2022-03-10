---
title: Функция ER FORMATELEMENTNAME
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности FORMATELEMENTNAME.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 72977edfbe06e0d68d9226c9c25fa0633e7951d22438e053ae2a7cf4ef9a5848
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764497"
---
# <a name="formatelementname-er-function"></a>Функция ER FORMATELEMENTNAME

[!include [banner](../includes/banner.md)]

Функция `FORMATELEMENTNAME` возвращает значение *строка*, представляющее имя элемента текущего формата электронной отчетности (ER).

## <a name="syntax"></a>Синтаксис

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a>Возвращаемые значения

*Строка*

Результирующее текстовое значение.

## <a name="usage-notes"></a>Примечания по использованию

Эта функция может вызываться в выражениях ER, настроенных для свойств **Имя ключа собранных данных** и **Значение ключа собранных данных** компонента формата УК из группы **Текст** в компоненте **Common\\File**, где включен параметр **Сбор сведений о результате**.

## <a name="example"></a>Пример

Для получения дополнительных сведений об использовании этой функции см. проводник по задаче [ER Использование выходных данных формата для инвентаризации и агрегирования](tasks/er-format-counting-summing-1.md), который является частью бизнес-процесса **Приобретение/разработка компонентов ИТ-услуг и решений**.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Функции сбора данных](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]