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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 03bed091350b39601edb22b5af6bda5a83af47eb
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041362"
---
# <span data-ttu-id="743f8-103"><a name="FA_SUM">Функция ER FA_SUM</a></span><span class="sxs-lookup"><span data-stu-id="743f8-103"><a name="FA_SUM">FA_SUM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="743f8-104">Функция `FA_SUM` возвращает значение *Контейнер (запись)*, которое состоит из данных сумм основных средств для указанного элемента основных средств, кода модели стоимости и периода дат.</span><span class="sxs-lookup"><span data-stu-id="743f8-104">The `FA_SUM` function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span>

## <a name="syntax"></a><span data-ttu-id="743f8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="743f8-105">Syntax</span></span>

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a><span data-ttu-id="743f8-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="743f8-106">Arguments</span></span>

<span data-ttu-id="743f8-107">`fixed asset code`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="743f8-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="743f8-108">Значение *строка*, представляющее код элемента основного средства, для которого рассчитывается сальдо.</span><span class="sxs-lookup"><span data-stu-id="743f8-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="743f8-109">`value model code`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="743f8-109">`value model code`: *String*</span></span>

<span data-ttu-id="743f8-110">Значение *строка*, представляющее код модели стоимости, для которого рассчитывается сальдо.</span><span class="sxs-lookup"><span data-stu-id="743f8-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="743f8-111">`start date`: *Дата*</span><span class="sxs-lookup"><span data-stu-id="743f8-111">`start date`: *Date*</span></span>

<span data-ttu-id="743f8-112">Значение *Дата*, представляющее дату начала периода, для которого рассчитываются суммы основного средства.</span><span class="sxs-lookup"><span data-stu-id="743f8-112">A *Date* value that represents the start date of a period that the fixed asset amounts are calculated for.</span></span>

<span data-ttu-id="743f8-113">`end date`: *Дата*</span><span class="sxs-lookup"><span data-stu-id="743f8-113">`end date`: *Date*</span></span>

<span data-ttu-id="743f8-114">Значение *Дата*, представляющее дату окончания периода, для которого рассчитываются суммы основного средства.</span><span class="sxs-lookup"><span data-stu-id="743f8-114">A *Date* value that represents the end date of a period that the fixed asset amounts are calculated for.</span></span>

## <a name="return-values"></a><span data-ttu-id="743f8-115">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="743f8-115">Return values</span></span>

<span data-ttu-id="743f8-116">*Контейнер (запись)*</span><span class="sxs-lookup"><span data-stu-id="743f8-116">*Container (record)*</span></span>

<span data-ttu-id="743f8-117">Результирующее значение записи.</span><span class="sxs-lookup"><span data-stu-id="743f8-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="743f8-118">Пример</span><span class="sxs-lookup"><span data-stu-id="743f8-118">Example</span></span>

<span data-ttu-id="743f8-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` возвращает контейнер данных для основного средства **COMP-000001**, которое было подготовлено для модели стоимости **Current** и за период с **Date1** по **Date2**.</span><span class="sxs-lookup"><span data-stu-id="743f8-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returns the data container for fixed asset **COMP-000001** that has been prepared for the **Current** value model and for a period from **Date1** to **Date2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="743f8-120">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="743f8-120">Additional resources</span></span>

[<span data-ttu-id="743f8-121">Другие функции (характерные для конкретных бизнес-доменов)</span><span class="sxs-lookup"><span data-stu-id="743f8-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
