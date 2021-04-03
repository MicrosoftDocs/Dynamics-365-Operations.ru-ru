---
title: Состояние запроса по набору сотрудников
description: В этом разделе описывается набор параметров состояния запроса на набор сотрудников для Dynamics 365 Human Resources.
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
ms.openlocfilehash: 0032e6bfdbfd2792dafda8bf24a1b0cbc551740d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464654"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="01e74-103">Состояние запроса по набору сотрудников</span><span class="sxs-lookup"><span data-stu-id="01e74-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="01e74-104">В этом разделе описывается набор параметров состояния запроса на набор сотрудников для Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="01e74-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="01e74-105">Физическое имя: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="01e74-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="01e74-106">Это перечисление предоставляет набор параметров для значений состояния сущности RecruitingRequest.</span><span class="sxs-lookup"><span data-stu-id="01e74-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="01e74-107">значение</span><span class="sxs-lookup"><span data-stu-id="01e74-107">Value</span></span> | <span data-ttu-id="01e74-108">Этикетка</span><span class="sxs-lookup"><span data-stu-id="01e74-108">Label</span></span> | <span data-ttu-id="01e74-109">описание</span><span class="sxs-lookup"><span data-stu-id="01e74-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="01e74-110">200000000</span><span class="sxs-lookup"><span data-stu-id="01e74-110">200000000</span></span> | <span data-ttu-id="01e74-111">Черновой</span><span class="sxs-lookup"><span data-stu-id="01e74-111">Draft</span></span> | <span data-ttu-id="01e74-112">Запрос находится в состоянии черновика и не готов к активному набору сотрудников.</span><span class="sxs-lookup"><span data-stu-id="01e74-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="01e74-113">200000001</span><span class="sxs-lookup"><span data-stu-id="01e74-113">200000001</span></span> | <span data-ttu-id="01e74-114">На рассмотрении</span><span class="sxs-lookup"><span data-stu-id="01e74-114">In Review</span></span> | <span data-ttu-id="01e74-115">Запрос был отправлен и направляется на утверждение по рабочему процессу.</span><span class="sxs-lookup"><span data-stu-id="01e74-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="01e74-116">Доступно только в том случае, если включен рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="01e74-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="01e74-117">200000002</span><span class="sxs-lookup"><span data-stu-id="01e74-117">200000002</span></span> | <span data-ttu-id="01e74-118">Ожидает</span><span class="sxs-lookup"><span data-stu-id="01e74-118">Pending</span></span> | <span data-ttu-id="01e74-119">Запрос ожидает действия рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="01e74-119">The request is pending workflow action.</span></span> <span data-ttu-id="01e74-120">Доступно только в том случае, если включен рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="01e74-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="01e74-121">200000003</span><span class="sxs-lookup"><span data-stu-id="01e74-121">200000003</span></span> | <span data-ttu-id="01e74-122">Отменено</span><span class="sxs-lookup"><span data-stu-id="01e74-122">Canceled</span></span> | <span data-ttu-id="01e74-123">Запрос отменен.</span><span class="sxs-lookup"><span data-stu-id="01e74-123">The request has been canceled.</span></span> <span data-ttu-id="01e74-124">Доступно только в том случае, если включен рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="01e74-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="01e74-125">200000004</span><span class="sxs-lookup"><span data-stu-id="01e74-125">200000004</span></span> | <span data-ttu-id="01e74-126">Отказано</span><span class="sxs-lookup"><span data-stu-id="01e74-126">Denied</span></span> | <span data-ttu-id="01e74-127">Запрос был отклонен.</span><span class="sxs-lookup"><span data-stu-id="01e74-127">The request has been denied.</span></span> <span data-ttu-id="01e74-128">Доступно только в том случае, если включен рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="01e74-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="01e74-129">200000005</span><span class="sxs-lookup"><span data-stu-id="01e74-129">200000005</span></span> | <span data-ttu-id="01e74-130">Активные сотрудники</span><span class="sxs-lookup"><span data-stu-id="01e74-130">Active</span></span> | <span data-ttu-id="01e74-131">Все рабочие процессы выполнены и утверждены, и запрос готов к активному набору сотрудников.</span><span class="sxs-lookup"><span data-stu-id="01e74-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="01e74-132">200000006</span><span class="sxs-lookup"><span data-stu-id="01e74-132">200000006</span></span> | <span data-ttu-id="01e74-133">Закрытые</span><span class="sxs-lookup"><span data-stu-id="01e74-133">Closed</span></span> | <span data-ttu-id="01e74-134">Запроса на набор сотрудников закрыт.</span><span class="sxs-lookup"><span data-stu-id="01e74-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="01e74-135">См. также</span><span class="sxs-lookup"><span data-stu-id="01e74-135">See also</span></span>

[<span data-ttu-id="01e74-136">Введение в интерфейс API интеграции системы отслеживания кандидатов</span><span class="sxs-lookup"><span data-stu-id="01e74-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="01e74-137">Пример запроса для запроса на набор персонала</span><span class="sxs-lookup"><span data-stu-id="01e74-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]