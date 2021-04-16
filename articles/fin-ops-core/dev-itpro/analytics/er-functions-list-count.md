---
title: Функция ER COUNT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности COUNT.
author: NickSelin
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
ms.openlocfilehash: a0b780051684ef52d06a9baf78d9b513d9ac1f0e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746635"
---
# <a name="count-er-function"></a><span data-ttu-id="c4a85-103">Функция ER COUNT</span><span class="sxs-lookup"><span data-stu-id="c4a85-103">COUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4a85-104">Функция `COUNT` возвращает *целочисленное* значение, представляющее количество записей в указанном списке, если список не пуст.</span><span class="sxs-lookup"><span data-stu-id="c4a85-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="c4a85-105">Если список пуст, эта функция возвращает **0** (ноль).</span><span class="sxs-lookup"><span data-stu-id="c4a85-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="c4a85-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4a85-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="c4a85-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="c4a85-107">Arguments</span></span>

<span data-ttu-id="c4a85-108">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="c4a85-108">`list`: *Record list*</span></span>

<span data-ttu-id="c4a85-109">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="c4a85-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="c4a85-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="c4a85-110">Return values</span></span>

<span data-ttu-id="c4a85-111">*Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="c4a85-111">*Integer*</span></span>

<span data-ttu-id="c4a85-112">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="c4a85-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="c4a85-113">Пример</span><span class="sxs-lookup"><span data-stu-id="c4a85-113">Example</span></span>

<span data-ttu-id="c4a85-114">`COUNT (SPLIT("abcd" , 3))` возвращает **2**, потому что функция `SPLIT`, которая используется в этом примере, создает список, который состоит из двух записей.</span><span class="sxs-lookup"><span data-stu-id="c4a85-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c4a85-115">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c4a85-115">Additional resources</span></span>

[<span data-ttu-id="c4a85-116">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="c4a85-116">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]