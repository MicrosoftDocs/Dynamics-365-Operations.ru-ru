---
title: Функция ER REVERSE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности REVERSE.
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
ms.openlocfilehash: 3343ad788cef29a79f9b110bf29809cd5f0e5c63
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917243"
---
# <span data-ttu-id="2c30c-103"><a name="REVERSE">Функция ER REVERSE</a></span><span class="sxs-lookup"><span data-stu-id="2c30c-103"><a name="REVERSE">REVERSE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c30c-104">Функция `REVERSE` возвращает указанный список в качестве значения *Список записей* в обратном порядке сортировки.</span><span class="sxs-lookup"><span data-stu-id="2c30c-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c30c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c30c-105">Syntax</span></span>

```
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="2c30c-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="2c30c-106">Arguments</span></span>

<span data-ttu-id="2c30c-107">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="2c30c-107">`list`: *Record list*</span></span>

<span data-ttu-id="2c30c-108">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="2c30c-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="2c30c-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="2c30c-109">Return values</span></span>

<span data-ttu-id="2c30c-110">*Список записей*</span><span class="sxs-lookup"><span data-stu-id="2c30c-110">*Record list*</span></span>

<span data-ttu-id="2c30c-111">Полученный список записей.</span><span class="sxs-lookup"><span data-stu-id="2c30c-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="2c30c-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2c30c-112">Example 1</span></span>

<span data-ttu-id="2c30c-113">Если вы введете источник данных **DS** типа *Вычисляемое поле* и он содержит выражение `SPLIT ("C|B|A", "|")`, выражение `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` возвращает текстовое значение **"C"**.</span><span class="sxs-lookup"><span data-stu-id="2c30c-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="2c30c-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2c30c-114">Example 2</span></span>

<span data-ttu-id="2c30c-115">Если **Поставщик** настраивается в качестве источника данных электронной отчетности (ER), который ссылается на таблицу VendTable, выражение `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` возвращает список поставщиков, который отсортирован по имени в нисходящем порядке.</span><span class="sxs-lookup"><span data-stu-id="2c30c-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c30c-116">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2c30c-116">Additional resources</span></span>

[<span data-ttu-id="2c30c-117">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="2c30c-117">List functions</span></span>](er-functions-category-list.md)
