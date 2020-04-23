---
title: Функция STRINGJOIN электронной отчетности
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности LISTJOIN.
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3b5b82917e3083b5ffe4546a6a15fd14938383a
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249043"
---
# <a name=""></a><span data-ttu-id="36b8e-103"><a name="LISTJOIN">Функция STRINGJOIN электронной отчетности</a></span><span class="sxs-lookup"><span data-stu-id="36b8e-103"><a name="LISTJOIN">LISTJOIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36b8e-104">Функция `LISTJOIN` возвращает значение *Список записей*, представляющее новый объединенный список записей, созданный из указанных аргументов.</span><span class="sxs-lookup"><span data-stu-id="36b8e-104">The `LISTJOIN` function returns a *Record list* value that represents a new joined list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="36b8e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36b8e-105">Syntax</span></span>

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a><span data-ttu-id="36b8e-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="36b8e-106">Arguments</span></span>

<span data-ttu-id="36b8e-107">`list 1`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="36b8e-107">`list 1`: *Record list*</span></span>

<span data-ttu-id="36b8e-108">Ссылка на источник данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="36b8e-108">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="36b8e-109">Этот аргумент является обязательным.</span><span class="sxs-lookup"><span data-stu-id="36b8e-109">This argument is mandatory.</span></span>

<span data-ttu-id="36b8e-110">`list N`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="36b8e-110">`list N`: *Record list*</span></span>

<span data-ttu-id="36b8e-111">Ссылка на источник данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="36b8e-111">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="36b8e-112">Эти дополнительные аргументы являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="36b8e-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="36b8e-113">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="36b8e-113">Return values</span></span>

<span data-ttu-id="36b8e-114">*Список записей*</span><span class="sxs-lookup"><span data-stu-id="36b8e-114">*Record list*</span></span>

<span data-ttu-id="36b8e-115">Полученный список записей.</span><span class="sxs-lookup"><span data-stu-id="36b8e-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="36b8e-116">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="36b8e-116">Usage notes</span></span>

<span data-ttu-id="36b8e-117">Структура создаваемого списка содержит только поля, представленные в структуре каждого списка записей, указанных в аргументах.</span><span class="sxs-lookup"><span data-stu-id="36b8e-117">The structure of the list that is created contains only the fields that are present in the structure of every record list that is referenced in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="36b8e-118">Пример</span><span class="sxs-lookup"><span data-stu-id="36b8e-118">Example</span></span>

<span data-ttu-id="36b8e-119">Вы вводите источник данных **Запись 1** типа `Container`.</span><span class="sxs-lookup"><span data-stu-id="36b8e-119">You enter data source **Record 1** of the `Container` type.</span></span> <span data-ttu-id="36b8e-120">Этот источник данных содержит следующие вложенные поля типа `Calculated field`:</span><span class="sxs-lookup"><span data-stu-id="36b8e-120">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="36b8e-121">**Код:** это поле содержит выражение, возвращающее значение типа `String`.</span><span class="sxs-lookup"><span data-stu-id="36b8e-121">**Code**: This field contains an expression that returns a value of the `String` type.</span></span>
- <span data-ttu-id="36b8e-122">**Сумма**: это поле содержит выражение, возвращающее значение типа `Real`.</span><span class="sxs-lookup"><span data-stu-id="36b8e-122">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>

<span data-ttu-id="36b8e-123">Вы затем вводите источник данных **Запись 2** типа `Container`.</span><span class="sxs-lookup"><span data-stu-id="36b8e-123">You then enter data source **Record 2** of the `Container` type.</span></span> <span data-ttu-id="36b8e-124">Этот источник данных содержит следующие вложенные поля типа `Calculated field`:</span><span class="sxs-lookup"><span data-stu-id="36b8e-124">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="36b8e-125">**Сумма**: это поле содержит выражение, возвращающее значение типа `Real`.</span><span class="sxs-lookup"><span data-stu-id="36b8e-125">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>
- <span data-ttu-id="36b8e-126">**IsValid**: это поле содержит выражение, возвращающее значение типа `Boolean`.</span><span class="sxs-lookup"><span data-stu-id="36b8e-126">**IsValid**: This field contains an expression that returns a value of the `Boolean` type.</span></span>

<span data-ttu-id="36b8e-127">В этом случае выражение `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` возвращает новый список, содержащий две записи.</span><span class="sxs-lookup"><span data-stu-id="36b8e-127">In this case, the expression `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` returns a new list that contains two records.</span></span> <span data-ttu-id="36b8e-128">Структура этого списка состоит из одного поля **Сумма** типа `Real`, потому что это поле является единственным полем, которое представлено в каждом аргументе вызываемой функции.</span><span class="sxs-lookup"><span data-stu-id="36b8e-128">The structure of this list consists of a single **Amount** field of the `Real` type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="36b8e-129">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="36b8e-129">Additional resources</span></span>

[<span data-ttu-id="36b8e-130">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="36b8e-130">List functions</span></span>](er-functions-category-list.md)
