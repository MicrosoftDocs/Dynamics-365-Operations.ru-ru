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
ms.openlocfilehash: c8450c17fe2de964016951197b0d4e231c550a99
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916139"
---
# <span data-ttu-id="9d490-103"><a name="ISEMPTY">Функция ER ISEMPTY</a></span><span class="sxs-lookup"><span data-stu-id="9d490-103"><a name="ISEMPTY">ISEMPTY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d490-104">Функция `ISEMPTY` возвращает *логическое* значение **TRUE**, если указанный список не содержит записей.</span><span class="sxs-lookup"><span data-stu-id="9d490-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="9d490-105">В противном случае возвращает *логическое* значение **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="9d490-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d490-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d490-106">Syntax</span></span>

```
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="9d490-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="9d490-107">Arguments</span></span>

<span data-ttu-id="9d490-108">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="9d490-108">`list`: *Record list*</span></span>

<span data-ttu-id="9d490-109">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="9d490-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="9d490-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="9d490-110">Return values</span></span>

<span data-ttu-id="9d490-111">*Логический*</span><span class="sxs-lookup"><span data-stu-id="9d490-111">*Boolean*</span></span>

<span data-ttu-id="9d490-112">Результирующее *логическое* значение.</span><span class="sxs-lookup"><span data-stu-id="9d490-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="9d490-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9d490-113">Example 1</span></span>

<span data-ttu-id="9d490-114">Если вы введете источник данных **DS** типа *Вычисляемое поле* и он содержит выражение `SPLIT ("A|B|C", "|")`, выражение `ISEMPTY(DS)` возвращает **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="9d490-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="9d490-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9d490-115">Example 2</span></span>

<span data-ttu-id="9d490-116">Выражение `ISEMPTY (SPLIT ("",1))` возвращает **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="9d490-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9d490-117">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9d490-117">Additional resources</span></span>

[<span data-ttu-id="9d490-118">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="9d490-118">List functions</span></span>](er-functions-category-list.md)
