---
title: Результат интеграции кандидата
description: В этом разделе описывается набор параметров результата интеграции заявителя для Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8bef974abff18d7c07ecd679b7e01b31ea1459c4
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053907"
---
# <a name="applicant-integration-result"></a><span data-ttu-id="f92bc-103">Результат интеграции кандидата</span><span class="sxs-lookup"><span data-stu-id="f92bc-103">Applicant integration result</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f92bc-104">В этом разделе описывается набор параметров результата интеграции заявителя для Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f92bc-104">This topic describes the Applicant integration result option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="f92bc-105">Физическое имя: mshr_hcmapplicantintegrationresult</span><span class="sxs-lookup"><span data-stu-id="f92bc-105">Physical name: mshr_hcmapplicantintegrationresult</span></span>

<span data-ttu-id="f92bc-106">Это перечисление предоставляет статус для записи кандидата.</span><span class="sxs-lookup"><span data-stu-id="f92bc-106">This enumeration provides status for a candidate record.</span></span>

| <span data-ttu-id="f92bc-107">значение</span><span class="sxs-lookup"><span data-stu-id="f92bc-107">Value</span></span> | <span data-ttu-id="f92bc-108">Этикетка</span><span class="sxs-lookup"><span data-stu-id="f92bc-108">Label</span></span> | <span data-ttu-id="f92bc-109">описание</span><span class="sxs-lookup"><span data-stu-id="f92bc-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="f92bc-110">200000000</span><span class="sxs-lookup"><span data-stu-id="f92bc-110">200000000</span></span> | <span data-ttu-id="f92bc-111">Не обработано</span><span class="sxs-lookup"><span data-stu-id="f92bc-111">Not processed</span></span> | <span data-ttu-id="f92bc-112">Кандидат все еще находится в процессе рассмотрения.</span><span class="sxs-lookup"><span data-stu-id="f92bc-112">Candidate is still under consideration.</span></span> |
| <span data-ttu-id="f92bc-113">200000001</span><span class="sxs-lookup"><span data-stu-id="f92bc-113">200000001</span></span> | <span data-ttu-id="f92bc-114">Принят</span><span class="sxs-lookup"><span data-stu-id="f92bc-114">Hired</span></span> | <span data-ttu-id="f92bc-115">Кандидат был принят на работу.</span><span class="sxs-lookup"><span data-stu-id="f92bc-115">The candidate has been hired.</span></span> |
| <span data-ttu-id="f92bc-116">200000002</span><span class="sxs-lookup"><span data-stu-id="f92bc-116">200000002</span></span> | <span data-ttu-id="f92bc-117">Не принят на работу</span><span class="sxs-lookup"><span data-stu-id="f92bc-117">Not hired</span></span> | <span data-ttu-id="f92bc-118">Принято решение не нанимать кандидата.</span><span class="sxs-lookup"><span data-stu-id="f92bc-118">Decision was made to not hire the candidate.</span></span> |
| <span data-ttu-id="f92bc-119">200000003</span><span class="sxs-lookup"><span data-stu-id="f92bc-119">200000003</span></span> | <span data-ttu-id="f92bc-120">Отменено</span><span class="sxs-lookup"><span data-stu-id="f92bc-120">Dismissed</span></span> | <span data-ttu-id="f92bc-121">Кандидат был исключен из рассмотрения.</span><span class="sxs-lookup"><span data-stu-id="f92bc-121">The candidate was dismissed from consideration.</span></span> |

## <a name="see-also"></a><span data-ttu-id="f92bc-122">См. также</span><span class="sxs-lookup"><span data-stu-id="f92bc-122">See also</span></span>

[<span data-ttu-id="f92bc-123">Введение в интерфейс API интеграции системы отслеживания кандидатов</span><span class="sxs-lookup"><span data-stu-id="f92bc-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="f92bc-124">Пример запроса кандидата для приема на работу</span><span class="sxs-lookup"><span data-stu-id="f92bc-124">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]