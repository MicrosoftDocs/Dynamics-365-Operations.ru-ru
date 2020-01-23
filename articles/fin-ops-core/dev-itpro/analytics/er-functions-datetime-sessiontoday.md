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
ms.openlocfilehash: bcfb36d6e3fb8475546f7cfb420c4aca848ac896
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917473"
---
# <span data-ttu-id="80c0a-103"><a name="SESSIONTODAY">Функция ER SESSIONTODAY</a></span><span class="sxs-lookup"><span data-stu-id="80c0a-103"><a name="SESSIONTODAY">SESSIONTODAY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="80c0a-104">Функция `SESSIONTODAY` возвращает значение *Date*, которое представляет текущую дату сеанса приложения.</span><span class="sxs-lookup"><span data-stu-id="80c0a-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="80c0a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80c0a-105">Syntax</span></span>

```
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="80c0a-106">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="80c0a-106">Return values</span></span>

<span data-ttu-id="80c0a-107">*Дата*</span><span class="sxs-lookup"><span data-stu-id="80c0a-107">*Date*</span></span>

<span data-ttu-id="80c0a-108">Результирующее значение даты.</span><span class="sxs-lookup"><span data-stu-id="80c0a-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="80c0a-109">Пример</span><span class="sxs-lookup"><span data-stu-id="80c0a-109">Example</span></span>

<span data-ttu-id="80c0a-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` возвращает текущую дату сеанса приложения, 24 декабря 2015 года, как строку **"24-12-2015"** на основе выбранной немецкой культуры и указанного формата.</span><span class="sxs-lookup"><span data-stu-id="80c0a-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="80c0a-111">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="80c0a-111">Additional resources</span></span>

[<span data-ttu-id="80c0a-112">Функции даты и времени</span><span class="sxs-lookup"><span data-stu-id="80c0a-112">Date and time functions</span></span>](er-functions-category-datetime.md)
