---
title: Функция ER DAYS
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности DAYS
author: NickSelin
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
ms.openlocfilehash: 310359a29a506d69d1f34aaa710a82b0f2ea528e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746899"
---
# <a name="days-er-function"></a><span data-ttu-id="3d480-103">Функция ER DAYS</span><span class="sxs-lookup"><span data-stu-id="3d480-103">DAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d480-104">Функция `DAYS` возвращает *целочисленное* значение числа дней между одной указанной датой и второй указанной датой.</span><span class="sxs-lookup"><span data-stu-id="3d480-104">The `DAYS` function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d480-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d480-105">Syntax</span></span>

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a><span data-ttu-id="3d480-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="3d480-106">Arguments</span></span>

<span data-ttu-id="3d480-107">`date 1`: *Дата*</span><span class="sxs-lookup"><span data-stu-id="3d480-107">`date 1`: *Date*</span></span>

<span data-ttu-id="3d480-108">Значение даты, представляющее дату начала для расчета количества дней.</span><span class="sxs-lookup"><span data-stu-id="3d480-108">A date value that represents the start date for the calculation of the number of days.</span></span>

<span data-ttu-id="3d480-109">`date 2`: *Дата*</span><span class="sxs-lookup"><span data-stu-id="3d480-109">`date 2`: *Date*</span></span>

<span data-ttu-id="3d480-110">Значение даты, представляющее дату окончания для расчета количества дней.</span><span class="sxs-lookup"><span data-stu-id="3d480-110">A date value that represents the end date for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="3d480-111">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="3d480-111">Return values</span></span>

<span data-ttu-id="3d480-112">*Целочисленный*</span><span class="sxs-lookup"><span data-stu-id="3d480-112">*Integer*</span></span>

<span data-ttu-id="3d480-113">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="3d480-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3d480-114">Примечания по использованию</span><span class="sxs-lookup"><span data-stu-id="3d480-114">Usage notes</span></span>

<span data-ttu-id="3d480-115">Функция `DAYS` возвращает положительное значение, если первая дата позднее второй даты, возвращает **0** (ноль), когда первая дата равна второй дате, и возвращает отрицательное значение, когда первая дата раньше, чем вторая дата.</span><span class="sxs-lookup"><span data-stu-id="3d480-115">The `DAYS` function returns a positive value when the first date is later than the second date, it returns **0** (zero) when the first date equals the second date, and it returns a negative value when the first date is earlier than the second date.</span></span>

## <a name="example"></a><span data-ttu-id="3d480-116">Пример</span><span class="sxs-lookup"><span data-stu-id="3d480-116">Example</span></span>

<span data-ttu-id="3d480-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` возвращает **-1**.</span><span class="sxs-lookup"><span data-stu-id="3d480-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returns **-1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3d480-118">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3d480-118">Additional resources</span></span>

[<span data-ttu-id="3d480-119">Функции даты и времени</span><span class="sxs-lookup"><span data-stu-id="3d480-119">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]