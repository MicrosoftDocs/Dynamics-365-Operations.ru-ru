---
title: Список функций электронной отчетности в категории-контейнере
description: В этой теме содержится информация о контейнерных функциях, которые поддерживаются в электронной отчетности (ER).
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
ms.openlocfilehash: 46d1af85773f6c3d07865658c554dee74fae625f
ms.sourcegitcommit: e8a46e127d70986539c138b27a641bff6f6874d0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/15/2020
ms.locfileid: "4739106"
---
# <a name="list-of-er-functions-in-the-container-category"></a><span data-ttu-id="d9c9d-103">Список функций электронной отчетности в категории-контейнере</span><span class="sxs-lookup"><span data-stu-id="d9c9d-103">List of ER functions in the container category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9c9d-104">[Функции](er-formula-language.md#functions) контейнера [электронной отчетности (ER)](general-electronic-reporting.md) могут использоваться для выполнения операций, связанных с источниками данных с типом данных *Контейнер*.</span><span class="sxs-lookup"><span data-stu-id="d9c9d-104">[Electronic reporting (ER)](general-electronic-reporting.md) container [functions](er-formula-language.md#functions) can be used to perform operations that involve data sources of the *Container* data type.</span></span> <span data-ttu-id="d9c9d-105">Эти операции выполняются, когда обрабатываемые данные представляют собой коллекцию двоичных данных в формате больших двоичных объектов (BLOB).</span><span class="sxs-lookup"><span data-stu-id="d9c9d-105">These operations occur when the processing data represents a collection of binary data in binary large object (BLOB) format.</span></span> <span data-ttu-id="d9c9d-106">В этой теме приводится краткое изложение этих функций.</span><span class="sxs-lookup"><span data-stu-id="d9c9d-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="d9c9d-107">Список поддерживаемых функций</span><span class="sxs-lookup"><span data-stu-id="d9c9d-107">List of supported functions</span></span>

| <span data-ttu-id="d9c9d-108">Функция</span><span class="sxs-lookup"><span data-stu-id="d9c9d-108">Function</span></span> | <span data-ttu-id="d9c9d-109">описание</span><span class="sxs-lookup"><span data-stu-id="d9c9d-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="d9c9d-110">Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="d9c9d-110">Base64StringToContainer</span></span>](er-functions-container-base64stringtocontainer.md) | <span data-ttu-id="d9c9d-111">Эта функция возвращает значение *Контейнер*, состоящее из двоичного содержимого, которое декодировано из заданной ASCII-строки, представляющей собой группу Base64 из схем кодирования двоичных значений в текст.</span><span class="sxs-lookup"><span data-stu-id="d9c9d-111">This function returns a *Container* value that consists of binary content that is decoded from the specified ASCII string that represents a Base64 group of binary-to-text encoding schemes.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="d9c9d-112">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d9c9d-112">Additional resources</span></span>

[<span data-ttu-id="d9c9d-113">Обзор электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="d9c9d-113">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="d9c9d-114">Конструктор формул в электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="d9c9d-114">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="d9c9d-115">Язык формул электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="d9c9d-115">Electronic reporting formula language</span></span>](er-formula-language.md)
