---
title: Функция ER LIST
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности LIST
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
ms.openlocfilehash: c7f8e701ec2836206d2299abba5e5b8542b4cf92
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683095"
---
# <a name="list-er-function"></a><span data-ttu-id="26f6d-103">Функция ER LIST</span><span class="sxs-lookup"><span data-stu-id="26f6d-103">LIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26f6d-104">Функция `LIST` возвращает значение *Список записей*, состоящее из нового списка записей, созданного из указанных аргументов.</span><span class="sxs-lookup"><span data-stu-id="26f6d-104">The `LIST` function returns a *Record list* value that consists of a new list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="26f6d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26f6d-105">Syntax</span></span>

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a><span data-ttu-id="26f6d-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="26f6d-106">Arguments</span></span>

<span data-ttu-id="26f6d-107">`record 1`: *Контейнер (запись)*</span><span class="sxs-lookup"><span data-stu-id="26f6d-107">`record 1`: *Container (record)*</span></span>

<span data-ttu-id="26f6d-108">Ссылка на источник данных типа данных *Запись*.</span><span class="sxs-lookup"><span data-stu-id="26f6d-108">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="26f6d-109">Этот аргумент обязательный.</span><span class="sxs-lookup"><span data-stu-id="26f6d-109">This argument is required.</span></span>

<span data-ttu-id="26f6d-110">`record N`: *Контейнер (запись)*</span><span class="sxs-lookup"><span data-stu-id="26f6d-110">`record N`: *Container (record)*</span></span>

<span data-ttu-id="26f6d-111">Ссылка на источник данных типа данных *Запись*.</span><span class="sxs-lookup"><span data-stu-id="26f6d-111">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="26f6d-112">Эти дополнительные аргументы являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="26f6d-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="26f6d-113">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="26f6d-113">Return values</span></span>

<span data-ttu-id="26f6d-114">*Список записей*</span><span class="sxs-lookup"><span data-stu-id="26f6d-114">*Record list*</span></span>

<span data-ttu-id="26f6d-115">Полученный список записей.</span><span class="sxs-lookup"><span data-stu-id="26f6d-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="26f6d-116">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="26f6d-116">Usage notes</span></span>

<span data-ttu-id="26f6d-117">Структура создаваемого списка содержит только поля, представленные в структуре каждой записи, упомянутой в аргументах.</span><span class="sxs-lookup"><span data-stu-id="26f6d-117">The structure of the list that is created contains only the fields that are presented in the structure of every record that is mentioned in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="26f6d-118">Пример</span><span class="sxs-lookup"><span data-stu-id="26f6d-118">Example</span></span>

<span data-ttu-id="26f6d-119">Вы вводите источник данных **Запись 1** типа *Контейнер*.</span><span class="sxs-lookup"><span data-stu-id="26f6d-119">You enter data source **Record 1** of the *Container* type.</span></span> <span data-ttu-id="26f6d-120">Этот источник данных содержит следующие вложенные поля типа *Вычисляемое поле*:</span><span class="sxs-lookup"><span data-stu-id="26f6d-120">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="26f6d-121">**Код**: это поле содержит выражение, возвращающее значение типа *Строка*.</span><span class="sxs-lookup"><span data-stu-id="26f6d-121">**Code:** This field contains an expression that returns a value of the *String* type.</span></span>
- <span data-ttu-id="26f6d-122">**Сумма**: это поле содержит выражение, возвращающее значение типа *вещественное*.</span><span class="sxs-lookup"><span data-stu-id="26f6d-122">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>

<span data-ttu-id="26f6d-123">Затем вы вводите источник данных **Запись 2** типа *Контейнер*.</span><span class="sxs-lookup"><span data-stu-id="26f6d-123">You then enter data source **Record 2** of the *Container* type.</span></span> <span data-ttu-id="26f6d-124">Этот источник данных содержит следующие вложенные поля типа *Вычисляемое поле*:</span><span class="sxs-lookup"><span data-stu-id="26f6d-124">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="26f6d-125">**Сумма**: это поле содержит выражение, возвращающее значение типа *вещественное*.</span><span class="sxs-lookup"><span data-stu-id="26f6d-125">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>
- <span data-ttu-id="26f6d-126">**IsValid**: это поле содержит выражение, возвращающее значение типа *логическое*.</span><span class="sxs-lookup"><span data-stu-id="26f6d-126">**IsValid:** This field contains an expression that returns a value of the *Boolean* type.</span></span>

<span data-ttu-id="26f6d-127">В этом случае выражение `LIST('Record 1', 'Record 2')` возвращает новый список, содержащий две записи.</span><span class="sxs-lookup"><span data-stu-id="26f6d-127">In this case, the expression `LIST('Record 1', 'Record 2')` returns a new list that contains two records.</span></span> <span data-ttu-id="26f6d-128">Структура этого списка состоит из единого поля **Сумма** типа *Вещественное*, потому что это поле является единственным полем, которое представлено в каждом аргументе вызываемой функции.</span><span class="sxs-lookup"><span data-stu-id="26f6d-128">The structure of this list consists of a single **Amount** field of the *Real* type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="26f6d-129">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="26f6d-129">Additional resources</span></span>

[<span data-ttu-id="26f6d-130">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="26f6d-130">List functions</span></span>](er-functions-category-list.md)
