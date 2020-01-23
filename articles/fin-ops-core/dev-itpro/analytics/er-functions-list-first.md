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
ms.openlocfilehash: 211891a0ad5dc6152ce8d980bcd40a9a6bc7e3e6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917358"
---
# <span data-ttu-id="8ec17-103"><a name="FIRST">Функция ER FIRST</a></span><span class="sxs-lookup"><span data-stu-id="8ec17-103"><a name="FIRST">FIRST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ec17-104">Функция `FIRST` возвращает первую запись указанного списка в виде значения *Контейнер (запись)*, если этот список не пуст.</span><span class="sxs-lookup"><span data-stu-id="8ec17-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="8ec17-105">Если список пуст, эта функция выдает исключение.</span><span class="sxs-lookup"><span data-stu-id="8ec17-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ec17-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ec17-106">Syntax</span></span>

```
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="8ec17-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="8ec17-107">Arguments</span></span>

<span data-ttu-id="8ec17-108">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="8ec17-108">`list`: *Record list*</span></span>

<span data-ttu-id="8ec17-109">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="8ec17-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="8ec17-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="8ec17-110">Return values</span></span>

<span data-ttu-id="8ec17-111">*Контейнер (запись)*</span><span class="sxs-lookup"><span data-stu-id="8ec17-111">*Container (record)*</span></span>

<span data-ttu-id="8ec17-112">Результирующее значение записи.</span><span class="sxs-lookup"><span data-stu-id="8ec17-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="8ec17-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8ec17-113">Example 1</span></span>

<span data-ttu-id="8ec17-114">Выражение `FIRST(SPLIT("ABC",1)).Value` возвращает значение текста **"A"**.</span><span class="sxs-lookup"><span data-stu-id="8ec17-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="8ec17-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8ec17-115">Example 2</span></span>

<span data-ttu-id="8ec17-116">Выражение `FIRST(SPLIT("",1)).Value` выдает исключение во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="8ec17-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8ec17-117">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8ec17-117">Additional resources</span></span>

[<span data-ttu-id="8ec17-118">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="8ec17-118">List functions</span></span>](er-functions-category-list.md)
