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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 44e23a076733bac782a0366aeba3456911522abe
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803641"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="9a7da-103">Обзор MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="9a7da-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9a7da-104">Объект MyLeaveRequests в Microsoft Dynamics 365 Human Resources предоставляет список запросов отпусков в системе с областью действия (ограниченной) для запросов, доступных текущему пользователю, запрашивающему объект.</span><span class="sxs-lookup"><span data-stu-id="9a7da-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="9a7da-105">Ключ</span><span class="sxs-lookup"><span data-stu-id="9a7da-105">Key</span></span>

  | <span data-ttu-id="9a7da-106">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="9a7da-106">Property Name</span></span> | <span data-ttu-id="9a7da-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9a7da-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="9a7da-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="9a7da-108">dataAreaId</span></span>    | <span data-ttu-id="9a7da-109">Строка</span><span class="sxs-lookup"><span data-stu-id="9a7da-109">String</span></span>    |
  | <span data-ttu-id="9a7da-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="9a7da-110">RequestId</span></span>     | <span data-ttu-id="9a7da-111">Строка</span><span class="sxs-lookup"><span data-stu-id="9a7da-111">String</span></span>    |
  | <span data-ttu-id="9a7da-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="9a7da-112">LeaveType</span></span>     | <span data-ttu-id="9a7da-113">Строка</span><span class="sxs-lookup"><span data-stu-id="9a7da-113">String</span></span>    |
  | <span data-ttu-id="9a7da-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="9a7da-114">LeaveDate</span></span>     | <span data-ttu-id="9a7da-115">Дата</span><span class="sxs-lookup"><span data-stu-id="9a7da-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="9a7da-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="9a7da-116">Properties</span></span>

  | <span data-ttu-id="9a7da-117">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="9a7da-117">Property Name</span></span>     | <span data-ttu-id="9a7da-118">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9a7da-118">Data Type</span></span> | <span data-ttu-id="9a7da-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9a7da-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="9a7da-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="9a7da-120">dataAreaId</span></span>        | <span data-ttu-id="9a7da-121">Строка</span><span class="sxs-lookup"><span data-stu-id="9a7da-121">String</span></span>    | <span data-ttu-id="9a7da-122">Х</span><span class="sxs-lookup"><span data-stu-id="9a7da-122">X</span></span>        |
  | <span data-ttu-id="9a7da-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="9a7da-123">RequestId</span></span>         | <span data-ttu-id="9a7da-124">Строка</span><span class="sxs-lookup"><span data-stu-id="9a7da-124">String</span></span>    | <span data-ttu-id="9a7da-125">Х</span><span class="sxs-lookup"><span data-stu-id="9a7da-125">X</span></span>        |
  | <span data-ttu-id="9a7da-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="9a7da-126">LeaveType</span></span>         | <span data-ttu-id="9a7da-127">Строка</span><span class="sxs-lookup"><span data-stu-id="9a7da-127">String</span></span>    | <span data-ttu-id="9a7da-128">Х</span><span class="sxs-lookup"><span data-stu-id="9a7da-128">X</span></span>        |
  | <span data-ttu-id="9a7da-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="9a7da-129">LeaveDate</span></span>         | <span data-ttu-id="9a7da-130">Дата</span><span class="sxs-lookup"><span data-stu-id="9a7da-130">Date</span></span>      | <span data-ttu-id="9a7da-131">Х</span><span class="sxs-lookup"><span data-stu-id="9a7da-131">X</span></span>        |
  | <span data-ttu-id="9a7da-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="9a7da-132">ReasonCodeId</span></span>      | <span data-ttu-id="9a7da-133">Строка</span><span class="sxs-lookup"><span data-stu-id="9a7da-133">String</span></span>    |          |
  | <span data-ttu-id="9a7da-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="9a7da-134">PersonnelNumber</span></span>   | <span data-ttu-id="9a7da-135">Строка</span><span class="sxs-lookup"><span data-stu-id="9a7da-135">String</span></span>    | <span data-ttu-id="9a7da-136">Х</span><span class="sxs-lookup"><span data-stu-id="9a7da-136">X</span></span>        |
  | <span data-ttu-id="9a7da-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="9a7da-137">RequestDate</span></span>       | <span data-ttu-id="9a7da-138">Дата</span><span class="sxs-lookup"><span data-stu-id="9a7da-138">Date</span></span>      | <span data-ttu-id="9a7da-139">Х</span><span class="sxs-lookup"><span data-stu-id="9a7da-139">X</span></span>        |
  | <span data-ttu-id="9a7da-140">Комментарий</span><span class="sxs-lookup"><span data-stu-id="9a7da-140">Comment</span></span>           | <span data-ttu-id="9a7da-141">Строка</span><span class="sxs-lookup"><span data-stu-id="9a7da-141">String</span></span>    |          |
  | <span data-ttu-id="9a7da-142">Состояние</span><span class="sxs-lookup"><span data-stu-id="9a7da-142">Status</span></span>            | <span data-ttu-id="9a7da-143">Перечислимый тип</span><span class="sxs-lookup"><span data-stu-id="9a7da-143">Enum</span></span>      | <span data-ttu-id="9a7da-144">Х</span><span class="sxs-lookup"><span data-stu-id="9a7da-144">X</span></span>        |
  | <span data-ttu-id="9a7da-145">Сумма, руб.</span><span class="sxs-lookup"><span data-stu-id="9a7da-145">Amount</span></span>            | <span data-ttu-id="9a7da-146">Действующий</span><span class="sxs-lookup"><span data-stu-id="9a7da-146">Real</span></span>      |          |
  | <span data-ttu-id="9a7da-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="9a7da-147">HalfDayDefinition</span></span> | <span data-ttu-id="9a7da-148">Перечислимый тип</span><span class="sxs-lookup"><span data-stu-id="9a7da-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="9a7da-149">Действия</span><span class="sxs-lookup"><span data-stu-id="9a7da-149">Actions</span></span>

 | <span data-ttu-id="9a7da-150">Имя действия</span><span class="sxs-lookup"><span data-stu-id="9a7da-150">Action Name</span></span>                               | <span data-ttu-id="9a7da-151">Описание</span><span class="sxs-lookup"><span data-stu-id="9a7da-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="9a7da-152">submit</span><span class="sxs-lookup"><span data-stu-id="9a7da-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="9a7da-153">Отправка запроса, который должен обрабатываться workflow-процессом.</span><span class="sxs-lookup"><span data-stu-id="9a7da-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="9a7da-154">См. также</span><span class="sxs-lookup"><span data-stu-id="9a7da-154">See also</span></span>

- [<span data-ttu-id="9a7da-155">Отправка запроса на отпуск в workflow-процесс</span><span class="sxs-lookup"><span data-stu-id="9a7da-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="9a7da-156">Проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="9a7da-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]