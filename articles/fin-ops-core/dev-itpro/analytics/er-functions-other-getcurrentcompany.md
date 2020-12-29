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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e14c6a8aaff0a32a115117938d0e853bb34bb14
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684867"
---
# <a name="getcurrentcompany-er-function"></a><span data-ttu-id="42ee1-103">Функция ER GETCURRENTCOMPANY</span><span class="sxs-lookup"><span data-stu-id="42ee1-103">GETCURRENTCOMPANY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="42ee1-104">Функция `GETCURRENTCOMPANY` возвращает *строковое* значение, представляющее код для юридического лица (компании), в которую выполнил вход пользователь.</span><span class="sxs-lookup"><span data-stu-id="42ee1-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="42ee1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42ee1-105">Syntax</span></span>

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="42ee1-106">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="42ee1-106">Return values</span></span>

<span data-ttu-id="42ee1-107">*Строка*</span><span class="sxs-lookup"><span data-stu-id="42ee1-107">*String*</span></span>

<span data-ttu-id="42ee1-108">Результирующее текстовое значение.</span><span class="sxs-lookup"><span data-stu-id="42ee1-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="42ee1-109">Пример</span><span class="sxs-lookup"><span data-stu-id="42ee1-109">Example</span></span>

<span data-ttu-id="42ee1-110">`GETCURRENTCOMPANY ()` возвращает **USMF** для пользователя, выполнившего вход в компанию **Contoso Entertainment System USA**.</span><span class="sxs-lookup"><span data-stu-id="42ee1-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="42ee1-111">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="42ee1-111">Additional resources</span></span>

[<span data-ttu-id="42ee1-112">Другие функции (характерные для конкретных бизнес-доменов)</span><span class="sxs-lookup"><span data-stu-id="42ee1-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
