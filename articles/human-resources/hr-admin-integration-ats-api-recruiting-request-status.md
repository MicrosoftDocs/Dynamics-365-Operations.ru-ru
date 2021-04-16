---
title: Состояние запроса по набору сотрудников
description: В этом разделе описывается набор параметров состояния запроса на набор сотрудников для Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 888fbc511bffbecd837c929049006266191da5ba
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5806050"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="81616-103">Состояние запроса по набору сотрудников</span><span class="sxs-lookup"><span data-stu-id="81616-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="81616-104">В этом разделе описывается набор параметров состояния запроса на набор сотрудников для Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="81616-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="81616-105">Физическое имя: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="81616-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="81616-106">Это перечисление предоставляет набор параметров для значений состояния сущности RecruitingRequest.</span><span class="sxs-lookup"><span data-stu-id="81616-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="81616-107">значение</span><span class="sxs-lookup"><span data-stu-id="81616-107">Value</span></span> | <span data-ttu-id="81616-108">Этикетка</span><span class="sxs-lookup"><span data-stu-id="81616-108">Label</span></span> | <span data-ttu-id="81616-109">описание</span><span class="sxs-lookup"><span data-stu-id="81616-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="81616-110">200000000</span><span class="sxs-lookup"><span data-stu-id="81616-110">200000000</span></span> | <span data-ttu-id="81616-111">Черновой</span><span class="sxs-lookup"><span data-stu-id="81616-111">Draft</span></span> | <span data-ttu-id="81616-112">Запрос находится в состоянии черновика и не готов к активному набору сотрудников.</span><span class="sxs-lookup"><span data-stu-id="81616-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="81616-113">200000001</span><span class="sxs-lookup"><span data-stu-id="81616-113">200000001</span></span> | <span data-ttu-id="81616-114">На рассмотрении</span><span class="sxs-lookup"><span data-stu-id="81616-114">In Review</span></span> | <span data-ttu-id="81616-115">Запрос был отправлен и направляется на утверждение по рабочему процессу.</span><span class="sxs-lookup"><span data-stu-id="81616-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="81616-116">Доступно только в том случае, если включен рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="81616-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="81616-117">200000002</span><span class="sxs-lookup"><span data-stu-id="81616-117">200000002</span></span> | <span data-ttu-id="81616-118">Ожидает</span><span class="sxs-lookup"><span data-stu-id="81616-118">Pending</span></span> | <span data-ttu-id="81616-119">Запрос ожидает действия рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="81616-119">The request is pending workflow action.</span></span> <span data-ttu-id="81616-120">Доступно только в том случае, если включен рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="81616-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="81616-121">200000003</span><span class="sxs-lookup"><span data-stu-id="81616-121">200000003</span></span> | <span data-ttu-id="81616-122">Отменено</span><span class="sxs-lookup"><span data-stu-id="81616-122">Canceled</span></span> | <span data-ttu-id="81616-123">Запрос отменен.</span><span class="sxs-lookup"><span data-stu-id="81616-123">The request has been canceled.</span></span> <span data-ttu-id="81616-124">Доступно только в том случае, если включен рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="81616-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="81616-125">200000004</span><span class="sxs-lookup"><span data-stu-id="81616-125">200000004</span></span> | <span data-ttu-id="81616-126">Отказано</span><span class="sxs-lookup"><span data-stu-id="81616-126">Denied</span></span> | <span data-ttu-id="81616-127">Запрос был отклонен.</span><span class="sxs-lookup"><span data-stu-id="81616-127">The request has been denied.</span></span> <span data-ttu-id="81616-128">Доступно только в том случае, если включен рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="81616-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="81616-129">200000005</span><span class="sxs-lookup"><span data-stu-id="81616-129">200000005</span></span> | <span data-ttu-id="81616-130">Активные сотрудники</span><span class="sxs-lookup"><span data-stu-id="81616-130">Active</span></span> | <span data-ttu-id="81616-131">Все рабочие процессы выполнены и утверждены, и запрос готов к активному набору сотрудников.</span><span class="sxs-lookup"><span data-stu-id="81616-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="81616-132">200000006</span><span class="sxs-lookup"><span data-stu-id="81616-132">200000006</span></span> | <span data-ttu-id="81616-133">Закрытые</span><span class="sxs-lookup"><span data-stu-id="81616-133">Closed</span></span> | <span data-ttu-id="81616-134">Запроса на набор сотрудников закрыт.</span><span class="sxs-lookup"><span data-stu-id="81616-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="81616-135">См. также</span><span class="sxs-lookup"><span data-stu-id="81616-135">See also</span></span>

[<span data-ttu-id="81616-136">Введение в интерфейс API интеграции системы отслеживания кандидатов</span><span class="sxs-lookup"><span data-stu-id="81616-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="81616-137">Пример запроса для запроса на набор персонала</span><span class="sxs-lookup"><span data-stu-id="81616-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]