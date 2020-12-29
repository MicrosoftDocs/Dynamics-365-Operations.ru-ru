---
title: Функция ER FILTER
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности FILTER.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 55fa3d4ad4427e2a45f7c5fce679c50a91c40b6d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679446"
---
# <a name="filter-er-function"></a><span data-ttu-id="80d46-103">Функция ER FILTER</span><span class="sxs-lookup"><span data-stu-id="80d46-103">FILTER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="80d46-104">Функция `FILTER` возвращает указанный список в качестве значения *Список записей* после изменения запроса, чтобы он фильтровал для указанного состояния.</span><span class="sxs-lookup"><span data-stu-id="80d46-104">The `FILTER` function returns the specified list as a *Record list* value after the query has been changed so that it filters for the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="80d46-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80d46-105">Syntax</span></span>

```vb
FILTER (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="80d46-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="80d46-106">Arguments</span></span>

<span data-ttu-id="80d46-107">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="80d46-107">`list`: *Record list*</span></span>

<span data-ttu-id="80d46-108">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="80d46-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="80d46-109">`condition`: *Логический*</span><span class="sxs-lookup"><span data-stu-id="80d46-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="80d46-110">Действительное условное выражение, используемое для фильтрации записей указанного списка.</span><span class="sxs-lookup"><span data-stu-id="80d46-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="80d46-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="80d46-111">Return values</span></span>

<span data-ttu-id="80d46-112">*Список записей*</span><span class="sxs-lookup"><span data-stu-id="80d46-112">*Record list*</span></span>

<span data-ttu-id="80d46-113">Полученный список записей.</span><span class="sxs-lookup"><span data-stu-id="80d46-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="80d46-114">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="80d46-114">Usage notes</span></span>

<span data-ttu-id="80d46-115">Эта функция отличается от функции [WHERE](er-functions-list-where.md), так как указанное условие применяется на уровне базы данных к любому источнику данных электронной отчетности (ER) с типом *Записи таблицы*.</span><span class="sxs-lookup"><span data-stu-id="80d46-115">This function differs from the [WHERE](er-functions-list-where.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Table records* type at the database level.</span></span> <span data-ttu-id="80d46-116">Список и условие могут определяться с помощью таблиц и связей.</span><span class="sxs-lookup"><span data-stu-id="80d46-116">The list and condition can be defined by using tables and relations.</span></span>

<span data-ttu-id="80d46-117">Если один или оба аргумента, настроенные для этой функции (`list` и `condition`) не позволяют перевести этот запрос на прямой вызов SQL, во время разработке будет выдано исключение.</span><span class="sxs-lookup"><span data-stu-id="80d46-117">If one or both arguments that are configured for this function (`list` and `condition`) don't allow this request to be translated to the direct SQL call, an exception is thrown at design time.</span></span> <span data-ttu-id="80d46-118">Это исключение информирует пользователя о том, что `list` или `condition` невозможно использовать для запроса базы данных.</span><span class="sxs-lookup"><span data-stu-id="80d46-118">This exception informs the user that either `list` or `condition` can't be used to query the database.</span></span>

## <a name="example-1"></a><span data-ttu-id="80d46-119">Пример 1</span><span class="sxs-lookup"><span data-stu-id="80d46-119">Example 1</span></span>

<span data-ttu-id="80d46-120">Если **Поставщик** настраивается в качестве источника данных ER, который ссылается на таблицу VendTable, выражение `FILTER (Vendors, Vendors.VendGroup = "40")` возвращает список только поставщиков, которые относятся к группе поставщиков 40.</span><span class="sxs-lookup"><span data-stu-id="80d46-120">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `FILTER (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="80d46-121">Пример 2</span><span class="sxs-lookup"><span data-stu-id="80d46-121">Example 2</span></span>

<span data-ttu-id="80d46-122">Если **Поставщик** настроен в качестве источника данных ER, который ссылается на таблицу VendTable и если **parmVendorBankGroup** настроен как источник данных ER, который возвращает значение *строкового* типа данных, выражение `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` возвращает список только счетов поставщиков, входящих в конкретную банковскую группу.</span><span class="sxs-lookup"><span data-stu-id="80d46-122">If **Vendor** is configured as an ER data source that refers to the VendTable table, and if **parmVendorBankGroup** is configured as an ER data source that returns a value of the *String* data type, the expression `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` returns a list of only vendor accounts that belong to a specific bank group.</span></span>

## <a name="example-3"></a><span data-ttu-id="80d46-123">Пример 3</span><span class="sxs-lookup"><span data-stu-id="80d46-123">Example 3</span></span>

<span data-ttu-id="80d46-124">Вы вводите источник данных **DS** типа *Вычисляемое поле*, и он содержит выражение `SPLIT ("A,B,C", ",")`.</span><span class="sxs-lookup"><span data-stu-id="80d46-124">You enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A,B,C", ",")`.</span></span> <span data-ttu-id="80d46-125">Затем вы вводите другое выражение, `FILTER( DS, DS.Value = "B")`.</span><span class="sxs-lookup"><span data-stu-id="80d46-125">You then enter another expression, `FILTER( DS, DS.Value = "B")`.</span></span> <span data-ttu-id="80d46-126">При попытке сохранить это выражение в конструкторе формул ER выдается следующее исключение: «Ошибка проверки: выражение списка функции FILTER не может быть запрошено».</span><span class="sxs-lookup"><span data-stu-id="80d46-126">When you try to save this expression in the ER formula designer, the following exception is thrown: "Validation error: The list expression of FILTER function is not queryable."</span></span>

## <a name="additional-resources"></a><span data-ttu-id="80d46-127">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="80d46-127">Additional resources</span></span>

[<span data-ttu-id="80d46-128">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="80d46-128">List functions</span></span>](er-functions-category-list.md)
