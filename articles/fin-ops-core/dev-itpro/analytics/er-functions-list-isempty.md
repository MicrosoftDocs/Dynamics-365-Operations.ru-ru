---
title: Функция ER ISEMPTY
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ISEMPTY.
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
ms.openlocfilehash: 9c33e8b613bf5bf5bc17a42a7668d4cc4ee58e53
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750444"
---
# <a name="isempty-er-function"></a><span data-ttu-id="dc809-103">Функция ER ISEMPTY</span><span class="sxs-lookup"><span data-stu-id="dc809-103">ISEMPTY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc809-104">Функция `ISEMPTY` возвращает *логическое* значение **TRUE**, если указанный список не содержит записей.</span><span class="sxs-lookup"><span data-stu-id="dc809-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="dc809-105">В противном случае возвращает *логическое* значение **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="dc809-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc809-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc809-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="dc809-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="dc809-107">Arguments</span></span>

<span data-ttu-id="dc809-108">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="dc809-108">`list`: *Record list*</span></span>

<span data-ttu-id="dc809-109">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="dc809-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="dc809-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="dc809-110">Return values</span></span>

<span data-ttu-id="dc809-111">*Логический*</span><span class="sxs-lookup"><span data-stu-id="dc809-111">*Boolean*</span></span>

<span data-ttu-id="dc809-112">Результирующее *логическое* значение.</span><span class="sxs-lookup"><span data-stu-id="dc809-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="dc809-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dc809-113">Example 1</span></span>

<span data-ttu-id="dc809-114">Если вы введете источник данных **DS** типа *Вычисляемое поле* и он содержит выражение `SPLIT ("A|B|C", "|")`, выражение `ISEMPTY(DS)` возвращает **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="dc809-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="dc809-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="dc809-115">Example 2</span></span>

<span data-ttu-id="dc809-116">Выражение `ISEMPTY (SPLIT ("",1))` возвращает **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="dc809-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dc809-117">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="dc809-117">Additional resources</span></span>

[<span data-ttu-id="dc809-118">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="dc809-118">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]