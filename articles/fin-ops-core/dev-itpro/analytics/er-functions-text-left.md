---
title: Функция ER LEFT
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности LEFT
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 6f1ec7a21a16c3a34bed9779b05f20f21815ab9d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570000"
---
# <a name="left-er-function"></a><span data-ttu-id="1cb87-103">Функция ER LEFT</span><span class="sxs-lookup"><span data-stu-id="1cb87-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1cb87-104">Функция `LEFT` возвращает *строковое* значение, которое представляет указанное число символов от начала указанной строки.</span><span class="sxs-lookup"><span data-stu-id="1cb87-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cb87-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1cb87-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="1cb87-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="1cb87-106">Arguments</span></span>

<span data-ttu-id="1cb87-107">`text`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="1cb87-107">`text`: *String*</span></span>

<span data-ttu-id="1cb87-108">*Строковое* значение, представляющее исходный текст.</span><span class="sxs-lookup"><span data-stu-id="1cb87-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="1cb87-109">`number`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="1cb87-109">`number`: *Integer*</span></span>

<span data-ttu-id="1cb87-110">Количество символов, которые должны быть возвращены с начала исходного текста.</span><span class="sxs-lookup"><span data-stu-id="1cb87-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="1cb87-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="1cb87-111">Return values</span></span>

<span data-ttu-id="1cb87-112">*Строка*</span><span class="sxs-lookup"><span data-stu-id="1cb87-112">*String*</span></span>

<span data-ttu-id="1cb87-113">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="1cb87-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="1cb87-114">Пример</span><span class="sxs-lookup"><span data-stu-id="1cb87-114">Example</span></span>

<span data-ttu-id="1cb87-115">`LEFT ("Sample", 3)` возвращает **"Sam"**.</span><span class="sxs-lookup"><span data-stu-id="1cb87-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1cb87-116">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1cb87-116">Additional resources</span></span>

[<span data-ttu-id="1cb87-117">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="1cb87-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]