---
title: Функция ER SPLITLIST
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности SPLITLIST.
author: NickSelin
ms.date: 03/15/2021
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
ms.openlocfilehash: 99e199e238b3132622a8b305895637b430e8f6d2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745577"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="77030-103">Функция ER SPLITLIST</span><span class="sxs-lookup"><span data-stu-id="77030-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77030-104">Функция `SPLITLIST` разделяет список на подсписки (или пакеты), каждый из которых содержит указанное число записей.</span><span class="sxs-lookup"><span data-stu-id="77030-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="77030-105">Затем она возвращает результат в качестве нового значения *Список записей*, которое состоит из пакетов.</span><span class="sxs-lookup"><span data-stu-id="77030-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="77030-106">Синтаксис 1</span><span class="sxs-lookup"><span data-stu-id="77030-106">Syntax 1</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a><span data-ttu-id="77030-107">Синтаксис 2</span><span class="sxs-lookup"><span data-stu-id="77030-107">Syntax 2</span></span>

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a><span data-ttu-id="77030-108">Аргументы</span><span class="sxs-lookup"><span data-stu-id="77030-108">Arguments</span></span>

<span data-ttu-id="77030-109">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="77030-109">`list`: *Record list*</span></span>

<span data-ttu-id="77030-110">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="77030-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="77030-111">`number`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="77030-111">`number`: *Integer*</span></span>

<span data-ttu-id="77030-112">Максимальное количество записей на один пакет.</span><span class="sxs-lookup"><span data-stu-id="77030-112">The maximum number of records per batch.</span></span>

<span data-ttu-id="77030-113">`on-demand reading flag`: *Логический*</span><span class="sxs-lookup"><span data-stu-id="77030-113">`on-demand reading flag`: *Boolean*</span></span>

<span data-ttu-id="77030-114">*Логическое* значение, которое указывает, должны ли при необходимости создаваться элементы вложенных списков.</span><span class="sxs-lookup"><span data-stu-id="77030-114">A *Boolean* value that specifies whether elements of sublists should be generated on demand.</span></span>

## <a name="return-values"></a><span data-ttu-id="77030-115">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="77030-115">Return values</span></span>

<span data-ttu-id="77030-116">*Список записей*</span><span class="sxs-lookup"><span data-stu-id="77030-116">*Record list*</span></span>

<span data-ttu-id="77030-117">Полученный список записей.</span><span class="sxs-lookup"><span data-stu-id="77030-117">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="77030-118">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="77030-118">Usage notes</span></span>

<span data-ttu-id="77030-119">Возвращаемый список пакетов содержит следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="77030-119">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="77030-120">**Значение:** *Список*</span><span class="sxs-lookup"><span data-stu-id="77030-120">**Value:** *List*</span></span>

    <span data-ttu-id="77030-121">Список записей, относящихся к текущему пакету.</span><span class="sxs-lookup"><span data-stu-id="77030-121">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="77030-122">**BatchNumber:** *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="77030-122">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="77030-123">Номер текущего пакета в возвращенном списке.</span><span class="sxs-lookup"><span data-stu-id="77030-123">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="77030-124">Если флаг чтения по запросу имеет значение **True**, вложенные списки создаются после запроса, что позволяет уменьшить потребление памяти, но может привести к ухудшению производительности, если элементы не используются последовательно.</span><span class="sxs-lookup"><span data-stu-id="77030-124">When the on-demand reading flag is set to **True**, sublists are generated upon request which allows for a reduction in memory consumption but may cause performance degradation if elements aren't used sequentially.</span></span>

## <a name="example"></a><span data-ttu-id="77030-125">Пример</span><span class="sxs-lookup"><span data-stu-id="77030-125">Example</span></span>

<span data-ttu-id="77030-126">На следующем рисунке источник данных **Строки** создается как список записей, содержащий три записи.</span><span class="sxs-lookup"><span data-stu-id="77030-126">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="77030-127">Этот список разделяется на пакеты, каждый из которых содержит до двух записей.</span><span class="sxs-lookup"><span data-stu-id="77030-127">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="77030-128">На следующем рисунке показан созданный макет формата.</span><span class="sxs-lookup"><span data-stu-id="77030-128">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="77030-129">В этом макете формата привязки к источнику данных **Строки** создаются для создания выходных данных в формате XML.</span><span class="sxs-lookup"><span data-stu-id="77030-129">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="77030-130">Эти выходные данные представляют отдельные узлы для каждого пакета и записей в нем.</span><span class="sxs-lookup"><span data-stu-id="77030-130">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="77030-131">На следующем рисунке показан результат выполнения созданного формата.</span><span class="sxs-lookup"><span data-stu-id="77030-131">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="77030-132">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="77030-132">Additional resources</span></span>

[<span data-ttu-id="77030-133">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="77030-133">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
