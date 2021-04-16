---
title: Функция ER SESSIONTODAY
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности SESSIONTODAY.
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
ms.openlocfilehash: 6d0fcbbf1a1fb0809e3f76161314f38bcd8a74aa
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746780"
---
# <a name="sessiontoday-er-function"></a><span data-ttu-id="3e62c-103">Функция ER SESSIONTODAY</span><span class="sxs-lookup"><span data-stu-id="3e62c-103">SESSIONTODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3e62c-104">Функция `SESSIONTODAY` возвращает значение *Date*, которое представляет текущую дату сеанса приложения.</span><span class="sxs-lookup"><span data-stu-id="3e62c-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e62c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3e62c-105">Syntax</span></span>

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="3e62c-106">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="3e62c-106">Return values</span></span>

<span data-ttu-id="3e62c-107">*Дата*</span><span class="sxs-lookup"><span data-stu-id="3e62c-107">*Date*</span></span>

<span data-ttu-id="3e62c-108">Результирующее значение даты.</span><span class="sxs-lookup"><span data-stu-id="3e62c-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="3e62c-109">Пример</span><span class="sxs-lookup"><span data-stu-id="3e62c-109">Example</span></span>

<span data-ttu-id="3e62c-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` возвращает текущую дату сеанса приложения, 24 декабря 2015 года, как строку **"24-12-2015"** на основе выбранной немецкой культуры и указанного формата.</span><span class="sxs-lookup"><span data-stu-id="3e62c-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3e62c-111">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3e62c-111">Additional resources</span></span>

[<span data-ttu-id="3e62c-112">Функции даты и времени</span><span class="sxs-lookup"><span data-stu-id="3e62c-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]