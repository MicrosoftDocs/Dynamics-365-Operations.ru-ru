---
title: Список функций ER в логической категории
description: В этой теме содержится информация о логических функциях, которые поддерживаются в электронной отчетности (ER).
author: NickSelin
manager: kfend
ms.date: 08/19/2020
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
ms.openlocfilehash: e622778c60646e5cc84cd6e23a5d4954a0fe0bb3
ms.sourcegitcommit: 38ad6f791c3d5688a5dc201a234ba89f155f7f03
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "3705103"
---
# <a name="list-of-er-functions-in-the-logical-category"></a><span data-ttu-id="e22ff-103">Список функций ER в логической категории</span><span class="sxs-lookup"><span data-stu-id="e22ff-103">List of ER functions in the logical category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e22ff-104">Логические функции электронной отчетности (ER) могут использоваться для работы с логическими значениями для выполнения более одного сравнения в одном выражении или для тестирования нескольких условий.</span><span class="sxs-lookup"><span data-stu-id="e22ff-104">Electronic reporting (ER) logical functions can be used to work with logical values to perform more than one comparison in a single expression or test multiple conditions.</span></span> <span data-ttu-id="e22ff-105">В этой теме приводится краткое изложение этих функций.</span><span class="sxs-lookup"><span data-stu-id="e22ff-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="e22ff-106">Список поддерживаемых функций</span><span class="sxs-lookup"><span data-stu-id="e22ff-106">List of supported functions</span></span>

| <span data-ttu-id="e22ff-107">Функция</span><span class="sxs-lookup"><span data-stu-id="e22ff-107">Function</span></span> | <span data-ttu-id="e22ff-108">Описание</span><span class="sxs-lookup"><span data-stu-id="e22ff-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="e22ff-109">И</span><span class="sxs-lookup"><span data-stu-id="e22ff-109">And</span></span>](er-functions-logical-and.md)                       | <span data-ttu-id="e22ff-110">Эта функция возвращает *логическое* значение **TRUE**, если все указанные условия — true.</span><span class="sxs-lookup"><span data-stu-id="e22ff-110">This function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="e22ff-111">В противном случае возвращает *логическое* значение **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="e22ff-111">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="e22ff-112">Обращение</span><span class="sxs-lookup"><span data-stu-id="e22ff-112">Case</span></span>](er-functions-logical-case.md)                     | <span data-ttu-id="e22ff-113">Эта функция оценивает значение указанного выражения по сравнению с указанными альтернативными вариантами и возвращает результат первого варианта, равного значению указанного выражения.</span><span class="sxs-lookup"><span data-stu-id="e22ff-113">This function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="e22ff-114">В противном случае возвращает дополнительный результат по умолчанию, если результат по умолчанию указан в качестве последнего аргумента вызванной функции, которой не предшествует вариант.</span><span class="sxs-lookup"><span data-stu-id="e22ff-114">Otherwise, it returns an optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="e22ff-115">Возвращаемое значение может быть значением любого из поддерживаемых типов данных.</span><span class="sxs-lookup"><span data-stu-id="e22ff-115">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="e22ff-116">Если</span><span class="sxs-lookup"><span data-stu-id="e22ff-116">If</span></span>](er-functions-logical-if.md)                         | <span data-ttu-id="e22ff-117">Эта функция возвращает первое указанное значение, если выполняется указанное условие.</span><span class="sxs-lookup"><span data-stu-id="e22ff-117">This function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="e22ff-118">В противном случае возвращает второе указанное значение.</span><span class="sxs-lookup"><span data-stu-id="e22ff-118">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="e22ff-119">Возвращаемое значение может быть значением любого из поддерживаемых типов данных.</span><span class="sxs-lookup"><span data-stu-id="e22ff-119">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="e22ff-120">Не</span><span class="sxs-lookup"><span data-stu-id="e22ff-120">Not</span></span>](er-functions-logical-not.md)                       | <span data-ttu-id="e22ff-121">Эта функция возвращает обратное логическое значение указанного условия в качестве *логического* значения.</span><span class="sxs-lookup"><span data-stu-id="e22ff-121">This function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span> |
| [<span data-ttu-id="e22ff-122">Или</span><span class="sxs-lookup"><span data-stu-id="e22ff-122">Or</span></span>](er-functions-logical-or.md)                         | <span data-ttu-id="e22ff-123">Эта функция возвращает *логическое* значение **FALSE**, если все указанные условия — false.</span><span class="sxs-lookup"><span data-stu-id="e22ff-123">This function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="e22ff-124">Если какое-либо указанное условие — true, эта функция возвращает *логическое* значение **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="e22ff-124">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span> |
| [<span data-ttu-id="e22ff-125">ValueIn</span><span class="sxs-lookup"><span data-stu-id="e22ff-125">ValueIn</span></span>](er-functions-logical-valuein.md)               | <span data-ttu-id="e22ff-126">Эта функция определяет, соответствует ли заданный ввод какому-либо значению указанного элемента в указанном списке.</span><span class="sxs-lookup"><span data-stu-id="e22ff-126">This function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="e22ff-127">Она возвращает *логическое* значение **TRUE**, если указанный ввод совпадает с результатом выполнения указанного выражения по крайней мере для одной записи указанного списка.</span><span class="sxs-lookup"><span data-stu-id="e22ff-127">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="e22ff-128">В противном случае возвращает *логическое* значение **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="e22ff-128">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="e22ff-129">ValueInLarge</span><span class="sxs-lookup"><span data-stu-id="e22ff-129">ValueInLarge</span></span>](er-functions-logical-valueinlarge.md)     | <span data-ttu-id="e22ff-130">Эта функция определяет, соответствует ли заданный ввод типа *Int64* или *Integer* какому-либо значению указанного элемента в указанном списке.</span><span class="sxs-lookup"><span data-stu-id="e22ff-130">This function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="e22ff-131">Она возвращает *логическое* значение **TRUE**, если указанный ввод совпадает с результатом выполнения указанного выражения по крайней мере для одной записи указанного списка.</span><span class="sxs-lookup"><span data-stu-id="e22ff-131">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="e22ff-132">В противном случае возвращает *логическое* значение **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="e22ff-132">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |


## <a name="additional-resources"></a><span data-ttu-id="e22ff-133">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e22ff-133">Additional resources</span></span>

[<span data-ttu-id="e22ff-134">Обзор электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="e22ff-134">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="e22ff-135">Конструктор формул в электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="e22ff-135">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="e22ff-136">Язык формул электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="e22ff-136">Electronic reporting formula language</span></span>](er-formula-language.md)
