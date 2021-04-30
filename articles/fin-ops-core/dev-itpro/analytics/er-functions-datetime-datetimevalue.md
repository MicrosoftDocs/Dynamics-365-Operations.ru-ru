---
title: Функция ER DATETIMEVALUE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности DATETIMEVALUE.
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: db5b2c56f0c6dcc019419801821d7a6eae8a0e91
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891289"
---
# <a name="datetimevalue-er-function"></a><span data-ttu-id="75225-103">Функция ER DATETIMEVALUE</span><span class="sxs-lookup"><span data-stu-id="75225-103">DATETIMEVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75225-104">Функция `DATETIMEVALUE` возвращает значение *DateTime*, которое преобразуется из текстового значения в указанном формате и в дополнительно указанной [культуре](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) в значение даты/времени.</span><span class="sxs-lookup"><span data-stu-id="75225-104">The `DATETIMEVALUE` function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date/time value.</span></span> <span data-ttu-id="75225-105">Сведения о поддерживаемых форматах см. в разделах [стандартный](/dotnet/standard/base-types/standard-date-and-time-format-strings) и [настраиваемый](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="75225-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) and [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="75225-106">Синтаксис 1</span><span class="sxs-lookup"><span data-stu-id="75225-106">Syntax 1</span></span>

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="75225-107">Синтаксис 2</span><span class="sxs-lookup"><span data-stu-id="75225-107">Syntax 2</span></span>

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="75225-108">Аргументы</span><span class="sxs-lookup"><span data-stu-id="75225-108">Arguments</span></span>

<span data-ttu-id="75225-109">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="75225-109">`text`: *String*</span></span>

<span data-ttu-id="75225-110">Текст, представляющий значение для формата.</span><span class="sxs-lookup"><span data-stu-id="75225-110">Text that represents the value to format.</span></span>

<span data-ttu-id="75225-111">`format`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="75225-111">`format`: *String*</span></span>

<span data-ttu-id="75225-112">Формат указанного текста.</span><span class="sxs-lookup"><span data-stu-id="75225-112">The format of the given text.</span></span>

<span data-ttu-id="75225-113">`culture`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="75225-113">`culture`: *String*</span></span>

<span data-ttu-id="75225-114">Культура, используемая для форматирования указанного текста.</span><span class="sxs-lookup"><span data-stu-id="75225-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="75225-115">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="75225-115">Return values</span></span>

<span data-ttu-id="75225-116">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="75225-116">*DateTime*</span></span>

<span data-ttu-id="75225-117">Результирующее значение даты/времени.</span><span class="sxs-lookup"><span data-stu-id="75225-117">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="75225-118">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="75225-118">Usage notes</span></span>

<span data-ttu-id="75225-119">Когда культура не определена как аргумент вызываемой функции, значение `culture` определяется контекстом вызова.</span><span class="sxs-lookup"><span data-stu-id="75225-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="75225-120">Например, если функция `DATETIMEVALUE` вызывается с помощью синтаксиса 1 в формате электронной отчетности (ER) для элемента **FILE**, настроенного на использование немецкой культуры, преобразование будет осуществляться с помощью немецкой культуры.</span><span class="sxs-lookup"><span data-stu-id="75225-120">For example, if the `DATETIMEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="75225-121">Значение шаблона `culture` по умолчанию — **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="75225-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="75225-122">Пример 1</span><span class="sxs-lookup"><span data-stu-id="75225-122">Example 1</span></span>

<span data-ttu-id="75225-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` возвращает **2:55:00 21 декабря 2016** на основе указанного пользовательского формата и культуры приложения по умолчанию **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="75225-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="75225-124">Пример 2</span><span class="sxs-lookup"><span data-stu-id="75225-124">Example 2</span></span>

<span data-ttu-id="75225-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` возвращает **2:55:00 21 декабря 2016** на основе указанного пользовательского формата и культуры.</span><span class="sxs-lookup"><span data-stu-id="75225-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="75225-126">Однако вызов `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` вызывает исключение, информирующее пользователя, что указанная строка не распознана как допустимое значение даты/времени для указанной культуры.</span><span class="sxs-lookup"><span data-stu-id="75225-126">However, `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date/time value for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="75225-127">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="75225-127">Additional resources</span></span>

[<span data-ttu-id="75225-128">Функции даты и времени</span><span class="sxs-lookup"><span data-stu-id="75225-128">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]