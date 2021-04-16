---
title: Функция ER REVERSE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности REVERSE.
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
ms.openlocfilehash: 746a736c8797c1c1c5bd71d7d803be4212984595
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755212"
---
# <a name="reverse-er-function"></a><span data-ttu-id="314c1-103">Функция ER REVERSE</span><span class="sxs-lookup"><span data-stu-id="314c1-103">REVERSE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="314c1-104">Функция `REVERSE` возвращает указанный список в качестве значения *Список записей* в обратном порядке сортировки.</span><span class="sxs-lookup"><span data-stu-id="314c1-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="314c1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="314c1-105">Syntax</span></span>

```vb
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="314c1-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="314c1-106">Arguments</span></span>

<span data-ttu-id="314c1-107">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="314c1-107">`list`: *Record list*</span></span>

<span data-ttu-id="314c1-108">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="314c1-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="314c1-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="314c1-109">Return values</span></span>

<span data-ttu-id="314c1-110">*Список записей*</span><span class="sxs-lookup"><span data-stu-id="314c1-110">*Record list*</span></span>

<span data-ttu-id="314c1-111">Полученный список записей.</span><span class="sxs-lookup"><span data-stu-id="314c1-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="314c1-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="314c1-112">Example 1</span></span>

<span data-ttu-id="314c1-113">Если вы введете источник данных **DS** типа *Вычисляемое поле* и он содержит выражение `SPLIT ("C|B|A", "|")`, выражение `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` возвращает текстовое значение **"C"**.</span><span class="sxs-lookup"><span data-stu-id="314c1-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="314c1-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="314c1-114">Example 2</span></span>

<span data-ttu-id="314c1-115">Если **Поставщик** настраивается в качестве источника данных электронной отчетности (ER), который ссылается на таблицу VendTable, выражение `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` возвращает список поставщиков, который отсортирован по имени в нисходящем порядке.</span><span class="sxs-lookup"><span data-stu-id="314c1-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="314c1-116">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="314c1-116">Additional resources</span></span>

[<span data-ttu-id="314c1-117">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="314c1-117">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]