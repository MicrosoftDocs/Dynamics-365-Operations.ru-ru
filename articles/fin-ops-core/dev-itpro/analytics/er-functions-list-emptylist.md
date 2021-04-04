---
title: Функция ER EMPTYLIST
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности EMPTYLIST.
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
ms.openlocfilehash: f6c2777065656affc992a427194286008c1df42f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559208"
---
# <a name="emptylist-er-function"></a><span data-ttu-id="25ba5-103">Функция ER EMPTYLIST</span><span class="sxs-lookup"><span data-stu-id="25ba5-103">EMPTYLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25ba5-104">Функция `EMPTYLIST` возвращает пустое значение *Список записей* с использованием указанного списка в качестве источника для структуры списка.</span><span class="sxs-lookup"><span data-stu-id="25ba5-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="25ba5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25ba5-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="25ba5-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="25ba5-106">Arguments</span></span>

<span data-ttu-id="25ba5-107">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="25ba5-107">`list`: *Record list*</span></span>

<span data-ttu-id="25ba5-108">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="25ba5-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="25ba5-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="25ba5-109">Return values</span></span>

<span data-ttu-id="25ba5-110">*Список записей*</span><span class="sxs-lookup"><span data-stu-id="25ba5-110">*Record list*</span></span>

<span data-ttu-id="25ba5-111">Полученный список записей.</span><span class="sxs-lookup"><span data-stu-id="25ba5-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="25ba5-112">Пример</span><span class="sxs-lookup"><span data-stu-id="25ba5-112">Example</span></span>

<span data-ttu-id="25ba5-113">`EMPTYLIST (SPLIT ("abc", 1))` возвращает новый пустой список, который имеет такую же структуру, как список, который возвращен функцией `SPLIT`.</span><span class="sxs-lookup"><span data-stu-id="25ba5-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="25ba5-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="25ba5-114">Additional resources</span></span>

[<span data-ttu-id="25ba5-115">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="25ba5-115">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]