---
title: Функция ER NUMBERFORMAT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности NUMBERFORMAT.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 8de57d8b0a45b8b58849a24f2d8f0cde41e0ea3a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746226"
---
# <a name="numberformat-er-function"></a><span data-ttu-id="cdbac-103">Функция ER NUMBERFORMAT</span><span class="sxs-lookup"><span data-stu-id="cdbac-103">NUMBERFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cdbac-104">Функция `NUMBERFORMAT` возвращает значение *строки*, которое представляет заданное число в указанном формате и в дополнительно указанной [культуре](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="cdbac-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="cdbac-105">Сведения о поддерживаемых форматах см. в разделах [стандартный](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) и [настраиваемый](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="cdbac-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="cdbac-106">Синтаксис 1</span><span class="sxs-lookup"><span data-stu-id="cdbac-106">Syntax 1</span></span>

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="cdbac-107">Синтаксис 2</span><span class="sxs-lookup"><span data-stu-id="cdbac-107">Syntax 2</span></span>

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="cdbac-108">Аргументы</span><span class="sxs-lookup"><span data-stu-id="cdbac-108">Arguments</span></span>

<span data-ttu-id="cdbac-109">`number`: *Целочисленный* или *Вещественный*</span><span class="sxs-lookup"><span data-stu-id="cdbac-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="cdbac-110">Числовое значение, которое определяет число, которое должно быть отформатировано.</span><span class="sxs-lookup"><span data-stu-id="cdbac-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="cdbac-111">`format`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="cdbac-111">`format` : *String*</span></span>

<span data-ttu-id="cdbac-112">*Строковое* значение, представляющее формат.</span><span class="sxs-lookup"><span data-stu-id="cdbac-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="cdbac-113">`culture`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="cdbac-113">`culture`: *String*</span></span>

<span data-ttu-id="cdbac-114">*Строковое* значение строки, которое представляет культуру для форматирования.</span><span class="sxs-lookup"><span data-stu-id="cdbac-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="cdbac-115">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="cdbac-115">Return values</span></span>

<span data-ttu-id="cdbac-116">*Строка*</span><span class="sxs-lookup"><span data-stu-id="cdbac-116">*String*</span></span>

<span data-ttu-id="cdbac-117">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="cdbac-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="cdbac-118">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="cdbac-118">Usage notes</span></span>

<span data-ttu-id="cdbac-119">Если культура не определена как аргумент вызываемо функции, контекст, в который работает эта функция, определяет культуру, используемую для форматирования чисел.</span><span class="sxs-lookup"><span data-stu-id="cdbac-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="cdbac-120">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cdbac-120">Example 1</span></span>

<span data-ttu-id="cdbac-121">Для культуры **EN-US**, `NUMBERFORMAT (0.45, "p")` возвращает **"45.00 %"**, а `NUMBERFORMAT (10.45, "#")`возвращает **"10"**.</span><span class="sxs-lookup"><span data-stu-id="cdbac-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="cdbac-122">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cdbac-122">Example 2</span></span>

<span data-ttu-id="cdbac-123">`NUMBERFORMAT (10/3, "F2", "de")` возвращает **3,33**, в то время как `NUMBERFORMAT (10/3, "F2", "en-us")` возвращает **3,33**.</span><span class="sxs-lookup"><span data-stu-id="cdbac-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cdbac-124">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cdbac-124">Additional resources</span></span>

[<span data-ttu-id="cdbac-125">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="cdbac-125">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]