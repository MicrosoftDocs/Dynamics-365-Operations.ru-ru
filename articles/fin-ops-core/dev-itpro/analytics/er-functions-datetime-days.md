---
title: Функция ER DAYS
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности DAYS
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
ms.openlocfilehash: 47d992d061f8664a55332024ee5c6cd41e4bc495
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743575"
---
# <a name="days-er-function"></a><span data-ttu-id="0b353-103">Функция ER DAYS</span><span class="sxs-lookup"><span data-stu-id="0b353-103">DAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b353-104">Функция `DAYS` возвращает *целочисленное* значение числа дней между одной указанной датой и второй указанной датой.</span><span class="sxs-lookup"><span data-stu-id="0b353-104">The `DAYS` function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b353-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b353-105">Syntax</span></span>

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a><span data-ttu-id="0b353-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="0b353-106">Arguments</span></span>

<span data-ttu-id="0b353-107">`date 1`: *Дата*</span><span class="sxs-lookup"><span data-stu-id="0b353-107">`date 1`: *Date*</span></span>

<span data-ttu-id="0b353-108">Значение даты, представляющее дату начала для расчета количества дней.</span><span class="sxs-lookup"><span data-stu-id="0b353-108">A date value that represents the start date for the calculation of the number of days.</span></span>

<span data-ttu-id="0b353-109">`date 2`: *Дата*</span><span class="sxs-lookup"><span data-stu-id="0b353-109">`date 2`: *Date*</span></span>

<span data-ttu-id="0b353-110">Значение даты, представляющее дату окончания для расчета количества дней.</span><span class="sxs-lookup"><span data-stu-id="0b353-110">A date value that represents the end date for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="0b353-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="0b353-111">Return values</span></span>

<span data-ttu-id="0b353-112">*Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="0b353-112">*Integer*</span></span>

<span data-ttu-id="0b353-113">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="0b353-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0b353-114">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="0b353-114">Usage notes</span></span>

<span data-ttu-id="0b353-115">Функция `DAYS` возвращает положительное значение, если первая дата позднее второй даты, возвращает **0** (ноль), когда первая дата равна второй дате, и возвращает отрицательное значение, когда первая дата раньше, чем вторая дата.</span><span class="sxs-lookup"><span data-stu-id="0b353-115">The `DAYS` function returns a positive value when the first date is later than the second date, it returns **0** (zero) when the first date equals the second date, and it returns a negative value when the first date is earlier than the second date.</span></span>

## <a name="example"></a><span data-ttu-id="0b353-116">Пример</span><span class="sxs-lookup"><span data-stu-id="0b353-116">Example</span></span>

<span data-ttu-id="0b353-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` возвращает **-1**.</span><span class="sxs-lookup"><span data-stu-id="0b353-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returns **-1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0b353-118">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0b353-118">Additional resources</span></span>

[<span data-ttu-id="0b353-119">Функции даты и времени</span><span class="sxs-lookup"><span data-stu-id="0b353-119">Date and time functions</span></span>](er-functions-category-datetime.md)
