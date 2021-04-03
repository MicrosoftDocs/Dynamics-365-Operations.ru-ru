---
title: Функция ER DATETODATETIME
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности DATETODATETIME.
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
ms.openlocfilehash: d30fdc9c7b6f277b8712b733cabdb0552db2a748
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563590"
---
# <a name="datetodatetime-er-function"></a><span data-ttu-id="fcc83-103">Функция ER DATETODATETIME</span><span class="sxs-lookup"><span data-stu-id="fcc83-103">DATETODATETIME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fcc83-104">Функция `DATETODATETIME` возвращает значение *DateTime*, которое преобразуется из заданного значения даты в значение даты/времени в формате UTC (Greenwich Mean Time \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="fcc83-104">The `DATETODATETIME` function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="fcc83-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fcc83-105">Syntax</span></span>

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a><span data-ttu-id="fcc83-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="fcc83-106">Arguments</span></span>

<span data-ttu-id="fcc83-107">`date`: *Дата*</span><span class="sxs-lookup"><span data-stu-id="fcc83-107">`date`: *Date*</span></span>

<span data-ttu-id="fcc83-108">Значение даты, представляющее дату для преобразования.</span><span class="sxs-lookup"><span data-stu-id="fcc83-108">A date value that represents the date to convert.</span></span>

## <a name="return-values"></a><span data-ttu-id="fcc83-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="fcc83-109">Return values</span></span>

<span data-ttu-id="fcc83-110">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="fcc83-110">*DateTime*</span></span>

<span data-ttu-id="fcc83-111">Результирующее значение даты/времени.</span><span class="sxs-lookup"><span data-stu-id="fcc83-111">The resulting date/time value.</span></span>

## <a name="example-1"></a><span data-ttu-id="fcc83-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fcc83-112">Example 1</span></span>

<span data-ttu-id="fcc83-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` возвращает дату текущего сеанса Microsoft Dynamics 365 Finance, 24 декабря 2015, как **12/24/2015 12:00:00 AM**.</span><span class="sxs-lookup"><span data-stu-id="fcc83-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` returns the date of the current Microsoft Dynamics 365 Finance session, December 24, 2015, as **12/24/2015 12:00:00 AM**.</span></span> <span data-ttu-id="fcc83-114">В этом примере **CompInfo** представляет собой источник данных электронной отчетности (ER) типа **Finance and Operations/Table** и ссылается на таблицу CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="fcc83-114">In this example, **CompInfo** is an Electronic reporting (ER) data source of the **Finance and Operations/Table** type, and it refers to the CompanyInfo table.</span></span>

## <a name="example-2"></a><span data-ttu-id="fcc83-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fcc83-115">Example 2</span></span>

<span data-ttu-id="fcc83-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` возвращает значение даты/времени **11/12/2019 12:00:00 AM**.</span><span class="sxs-lookup"><span data-stu-id="fcc83-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` returns the date/time value **11/12/2019 12:00:00 AM**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fcc83-117">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="fcc83-117">Additional resources</span></span>

[<span data-ttu-id="fcc83-118">Функции даты и времени</span><span class="sxs-lookup"><span data-stu-id="fcc83-118">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]