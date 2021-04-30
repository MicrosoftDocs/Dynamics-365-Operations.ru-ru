---
title: Функция ER SPLIT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности SPLIT.
author: NickSelin
ms.date: 04/01/2021
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
ms.openlocfilehash: 26b6ddeb2880fc220283b6389327a497549a4511
ms.sourcegitcommit: 74f5b04b482b2ae023c728e0df0eb78305493c6a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "5853451"
---
# <a name="split-er-function"></a><span data-ttu-id="4e301-103">Функция ER SPLIT</span><span class="sxs-lookup"><span data-stu-id="4e301-103">SPLIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e301-104">Функция `SPLIT` разделяет указанную строку ввода на подстроки и возвращает результат в виде нового значения *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="4e301-104">The `SPLIT` function splits the specified input string into substrings and returns the result as a new *Record list* value.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="4e301-105">Синтаксис 1</span><span class="sxs-lookup"><span data-stu-id="4e301-105">Syntax 1</span></span>

```vb
SPLIT (input, length)
```

<span data-ttu-id="4e301-106">Этот синтаксис используется для разделения указанной строки ввода на подстроки, каждая из которых имеет заданную длину.</span><span class="sxs-lookup"><span data-stu-id="4e301-106">This syntax is used to split the specified input string into substrings, each of which has the specified length.</span></span>

## <a name="syntax-2"></a><span data-ttu-id="4e301-107">Синтаксис 2</span><span class="sxs-lookup"><span data-stu-id="4e301-107">Syntax 2</span></span>

```vb
SPLIT (input, delimiter)
```

<span data-ttu-id="4e301-108">Этот синтаксис используется для разделения указанной строки ввода на подстроки на основе указанного разделителя.</span><span class="sxs-lookup"><span data-stu-id="4e301-108">This syntax is used to split the specified input string into substrings, based on the specified delimiter.</span></span>

## <a name="arguments"></a><span data-ttu-id="4e301-109">Аргументы</span><span class="sxs-lookup"><span data-stu-id="4e301-109">Arguments</span></span>

<span data-ttu-id="4e301-110">`input`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="4e301-110">`input`: *String*</span></span>

<span data-ttu-id="4e301-111">Текст для разделения.</span><span class="sxs-lookup"><span data-stu-id="4e301-111">The text to split.</span></span>

<span data-ttu-id="4e301-112">`length`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="4e301-112">`length`: *Integer*</span></span>

<span data-ttu-id="4e301-113">Максимальная длина одной подстроки.</span><span class="sxs-lookup"><span data-stu-id="4e301-113">The maximum length of a single substring.</span></span>

<span data-ttu-id="4e301-114">`delimiter`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="4e301-114">`delimiter`: *String*</span></span>

<span data-ttu-id="4e301-115">Разделитель, который используется для разделения подстрок.</span><span class="sxs-lookup"><span data-stu-id="4e301-115">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="4e301-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="4e301-116">Return values</span></span>

<span data-ttu-id="4e301-117">*Список записей*</span><span class="sxs-lookup"><span data-stu-id="4e301-117">*Record list*</span></span>

<span data-ttu-id="4e301-118">Полученный список записей.</span><span class="sxs-lookup"><span data-stu-id="4e301-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="4e301-119">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="4e301-119">Usage notes</span></span>

<span data-ttu-id="4e301-120">Структура записи возвращенного списка состоит из поля **Значение** типа *Строка*.</span><span class="sxs-lookup"><span data-stu-id="4e301-120">The record structure of the list that is returned consists of the **Value** field of the *String* type.</span></span> <span data-ttu-id="4e301-121">Каждая запись возвращаемого списка содержит созданные подстроки в этом поле.</span><span class="sxs-lookup"><span data-stu-id="4e301-121">Every record of the list that is returned contains generated substrings in this field.</span></span>

<span data-ttu-id="4e301-122">Если аргумент `delimiter` пуст, новый возвращаемый список состоит из одной записи с полем **Значение** типа *Строка*.</span><span class="sxs-lookup"><span data-stu-id="4e301-122">If the `delimiter` argument is empty, the new list that is returned consists of one record that has the **Value** field of the *String* type.</span></span> <span data-ttu-id="4e301-123">Это поле содержит введенный текст.</span><span class="sxs-lookup"><span data-stu-id="4e301-123">This field contains the input text.</span></span>

<span data-ttu-id="4e301-124">Если аргумент `input` пуст, возвращается новый пустой список.</span><span class="sxs-lookup"><span data-stu-id="4e301-124">If the `input` argument is empty, a new empty list is returned.</span></span> <span data-ttu-id="4e301-125">Если аргумент `input` или `delimiter` не указан (null), возникает исключение приложения.</span><span class="sxs-lookup"><span data-stu-id="4e301-125">If either the `input` or `delimiter` argument is unspecified (null), an application exception is thrown.</span></span>

## <a name="example-1"></a><span data-ttu-id="4e301-126">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4e301-126">Example 1</span></span>

<span data-ttu-id="4e301-127">`SPLIT ("abcd", 3)` возвращает новый список, который состоит из двух записей с полем **Значение** типа *Строка*.</span><span class="sxs-lookup"><span data-stu-id="4e301-127">`SPLIT ("abcd", 3)` returns a new list that consists of two records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="4e301-128">Поле **Значение** в первой записи содержит текст **"abc"**, и поле **Значение** во второй записи содержит текст **"d"**.</span><span class="sxs-lookup"><span data-stu-id="4e301-128">The **Value** field in the first record contains the text **"abc"**, and the **Value** field in the second record contains the text **"d"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="4e301-129">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4e301-129">Example 2</span></span>

<span data-ttu-id="4e301-130">`SPLIT ("XAb aBy", "aB")` возвращает новый список, который состоит из трех записей с полем **Значение** типа *Строка*.</span><span class="sxs-lookup"><span data-stu-id="4e301-130">`SPLIT ("XAb aBy", "aB")` returns a new list that consists of three records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="4e301-131">Поле **Значение** в первой записи содержит текст **"X"**, поле **Значение** во второй записи содержит текст **"&nbsp;"**, и поле **Значение** в третьей записи содержит текст **"y"**.</span><span class="sxs-lookup"><span data-stu-id="4e301-131">The **Value** field in the first record contains the text **"X"**, the **Value** field in the second record contains the text **"&nbsp;"**, and the **Value** field in the third record contains the text **"y"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="4e301-132">Пример 3</span><span class="sxs-lookup"><span data-stu-id="4e301-132">Example 3</span></span>

<span data-ttu-id="4e301-133">Можно использовать функцию [INDEX](er-functions-list-index.md) для доступа к отдельным элементам указанной строки ввода.</span><span class="sxs-lookup"><span data-stu-id="4e301-133">Yo can use the [INDEX](er-functions-list-index.md) function to access individual elements of the specified input string.</span></span> <span data-ttu-id="4e301-134">Если вы введете источник данных **MyList** типа **Вычисляемое поле** и настроите для него выражение `SPLIT("abc", 1)`, выражение `INDEX(MyList,2).Value` возвращает текст **"b"**.</span><span class="sxs-lookup"><span data-stu-id="4e301-134">If you enter the **MyList** data source of the **Calculated field** type and configure for it the `SPLIT("abc", 1)` expression, the expression `INDEX(MyList,2).Value` returns the text **"b"**.</span></span>

## <a name="example-4"></a><span data-ttu-id="4e301-135">Пример 4</span><span class="sxs-lookup"><span data-stu-id="4e301-135">Example 4</span></span>

<span data-ttu-id="4e301-136">Функция [ENUMERATE](er-functions-list-enumerate.md) также может помочь вам получить доступ к отдельным элементам указанной строки ввода.</span><span class="sxs-lookup"><span data-stu-id="4e301-136">The [ENUMERATE](er-functions-list-enumerate.md) function can also help you access individual elements of the specified input string.</span></span> <span data-ttu-id="4e301-137">Если сначала ввести источник данных **MyList** для типа **вычисляемого поля** и выполнить настройку выражения `SPLIT("abc", 1)`, а затем ввести источник данных **EnumeratedList** для типа **вычисляемого поля** и настроить для него выражение `ENUMERATE(MyList)`, выражение `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` возвратит текст **"b"**.</span><span class="sxs-lookup"><span data-stu-id="4e301-137">If you first enter the **MyList** data source of the **Calculated field** type and configure for it the `SPLIT("abc", 1)` expression, and then enter the **EnumeratedList** data source of the **Calculated field** type and configure for it the `ENUMERATE(MyList)` expression, the expression `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` returns the text **"b"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4e301-138">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4e301-138">Additional resources</span></span>

[<span data-ttu-id="4e301-139">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="4e301-139">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
