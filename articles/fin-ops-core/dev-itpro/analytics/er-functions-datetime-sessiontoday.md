---
title: Функция ER SESSIONTODAY
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности SESSIONTODAY.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 483ff46a27068bc2d70c80a848f0329861c914b3
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042281"
---
# <span data-ttu-id="13f9e-103"><a name="SESSIONTODAY">Функция ER SESSIONTODAY</a></span><span class="sxs-lookup"><span data-stu-id="13f9e-103"><a name="SESSIONTODAY">SESSIONTODAY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="13f9e-104">Функция `SESSIONTODAY` возвращает значение *Date*, которое представляет текущую дату сеанса приложения.</span><span class="sxs-lookup"><span data-stu-id="13f9e-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="13f9e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13f9e-105">Syntax</span></span>

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="13f9e-106">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="13f9e-106">Return values</span></span>

<span data-ttu-id="13f9e-107">*Дата*</span><span class="sxs-lookup"><span data-stu-id="13f9e-107">*Date*</span></span>

<span data-ttu-id="13f9e-108">Результирующее значение даты.</span><span class="sxs-lookup"><span data-stu-id="13f9e-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="13f9e-109">Пример</span><span class="sxs-lookup"><span data-stu-id="13f9e-109">Example</span></span>

<span data-ttu-id="13f9e-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` возвращает текущую дату сеанса приложения, 24 декабря 2015 года, как строку **"24-12-2015"** на основе выбранной немецкой культуры и указанного формата.</span><span class="sxs-lookup"><span data-stu-id="13f9e-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="13f9e-111">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="13f9e-111">Additional resources</span></span>

[<span data-ttu-id="13f9e-112">Функции даты и времени</span><span class="sxs-lookup"><span data-stu-id="13f9e-112">Date and time functions</span></span>](er-functions-category-datetime.md)
