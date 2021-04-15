---
title: Список функций электронной отчетности в категории-контейнере
description: В этой теме содержится информация о контейнерных функциях, которые поддерживаются в электронной отчетности (ER).
author: NickSelin
ms.date: 12/14/2020
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
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 95f207538ea4f0f7df775bf28d0dcf6529d1a91c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753248"
---
# <a name="list-of-er-functions-in-the-container-category"></a>Список функций электронной отчетности в категории-контейнере

[!include [banner](../includes/banner.md)]

[Функции](er-formula-language.md#functions) контейнера [электронной отчетности (ER)](general-electronic-reporting.md) могут использоваться для выполнения операций, связанных с источниками данных с типом данных *Контейнер*. Эти операции выполняются, когда обрабатываемые данные представляют собой коллекцию двоичных данных в формате больших двоичных объектов (BLOB). В этой теме приводится краткое изложение этих функций.

## <a name="list-of-supported-functions"></a>Список поддерживаемых функций

| Функция | описание |
|----------|-------------|
| [Base64StringToContainer](er-functions-container-base64stringtocontainer.md) | Эта функция возвращает значение *Контейнер*, состоящее из двоичного содержимого, которое декодировано из заданной ASCII-строки, представляющей собой группу Base64 из схем кодирования двоичных значений в текст. |

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор электронной отчетности](general-electronic-reporting.md)

[Конструктор формул в электронной отчетности](general-electronic-reporting-formula-designer.md)

[Язык формул электронной отчетности](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]