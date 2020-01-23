---
title: Функция ER FA_BALANCE
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности FA_BALANCE.
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
ms.openlocfilehash: 0907cb8cb4bc1e90b9fb59eccedb699a894b5cc9
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916024"
---
# <span data-ttu-id="4df73-103"><a name="FA_BALANCE">Функция ER FA_BALANCE</a></span><span class="sxs-lookup"><span data-stu-id="4df73-103"><a name="FA_BALANCE">FA_BALANCE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4df73-104">Функция `FA_BALANCE` возвращает значение *Контейнер (запись)*, которое состоит из данных баланса основных средств для указанного элемента основных средств, кода модели стоимости, отчетного года и даты отчетности.</span><span class="sxs-lookup"><span data-stu-id="4df73-104">The `FA_BALANCE` function returns a *Container (record)* value that consists of data for the fixed asset balance for the specified fixed asset item, value model code, reporting year, and reporting date.</span></span>

## <a name="syntax"></a><span data-ttu-id="4df73-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4df73-105">Syntax</span></span>

```
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a><span data-ttu-id="4df73-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="4df73-106">Arguments</span></span>

<span data-ttu-id="4df73-107">`fixed asset code`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="4df73-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="4df73-108">Значение *строка*, представляющее код элемента основного средства, для которого рассчитывается сальдо.</span><span class="sxs-lookup"><span data-stu-id="4df73-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="4df73-109">`value model code`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="4df73-109">`value model code`: *String*</span></span>

<span data-ttu-id="4df73-110">Значение *строка*, представляющее код модели стоимости, для которого рассчитывается сальдо.</span><span class="sxs-lookup"><span data-stu-id="4df73-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="4df73-111">`reporting year`: *Значение перечисления*</span><span class="sxs-lookup"><span data-stu-id="4df73-111">`reporting year`: *Enumeration value*</span></span>

<span data-ttu-id="4df73-112">Значения перечисления приложения **AssetYear**, определяющее период для расчета сальдо.</span><span class="sxs-lookup"><span data-stu-id="4df73-112">An enumeration value of the **AssetYear** application enumeration that defines a period for the balance calculation.</span></span>

<span data-ttu-id="4df73-113">`reporting date`: *Дата*</span><span class="sxs-lookup"><span data-stu-id="4df73-113">`reporting date`: *Date*</span></span>

<span data-ttu-id="4df73-114">Значение *Дата*, определяющее дату расчета сальдо.</span><span class="sxs-lookup"><span data-stu-id="4df73-114">A *Date* value that defines a date for the balance calculation.</span></span>

## <a name="return-values"></a><span data-ttu-id="4df73-115">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="4df73-115">Return values</span></span>

<span data-ttu-id="4df73-116">*Контейнер (запись)*</span><span class="sxs-lookup"><span data-stu-id="4df73-116">*Container (record)*</span></span>

<span data-ttu-id="4df73-117">Результирующее значение записи.</span><span class="sxs-lookup"><span data-stu-id="4df73-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="4df73-118">Пример</span><span class="sxs-lookup"><span data-stu-id="4df73-118">Example</span></span>

<span data-ttu-id="4df73-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` возвращает подготовленный контейнер данных сальдо для основного средства **COMP-000001**, подготовленного с моделью стоимости **Current** для даты текущего сеанса приложения.</span><span class="sxs-lookup"><span data-stu-id="4df73-119">`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returns the data container of balances for fixed asset **COMP-000001** that has been prepared for the **Current** value model on the current application session date.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4df73-120">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4df73-120">Additional resources</span></span>

[<span data-ttu-id="4df73-121">Другие функции (характерные для конкретных бизнес-доменов)</span><span class="sxs-lookup"><span data-stu-id="4df73-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
