---
title: Функция ER CHAR
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности CHAR
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
ms.openlocfilehash: a621328817171be7df0622507c84f5c6f6fe90a1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746443"
---
# <a name="char-er-function"></a><span data-ttu-id="761a6-103">Функция ER CHAR</span><span class="sxs-lookup"><span data-stu-id="761a6-103">CHAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="761a6-104">Функция `CHAR` возвращает *строковое* значение, которое представляет один символ, на который ссылается указанный номер Unicode.</span><span class="sxs-lookup"><span data-stu-id="761a6-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="761a6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="761a6-105">Syntax</span></span>

```vb
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="761a6-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="761a6-106">Arguments</span></span>

<span data-ttu-id="761a6-107">`number`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="761a6-107">`number`: *Integer*</span></span>

<span data-ttu-id="761a6-108">Номер, соответствующий ожидаемому одному символу.</span><span class="sxs-lookup"><span data-stu-id="761a6-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="761a6-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="761a6-109">Return values</span></span>

<span data-ttu-id="761a6-110">*Строка*</span><span class="sxs-lookup"><span data-stu-id="761a6-110">*String*</span></span>

<span data-ttu-id="761a6-111">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="761a6-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="761a6-112">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="761a6-112">Usage notes</span></span>

<span data-ttu-id="761a6-113">Строка, возвращаемая этой функцией, зависит от кодировки, выбранной в родительском элементе формата **FILE**.</span><span class="sxs-lookup"><span data-stu-id="761a6-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="761a6-114">Список поддерживаемых кодировок см. в разделе [Класс кодировки](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="761a6-114">For a list of the supported encodings, see [Encoding class](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span></span>

## <a name="example"></a><span data-ttu-id="761a6-115">Пример</span><span class="sxs-lookup"><span data-stu-id="761a6-115">Example</span></span>

<span data-ttu-id="761a6-116">`CHAR (255)` возвращает **"ÿ"**.</span><span class="sxs-lookup"><span data-stu-id="761a6-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="761a6-117">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="761a6-117">Additional resources</span></span>

[<span data-ttu-id="761a6-118">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="761a6-118">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]