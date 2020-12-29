---
title: Функция ER EMPTYLIST
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности EMPTYLIST.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ccb52d7d88f292720360ae913ead5be239165193
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687678"
---
# <a name="emptylist-er-function"></a><span data-ttu-id="a1f29-103">Функция ER EMPTYLIST</span><span class="sxs-lookup"><span data-stu-id="a1f29-103">EMPTYLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1f29-104">Функция `EMPTYLIST` возвращает пустое значение *Список записей* с использованием указанного списка в качестве источника для структуры списка.</span><span class="sxs-lookup"><span data-stu-id="a1f29-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1f29-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a1f29-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="a1f29-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="a1f29-106">Arguments</span></span>

<span data-ttu-id="a1f29-107">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="a1f29-107">`list`: *Record list*</span></span>

<span data-ttu-id="a1f29-108">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="a1f29-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="a1f29-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="a1f29-109">Return values</span></span>

<span data-ttu-id="a1f29-110">*Список записей*</span><span class="sxs-lookup"><span data-stu-id="a1f29-110">*Record list*</span></span>

<span data-ttu-id="a1f29-111">Полученный список записей.</span><span class="sxs-lookup"><span data-stu-id="a1f29-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="a1f29-112">Пример</span><span class="sxs-lookup"><span data-stu-id="a1f29-112">Example</span></span>

<span data-ttu-id="a1f29-113">`EMPTYLIST (SPLIT ("abc", 1))` возвращает новый пустой список, который имеет такую же структуру, как список, который возвращен функцией `SPLIT`.</span><span class="sxs-lookup"><span data-stu-id="a1f29-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a1f29-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a1f29-114">Additional resources</span></span>

[<span data-ttu-id="a1f29-115">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="a1f29-115">List functions</span></span>](er-functions-category-list.md)
