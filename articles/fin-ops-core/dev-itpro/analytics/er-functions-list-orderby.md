---
title: Функция ER ORDERBY
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ORDERBY.
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
ms.openlocfilehash: c39700fab90265ed1915b4815a6bb27af58d9516
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686472"
---
# <a name="orderby-er-function"></a><span data-ttu-id="ce7c4-103">Функция ER ORDERBY</span><span class="sxs-lookup"><span data-stu-id="ce7c4-103">ORDERBY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce7c4-104">Функция `ORDERBY` возвращает указанный список в качестве значения *Список записей* после того, как он был отсортирован в соответствии с указанными аргументами.</span><span class="sxs-lookup"><span data-stu-id="ce7c4-104">The `ORDERBY` function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="ce7c4-105">Эти аргументы могут определяться как выражения.</span><span class="sxs-lookup"><span data-stu-id="ce7c4-105">These arguments can be defined as expressions.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce7c4-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce7c4-106">Syntax</span></span>

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a><span data-ttu-id="ce7c4-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="ce7c4-107">Arguments</span></span>

<span data-ttu-id="ce7c4-108">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="ce7c4-108">`list`: *Record list*</span></span>

<span data-ttu-id="ce7c4-109">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="ce7c4-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="ce7c4-110">`expression 1`: *Поле*</span><span class="sxs-lookup"><span data-stu-id="ce7c4-110">`expression 1`: *Field*</span></span>

<span data-ttu-id="ce7c4-111">Действительный путь поля источника данных, на который ссылается аргумент `list` вызываемой функции.</span><span class="sxs-lookup"><span data-stu-id="ce7c4-111">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="ce7c4-112">Поле, на которое есть ссылка, должно быть полем примитивного типа данных.</span><span class="sxs-lookup"><span data-stu-id="ce7c4-112">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="ce7c4-113">Этот аргумент обязательный.</span><span class="sxs-lookup"><span data-stu-id="ce7c4-113">This argument is required.</span></span>

<span data-ttu-id="ce7c4-114">`expression N`: *Поле*</span><span class="sxs-lookup"><span data-stu-id="ce7c4-114">`expression N`: *Field*</span></span>

<span data-ttu-id="ce7c4-115">Действительный путь поля источника данных, на который ссылается аргумент `list` вызываемой функции.</span><span class="sxs-lookup"><span data-stu-id="ce7c4-115">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="ce7c4-116">Поле, на которое есть ссылка, должно быть полем примитивного типа данных.</span><span class="sxs-lookup"><span data-stu-id="ce7c4-116">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="ce7c4-117">Эти дополнительные аргументы являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="ce7c4-117">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="ce7c4-118">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ce7c4-118">Return values</span></span>

<span data-ttu-id="ce7c4-119">*Список записей*</span><span class="sxs-lookup"><span data-stu-id="ce7c4-119">*Record list*</span></span>

<span data-ttu-id="ce7c4-120">Полученный список записей.</span><span class="sxs-lookup"><span data-stu-id="ce7c4-120">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="ce7c4-121">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ce7c4-121">Example 1</span></span>

<span data-ttu-id="ce7c4-122">Если вы введете источник данных **DS** типа *Вычисляемое поле* и он содержит выражение `SPLIT ("C|B|A", "|")`, выражение `FIRST( ORDERBY( DS, DS. Value)).Value` возвращает текстовое значение **"A"**.</span><span class="sxs-lookup"><span data-stu-id="ce7c4-122">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( ORDERBY( DS, DS. Value)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="ce7c4-123">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ce7c4-123">Example 2</span></span>

<span data-ttu-id="ce7c4-124">Если **Поставщик** настраивается в качестве источника данных электронной отчетности (ER), который ссылается на таблицу VendTable, выражение `ORDERBY (Vendors, Vendors.'name()')` возвращает список поставщиков, который отсортирован по имени в восходящем порядке.</span><span class="sxs-lookup"><span data-stu-id="ce7c4-124">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `ORDERBY (Vendors, Vendors.'name()')` returns a list of vendors that is sorted by name in ascending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ce7c4-125">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ce7c4-125">Additional resources</span></span>

[<span data-ttu-id="ce7c4-126">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="ce7c4-126">List functions</span></span>](er-functions-category-list.md)
