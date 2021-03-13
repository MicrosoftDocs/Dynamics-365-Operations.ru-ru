---
title: Статус должности запроса набора персонала
description: В этом разделе описывается набор параметров состояния должности для запроса на набор сотрудников для Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3f7bae64f58f0bdc1603b3c1b5493f1ebcfa8de9
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126058"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="217d6-103">Статус должности запроса набора персонала</span><span class="sxs-lookup"><span data-stu-id="217d6-103">Recruiting request position status</span></span>

<span data-ttu-id="217d6-104">В этом разделе описывается набор параметров состояния должности для запроса на набор сотрудников для Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="217d6-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="217d6-105">Физическое имя: mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="217d6-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="217d6-106">Это перечисление предоставляет набор параметров для значений статуса для каждой должности запрос на набор персонала в сущности RecruitingRequestPosition.</span><span class="sxs-lookup"><span data-stu-id="217d6-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="217d6-107">значение</span><span class="sxs-lookup"><span data-stu-id="217d6-107">Value</span></span> | <span data-ttu-id="217d6-108">Этикетка</span><span class="sxs-lookup"><span data-stu-id="217d6-108">Label</span></span> | <span data-ttu-id="217d6-109">описание</span><span class="sxs-lookup"><span data-stu-id="217d6-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="217d6-110">200000000</span><span class="sxs-lookup"><span data-stu-id="217d6-110">200000000</span></span> | <span data-ttu-id="217d6-111">Открытые</span><span class="sxs-lookup"><span data-stu-id="217d6-111">Open</span></span> | <span data-ttu-id="217d6-112">Должность в запросе на набор персонала открыта для набора сотрудников.</span><span class="sxs-lookup"><span data-stu-id="217d6-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="217d6-113">Это не означает, что для данной должности нет активного в данный момент назначения должности.</span><span class="sxs-lookup"><span data-stu-id="217d6-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="217d6-114">В должности на момент набора персонала может существовать сотрудник.</span><span class="sxs-lookup"><span data-stu-id="217d6-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="217d6-115">Оно указывает только на то, что должность доступна для найма в контексте запроса на набор сотрудников.</span><span class="sxs-lookup"><span data-stu-id="217d6-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="217d6-116">200000001</span><span class="sxs-lookup"><span data-stu-id="217d6-116">200000001</span></span> | <span data-ttu-id="217d6-117">Занята</span><span class="sxs-lookup"><span data-stu-id="217d6-117">Filled</span></span> | <span data-ttu-id="217d6-118">Сотрудник, выбранный для назначения на данную должность.</span><span class="sxs-lookup"><span data-stu-id="217d6-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="217d6-119">200000002</span><span class="sxs-lookup"><span data-stu-id="217d6-119">200000002</span></span> | <span data-ttu-id="217d6-120">Отменено</span><span class="sxs-lookup"><span data-stu-id="217d6-120">Canceled</span></span> | <span data-ttu-id="217d6-121">Запрос на набор сотрудников для этой должности отменен.</span><span class="sxs-lookup"><span data-stu-id="217d6-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="217d6-122">См. также</span><span class="sxs-lookup"><span data-stu-id="217d6-122">See also</span></span>

[<span data-ttu-id="217d6-123">Введение в интерфейс API интеграции системы отслеживания кандидатов</span><span class="sxs-lookup"><span data-stu-id="217d6-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="217d6-124">Пример запроса для запроса на набор персонала</span><span class="sxs-lookup"><span data-stu-id="217d6-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)
