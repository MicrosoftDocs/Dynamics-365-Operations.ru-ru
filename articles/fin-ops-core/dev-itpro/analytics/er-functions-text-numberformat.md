---
title: Функция ER NUMBERFORMAT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности NUMBERFORMAT.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 41f48fb49b2d28acf69fe05fe87644a4c43e81fe
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070560"
---
# <span data-ttu-id="b9b78-103"><a name="NUMBERFORMAT">Функция ER NUMBERFORMAT</a></span><span class="sxs-lookup"><span data-stu-id="b9b78-103"><a name="NUMBERFORMAT">NUMBERFORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9b78-104">Функция `NUMBERFORMAT` возвращает значение *строки*, которое представляет заданное число в указанном формате и в дополнительно указанной [культуре](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="b9b78-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="b9b78-105">Сведения о поддерживаемых форматах см. в разделах [стандартный](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) и [настраиваемый](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="b9b78-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="b9b78-106">Синтаксис 1</span><span class="sxs-lookup"><span data-stu-id="b9b78-106">Syntax 1</span></span>

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="b9b78-107">Синтаксис 2</span><span class="sxs-lookup"><span data-stu-id="b9b78-107">Syntax 2</span></span>

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="b9b78-108">Аргументы</span><span class="sxs-lookup"><span data-stu-id="b9b78-108">Arguments</span></span>

<span data-ttu-id="b9b78-109">`number`: *Целочисленный* или *Вещественный*</span><span class="sxs-lookup"><span data-stu-id="b9b78-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="b9b78-110">Числовое значение, которое определяет число, которое должно быть отформатировано.</span><span class="sxs-lookup"><span data-stu-id="b9b78-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="b9b78-111">`format`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="b9b78-111">`format` : *String*</span></span>

<span data-ttu-id="b9b78-112">*Строковое* значение, представляющее формат.</span><span class="sxs-lookup"><span data-stu-id="b9b78-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="b9b78-113">`culture`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="b9b78-113">`culture`: *String*</span></span>

<span data-ttu-id="b9b78-114">*Строковое* значение строки, которое представляет культуру для форматирования.</span><span class="sxs-lookup"><span data-stu-id="b9b78-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="b9b78-115">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="b9b78-115">Return values</span></span>

<span data-ttu-id="b9b78-116">*Строка*</span><span class="sxs-lookup"><span data-stu-id="b9b78-116">*String*</span></span>

<span data-ttu-id="b9b78-117">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="b9b78-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b9b78-118">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="b9b78-118">Usage notes</span></span>

<span data-ttu-id="b9b78-119">Если культура не определена как аргумент вызываемо функции, контекст, в который работает эта функция, определяет культуру, используемую для форматирования чисел.</span><span class="sxs-lookup"><span data-stu-id="b9b78-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="b9b78-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b9b78-120">Example 1</span></span>

<span data-ttu-id="b9b78-121">Для культуры **EN-US**, `NUMBERFORMAT (0.45, "p")` возвращает **"45.00 %"**, а `NUMBERFORMAT (10.45, "#")`возвращает **"10"**.</span><span class="sxs-lookup"><span data-stu-id="b9b78-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="b9b78-122">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b9b78-122">Example 2</span></span>

<span data-ttu-id="b9b78-123">`NUMBERFORMAT (10/3, "F2", "de")` возвращает **3,33**, в то время как `NUMBERFORMAT (10/3, "F2", "en-us")` возвращает **3,33**.</span><span class="sxs-lookup"><span data-stu-id="b9b78-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b9b78-124">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b9b78-124">Additional resources</span></span>

[<span data-ttu-id="b9b78-125">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="b9b78-125">Text functions</span></span>](er-functions-category-text.md)
