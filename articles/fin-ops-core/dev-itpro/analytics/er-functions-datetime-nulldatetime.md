---
title: Функция ER NULLDATETIME
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности NULLDATETIME.
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
ms.openlocfilehash: 3cd4c152d4e220a2f6315265ed5e44d148134279
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042273"
---
# <span data-ttu-id="dc1d7-103"><a name="NULLDATETIME">Функция ER NULLDATETIME</a></span><span class="sxs-lookup"><span data-stu-id="dc1d7-103"><a name="NULLDATETIME">NULLDATETIME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc1d7-104">Функция `NULLDATETIME` возвращает значение *DateTime*, которое представляет значение **нулевой** даты/времени (1 января 1900 года) в формате UTC (Greenwich Mean Time \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="dc1d7-104">The `NULLDATETIME` function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="dc1d7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc1d7-105">Syntax</span></span>

```vb
NULLDATETIME ()
```

## <a name="return-values"></a><span data-ttu-id="dc1d7-106">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="dc1d7-106">Return values</span></span>

<span data-ttu-id="dc1d7-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="dc1d7-107">*DateTime*</span></span>

<span data-ttu-id="dc1d7-108">Результирующее значение даты/времени.</span><span class="sxs-lookup"><span data-stu-id="dc1d7-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="dc1d7-109">Пример</span><span class="sxs-lookup"><span data-stu-id="dc1d7-109">Example</span></span>

<span data-ttu-id="dc1d7-110">`DATETIMEFORMAT( NULLDATETIME(), "O")` возвращает значение строки **1900-01-01T00:00:00.0000000+00:00**, когда оно называется во время процесса, инициированного пользователем приложения со значением часового пояса **(GMT) UTC** в разделе **Настройки языка и страны/региона**.</span><span class="sxs-lookup"><span data-stu-id="dc1d7-110">`DATETIMEFORMAT( NULLDATETIME(), "O")` returns the string value **1900-01-01T00:00:00.0000000+00:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT) Coordinated Universal Time** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dc1d7-111">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="dc1d7-111">Additional resources</span></span>

[<span data-ttu-id="dc1d7-112">Функции даты и времени</span><span class="sxs-lookup"><span data-stu-id="dc1d7-112">Date and time functions</span></span>](er-functions-category-datetime.md)
