---
title: Функция ER ALLITEMS
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности ALLITEMS.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 79c43b6ecdb307433b0c2091840c21a5ada3a689
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917450"
---
# <span data-ttu-id="ea477-103"><a name="ALLITEMS">Функция ER ALLITEMS</a></span><span class="sxs-lookup"><span data-stu-id="ea477-103"><a name="ALLITEMS">ALLITEMS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ea477-104">Функция `ALLITEMS` выполняется как выбор в памяти и возвращает новое выровненное значение *Список записей* в виде списка записей, который представляет все элементы, которые соответствуют указанному пути.</span><span class="sxs-lookup"><span data-stu-id="ea477-104">The `ALLITEMS` function runs as an in-memory selection and returns a new flattened *Record list* value as a list of records that represents all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea477-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ea477-105">Syntax</span></span>

```
ALLITEMS (path)
```

## <a name="arguments"></a><span data-ttu-id="ea477-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="ea477-106">Arguments</span></span>

<span data-ttu-id="ea477-107">`path`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="ea477-107">`path`: *Record list*</span></span>

<span data-ttu-id="ea477-108">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="ea477-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="ea477-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ea477-109">Return values</span></span>

<span data-ttu-id="ea477-110">*Список записей*</span><span class="sxs-lookup"><span data-stu-id="ea477-110">*Record list*</span></span>

<span data-ttu-id="ea477-111">Полученный список записей.</span><span class="sxs-lookup"><span data-stu-id="ea477-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ea477-112">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="ea477-112">Usage notes</span></span>

<span data-ttu-id="ea477-113">Путь должен быть определен как действительный путь источника данных для элемента источника данных с типом данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="ea477-113">The path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="ea477-114">Элементы данных, такие как строка пути и дата, должны вызывать ошибку в построителе выражения электронной отчетности (ER) во время разработки.</span><span class="sxs-lookup"><span data-stu-id="ea477-114">Data elements such as the path string and date should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="ea477-115">Мы не рекомендуем использовать эту функцию для транзакционных источников данных, которые могут содержать большой объем данных.</span><span class="sxs-lookup"><span data-stu-id="ea477-115">We don't recommend that you use this function for transactional data sources that might contain a large volume of data.</span></span> <span data-ttu-id="ea477-116">Вместо этого, лучше использовать функцию [ALLTEMSQUERY](er-functions-list-allitemsquery.md).</span><span class="sxs-lookup"><span data-stu-id="ea477-116">Instead, consider using the [ALLTEMSQUERY](er-functions-list-allitemsquery.md) function.</span></span>

## <a name="example-1"></a><span data-ttu-id="ea477-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ea477-117">Example 1</span></span>

<span data-ttu-id="ea477-118">Если вы вводите `SPLIT("abcdef" , 2)` в качестве источника данных **DS**, выражение `COUNT( ALLITEMS (DS))` возвращает **3**.</span><span class="sxs-lookup"><span data-stu-id="ea477-118">If you enter `SPLIT("abcdef" , 2)` as data source **DS**, the expression `COUNT( ALLITEMS (DS))` returns **3**.</span></span>

## <a name="example-2"></a><span data-ttu-id="ea477-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ea477-119">Example 2</span></span>

<span data-ttu-id="ea477-120">Если вы введете **Vend** в качестве источника данных для типа данных *Список записей*, ссылающегося на таблицу приложений VendTable, выражение `ALLITEMS (Vend.'<Relations'.ContactPerson)` возвращает выровненный список записей со структурой таблицы **ContactPerson** и содержит все контактные лица, к которым можно получить доступ с помощью отношения **ContactPerson.ContactForParty == vendTable.Party**, это доступно для всех поставщиков из таблицы поставщиков по ссылке.</span><span class="sxs-lookup"><span data-stu-id="ea477-120">If you enter **Vend** as the data source of the *Record list* data type that refers to the VendTable application table, the expression `ALLITEMS (Vend.'<Relations'.ContactPerson)` returns a flattened list of records that has the **ContactPerson** table structure and contains all contact persons that can be accessed by using the **ContactPerson.ContactForParty == VendTable.Party** relation, and that is available for all vendors from the referenced vendor table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ea477-121">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ea477-121">Additional resources</span></span>

[<span data-ttu-id="ea477-122">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="ea477-122">List functions</span></span>](er-functions-category-list.md)
