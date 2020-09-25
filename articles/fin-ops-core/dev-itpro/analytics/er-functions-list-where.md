---
title: Функция ER WHERE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности WHERE.
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
ms.openlocfilehash: 94326986791c95eac7b0f5771f779014d865d3bb
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743449"
---
# <a name="where-er-function"></a><span data-ttu-id="0ad60-103">Функция ER WHERE</span><span class="sxs-lookup"><span data-stu-id="0ad60-103">WHERE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ad60-104">Функция `WHERE` возвращает указанный список в качестве значения *Список записей* после того, как он был отфильтрован в соответствии с указанным условием.</span><span class="sxs-lookup"><span data-stu-id="0ad60-104">The `WHERE` function returns the specified list as a *Record list* value after it has been filtered according to the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ad60-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ad60-105">Syntax</span></span>

```vb
WHERE (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="0ad60-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="0ad60-106">Arguments</span></span>

<span data-ttu-id="0ad60-107">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="0ad60-107">`list`: *Record list*</span></span>

<span data-ttu-id="0ad60-108">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="0ad60-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="0ad60-109">`condition`: *Логический*</span><span class="sxs-lookup"><span data-stu-id="0ad60-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="0ad60-110">Действительное условное выражение, используемое для фильтрации записей указанного списка.</span><span class="sxs-lookup"><span data-stu-id="0ad60-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="0ad60-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="0ad60-111">Return values</span></span>

<span data-ttu-id="0ad60-112">*Список записей*</span><span class="sxs-lookup"><span data-stu-id="0ad60-112">*Record list*</span></span>

<span data-ttu-id="0ad60-113">Полученный список записей.</span><span class="sxs-lookup"><span data-stu-id="0ad60-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0ad60-114">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="0ad60-114">Usage notes</span></span>

<span data-ttu-id="0ad60-115">Эта функция отличается от функции [FILTER](er-functions-list-filter.md), так как указанное условие применяется на уровне базы данных к любому источнику данных электронной отчетности (ER) с типом *Список записей*, присутствующему в памяти.</span><span class="sxs-lookup"><span data-stu-id="0ad60-115">This function differs from the [FILTER](er-functions-list-filter.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="0ad60-116">Если аргументы, настроенные для этой функции (`list` и `condition`) позволяют перевести этот запрос на прямой вызов SQL, во время разработки будет выдано предупреждающее сообщение.</span><span class="sxs-lookup"><span data-stu-id="0ad60-116">If the arguments that are configured for this function (`list` and `condition`) allow this request to be translated to the direct SQL call, a warning message is thrown at design time.</span></span> <span data-ttu-id="0ad60-117">Это сообщение информирует пользователя о том, что производительность может быть улучшена, если функцию [FILTER](er-functions-list-filter.md) использовать вместо `WHERE`.</span><span class="sxs-lookup"><span data-stu-id="0ad60-117">This message informs the user that performance might be improved if the [FILTER](er-functions-list-filter.md) function is used instead of `WHERE`.</span></span>

## <a name="example-1"></a><span data-ttu-id="0ad60-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0ad60-118">Example 1</span></span>

<span data-ttu-id="0ad60-119">Если **Поставщик** настраивается в качестве источника данных ER, который ссылается на таблицу VendTable, выражение `WHERE (Vendors, Vendors.VendGroup = "40")` возвращает список только поставщиков, которые относятся к группе поставщиков 40.</span><span class="sxs-lookup"><span data-stu-id="0ad60-119">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `WHERE (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="0ad60-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0ad60-120">Example 2</span></span>

<span data-ttu-id="0ad60-121">Если введен источник данных **DS** для типа *Вычисляемое поле* и он содержит выражение `SPLIT ("A|B|C", "|")`, выражение `WHERE( DS, DS.Value = "B")` возвращает список только одной записи, содержащей текст **"B"** в поле **Значение**.</span><span class="sxs-lookup"><span data-stu-id="0ad60-121">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `WHERE( DS, DS.Value = "B")` returns a list of only one record that contains the text **"B"** in the **Value** field.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0ad60-122">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0ad60-122">Additional resources</span></span>

[<span data-ttu-id="0ad60-123">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="0ad60-123">List functions</span></span>](er-functions-category-list.md)
