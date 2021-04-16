---
title: Функция ER ORDERBY
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ORDERBY.
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
ms.openlocfilehash: 51da7f3766f5af901c8be6668bc2511cd8e2f9e9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753200"
---
# <a name="orderby-er-function"></a><span data-ttu-id="03125-103">Функция ER ORDERBY</span><span class="sxs-lookup"><span data-stu-id="03125-103">ORDERBY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03125-104">Функция `ORDERBY` возвращает указанный список в качестве значения *Список записей* после того, как он был отсортирован в соответствии с указанными аргументами.</span><span class="sxs-lookup"><span data-stu-id="03125-104">The `ORDERBY` function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="03125-105">Эти аргументы могут определяться как выражения.</span><span class="sxs-lookup"><span data-stu-id="03125-105">These arguments can be defined as expressions.</span></span>

## <a name="syntax"></a><span data-ttu-id="03125-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03125-106">Syntax</span></span>

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a><span data-ttu-id="03125-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="03125-107">Arguments</span></span>

<span data-ttu-id="03125-108">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="03125-108">`list`: *Record list*</span></span>

<span data-ttu-id="03125-109">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="03125-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="03125-110">`expression 1`: *Поле*</span><span class="sxs-lookup"><span data-stu-id="03125-110">`expression 1`: *Field*</span></span>

<span data-ttu-id="03125-111">Действительный путь поля источника данных, на который ссылается аргумент `list` вызываемой функции.</span><span class="sxs-lookup"><span data-stu-id="03125-111">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="03125-112">Поле, на которое есть ссылка, должно быть полем примитивного типа данных.</span><span class="sxs-lookup"><span data-stu-id="03125-112">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="03125-113">Этот аргумент обязательный.</span><span class="sxs-lookup"><span data-stu-id="03125-113">This argument is required.</span></span>

<span data-ttu-id="03125-114">`expression N`: *Поле*</span><span class="sxs-lookup"><span data-stu-id="03125-114">`expression N`: *Field*</span></span>

<span data-ttu-id="03125-115">Действительный путь поля источника данных, на который ссылается аргумент `list` вызываемой функции.</span><span class="sxs-lookup"><span data-stu-id="03125-115">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="03125-116">Поле, на которое есть ссылка, должно быть полем примитивного типа данных.</span><span class="sxs-lookup"><span data-stu-id="03125-116">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="03125-117">Эти дополнительные аргументы являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="03125-117">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="03125-118">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="03125-118">Return values</span></span>

<span data-ttu-id="03125-119">*Список записей*</span><span class="sxs-lookup"><span data-stu-id="03125-119">*Record list*</span></span>

<span data-ttu-id="03125-120">Полученный список записей.</span><span class="sxs-lookup"><span data-stu-id="03125-120">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="03125-121">Пример 1</span><span class="sxs-lookup"><span data-stu-id="03125-121">Example 1</span></span>

<span data-ttu-id="03125-122">Если вы введете источник данных **DS** типа *Вычисляемое поле* и он содержит выражение `SPLIT ("C|B|A", "|")`, выражение `FIRST( ORDERBY( DS, DS. Value)).Value` возвращает текстовое значение **"A"**.</span><span class="sxs-lookup"><span data-stu-id="03125-122">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( ORDERBY( DS, DS. Value)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="03125-123">Пример 2</span><span class="sxs-lookup"><span data-stu-id="03125-123">Example 2</span></span>

<span data-ttu-id="03125-124">Если **Поставщик** настраивается в качестве источника данных электронной отчетности (ER), который ссылается на таблицу VendTable, выражение `ORDERBY (Vendors, Vendors.'name()')` возвращает список поставщиков, который отсортирован по имени в восходящем порядке.</span><span class="sxs-lookup"><span data-stu-id="03125-124">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `ORDERBY (Vendors, Vendors.'name()')` returns a list of vendors that is sorted by name in ascending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="03125-125">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="03125-125">Additional resources</span></span>

[<span data-ttu-id="03125-126">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="03125-126">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]