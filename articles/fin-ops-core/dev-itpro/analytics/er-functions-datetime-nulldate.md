---
title: Функция ER NULLDATE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности NULLDATE.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 327a06ab7657c334338073f67cb244cc40bfee31
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682325"
---
# <a name="nulldate-er-function"></a><span data-ttu-id="aa0f2-103">Функция ER NULLDATE</span><span class="sxs-lookup"><span data-stu-id="aa0f2-103">NULLDATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa0f2-104">Функция `NULLDATE` возвращает значение *Date*, которое представляет **нулевую** дату (1 января 1900 года).</span><span class="sxs-lookup"><span data-stu-id="aa0f2-104">The `NULLDATE` function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span>

## <a name="syntax"></a><span data-ttu-id="aa0f2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aa0f2-105">Syntax</span></span>

```vb
NULLDATE () as 
```

## <a name="return-values"></a><span data-ttu-id="aa0f2-106">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="aa0f2-106">Return values</span></span>

<span data-ttu-id="aa0f2-107">*Дата*</span><span class="sxs-lookup"><span data-stu-id="aa0f2-107">*Date*</span></span>

<span data-ttu-id="aa0f2-108">Результирующее значение даты.</span><span class="sxs-lookup"><span data-stu-id="aa0f2-108">The resulting date value.</span></span>

## <a name="example-1"></a><span data-ttu-id="aa0f2-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aa0f2-109">Example 1</span></span>

<span data-ttu-id="aa0f2-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` возвращает **нулевую** дату, 1 января 1900 года, как **"1900-01-01"**, на основе указанного пользовательского формата.</span><span class="sxs-lookup"><span data-stu-id="aa0f2-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returns the **null** date, January 1, 1900, as **"1900-01-01"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="aa0f2-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="aa0f2-111">Example 2</span></span>

<span data-ttu-id="aa0f2-112">Выражение `IF( Invoice.DocumentDate = NULLDATE(), true, false)` возвращает **True**, когда значение поля **DocumentDate** равняется **нулевой** дате.</span><span class="sxs-lookup"><span data-stu-id="aa0f2-112">The expression `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returns **True** when the value of the **DocumentDate** field equals the **null** date.</span></span> <span data-ttu-id="aa0f2-113">В этом примере **Invoice** представляет собой источник данных электронной отчетности (ER) типа **Записи Finance/Table** и ссылается на таблицу CustInvoiceJour.</span><span class="sxs-lookup"><span data-stu-id="aa0f2-113">In this example, **Invoice** is an Electronic reporting (ER) data source of the **Finance/Table records** type, and it refers to the CustInvoiceJour table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aa0f2-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="aa0f2-114">Additional resources</span></span>

[<span data-ttu-id="aa0f2-115">Функции даты и времени</span><span class="sxs-lookup"><span data-stu-id="aa0f2-115">Date and time functions</span></span>](er-functions-category-datetime.md)
