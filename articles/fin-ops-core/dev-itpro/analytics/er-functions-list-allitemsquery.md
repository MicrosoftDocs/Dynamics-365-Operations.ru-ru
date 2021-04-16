---
title: Функция ER ALLITEMSQUERY
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ALLITEMSQUERY.
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
ms.openlocfilehash: 7995b497a2bd95d4aec9ae6d5f1c3cb790823ea0
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746707"
---
# <a name="allitemsquery-er-function"></a><span data-ttu-id="990cf-103">Функция ER ALLITEMSQUERY</span><span class="sxs-lookup"><span data-stu-id="990cf-103">ALLITEMSQUERY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="990cf-104">Функция `ALLITEMSQUERY` работает как объединенный SQL-запрос.</span><span class="sxs-lookup"><span data-stu-id="990cf-104">The `ALLITEMSQUERY` function runs as a joined SQL query.</span></span> <span data-ttu-id="990cf-105">Возвращает новое выровненное значение *Список записей*, состоящее из списка записей, представляющих все элементы, которые соответствуют указанному пути.</span><span class="sxs-lookup"><span data-stu-id="990cf-105">It returns a new flattened *Record list* value that consists of a list of records that represent all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="990cf-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="990cf-106">Syntax</span></span>

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a><span data-ttu-id="990cf-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="990cf-107">Arguments</span></span>

<span data-ttu-id="990cf-108">`path`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="990cf-108">`path`: *Record list*</span></span>

<span data-ttu-id="990cf-109">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="990cf-109">The valid path of a data source of the *Record list* data type.</span></span> <span data-ttu-id="990cf-110">Должен содержать по крайней мере одно отношение.</span><span class="sxs-lookup"><span data-stu-id="990cf-110">It must contain at least one relation.</span></span>

## <a name="return-values"></a><span data-ttu-id="990cf-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="990cf-111">Return values</span></span>

<span data-ttu-id="990cf-112">*Список записей*</span><span class="sxs-lookup"><span data-stu-id="990cf-112">*Record list*</span></span>

<span data-ttu-id="990cf-113">Полученный список записей.</span><span class="sxs-lookup"><span data-stu-id="990cf-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="990cf-114">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="990cf-114">Usage notes</span></span>

<span data-ttu-id="990cf-115">Указанный путь должен быть определен как действительный путь источника данных для элемента источника данных с типом данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="990cf-115">The specified path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="990cf-116">Должен также содержать по крайней мере одно отношение.</span><span class="sxs-lookup"><span data-stu-id="990cf-116">It must also contain at least one relation.</span></span> <span data-ttu-id="990cf-117">Элементы данных, такие как *строка* и *дата* пути, должны вызывать ошибку в построителе выражения электронной отчетности (ER) во время разработки.</span><span class="sxs-lookup"><span data-stu-id="990cf-117">Data elements such as the path *String* and *Date* should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="990cf-118">Когда эта функция применяется к источникам данных для типа данных *Список записей*, которые относятся к объекту приложения, который может быть непосредственно вызван с помощью SQL (например, таблица, объект или запрос), она выполняется как объединенный SQL-запрос.</span><span class="sxs-lookup"><span data-stu-id="990cf-118">When this function is applied to data sources of the *Record list* data type that refer to an application object that can be directly called by using SQL (for example, an table, entity, or query), it runs as a joined SQL query.</span></span> <span data-ttu-id="990cf-119">В противном случае она работает в памяти как функция [ALLITEMS](er-functions-list-allitems.md).</span><span class="sxs-lookup"><span data-stu-id="990cf-119">Otherwise, it runs in memory as the [ALLITEMS](er-functions-list-allitems.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="990cf-120">Пример</span><span class="sxs-lookup"><span data-stu-id="990cf-120">Example</span></span>

<span data-ttu-id="990cf-121">Определите следующие источники данных в соответствии вашей модели:</span><span class="sxs-lookup"><span data-stu-id="990cf-121">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="990cf-122">Источник данных **CustInv** типа *Записи таблицы*, который относится к таблице CustInvoiceTable</span><span class="sxs-lookup"><span data-stu-id="990cf-122">A **CustInv** data source of the *Table records* type that refers to the CustInvoiceTable table</span></span>
- <span data-ttu-id="990cf-123">Источник данных **FilteredInv** типа *Вычисляемое поле*, содержащий выражение `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span><span class="sxs-lookup"><span data-stu-id="990cf-123">A **FilteredInv** data source of the *Calculated field* type that contains the expression `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span></span>
- <span data-ttu-id="990cf-124">**JourLines** типа *Вычисляемое поле*, содержащий выражение `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span><span class="sxs-lookup"><span data-stu-id="990cf-124">A **JourLines** of the *Calculated field* type that contains the expression `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span></span>

<span data-ttu-id="990cf-125">При выполнении сопоставления модели для обращения к источнику данных **JourLines**, выполняется следующая инструкция SQL:</span><span class="sxs-lookup"><span data-stu-id="990cf-125">When you run the model mapping to call the **JourLines** data source, the following SQL statement is run:</span></span>

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a><span data-ttu-id="990cf-126">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="990cf-126">Additional resources</span></span>

[<span data-ttu-id="990cf-127">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="990cf-127">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]