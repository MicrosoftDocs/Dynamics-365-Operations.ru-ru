---
title: Обзор MyLeaveRequests
description: Объект MyLeaveRequests в Microsoft Dynamics 365 Human Resources предоставляет список запросов отпусков в системе с областью действия (ограниченной) для запросов, доступных текущему пользователю, запрашивающему объект.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 0ca5bc225400338e76faee41a279e91fc00ce570
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115544"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="0f3f7-103">Обзор MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="0f3f7-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="0f3f7-104">Объект MyLeaveRequests в Microsoft Dynamics 365 Human Resources предоставляет список запросов отпусков в системе с областью действия (ограниченной) для запросов, доступных текущему пользователю, запрашивающему объект.</span><span class="sxs-lookup"><span data-stu-id="0f3f7-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="0f3f7-105">Ключ</span><span class="sxs-lookup"><span data-stu-id="0f3f7-105">Key</span></span>

  | <span data-ttu-id="0f3f7-106">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="0f3f7-106">Property Name</span></span> | <span data-ttu-id="0f3f7-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0f3f7-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="0f3f7-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="0f3f7-108">dataAreaId</span></span>    | <span data-ttu-id="0f3f7-109">Строка</span><span class="sxs-lookup"><span data-stu-id="0f3f7-109">String</span></span>    |
  | <span data-ttu-id="0f3f7-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="0f3f7-110">RequestId</span></span>     | <span data-ttu-id="0f3f7-111">Строка</span><span class="sxs-lookup"><span data-stu-id="0f3f7-111">String</span></span>    |
  | <span data-ttu-id="0f3f7-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="0f3f7-112">LeaveType</span></span>     | <span data-ttu-id="0f3f7-113">Строка</span><span class="sxs-lookup"><span data-stu-id="0f3f7-113">String</span></span>    |
  | <span data-ttu-id="0f3f7-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="0f3f7-114">LeaveDate</span></span>     | <span data-ttu-id="0f3f7-115">Дата</span><span class="sxs-lookup"><span data-stu-id="0f3f7-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="0f3f7-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="0f3f7-116">Properties</span></span>

  | <span data-ttu-id="0f3f7-117">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="0f3f7-117">Property Name</span></span>     | <span data-ttu-id="0f3f7-118">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0f3f7-118">Data Type</span></span> | <span data-ttu-id="0f3f7-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0f3f7-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="0f3f7-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="0f3f7-120">dataAreaId</span></span>        | <span data-ttu-id="0f3f7-121">Строка</span><span class="sxs-lookup"><span data-stu-id="0f3f7-121">String</span></span>    | <span data-ttu-id="0f3f7-122">Х</span><span class="sxs-lookup"><span data-stu-id="0f3f7-122">X</span></span>        |
  | <span data-ttu-id="0f3f7-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="0f3f7-123">RequestId</span></span>         | <span data-ttu-id="0f3f7-124">Строка</span><span class="sxs-lookup"><span data-stu-id="0f3f7-124">String</span></span>    | <span data-ttu-id="0f3f7-125">Х</span><span class="sxs-lookup"><span data-stu-id="0f3f7-125">X</span></span>        |
  | <span data-ttu-id="0f3f7-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="0f3f7-126">LeaveType</span></span>         | <span data-ttu-id="0f3f7-127">Строка</span><span class="sxs-lookup"><span data-stu-id="0f3f7-127">String</span></span>    | <span data-ttu-id="0f3f7-128">Х</span><span class="sxs-lookup"><span data-stu-id="0f3f7-128">X</span></span>        |
  | <span data-ttu-id="0f3f7-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="0f3f7-129">LeaveDate</span></span>         | <span data-ttu-id="0f3f7-130">Дата</span><span class="sxs-lookup"><span data-stu-id="0f3f7-130">Date</span></span>      | <span data-ttu-id="0f3f7-131">Х</span><span class="sxs-lookup"><span data-stu-id="0f3f7-131">X</span></span>        |
  | <span data-ttu-id="0f3f7-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="0f3f7-132">ReasonCodeId</span></span>      | <span data-ttu-id="0f3f7-133">Строка</span><span class="sxs-lookup"><span data-stu-id="0f3f7-133">String</span></span>    |          |
  | <span data-ttu-id="0f3f7-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="0f3f7-134">PersonnelNumber</span></span>   | <span data-ttu-id="0f3f7-135">Строка</span><span class="sxs-lookup"><span data-stu-id="0f3f7-135">String</span></span>    | <span data-ttu-id="0f3f7-136">Х</span><span class="sxs-lookup"><span data-stu-id="0f3f7-136">X</span></span>        |
  | <span data-ttu-id="0f3f7-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="0f3f7-137">RequestDate</span></span>       | <span data-ttu-id="0f3f7-138">Дата</span><span class="sxs-lookup"><span data-stu-id="0f3f7-138">Date</span></span>      | <span data-ttu-id="0f3f7-139">Х</span><span class="sxs-lookup"><span data-stu-id="0f3f7-139">X</span></span>        |
  | <span data-ttu-id="0f3f7-140">Комментарий</span><span class="sxs-lookup"><span data-stu-id="0f3f7-140">Comment</span></span>           | <span data-ttu-id="0f3f7-141">Строка</span><span class="sxs-lookup"><span data-stu-id="0f3f7-141">String</span></span>    |          |
  | <span data-ttu-id="0f3f7-142">Состояние</span><span class="sxs-lookup"><span data-stu-id="0f3f7-142">Status</span></span>            | <span data-ttu-id="0f3f7-143">Перечислимый тип</span><span class="sxs-lookup"><span data-stu-id="0f3f7-143">Enum</span></span>      | <span data-ttu-id="0f3f7-144">Х</span><span class="sxs-lookup"><span data-stu-id="0f3f7-144">X</span></span>        |
  | <span data-ttu-id="0f3f7-145">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="0f3f7-145">Amount</span></span>            | <span data-ttu-id="0f3f7-146">Действующий</span><span class="sxs-lookup"><span data-stu-id="0f3f7-146">Real</span></span>      |          |
  | <span data-ttu-id="0f3f7-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="0f3f7-147">HalfDayDefinition</span></span> | <span data-ttu-id="0f3f7-148">Перечислимый тип</span><span class="sxs-lookup"><span data-stu-id="0f3f7-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="0f3f7-149">Действия</span><span class="sxs-lookup"><span data-stu-id="0f3f7-149">Actions</span></span>

 | <span data-ttu-id="0f3f7-150">Имя действия</span><span class="sxs-lookup"><span data-stu-id="0f3f7-150">Action Name</span></span>                               | <span data-ttu-id="0f3f7-151">Описание</span><span class="sxs-lookup"><span data-stu-id="0f3f7-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="0f3f7-152">submit</span><span class="sxs-lookup"><span data-stu-id="0f3f7-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="0f3f7-153">Отправка запроса, который должен обрабатываться workflow-процессом.</span><span class="sxs-lookup"><span data-stu-id="0f3f7-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="0f3f7-154">См. также</span><span class="sxs-lookup"><span data-stu-id="0f3f7-154">See also</span></span>

- [<span data-ttu-id="0f3f7-155">Отправка запроса на отпуск в workflow-процесс</span><span class="sxs-lookup"><span data-stu-id="0f3f7-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="0f3f7-156">Проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="0f3f7-156">Authentication</span></span>](hr-developer-api-authentication.md)