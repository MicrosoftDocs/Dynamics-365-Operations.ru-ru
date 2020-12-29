---
title: Функция ER FA_SUM
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности FA_SUM
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 1c46f945a9caae2836886d051da820658e8be9af
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687704"
---
# <a name="fa_sum-er-function"></a><span data-ttu-id="01d75-103">Функция ER FA_SUM</span><span class="sxs-lookup"><span data-stu-id="01d75-103">FA_SUM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01d75-104">Функция `FA_SUM` возвращает значение *Контейнер (запись)*, которое состоит из данных сумм основных средств для указанного элемента основных средств, кода модели стоимости и периода дат.</span><span class="sxs-lookup"><span data-stu-id="01d75-104">The `FA_SUM` function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span>

## <a name="syntax"></a><span data-ttu-id="01d75-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01d75-105">Syntax</span></span>

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a><span data-ttu-id="01d75-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="01d75-106">Arguments</span></span>

<span data-ttu-id="01d75-107">`fixed asset code`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="01d75-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="01d75-108">Значение *строка*, представляющее код элемента основного средства, для которого рассчитывается сальдо.</span><span class="sxs-lookup"><span data-stu-id="01d75-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="01d75-109">`value model code`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="01d75-109">`value model code`: *String*</span></span>

<span data-ttu-id="01d75-110">Значение *строка*, представляющее код модели стоимости, для которого рассчитывается сальдо.</span><span class="sxs-lookup"><span data-stu-id="01d75-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="01d75-111">`start date`: *Дата*</span><span class="sxs-lookup"><span data-stu-id="01d75-111">`start date`: *Date*</span></span>

<span data-ttu-id="01d75-112">Значение *Дата*, представляющее дату начала периода, для которого рассчитываются суммы основного средства.</span><span class="sxs-lookup"><span data-stu-id="01d75-112">A *Date* value that represents the start date of a period that the fixed asset amounts are calculated for.</span></span>

<span data-ttu-id="01d75-113">`end date`: *Дата*</span><span class="sxs-lookup"><span data-stu-id="01d75-113">`end date`: *Date*</span></span>

<span data-ttu-id="01d75-114">Значение *Дата*, представляющее дату окончания периода, для которого рассчитываются суммы основного средства.</span><span class="sxs-lookup"><span data-stu-id="01d75-114">A *Date* value that represents the end date of a period that the fixed asset amounts are calculated for.</span></span>

## <a name="return-values"></a><span data-ttu-id="01d75-115">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="01d75-115">Return values</span></span>

<span data-ttu-id="01d75-116">*Контейнер (запись)*</span><span class="sxs-lookup"><span data-stu-id="01d75-116">*Container (record)*</span></span>

<span data-ttu-id="01d75-117">Результирующее значение записи.</span><span class="sxs-lookup"><span data-stu-id="01d75-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="01d75-118">Пример</span><span class="sxs-lookup"><span data-stu-id="01d75-118">Example</span></span>

<span data-ttu-id="01d75-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` возвращает контейнер данных для основного средства **COMP-000001**, которое было подготовлено для модели стоимости **Current** и за период с **Date1** по **Date2**.</span><span class="sxs-lookup"><span data-stu-id="01d75-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returns the data container for fixed asset **COMP-000001** that has been prepared for the **Current** value model and for a period from **Date1** to **Date2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="01d75-120">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="01d75-120">Additional resources</span></span>

[<span data-ttu-id="01d75-121">Другие функции (характерные для конкретных бизнес-доменов)</span><span class="sxs-lookup"><span data-stu-id="01d75-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
