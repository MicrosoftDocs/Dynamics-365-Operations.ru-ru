---
title: Статус должности запроса набора персонала
description: В этом разделе описывается набор параметров состояния должности для запроса на набор сотрудников для Dynamics 365 Human Resources.
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
ms.openlocfilehash: e287ec4b9b78194b76ef3c993c6ce32f808e26f9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051889"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="23ea5-103">Статус должности запроса набора персонала</span><span class="sxs-lookup"><span data-stu-id="23ea5-103">Recruiting request position status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="23ea5-104">В этом разделе описывается набор параметров состояния должности для запроса на набор сотрудников для Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="23ea5-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="23ea5-105">Физическое имя: mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="23ea5-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="23ea5-106">Это перечисление предоставляет набор параметров для значений статуса для каждой должности запрос на набор персонала в сущности RecruitingRequestPosition.</span><span class="sxs-lookup"><span data-stu-id="23ea5-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="23ea5-107">значение</span><span class="sxs-lookup"><span data-stu-id="23ea5-107">Value</span></span> | <span data-ttu-id="23ea5-108">Этикетка</span><span class="sxs-lookup"><span data-stu-id="23ea5-108">Label</span></span> | <span data-ttu-id="23ea5-109">описание</span><span class="sxs-lookup"><span data-stu-id="23ea5-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="23ea5-110">200000000</span><span class="sxs-lookup"><span data-stu-id="23ea5-110">200000000</span></span> | <span data-ttu-id="23ea5-111">Открытые</span><span class="sxs-lookup"><span data-stu-id="23ea5-111">Open</span></span> | <span data-ttu-id="23ea5-112">Должность в запросе на набор персонала открыта для набора сотрудников.</span><span class="sxs-lookup"><span data-stu-id="23ea5-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="23ea5-113">Это не означает, что для данной должности нет активного в данный момент назначения должности.</span><span class="sxs-lookup"><span data-stu-id="23ea5-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="23ea5-114">В должности на момент набора персонала может существовать сотрудник.</span><span class="sxs-lookup"><span data-stu-id="23ea5-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="23ea5-115">Оно указывает только на то, что должность доступна для найма в контексте запроса на набор сотрудников.</span><span class="sxs-lookup"><span data-stu-id="23ea5-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="23ea5-116">200000001</span><span class="sxs-lookup"><span data-stu-id="23ea5-116">200000001</span></span> | <span data-ttu-id="23ea5-117">Занята</span><span class="sxs-lookup"><span data-stu-id="23ea5-117">Filled</span></span> | <span data-ttu-id="23ea5-118">Сотрудник, выбранный для назначения на данную должность.</span><span class="sxs-lookup"><span data-stu-id="23ea5-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="23ea5-119">200000002</span><span class="sxs-lookup"><span data-stu-id="23ea5-119">200000002</span></span> | <span data-ttu-id="23ea5-120">Отменено</span><span class="sxs-lookup"><span data-stu-id="23ea5-120">Canceled</span></span> | <span data-ttu-id="23ea5-121">Запрос на набор сотрудников для этой должности отменен.</span><span class="sxs-lookup"><span data-stu-id="23ea5-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="23ea5-122">См. также</span><span class="sxs-lookup"><span data-stu-id="23ea5-122">See also</span></span>

[<span data-ttu-id="23ea5-123">Введение в интерфейс API интеграции системы отслеживания кандидатов</span><span class="sxs-lookup"><span data-stu-id="23ea5-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="23ea5-124">Пример запроса для запроса на набор персонала</span><span class="sxs-lookup"><span data-stu-id="23ea5-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]