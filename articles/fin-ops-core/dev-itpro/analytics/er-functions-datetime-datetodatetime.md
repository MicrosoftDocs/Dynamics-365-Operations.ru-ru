---
title: Функция ER DATETODATETIME
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности DATETODATETIME.
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
ms.openlocfilehash: 961ccd18e70d4f9851027492366a7d9408a668c5
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042420"
---
# <span data-ttu-id="9a57a-103"><a name="DATETODATETIME">Функция ER DATETODATETIME</a></span><span class="sxs-lookup"><span data-stu-id="9a57a-103"><a name="DATETODATETIME">DATETODATETIME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9a57a-104">Функция `DATETODATETIME` возвращает значение *DateTime*, которое преобразуется из заданного значения даты в значение даты/времени в формате UTC (Greenwich Mean Time \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="9a57a-104">The `DATETODATETIME` function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="9a57a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a57a-105">Syntax</span></span>

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a><span data-ttu-id="9a57a-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="9a57a-106">Arguments</span></span>

<span data-ttu-id="9a57a-107">`date`: *Дата*</span><span class="sxs-lookup"><span data-stu-id="9a57a-107">`date`: *Date*</span></span>

<span data-ttu-id="9a57a-108">Значение даты, представляющее дату для преобразования.</span><span class="sxs-lookup"><span data-stu-id="9a57a-108">A date value that represents the date to convert.</span></span>

## <a name="return-values"></a><span data-ttu-id="9a57a-109">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="9a57a-109">Return values</span></span>

<span data-ttu-id="9a57a-110">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="9a57a-110">*DateTime*</span></span>

<span data-ttu-id="9a57a-111">Результирующее значение даты/времени.</span><span class="sxs-lookup"><span data-stu-id="9a57a-111">The resulting date/time value.</span></span>

## <a name="example-1"></a><span data-ttu-id="9a57a-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9a57a-112">Example 1</span></span>

<span data-ttu-id="9a57a-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` возвращает дату текущего сеанса Microsoft Dynamics 365 Finance, 24 декабря 2015, как **12/24/2015 12:00:00 AM**.</span><span class="sxs-lookup"><span data-stu-id="9a57a-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` returns the date of the current Microsoft Dynamics 365 Finance session, December 24, 2015, as **12/24/2015 12:00:00 AM**.</span></span> <span data-ttu-id="9a57a-114">В этом примере **CompInfo** представляет собой источник данных электронной отчетности (ER) типа **Finance and Operations/Table** и ссылается на таблицу CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="9a57a-114">In this example, **CompInfo** is an Electronic reporting (ER) data source of the **Finance and Operations/Table** type, and it refers to the CompanyInfo table.</span></span>

## <a name="example-2"></a><span data-ttu-id="9a57a-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9a57a-115">Example 2</span></span>

<span data-ttu-id="9a57a-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` возвращает значение даты/времени **11/12/2019 12:00:00 AM**.</span><span class="sxs-lookup"><span data-stu-id="9a57a-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` returns the date/time value **11/12/2019 12:00:00 AM**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9a57a-117">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9a57a-117">Additional resources</span></span>

[<span data-ttu-id="9a57a-118">Функции даты и времени</span><span class="sxs-lookup"><span data-stu-id="9a57a-118">Date and time functions</span></span>](er-functions-category-datetime.md)
