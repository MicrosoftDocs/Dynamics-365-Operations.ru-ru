---
title: Методология соглашения по амортизации за полугодие
description: В этой теме описывается метод, используемый для основных средств для расчета амортизации с использованием полугодового соглашения, который рассчитывает шесть месяцев амортизации в течение первого и последнего года эксплуатации.
author: moaamer
ms.date: 08/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-17
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: d0e33128c37e970ebf5af87bd601ae30aef96952
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818592"
---
# <a name="half-year-depreciation-convention-methodology"></a><span data-ttu-id="bfca4-103">Методология соглашения по амортизации за полугодие</span><span class="sxs-lookup"><span data-stu-id="bfca4-103">Half-year depreciation convention methodology</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="bfca4-104">В этой теме описывается метод, используемый в модуле основных средств для расчета амортизации с использованием полугодового соглашения.</span><span class="sxs-lookup"><span data-stu-id="bfca4-104">This topic describes the method that is used in fixed assets to calculate depreciation using the half-year convention.</span></span> <span data-ttu-id="bfca4-105">Полугодовое соглашение рассчитывает шесть месяцев амортизации в течение первого и последнего года эксплуатации актива.</span><span class="sxs-lookup"><span data-stu-id="bfca4-105">The half-year convention calculates six months of depreciation during an asset’s first and last year of service.</span></span> <span data-ttu-id="bfca4-106">Дополнительные сведения о соглашениях по амортизации см. в разделе [Методы амортизации и соглашения по амортизации](Fixed-asset-depreciation-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="bfca4-106">For more information about depreciation conventions, see [Depreciation methods and conventions](Fixed-asset-depreciation-conventions.md).</span></span> 

<span data-ttu-id="bfca4-107">При использовании соглашения по амортизации за шесть месяцев система использует год приобретения или год, в котором актив был введен в эксплуатацию, затем рассчитывается пять лет амортизации с этого года, затем добавляется шесть месяцев.</span><span class="sxs-lookup"><span data-stu-id="bfca4-107">When you use the six-month depreciation convention, the system uses the acquisition year or the year that the asset was placed in service, then calculates five years of depreciation from that year, and then adds six months.</span></span> <span data-ttu-id="bfca4-108">Чтобы продемонстрировать этот процесс, рассмотрим актив, приобретенный за цену 50 000, и введенный в эксплуатацию в апреле 2020 года.</span><span class="sxs-lookup"><span data-stu-id="bfca4-108">To illustrate this process, consider an asset that was acquired for the price of 50,000, and placed in service in April 2020.</span></span> <span data-ttu-id="bfca4-109">Также предположим, что актив имеет пять лет срока службы.</span><span class="sxs-lookup"><span data-stu-id="bfca4-109">Also assume that the asset has a five-year service life.</span></span>

<span data-ttu-id="bfca4-110">Первый год эксплуатации завершается в декабре 2020 года, что означает завершение пяти лет срока службы в декабре 2024 года.</span><span class="sxs-lookup"><span data-stu-id="bfca4-110">The first year of service will conclude in December 2020, which means the end of the asset’s five-year service life will be December 2024.</span></span> <span data-ttu-id="bfca4-111">Соглашение по амортизации за полугодие добавляет в срок службы актива шесть месяцев, что означает, что его срок службы заканчивается в июне 2025 года.</span><span class="sxs-lookup"><span data-stu-id="bfca4-111">The half-year depreciation convention will add six months to the asset’s life, which means its service life will end in June 2025.</span></span> 

> <span data-ttu-id="bfca4-112">Ежегодная амортизация 50 000/5 = 10 000 месячная амортизация 10 000/12 = 833,33</span><span class="sxs-lookup"><span data-stu-id="bfca4-112">Yearly depreciation 50,000/5 = 10,000 monthly depreciation 10,000/12 = 833.33</span></span> <br>
> <span data-ttu-id="bfca4-113">Амортизация за первый год равна 10 000/2 = 5 000, и последующая ежемесячная амортизация 5 000/9 = 555,56</span><span class="sxs-lookup"><span data-stu-id="bfca4-113">First year depreciation 10,000/2 = 5,000  and the subsequent monthly depreciation 5,000/9 = 555.56</span></span>

   <span data-ttu-id="bfca4-114">[![График амортизации для соглашения об амортизации за полугодие](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)</span><span class="sxs-lookup"><span data-stu-id="bfca4-114">[![Depreciation schedule for half-year depreciation convention](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)</span></span>

<span data-ttu-id="bfca4-115">Расширенные периоды амортизации, добавленные с помощью полугодового соглашения, обеспечивают более точное распределение амортизации.</span><span class="sxs-lookup"><span data-stu-id="bfca4-115">The extended depreciation periods that are added by the half-year convention provide more accurate allocation of depreciation.</span></span> <span data-ttu-id="bfca4-116">Соглашение на шесть месяцев представляет расходы на амортизацию более ровными, что полезно для отчетности по отчету о прибылях и убытках.</span><span class="sxs-lookup"><span data-stu-id="bfca4-116">The six-month convention represents depreciation expenses more equally, which is useful for reporting on the profit and loss statement.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]