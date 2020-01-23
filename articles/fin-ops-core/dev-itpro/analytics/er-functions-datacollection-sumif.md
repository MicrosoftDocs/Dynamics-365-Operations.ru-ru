---
title: Функция ER SUMIF
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности SUMIF.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 579b14c713bc5f9831c5e012d16bb3b6f97b1035
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916438"
---
# <span data-ttu-id="8b3db-103"><a name="SUMIF">Функция ER SUMIF</a></span><span class="sxs-lookup"><span data-stu-id="8b3db-103"><a name="SUMIF">SUMIF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8b3db-104">Функция `SUMIF` возвращает *вещественное* значение, представляющее сумму значений, которые были возвращены привязками элементов формата и собраны во время использования для создания исходящего документа во время выполнения формата, и удовлетворяющее указанному условию.</span><span class="sxs-lookup"><span data-stu-id="8b3db-104">The `SUMIF` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="8b3db-105">Условие состоит из диапазона ключей и значения ключа.</span><span class="sxs-lookup"><span data-stu-id="8b3db-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b3db-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b3db-106">Syntax</span></span>

```
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="8b3db-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="8b3db-107">Arguments</span></span>

<span data-ttu-id="8b3db-108">`key name for summing`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="8b3db-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="8b3db-109">Значение, возвращаемое выражением, настроенным в свойстве **Имя ключа собранных данных** компонента формата электронной отчетности (ER), для которого значение привязки должно использоваться для целей суммирования.</span><span class="sxs-lookup"><span data-stu-id="8b3db-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="8b3db-110">Свойство **Значение ключа собранных данных** можно настроить как для компонента **Последовательность**, так и для компонента **Элемент XML** в формате ER, который находится в компоненте **Common\\File**, где включен параметр **Сбор сведений о результате**.</span><span class="sxs-lookup"><span data-stu-id="8b3db-110">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="8b3db-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="8b3db-111">Return values</span></span>

<span data-ttu-id="8b3db-112">*Действующий*</span><span class="sxs-lookup"><span data-stu-id="8b3db-112">*Real*</span></span>

<span data-ttu-id="8b3db-113">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="8b3db-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8b3db-114">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="8b3db-114">Usage notes</span></span>

<span data-ttu-id="8b3db-115">Эта функция возвращает значение **0** (ноль), когда параметр **Сбор сведений о результате** для текущего компонента **Common\\File** выключен.</span><span class="sxs-lookup"><span data-stu-id="8b3db-115">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="8b3db-116">В аргументе `condition range` подстановочный знак **"\*"** может быть использован для представления нескольких символов.</span><span class="sxs-lookup"><span data-stu-id="8b3db-116">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="8b3db-117">В аргументе `condition value` подстановочный знак **"\*"** может быть использован для представления нескольких символов.</span><span class="sxs-lookup"><span data-stu-id="8b3db-117">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="8b3db-118">Пример</span><span class="sxs-lookup"><span data-stu-id="8b3db-118">Example</span></span>

<span data-ttu-id="8b3db-119">Для получения дополнительных сведений об использовании этой функции см. проводник по задаче [ER Использование выходных данных формата для инвентаризации и агрегирования](tasks/er-format-counting-summing-1.md), который является частью бизнес-процесса **Приобретение/разработка компонентов ИТ-услуг и решений**.</span><span class="sxs-lookup"><span data-stu-id="8b3db-119">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8b3db-120">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8b3db-120">Additional resources</span></span>

[<span data-ttu-id="8b3db-121">Функции сбора данных</span><span class="sxs-lookup"><span data-stu-id="8b3db-121">Data collection functions</span></span>](er-functions-category-data-collection.md)
