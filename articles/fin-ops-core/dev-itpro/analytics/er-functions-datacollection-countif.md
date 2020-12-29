---
title: Функция ER COUNTIF
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности COUNTIF.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f1429ad98f9d4fdab992c2011c6518734484a84
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681192"
---
# <a name="countif-er-function"></a><span data-ttu-id="b10db-103">Функция ER COUNTIF</span><span class="sxs-lookup"><span data-stu-id="b10db-103">COUNTIF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b10db-104">Функция `COUNTIF` возвращает *целочисленное* значение, представляющее количество элементов формата, которые были собраны при использовании элементов формата для создания исходящего документа во время выполнения формата, и удовлетворяющее указанному условию.</span><span class="sxs-lookup"><span data-stu-id="b10db-104">The `COUNTIF` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="b10db-105">Условие состоит из диапазона ключей и значения ключа.</span><span class="sxs-lookup"><span data-stu-id="b10db-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="b10db-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b10db-106">Syntax</span></span>

```vb
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="b10db-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="b10db-107">Arguments</span></span>

<span data-ttu-id="b10db-108">`condition range`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="b10db-108">`condition range`: *String*</span></span>

<span data-ttu-id="b10db-109">Значение, возвращаемое выражением, настроенное в свойстве **Имя ключа собранных данных** компонента формата электронной отчетности (ER).</span><span class="sxs-lookup"><span data-stu-id="b10db-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span>

<span data-ttu-id="b10db-110">`condition value`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="b10db-110">`condition value`: *String*</span></span>

<span data-ttu-id="b10db-111">Значение, возвращаемое выражением, настроенное в свойстве **Значение ключа собранных данных** компонента формата ER.</span><span class="sxs-lookup"><span data-stu-id="b10db-111">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span>

## <a name="return-values"></a><span data-ttu-id="b10db-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="b10db-112">Return values</span></span>

<span data-ttu-id="b10db-113">*Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="b10db-113">*Integer*</span></span>

<span data-ttu-id="b10db-114">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="b10db-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b10db-115">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="b10db-115">Usage notes</span></span>

<span data-ttu-id="b10db-116">Свойства **Имя ключа собранных данных** и **Значение ключа собранных данных** могут быть настроены как для компонента **Последовательность**, так и для компонента **Элемент XML** в формате ER, который находится в компоненте **Common\\File**, где включен параметр **Сбор сведений о результате**.</span><span class="sxs-lookup"><span data-stu-id="b10db-116">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="b10db-117">Эта функция возвращает значение **0** (ноль), когда параметр **Сбор сведений о результате** для текущего компонента **Common\\File** выключен.</span><span class="sxs-lookup"><span data-stu-id="b10db-117">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="b10db-118">В аргументе `condition range` подстановочный знак **"\*"** может быть использован для представления нескольких символов.</span><span class="sxs-lookup"><span data-stu-id="b10db-118">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="b10db-119">В аргументе `condition value` подстановочный знак **"\*"** может быть использован для представления нескольких символов.</span><span class="sxs-lookup"><span data-stu-id="b10db-119">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="b10db-120">Пример</span><span class="sxs-lookup"><span data-stu-id="b10db-120">Example</span></span>

<span data-ttu-id="b10db-121">Для получения дополнительных сведений об использовании этой функции см. проводник по задаче [ER Использование выходных данных формата для инвентаризации и агрегирования](tasks/er-format-counting-summing-1.md), который является частью бизнес-процесса **Приобретение/разработка компонентов ИТ-услуг и решений**.</span><span class="sxs-lookup"><span data-stu-id="b10db-121">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b10db-122">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b10db-122">Additional resources</span></span>

[<span data-ttu-id="b10db-123">Функции сбора данных</span><span class="sxs-lookup"><span data-stu-id="b10db-123">Data collection functions</span></span>](er-functions-category-data-collection.md)
