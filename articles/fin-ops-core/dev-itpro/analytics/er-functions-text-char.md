---
title: Функция ER CHAR
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности CHAR
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: a9f0f70c250592bf74b1a1df823e66803e853a64
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682999"
---
# <a name="char-er-function"></a><span data-ttu-id="11200-103">Функция ER CHAR</span><span class="sxs-lookup"><span data-stu-id="11200-103">CHAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11200-104">Функция `CHAR` возвращает *строковое* значение, которое представляет один символ, на который ссылается указанный номер Unicode.</span><span class="sxs-lookup"><span data-stu-id="11200-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="11200-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11200-105">Syntax</span></span>

```vb
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="11200-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="11200-106">Arguments</span></span>

<span data-ttu-id="11200-107">`number`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="11200-107">`number`: *Integer*</span></span>

<span data-ttu-id="11200-108">Номер, соответствующий ожидаемому одному символу.</span><span class="sxs-lookup"><span data-stu-id="11200-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="11200-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="11200-109">Return values</span></span>

<span data-ttu-id="11200-110">*Строка*</span><span class="sxs-lookup"><span data-stu-id="11200-110">*String*</span></span>

<span data-ttu-id="11200-111">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="11200-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="11200-112">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="11200-112">Usage notes</span></span>

<span data-ttu-id="11200-113">Строка, возвращаемая этой функцией, зависит от кодировки, выбранной в родительском элементе формата **FILE**.</span><span class="sxs-lookup"><span data-stu-id="11200-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="11200-114">Список поддерживаемых кодировок см. в разделе [Класс кодировки](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="11200-114">For a list of the supported encodings, see [Encoding class](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span></span>

## <a name="example"></a><span data-ttu-id="11200-115">Пример</span><span class="sxs-lookup"><span data-stu-id="11200-115">Example</span></span>

<span data-ttu-id="11200-116">`CHAR (255)` возвращает **"ÿ"**.</span><span class="sxs-lookup"><span data-stu-id="11200-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="11200-117">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="11200-117">Additional resources</span></span>

[<span data-ttu-id="11200-118">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="11200-118">Text functions</span></span>](er-functions-category-text.md)
