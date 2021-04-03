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
ms.openlocfilehash: c2c14a0cc935ad166a2c6600f1e96c3e09ab16ca
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465518"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="9e68f-103">Обзор MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="9e68f-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9e68f-104">Объект MyLeaveRequests в Microsoft Dynamics 365 Human Resources предоставляет список запросов отпусков в системе с областью действия (ограниченной) для запросов, доступных текущему пользователю, запрашивающему объект.</span><span class="sxs-lookup"><span data-stu-id="9e68f-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="9e68f-105">Ключ</span><span class="sxs-lookup"><span data-stu-id="9e68f-105">Key</span></span>

  | <span data-ttu-id="9e68f-106">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="9e68f-106">Property Name</span></span> | <span data-ttu-id="9e68f-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9e68f-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="9e68f-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="9e68f-108">dataAreaId</span></span>    | <span data-ttu-id="9e68f-109">Строка</span><span class="sxs-lookup"><span data-stu-id="9e68f-109">String</span></span>    |
  | <span data-ttu-id="9e68f-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="9e68f-110">RequestId</span></span>     | <span data-ttu-id="9e68f-111">Строка</span><span class="sxs-lookup"><span data-stu-id="9e68f-111">String</span></span>    |
  | <span data-ttu-id="9e68f-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="9e68f-112">LeaveType</span></span>     | <span data-ttu-id="9e68f-113">Строка</span><span class="sxs-lookup"><span data-stu-id="9e68f-113">String</span></span>    |
  | <span data-ttu-id="9e68f-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="9e68f-114">LeaveDate</span></span>     | <span data-ttu-id="9e68f-115">Дата</span><span class="sxs-lookup"><span data-stu-id="9e68f-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="9e68f-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="9e68f-116">Properties</span></span>

  | <span data-ttu-id="9e68f-117">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="9e68f-117">Property Name</span></span>     | <span data-ttu-id="9e68f-118">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9e68f-118">Data Type</span></span> | <span data-ttu-id="9e68f-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9e68f-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="9e68f-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="9e68f-120">dataAreaId</span></span>        | <span data-ttu-id="9e68f-121">Строка</span><span class="sxs-lookup"><span data-stu-id="9e68f-121">String</span></span>    | <span data-ttu-id="9e68f-122">Х</span><span class="sxs-lookup"><span data-stu-id="9e68f-122">X</span></span>        |
  | <span data-ttu-id="9e68f-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="9e68f-123">RequestId</span></span>         | <span data-ttu-id="9e68f-124">Строка</span><span class="sxs-lookup"><span data-stu-id="9e68f-124">String</span></span>    | <span data-ttu-id="9e68f-125">Х</span><span class="sxs-lookup"><span data-stu-id="9e68f-125">X</span></span>        |
  | <span data-ttu-id="9e68f-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="9e68f-126">LeaveType</span></span>         | <span data-ttu-id="9e68f-127">Строка</span><span class="sxs-lookup"><span data-stu-id="9e68f-127">String</span></span>    | <span data-ttu-id="9e68f-128">Х</span><span class="sxs-lookup"><span data-stu-id="9e68f-128">X</span></span>        |
  | <span data-ttu-id="9e68f-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="9e68f-129">LeaveDate</span></span>         | <span data-ttu-id="9e68f-130">Дата</span><span class="sxs-lookup"><span data-stu-id="9e68f-130">Date</span></span>      | <span data-ttu-id="9e68f-131">Х</span><span class="sxs-lookup"><span data-stu-id="9e68f-131">X</span></span>        |
  | <span data-ttu-id="9e68f-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="9e68f-132">ReasonCodeId</span></span>      | <span data-ttu-id="9e68f-133">Строка</span><span class="sxs-lookup"><span data-stu-id="9e68f-133">String</span></span>    |          |
  | <span data-ttu-id="9e68f-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="9e68f-134">PersonnelNumber</span></span>   | <span data-ttu-id="9e68f-135">Строка</span><span class="sxs-lookup"><span data-stu-id="9e68f-135">String</span></span>    | <span data-ttu-id="9e68f-136">Х</span><span class="sxs-lookup"><span data-stu-id="9e68f-136">X</span></span>        |
  | <span data-ttu-id="9e68f-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="9e68f-137">RequestDate</span></span>       | <span data-ttu-id="9e68f-138">Дата</span><span class="sxs-lookup"><span data-stu-id="9e68f-138">Date</span></span>      | <span data-ttu-id="9e68f-139">Х</span><span class="sxs-lookup"><span data-stu-id="9e68f-139">X</span></span>        |
  | <span data-ttu-id="9e68f-140">Комментарий</span><span class="sxs-lookup"><span data-stu-id="9e68f-140">Comment</span></span>           | <span data-ttu-id="9e68f-141">Строка</span><span class="sxs-lookup"><span data-stu-id="9e68f-141">String</span></span>    |          |
  | <span data-ttu-id="9e68f-142">Состояние</span><span class="sxs-lookup"><span data-stu-id="9e68f-142">Status</span></span>            | <span data-ttu-id="9e68f-143">Перечислимый тип</span><span class="sxs-lookup"><span data-stu-id="9e68f-143">Enum</span></span>      | <span data-ttu-id="9e68f-144">Х</span><span class="sxs-lookup"><span data-stu-id="9e68f-144">X</span></span>        |
  | <span data-ttu-id="9e68f-145">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="9e68f-145">Amount</span></span>            | <span data-ttu-id="9e68f-146">Действующий</span><span class="sxs-lookup"><span data-stu-id="9e68f-146">Real</span></span>      |          |
  | <span data-ttu-id="9e68f-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="9e68f-147">HalfDayDefinition</span></span> | <span data-ttu-id="9e68f-148">Перечислимый тип</span><span class="sxs-lookup"><span data-stu-id="9e68f-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="9e68f-149">Действия</span><span class="sxs-lookup"><span data-stu-id="9e68f-149">Actions</span></span>

 | <span data-ttu-id="9e68f-150">Имя действия</span><span class="sxs-lookup"><span data-stu-id="9e68f-150">Action Name</span></span>                               | <span data-ttu-id="9e68f-151">Описание</span><span class="sxs-lookup"><span data-stu-id="9e68f-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="9e68f-152">submit</span><span class="sxs-lookup"><span data-stu-id="9e68f-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="9e68f-153">Отправка запроса, который должен обрабатываться workflow-процессом.</span><span class="sxs-lookup"><span data-stu-id="9e68f-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="9e68f-154">См. также</span><span class="sxs-lookup"><span data-stu-id="9e68f-154">See also</span></span>

- [<span data-ttu-id="9e68f-155">Отправка запроса на отпуск в workflow-процесс</span><span class="sxs-lookup"><span data-stu-id="9e68f-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="9e68f-156">Проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="9e68f-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]