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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 24a295a6ad8aca7718e60dd351248c9fbfdafee8
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042328"
---
# <span data-ttu-id="be1ca-103"><a name="NULLDATE">Функция ER NULLDATE</a></span><span class="sxs-lookup"><span data-stu-id="be1ca-103"><a name="NULLDATE">NULLDATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be1ca-104">Функция `NULLDATE` возвращает значение *Date*, которое представляет **нулевую** дату (1 января 1900 года).</span><span class="sxs-lookup"><span data-stu-id="be1ca-104">The `NULLDATE` function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span>

## <a name="syntax"></a><span data-ttu-id="be1ca-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be1ca-105">Syntax</span></span>

```vb
NULLDATE () as 
```

## <a name="return-values"></a><span data-ttu-id="be1ca-106">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="be1ca-106">Return values</span></span>

<span data-ttu-id="be1ca-107">*Дата*</span><span class="sxs-lookup"><span data-stu-id="be1ca-107">*Date*</span></span>

<span data-ttu-id="be1ca-108">Результирующее значение даты.</span><span class="sxs-lookup"><span data-stu-id="be1ca-108">The resulting date value.</span></span>

## <a name="example-1"></a><span data-ttu-id="be1ca-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="be1ca-109">Example 1</span></span>

<span data-ttu-id="be1ca-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` возвращает **нулевую** дату, 1 января 1900 года, как **"1900-01-01"**, на основе указанного пользовательского формата.</span><span class="sxs-lookup"><span data-stu-id="be1ca-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returns the **null** date, January 1, 1900, as **"1900-01-01"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="be1ca-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="be1ca-111">Example 2</span></span>

<span data-ttu-id="be1ca-112">Выражение `IF( Invoice.DocumentDate = NULLDATE(), true, false)` возвращает **True**, когда значение поля **DocumentDate** равняется **нулевой** дате.</span><span class="sxs-lookup"><span data-stu-id="be1ca-112">The expression `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returns **True** when the value of the **DocumentDate** field equals the **null** date.</span></span> <span data-ttu-id="be1ca-113">В этом примере **Invoice** представляет собой источник данных электронной отчетности (ER) типа **Записи Finance/Table** и ссылается на таблицу CustInvoiceJour.</span><span class="sxs-lookup"><span data-stu-id="be1ca-113">In this example, **Invoice** is an Electronic reporting (ER) data source of the **Finance/Table records** type, and it refers to the CustInvoiceJour table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="be1ca-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="be1ca-114">Additional resources</span></span>

[<span data-ttu-id="be1ca-115">Функции даты и времени</span><span class="sxs-lookup"><span data-stu-id="be1ca-115">Date and time functions</span></span>](er-functions-category-datetime.md)
