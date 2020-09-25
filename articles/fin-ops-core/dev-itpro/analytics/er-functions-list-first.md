---
title: Функция ER FIRST
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности FIRST.
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
ms.openlocfilehash: 3ed0e0aaf29e2a67a4842d71121f1adc24f524f7
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745233"
---
# <a name="first-er-function"></a><span data-ttu-id="e9ac0-103">Функция ER FIRST</span><span class="sxs-lookup"><span data-stu-id="e9ac0-103">FIRST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e9ac0-104">Функция `FIRST` возвращает первую запись указанного списка в виде значения *Контейнер (запись)*, если этот список не пуст.</span><span class="sxs-lookup"><span data-stu-id="e9ac0-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="e9ac0-105">Если список пуст, эта функция выдает исключение.</span><span class="sxs-lookup"><span data-stu-id="e9ac0-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9ac0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9ac0-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="e9ac0-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="e9ac0-107">Arguments</span></span>

<span data-ttu-id="e9ac0-108">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="e9ac0-108">`list`: *Record list*</span></span>

<span data-ttu-id="e9ac0-109">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="e9ac0-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="e9ac0-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="e9ac0-110">Return values</span></span>

<span data-ttu-id="e9ac0-111">*Контейнер (запись)*</span><span class="sxs-lookup"><span data-stu-id="e9ac0-111">*Container (record)*</span></span>

<span data-ttu-id="e9ac0-112">Результирующее значение записи.</span><span class="sxs-lookup"><span data-stu-id="e9ac0-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="e9ac0-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e9ac0-113">Example 1</span></span>

<span data-ttu-id="e9ac0-114">Выражение `FIRST(SPLIT("ABC",1)).Value` возвращает значение текста **"A"**.</span><span class="sxs-lookup"><span data-stu-id="e9ac0-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="e9ac0-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e9ac0-115">Example 2</span></span>

<span data-ttu-id="e9ac0-116">Выражение `FIRST(SPLIT("",1)).Value` выдает исключение во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="e9ac0-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e9ac0-117">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e9ac0-117">Additional resources</span></span>

[<span data-ttu-id="e9ac0-118">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="e9ac0-118">List functions</span></span>](er-functions-category-list.md)
