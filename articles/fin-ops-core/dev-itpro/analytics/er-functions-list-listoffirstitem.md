---
title: Функция ER LISTOFFIRSTITEM
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности LISTOFFIRSTITEM.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 6dd6c84b43bea36bf922ae9348f95b450e882832
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750188"
---
# <a name="listoffirstitem-er-function"></a><span data-ttu-id="d6d44-103">Функция ER LISTOFFIRSTITEM</span><span class="sxs-lookup"><span data-stu-id="d6d44-103">LISTOFFIRSTITEM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d6d44-104">Функция `LISTOFFIRSTITEM` возвращает значение *Список записей*, состоящее только из первой записи указанного списка.</span><span class="sxs-lookup"><span data-stu-id="d6d44-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6d44-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d6d44-105">Syntax</span></span>

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="d6d44-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="d6d44-106">Arguments</span></span>

<span data-ttu-id="d6d44-107">`list`: *Список записей*</span><span class="sxs-lookup"><span data-stu-id="d6d44-107">`list`: *Record list*</span></span>

<span data-ttu-id="d6d44-108">Действительный путь источника данных типа данных *Список записей*.</span><span class="sxs-lookup"><span data-stu-id="d6d44-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="d6d44-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="d6d44-109">Return values</span></span>

<span data-ttu-id="d6d44-110">*Список записей*</span><span class="sxs-lookup"><span data-stu-id="d6d44-110">*Record list*</span></span>

<span data-ttu-id="d6d44-111">Полученный список записей.</span><span class="sxs-lookup"><span data-stu-id="d6d44-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="d6d44-112">Пример</span><span class="sxs-lookup"><span data-stu-id="d6d44-112">Example</span></span>

<span data-ttu-id="d6d44-113">Выражение `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` возвращает значение текста **"A"**.</span><span class="sxs-lookup"><span data-stu-id="d6d44-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d6d44-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d6d44-114">Additional resources</span></span>

[<span data-ttu-id="d6d44-115">Функции для работы со списками</span><span class="sxs-lookup"><span data-stu-id="d6d44-115">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]