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
ms.openlocfilehash: 45e95751e3adfe6aa208daaba774a349216e1f1f
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042075"
---
# <span data-ttu-id="6111d-103"><a name="INDEX">Функция ER INDEX</a></span><span class="sxs-lookup"><span data-stu-id="6111d-103"><a name="INDEX">INDEX ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6111d-104">Функция `INDEX` возвращает значение *Контейнер (запись)*, выбранное с помощью указанного числового индекса в указанном списке.</span><span class="sxs-lookup"><span data-stu-id="6111d-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="6111d-105">Если индекс выходит за пределы диапазона записей в указанном списке, выдается исключение.</span><span class="sxs-lookup"><span data-stu-id="6111d-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="6111d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6111d-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="6111d-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="6111d-107">Arguments</span></span>

<span data-ttu-id="6111d-108">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="6111d-108">`list`: *Record list*</span></span>

<span data-ttu-id="6111d-109">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="6111d-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="6111d-110">`index`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="6111d-110">`index`: *Integer*</span></span>

<span data-ttu-id="6111d-111">Числовой индекс, указывающий положение желаемой записи в указанном списке.</span><span class="sxs-lookup"><span data-stu-id="6111d-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="6111d-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="6111d-112">Return values</span></span>

<span data-ttu-id="6111d-113">*Контейнер (запись)*</span><span class="sxs-lookup"><span data-stu-id="6111d-113">*Container (record)*</span></span>

<span data-ttu-id="6111d-114">Результирующее значение записи.</span><span class="sxs-lookup"><span data-stu-id="6111d-114">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="6111d-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6111d-115">Example 1</span></span>

<span data-ttu-id="6111d-116">Если введен источник данных **DS** для типа *Вычисляемое поле* и он содержит выражение `SPLIT ("A|B|C", "|")`, выражение `DS.Value` возвращает текстовое значение **"B"** для второй записи этого списка записей.</span><span class="sxs-lookup"><span data-stu-id="6111d-116">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="6111d-117">Выражение `INDEX (SPLIT ("A|B|C", "|"), 2).Value` также возвращает значение текста **"B"**.</span><span class="sxs-lookup"><span data-stu-id="6111d-117">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="6111d-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6111d-118">Example 2</span></span>

<span data-ttu-id="6111d-119">Если вы введете источник данных **DS** типа *Вычисляемое поле* и он содержит выражение `SPLIT ("A|B|C", "|")`, выражение `INDEX (SPLIT ("A|B|C", "|"), 4).Value` выдает исключение во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="6111d-119">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6111d-120">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6111d-120">Additional resources</span></span>

[<span data-ttu-id="6111d-121">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="6111d-121">List functions</span></span>](er-functions-category-list.md)
