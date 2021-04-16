---
title: Функция ER NUMSEQVALUE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности NUMSEQVALUE.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: c3351360d0c1afca9f828ba4fc935096ddfd67f2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744011"
---
# <a name="numseqvalue-er-function"></a><span data-ttu-id="17081-103">Функция ER NUMSEQVALUE</span><span class="sxs-lookup"><span data-stu-id="17081-103">NUMSEQVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17081-104">Функция `NUMSEQVALUE` возвращает *строковое* значение, представляющее новое создаваемое значение номерной серии на основе заданной номерной серии, области и идентификатора области.</span><span class="sxs-lookup"><span data-stu-id="17081-104">The `NUMSEQVALUE` function returns a *String* value that represents the new generated value of a number sequence, based on the specified number sequence, scope, and scope ID.</span></span> <span data-ttu-id="17081-105">Идентификатор области равен коду компании из контекста, в котором выполняется формат электронной отчетности (ER).</span><span class="sxs-lookup"><span data-stu-id="17081-105">The scope ID equals the company code that is supplied by the context that the Electronic reporting (ER) format is run under.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="17081-106">Синтаксис 1</span><span class="sxs-lookup"><span data-stu-id="17081-106">Syntax 1</span></span>

```vb
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a><span data-ttu-id="17081-107">Синтаксис 2</span><span class="sxs-lookup"><span data-stu-id="17081-107">Syntax 2</span></span>

```vb
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a><span data-ttu-id="17081-108">Синтаксис 3</span><span class="sxs-lookup"><span data-stu-id="17081-108">Syntax 3</span></span>

```vb
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a><span data-ttu-id="17081-109">Аргументы</span><span class="sxs-lookup"><span data-stu-id="17081-109">Arguments</span></span>

<span data-ttu-id="17081-110">`number sequence code`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="17081-110">`number sequence code`: *String*</span></span>

<span data-ttu-id="17081-111">Текстовое значение, представляющее код номерной серии, в которой требуется новое значение.</span><span class="sxs-lookup"><span data-stu-id="17081-111">A text value that represents the code of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="17081-112">`number sequence record ID`: *Int64*</span><span class="sxs-lookup"><span data-stu-id="17081-112">`number sequence record ID`: *Int64*</span></span>

<span data-ttu-id="17081-113">Значение *Int64*, представляющее идентификатор записи в таблице NumberSequenceTable, содержащий определение номерной серии, в которой требуется новое значение.</span><span class="sxs-lookup"><span data-stu-id="17081-113">An *Int64* value that represents the record ID of a record in the NumberSequenceTable table that contains the definition of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="17081-114">`scope type`: *Значение перечисления*</span><span class="sxs-lookup"><span data-stu-id="17081-114">`scope type`: *Enum value*</span></span>

<span data-ttu-id="17081-115">Значение перечисления в перечислении **ERExpressionNumberSequenceScopeType**, определяющее область номерной серии, в которой требуется новое значение.</span><span class="sxs-lookup"><span data-stu-id="17081-115">An enumeration value of the **ERExpressionNumberSequenceScopeType** enumeration that defines the scope of the number sequence that a new value is required in.</span></span> <span data-ttu-id="17081-116">Доступные типы области являются **общий**, **юридическое лицо** и **компания**.</span><span class="sxs-lookup"><span data-stu-id="17081-116">The available scope types are **Shared**, **Legal entity**, and **Company**.</span></span>

<span data-ttu-id="17081-117">`scope ID`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="17081-117">`scope ID`: *String*</span></span>

<span data-ttu-id="17081-118">*Строковое* значение, идентифицирующее область на основе заданного типа области.</span><span class="sxs-lookup"><span data-stu-id="17081-118">A *String* value that identifies the scope, based on the specified scope type.</span></span>

## <a name="return-values"></a><span data-ttu-id="17081-119">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="17081-119">Return values</span></span>

<span data-ttu-id="17081-120">*Строка*</span><span class="sxs-lookup"><span data-stu-id="17081-120">*String*</span></span>

<span data-ttu-id="17081-121">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="17081-121">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="17081-122">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="17081-122">Usage notes</span></span>

<span data-ttu-id="17081-123">Для типа области **Общие** укажите пустую строку как код области.</span><span class="sxs-lookup"><span data-stu-id="17081-123">For the **Shared** scope type, specify an empty string as the scope ID.</span></span>

<span data-ttu-id="17081-124">Для типов областей **Компания** и **Юридическое лицо** укажите код компании как код области.</span><span class="sxs-lookup"><span data-stu-id="17081-124">For the **Company** and **Legal entity** scope types, specify the company code as the scope ID.</span></span> <span data-ttu-id="17081-125">Если указать пустую строку в качестве кода области для этих типов областей, используется код текущей компании.</span><span class="sxs-lookup"><span data-stu-id="17081-125">If you specify an empty string as the scope ID for these scope types, the current company code is used.</span></span>

<span data-ttu-id="17081-126">При использовании синтаксиса 1 запрашивается номерная серия для типа области **Компания**, а код компании предоставляется контекстом, в котором работает формат ER.</span><span class="sxs-lookup"><span data-stu-id="17081-126">When syntax 1 is used, the number sequence is requested for the **Company** scope type, and the company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-1"></a><span data-ttu-id="17081-127">Пример 1</span><span class="sxs-lookup"><span data-stu-id="17081-127">Example 1</span></span>

<span data-ttu-id="17081-128">В формате ER вы определяете источник данных **AskNumSeq** типа *Параметр пользовательского ввода*.</span><span class="sxs-lookup"><span data-stu-id="17081-128">In your ER format, you define the **AskNumSeq** data source of the *User input parameter* type.</span></span> <span data-ttu-id="17081-129">Этот источник данных относится к расширенному типу данных **Описание** (EDT).</span><span class="sxs-lookup"><span data-stu-id="17081-129">This data source refers to the **Description** extended data type (EDT).</span></span> <span data-ttu-id="17081-130">Далее вы определяете источник данных **NumSeq** типа *Вычисляемое поле*.</span><span class="sxs-lookup"><span data-stu-id="17081-130">Next, you define the **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="17081-131">Этот источник данных содержит выражение `NUMSEQVALUE (AskNumSeq)`.</span><span class="sxs-lookup"><span data-stu-id="17081-131">This data source contains the expression `NUMSEQVALUE (AskNumSeq)`.</span></span> <span data-ttu-id="17081-132">При вызове источника данных **NumSeq** возвращается новое создаваемое значение номерной серии, указанное во время выполнения вводом кода в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="17081-132">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that was specified at runtime by entering its code in the dialog box.</span></span> <span data-ttu-id="17081-133">Номерная серия запрашивается для типа области **Компания**.</span><span class="sxs-lookup"><span data-stu-id="17081-133">The number sequence is requested for the **Company** scope type.</span></span> <span data-ttu-id="17081-134">Код компании предоставляется контекстом, в котором работает формат ER.</span><span class="sxs-lookup"><span data-stu-id="17081-134">The company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-2"></a><span data-ttu-id="17081-135">Пример 2</span><span class="sxs-lookup"><span data-stu-id="17081-135">Example 2</span></span>

<span data-ttu-id="17081-136">Следующие источники данных определяются в вашем сопоставлении модели:</span><span class="sxs-lookup"><span data-stu-id="17081-136">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="17081-137">Источник данных **LedgerParms** типа *Таблица*.</span><span class="sxs-lookup"><span data-stu-id="17081-137">The **LedgerParms** data source of the *Table* type.</span></span> <span data-ttu-id="17081-138">Этот источник данных ссылается на таблицу LedgerParameters.</span><span class="sxs-lookup"><span data-stu-id="17081-138">This data source refers to the LedgerParameters table.</span></span>
- <span data-ttu-id="17081-139">Источник данных **NumSeq** типа *Вычисляемое поле*.</span><span class="sxs-lookup"><span data-stu-id="17081-139">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="17081-140">Этот источник данных содержит выражение `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.</span><span class="sxs-lookup"><span data-stu-id="17081-140">This data source contains the expression `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.</span></span>

<span data-ttu-id="17081-141">При вызове источника данных **NumSeq** он возвращает новое сформированное значение номерной серии, которая была настроена в параметрах главной книги для компании, предоставляющая контекст, в котором выполняется формат электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="17081-141">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that has been configured in the General ledger parameters for the company that supplies the context that the ER format is run under.</span></span> <span data-ttu-id="17081-142">Эта номерная серия уникальным образом идентифицирует журналы и выступает в качестве номера партии, который связывает проводки друг с другом.</span><span class="sxs-lookup"><span data-stu-id="17081-142">This number sequence uniquely identifies journals and acts as a batch number that links the transactions together.</span></span>

## <a name="example-3"></a><span data-ttu-id="17081-143">Пример 3</span><span class="sxs-lookup"><span data-stu-id="17081-143">Example 3</span></span>

<span data-ttu-id="17081-144">Следующие источники данных определяются в вашем сопоставлении модели:</span><span class="sxs-lookup"><span data-stu-id="17081-144">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="17081-145">Источник данных **enumScope** типа *перечисления* Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="17081-145">The **enumScope** data source of the Microsoft Dynamics 365 Finance *enumeration* type.</span></span> <span data-ttu-id="17081-146">Этот источник данных относится к перечислению **ERExpressionNumberSequenceScopeType**.</span><span class="sxs-lookup"><span data-stu-id="17081-146">This data source refers to the **ERExpressionNumberSequenceScopeType** enumeration.</span></span>
- <span data-ttu-id="17081-147">Источник данных **NumSeq** типа *Вычисляемое поле*.</span><span class="sxs-lookup"><span data-stu-id="17081-147">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="17081-148">Этот источник данных содержит выражение `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.</span><span class="sxs-lookup"><span data-stu-id="17081-148">This data source contains the expression `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.</span></span>

<span data-ttu-id="17081-149">При вызове источника данных **NumSeq** он возвращает новое сформированное значение номерной серии **Gene\_1**, которая была настроена для компании, предоставляющая контекст, в котором выполняется формат электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="17081-149">When the **NumSeq** data source is called, it returns the new generated value of the **Gene\_1** number sequence that has been configured for the company that supplies the context that the ER format is run under.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="17081-150">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="17081-150">Additional resources</span></span>

[<span data-ttu-id="17081-151">Другие функции (характерные для конкретных бизнес-доменов)</span><span class="sxs-lookup"><span data-stu-id="17081-151">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]