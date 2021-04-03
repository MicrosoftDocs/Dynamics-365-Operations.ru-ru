---
title: Функция ER COUNT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности COUNT.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: e36347d928148e85bc9295d529cbf2801946433a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567900"
---
# <a name="count-er-function"></a><span data-ttu-id="73682-103">Функция ER COUNT</span><span class="sxs-lookup"><span data-stu-id="73682-103">COUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73682-104">Функция `COUNT` возвращает *целочисленное* значение, представляющее количество записей в указанном списке, если список не пуст.</span><span class="sxs-lookup"><span data-stu-id="73682-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="73682-105">Если список пуст, эта функция возвращает **0** (ноль).</span><span class="sxs-lookup"><span data-stu-id="73682-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="73682-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73682-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="73682-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="73682-107">Arguments</span></span>

<span data-ttu-id="73682-108">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="73682-108">`list`: *Record list*</span></span>

<span data-ttu-id="73682-109">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="73682-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="73682-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="73682-110">Return values</span></span>

<span data-ttu-id="73682-111">*Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="73682-111">*Integer*</span></span>

<span data-ttu-id="73682-112">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="73682-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="73682-113">Пример</span><span class="sxs-lookup"><span data-stu-id="73682-113">Example</span></span>

<span data-ttu-id="73682-114">`COUNT (SPLIT("abcd" , 3))` возвращает **2**, потому что функция `SPLIT`, которая используется в этом примере, создает список, который состоит из двух записей.</span><span class="sxs-lookup"><span data-stu-id="73682-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="73682-115">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="73682-115">Additional resources</span></span>

[<span data-ttu-id="73682-116">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="73682-116">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]