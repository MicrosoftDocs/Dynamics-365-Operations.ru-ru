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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7813b0c6002e47aef6a8c119c72728a49584401b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041244"
---
# <span data-ttu-id="57fe8-103"><a name="CHAR">Функция ER CHAR</a></span><span class="sxs-lookup"><span data-stu-id="57fe8-103"><a name="CHAR">CHAR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57fe8-104">Функция `CHAR` возвращает *строковое* значение, которое представляет один символ, на который ссылается указанный номер Unicode.</span><span class="sxs-lookup"><span data-stu-id="57fe8-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="57fe8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="57fe8-105">Syntax</span></span>

```vb
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="57fe8-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="57fe8-106">Arguments</span></span>

<span data-ttu-id="57fe8-107">`number`: *Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="57fe8-107">`number`: *Integer*</span></span>

<span data-ttu-id="57fe8-108">Номер, соответствующий ожидаемому одному символу.</span><span class="sxs-lookup"><span data-stu-id="57fe8-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="57fe8-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="57fe8-109">Return values</span></span>

<span data-ttu-id="57fe8-110">*Строка*</span><span class="sxs-lookup"><span data-stu-id="57fe8-110">*String*</span></span>

<span data-ttu-id="57fe8-111">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="57fe8-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="57fe8-112">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="57fe8-112">Usage notes</span></span>

<span data-ttu-id="57fe8-113">Строка, возвращаемая этой функцией, зависит от кодировки, выбранной в родительском элементе формата **FILE**.</span><span class="sxs-lookup"><span data-stu-id="57fe8-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="57fe8-114">Список поддерживаемых кодировок см. в разделе [Класс кодировки](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="57fe8-114">For a list of the supported encodings, see [Encoding class](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span></span>

## <a name="example"></a><span data-ttu-id="57fe8-115">Пример</span><span class="sxs-lookup"><span data-stu-id="57fe8-115">Example</span></span>

<span data-ttu-id="57fe8-116">`CHAR (255)` возвращает **"ÿ"**.</span><span class="sxs-lookup"><span data-stu-id="57fe8-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="57fe8-117">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="57fe8-117">Additional resources</span></span>

[<span data-ttu-id="57fe8-118">Текстовые функции</span><span class="sxs-lookup"><span data-stu-id="57fe8-118">Text functions</span></span>](er-functions-category-text.md)
