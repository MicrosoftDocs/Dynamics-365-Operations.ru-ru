---
title: Список функций ER в категории сбора данных
description: В этой теме содержится информация о функциях сбора данных, которые поддерживаются в электронной отчетности (ER).
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: b318945c9cd10b237843d26cfdc46fc08e84e268
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917818"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a><span data-ttu-id="7540f-103">Список функций ER в категории сбора данных</span><span class="sxs-lookup"><span data-stu-id="7540f-103">List of ER functions in the data collection category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7540f-104">Функции сбора данных электронной отчетности (ER) используются для подсчета и подведения итогов в формате ER, который выполняется, на основе данных вывода, которые уже были созданы в формате **Текст** или **Xml**.</span><span class="sxs-lookup"><span data-stu-id="7540f-104">Electronic reporting (ER) data collection functions are used to do counting and summing in an ER format that is being run, based on data of the output that has already been generated in **Text** or **Xml** format.</span></span> <span data-ttu-id="7540f-105">Этот подход используется для повышения производительности формата ER, который работает, для ввода значений итогов выполнения в создаваемых документах и для других целей.</span><span class="sxs-lookup"><span data-stu-id="7540f-105">This approach is used to help improve performance of an ER format that is run, to enter values of running totals in generated documents, and for other purposes.</span></span> <span data-ttu-id="7540f-106">В этой теме приводится краткое изложение этих функций.</span><span class="sxs-lookup"><span data-stu-id="7540f-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="7540f-107">Список поддерживаемых функций</span><span class="sxs-lookup"><span data-stu-id="7540f-107">List of supported functions</span></span>

| <span data-ttu-id="7540f-108">Функция</span><span class="sxs-lookup"><span data-stu-id="7540f-108">Function</span></span> | <span data-ttu-id="7540f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="7540f-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="7540f-110">CollectedList</span><span class="sxs-lookup"><span data-stu-id="7540f-110">CollectedList</span></span>](er-functions-datacollection-collectedlist.md) | <span data-ttu-id="7540f-111">Эта функция возвращает значение *Список записей*, содержащее список значений, которые были возвращены свойством **Значение ключа собранных данных** формата элементов и собраны, когда элементы формата использовались для создания исходящего документа во время выполнения формата, и что удовлетворяет указанным условиям.</span><span class="sxs-lookup"><span data-stu-id="7540f-111">This function returns a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="7540f-112">Каждое условие состоит из диапазона ключей и значения ключа.</span><span class="sxs-lookup"><span data-stu-id="7540f-112">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="7540f-113">CountIF</span><span class="sxs-lookup"><span data-stu-id="7540f-113">CountIF</span></span>](er-functions-datacollection-countif.md) | <span data-ttu-id="7540f-114">Эта функция возвращает *целочисленное* значение, представляющее количество элементов формата, которые были собраны при использовании элементов формата для создания исходящего документа во время выполнения формата, и удовлетворяющее указанному условию.</span><span class="sxs-lookup"><span data-stu-id="7540f-114">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="7540f-115">Условие состоит из диапазона ключей и значения ключа.</span><span class="sxs-lookup"><span data-stu-id="7540f-115">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="7540f-116">CountIFs</span><span class="sxs-lookup"><span data-stu-id="7540f-116">CountIFs</span></span>](er-functions-datacollection-countifs.md) | <span data-ttu-id="7540f-117">Эта функция возвращает *целочисленное* значение, представляющее количество элементов формата, которые были собраны при использовании элементов формата для создания исходящего документа во время выполнения формата, и удовлетворяющее указанным условиям.</span><span class="sxs-lookup"><span data-stu-id="7540f-117">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="7540f-118">Каждое условие состоит из диапазона ключей и значения ключа.</span><span class="sxs-lookup"><span data-stu-id="7540f-118">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="7540f-119">FormatElementName</span><span class="sxs-lookup"><span data-stu-id="7540f-119">FormatElementName</span></span>](er-functions-datacollection-formatelementname.md) | <span data-ttu-id="7540f-120">Эта функция возвращает значение *строка*, представляющее имя элемента текущего формата ER.</span><span class="sxs-lookup"><span data-stu-id="7540f-120">This function returns a *String* value that represents the name of the current ER format's element.</span></span> |
| [<span data-ttu-id="7540f-121">SumIF</span><span class="sxs-lookup"><span data-stu-id="7540f-121">SumIF</span></span>](er-functions-datacollection-sumif.md) | <span data-ttu-id="7540f-122">Эта функция возвращает *вещественное* значение, представляющее сумму значений, которые были возвращены привязками элементов формата и собраны во время использования для создания исходящего документа во время выполнения формата, и удовлетворяющее указанному условию.</span><span class="sxs-lookup"><span data-stu-id="7540f-122">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="7540f-123">Условие состоит из диапазона ключей и значения ключа.</span><span class="sxs-lookup"><span data-stu-id="7540f-123">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="7540f-124">SumIFs</span><span class="sxs-lookup"><span data-stu-id="7540f-124">SumIFs</span></span>](er-functions-datacollection-sumifs.md) | <span data-ttu-id="7540f-125">Эта функция возвращает *вещественное* значение, представляющее сумму значений, которые были возвращены привязками элементов формата и собраны во время использования для создания исходящего документа во время выполнения формата, и удовлетворяющее указанным условиям.</span><span class="sxs-lookup"><span data-stu-id="7540f-125">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="7540f-126">Каждое условие состоит из диапазона ключей и значения ключа.</span><span class="sxs-lookup"><span data-stu-id="7540f-126">Each condition consists of a key range and a key value.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="7540f-127">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7540f-127">Additional resources</span></span>

[<span data-ttu-id="7540f-128">Обзор электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="7540f-128">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="7540f-129">Конструктор формул в электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="7540f-129">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="7540f-130">Язык формул электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="7540f-130">Electronic reporting formula language</span></span>](er-formula-language.md)
