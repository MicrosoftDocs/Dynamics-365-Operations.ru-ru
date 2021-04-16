---
title: Функция ER UPPER
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности UPPER.
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
ms.openlocfilehash: 0e0e9837765914c657a72c5ce04c6f565fa13788
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749149"
---
# <a name="upper-er-function"></a><span data-ttu-id="71931-103">Функция ER UPPER</span><span class="sxs-lookup"><span data-stu-id="71931-103">UPPER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71931-104">Функция `UPPER` возвращает указанную строку текста в качестве *строкового* значения после того, как она была преобразована в буквы верхнего регистра.</span><span class="sxs-lookup"><span data-stu-id="71931-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="71931-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71931-105">Syntax</span></span>

```vb
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="71931-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="71931-106">Arguments</span></span>

<span data-ttu-id="71931-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="71931-107">`text`: *String*</span></span>

<span data-ttu-id="71931-108">Действительный путь источника данных типа *Строка*.</span><span class="sxs-lookup"><span data-stu-id="71931-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="71931-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="71931-109">Return values</span></span>

<span data-ttu-id="71931-110">*Строка*</span><span class="sxs-lookup"><span data-stu-id="71931-110">*String*</span></span>

<span data-ttu-id="71931-111">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="71931-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="71931-112">Пример</span><span class="sxs-lookup"><span data-stu-id="71931-112">Example</span></span>

<span data-ttu-id="71931-113">`UPPER ("Sample")` возвращает **"SAMPLE"**.</span><span class="sxs-lookup"><span data-stu-id="71931-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="71931-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="71931-114">Additional resources</span></span>

[<span data-ttu-id="71931-115">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="71931-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]