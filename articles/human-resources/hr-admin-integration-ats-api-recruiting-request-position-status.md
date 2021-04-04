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
ms.openlocfilehash: 01e8aa5157d0ad1c01f996886e7845e49ab97603
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464726"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="4b9bc-103">Статус должности запроса набора персонала</span><span class="sxs-lookup"><span data-stu-id="4b9bc-103">Recruiting request position status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="4b9bc-104">В этом разделе описывается набор параметров состояния должности для запроса на набор сотрудников для Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4b9bc-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="4b9bc-105">Физическое имя: mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="4b9bc-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="4b9bc-106">Это перечисление предоставляет набор параметров для значений статуса для каждой должности запрос на набор персонала в сущности RecruitingRequestPosition.</span><span class="sxs-lookup"><span data-stu-id="4b9bc-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="4b9bc-107">значение</span><span class="sxs-lookup"><span data-stu-id="4b9bc-107">Value</span></span> | <span data-ttu-id="4b9bc-108">Этикетка</span><span class="sxs-lookup"><span data-stu-id="4b9bc-108">Label</span></span> | <span data-ttu-id="4b9bc-109">описание</span><span class="sxs-lookup"><span data-stu-id="4b9bc-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="4b9bc-110">200000000</span><span class="sxs-lookup"><span data-stu-id="4b9bc-110">200000000</span></span> | <span data-ttu-id="4b9bc-111">Открытые</span><span class="sxs-lookup"><span data-stu-id="4b9bc-111">Open</span></span> | <span data-ttu-id="4b9bc-112">Должность в запросе на набор персонала открыта для набора сотрудников.</span><span class="sxs-lookup"><span data-stu-id="4b9bc-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="4b9bc-113">Это не означает, что для данной должности нет активного в данный момент назначения должности.</span><span class="sxs-lookup"><span data-stu-id="4b9bc-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="4b9bc-114">В должности на момент набора персонала может существовать сотрудник.</span><span class="sxs-lookup"><span data-stu-id="4b9bc-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="4b9bc-115">Оно указывает только на то, что должность доступна для найма в контексте запроса на набор сотрудников.</span><span class="sxs-lookup"><span data-stu-id="4b9bc-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="4b9bc-116">200000001</span><span class="sxs-lookup"><span data-stu-id="4b9bc-116">200000001</span></span> | <span data-ttu-id="4b9bc-117">Занята</span><span class="sxs-lookup"><span data-stu-id="4b9bc-117">Filled</span></span> | <span data-ttu-id="4b9bc-118">Сотрудник, выбранный для назначения на данную должность.</span><span class="sxs-lookup"><span data-stu-id="4b9bc-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="4b9bc-119">200000002</span><span class="sxs-lookup"><span data-stu-id="4b9bc-119">200000002</span></span> | <span data-ttu-id="4b9bc-120">Отменено</span><span class="sxs-lookup"><span data-stu-id="4b9bc-120">Canceled</span></span> | <span data-ttu-id="4b9bc-121">Запрос на набор сотрудников для этой должности отменен.</span><span class="sxs-lookup"><span data-stu-id="4b9bc-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="4b9bc-122">См. также</span><span class="sxs-lookup"><span data-stu-id="4b9bc-122">See also</span></span>

[<span data-ttu-id="4b9bc-123">Введение в интерфейс API интеграции системы отслеживания кандидатов</span><span class="sxs-lookup"><span data-stu-id="4b9bc-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="4b9bc-124">Пример запроса для запроса на набор персонала</span><span class="sxs-lookup"><span data-stu-id="4b9bc-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]