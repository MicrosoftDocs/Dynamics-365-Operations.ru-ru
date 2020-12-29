---
title: Функция ER GETENUMVALUEBYNAME
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности GETENUMVALUEBYNAME.
author: NickSelin
manager: kfend
ms.date: 09/23/2020
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
ms.openlocfilehash: 29d7ec6498090ea47259303237c5a64a26e4926b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685940"
---
# <a name="getenumvaluebyname-er-function"></a><span data-ttu-id="5687b-103">Функция ER GETENUMVALUEBYNAME</span><span class="sxs-lookup"><span data-stu-id="5687b-103">GETENUMVALUEBYNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5687b-104">Функция `GETENUMVALUEBYNAME` выполняет поиск определенного значения *Enum* в указанном источнике данных перечисления, используя имя перечисления, указанное как значение *строка*.</span><span class="sxs-lookup"><span data-stu-id="5687b-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="5687b-105">При обнаружении значения *Enum* функция возвращает его.</span><span class="sxs-lookup"><span data-stu-id="5687b-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="5687b-106">В противном случае функция возвращает значение перечисления **null**.</span><span class="sxs-lookup"><span data-stu-id="5687b-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="5687b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5687b-107">Syntax</span></span>

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="5687b-108">Аргументы</span><span class="sxs-lookup"><span data-stu-id="5687b-108">Arguments</span></span>

<span data-ttu-id="5687b-109">`enumeration data source path`: *Перечисление*</span><span class="sxs-lookup"><span data-stu-id="5687b-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="5687b-110">Действительный путь источника данных одного из следующих типов перечисления:</span><span class="sxs-lookup"><span data-stu-id="5687b-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="5687b-111">Перечисление модели электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="5687b-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="5687b-112">Перечисление формата ER</span><span class="sxs-lookup"><span data-stu-id="5687b-112">ER format enumeration</span></span>
- <span data-ttu-id="5687b-113">Перечисление Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="5687b-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="5687b-114">`enumeration value text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="5687b-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="5687b-115">Строковое значение, представляющее имя одного значения перечисления.</span><span class="sxs-lookup"><span data-stu-id="5687b-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="5687b-116">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="5687b-116">Return values</span></span>

<span data-ttu-id="5687b-117">Обнуляемый *Enum*</span><span class="sxs-lookup"><span data-stu-id="5687b-117">Nullable *Enum*</span></span>

<span data-ttu-id="5687b-118">Результирующее значение перечисления.</span><span class="sxs-lookup"><span data-stu-id="5687b-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5687b-119">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="5687b-119">Usage notes</span></span>

<span data-ttu-id="5687b-120">Исключение не выдается, если значение *Enum* не найдено с помощью имени значения перечисления, указанного как значение *строки*.</span><span class="sxs-lookup"><span data-stu-id="5687b-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="5687b-121">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5687b-121">Example 1</span></span>

<span data-ttu-id="5687b-122">На следующем рисунке показано перечисление **ReportDirection** введенное в модели данных.</span><span class="sxs-lookup"><span data-stu-id="5687b-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="5687b-123">Обратите внимание, что метки определены для значений перечисления.</span><span class="sxs-lookup"><span data-stu-id="5687b-123">Notice that labels are defined for the enumeration values.</span></span>

![Доступные значения для перечисления модели данных](./media/ER-data-model-enumeration-values.PNG)

<span data-ttu-id="5687b-125">Следующая иллюстрация показывает эти детали:</span><span class="sxs-lookup"><span data-stu-id="5687b-125">The following illustration shows these details:</span></span>

- <span data-ttu-id="5687b-126">Источник данных **$Direction** настроен в отчете ER.</span><span class="sxs-lookup"><span data-stu-id="5687b-126">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="5687b-127">Этот источник данных настроен на основе перечисления модели **ReportDirection**.</span><span class="sxs-lookup"><span data-stu-id="5687b-127">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="5687b-128">Выражение `$IsArrivals` разработано для использования модели на основе перечисления для источника данных **$Direction** в качестве параметра этой функции.</span><span class="sxs-lookup"><span data-stu-id="5687b-128">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="5687b-129">Значение этого выражения сравнения — **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="5687b-129">The value of this comparison expression is **TRUE**.</span></span>

![Пример перечисления модели данных](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a><span data-ttu-id="5687b-131">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5687b-131">Example 2</span></span>

<span data-ttu-id="5687b-132">Функции `GETENUMVALUEBYNAME` и [`LISTOFFIELDS`](er-functions-list-listoffields.md) позволяют выбирать значения и метки поддерживаемых перечислений как текстовые значения.</span><span class="sxs-lookup"><span data-stu-id="5687b-132">The `GETENUMVALUEBYNAME` and [`LISTOFFIELDS`](er-functions-list-listoffields.md) functions let you fetch values and labels of supported enumerations as text values.</span></span> <span data-ttu-id="5687b-133">(Поддерживаемые перечисления: перечисления приложений, перечисления моделей данных и перечисления форматов.)</span><span class="sxs-lookup"><span data-stu-id="5687b-133">(The supported enumerations are application enumerations, data model enumerations, and format enumerations.)</span></span>

<span data-ttu-id="5687b-134">На следующем рисунке источник данных **TransType** вводится в сопоставлении модели.</span><span class="sxs-lookup"><span data-stu-id="5687b-134">In the following illustration, the **TransType** data source is introduced in a model mapping.</span></span> <span data-ttu-id="5687b-135">Этот источник данных относится к перечислению приложения **LedgerTransType**.</span><span class="sxs-lookup"><span data-stu-id="5687b-135">This data source refers to the **LedgerTransType** application enumeration.</span></span>

![Источник данных сопоставления модели, ссылающийся на перечисление приложения](./media/er-functions-text-getenumvaluebyname-example2-1.png)

<span data-ttu-id="5687b-137">На следующем рисунке показан источник данных **TransTypeList**, настроенный в сопоставлении модели.</span><span class="sxs-lookup"><span data-stu-id="5687b-137">The following illustration shows the **TransTypeList** data source that is configured in a model mapping.</span></span> <span data-ttu-id="5687b-138">Этот источник данных настроен на основе перечисления приложения **TransType**.</span><span class="sxs-lookup"><span data-stu-id="5687b-138">This data source is configured based on the **TransType** application enumeration.</span></span> <span data-ttu-id="5687b-139">Функция `LISTOFFIELDS` используется для того, чтобы вернуть все значения перечисления в виде списка записей, содержащих поля.</span><span class="sxs-lookup"><span data-stu-id="5687b-139">The `LISTOFFIELDS` function is used to return all enumeration values as a list of records that contain fields.</span></span> <span data-ttu-id="5687b-140">Таким образом предоставляются сведения о каждом значении перечисления.</span><span class="sxs-lookup"><span data-stu-id="5687b-140">In this way, the details of every enumeration value are exposed.</span></span>

> [!NOTE]
> <span data-ttu-id="5687b-141">Поле **EnumValue** настроено для источника данных **TransTypeList** с помощью выражения `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)`.</span><span class="sxs-lookup"><span data-stu-id="5687b-141">The **EnumValue** field is configured for the **TransTypeList** data source by using the `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` expression.</span></span> <span data-ttu-id="5687b-142">Это поле возвращает значение перечисления для каждой записи в данном списке.</span><span class="sxs-lookup"><span data-stu-id="5687b-142">This field returns an enumeration value for every record in this list.</span></span>

![Источник данных сопоставления модели, который возвращает все значения перечисления выбранного перечисления в виде списка записей](./media/er-functions-text-getenumvaluebyname-example2-2.png)

<span data-ttu-id="5687b-144">На следующем рисунке показан источник данных **VendTrans**, настроенный в сопоставлении модели.</span><span class="sxs-lookup"><span data-stu-id="5687b-144">The following illustration shows the **VendTrans** data source that is configured in a model mapping.</span></span> <span data-ttu-id="5687b-145">Этот источник данных возвращает записи проводок поставщика из таблицы приложения **VendTrans**.</span><span class="sxs-lookup"><span data-stu-id="5687b-145">This data source returns vendor transaction records from the **VendTrans** application table.</span></span> <span data-ttu-id="5687b-146">Тип книги учета каждой проводки определяется значением поля **TransType**.</span><span class="sxs-lookup"><span data-stu-id="5687b-146">The ledger type of every transaction is defined by the value of the **TransType** field.</span></span>

> [!NOTE]
> <span data-ttu-id="5687b-147">Поле **TransTypeTitle** настроено для источника данных **VendTrans** с помощью выражения `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label`.</span><span class="sxs-lookup"><span data-stu-id="5687b-147">The **TransTypeTitle** field is configured for the **VendTrans** data source by using the `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` expression.</span></span> <span data-ttu-id="5687b-148">Это поле возвращает метку значения перечисления текущей проводки в виде текста, если это значение перечисления доступно.</span><span class="sxs-lookup"><span data-stu-id="5687b-148">This field returns the label of an enumeration value of the current transaction as text, if this enumeration value is available.</span></span> <span data-ttu-id="5687b-149">В противном случае оно возвращает пустое значение.</span><span class="sxs-lookup"><span data-stu-id="5687b-149">Otherwise, it returns a blank string value.</span></span>
>
> <span data-ttu-id="5687b-150">Поле **TransTypeTitle** связано с полем **LedgerType** модели данных, которое позволяет использовать эту информацию в любом формате электронной отчетности, который использует модель данных в качестве источника данных.</span><span class="sxs-lookup"><span data-stu-id="5687b-150">The **TransTypeTitle** field is bound to the **LedgerType** field of a data model that enables this information to be used in every ER format that uses the data model as a source of data.</span></span>

![Источник данных сопоставления модели, который возвращает проводки поставщика](./media/er-functions-text-getenumvaluebyname-example2-3.png)

<span data-ttu-id="5687b-152">На следующем рисунке показано, как можно использовать [отладчик источников данных](er-debug-data-sources.md) для проверки настроенного сопоставления модели.</span><span class="sxs-lookup"><span data-stu-id="5687b-152">The following illustration shows how you can use the [data source debugger](er-debug-data-sources.md) to test the configured model mapping.</span></span>

![Проверка настроенного сопоставления модели с помощью отладчика источника данных](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

<span data-ttu-id="5687b-154">Поле **LedgerType** модели данных предоставляет метки типов проводок, как и ожидается.</span><span class="sxs-lookup"><span data-stu-id="5687b-154">The **LedgerType** field of a data model exposes labels of transaction types as expected.</span></span>

<span data-ttu-id="5687b-155">Если планируется использовать этот подход для больших объемов данных по проводкам, следует рассмотреть производительность выполнения.</span><span class="sxs-lookup"><span data-stu-id="5687b-155">If you plan to use this approach for a large amount of transactional data, you must consider execution performance.</span></span> <span data-ttu-id="5687b-156">Дополнительные сведения см. в разделе [Трассировка выполнения форматов электронной отчетности для устранения неполадок, связанных с производительностью](trace-execution-er-troubleshoot-perf.md).</span><span class="sxs-lookup"><span data-stu-id="5687b-156">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5687b-157">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5687b-157">Additional resources</span></span>

[<span data-ttu-id="5687b-158">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="5687b-158">Text functions</span></span>](er-functions-category-text.md)

[<span data-ttu-id="5687b-159">Трассировка выполнения форматов электронной отчетности для устранения неполадок, связанных с производительностью</span><span class="sxs-lookup"><span data-stu-id="5687b-159">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)

[<span data-ttu-id="5687b-160">Функция ER LISTOFFIELDS</span><span class="sxs-lookup"><span data-stu-id="5687b-160">LISTOFFIELDS ER function</span></span>](er-functions-list-listoffields.md)

[<span data-ttu-id="5687b-161">Функция ER FIRSTORNULL</span><span class="sxs-lookup"><span data-stu-id="5687b-161">FIRSTORNULL ER function</span></span>](er-functions-list-firstornull.md)

[<span data-ttu-id="5687b-162">Функция ER WHERE</span><span class="sxs-lookup"><span data-stu-id="5687b-162">WHERE ER function</span></span>](er-functions-list-where.md)
