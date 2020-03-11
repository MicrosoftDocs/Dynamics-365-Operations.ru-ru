---
title: Функция ER COUNTIFS
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности COUNTIFS.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 9627c7835c8f3f1b6aedc1f691470dc29a11d6b5
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042558"
---
# <span data-ttu-id="2c82f-103"><a name="COUNTIFS">Функция ER COUNTIFS</a></span><span class="sxs-lookup"><span data-stu-id="2c82f-103"><a name="COUNTIFS">COUNTIFS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c82f-104">Функция `COUNTIFS` возвращает *целочисленное* значение, представляющее количество элементов формата, которые были собраны при использовании элементов формата для создания исходящего документа во время выполнения формата, и удовлетворяющее указанным условиям.</span><span class="sxs-lookup"><span data-stu-id="2c82f-104">The `COUNTIFS` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="2c82f-105">Каждое условие состоит из диапазона ключей и значения ключа.</span><span class="sxs-lookup"><span data-stu-id="2c82f-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c82f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c82f-106">Syntax</span></span>

```vb
COUNTIFS (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="2c82f-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="2c82f-107">Arguments</span></span>

<span data-ttu-id="2c82f-108">`condition 1 range`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="2c82f-108">`condition 1 range`: *String*</span></span>

<span data-ttu-id="2c82f-109">Значение, возвращаемое выражением, настроенное в свойстве **Имя ключа собранных данных** компонента формата электронной отчетности (ER).</span><span class="sxs-lookup"><span data-stu-id="2c82f-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span> <span data-ttu-id="2c82f-110">Этот аргумент является обязательным.</span><span class="sxs-lookup"><span data-stu-id="2c82f-110">This argument is mandatory.</span></span>

<span data-ttu-id="2c82f-111">`condition 1 value`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="2c82f-111">`condition 1 value`: *String*</span></span>

<span data-ttu-id="2c82f-112">Значение, возвращаемое выражением, настроенное в свойстве **Значение ключа собранных данных** компонента формата ER.</span><span class="sxs-lookup"><span data-stu-id="2c82f-112">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="2c82f-113">Этот аргумент является обязательным.</span><span class="sxs-lookup"><span data-stu-id="2c82f-113">This argument is mandatory.</span></span>

<span data-ttu-id="2c82f-114">`condition N range`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="2c82f-114">`condition N range`: *String*</span></span>

<span data-ttu-id="2c82f-115">Значение, возвращаемое выражением, настроенное в свойстве **Имя ключа собранных данных** компонента формата ER.</span><span class="sxs-lookup"><span data-stu-id="2c82f-115">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="2c82f-116">Эти дополнительные аргументы являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="2c82f-116">These additional arguments are optional.</span></span>

<span data-ttu-id="2c82f-117">`condition N value`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="2c82f-117">`condition N value`: *String*</span></span>

<span data-ttu-id="2c82f-118">Значение, возвращаемое выражением, настроенное в свойстве **Значение ключа собранных данных** компонента формата ER.</span><span class="sxs-lookup"><span data-stu-id="2c82f-118">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="2c82f-119">Эти дополнительные аргументы являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="2c82f-119">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="2c82f-120">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="2c82f-120">Return values</span></span>

<span data-ttu-id="2c82f-121">*Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="2c82f-121">*Integer*</span></span>

<span data-ttu-id="2c82f-122">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="2c82f-122">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2c82f-123">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="2c82f-123">Usage notes</span></span>

<span data-ttu-id="2c82f-124">Свойства **Имя ключа собранных данных** и **Значение ключа собранных данных** могут быть настроены как для компонента **Последовательность**, так и для компонента **Элемент XML** в формате ER, который находится в компоненте **Common\\File**, где включен параметр **Сбор сведений о результате**.</span><span class="sxs-lookup"><span data-stu-id="2c82f-124">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="2c82f-125">Эта функция возвращает значение **0** (ноль), когда параметр **Сбор сведений о результате** для текущего компонента **Common\\File** выключен.</span><span class="sxs-lookup"><span data-stu-id="2c82f-125">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="2c82f-126">В аргументах `condition range` подстановочный знак **"\*"** может быть использован для представления нескольких символов.</span><span class="sxs-lookup"><span data-stu-id="2c82f-126">In `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="2c82f-127">В аргументах `condition value` подстановочный знак **"\*"** может быть использован для представления нескольких символов.</span><span class="sxs-lookup"><span data-stu-id="2c82f-127">In `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="2c82f-128">Пример</span><span class="sxs-lookup"><span data-stu-id="2c82f-128">Example</span></span>

<span data-ttu-id="2c82f-129">Для получения дополнительных сведений об использовании этой функции см. проводник по задаче [ER Использование выходных данных формата для инвентаризации и агрегирования](tasks/er-format-counting-summing-1.md), который является частью бизнес-процесса **Приобретение/разработка компонентов ИТ-услуг и решений**.</span><span class="sxs-lookup"><span data-stu-id="2c82f-129">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c82f-130">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2c82f-130">Additional resources</span></span>

[<span data-ttu-id="2c82f-131">Функции сбора данных</span><span class="sxs-lookup"><span data-stu-id="2c82f-131">Data collection functions</span></span>](er-functions-category-data-collection.md)
