---
title: Функция ER CONVERTCURRENCY
description: Этот раздел содержит общие сведения об использовании функции электронной отчетности CONVERTCURRENCY.
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
ms.openlocfilehash: fb8f7f28f5a9bb27402544efcffa6393238e38d8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744375"
---
# <a name="convertcurrency-er-function"></a><span data-ttu-id="4606f-103">Функция ER CONVERTCURRENCY</span><span class="sxs-lookup"><span data-stu-id="4606f-103">CONVERTCURRENCY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4606f-104">Функция `CONVERTCURRENCY` возвращает *вещественное* значение, представляющее результат преобразования указанной денежной суммы от указанной валюты источника в указанную целевую валюту, используя настройки определенной компании на указанную дату.</span><span class="sxs-lookup"><span data-stu-id="4606f-104">The `CONVERTCURRENCY` function returns a *Real* value that represents the result of converting the specified monetary amount from the specified source currency to the specified target currency by using the settings of the specified company on the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="4606f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4606f-105">Syntax</span></span>

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a><span data-ttu-id="4606f-106">Аргументы</span><span class="sxs-lookup"><span data-stu-id="4606f-106">Arguments</span></span>

<span data-ttu-id="4606f-107">`amount`: *Целочисленный* или *Вещественный*</span><span class="sxs-lookup"><span data-stu-id="4606f-107">`amount`: *Integer* or *Real*</span></span>

<span data-ttu-id="4606f-108">Числовое значение, представляющее денежную сумму, которая должна быть конвертирована.</span><span class="sxs-lookup"><span data-stu-id="4606f-108">A numeric value that represents the monetary amount that must be converted.</span></span>

<span data-ttu-id="4606f-109">`source currency`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="4606f-109">`source currency`: *String*</span></span>

<span data-ttu-id="4606f-110">Код исходной валюты.</span><span class="sxs-lookup"><span data-stu-id="4606f-110">The code of the source currency.</span></span>

<span data-ttu-id="4606f-111">`target currency`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="4606f-111">`target currency`: *String*</span></span>

<span data-ttu-id="4606f-112">Код целевой валюты.</span><span class="sxs-lookup"><span data-stu-id="4606f-112">The code of the target currency.</span></span>

<span data-ttu-id="4606f-113">`date`: *Дата*</span><span class="sxs-lookup"><span data-stu-id="4606f-113">`date`: *Date*</span></span>

<span data-ttu-id="4606f-114">Значение *Дата*, представляющее дату, используемую для определения валютного курса для конвертации.</span><span class="sxs-lookup"><span data-stu-id="4606f-114">A *Date* value that represents the date that is used to determine the exchange rate for the conversion.</span></span>

<span data-ttu-id="4606f-115">`company`: *Строка*</span><span class="sxs-lookup"><span data-stu-id="4606f-115">`company`: *String*</span></span>

<span data-ttu-id="4606f-116">Значение *строка*, представляющее код компании, которая представляет параметры, используемые для конвертации.</span><span class="sxs-lookup"><span data-stu-id="4606f-116">A *String* value that represents the code of a company that supplies the settings that are used for the conversion.</span></span>

## <a name="return-values"></a><span data-ttu-id="4606f-117">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="4606f-117">Return values</span></span>

<span data-ttu-id="4606f-118">*Действующий*</span><span class="sxs-lookup"><span data-stu-id="4606f-118">*Real*</span></span>

<span data-ttu-id="4606f-119">Результирующее числовое значение.</span><span class="sxs-lookup"><span data-stu-id="4606f-119">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="4606f-120">Пример</span><span class="sxs-lookup"><span data-stu-id="4606f-120">Example</span></span>

<span data-ttu-id="4606f-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` возвращает эквивалент одного евро в долларах США на текущую дату сеанса на основе настроек для компании **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="4606f-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returns the equivalent of one euro in US dollars on the current session date, based on settings for the **DEMF** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4606f-122">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="4606f-122">Additional resources</span></span>

[<span data-ttu-id="4606f-123">Другие функции (характерные для конкретных бизнес-доменов)</span><span class="sxs-lookup"><span data-stu-id="4606f-123">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]