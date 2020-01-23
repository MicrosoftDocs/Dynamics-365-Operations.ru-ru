---
title: Функция ER NOW
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности NOW
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: cffb23afa4cb347d2840b099b0b49a71150d87d8
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917565"
---
# <span data-ttu-id="1fe79-103"><a name="NOW">Функция ER NOW</a></span><span class="sxs-lookup"><span data-stu-id="1fe79-103"><a name="NOW">NOW ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1fe79-104">Функция `NOW` возвращает значение *DateTime*, которое представляет текущую дату и время сервера приложения.</span><span class="sxs-lookup"><span data-stu-id="1fe79-104">The `NOW` function returns a *DateTime* value that represents the current application server date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fe79-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1fe79-105">Syntax</span></span>

```
NOW ()
```

## <a name="return-values"></a><span data-ttu-id="1fe79-106">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="1fe79-106">Return values</span></span>

<span data-ttu-id="1fe79-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="1fe79-107">*DateTime*</span></span>

<span data-ttu-id="1fe79-108">Результирующее значение даты/времени.</span><span class="sxs-lookup"><span data-stu-id="1fe79-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="1fe79-109">Пример</span><span class="sxs-lookup"><span data-stu-id="1fe79-109">Example</span></span>

<span data-ttu-id="1fe79-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` возвращает текущую дату/время сервера приложений, 24 декабря 2015, как **"24-12-2015"**, на основе указанного настраиваемого формата.</span><span class="sxs-lookup"><span data-stu-id="1fe79-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1fe79-111">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1fe79-111">Additional resources</span></span>

[<span data-ttu-id="1fe79-112">Функции даты и времени</span><span class="sxs-lookup"><span data-stu-id="1fe79-112">Date and time functions</span></span>](er-functions-category-datetime.md)
