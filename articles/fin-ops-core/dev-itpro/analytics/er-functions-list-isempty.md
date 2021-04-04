---
title: Функция ER ISEMPTY
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ISEMPTY.
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
ms.openlocfilehash: b689e6d4bb849f07db5d00cf8a9dc5c16646a927
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563880"
---
# <a name="isempty-er-function"></a><span data-ttu-id="a224e-103">Функция ER ISEMPTY</span><span class="sxs-lookup"><span data-stu-id="a224e-103">ISEMPTY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a224e-104">Функция `ISEMPTY` возвращает *логическое* значение **TRUE**, если указанный список не содержит записей.</span><span class="sxs-lookup"><span data-stu-id="a224e-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="a224e-105">В противном случае возвращает *логическое* значение **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a224e-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a224e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a224e-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="a224e-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="a224e-107">Arguments</span></span>

<span data-ttu-id="a224e-108">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="a224e-108">`list`: *Record list*</span></span>

<span data-ttu-id="a224e-109">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="a224e-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="a224e-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="a224e-110">Return values</span></span>

<span data-ttu-id="a224e-111">*Логический*</span><span class="sxs-lookup"><span data-stu-id="a224e-111">*Boolean*</span></span>

<span data-ttu-id="a224e-112">Результирующее *логическое* значение.</span><span class="sxs-lookup"><span data-stu-id="a224e-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="a224e-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a224e-113">Example 1</span></span>

<span data-ttu-id="a224e-114">Если вы введете источник данных **DS** типа *Вычисляемое поле* и он содержит выражение `SPLIT ("A|B|C", "|")`, выражение `ISEMPTY(DS)` возвращает **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a224e-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="a224e-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a224e-115">Example 2</span></span>

<span data-ttu-id="a224e-116">Выражение `ISEMPTY (SPLIT ("",1))` возвращает **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="a224e-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a224e-117">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a224e-117">Additional resources</span></span>

[<span data-ttu-id="a224e-118">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="a224e-118">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]