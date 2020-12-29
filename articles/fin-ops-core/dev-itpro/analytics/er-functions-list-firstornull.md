---
title: Функция ER FIRSTORNULL
description: Этот раздел объясняет способ использования функции электронной отчетности FIRSTORNULL.
author: NickSelin
manager: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: 3547eeea3c6fef5cca0699002cc0c35cffd940b3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688051"
---
# <a name="firstornull-er-function"></a><span data-ttu-id="18302-103">Функция ER FIRSTORNULL</span><span class="sxs-lookup"><span data-stu-id="18302-103">FIRSTORNULL ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="18302-104">Функция `FIRSTORNULL` возвращает первую запись указанного списка в виде значения *Контейнер (запись)*, если эта запись не пуста.</span><span class="sxs-lookup"><span data-stu-id="18302-104">The `FIRSTORNULL` function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="18302-105">Если запись пуста, эта функция возвращает нулевое значение *Контейнер (запись)*.</span><span class="sxs-lookup"><span data-stu-id="18302-105">If the record is empty, this function returns a null *Container (record)* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="18302-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18302-106">Syntax</span></span>

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a><span data-ttu-id="18302-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="18302-107">Arguments</span></span>

<span data-ttu-id="18302-108">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="18302-108">`list`: *Record list*</span></span>

<span data-ttu-id="18302-109">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="18302-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="18302-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="18302-110">Return values</span></span>

<span data-ttu-id="18302-111">*Контейнер (запись)*</span><span class="sxs-lookup"><span data-stu-id="18302-111">*Container (record)*</span></span>

<span data-ttu-id="18302-112">Результирующее значение записи.</span><span class="sxs-lookup"><span data-stu-id="18302-112">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="18302-113">Пример</span><span class="sxs-lookup"><span data-stu-id="18302-113">Example</span></span>

<span data-ttu-id="18302-114">Выражение `FIRSTORNULL(SPLIT("",1)).Value` возвращает пустую строку (**""**).</span><span class="sxs-lookup"><span data-stu-id="18302-114">The expression `FIRSTORNULL(SPLIT("",1)).Value` returns an empty string (**""**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="18302-115">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="18302-115">Additional resources</span></span>

[<span data-ttu-id="18302-116">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="18302-116">List functions</span></span>](er-functions-category-list.md)
