---
title: Функция ER FILTER
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности FILTER.
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
ms.openlocfilehash: aa8c0b4601db625d442dd545151968f38bd58cf1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746611"
---
# <a name="filter-er-function"></a><span data-ttu-id="a79de-103">Функция ER FILTER</span><span class="sxs-lookup"><span data-stu-id="a79de-103">FILTER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a79de-104">Функция `FILTER` возвращает указанный список в качестве значения *Список записей* после изменения запроса, чтобы он фильтровал для указанного состояния.</span><span class="sxs-lookup"><span data-stu-id="a79de-104">The `FILTER` function returns the specified list as a *Record list* value after the query has been changed so that it filters for the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="a79de-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a79de-105">Syntax</span></span>

```vb
FILTER (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="a79de-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="a79de-106">Arguments</span></span>

<span data-ttu-id="a79de-107">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="a79de-107">`list`: *Record list*</span></span>

<span data-ttu-id="a79de-108">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="a79de-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="a79de-109">`condition`: *Логический*</span><span class="sxs-lookup"><span data-stu-id="a79de-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="a79de-110">Действительное условное выражение, используемое для фильтрации записей указанного списка.</span><span class="sxs-lookup"><span data-stu-id="a79de-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="a79de-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="a79de-111">Return values</span></span>

<span data-ttu-id="a79de-112">*Список записей*</span><span class="sxs-lookup"><span data-stu-id="a79de-112">*Record list*</span></span>

<span data-ttu-id="a79de-113">Полученный список записей.</span><span class="sxs-lookup"><span data-stu-id="a79de-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a79de-114">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="a79de-114">Usage notes</span></span>

<span data-ttu-id="a79de-115">Эта функция отличается от функции [WHERE](er-functions-list-where.md), так как указанное условие применяется на уровне базы данных к любому источнику данных электронной отчетности (ER) с типом *Записи таблицы*.</span><span class="sxs-lookup"><span data-stu-id="a79de-115">This function differs from the [WHERE](er-functions-list-where.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Table records* type at the database level.</span></span> <span data-ttu-id="a79de-116">Список и условие могут определяться с помощью таблиц и связей.</span><span class="sxs-lookup"><span data-stu-id="a79de-116">The list and condition can be defined by using tables and relations.</span></span>

<span data-ttu-id="a79de-117">Если один или оба аргумента, настроенные для этой функции (`list` и `condition`) не позволяют перевести этот запрос на прямой вызов SQL, во время разработке будет выдано исключение.</span><span class="sxs-lookup"><span data-stu-id="a79de-117">If one or both arguments that are configured for this function (`list` and `condition`) don't allow this request to be translated to the direct SQL call, an exception is thrown at design time.</span></span> <span data-ttu-id="a79de-118">Это исключение информирует пользователя о том, что `list` или `condition` невозможно использовать для запроса базы данных.</span><span class="sxs-lookup"><span data-stu-id="a79de-118">This exception informs the user that either `list` or `condition` can't be used to query the database.</span></span>

## <a name="example-1"></a><span data-ttu-id="a79de-119">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a79de-119">Example 1</span></span>

<span data-ttu-id="a79de-120">Если **Поставщик** настраивается в качестве источника данных ER, который ссылается на таблицу VendTable, выражение `FILTER (Vendors, Vendors.VendGroup = "40")` возвращает список только поставщиков, которые относятся к группе поставщиков 40.</span><span class="sxs-lookup"><span data-stu-id="a79de-120">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `FILTER (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="a79de-121">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a79de-121">Example 2</span></span>

<span data-ttu-id="a79de-122">Если **Поставщик** настроен в качестве источника данных ER, который ссылается на таблицу VendTable и если **parmVendorBankGroup** настроен как источник данных ER, который возвращает значение *строкового* типа данных, выражение `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` возвращает список только счетов поставщиков, входящих в конкретную банковскую группу.</span><span class="sxs-lookup"><span data-stu-id="a79de-122">If **Vendor** is configured as an ER data source that refers to the VendTable table, and if **parmVendorBankGroup** is configured as an ER data source that returns a value of the *String* data type, the expression `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` returns a list of only vendor accounts that belong to a specific bank group.</span></span>

## <a name="example-3"></a><span data-ttu-id="a79de-123">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a79de-123">Example 3</span></span>

<span data-ttu-id="a79de-124">Вы вводите источник данных **DS** типа *Вычисляемое поле*, и он содержит выражение `SPLIT ("A,B,C", ",")`.</span><span class="sxs-lookup"><span data-stu-id="a79de-124">You enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A,B,C", ",")`.</span></span> <span data-ttu-id="a79de-125">Затем вы вводите другое выражение, `FILTER( DS, DS.Value = "B")`.</span><span class="sxs-lookup"><span data-stu-id="a79de-125">You then enter another expression, `FILTER( DS, DS.Value = "B")`.</span></span> <span data-ttu-id="a79de-126">При попытке сохранить это выражение в конструкторе формул ER выдается следующее исключение: «Ошибка проверки: выражение списка функции FILTER не может быть запрошено».</span><span class="sxs-lookup"><span data-stu-id="a79de-126">When you try to save this expression in the ER formula designer, the following exception is thrown: "Validation error: The list expression of FILTER function is not queryable."</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a79de-127">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a79de-127">Additional resources</span></span>

[<span data-ttu-id="a79de-128">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="a79de-128">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]