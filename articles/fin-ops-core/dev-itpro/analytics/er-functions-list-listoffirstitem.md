---
title: Функция ER LISTOFFIRSTITEM
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности LISTOFFIRSTITEM.
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
ms.openlocfilehash: 8ea81bce8cd6b922f3ef1d53ec0c4b2574780377
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686496"
---
# <a name="listoffirstitem-er-function"></a><span data-ttu-id="5d007-103">Функция ER LISTOFFIRSTITEM</span><span class="sxs-lookup"><span data-stu-id="5d007-103">LISTOFFIRSTITEM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d007-104">Функция `LISTOFFIRSTITEM` возвращает значение *Список записей*, состоящее только из первой записи указанного списка.</span><span class="sxs-lookup"><span data-stu-id="5d007-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d007-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d007-105">Syntax</span></span>

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="5d007-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="5d007-106">Arguments</span></span>

<span data-ttu-id="5d007-107">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="5d007-107">`list`: *Record list*</span></span>

<span data-ttu-id="5d007-108">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="5d007-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="5d007-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="5d007-109">Return values</span></span>

<span data-ttu-id="5d007-110">*Список записей*</span><span class="sxs-lookup"><span data-stu-id="5d007-110">*Record list*</span></span>

<span data-ttu-id="5d007-111">Полученный список записей.</span><span class="sxs-lookup"><span data-stu-id="5d007-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="5d007-112">Пример</span><span class="sxs-lookup"><span data-stu-id="5d007-112">Example</span></span>

<span data-ttu-id="5d007-113">Выражение `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` возвращает значение текста **"A"**.</span><span class="sxs-lookup"><span data-stu-id="5d007-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5d007-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5d007-114">Additional resources</span></span>

[<span data-ttu-id="5d007-115">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="5d007-115">List functions</span></span>](er-functions-category-list.md)
