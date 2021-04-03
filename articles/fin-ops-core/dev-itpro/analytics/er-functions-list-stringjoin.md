---
title: Функция ER STRINGJOIN
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности STRINGJOIN.
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
ms.openlocfilehash: 755e6481abb65dfecc8ddb6bceb032c8110095e2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568178"
---
# <a name="stringjoin-er-function"></a><span data-ttu-id="a3cf8-103">Функция ER STRINGJOIN</span><span class="sxs-lookup"><span data-stu-id="a3cf8-103">STRINGJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3cf8-104">Функция `STRINGJOIN` возвращает значение *строка*, состоящее из связанных значений указанного поля из указанного списка.</span><span class="sxs-lookup"><span data-stu-id="a3cf8-104">The `STRINGJOIN` function returns a *String* value that consists of concatenated values of the specified field from the specified list.</span></span> <span data-ttu-id="a3cf8-105">Значения могут разделяться указанным разделителем.</span><span class="sxs-lookup"><span data-stu-id="a3cf8-105">The values can be separated by the specified delimiter.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3cf8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3cf8-106">Syntax</span></span>

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a><span data-ttu-id="a3cf8-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="a3cf8-107">Arguments</span></span>

<span data-ttu-id="a3cf8-108">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="a3cf8-108">`list`: *Record list*</span></span>

<span data-ttu-id="a3cf8-109">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="a3cf8-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="a3cf8-110">`field`: *Поле*</span><span class="sxs-lookup"><span data-stu-id="a3cf8-110">`field`: *Field*</span></span>

<span data-ttu-id="a3cf8-111">Действительный путь поля типа данных *Строка* в указанном списке.</span><span class="sxs-lookup"><span data-stu-id="a3cf8-111">The valid path of a field of the *String* data type in the specified list.</span></span>

<span data-ttu-id="a3cf8-112">`delimiter`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="a3cf8-112">`delimiter`: *String*</span></span>

<span data-ttu-id="a3cf8-113">Разделитель, который используется для разделения подстрок.</span><span class="sxs-lookup"><span data-stu-id="a3cf8-113">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="a3cf8-114">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="a3cf8-114">Return values</span></span>

<span data-ttu-id="a3cf8-115">*Строка*</span><span class="sxs-lookup"><span data-stu-id="a3cf8-115">*String*</span></span>

<span data-ttu-id="a3cf8-116">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="a3cf8-116">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="a3cf8-117">Пример</span><span class="sxs-lookup"><span data-stu-id="a3cf8-117">Example</span></span>

<span data-ttu-id="a3cf8-118">Если вы вводите `SPLIT("abc" , 1)` в качестве источника данных **DS**, выражение `STRINGJOIN (DS, DS.Value, "-")` возвращает **"a-b-c"**.</span><span class="sxs-lookup"><span data-stu-id="a3cf8-118">If you enter `SPLIT("abc" , 1)` as data source **DS**, the expression `STRINGJOIN (DS, DS.Value, "-")` returns **"a-b-c"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a3cf8-119">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a3cf8-119">Additional resources</span></span>

[<span data-ttu-id="a3cf8-120">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="a3cf8-120">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]