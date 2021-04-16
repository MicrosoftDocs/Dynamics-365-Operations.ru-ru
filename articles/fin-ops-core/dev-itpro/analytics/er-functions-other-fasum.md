---
title: Функция ER FA_SUM
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности FA_SUM
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: d6f380e384e591e7417cfa40c73f9be6575fb0f6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744303"
---
# <a name="fa_sum-er-function"></a><span data-ttu-id="719e6-103">Функция ER FA_SUM</span><span class="sxs-lookup"><span data-stu-id="719e6-103">FA_SUM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="719e6-104">Функция `FA_SUM` возвращает значение *Контейнер (запись)*, которое состоит из данных сумм основных средств для указанного элемента основных средств, кода модели стоимости и периода дат.</span><span class="sxs-lookup"><span data-stu-id="719e6-104">The `FA_SUM` function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span>

## <a name="syntax"></a><span data-ttu-id="719e6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="719e6-105">Syntax</span></span>

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a><span data-ttu-id="719e6-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="719e6-106">Arguments</span></span>

<span data-ttu-id="719e6-107">`fixed asset code`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="719e6-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="719e6-108">Значение *строка*, представляющее код элемента основного средства, для которого рассчитывается сальдо.</span><span class="sxs-lookup"><span data-stu-id="719e6-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="719e6-109">`value model code`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="719e6-109">`value model code`: *String*</span></span>

<span data-ttu-id="719e6-110">Значение *строка*, представляющее код модели стоимости, для которого рассчитывается сальдо.</span><span class="sxs-lookup"><span data-stu-id="719e6-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="719e6-111">`start date`: *Дата*</span><span class="sxs-lookup"><span data-stu-id="719e6-111">`start date`: *Date*</span></span>

<span data-ttu-id="719e6-112">Значение *Дата*, представляющее дату начала периода, для которого рассчитываются суммы основного средства.</span><span class="sxs-lookup"><span data-stu-id="719e6-112">A *Date* value that represents the start date of a period that the fixed asset amounts are calculated for.</span></span>

<span data-ttu-id="719e6-113">`end date`: *Дата*</span><span class="sxs-lookup"><span data-stu-id="719e6-113">`end date`: *Date*</span></span>

<span data-ttu-id="719e6-114">Значение *Дата*, представляющее дату окончания периода, для которого рассчитываются суммы основного средства.</span><span class="sxs-lookup"><span data-stu-id="719e6-114">A *Date* value that represents the end date of a period that the fixed asset amounts are calculated for.</span></span>

## <a name="return-values"></a><span data-ttu-id="719e6-115">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="719e6-115">Return values</span></span>

<span data-ttu-id="719e6-116">*Контейнер (запись)*</span><span class="sxs-lookup"><span data-stu-id="719e6-116">*Container (record)*</span></span>

<span data-ttu-id="719e6-117">Результирующее значение записи.</span><span class="sxs-lookup"><span data-stu-id="719e6-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="719e6-118">Пример</span><span class="sxs-lookup"><span data-stu-id="719e6-118">Example</span></span>

<span data-ttu-id="719e6-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` возвращает контейнер данных для основного средства **COMP-000001**, которое было подготовлено для модели стоимости **Current** и за период с **Date1** по **Date2**.</span><span class="sxs-lookup"><span data-stu-id="719e6-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returns the data container for fixed asset **COMP-000001** that has been prepared for the **Current** value model and for a period from **Date1** to **Date2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="719e6-120">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="719e6-120">Additional resources</span></span>

[<span data-ttu-id="719e6-121">Другие функции (характерные для конкретных бизнес-доменов)</span><span class="sxs-lookup"><span data-stu-id="719e6-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]