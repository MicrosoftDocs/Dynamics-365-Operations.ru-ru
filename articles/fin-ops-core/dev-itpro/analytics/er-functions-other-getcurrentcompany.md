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
ms.openlocfilehash: 7e3c164c6d54d8387eed5018219da5fd82c765c8
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744137"
---
# <a name="getcurrentcompany-er-function"></a><span data-ttu-id="700dd-103">Функция ER GETCURRENTCOMPANY</span><span class="sxs-lookup"><span data-stu-id="700dd-103">GETCURRENTCOMPANY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="700dd-104">Функция `GETCURRENTCOMPANY` возвращает *строковое* значение, представляющее код для юридического лица (компании), в которую выполнил вход пользователь.</span><span class="sxs-lookup"><span data-stu-id="700dd-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="700dd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="700dd-105">Syntax</span></span>

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="700dd-106">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="700dd-106">Return values</span></span>

<span data-ttu-id="700dd-107">*Строка*</span><span class="sxs-lookup"><span data-stu-id="700dd-107">*String*</span></span>

<span data-ttu-id="700dd-108">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="700dd-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="700dd-109">Пример</span><span class="sxs-lookup"><span data-stu-id="700dd-109">Example</span></span>

<span data-ttu-id="700dd-110">`GETCURRENTCOMPANY ()` возвращает **USMF** для пользователя, выполнившего вход в компанию **Contoso Entertainment System USA**.</span><span class="sxs-lookup"><span data-stu-id="700dd-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="700dd-111">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="700dd-111">Additional resources</span></span>

[<span data-ttu-id="700dd-112">Другие функции (характерные для конкретных бизнес-доменов)</span><span class="sxs-lookup"><span data-stu-id="700dd-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
