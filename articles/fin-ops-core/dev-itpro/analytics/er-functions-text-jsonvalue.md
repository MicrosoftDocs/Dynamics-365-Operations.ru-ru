---
title: Функция ER JSONVALUE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности JSONVALUE.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 11f9ac680ea00622367ea56106fd22508628d85d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685915"
---
# <a name="jsonvalue-er-function"></a><span data-ttu-id="df76d-103">Функция ER JSONVALUE</span><span class="sxs-lookup"><span data-stu-id="df76d-103">JSONVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df76d-104">Функция `JSONVALUE` анализирует данные в формате JavaScript Object Notation (JSON), к которому осуществляется доступ по специальному пути и извлекает скалярное значение с указанным идентификатором.</span><span class="sxs-lookup"><span data-stu-id="df76d-104">The `JSONVALUE` function parses data in JavaScript Object Notation (JSON) format that is accessed at the specified path, and it extracts a scalar value that has the specified ID.</span></span> <span data-ttu-id="df76d-105">Затем она возвращает извлеченное скалярное значение как *строковое* значение.</span><span class="sxs-lookup"><span data-stu-id="df76d-105">It then returns the extracted scalar value as a *String* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="df76d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df76d-106">Syntax</span></span>

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a><span data-ttu-id="df76d-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="df76d-107">Arguments</span></span>

<span data-ttu-id="df76d-108">`input`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="df76d-108">`input`: *String*</span></span>

<span data-ttu-id="df76d-109">Действительный путь источника данных типа *Строка*, содержащего данные JSON.</span><span class="sxs-lookup"><span data-stu-id="df76d-109">The valid path of a data source of the *String* type that contains JSON data.</span></span>

<span data-ttu-id="df76d-110">`path`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="df76d-110">`path`: *String*</span></span>

<span data-ttu-id="df76d-111">Код скалярного значения данных JSON.</span><span class="sxs-lookup"><span data-stu-id="df76d-111">The identifier of a scalar value of JSON data.</span></span>

## <a name="return-values"></a><span data-ttu-id="df76d-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="df76d-112">Return values</span></span>

<span data-ttu-id="df76d-113">*Строка*</span><span class="sxs-lookup"><span data-stu-id="df76d-113">*String*</span></span>

<span data-ttu-id="df76d-114">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="df76d-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="df76d-115">Пример</span><span class="sxs-lookup"><span data-stu-id="df76d-115">Example</span></span>

<span data-ttu-id="df76d-116">Источник данных **JsonField** содержит следующие данные в формате JSON: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span><span class="sxs-lookup"><span data-stu-id="df76d-116">The **JsonField** data source contains the following data in JSON format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span></span> <span data-ttu-id="df76d-117">В этом случае выражение `JSONVALUE (JsonField, "BuildNumber")` возвращает следующее значение типа данных *Строка*: **"7.3.1234.1"**.</span><span class="sxs-lookup"><span data-stu-id="df76d-117">In this case, the expression `JSONVALUE (JsonField, "BuildNumber")` returns the following value of the *String* data type: **"7.3.1234.1"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="df76d-118">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="df76d-118">Additional resources</span></span>

[<span data-ttu-id="df76d-119">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="df76d-119">Text functions</span></span>](er-functions-category-text.md)
