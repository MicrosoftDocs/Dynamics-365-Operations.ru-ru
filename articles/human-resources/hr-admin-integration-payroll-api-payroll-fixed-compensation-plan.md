---
title: План фиксированной компенсации зарплаты
description: В этом разделе представлены сведения и пример запроса для сущности плана фиксированной компенсации заработной платы в Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 227082358c59abddd63f4faa4536a8df270a4d80
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059096"
---
# <a name="payroll-fixed-compensation-plan"></a><span data-ttu-id="80929-103">План фиксированной компенсации зарплаты</span><span class="sxs-lookup"><span data-stu-id="80929-103">Payroll fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="80929-104">В этом разделе представлены сведения и пример запроса для сущности плана фиксированной компенсации заработной платы в Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="80929-104">This topic provides details and an example query for the Payroll fixed compensation plan entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="80929-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="80929-105">Properties</span></span>

| <span data-ttu-id="80929-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="80929-106">Property</span></span><br><span data-ttu-id="80929-107">**Физическое имя**</span><span class="sxs-lookup"><span data-stu-id="80929-107">**Physical name**</span></span><br><span data-ttu-id="80929-108">**_Вид_**</span><span class="sxs-lookup"><span data-stu-id="80929-108">**_Type_**</span></span> | <span data-ttu-id="80929-109">Использование</span><span class="sxs-lookup"><span data-stu-id="80929-109">Use</span></span> | <span data-ttu-id="80929-110">описание</span><span class="sxs-lookup"><span data-stu-id="80929-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="80929-111">**Код сотрудника**</span><span class="sxs-lookup"><span data-stu-id="80929-111">**Employee ID**</span></span><br><span data-ttu-id="80929-112">mshr_fk_employee_id_value</span><span class="sxs-lookup"><span data-stu-id="80929-112">mshr_fk_employee_id_value</span></span><br><span data-ttu-id="80929-113">*GUID*</span><span class="sxs-lookup"><span data-stu-id="80929-113">*GUID*</span></span> | <span data-ttu-id="80929-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="80929-114">Read-only</span></span><br><span data-ttu-id="80929-115">Требуется</span><span class="sxs-lookup"><span data-stu-id="80929-115">Required</span></span><br><span data-ttu-id="80929-116">Внешний ключ:mshr_Employee_id of mshr_payrollemployeeentity entity</span><span class="sxs-lookup"><span data-stu-id="80929-116">Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity</span></span>  | <span data-ttu-id="80929-117">Код сотрудника</span><span class="sxs-lookup"><span data-stu-id="80929-117">Employee ID</span></span> |
| <span data-ttu-id="80929-118">**Ставка зарплаты**</span><span class="sxs-lookup"><span data-stu-id="80929-118">**Pay rate**</span></span><br><span data-ttu-id="80929-119">mshr_payrate</span><span class="sxs-lookup"><span data-stu-id="80929-119">mshr_payrate</span></span><br><span data-ttu-id="80929-120">*Десятичн.*</span><span class="sxs-lookup"><span data-stu-id="80929-120">*Decimal*</span></span> | <span data-ttu-id="80929-121">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="80929-121">Read-only</span></span><br><span data-ttu-id="80929-122">Требуется</span><span class="sxs-lookup"><span data-stu-id="80929-122">Required</span></span> | <span data-ttu-id="80929-123">Ставка оплаты, определенная в плане фиксированной компенсации.</span><span class="sxs-lookup"><span data-stu-id="80929-123">Pay rate defined in fixed compensation plan.</span></span> |
| <span data-ttu-id="80929-124">**Код плана**</span><span class="sxs-lookup"><span data-stu-id="80929-124">**Plan ID**</span></span><br><span data-ttu-id="80929-125">mshr_planid</span><span class="sxs-lookup"><span data-stu-id="80929-125">mshr_planid</span></span><br><span data-ttu-id="80929-126">*Строка*</span><span class="sxs-lookup"><span data-stu-id="80929-126">*String*</span></span> | <span data-ttu-id="80929-127">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="80929-127">Read-only</span></span><br><span data-ttu-id="80929-128">Требуется</span><span class="sxs-lookup"><span data-stu-id="80929-128">Required</span></span> |<span data-ttu-id="80929-129">Определение плана компенсации.</span><span class="sxs-lookup"><span data-stu-id="80929-129">Specifies the compensation plan.</span></span>  |
| <span data-ttu-id="80929-130">**Действительно с**</span><span class="sxs-lookup"><span data-stu-id="80929-130">**Valid from**</span></span><br><span data-ttu-id="80929-131">mshr_validfrom</span><span class="sxs-lookup"><span data-stu-id="80929-131">mshr_validfrom</span></span><br><span data-ttu-id="80929-132">*Смещение даты и времени*</span><span class="sxs-lookup"><span data-stu-id="80929-132">*Date Time Offset*</span></span> |  <span data-ttu-id="80929-133">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="80929-133">Read-only</span></span><br><span data-ttu-id="80929-134">Требуется</span><span class="sxs-lookup"><span data-stu-id="80929-134">Required</span></span> |<span data-ttu-id="80929-135">Дата, с которой действительна фиксированная компенсация сотрудника.</span><span class="sxs-lookup"><span data-stu-id="80929-135">Date the employee fixed compensation is valid from.</span></span>  |
| <span data-ttu-id="80929-136">**Сущность плана фиксированной компенсации заработной платы**</span><span class="sxs-lookup"><span data-stu-id="80929-136">**Payroll Fixed Compensation Plan entity**</span></span><br><span data-ttu-id="80929-137">mshr_payrollfixedcompensationplanentityid</span><span class="sxs-lookup"><span data-stu-id="80929-137">mshr_payrollfixedcompensationplanentityid</span></span><br><span data-ttu-id="80929-138">*GUID*</span><span class="sxs-lookup"><span data-stu-id="80929-138">*GUID*</span></span> | <span data-ttu-id="80929-139">Требуется</span><span class="sxs-lookup"><span data-stu-id="80929-139">Required</span></span><br><span data-ttu-id="80929-140">Создано системой</span><span class="sxs-lookup"><span data-stu-id="80929-140">Sytem generated</span></span> | <span data-ttu-id="80929-141">Создаваемое системой значение GUID для однозначной идентификации плана компенсации.</span><span class="sxs-lookup"><span data-stu-id="80929-141">A system-generated GUID value to uniquely identify the compensation plan.</span></span> |
| <span data-ttu-id="80929-142">**Частота платежей**</span><span class="sxs-lookup"><span data-stu-id="80929-142">**Pay frequency**</span></span><br><span data-ttu-id="80929-143">mshr_payfrequency</span><span class="sxs-lookup"><span data-stu-id="80929-143">mshr_payfrequency</span></span><br><span data-ttu-id="80929-144">*Строка*</span><span class="sxs-lookup"><span data-stu-id="80929-144">*String*</span></span> | <span data-ttu-id="80929-145">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="80929-145">Read-only</span></span><br><span data-ttu-id="80929-146">Требуется</span><span class="sxs-lookup"><span data-stu-id="80929-146">Required</span></span> |<span data-ttu-id="80929-147">Частота выплаты сотруднику.</span><span class="sxs-lookup"><span data-stu-id="80929-147">The frequency the employee will be paid.</span></span>  |
| <span data-ttu-id="80929-148">**Действительно до**</span><span class="sxs-lookup"><span data-stu-id="80929-148">**Valid to**</span></span><br><span data-ttu-id="80929-149">mshr_validto</span><span class="sxs-lookup"><span data-stu-id="80929-149">mshr_validto</span></span><br><span data-ttu-id="80929-150">*Смещение даты и времени*</span><span class="sxs-lookup"><span data-stu-id="80929-150">*Date Time Offset*</span></span> | <span data-ttu-id="80929-151">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="80929-151">Read-only</span></span> <br><span data-ttu-id="80929-152">Требуется</span><span class="sxs-lookup"><span data-stu-id="80929-152">Required</span></span> | <span data-ttu-id="80929-153">Дата, до которой действительна фиксированная компенсация сотрудника.</span><span class="sxs-lookup"><span data-stu-id="80929-153">Date the employee fixed compensation is valid to.</span></span> |
| <span data-ttu-id="80929-154">**Код должности**</span><span class="sxs-lookup"><span data-stu-id="80929-154">**Position ID**</span></span><br><span data-ttu-id="80929-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="80929-155">mshr_positionid</span></span><br><span data-ttu-id="80929-156">*Строка*</span><span class="sxs-lookup"><span data-stu-id="80929-156">*String*</span></span> | <span data-ttu-id="80929-157">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="80929-157">Read-only</span></span> <br><span data-ttu-id="80929-158">Требуется</span><span class="sxs-lookup"><span data-stu-id="80929-158">Required</span></span> | <span data-ttu-id="80929-159">ИД разноски, связанный с сотрудником и соглашением о регистрации плана фиксированной компенсации.</span><span class="sxs-lookup"><span data-stu-id="80929-159">Postion ID associated with the employee and fixed compensation plan enrollment.</span></span> |
| <span data-ttu-id="80929-160">**Валютное**</span><span class="sxs-lookup"><span data-stu-id="80929-160">**Currency**</span></span><br><span data-ttu-id="80929-161">mshr_currency</span><span class="sxs-lookup"><span data-stu-id="80929-161">mshr_currency</span></span><br><span data-ttu-id="80929-162">*Строка*</span><span class="sxs-lookup"><span data-stu-id="80929-162">*String*</span></span> | <span data-ttu-id="80929-163">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="80929-163">Read-only</span></span> <br><span data-ttu-id="80929-164">Требуется</span><span class="sxs-lookup"><span data-stu-id="80929-164">Required</span></span> |<span data-ttu-id="80929-165">Валюта, определенная для плана фиксированной компенсации</span><span class="sxs-lookup"><span data-stu-id="80929-165">The currency defined for the fixed compensation plan</span></span>   |
| <span data-ttu-id="80929-166">**Табельный номер**</span><span class="sxs-lookup"><span data-stu-id="80929-166">**Personnel number**</span></span><br><span data-ttu-id="80929-167">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="80929-167">mshr_personnelnumber</span></span><br><span data-ttu-id="80929-168">*Строка*</span><span class="sxs-lookup"><span data-stu-id="80929-168">*String*</span></span> | <span data-ttu-id="80929-169">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="80929-169">Read-only</span></span><br><span data-ttu-id="80929-170">Требуется</span><span class="sxs-lookup"><span data-stu-id="80929-170">Required</span></span> |<span data-ttu-id="80929-171">Уникальный табельный номер для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="80929-171">The employee's unique personnel number.</span></span>  |

<span data-ttu-id="80929-172">**Запрос**</span><span class="sxs-lookup"><span data-stu-id="80929-172">**Query**</span></span>

<span data-ttu-id="80929-173">**Запрос**</span><span class="sxs-lookup"><span data-stu-id="80929-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="80929-174">**Отклик**</span><span class="sxs-lookup"><span data-stu-id="80929-174">**Response**</span></span>

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
