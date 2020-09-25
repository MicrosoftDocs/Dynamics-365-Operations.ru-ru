---
title: Функция ER INDEX
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности INDEX.
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
ms.openlocfilehash: 051e22daa3fe2d6c328e36403201d940f724bd29
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745188"
---
# <a name="index-er-function"></a><span data-ttu-id="f5f76-103">Функция ER INDEX</span><span class="sxs-lookup"><span data-stu-id="f5f76-103">INDEX ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5f76-104">Функция `INDEX` возвращает значение *Контейнер (запись)*, выбранное с помощью указанного числового индекса в указанном списке.</span><span class="sxs-lookup"><span data-stu-id="f5f76-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="f5f76-105">Если индекс выходит за пределы диапазона записей в указанном списке, выдается исключение.</span><span class="sxs-lookup"><span data-stu-id="f5f76-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5f76-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5f76-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="f5f76-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="f5f76-107">Arguments</span></span>

<span data-ttu-id="f5f76-108">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="f5f76-108">`list`: *Record list*</span></span>

<span data-ttu-id="f5f76-109">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="f5f76-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="f5f76-110">`index`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="f5f76-110">`index`: *Integer*</span></span>

<span data-ttu-id="f5f76-111">Числовой индекс, указывающий положение желаемой записи в указанном списке.</span><span class="sxs-lookup"><span data-stu-id="f5f76-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="f5f76-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="f5f76-112">Return values</span></span>

<span data-ttu-id="f5f76-113">*Контейнер (запись)*</span><span class="sxs-lookup"><span data-stu-id="f5f76-113">*Container (record)*</span></span>

<span data-ttu-id="f5f76-114">Результирующее значение записи.</span><span class="sxs-lookup"><span data-stu-id="f5f76-114">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="f5f76-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f5f76-115">Example 1</span></span>

<span data-ttu-id="f5f76-116">Если введен источник данных **DS** для типа *Вычисляемое поле* и он содержит выражение `SPLIT ("A|B|C", "|")`, выражение `DS.Value` возвращает текстовое значение **"B"** для второй записи этого списка записей.</span><span class="sxs-lookup"><span data-stu-id="f5f76-116">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="f5f76-117">Выражение `INDEX (SPLIT ("A|B|C", "|"), 2).Value` также возвращает значение текста **"B"**.</span><span class="sxs-lookup"><span data-stu-id="f5f76-117">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="f5f76-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f5f76-118">Example 2</span></span>

<span data-ttu-id="f5f76-119">Если вы введете источник данных **DS** типа *Вычисляемое поле* и он содержит выражение `SPLIT ("A|B|C", "|")`, выражение `INDEX (SPLIT ("A|B|C", "|"), 4).Value` выдает исключение во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="f5f76-119">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f5f76-120">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f5f76-120">Additional resources</span></span>

[<span data-ttu-id="f5f76-121">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="f5f76-121">List functions</span></span>](er-functions-category-list.md)
