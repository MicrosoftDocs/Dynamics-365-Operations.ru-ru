---
title: Функция ER FORMATELEMENTNAME
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности FORMATELEMENTNAME.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 5f299a4bb697afce152a61ec35fcefab7157f356
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042535"
---
# <a name="FORMATELEMENTNAME">Функция ER FORMATELEMENTNAME</a>

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