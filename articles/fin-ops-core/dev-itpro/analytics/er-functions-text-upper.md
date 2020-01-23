---
title: Функция ER UPPER
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности UPPER.
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
ms.openlocfilehash: ed862ab823cfc3539c420d3066c9397e1e6d870e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916691"
---
# <span data-ttu-id="a3823-103"><a name="UPPER">Функция ER UPPER</a></span><span class="sxs-lookup"><span data-stu-id="a3823-103"><a name="UPPER">UPPER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3823-104">Функция `UPPER` возвращает указанную строку текста в качестве *строкового* значения после того, как она была преобразована в буквы верхнего регистра.</span><span class="sxs-lookup"><span data-stu-id="a3823-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3823-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3823-105">Syntax</span></span>

```
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="a3823-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="a3823-106">Arguments</span></span>

<span data-ttu-id="a3823-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="a3823-107">`text`: *String*</span></span>

<span data-ttu-id="a3823-108">Действительный путь источника данных типа *Строка*.</span><span class="sxs-lookup"><span data-stu-id="a3823-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="a3823-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="a3823-109">Return values</span></span>

<span data-ttu-id="a3823-110">*Строка*</span><span class="sxs-lookup"><span data-stu-id="a3823-110">*String*</span></span>

<span data-ttu-id="a3823-111">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="a3823-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="a3823-112">Пример</span><span class="sxs-lookup"><span data-stu-id="a3823-112">Example</span></span>

<span data-ttu-id="a3823-113">`UPPER ("Sample")` возвращает **"SAMPLE"**.</span><span class="sxs-lookup"><span data-stu-id="a3823-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a3823-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a3823-114">Additional resources</span></span>

[<span data-ttu-id="a3823-115">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="a3823-115">Text functions</span></span>](er-functions-category-text.md)
