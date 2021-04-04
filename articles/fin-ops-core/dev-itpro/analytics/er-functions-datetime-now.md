---
title: Функция ER NOW
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности NOW
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 8e549634b3856777aff610fa0e61c19bcad71dd7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563518"
---
# <a name="now-er-function"></a><span data-ttu-id="adeb8-103">Функция ER NOW</span><span class="sxs-lookup"><span data-stu-id="adeb8-103">NOW ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="adeb8-104">Функция `NOW` возвращает значение *DateTime*, которое представляет текущую дату и время сервера приложения.</span><span class="sxs-lookup"><span data-stu-id="adeb8-104">The `NOW` function returns a *DateTime* value that represents the current application server date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="adeb8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="adeb8-105">Syntax</span></span>

```vb
NOW ()
```

## <a name="return-values"></a><span data-ttu-id="adeb8-106">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="adeb8-106">Return values</span></span>

<span data-ttu-id="adeb8-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="adeb8-107">*DateTime*</span></span>

<span data-ttu-id="adeb8-108">Результирующее значение даты/времени.</span><span class="sxs-lookup"><span data-stu-id="adeb8-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="adeb8-109">Пример</span><span class="sxs-lookup"><span data-stu-id="adeb8-109">Example</span></span>

<span data-ttu-id="adeb8-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` возвращает текущую дату/время сервера приложений, 24 декабря 2015, как **"24-12-2015"**, на основе указанного настраиваемого формата.</span><span class="sxs-lookup"><span data-stu-id="adeb8-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="adeb8-111">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="adeb8-111">Additional resources</span></span>

[<span data-ttu-id="adeb8-112">Функции даты и времени</span><span class="sxs-lookup"><span data-stu-id="adeb8-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]