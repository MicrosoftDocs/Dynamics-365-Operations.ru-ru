---
title: Функция ER JSONVALUE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности JSONVALUE.
author: NickSelin
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
ms.openlocfilehash: e8336e43a236e3f3b875fb3cb81bc139507673c2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746371"
---
# <a name="jsonvalue-er-function"></a><span data-ttu-id="c69e1-103">Функция ER JSONVALUE</span><span class="sxs-lookup"><span data-stu-id="c69e1-103">JSONVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c69e1-104">Функция `JSONVALUE` анализирует данные в формате JavaScript Object Notation (JSON), к которому осуществляется доступ по специальному пути и извлекает скалярное значение с указанным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="c69e1-104">The `JSONVALUE` function parses data in JavaScript Object Notation (JSON) format that is accessed at the specified path, and it extracts a scalar value that has the specified ID.</span></span> <span data-ttu-id="c69e1-105">Затем она возвращает извлеченное скалярное значение как *строковое* значение.</span><span class="sxs-lookup"><span data-stu-id="c69e1-105">It then returns the extracted scalar value as a *String* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c69e1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c69e1-106">Syntax</span></span>

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a><span data-ttu-id="c69e1-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="c69e1-107">Arguments</span></span>

<span data-ttu-id="c69e1-108">`input`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="c69e1-108">`input`: *String*</span></span>

<span data-ttu-id="c69e1-109">Действительный путь источника данных типа *Строка*, содержащего данные JSON.</span><span class="sxs-lookup"><span data-stu-id="c69e1-109">The valid path of a data source of the *String* type that contains JSON data.</span></span>

<span data-ttu-id="c69e1-110">`path`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="c69e1-110">`path`: *String*</span></span>

<span data-ttu-id="c69e1-111">Код скалярного значения данных JSON.</span><span class="sxs-lookup"><span data-stu-id="c69e1-111">The identifier of a scalar value of JSON data.</span></span>

## <a name="return-values"></a><span data-ttu-id="c69e1-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="c69e1-112">Return values</span></span>

<span data-ttu-id="c69e1-113">*Строка*</span><span class="sxs-lookup"><span data-stu-id="c69e1-113">*String*</span></span>

<span data-ttu-id="c69e1-114">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="c69e1-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="c69e1-115">Пример</span><span class="sxs-lookup"><span data-stu-id="c69e1-115">Example</span></span>

<span data-ttu-id="c69e1-116">Источник данных **JsonField** содержит следующие данные в формате JSON: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span><span class="sxs-lookup"><span data-stu-id="c69e1-116">The **JsonField** data source contains the following data in JSON format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span></span> <span data-ttu-id="c69e1-117">В этом случае выражение `JSONVALUE (JsonField, "BuildNumber")` возвращает следующее значение типа данных *Строка*: **"7.3.1234.1"**.</span><span class="sxs-lookup"><span data-stu-id="c69e1-117">In this case, the expression `JSONVALUE (JsonField, "BuildNumber")` returns the following value of the *String* data type: **"7.3.1234.1"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c69e1-118">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c69e1-118">Additional resources</span></span>

[<span data-ttu-id="c69e1-119">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="c69e1-119">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]