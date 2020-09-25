---
title: Функция ER ISEMPTY
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ISEMPTY.
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
ms.openlocfilehash: 5b6fde7cbadec7aae052742ef598e1af4dbae793
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745137"
---
# <a name="isempty-er-function"></a><span data-ttu-id="bd5a8-103">Функция ER ISEMPTY</span><span class="sxs-lookup"><span data-stu-id="bd5a8-103">ISEMPTY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd5a8-104">Функция `ISEMPTY` возвращает *логическое* значение **TRUE**, если указанный список не содержит записей.</span><span class="sxs-lookup"><span data-stu-id="bd5a8-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="bd5a8-105">В противном случае возвращает *логическое* значение **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="bd5a8-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd5a8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bd5a8-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="bd5a8-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="bd5a8-107">Arguments</span></span>

<span data-ttu-id="bd5a8-108">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="bd5a8-108">`list`: *Record list*</span></span>

<span data-ttu-id="bd5a8-109">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="bd5a8-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="bd5a8-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="bd5a8-110">Return values</span></span>

<span data-ttu-id="bd5a8-111">*Логический*</span><span class="sxs-lookup"><span data-stu-id="bd5a8-111">*Boolean*</span></span>

<span data-ttu-id="bd5a8-112">Результирующее *логическое* значение.</span><span class="sxs-lookup"><span data-stu-id="bd5a8-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="bd5a8-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bd5a8-113">Example 1</span></span>

<span data-ttu-id="bd5a8-114">Если вы введете источник данных **DS** типа *Вычисляемое поле* и он содержит выражение `SPLIT ("A|B|C", "|")`, выражение `ISEMPTY(DS)` возвращает **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="bd5a8-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="bd5a8-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="bd5a8-115">Example 2</span></span>

<span data-ttu-id="bd5a8-116">Выражение `ISEMPTY (SPLIT ("",1))` возвращает **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="bd5a8-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bd5a8-117">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bd5a8-117">Additional resources</span></span>

[<span data-ttu-id="bd5a8-118">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="bd5a8-118">List functions</span></span>](er-functions-category-list.md)
