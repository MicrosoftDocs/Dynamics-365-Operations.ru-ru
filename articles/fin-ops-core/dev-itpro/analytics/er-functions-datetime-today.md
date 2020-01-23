---
title: Функция ER TODAY
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности TODAY.
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
ms.openlocfilehash: c7e9917dcdc45a52e0ad490f5fa194d5390cc437
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917427"
---
# <span data-ttu-id="03bd6-103"><a name="TODAY">Функция ER TODAY</a></span><span class="sxs-lookup"><span data-stu-id="03bd6-103"><a name="TODAY">TODAY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03bd6-104">Функция `TODAY` возвращает значение *Date*, которое представляет текущую дату сервера приложения.</span><span class="sxs-lookup"><span data-stu-id="03bd6-104">The `TODAY` function returns a *Date* value that represents the current application server date.</span></span>

## <a name="syntax"></a><span data-ttu-id="03bd6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03bd6-105">Syntax</span></span>

```
TODAY ()
```

## <a name="return-values"></a><span data-ttu-id="03bd6-106">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="03bd6-106">Return values</span></span>

<span data-ttu-id="03bd6-107">*Дата*</span><span class="sxs-lookup"><span data-stu-id="03bd6-107">*Date*</span></span>

<span data-ttu-id="03bd6-108">Результирующее значение даты.</span><span class="sxs-lookup"><span data-stu-id="03bd6-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="03bd6-109">Пример</span><span class="sxs-lookup"><span data-stu-id="03bd6-109">Example</span></span>

<span data-ttu-id="03bd6-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` возвращает текущую дату сервера приложений, 24 декабря 2015, как строку **"24-12-2015"**, на основе указанного настраиваемого формата.</span><span class="sxs-lookup"><span data-stu-id="03bd6-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="03bd6-111">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="03bd6-111">Additional resources</span></span>

[<span data-ttu-id="03bd6-112">Функции даты и времени</span><span class="sxs-lookup"><span data-stu-id="03bd6-112">Date and time functions</span></span>](er-functions-category-datetime.md)
