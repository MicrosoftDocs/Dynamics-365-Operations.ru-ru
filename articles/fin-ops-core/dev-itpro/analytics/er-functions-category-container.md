---
title: Список функций электронной отчетности в категории-контейнере
description: В этой статье содержится информация о функциях контейнера, которые поддерживаются в электронной отчетности (ER).
author: NickSelin
ms.date: 12/14/2020
ms.prod: ''
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
ms.openlocfilehash: 5c86b0ae6cbf4ac6515491b55390d42c371eae4b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883827"
---
# <a name="list-of-er-functions-in-the-container-category"></a>Список функций электронной отчетности в категории-контейнере

[!include [banner](../includes/banner.md)]

[Функции](er-formula-language.md#Functions) контейнера [электронной отчетности (ER)](general-electronic-reporting.md) могут использоваться для выполнения операций, связанных с источниками данных с типом данных *Контейнер*. Эти операции выполняются, когда обрабатываемые данные представляют собой коллекцию двоичных данных в формате больших двоичных объектов (BLOB). В данной статье приводится краткое описание этих функций.

## <a name="list-of-supported-functions"></a>Список поддерживаемых функций

| Функция | описание |
|----------|-------------|
| [Base64StringToContainer](er-functions-container-base64stringtocontainer.md) | Эта функция возвращает значение *Контейнер*, состоящее из двоичного содержимого, которое декодировано из заданной ASCII-строки, представляющей собой группу Base64 из схем кодирования двоичных значений в текст. |

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор электронной отчетности](general-electronic-reporting.md)

[Конструктор формул в электронной отчетности](general-electronic-reporting-formula-designer.md)

[Язык формул электронной отчетности](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
