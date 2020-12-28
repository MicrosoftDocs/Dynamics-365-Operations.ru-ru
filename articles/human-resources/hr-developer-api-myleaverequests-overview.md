---
title: Обзор MyLeaveRequests
description: Объект MyLeaveRequests в Microsoft Dynamics 365 Human Resources предоставляет список запросов отпусков в системе с областью действия (ограниченной) для запросов, доступных текущему пользователю, запрашивающему объект.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4bf3b298af9eb39e03514a4005afb43a42908e47
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420173"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="d50b0-103">Обзор MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="d50b0-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="d50b0-104">Объект MyLeaveRequests в Microsoft Dynamics 365 Human Resources предоставляет список запросов отпусков в системе с областью действия (ограниченной) для запросов, доступных текущему пользователю, запрашивающему объект.</span><span class="sxs-lookup"><span data-stu-id="d50b0-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="d50b0-105">Ключ</span><span class="sxs-lookup"><span data-stu-id="d50b0-105">Key</span></span>

  | <span data-ttu-id="d50b0-106">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="d50b0-106">Property Name</span></span> | <span data-ttu-id="d50b0-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d50b0-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="d50b0-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="d50b0-108">dataAreaId</span></span>    | <span data-ttu-id="d50b0-109">Строка</span><span class="sxs-lookup"><span data-stu-id="d50b0-109">String</span></span>    |
  | <span data-ttu-id="d50b0-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="d50b0-110">RequestId</span></span>     | <span data-ttu-id="d50b0-111">Строка</span><span class="sxs-lookup"><span data-stu-id="d50b0-111">String</span></span>    |
  | <span data-ttu-id="d50b0-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="d50b0-112">LeaveType</span></span>     | <span data-ttu-id="d50b0-113">Строка</span><span class="sxs-lookup"><span data-stu-id="d50b0-113">String</span></span>    |
  | <span data-ttu-id="d50b0-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="d50b0-114">LeaveDate</span></span>     | <span data-ttu-id="d50b0-115">Дата</span><span class="sxs-lookup"><span data-stu-id="d50b0-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="d50b0-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="d50b0-116">Properties</span></span>

  | <span data-ttu-id="d50b0-117">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="d50b0-117">Property Name</span></span>     | <span data-ttu-id="d50b0-118">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d50b0-118">Data Type</span></span> | <span data-ttu-id="d50b0-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d50b0-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="d50b0-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="d50b0-120">dataAreaId</span></span>        | <span data-ttu-id="d50b0-121">Строка</span><span class="sxs-lookup"><span data-stu-id="d50b0-121">String</span></span>    | <span data-ttu-id="d50b0-122">Х</span><span class="sxs-lookup"><span data-stu-id="d50b0-122">X</span></span>        |
  | <span data-ttu-id="d50b0-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="d50b0-123">RequestId</span></span>         | <span data-ttu-id="d50b0-124">Строка</span><span class="sxs-lookup"><span data-stu-id="d50b0-124">String</span></span>    | <span data-ttu-id="d50b0-125">Х</span><span class="sxs-lookup"><span data-stu-id="d50b0-125">X</span></span>        |
  | <span data-ttu-id="d50b0-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="d50b0-126">LeaveType</span></span>         | <span data-ttu-id="d50b0-127">Строка</span><span class="sxs-lookup"><span data-stu-id="d50b0-127">String</span></span>    | <span data-ttu-id="d50b0-128">Х</span><span class="sxs-lookup"><span data-stu-id="d50b0-128">X</span></span>        |
  | <span data-ttu-id="d50b0-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="d50b0-129">LeaveDate</span></span>         | <span data-ttu-id="d50b0-130">Дата</span><span class="sxs-lookup"><span data-stu-id="d50b0-130">Date</span></span>      | <span data-ttu-id="d50b0-131">Х</span><span class="sxs-lookup"><span data-stu-id="d50b0-131">X</span></span>        |
  | <span data-ttu-id="d50b0-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="d50b0-132">ReasonCodeId</span></span>      | <span data-ttu-id="d50b0-133">Строка</span><span class="sxs-lookup"><span data-stu-id="d50b0-133">String</span></span>    |          |
  | <span data-ttu-id="d50b0-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="d50b0-134">PersonnelNumber</span></span>   | <span data-ttu-id="d50b0-135">Строка</span><span class="sxs-lookup"><span data-stu-id="d50b0-135">String</span></span>    | <span data-ttu-id="d50b0-136">Х</span><span class="sxs-lookup"><span data-stu-id="d50b0-136">X</span></span>        |
  | <span data-ttu-id="d50b0-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="d50b0-137">RequestDate</span></span>       | <span data-ttu-id="d50b0-138">Дата</span><span class="sxs-lookup"><span data-stu-id="d50b0-138">Date</span></span>      | <span data-ttu-id="d50b0-139">Х</span><span class="sxs-lookup"><span data-stu-id="d50b0-139">X</span></span>        |
  | <span data-ttu-id="d50b0-140">Комментарий</span><span class="sxs-lookup"><span data-stu-id="d50b0-140">Comment</span></span>           | <span data-ttu-id="d50b0-141">Строка</span><span class="sxs-lookup"><span data-stu-id="d50b0-141">String</span></span>    |          |
  | <span data-ttu-id="d50b0-142">Состояние</span><span class="sxs-lookup"><span data-stu-id="d50b0-142">Status</span></span>            | <span data-ttu-id="d50b0-143">Перечислимый тип</span><span class="sxs-lookup"><span data-stu-id="d50b0-143">Enum</span></span>      | <span data-ttu-id="d50b0-144">Х</span><span class="sxs-lookup"><span data-stu-id="d50b0-144">X</span></span>        |
  | <span data-ttu-id="d50b0-145">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="d50b0-145">Amount</span></span>            | <span data-ttu-id="d50b0-146">Действующий</span><span class="sxs-lookup"><span data-stu-id="d50b0-146">Real</span></span>      |          |
  | <span data-ttu-id="d50b0-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="d50b0-147">HalfDayDefinition</span></span> | <span data-ttu-id="d50b0-148">Перечислимый тип</span><span class="sxs-lookup"><span data-stu-id="d50b0-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="d50b0-149">Действия</span><span class="sxs-lookup"><span data-stu-id="d50b0-149">Actions</span></span>

 | <span data-ttu-id="d50b0-150">Имя действия</span><span class="sxs-lookup"><span data-stu-id="d50b0-150">Action Name</span></span>                               | <span data-ttu-id="d50b0-151">Описание</span><span class="sxs-lookup"><span data-stu-id="d50b0-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="d50b0-152">submit</span><span class="sxs-lookup"><span data-stu-id="d50b0-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="d50b0-153">Отправка запроса, который должен обрабатываться workflow-процессом.</span><span class="sxs-lookup"><span data-stu-id="d50b0-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="d50b0-154">См. также</span><span class="sxs-lookup"><span data-stu-id="d50b0-154">See also</span></span>

- [<span data-ttu-id="d50b0-155">Отправка запроса на отпуск в workflow-процесс</span><span class="sxs-lookup"><span data-stu-id="d50b0-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="d50b0-156">Проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="d50b0-156">Authentication</span></span>](hr-developer-api-authentication.md)