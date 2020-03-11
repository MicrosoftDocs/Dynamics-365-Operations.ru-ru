---
title: Функция ER GETENUMVALUEBYNAME
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности GETENUMVALUEBYNAME.
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
ms.openlocfilehash: 87613978c149b5d41aefc58f9896424229819626
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041198"
---
# <span data-ttu-id="8abf3-103"><a name="GETENUMVALUEBYNAME">Функция ER GETENUMVALUEBYNAME</a></span><span class="sxs-lookup"><span data-stu-id="8abf3-103"><a name="GETENUMVALUEBYNAME">GETENUMVALUEBYNAME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8abf3-104">Функция `GETENUMVALUEBYNAME` выполняет поиск определенного значения *Enum* в указанном источнике данных перечисления, используя имя перечисления, указанное как значение *строка*.</span><span class="sxs-lookup"><span data-stu-id="8abf3-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="8abf3-105">При обнаружении значения *Enum* функция возвращает его.</span><span class="sxs-lookup"><span data-stu-id="8abf3-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="8abf3-106">В противном случае функция возвращает значение перечисления **null**.</span><span class="sxs-lookup"><span data-stu-id="8abf3-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="8abf3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8abf3-107">Syntax</span></span>

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="8abf3-108">Аргументы</span><span class="sxs-lookup"><span data-stu-id="8abf3-108">Arguments</span></span>

<span data-ttu-id="8abf3-109">`enumeration data source path`: *Перечисление*</span><span class="sxs-lookup"><span data-stu-id="8abf3-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="8abf3-110">Действительный путь источника данных одного из следующих типов перечисления:</span><span class="sxs-lookup"><span data-stu-id="8abf3-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="8abf3-111">Перечисление модели электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="8abf3-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="8abf3-112">Перечисление формата ER</span><span class="sxs-lookup"><span data-stu-id="8abf3-112">ER format enumeration</span></span>
- <span data-ttu-id="8abf3-113">Перечисление Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="8abf3-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="8abf3-114">`enumeration value text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="8abf3-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="8abf3-115">Строковое значение, представляющее имя одного значения перечисления.</span><span class="sxs-lookup"><span data-stu-id="8abf3-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="8abf3-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="8abf3-116">Return values</span></span>

<span data-ttu-id="8abf3-117">Обнуляемый *Enum*</span><span class="sxs-lookup"><span data-stu-id="8abf3-117">Nullable *Enum*</span></span>

<span data-ttu-id="8abf3-118">Результирующее значение перечисления.</span><span class="sxs-lookup"><span data-stu-id="8abf3-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8abf3-119">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="8abf3-119">Usage notes</span></span>

<span data-ttu-id="8abf3-120">Исключение не выдается, если значение *Enum* не найдено с помощью имени значения перечисления, указанного как значение *строки*.</span><span class="sxs-lookup"><span data-stu-id="8abf3-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example"></a><span data-ttu-id="8abf3-121">Пример</span><span class="sxs-lookup"><span data-stu-id="8abf3-121">Example</span></span>

<span data-ttu-id="8abf3-122">На следующем рисунке показано перечисление **ReportDirection** введенное в модели данных.</span><span class="sxs-lookup"><span data-stu-id="8abf3-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="8abf3-123">Обратите внимание, что метки определены для значений перечисления.</span><span class="sxs-lookup"><span data-stu-id="8abf3-123">Notice that labels are defined for the enumeration values.</span></span>

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="8abf3-124">Следующая иллюстрация показывает эти детали:</span><span class="sxs-lookup"><span data-stu-id="8abf3-124">The following illustration shows these details:</span></span>

- <span data-ttu-id="8abf3-125">Источник данных **$Direction** настроен в отчете ER.</span><span class="sxs-lookup"><span data-stu-id="8abf3-125">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="8abf3-126">Этот источник данных настроен на основе перечисления модели **ReportDirection**.</span><span class="sxs-lookup"><span data-stu-id="8abf3-126">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="8abf3-127">Выражение `$IsArrivals` разработано для использования модели на основе перечисления для источника данных **$Direction** в качестве параметра этой функции.</span><span class="sxs-lookup"><span data-stu-id="8abf3-127">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="8abf3-128">Значение этого выражения сравнения — **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="8abf3-128">The value of this comparison expression is **TRUE**.</span></span>

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a><span data-ttu-id="8abf3-129">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8abf3-129">Additional resources</span></span>

[<span data-ttu-id="8abf3-130">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="8abf3-130">Text functions</span></span>](er-functions-category-text.md)
