---
title: Состояние запроса по набору сотрудников
description: В этом разделе описывается набор параметров состояния запроса на набор сотрудников для Dynamics 365 Human Resources.
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
ms.openlocfilehash: 3b05cc531a84144708ff52913927bbd04574a3b2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059192"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="947b3-103">Состояние запроса по набору сотрудников</span><span class="sxs-lookup"><span data-stu-id="947b3-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="947b3-104">В этом разделе описывается набор параметров состояния запроса на набор сотрудников для Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="947b3-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="947b3-105">Физическое имя: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="947b3-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="947b3-106">Это перечисление предоставляет набор параметров для значений состояния сущности RecruitingRequest.</span><span class="sxs-lookup"><span data-stu-id="947b3-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="947b3-107">значение</span><span class="sxs-lookup"><span data-stu-id="947b3-107">Value</span></span> | <span data-ttu-id="947b3-108">Этикетка</span><span class="sxs-lookup"><span data-stu-id="947b3-108">Label</span></span> | <span data-ttu-id="947b3-109">описание</span><span class="sxs-lookup"><span data-stu-id="947b3-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="947b3-110">200000000</span><span class="sxs-lookup"><span data-stu-id="947b3-110">200000000</span></span> | <span data-ttu-id="947b3-111">Черновой</span><span class="sxs-lookup"><span data-stu-id="947b3-111">Draft</span></span> | <span data-ttu-id="947b3-112">Запрос находится в состоянии черновика и не готов к активному набору сотрудников.</span><span class="sxs-lookup"><span data-stu-id="947b3-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="947b3-113">200000001</span><span class="sxs-lookup"><span data-stu-id="947b3-113">200000001</span></span> | <span data-ttu-id="947b3-114">На рассмотрении</span><span class="sxs-lookup"><span data-stu-id="947b3-114">In Review</span></span> | <span data-ttu-id="947b3-115">Запрос был отправлен и направляется на утверждение по рабочему процессу.</span><span class="sxs-lookup"><span data-stu-id="947b3-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="947b3-116">Доступно только в том случае, если включен рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="947b3-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="947b3-117">200000002</span><span class="sxs-lookup"><span data-stu-id="947b3-117">200000002</span></span> | <span data-ttu-id="947b3-118">Ожидает</span><span class="sxs-lookup"><span data-stu-id="947b3-118">Pending</span></span> | <span data-ttu-id="947b3-119">Запрос ожидает действия рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="947b3-119">The request is pending workflow action.</span></span> <span data-ttu-id="947b3-120">Доступно только в том случае, если включен рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="947b3-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="947b3-121">200000003</span><span class="sxs-lookup"><span data-stu-id="947b3-121">200000003</span></span> | <span data-ttu-id="947b3-122">Отменено</span><span class="sxs-lookup"><span data-stu-id="947b3-122">Canceled</span></span> | <span data-ttu-id="947b3-123">Запрос отменен.</span><span class="sxs-lookup"><span data-stu-id="947b3-123">The request has been canceled.</span></span> <span data-ttu-id="947b3-124">Доступно только в том случае, если включен рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="947b3-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="947b3-125">200000004</span><span class="sxs-lookup"><span data-stu-id="947b3-125">200000004</span></span> | <span data-ttu-id="947b3-126">Отказано</span><span class="sxs-lookup"><span data-stu-id="947b3-126">Denied</span></span> | <span data-ttu-id="947b3-127">Запрос был отклонен.</span><span class="sxs-lookup"><span data-stu-id="947b3-127">The request has been denied.</span></span> <span data-ttu-id="947b3-128">Доступно только в том случае, если включен рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="947b3-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="947b3-129">200000005</span><span class="sxs-lookup"><span data-stu-id="947b3-129">200000005</span></span> | <span data-ttu-id="947b3-130">Активные сотрудники</span><span class="sxs-lookup"><span data-stu-id="947b3-130">Active</span></span> | <span data-ttu-id="947b3-131">Все рабочие процессы выполнены и утверждены, и запрос готов к активному набору сотрудников.</span><span class="sxs-lookup"><span data-stu-id="947b3-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="947b3-132">200000006</span><span class="sxs-lookup"><span data-stu-id="947b3-132">200000006</span></span> | <span data-ttu-id="947b3-133">Закрытые</span><span class="sxs-lookup"><span data-stu-id="947b3-133">Closed</span></span> | <span data-ttu-id="947b3-134">Запроса на набор сотрудников закрыт.</span><span class="sxs-lookup"><span data-stu-id="947b3-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="947b3-135">См. также</span><span class="sxs-lookup"><span data-stu-id="947b3-135">See also</span></span>

[<span data-ttu-id="947b3-136">Введение в интерфейс API интеграции системы отслеживания кандидатов</span><span class="sxs-lookup"><span data-stu-id="947b3-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="947b3-137">Пример запроса для запроса на набор персонала</span><span class="sxs-lookup"><span data-stu-id="947b3-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]