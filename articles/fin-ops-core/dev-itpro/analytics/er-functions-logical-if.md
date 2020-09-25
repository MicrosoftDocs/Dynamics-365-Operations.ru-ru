---
title: Функция ER IF
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности IF.
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
ms.openlocfilehash: 87e252a2751beeecb51e512cae38b271c1456fae
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744703"
---
# <a name="if-er-function"></a><span data-ttu-id="0f661-103">Функция ER IF</span><span class="sxs-lookup"><span data-stu-id="0f661-103">IF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f661-104">Функция `IF` возвращает первое указанное значение, если выполняется указанное условие.</span><span class="sxs-lookup"><span data-stu-id="0f661-104">The `IF` function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="0f661-105">В противном случае возвращает второе указанное значение.</span><span class="sxs-lookup"><span data-stu-id="0f661-105">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="0f661-106">Возвращаемое значение может быть значением любого из поддерживаемых типов данных.</span><span class="sxs-lookup"><span data-stu-id="0f661-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f661-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f661-107">Syntax</span></span>

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a><span data-ttu-id="0f661-108">Аргументы</span><span class="sxs-lookup"><span data-stu-id="0f661-108">Arguments</span></span>

<span data-ttu-id="0f661-109">`condition`: *Логический*</span><span class="sxs-lookup"><span data-stu-id="0f661-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="0f661-110">Действительное условное выражение, которое должно быть протестировано.</span><span class="sxs-lookup"><span data-stu-id="0f661-110">A valid conditional expression that must be tested.</span></span>

<span data-ttu-id="0f661-111">`first value`: *Любой из поддерживаемых типов данных*</span><span class="sxs-lookup"><span data-stu-id="0f661-111">`first value`: *Any of the supported data types*</span></span>

<span data-ttu-id="0f661-112">Результат, который возвращается при выполнении условия.</span><span class="sxs-lookup"><span data-stu-id="0f661-112">The result that is returned if the condition is met.</span></span>

<span data-ttu-id="0f661-113">`second value`: *Любой из поддерживаемых типов данных*</span><span class="sxs-lookup"><span data-stu-id="0f661-113">`second value`: *Any of the supported data types*</span></span>

<span data-ttu-id="0f661-114">Результат, который возвращается при невыполнении условия.</span><span class="sxs-lookup"><span data-stu-id="0f661-114">The result that is returned if the condition isn't met.</span></span>

## <a name="return-values"></a><span data-ttu-id="0f661-115">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="0f661-115">Return values</span></span>

<span data-ttu-id="0f661-116">*Любой из поддерживаемых типов данных*</span><span class="sxs-lookup"><span data-stu-id="0f661-116">*Any of the supported data types*</span></span>

<span data-ttu-id="0f661-117">Полученное значение любого из поддерживаемых типов данных.</span><span class="sxs-lookup"><span data-stu-id="0f661-117">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0f661-118">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="0f661-118">Usage notes</span></span>

<span data-ttu-id="0f661-119">Аргументы `first value` и `second value` должны быть указаны с помощью одного и того же типа данных.</span><span class="sxs-lookup"><span data-stu-id="0f661-119">The `first value` and `second value` arguments must be specified by using the same data type.</span></span> <span data-ttu-id="0f661-120">Исключение выдается во время разработки, если типы данных настроенных значений не совпадают.</span><span class="sxs-lookup"><span data-stu-id="0f661-120">An exception is thrown at design time if the data types of the configured values don't match.</span></span>

<span data-ttu-id="0f661-121">Если первое значение и второе значение являются значениями типа данных *Контейнер (запись)* или *Список записей*, то в результате есть только поля, которые существуют в обоих значениях.</span><span class="sxs-lookup"><span data-stu-id="0f661-121">If the first value and the second value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="0f661-122">Пример</span><span class="sxs-lookup"><span data-stu-id="0f661-122">Example</span></span>

<span data-ttu-id="0f661-123">`IF (1=2, "condition is met", "condition is not met")` возвращает строку **"условие не выполняется"**.</span><span class="sxs-lookup"><span data-stu-id="0f661-123">`IF (1=2, "condition is met", "condition is not met")` returns the string **"condition is not met"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0f661-124">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0f661-124">Additional resources</span></span>

[<span data-ttu-id="0f661-125">Логические функции</span><span class="sxs-lookup"><span data-stu-id="0f661-125">Logical functions</span></span>](er-functions-category-logical.md)
