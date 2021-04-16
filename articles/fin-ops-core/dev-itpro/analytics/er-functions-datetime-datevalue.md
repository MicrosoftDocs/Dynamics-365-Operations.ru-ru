---
title: Функция ER DATEVALUE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности DATEVALUE.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: d760c3f874bfebad11b9497b136cb67df4e9ea61
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746947"
---
# <a name="datevalue-er-function"></a><span data-ttu-id="98915-103">Функция ER DATEVALUE</span><span class="sxs-lookup"><span data-stu-id="98915-103">DATEVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98915-104">Функция `DATEVALUE` возвращает значение *Date*, которое преобразуется из текстового значения в указанном формате и в дополнительно указанной [культуре](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) в значение даты.</span><span class="sxs-lookup"><span data-stu-id="98915-104">The `DATEVALUE` function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date value.</span></span> <span data-ttu-id="98915-105">Сведения о поддерживаемых форматах см. в разделах [стандартный](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) и [настраиваемый](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="98915-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="98915-106">Синтаксис 1</span><span class="sxs-lookup"><span data-stu-id="98915-106">Syntax 1</span></span>

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="98915-107">Синтаксис 2</span><span class="sxs-lookup"><span data-stu-id="98915-107">Syntax 2</span></span>

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="98915-108">Аргументы</span><span class="sxs-lookup"><span data-stu-id="98915-108">Arguments</span></span>

<span data-ttu-id="98915-109">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="98915-109">`text`: *String*</span></span>

<span data-ttu-id="98915-110">Текст, представляющий значение для формата.</span><span class="sxs-lookup"><span data-stu-id="98915-110">Text that represents the value to format.</span></span>

<span data-ttu-id="98915-111">`format`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="98915-111">`format`: *String*</span></span>

<span data-ttu-id="98915-112">Формат указанного текста.</span><span class="sxs-lookup"><span data-stu-id="98915-112">The format of the given text.</span></span>

<span data-ttu-id="98915-113">`culture`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="98915-113">`culture`: *String*</span></span>

<span data-ttu-id="98915-114">Культура, используемая для форматирования указанного текста.</span><span class="sxs-lookup"><span data-stu-id="98915-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="98915-115">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="98915-115">Return values</span></span>

<span data-ttu-id="98915-116">*Дата*</span><span class="sxs-lookup"><span data-stu-id="98915-116">*Date*</span></span>

<span data-ttu-id="98915-117">Результирующее значение даты.</span><span class="sxs-lookup"><span data-stu-id="98915-117">The resulting date value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="98915-118">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="98915-118">Usage notes</span></span>

<span data-ttu-id="98915-119">Когда культура не определена как аргумент вызываемой функции, значение `culture` определяется контекстом вызова.</span><span class="sxs-lookup"><span data-stu-id="98915-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="98915-120">Например, если функция `DATEVALUE` вызывается с помощью синтаксиса 1 в формате электронной отчетности (ER) для элемента **FILE**, настроенного на использование немецкой культуры, преобразование будет осуществляться с помощью немецкой культуры.</span><span class="sxs-lookup"><span data-stu-id="98915-120">For example, if the `DATEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="98915-121">Значение шаблона `culture` по умолчанию — **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="98915-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="98915-122">Пример 1</span><span class="sxs-lookup"><span data-stu-id="98915-122">Example 1</span></span>

<span data-ttu-id="98915-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` возвращает значение данных **21 декабря 2016** на основе указанного пользовательского формата и культуры приложения по умолчанию **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="98915-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` returns the date value **December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="98915-124">Пример 2</span><span class="sxs-lookup"><span data-stu-id="98915-124">Example 2</span></span>

<span data-ttu-id="98915-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` возвращает значение даты **21 января2016** на основе указанного пользовательского формата и культуры.</span><span class="sxs-lookup"><span data-stu-id="98915-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` returns the date value **January 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="98915-126">Однако вызов `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` вызывает исключение, информирующее пользователя, что указанная строка не распознана как допустимое значение даты для указанной культуры.</span><span class="sxs-lookup"><span data-stu-id="98915-126">However, `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="98915-127">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="98915-127">Additional resources</span></span>

[<span data-ttu-id="98915-128">Функции даты и времени</span><span class="sxs-lookup"><span data-stu-id="98915-128">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]