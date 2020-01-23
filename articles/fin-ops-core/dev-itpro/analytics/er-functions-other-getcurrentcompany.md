---
title: Функция ER GETCURRENTCOMPANY
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности GETCURRENTCOMPANY.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: a0b4c93a4705cd0e382b9b6c7af1d199beeceabe
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916001"
---
# <span data-ttu-id="67ffe-103"><a name="GETCURRENTCOMPANY">Функция ER GETCURRENTCOMPANY</a></span><span class="sxs-lookup"><span data-stu-id="67ffe-103"><a name="GETCURRENTCOMPANY">GETCURRENTCOMPANY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67ffe-104">Функция `GETCURRENTCOMPANY` возвращает *строковое* значение, представляющее код для юридического лица (компании), в которую выполнил вход пользователь.</span><span class="sxs-lookup"><span data-stu-id="67ffe-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="67ffe-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="67ffe-105">Syntax</span></span>

```
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="67ffe-106">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="67ffe-106">Return values</span></span>

<span data-ttu-id="67ffe-107">*Строка*</span><span class="sxs-lookup"><span data-stu-id="67ffe-107">*String*</span></span>

<span data-ttu-id="67ffe-108">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="67ffe-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="67ffe-109">Пример</span><span class="sxs-lookup"><span data-stu-id="67ffe-109">Example</span></span>

<span data-ttu-id="67ffe-110">`GETCURRENTCOMPANY ()` возвращает **USMF** для пользователя, выполнившего вход в компанию **Contoso Entertainment System USA**.</span><span class="sxs-lookup"><span data-stu-id="67ffe-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="67ffe-111">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="67ffe-111">Additional resources</span></span>

[<span data-ttu-id="67ffe-112">Другие функции (характерные для конкретных бизнес-доменов)</span><span class="sxs-lookup"><span data-stu-id="67ffe-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
