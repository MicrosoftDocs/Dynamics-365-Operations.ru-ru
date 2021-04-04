---
title: Функция ER JSONVALUE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности JSONVALUE.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 203fe1b1616f724ddf3015258306e0d9e8d4f599
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570024"
---
# <a name="jsonvalue-er-function"></a><span data-ttu-id="14485-103">Функция ER JSONVALUE</span><span class="sxs-lookup"><span data-stu-id="14485-103">JSONVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14485-104">Функция `JSONVALUE` анализирует данные в формате JavaScript Object Notation (JSON), к которому осуществляется доступ по специальному пути и извлекает скалярное значение с указанным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="14485-104">The `JSONVALUE` function parses data in JavaScript Object Notation (JSON) format that is accessed at the specified path, and it extracts a scalar value that has the specified ID.</span></span> <span data-ttu-id="14485-105">Затем она возвращает извлеченное скалярное значение как *строковое* значение.</span><span class="sxs-lookup"><span data-stu-id="14485-105">It then returns the extracted scalar value as a *String* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="14485-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14485-106">Syntax</span></span>

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a><span data-ttu-id="14485-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="14485-107">Arguments</span></span>

<span data-ttu-id="14485-108">`input`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="14485-108">`input`: *String*</span></span>

<span data-ttu-id="14485-109">Действительный путь источника данных типа *Строка*, содержащего данные JSON.</span><span class="sxs-lookup"><span data-stu-id="14485-109">The valid path of a data source of the *String* type that contains JSON data.</span></span>

<span data-ttu-id="14485-110">`path`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="14485-110">`path`: *String*</span></span>

<span data-ttu-id="14485-111">Код скалярного значения данных JSON.</span><span class="sxs-lookup"><span data-stu-id="14485-111">The identifier of a scalar value of JSON data.</span></span>

## <a name="return-values"></a><span data-ttu-id="14485-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="14485-112">Return values</span></span>

<span data-ttu-id="14485-113">*Строка*</span><span class="sxs-lookup"><span data-stu-id="14485-113">*String*</span></span>

<span data-ttu-id="14485-114">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="14485-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="14485-115">Пример</span><span class="sxs-lookup"><span data-stu-id="14485-115">Example</span></span>

<span data-ttu-id="14485-116">Источник данных **JsonField** содержит следующие данные в формате JSON: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span><span class="sxs-lookup"><span data-stu-id="14485-116">The **JsonField** data source contains the following data in JSON format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span></span> <span data-ttu-id="14485-117">В этом случае выражение `JSONVALUE (JsonField, "BuildNumber")` возвращает следующее значение типа данных *Строка*: **"7.3.1234.1"**.</span><span class="sxs-lookup"><span data-stu-id="14485-117">In this case, the expression `JSONVALUE (JsonField, "BuildNumber")` returns the following value of the *String* data type: **"7.3.1234.1"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="14485-118">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="14485-118">Additional resources</span></span>

[<span data-ttu-id="14485-119">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="14485-119">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]