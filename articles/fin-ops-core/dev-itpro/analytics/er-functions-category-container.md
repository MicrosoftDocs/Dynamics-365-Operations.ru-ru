---
title: Список функций электронной отчетности в категории-контейнере
description: В этой статье содержится информация о функциях контейнера, которые поддерживаются в электронной отчетности (ER).
author: kfend
ms.date: 12/14/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: f07c3645f824fc2fe8ca156c8cf06840e993a9a5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282662"
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
