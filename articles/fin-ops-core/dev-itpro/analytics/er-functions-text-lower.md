---
title: Функция ER LOWER
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности LOWER.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 6784384bac31d8c7cdc9c6f71b7dbab79c15a934
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041109"
---
# <span data-ttu-id="dd593-103"><a name="LOWER">Функция ER LOWER</a></span><span class="sxs-lookup"><span data-stu-id="dd593-103"><a name="LOWER">LOWER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dd593-104">Функция `LOWER` возвращает указанную строку текста в качестве *строкового* значения после того, как она была преобразована в буквы нижнего регистра.</span><span class="sxs-lookup"><span data-stu-id="dd593-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd593-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd593-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="dd593-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="dd593-106">Arguments</span></span>

<span data-ttu-id="dd593-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="dd593-107">`text`: *String*</span></span>

<span data-ttu-id="dd593-108">*Строковое* значение, задающее текст.</span><span class="sxs-lookup"><span data-stu-id="dd593-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="dd593-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="dd593-109">Return values</span></span>

<span data-ttu-id="dd593-110">*Строка*</span><span class="sxs-lookup"><span data-stu-id="dd593-110">*String*</span></span>

<span data-ttu-id="dd593-111">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="dd593-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="dd593-112">Пример</span><span class="sxs-lookup"><span data-stu-id="dd593-112">Example</span></span>

<span data-ttu-id="dd593-113">`LOWER ("Sample")` возвращает **"sample"**.</span><span class="sxs-lookup"><span data-stu-id="dd593-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dd593-114">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="dd593-114">Additional resources</span></span>

[<span data-ttu-id="dd593-115">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="dd593-115">Text functions</span></span>](er-functions-category-text.md)
