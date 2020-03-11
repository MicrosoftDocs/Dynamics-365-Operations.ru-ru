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
ms.openlocfilehash: 4d10abcf15b93961bd2ba4aec22914825d9ac38c
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042098"
---
# <span data-ttu-id="9dee8-103"><a name="FIRST">Функция ER FIRST</a></span><span class="sxs-lookup"><span data-stu-id="9dee8-103"><a name="FIRST">FIRST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9dee8-104">Функция `FIRST` возвращает первую запись указанного списка в виде значения *Контейнер (запись)*, если этот список не пуст.</span><span class="sxs-lookup"><span data-stu-id="9dee8-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="9dee8-105">Если список пуст, эта функция выдает исключение.</span><span class="sxs-lookup"><span data-stu-id="9dee8-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dee8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9dee8-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="9dee8-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="9dee8-107">Arguments</span></span>

<span data-ttu-id="9dee8-108">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="9dee8-108">`list`: *Record list*</span></span>

<span data-ttu-id="9dee8-109">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="9dee8-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="9dee8-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="9dee8-110">Return values</span></span>

<span data-ttu-id="9dee8-111">*Контейнер (запись)*</span><span class="sxs-lookup"><span data-stu-id="9dee8-111">*Container (record)*</span></span>

<span data-ttu-id="9dee8-112">Результирующее значение записи.</span><span class="sxs-lookup"><span data-stu-id="9dee8-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="9dee8-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9dee8-113">Example 1</span></span>

<span data-ttu-id="9dee8-114">Выражение `FIRST(SPLIT("ABC",1)).Value` возвращает значение текста **"A"**.</span><span class="sxs-lookup"><span data-stu-id="9dee8-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="9dee8-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9dee8-115">Example 2</span></span>

<span data-ttu-id="9dee8-116">Выражение `FIRST(SPLIT("",1)).Value` выдает исключение во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="9dee8-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9dee8-117">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9dee8-117">Additional resources</span></span>

[<span data-ttu-id="9dee8-118">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="9dee8-118">List functions</span></span>](er-functions-category-list.md)
