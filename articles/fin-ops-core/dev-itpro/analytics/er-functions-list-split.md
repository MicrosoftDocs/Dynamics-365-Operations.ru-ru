---
title: Функция ER SPLIT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности SPLIT.
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
ms.openlocfilehash: 31caf7c728a92d31428f47320c074fa9fc35bda6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916116"
---
# <span data-ttu-id="6eebd-103"><a name="SPLIT">Функция ER SPLIT</a></span><span class="sxs-lookup"><span data-stu-id="6eebd-103"><a name="SPLIT">SPLIT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6eebd-104">Функция `SPLIT` разделяет указанную строку ввода на подстроки и возвращает результат в виде нового значения *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="6eebd-104">The `SPLIT` function splits the specified input string into substrings and returns the result as a new *Record list* value.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="6eebd-105">Синтаксис 1</span><span class="sxs-lookup"><span data-stu-id="6eebd-105">Syntax 1</span></span>

```
SPLIT (input, length)
```

<span data-ttu-id="6eebd-106">Этот синтаксис используется для разделения указанной строки ввода на подстроки, каждая из которых имеет заданную длину.</span><span class="sxs-lookup"><span data-stu-id="6eebd-106">This syntax is used to split the specified input string into substrings, each of which has the specified length.</span></span>

## <a name="syntax-2"></a><span data-ttu-id="6eebd-107">Синтаксис 2</span><span class="sxs-lookup"><span data-stu-id="6eebd-107">Syntax 2</span></span>

```
SPLIT (input, delimiter)
```

<span data-ttu-id="6eebd-108">Этот синтаксис используется для разделения указанной строки ввода на подстроки на основе указанного разделителя.</span><span class="sxs-lookup"><span data-stu-id="6eebd-108">This syntax is used to split the specified input string into substrings, based on the specified delimiter.</span></span>

## <a name="arguments"></a><span data-ttu-id="6eebd-109">Аргументы</span><span class="sxs-lookup"><span data-stu-id="6eebd-109">Arguments</span></span>

<span data-ttu-id="6eebd-110">`input`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="6eebd-110">`input`: *String*</span></span>

<span data-ttu-id="6eebd-111">Текст для разделения.</span><span class="sxs-lookup"><span data-stu-id="6eebd-111">The text to split.</span></span>

<span data-ttu-id="6eebd-112">`length`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="6eebd-112">`length`: *Integer*</span></span>

<span data-ttu-id="6eebd-113">Максимальная длина одной подстроки.</span><span class="sxs-lookup"><span data-stu-id="6eebd-113">The maximum length of a single substring.</span></span>

<span data-ttu-id="6eebd-114">`delimiter`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="6eebd-114">`delimiter`: *String*</span></span>

<span data-ttu-id="6eebd-115">Разделитель, который используется для разделения подстрок.</span><span class="sxs-lookup"><span data-stu-id="6eebd-115">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="6eebd-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="6eebd-116">Return values</span></span>

<span data-ttu-id="6eebd-117">*Список записей*</span><span class="sxs-lookup"><span data-stu-id="6eebd-117">*Record list*</span></span>

<span data-ttu-id="6eebd-118">Полученный список записей.</span><span class="sxs-lookup"><span data-stu-id="6eebd-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6eebd-119">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="6eebd-119">Usage notes</span></span>

<span data-ttu-id="6eebd-120">Структура записи возвращенного списка состоит из поля **Значение** типа *Строка*.</span><span class="sxs-lookup"><span data-stu-id="6eebd-120">The record structure of the list that is returned consists of the **Value** field of the *String* type.</span></span> <span data-ttu-id="6eebd-121">Каждая запись возвращаемого списка содержит созданные подстроки в этом поле.</span><span class="sxs-lookup"><span data-stu-id="6eebd-121">Every record of the list that is returned contains generated substrings in this field.</span></span>

<span data-ttu-id="6eebd-122">Если аргумент `delimiter` пуст, новый возвращаемый список состоит из одной записи с полем **Значение** типа *Строка*.</span><span class="sxs-lookup"><span data-stu-id="6eebd-122">If the `delimiter` argument is empty, the new list that is returned consists of one record that has the **Value** field of the *String* type.</span></span> <span data-ttu-id="6eebd-123">Это поле содержит введенный текст.</span><span class="sxs-lookup"><span data-stu-id="6eebd-123">This field contains the input text.</span></span>

<span data-ttu-id="6eebd-124">Если аргумент `input` пуст, возвращается новый пустой список.</span><span class="sxs-lookup"><span data-stu-id="6eebd-124">If the `input` argument is empty, a new empty list is returned.</span></span> <span data-ttu-id="6eebd-125">Если аргумент `input` или `delimiter` не указан (null), возникает исключение приложения.</span><span class="sxs-lookup"><span data-stu-id="6eebd-125">If either the `input` or `delimiter` argument is unspecified (null), an application exception is thrown.</span></span>

## <a name="example-1"></a><span data-ttu-id="6eebd-126">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6eebd-126">Example 1</span></span>

<span data-ttu-id="6eebd-127">`SPLIT ("abcd", 3)` возвращает новый список, который состоит из двух записей с полем **Значение** типа *Строка*.</span><span class="sxs-lookup"><span data-stu-id="6eebd-127">`SPLIT ("abcd", 3)` returns a new list that consists of two records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="6eebd-128">Поле **Значение** в первой записи содержит текст **"abc"**, и поле **Значение** во второй записи содержит текст **"d"**.</span><span class="sxs-lookup"><span data-stu-id="6eebd-128">The **Value** field in the first record contains the text **"abc"**, and the **Value** field in the second record contains the text **"d"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="6eebd-129">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6eebd-129">Example 2</span></span>

<span data-ttu-id="6eebd-130">`SPLIT ("XAb aBy", "aB")` возвращает новый список, который состоит из трех записей с полем **Значение** типа *Строка*.</span><span class="sxs-lookup"><span data-stu-id="6eebd-130">`SPLIT ("XAb aBy", "aB")` returns a new list that consists of three records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="6eebd-131">Поле **Значение** в первой записи содержит текст **"X"**, поле **Значение** во второй записи содержит текст **"&nbsp;"**, и поле **Значение** в третьей записи содержит текст **"y"**.</span><span class="sxs-lookup"><span data-stu-id="6eebd-131">The **Value** field in the first record contains the text **"X"**, the **Value** field in the second record contains the text **"&nbsp;"**, and the **Value** field in the third record contains the text **"y"**.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="6eebd-132">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6eebd-132">Additional resources</span></span>

[<span data-ttu-id="6eebd-133">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="6eebd-133">List functions</span></span>](er-functions-category-list.md)
