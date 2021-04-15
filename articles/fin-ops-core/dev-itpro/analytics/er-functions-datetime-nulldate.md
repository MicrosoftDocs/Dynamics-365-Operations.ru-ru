---
title: Функция ER NULLDATE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности NULLDATE.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 6ac8da3f18c7793512685d52dd64a9bd55bfb8fc
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746851"
---
# <a name="nulldate-er-function"></a><span data-ttu-id="1ff5c-103">Функция ER NULLDATE</span><span class="sxs-lookup"><span data-stu-id="1ff5c-103">NULLDATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ff5c-104">Функция `NULLDATE` возвращает значение *Date*, которое представляет **нулевую** дату (1 января 1900 года).</span><span class="sxs-lookup"><span data-stu-id="1ff5c-104">The `NULLDATE` function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span>

## <a name="syntax"></a><span data-ttu-id="1ff5c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ff5c-105">Syntax</span></span>

```vb
NULLDATE () as 
```

## <a name="return-values"></a><span data-ttu-id="1ff5c-106">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="1ff5c-106">Return values</span></span>

<span data-ttu-id="1ff5c-107">*Дата*</span><span class="sxs-lookup"><span data-stu-id="1ff5c-107">*Date*</span></span>

<span data-ttu-id="1ff5c-108">Результирующее значение даты.</span><span class="sxs-lookup"><span data-stu-id="1ff5c-108">The resulting date value.</span></span>

## <a name="example-1"></a><span data-ttu-id="1ff5c-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1ff5c-109">Example 1</span></span>

<span data-ttu-id="1ff5c-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` возвращает **нулевую** дату, 1 января 1900 года, как **"1900-01-01"**, на основе указанного пользовательского формата.</span><span class="sxs-lookup"><span data-stu-id="1ff5c-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returns the **null** date, January 1, 1900, as **"1900-01-01"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="1ff5c-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1ff5c-111">Example 2</span></span>

<span data-ttu-id="1ff5c-112">Выражение `IF( Invoice.DocumentDate = NULLDATE(), true, false)` возвращает **True**, когда значение поля **DocumentDate** равняется **нулевой** дате.</span><span class="sxs-lookup"><span data-stu-id="1ff5c-112">The expression `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returns **True** when the value of the **DocumentDate** field equals the **null** date.</span></span> <span data-ttu-id="1ff5c-113">В этом примере **Invoice** представляет собой источник данных электронной отчетности (ER) типа **Записи Finance/Table** и ссылается на таблицу CustInvoiceJour.</span><span class="sxs-lookup"><span data-stu-id="1ff5c-113">In this example, **Invoice** is an Electronic reporting (ER) data source of the **Finance/Table records** type, and it refers to the CustInvoiceJour table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1ff5c-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1ff5c-114">Additional resources</span></span>

[<span data-ttu-id="1ff5c-115">Функции даты и времени</span><span class="sxs-lookup"><span data-stu-id="1ff5c-115">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]