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
ms.openlocfilehash: 392cf7acebd7ad95bcc0f5d4b7a67500a412a795
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041845"
---
# <span data-ttu-id="d6306-103"><a name="WHERE">Функция ER WHERE</a></span><span class="sxs-lookup"><span data-stu-id="d6306-103"><a name="WHERE">WHERE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d6306-104">Функция `WHERE` возвращает указанный список в качестве значения *Список записей* после того, как он был отфильтрован в соответствии с указанным условием.</span><span class="sxs-lookup"><span data-stu-id="d6306-104">The `WHERE` function returns the specified list as a *Record list* value after it has been filtered according to the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6306-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d6306-105">Syntax</span></span>

```vb
WHERE (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="d6306-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="d6306-106">Arguments</span></span>

<span data-ttu-id="d6306-107">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="d6306-107">`list`: *Record list*</span></span>

<span data-ttu-id="d6306-108">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="d6306-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="d6306-109">`condition`: *Логический*</span><span class="sxs-lookup"><span data-stu-id="d6306-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="d6306-110">Действительное условное выражение, используемое для фильтрации записей указанного списка.</span><span class="sxs-lookup"><span data-stu-id="d6306-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="d6306-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="d6306-111">Return values</span></span>

<span data-ttu-id="d6306-112">*Список записей*</span><span class="sxs-lookup"><span data-stu-id="d6306-112">*Record list*</span></span>

<span data-ttu-id="d6306-113">Полученный список записей.</span><span class="sxs-lookup"><span data-stu-id="d6306-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d6306-114">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="d6306-114">Usage notes</span></span>

<span data-ttu-id="d6306-115">Эта функция отличается от функции [FILTER](er-functions-list-filter.md), так как указанное условие применяется на уровне базы данных к любому источнику данных электронной отчетности (ER) с типом *Список записей*, присутствующему в памяти.</span><span class="sxs-lookup"><span data-stu-id="d6306-115">This function differs from the [FILTER](er-functions-list-filter.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="d6306-116">Если аргументы, настроенные для этой функции (`list` и `condition`) позволяют перевести этот запрос на прямой вызов SQL, во время разработки будет выдано предупреждающее сообщение.</span><span class="sxs-lookup"><span data-stu-id="d6306-116">If the arguments that are configured for this function (`list` and `condition`) allow this request to be translated to the direct SQL call, a warning message is thrown at design time.</span></span> <span data-ttu-id="d6306-117">Это сообщение информирует пользователя о том, что производительность может быть улучшена, если функцию [FILTER](er-functions-list-filter.md) использовать вместо `WHERE`.</span><span class="sxs-lookup"><span data-stu-id="d6306-117">This message informs the user that performance might be improved if the [FILTER](er-functions-list-filter.md) function is used instead of `WHERE`.</span></span>

## <a name="example-1"></a><span data-ttu-id="d6306-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d6306-118">Example 1</span></span>

<span data-ttu-id="d6306-119">Если **Поставщик** настраивается в качестве источника данных ER, который ссылается на таблицу VendTable, выражение `WHERE (Vendors, Vendors.VendGroup = "40")` возвращает список только поставщиков, которые относятся к группе поставщиков 40.</span><span class="sxs-lookup"><span data-stu-id="d6306-119">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `WHERE (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="d6306-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d6306-120">Example 2</span></span>

<span data-ttu-id="d6306-121">Если введен источник данных **DS** для типа *Вычисляемое поле* и он содержит выражение `SPLIT ("A|B|C", "|")`, выражение `WHERE( DS, DS.Value = "B")` возвращает список только одной записи, содержащей текст **"B"** в поле **Значение**.</span><span class="sxs-lookup"><span data-stu-id="d6306-121">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `WHERE( DS, DS.Value = "B")` returns a list of only one record that contains the text **"B"** in the **Value** field.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d6306-122">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d6306-122">Additional resources</span></span>

[<span data-ttu-id="d6306-123">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="d6306-123">List functions</span></span>](er-functions-category-list.md)
