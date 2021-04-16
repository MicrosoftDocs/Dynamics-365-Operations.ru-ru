---
title: Функция ER TRIM
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности TRIM
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 93b08792a7aab7245d0443da05e0330bf8b2d56e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746057"
---
# <a name="trim-er-function"></a><span data-ttu-id="66c76-103">Функция ER TRIM</span><span class="sxs-lookup"><span data-stu-id="66c76-103">TRIM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="66c76-104">Функция `TRIM` возвращает указанную текстовую строку в качестве *строкового* значения после удаления начальных и конечных пробелов и после преобразования нескольких пробелов между словами в одинарные пробелы.</span><span class="sxs-lookup"><span data-stu-id="66c76-104">The `TRIM` function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="66c76-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66c76-105">Syntax</span></span>

```vb
TRIM (text )
```

## <a name="arguments"></a><span data-ttu-id="66c76-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="66c76-106">Arguments</span></span>

<span data-ttu-id="66c76-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="66c76-107">`text`: *String*</span></span>

<span data-ttu-id="66c76-108">Действительный путь источника данных типа *Строка*.</span><span class="sxs-lookup"><span data-stu-id="66c76-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="66c76-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="66c76-109">Return values</span></span>

<span data-ttu-id="66c76-110">*Строка*</span><span class="sxs-lookup"><span data-stu-id="66c76-110">*String*</span></span>

<span data-ttu-id="66c76-111">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="66c76-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="66c76-112">Пример</span><span class="sxs-lookup"><span data-stu-id="66c76-112">Example</span></span>

<span data-ttu-id="66c76-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` возвращает **"Sample text"**.</span><span class="sxs-lookup"><span data-stu-id="66c76-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returns **"Sample text"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="66c76-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="66c76-114">Additional resources</span></span>

[<span data-ttu-id="66c76-115">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="66c76-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]