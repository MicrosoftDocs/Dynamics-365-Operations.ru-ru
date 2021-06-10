---
title: Обзор MyLeaveRequests
description: Объект MyLeaveRequests в Microsoft Dynamics 365 Human Resources предоставляет список запросов отпусков в системе с областью действия (ограниченной) для запросов, доступных текущему пользователю, запрашивающему объект.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f29d5cf1469b58b4ea1837dc82b9513f5c002609
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054964"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="3f100-103">Обзор MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="3f100-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3f100-104">Объект MyLeaveRequests в Microsoft Dynamics 365 Human Resources предоставляет список запросов отпусков в системе с областью действия (ограниченной) для запросов, доступных текущему пользователю, запрашивающему объект.</span><span class="sxs-lookup"><span data-stu-id="3f100-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="3f100-105">Ключ</span><span class="sxs-lookup"><span data-stu-id="3f100-105">Key</span></span>

  | <span data-ttu-id="3f100-106">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="3f100-106">Property Name</span></span> | <span data-ttu-id="3f100-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="3f100-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="3f100-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="3f100-108">dataAreaId</span></span>    | <span data-ttu-id="3f100-109">Строка</span><span class="sxs-lookup"><span data-stu-id="3f100-109">String</span></span>    |
  | <span data-ttu-id="3f100-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="3f100-110">RequestId</span></span>     | <span data-ttu-id="3f100-111">Строка</span><span class="sxs-lookup"><span data-stu-id="3f100-111">String</span></span>    |
  | <span data-ttu-id="3f100-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="3f100-112">LeaveType</span></span>     | <span data-ttu-id="3f100-113">Строка</span><span class="sxs-lookup"><span data-stu-id="3f100-113">String</span></span>    |
  | <span data-ttu-id="3f100-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="3f100-114">LeaveDate</span></span>     | <span data-ttu-id="3f100-115">Дата</span><span class="sxs-lookup"><span data-stu-id="3f100-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="3f100-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="3f100-116">Properties</span></span>

  | <span data-ttu-id="3f100-117">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="3f100-117">Property Name</span></span>     | <span data-ttu-id="3f100-118">Тип данных</span><span class="sxs-lookup"><span data-stu-id="3f100-118">Data Type</span></span> | <span data-ttu-id="3f100-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3f100-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="3f100-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="3f100-120">dataAreaId</span></span>        | <span data-ttu-id="3f100-121">Строка</span><span class="sxs-lookup"><span data-stu-id="3f100-121">String</span></span>    | <span data-ttu-id="3f100-122">Х</span><span class="sxs-lookup"><span data-stu-id="3f100-122">X</span></span>        |
  | <span data-ttu-id="3f100-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="3f100-123">RequestId</span></span>         | <span data-ttu-id="3f100-124">Строка</span><span class="sxs-lookup"><span data-stu-id="3f100-124">String</span></span>    | <span data-ttu-id="3f100-125">Х</span><span class="sxs-lookup"><span data-stu-id="3f100-125">X</span></span>        |
  | <span data-ttu-id="3f100-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="3f100-126">LeaveType</span></span>         | <span data-ttu-id="3f100-127">Строка</span><span class="sxs-lookup"><span data-stu-id="3f100-127">String</span></span>    | <span data-ttu-id="3f100-128">Х</span><span class="sxs-lookup"><span data-stu-id="3f100-128">X</span></span>        |
  | <span data-ttu-id="3f100-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="3f100-129">LeaveDate</span></span>         | <span data-ttu-id="3f100-130">Дата</span><span class="sxs-lookup"><span data-stu-id="3f100-130">Date</span></span>      | <span data-ttu-id="3f100-131">Х</span><span class="sxs-lookup"><span data-stu-id="3f100-131">X</span></span>        |
  | <span data-ttu-id="3f100-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="3f100-132">ReasonCodeId</span></span>      | <span data-ttu-id="3f100-133">Строка</span><span class="sxs-lookup"><span data-stu-id="3f100-133">String</span></span>    |          |
  | <span data-ttu-id="3f100-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="3f100-134">PersonnelNumber</span></span>   | <span data-ttu-id="3f100-135">Строка</span><span class="sxs-lookup"><span data-stu-id="3f100-135">String</span></span>    | <span data-ttu-id="3f100-136">Х</span><span class="sxs-lookup"><span data-stu-id="3f100-136">X</span></span>        |
  | <span data-ttu-id="3f100-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="3f100-137">RequestDate</span></span>       | <span data-ttu-id="3f100-138">Дата</span><span class="sxs-lookup"><span data-stu-id="3f100-138">Date</span></span>      | <span data-ttu-id="3f100-139">Х</span><span class="sxs-lookup"><span data-stu-id="3f100-139">X</span></span>        |
  | <span data-ttu-id="3f100-140">Комментарий</span><span class="sxs-lookup"><span data-stu-id="3f100-140">Comment</span></span>           | <span data-ttu-id="3f100-141">Строка</span><span class="sxs-lookup"><span data-stu-id="3f100-141">String</span></span>    |          |
  | <span data-ttu-id="3f100-142">Состояние</span><span class="sxs-lookup"><span data-stu-id="3f100-142">Status</span></span>            | <span data-ttu-id="3f100-143">Перечислимый тип</span><span class="sxs-lookup"><span data-stu-id="3f100-143">Enum</span></span>      | <span data-ttu-id="3f100-144">Х</span><span class="sxs-lookup"><span data-stu-id="3f100-144">X</span></span>        |
  | <span data-ttu-id="3f100-145">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="3f100-145">Amount</span></span>            | <span data-ttu-id="3f100-146">Действующий</span><span class="sxs-lookup"><span data-stu-id="3f100-146">Real</span></span>      |          |
  | <span data-ttu-id="3f100-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="3f100-147">HalfDayDefinition</span></span> | <span data-ttu-id="3f100-148">Перечислимый тип</span><span class="sxs-lookup"><span data-stu-id="3f100-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="3f100-149">Действия</span><span class="sxs-lookup"><span data-stu-id="3f100-149">Actions</span></span>

 | <span data-ttu-id="3f100-150">Имя действия</span><span class="sxs-lookup"><span data-stu-id="3f100-150">Action Name</span></span>                               | <span data-ttu-id="3f100-151">Описание</span><span class="sxs-lookup"><span data-stu-id="3f100-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="3f100-152">submit</span><span class="sxs-lookup"><span data-stu-id="3f100-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="3f100-153">Отправка запроса, который должен обрабатываться workflow-процессом.</span><span class="sxs-lookup"><span data-stu-id="3f100-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="3f100-154">См. также</span><span class="sxs-lookup"><span data-stu-id="3f100-154">See also</span></span>

- [<span data-ttu-id="3f100-155">Отправка запроса на отпуск в workflow-процесс</span><span class="sxs-lookup"><span data-stu-id="3f100-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="3f100-156">Проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="3f100-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]