---
title: Функция ER SPLITLIST
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности SPLITLIST.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: b324d42a53b35074ba62ccf3df7b77cb4db70450
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917220"
---
# <span data-ttu-id="e69c9-103"><a name="SPLITLIST">Функция ER SPLITLIST</a></span><span class="sxs-lookup"><span data-stu-id="e69c9-103"><a name="SPLITLIST">SPLITLIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e69c9-104">Функция `SPLITLIST` разделяет список на подсписки (или пакеты), каждый из которых содержит указанное число записей.</span><span class="sxs-lookup"><span data-stu-id="e69c9-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="e69c9-105">Затем она возвращает результат в качестве нового значения *Список записей*, которое состоит из пакетов.</span><span class="sxs-lookup"><span data-stu-id="e69c9-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="e69c9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e69c9-106">Syntax</span></span>

```
SPLITLIST (list, number)
```

## <a name="arguments"></a><span data-ttu-id="e69c9-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="e69c9-107">Arguments</span></span>

<span data-ttu-id="e69c9-108">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="e69c9-108">`list`: *Record list*</span></span>

<span data-ttu-id="e69c9-109">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="e69c9-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="e69c9-110">`number`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="e69c9-110">`number`: *Integer*</span></span>

<span data-ttu-id="e69c9-111">Максимальное количество записей на один пакет.</span><span class="sxs-lookup"><span data-stu-id="e69c9-111">The maximum number of records per batch.</span></span>

## <a name="return-values"></a><span data-ttu-id="e69c9-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="e69c9-112">Return values</span></span>

<span data-ttu-id="e69c9-113">*Список записей*</span><span class="sxs-lookup"><span data-stu-id="e69c9-113">*Record list*</span></span>

<span data-ttu-id="e69c9-114">Полученный список записей.</span><span class="sxs-lookup"><span data-stu-id="e69c9-114">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e69c9-115">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="e69c9-115">Usage notes</span></span>

<span data-ttu-id="e69c9-116">Возвращаемый список пакетов содержит следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="e69c9-116">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="e69c9-117">**Значение:** *Список*</span><span class="sxs-lookup"><span data-stu-id="e69c9-117">**Value:** *List*</span></span>

    <span data-ttu-id="e69c9-118">Список записей, относящихся к текущему пакету.</span><span class="sxs-lookup"><span data-stu-id="e69c9-118">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="e69c9-119">**BatchNumber:** *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="e69c9-119">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="e69c9-120">Номер текущего пакета в возвращенном списке.</span><span class="sxs-lookup"><span data-stu-id="e69c9-120">The number of the current batch in the returned list.</span></span>

## <a name="example"></a><span data-ttu-id="e69c9-121">Пример</span><span class="sxs-lookup"><span data-stu-id="e69c9-121">Example</span></span>

<span data-ttu-id="e69c9-122">На следующем рисунке источник данных **Строки** создается как список записей, содержащий три записи.</span><span class="sxs-lookup"><span data-stu-id="e69c9-122">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="e69c9-123">Этот список разделяется на пакеты, каждый из которых содержит до двух записей.</span><span class="sxs-lookup"><span data-stu-id="e69c9-123">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="e69c9-124">На следующем рисунке показан созданный макет формата.</span><span class="sxs-lookup"><span data-stu-id="e69c9-124">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="e69c9-125">В этом макете формата привязки к источнику данных **Строки** создаются для создания выходных данных в формате XML.</span><span class="sxs-lookup"><span data-stu-id="e69c9-125">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="e69c9-126">Эти выходные данные представляют отдельные узлы для каждого пакета и записей в нем.</span><span class="sxs-lookup"><span data-stu-id="e69c9-126">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="e69c9-127">На следующем рисунке показан результат выполнения созданного формата.</span><span class="sxs-lookup"><span data-stu-id="e69c9-127">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="e69c9-128">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e69c9-128">Additional resources</span></span>

[<span data-ttu-id="e69c9-129">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="e69c9-129">List functions</span></span>](er-functions-category-list.md)
