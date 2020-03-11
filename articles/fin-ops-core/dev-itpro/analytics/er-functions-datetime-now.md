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
ms.openlocfilehash: cb5b2fa1b8c466582b15d60a56260f0f7111ebd9
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042351"
---
# <span data-ttu-id="2e927-103"><a name="NOW">Функция ER NOW</a></span><span class="sxs-lookup"><span data-stu-id="2e927-103"><a name="NOW">NOW ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e927-104">Функция `NOW` возвращает значение *DateTime*, которое представляет текущую дату и время сервера приложения.</span><span class="sxs-lookup"><span data-stu-id="2e927-104">The `NOW` function returns a *DateTime* value that represents the current application server date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e927-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e927-105">Syntax</span></span>

```vb
NOW ()
```

## <a name="return-values"></a><span data-ttu-id="2e927-106">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="2e927-106">Return values</span></span>

<span data-ttu-id="2e927-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="2e927-107">*DateTime*</span></span>

<span data-ttu-id="2e927-108">Результирующее значение даты/времени.</span><span class="sxs-lookup"><span data-stu-id="2e927-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="2e927-109">Пример</span><span class="sxs-lookup"><span data-stu-id="2e927-109">Example</span></span>

<span data-ttu-id="2e927-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` возвращает текущую дату/время сервера приложений, 24 декабря 2015, как **"24-12-2015"**, на основе указанного настраиваемого формата.</span><span class="sxs-lookup"><span data-stu-id="2e927-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2e927-111">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2e927-111">Additional resources</span></span>

[<span data-ttu-id="2e927-112">Функции даты и времени</span><span class="sxs-lookup"><span data-stu-id="2e927-112">Date and time functions</span></span>](er-functions-category-datetime.md)
