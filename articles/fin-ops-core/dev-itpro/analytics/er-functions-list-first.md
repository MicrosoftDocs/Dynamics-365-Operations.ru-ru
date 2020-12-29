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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a5c52d3f999b4c6fbdea0685977ab13fca1e8ffb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679422"
---
# <a name="first-er-function"></a><span data-ttu-id="ca5fe-103">Функция ER FIRST</span><span class="sxs-lookup"><span data-stu-id="ca5fe-103">FIRST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca5fe-104">Функция `FIRST` возвращает первую запись указанного списка в виде значения *Контейнер (запись)*, если этот список не пуст.</span><span class="sxs-lookup"><span data-stu-id="ca5fe-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="ca5fe-105">Если список пуст, эта функция выдает исключение.</span><span class="sxs-lookup"><span data-stu-id="ca5fe-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca5fe-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca5fe-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="ca5fe-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="ca5fe-107">Arguments</span></span>

<span data-ttu-id="ca5fe-108">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="ca5fe-108">`list`: *Record list*</span></span>

<span data-ttu-id="ca5fe-109">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="ca5fe-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="ca5fe-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ca5fe-110">Return values</span></span>

<span data-ttu-id="ca5fe-111">*Контейнер (запись)*</span><span class="sxs-lookup"><span data-stu-id="ca5fe-111">*Container (record)*</span></span>

<span data-ttu-id="ca5fe-112">Результирующее значение записи.</span><span class="sxs-lookup"><span data-stu-id="ca5fe-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="ca5fe-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ca5fe-113">Example 1</span></span>

<span data-ttu-id="ca5fe-114">Выражение `FIRST(SPLIT("ABC",1)).Value` возвращает значение текста **"A"**.</span><span class="sxs-lookup"><span data-stu-id="ca5fe-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="ca5fe-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ca5fe-115">Example 2</span></span>

<span data-ttu-id="ca5fe-116">Выражение `FIRST(SPLIT("",1)).Value` выдает исключение во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="ca5fe-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ca5fe-117">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ca5fe-117">Additional resources</span></span>

[<span data-ttu-id="ca5fe-118">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="ca5fe-118">List functions</span></span>](er-functions-category-list.md)
