---
title: Обзор MyLeaveRequests
description: ''
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
ms.openlocfilehash: 66f161d6736b1bb544d02871d9d51b2949b1cfa0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010331"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="e73da-102">Обзор MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="e73da-102">MyLeaveRequests overview</span></span>

<span data-ttu-id="e73da-103">Объект MyLeaveRequests в Microsoft Dynamics 365 Human Resources предоставляет список запросов отпусков в системе с областью действия (ограниченной) для запросов, доступных текущему пользователю, запрашивающему объект.</span><span class="sxs-lookup"><span data-stu-id="e73da-103">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="e73da-104">Ключ</span><span class="sxs-lookup"><span data-stu-id="e73da-104">Key</span></span>

  | <span data-ttu-id="e73da-105">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="e73da-105">Property Name</span></span> | <span data-ttu-id="e73da-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e73da-106">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="e73da-107">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="e73da-107">dataAreaId</span></span>    | <span data-ttu-id="e73da-108">Строка</span><span class="sxs-lookup"><span data-stu-id="e73da-108">String</span></span>    |
  | <span data-ttu-id="e73da-109">RequestId</span><span class="sxs-lookup"><span data-stu-id="e73da-109">RequestId</span></span>     | <span data-ttu-id="e73da-110">Строка</span><span class="sxs-lookup"><span data-stu-id="e73da-110">String</span></span>    |
  | <span data-ttu-id="e73da-111">LeaveType</span><span class="sxs-lookup"><span data-stu-id="e73da-111">LeaveType</span></span>     | <span data-ttu-id="e73da-112">Строка</span><span class="sxs-lookup"><span data-stu-id="e73da-112">String</span></span>    |
  | <span data-ttu-id="e73da-113">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="e73da-113">LeaveDate</span></span>     | <span data-ttu-id="e73da-114">Дата</span><span class="sxs-lookup"><span data-stu-id="e73da-114">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="e73da-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="e73da-115">Properties</span></span>

  | <span data-ttu-id="e73da-116">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="e73da-116">Property Name</span></span>     | <span data-ttu-id="e73da-117">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e73da-117">Data Type</span></span> | <span data-ttu-id="e73da-118">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e73da-118">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="e73da-119">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="e73da-119">dataAreaId</span></span>        | <span data-ttu-id="e73da-120">Строка</span><span class="sxs-lookup"><span data-stu-id="e73da-120">String</span></span>    | <span data-ttu-id="e73da-121">Х</span><span class="sxs-lookup"><span data-stu-id="e73da-121">X</span></span>        |
  | <span data-ttu-id="e73da-122">RequestId</span><span class="sxs-lookup"><span data-stu-id="e73da-122">RequestId</span></span>         | <span data-ttu-id="e73da-123">Строка</span><span class="sxs-lookup"><span data-stu-id="e73da-123">String</span></span>    | <span data-ttu-id="e73da-124">Х</span><span class="sxs-lookup"><span data-stu-id="e73da-124">X</span></span>        |
  | <span data-ttu-id="e73da-125">LeaveType</span><span class="sxs-lookup"><span data-stu-id="e73da-125">LeaveType</span></span>         | <span data-ttu-id="e73da-126">Строка</span><span class="sxs-lookup"><span data-stu-id="e73da-126">String</span></span>    | <span data-ttu-id="e73da-127">Х</span><span class="sxs-lookup"><span data-stu-id="e73da-127">X</span></span>        |
  | <span data-ttu-id="e73da-128">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="e73da-128">LeaveDate</span></span>         | <span data-ttu-id="e73da-129">Дата</span><span class="sxs-lookup"><span data-stu-id="e73da-129">Date</span></span>      | <span data-ttu-id="e73da-130">Х</span><span class="sxs-lookup"><span data-stu-id="e73da-130">X</span></span>        |
  | <span data-ttu-id="e73da-131">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="e73da-131">ReasonCodeId</span></span>      | <span data-ttu-id="e73da-132">Строка</span><span class="sxs-lookup"><span data-stu-id="e73da-132">String</span></span>    |          |
  | <span data-ttu-id="e73da-133">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="e73da-133">PersonnelNumber</span></span>   | <span data-ttu-id="e73da-134">Строка</span><span class="sxs-lookup"><span data-stu-id="e73da-134">String</span></span>    | <span data-ttu-id="e73da-135">Х</span><span class="sxs-lookup"><span data-stu-id="e73da-135">X</span></span>        |
  | <span data-ttu-id="e73da-136">RequestDate</span><span class="sxs-lookup"><span data-stu-id="e73da-136">RequestDate</span></span>       | <span data-ttu-id="e73da-137">Дата</span><span class="sxs-lookup"><span data-stu-id="e73da-137">Date</span></span>      | <span data-ttu-id="e73da-138">Х</span><span class="sxs-lookup"><span data-stu-id="e73da-138">X</span></span>        |
  | <span data-ttu-id="e73da-139">Комментарий</span><span class="sxs-lookup"><span data-stu-id="e73da-139">Comment</span></span>           | <span data-ttu-id="e73da-140">Строка</span><span class="sxs-lookup"><span data-stu-id="e73da-140">String</span></span>    |          |
  | <span data-ttu-id="e73da-141">Состояние</span><span class="sxs-lookup"><span data-stu-id="e73da-141">Status</span></span>            | <span data-ttu-id="e73da-142">Перечислимый тип</span><span class="sxs-lookup"><span data-stu-id="e73da-142">Enum</span></span>      | <span data-ttu-id="e73da-143">Х</span><span class="sxs-lookup"><span data-stu-id="e73da-143">X</span></span>        |
  | <span data-ttu-id="e73da-144">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="e73da-144">Amount</span></span>            | <span data-ttu-id="e73da-145">Действующий</span><span class="sxs-lookup"><span data-stu-id="e73da-145">Real</span></span>      |          |
  | <span data-ttu-id="e73da-146">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="e73da-146">HalfDayDefinition</span></span> | <span data-ttu-id="e73da-147">Перечислимый тип</span><span class="sxs-lookup"><span data-stu-id="e73da-147">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="e73da-148">Действия</span><span class="sxs-lookup"><span data-stu-id="e73da-148">Actions</span></span>

 | <span data-ttu-id="e73da-149">Имя действия</span><span class="sxs-lookup"><span data-stu-id="e73da-149">Action Name</span></span>                               | <span data-ttu-id="e73da-150">Описание</span><span class="sxs-lookup"><span data-stu-id="e73da-150">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="e73da-151">submit</span><span class="sxs-lookup"><span data-stu-id="e73da-151">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="e73da-152">Отправка запроса, который должен обрабатываться workflow-процессом.</span><span class="sxs-lookup"><span data-stu-id="e73da-152">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="e73da-153">См. также</span><span class="sxs-lookup"><span data-stu-id="e73da-153">See also</span></span>

- [<span data-ttu-id="e73da-154">Отправка запроса на отпуск в workflow-процесс</span><span class="sxs-lookup"><span data-stu-id="e73da-154">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="e73da-155">Проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="e73da-155">Authentication</span></span>](hr-developer-api-authentication.md)