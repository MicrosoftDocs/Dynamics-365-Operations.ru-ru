---
title: Функция ER STRINGJOIN
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности STRINGJOIN.
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
ms.openlocfilehash: 10a98e98d913b0b4fe36690f7effd5d8d9a3faf4
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041799"
---
# <span data-ttu-id="37090-103"><a name="STRINGJOIN">Функция ER STRINGJOIN</a></span><span class="sxs-lookup"><span data-stu-id="37090-103"><a name="STRINGJOIN">STRINGJOIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37090-104">Функция `STRINGJOIN` возвращает значение *строка*, состоящее из связанных значений указанного поля из указанного списка.</span><span class="sxs-lookup"><span data-stu-id="37090-104">The `STRINGJOIN` function returns a *String* value that consists of concatenated values of the specified field from the specified list.</span></span> <span data-ttu-id="37090-105">Значения могут разделяться указанным разделителем.</span><span class="sxs-lookup"><span data-stu-id="37090-105">The values can be separated by the specified delimiter.</span></span>

## <a name="syntax"></a><span data-ttu-id="37090-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="37090-106">Syntax</span></span>

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a><span data-ttu-id="37090-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="37090-107">Arguments</span></span>

<span data-ttu-id="37090-108">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="37090-108">`list`: *Record list*</span></span>

<span data-ttu-id="37090-109">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="37090-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="37090-110">`field`: *Поле*</span><span class="sxs-lookup"><span data-stu-id="37090-110">`field`: *Field*</span></span>

<span data-ttu-id="37090-111">Действительный путь поля типа данных *Строка* в указанном списке.</span><span class="sxs-lookup"><span data-stu-id="37090-111">The valid path of a field of the *String* data type in the specified list.</span></span>

<span data-ttu-id="37090-112">`delimiter`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="37090-112">`delimiter`: *String*</span></span>

<span data-ttu-id="37090-113">Разделитель, который используется для разделения подстрок.</span><span class="sxs-lookup"><span data-stu-id="37090-113">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="37090-114">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="37090-114">Return values</span></span>

<span data-ttu-id="37090-115">*Строка*</span><span class="sxs-lookup"><span data-stu-id="37090-115">*String*</span></span>

<span data-ttu-id="37090-116">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="37090-116">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="37090-117">Пример</span><span class="sxs-lookup"><span data-stu-id="37090-117">Example</span></span>

<span data-ttu-id="37090-118">Если вы вводите `SPLIT("abc" , 1)` в качестве источника данных **DS**, выражение `STRINGJOIN (DS, DS.Value, "-")` возвращает **"a-b-c"**.</span><span class="sxs-lookup"><span data-stu-id="37090-118">If you enter `SPLIT("abc" , 1)` as data source **DS**, the expression `STRINGJOIN (DS, DS.Value, "-")` returns **"a-b-c"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="37090-119">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="37090-119">Additional resources</span></span>

[<span data-ttu-id="37090-120">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="37090-120">List functions</span></span>](er-functions-category-list.md)
