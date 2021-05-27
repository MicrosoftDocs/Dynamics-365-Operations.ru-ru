---
title: План фиксированной компенсации зарплаты
description: В этом разделе представлены сведения и пример запроса для сущности плана фиксированной компенсации заработной платы в Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 85cfce6f626090adab422ea6c60fc0778fd1ac67
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021304"
---
# <a name="payroll-fixed-compensation-plan"></a><span data-ttu-id="9b972-103">План фиксированной компенсации зарплаты</span><span class="sxs-lookup"><span data-stu-id="9b972-103">Payroll fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9b972-104">В этом разделе представлены сведения и пример запроса для сущности плана фиксированной компенсации заработной платы в Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9b972-104">This topic provides details and an example query for the Payroll fixed compensation plan entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="9b972-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="9b972-105">Properties</span></span>

| <span data-ttu-id="9b972-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="9b972-106">Property</span></span><br><span data-ttu-id="9b972-107">**Физическое имя**</span><span class="sxs-lookup"><span data-stu-id="9b972-107">**Physical name**</span></span><br><span data-ttu-id="9b972-108">**_Вид_**</span><span class="sxs-lookup"><span data-stu-id="9b972-108">**_Type_**</span></span> | <span data-ttu-id="9b972-109">Использование</span><span class="sxs-lookup"><span data-stu-id="9b972-109">Use</span></span> | <span data-ttu-id="9b972-110">описание</span><span class="sxs-lookup"><span data-stu-id="9b972-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="9b972-111">**Код сотрудника**</span><span class="sxs-lookup"><span data-stu-id="9b972-111">**Employee ID**</span></span><br><span data-ttu-id="9b972-112">mshr_fk_employee_id_value</span><span class="sxs-lookup"><span data-stu-id="9b972-112">mshr_fk_employee_id_value</span></span><br><span data-ttu-id="9b972-113">*GUID*</span><span class="sxs-lookup"><span data-stu-id="9b972-113">*GUID*</span></span> | <span data-ttu-id="9b972-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="9b972-114">Read-only</span></span><br><span data-ttu-id="9b972-115">Требуется</span><span class="sxs-lookup"><span data-stu-id="9b972-115">Required</span></span><br><span data-ttu-id="9b972-116">Внешний ключ:mshr_Employee_id of mshr_payrollemployeeentity entity</span><span class="sxs-lookup"><span data-stu-id="9b972-116">Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity</span></span>  | <span data-ttu-id="9b972-117">Код сотрудника</span><span class="sxs-lookup"><span data-stu-id="9b972-117">Employee ID</span></span> |
| <span data-ttu-id="9b972-118">**Ставка зарплаты**</span><span class="sxs-lookup"><span data-stu-id="9b972-118">**Pay rate**</span></span><br><span data-ttu-id="9b972-119">mshr_payrate</span><span class="sxs-lookup"><span data-stu-id="9b972-119">mshr_payrate</span></span><br><span data-ttu-id="9b972-120">*Десятичн.*</span><span class="sxs-lookup"><span data-stu-id="9b972-120">*Decimal*</span></span> | <span data-ttu-id="9b972-121">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="9b972-121">Read-only</span></span><br><span data-ttu-id="9b972-122">Требуется</span><span class="sxs-lookup"><span data-stu-id="9b972-122">Required</span></span> | <span data-ttu-id="9b972-123">Ставка оплаты, определенная в плане фиксированной компенсации.</span><span class="sxs-lookup"><span data-stu-id="9b972-123">Pay rate defined in fixed compensation plan.</span></span> |
| <span data-ttu-id="9b972-124">**Код плана**</span><span class="sxs-lookup"><span data-stu-id="9b972-124">**Plan ID**</span></span><br><span data-ttu-id="9b972-125">mshr_planid</span><span class="sxs-lookup"><span data-stu-id="9b972-125">mshr_planid</span></span><br><span data-ttu-id="9b972-126">*Строка*</span><span class="sxs-lookup"><span data-stu-id="9b972-126">*String*</span></span> | <span data-ttu-id="9b972-127">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="9b972-127">Read-only</span></span><br><span data-ttu-id="9b972-128">Требуется</span><span class="sxs-lookup"><span data-stu-id="9b972-128">Required</span></span> |<span data-ttu-id="9b972-129">Определение плана компенсации.</span><span class="sxs-lookup"><span data-stu-id="9b972-129">Specifies the compensation plan.</span></span>  |
| <span data-ttu-id="9b972-130">**Действительно с**</span><span class="sxs-lookup"><span data-stu-id="9b972-130">**Valid from**</span></span><br><span data-ttu-id="9b972-131">mshr_validfrom</span><span class="sxs-lookup"><span data-stu-id="9b972-131">mshr_validfrom</span></span><br><span data-ttu-id="9b972-132">*Смещение даты и времени*</span><span class="sxs-lookup"><span data-stu-id="9b972-132">*Date Time Offset*</span></span> |  <span data-ttu-id="9b972-133">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="9b972-133">Read-only</span></span><br><span data-ttu-id="9b972-134">Требуется</span><span class="sxs-lookup"><span data-stu-id="9b972-134">Required</span></span> |<span data-ttu-id="9b972-135">Дата, с которой действительна фиксированная компенсация сотрудника.</span><span class="sxs-lookup"><span data-stu-id="9b972-135">Date the employee fixed compensation is valid from.</span></span>  |
| <span data-ttu-id="9b972-136">**Сущность плана фиксированной компенсации заработной платы**</span><span class="sxs-lookup"><span data-stu-id="9b972-136">**Payroll Fixed Compensation Plan entity**</span></span><br><span data-ttu-id="9b972-137">mshr_payrollfixedcompensationplanentityid</span><span class="sxs-lookup"><span data-stu-id="9b972-137">mshr_payrollfixedcompensationplanentityid</span></span><br><span data-ttu-id="9b972-138">*GUID*</span><span class="sxs-lookup"><span data-stu-id="9b972-138">*GUID*</span></span> | <span data-ttu-id="9b972-139">Требуется</span><span class="sxs-lookup"><span data-stu-id="9b972-139">Required</span></span><br><span data-ttu-id="9b972-140">Создано системой</span><span class="sxs-lookup"><span data-stu-id="9b972-140">Sytem generated</span></span> | <span data-ttu-id="9b972-141">Создаваемое системой значение GUID для однозначной идентификации плана компенсации.</span><span class="sxs-lookup"><span data-stu-id="9b972-141">A system-generated GUID value to uniquely identify the compensation plan.</span></span> |
| <span data-ttu-id="9b972-142">**Частота платежей**</span><span class="sxs-lookup"><span data-stu-id="9b972-142">**Pay frequency**</span></span><br><span data-ttu-id="9b972-143">mshr_payfrequency</span><span class="sxs-lookup"><span data-stu-id="9b972-143">mshr_payfrequency</span></span><br><span data-ttu-id="9b972-144">*Строка*</span><span class="sxs-lookup"><span data-stu-id="9b972-144">*String*</span></span> | <span data-ttu-id="9b972-145">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="9b972-145">Read-only</span></span><br><span data-ttu-id="9b972-146">Требуется</span><span class="sxs-lookup"><span data-stu-id="9b972-146">Required</span></span> |<span data-ttu-id="9b972-147">Частота выплаты сотруднику.</span><span class="sxs-lookup"><span data-stu-id="9b972-147">The frequency the employee will be paid.</span></span>  |
| <span data-ttu-id="9b972-148">**Действительно до**</span><span class="sxs-lookup"><span data-stu-id="9b972-148">**Valid to**</span></span><br><span data-ttu-id="9b972-149">mshr_validto</span><span class="sxs-lookup"><span data-stu-id="9b972-149">mshr_validto</span></span><br><span data-ttu-id="9b972-150">*Смещение даты и времени*</span><span class="sxs-lookup"><span data-stu-id="9b972-150">*Date Time Offset*</span></span> | <span data-ttu-id="9b972-151">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="9b972-151">Read-only</span></span> <br><span data-ttu-id="9b972-152">Требуется</span><span class="sxs-lookup"><span data-stu-id="9b972-152">Required</span></span> | <span data-ttu-id="9b972-153">Дата, до которой действительна фиксированная компенсация сотрудника.</span><span class="sxs-lookup"><span data-stu-id="9b972-153">Date the employee fixed compensation is valid to.</span></span> |
| <span data-ttu-id="9b972-154">**Код должности**</span><span class="sxs-lookup"><span data-stu-id="9b972-154">**Position ID**</span></span><br><span data-ttu-id="9b972-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="9b972-155">mshr_positionid</span></span><br><span data-ttu-id="9b972-156">*Строка*</span><span class="sxs-lookup"><span data-stu-id="9b972-156">*String*</span></span> | <span data-ttu-id="9b972-157">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="9b972-157">Read-only</span></span> <br><span data-ttu-id="9b972-158">Требуется</span><span class="sxs-lookup"><span data-stu-id="9b972-158">Required</span></span> | <span data-ttu-id="9b972-159">ИД разноски, связанный с сотрудником и соглашением о регистрации плана фиксированной компенсации.</span><span class="sxs-lookup"><span data-stu-id="9b972-159">Postion ID associated with the employee and fixed compensation plan enrollment.</span></span> |
| <span data-ttu-id="9b972-160">**Валютное**</span><span class="sxs-lookup"><span data-stu-id="9b972-160">**Currency**</span></span><br><span data-ttu-id="9b972-161">mshr_currency</span><span class="sxs-lookup"><span data-stu-id="9b972-161">mshr_currency</span></span><br><span data-ttu-id="9b972-162">*Строка*</span><span class="sxs-lookup"><span data-stu-id="9b972-162">*String*</span></span> | <span data-ttu-id="9b972-163">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="9b972-163">Read-only</span></span> <br><span data-ttu-id="9b972-164">Требуется</span><span class="sxs-lookup"><span data-stu-id="9b972-164">Required</span></span> |<span data-ttu-id="9b972-165">Валюта, определенная для плана фиксированной компенсации</span><span class="sxs-lookup"><span data-stu-id="9b972-165">The currency defined for the fixed compensation plan</span></span>   |
| <span data-ttu-id="9b972-166">**Табельный номер**</span><span class="sxs-lookup"><span data-stu-id="9b972-166">**Personnel number**</span></span><br><span data-ttu-id="9b972-167">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="9b972-167">mshr_personnelnumber</span></span><br><span data-ttu-id="9b972-168">*Строка*</span><span class="sxs-lookup"><span data-stu-id="9b972-168">*String*</span></span> | <span data-ttu-id="9b972-169">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="9b972-169">Read-only</span></span><br><span data-ttu-id="9b972-170">Требуется</span><span class="sxs-lookup"><span data-stu-id="9b972-170">Required</span></span> |<span data-ttu-id="9b972-171">Уникальный табельный номер для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="9b972-171">The employee's unique personnel number.</span></span>  |

<span data-ttu-id="9b972-172">**Запрос**</span><span class="sxs-lookup"><span data-stu-id="9b972-172">**Query**</span></span>

<span data-ttu-id="9b972-173">**Запрос**</span><span class="sxs-lookup"><span data-stu-id="9b972-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="9b972-174">**Отклик**</span><span class="sxs-lookup"><span data-stu-id="9b972-174">**Response**</span></span>

```json
{
            "mshr_planid": "GradeC",
            "mshr_personnelnumber": "000041",
            "mshr_payrate": 75200,
            "mshr_positionid": "000276",
            "mshr_validfrom": "2011-04-05T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_payfrequency": "Annual",
            "mshr_currency": "USD",
            "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
            "_mshr_fk_payroll_id_value": null
}
```
