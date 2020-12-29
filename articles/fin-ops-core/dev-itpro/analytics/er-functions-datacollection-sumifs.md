---
title: Функция ER SUMIFS
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности SUMIFS.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9d9ef51f3c8cb090f940670c4c3afae104268ed
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687970"
---
# <a name="sumifs-er-function"></a><span data-ttu-id="24277-103">Функция ER SUMIFS</span><span class="sxs-lookup"><span data-stu-id="24277-103">SUMIFS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="24277-104">Функция `SUMIFS` возвращает *вещественное* значение, представляющее сумму значений, которые были возвращены привязками элементов формата и собраны во время использования для создания исходящего документа во время выполнения формата, и удовлетворяющее указанным условиям.</span><span class="sxs-lookup"><span data-stu-id="24277-104">The `SUMIFS` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="24277-105">Каждое условие состоит из диапазона ключей и значения ключа.</span><span class="sxs-lookup"><span data-stu-id="24277-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="24277-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24277-106">Syntax</span></span>

```vb
SUMIFS (key name for summing, condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="24277-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="24277-107">Arguments</span></span>

<span data-ttu-id="24277-108">`key name for summing`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="24277-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="24277-109">Значение, возвращаемое выражением, настроенным в свойстве **Имя ключа собранных данных** компонента формата электронной отчетности (ER), для которого значение привязки должно использоваться для целей суммирования.</span><span class="sxs-lookup"><span data-stu-id="24277-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="24277-110">Свойство **Имя ключа собранных данных** можно настроить как для компонента **Числовой**, так и для компонента **Строка** в формате ER, который находится в компоненте **Common\\File**, где включен параметр **Сбор сведений о результате**.</span><span class="sxs-lookup"><span data-stu-id="24277-110">The **Collected data key name** property can be configured for either a **Numeric** component or a **String** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="24277-111">`condition 1 range`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="24277-111">`condition 1 range`: *String*</span></span>

<span data-ttu-id="24277-112">Значение, возвращаемое выражением, настроенное в свойстве **Имя ключа собранных данных** компонента формата ER.</span><span class="sxs-lookup"><span data-stu-id="24277-112">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="24277-113">Этот аргумент является обязательным.</span><span class="sxs-lookup"><span data-stu-id="24277-113">This argument is mandatory.</span></span>

<span data-ttu-id="24277-114">Свойство **Имя ключа собранных данных** можно настроить как для компонента **Последовательность**, так и для компонента **Элемент XML** в формате ER, который находится в компоненте **Common\\File**, где включен параметр **Сбор сведений о результате**.</span><span class="sxs-lookup"><span data-stu-id="24277-114">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="24277-115">`condition 1 value`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="24277-115">`condition 1 value`: *String*</span></span>

<span data-ttu-id="24277-116">Значение, возвращаемое выражением, настроенное в свойстве **Значение ключа собранных данных** компонента формата ER.</span><span class="sxs-lookup"><span data-stu-id="24277-116">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="24277-117">Этот аргумент является обязательным.</span><span class="sxs-lookup"><span data-stu-id="24277-117">This argument is mandatory.</span></span>

<span data-ttu-id="24277-118">Свойство **Значение ключа собранных данных** можно настроить как для компонента **Последовательность**, так и для компонента **Элемент XML** в формате ER, который находится в компоненте **Common\\File**, где включен параметр **Сбор сведений о результате**.</span><span class="sxs-lookup"><span data-stu-id="24277-118">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="24277-119">`condition N range`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="24277-119">`condition N range`: *String*</span></span>

<span data-ttu-id="24277-120">Значение, возвращаемое выражением, настроенное в свойстве **Имя ключа собранных данных** компонента формата ER.</span><span class="sxs-lookup"><span data-stu-id="24277-120">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="24277-121">Эти дополнительные аргументы являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="24277-121">These additional arguments are optional.</span></span>

<span data-ttu-id="24277-122">Свойство **Имя ключа собранных данных** можно настроить как для компонента **Последовательность**, так и для компонента **Элемент XML** в формате ER, который находится в компоненте **Common\\File**, где включен параметр **Сбор сведений о результате**.</span><span class="sxs-lookup"><span data-stu-id="24277-122">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="24277-123">`condition N value`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="24277-123">`condition N value`: *String*</span></span>

<span data-ttu-id="24277-124">Значение, возвращаемое выражением, настроенное в свойстве **Значение ключа собранных данных** компонента формата ER.</span><span class="sxs-lookup"><span data-stu-id="24277-124">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="24277-125">Эти дополнительные аргументы являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="24277-125">These additional arguments are optional.</span></span>

<span data-ttu-id="24277-126">Свойство **Значение ключа собранных данных** можно настроить как для компонента **Последовательность**, так и для компонента **Элемент XML** в формате ER, который находится в компоненте **Common\\File**, где включен параметр **Сбор сведений о результате**.</span><span class="sxs-lookup"><span data-stu-id="24277-126">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="24277-127">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="24277-127">Return values</span></span>

<span data-ttu-id="24277-128">*Действующий*</span><span class="sxs-lookup"><span data-stu-id="24277-128">*Real*</span></span>

<span data-ttu-id="24277-129">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="24277-129">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="24277-130">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="24277-130">Usage notes</span></span>

<span data-ttu-id="24277-131">Эта функция возвращает значение **0** (ноль), когда параметр **Сбор сведений о результате** для текущего компонента **Common\\File** выключен.</span><span class="sxs-lookup"><span data-stu-id="24277-131">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="24277-132">В аргументах `condition range` подстановочный знак **"\*"** может быть использован для представления нескольких символов.</span><span class="sxs-lookup"><span data-stu-id="24277-132">In the `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="24277-133">В аргументах `condition value` подстановочный знак **"\*"** может быть использован для представления нескольких символов.</span><span class="sxs-lookup"><span data-stu-id="24277-133">In the `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="24277-134">Пример</span><span class="sxs-lookup"><span data-stu-id="24277-134">Example</span></span>

<span data-ttu-id="24277-135">Для получения дополнительных сведений об использовании этой функции см. проводник по задаче [ER Использование выходных данных формата для инвентаризации и агрегирования](tasks/er-format-counting-summing-1.md), который является частью бизнес-процесса **Приобретение/разработка компонентов ИТ-услуг и решений**.</span><span class="sxs-lookup"><span data-stu-id="24277-135">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="24277-136">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="24277-136">Additional resources</span></span>

[<span data-ttu-id="24277-137">Функции сбора данных</span><span class="sxs-lookup"><span data-stu-id="24277-137">Data collection functions</span></span>](er-functions-category-data-collection.md)
