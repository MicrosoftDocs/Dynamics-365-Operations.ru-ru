---
title: Функция ER FIRSTORNULL
description: Этот раздел объясняет способ использования функции электронной отчетности FIRSTORNULL.
author: NickSelin
ms.date: 11/29/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 1ccc094fc468470ffc857c729b6d8402796785d7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753224"
---
# <a name="firstornull-er-function"></a><span data-ttu-id="98507-103">Функция ER FIRSTORNULL</span><span class="sxs-lookup"><span data-stu-id="98507-103">FIRSTORNULL ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98507-104">Функция `FIRSTORNULL` возвращает первую запись указанного списка в виде значения *Контейнер (запись)*, если эта запись не пуста.</span><span class="sxs-lookup"><span data-stu-id="98507-104">The `FIRSTORNULL` function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="98507-105">Если запись пуста, эта функция возвращает нулевое значение *Контейнер (запись)*.</span><span class="sxs-lookup"><span data-stu-id="98507-105">If the record is empty, this function returns a null *Container (record)* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="98507-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98507-106">Syntax</span></span>

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a><span data-ttu-id="98507-107">Аргументы</span><span class="sxs-lookup"><span data-stu-id="98507-107">Arguments</span></span>

<span data-ttu-id="98507-108">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="98507-108">`list`: *Record list*</span></span>

<span data-ttu-id="98507-109">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="98507-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="98507-110">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="98507-110">Return values</span></span>

<span data-ttu-id="98507-111">*Контейнер (запись)*</span><span class="sxs-lookup"><span data-stu-id="98507-111">*Container (record)*</span></span>

<span data-ttu-id="98507-112">Результирующее значение записи.</span><span class="sxs-lookup"><span data-stu-id="98507-112">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="98507-113">Пример</span><span class="sxs-lookup"><span data-stu-id="98507-113">Example</span></span>

<span data-ttu-id="98507-114">Выражение `FIRSTORNULL(SPLIT("",1)).Value` возвращает пустую строку (**""**).</span><span class="sxs-lookup"><span data-stu-id="98507-114">The expression `FIRSTORNULL(SPLIT("",1)).Value` returns an empty string (**""**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="98507-115">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="98507-115">Additional resources</span></span>

[<span data-ttu-id="98507-116">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="98507-116">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]