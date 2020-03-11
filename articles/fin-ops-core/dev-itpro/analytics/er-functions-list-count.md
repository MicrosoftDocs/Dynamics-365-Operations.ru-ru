---
title: Функция ER COUNT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности COUNT.
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
ms.openlocfilehash: 72d2ea1b26c295c97575a3c7a479ee4e06762424
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042213"
---
# <span data-ttu-id="33bab-103"><a name="COUNT">Функция ER COUNT</a></span><span class="sxs-lookup"><span data-stu-id="33bab-103"><a name="COUNT">COUNT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33bab-104">Функция `COUNT` возвращает *целочисленное* значение, представляющее количество записей в указанном списке, если список не пуст.</span><span class="sxs-lookup"><span data-stu-id="33bab-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="33bab-105">Если список пуст, эта функция возвращает **0** (ноль).</span><span class="sxs-lookup"><span data-stu-id="33bab-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="33bab-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="33bab-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="33bab-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="33bab-107">Arguments</span></span>

<span data-ttu-id="33bab-108">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="33bab-108">`list`: *Record list*</span></span>

<span data-ttu-id="33bab-109">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="33bab-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="33bab-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="33bab-110">Return values</span></span>

<span data-ttu-id="33bab-111">*Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="33bab-111">*Integer*</span></span>

<span data-ttu-id="33bab-112">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="33bab-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="33bab-113">Пример</span><span class="sxs-lookup"><span data-stu-id="33bab-113">Example</span></span>

<span data-ttu-id="33bab-114">`COUNT (SPLIT("abcd" , 3))` возвращает **2**, потому что функция `SPLIT`, которая используется в этом примере, создает список, который состоит из двух записей.</span><span class="sxs-lookup"><span data-stu-id="33bab-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="33bab-115">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="33bab-115">Additional resources</span></span>

[<span data-ttu-id="33bab-116">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="33bab-116">List functions</span></span>](er-functions-category-list.md)
