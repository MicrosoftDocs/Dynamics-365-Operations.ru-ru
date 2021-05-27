---
title: Сведения о заработной плате для должностей
description: В этом разделе представлены сведения и пример запроса для сущности Сведения о заработной плате для должностей в Dynamics 365 Human Resources.
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
ms.openlocfilehash: 7b23ac5d11b18c77109be21afe1570755dccba20
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019330"
---
# <a name="payroll-position"></a><span data-ttu-id="cfdd0-103">Позиция зарплаты</span><span class="sxs-lookup"><span data-stu-id="cfdd0-103">Payroll position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="cfdd0-104">В этом разделе представлены сведения и пример запроса для сущности Сведения о заработной плате для должностей в Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="cfdd0-104">This topic provides details and an example query for the Payroll details for the Positions entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="cfdd0-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="cfdd0-105">Properties</span></span>

| <span data-ttu-id="cfdd0-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="cfdd0-106">Property</span></span><br><span data-ttu-id="cfdd0-107">**Физическое имя**</span><span class="sxs-lookup"><span data-stu-id="cfdd0-107">**Physical name**</span></span><br><span data-ttu-id="cfdd0-108">**_Вид_**</span><span class="sxs-lookup"><span data-stu-id="cfdd0-108">**_Type_**</span></span> | <span data-ttu-id="cfdd0-109">Использование</span><span class="sxs-lookup"><span data-stu-id="cfdd0-109">Use</span></span> | <span data-ttu-id="cfdd0-110">описание</span><span class="sxs-lookup"><span data-stu-id="cfdd0-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="cfdd0-111">**Обычные часы за год**</span><span class="sxs-lookup"><span data-stu-id="cfdd0-111">**Annual regular hours**</span></span><br><span data-ttu-id="cfdd0-112">annualregularhours</span><span class="sxs-lookup"><span data-stu-id="cfdd0-112">annualregularhours</span></span><br><span data-ttu-id="cfdd0-113">*Десятичн.*</span><span class="sxs-lookup"><span data-stu-id="cfdd0-113">*Decimal*</span></span> | <span data-ttu-id="cfdd0-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cfdd0-114">Read-only</span></span><br><span data-ttu-id="cfdd0-115">Требуется</span><span class="sxs-lookup"><span data-stu-id="cfdd0-115">Required</span></span> | <span data-ttu-id="cfdd0-116">Обычные часы за год, определенные для данной должности.</span><span class="sxs-lookup"><span data-stu-id="cfdd0-116">Annual regular hours defined on the position.</span></span>  |
| <span data-ttu-id="cfdd0-117">**ИД сущности Сведения о заработной плате для должностей**</span><span class="sxs-lookup"><span data-stu-id="cfdd0-117">**Payroll position details entity ID**</span></span><br><span data-ttu-id="cfdd0-118">payrollpositiondetailsentityid</span><span class="sxs-lookup"><span data-stu-id="cfdd0-118">payrollpositiondetailsentityid</span></span><br><span data-ttu-id="cfdd0-119">*Guid*</span><span class="sxs-lookup"><span data-stu-id="cfdd0-119">*Guid*</span></span> | <span data-ttu-id="cfdd0-120">Требуется</span><span class="sxs-lookup"><span data-stu-id="cfdd0-120">Required</span></span><br><span data-ttu-id="cfdd0-121">Создано системой.</span><span class="sxs-lookup"><span data-stu-id="cfdd0-121">System generated.</span></span> | <span data-ttu-id="cfdd0-122">Создаваемое системой значение GUID для уникальной идентификации должности.</span><span class="sxs-lookup"><span data-stu-id="cfdd0-122">A system-generated GUID value to uniquely identify the position.</span></span>  |
| <span data-ttu-id="cfdd0-123">**Основное поле**</span><span class="sxs-lookup"><span data-stu-id="cfdd0-123">**Primary field**</span></span><br><span data-ttu-id="cfdd0-124">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="cfdd0-124">mshr_primaryfield</span></span><br><span data-ttu-id="cfdd0-125">*Строка*</span><span class="sxs-lookup"><span data-stu-id="cfdd0-125">*String*</span></span> | <span data-ttu-id="cfdd0-126">Требуется</span><span class="sxs-lookup"><span data-stu-id="cfdd0-126">Required</span></span><br><span data-ttu-id="cfdd0-127">Создано системой</span><span class="sxs-lookup"><span data-stu-id="cfdd0-127">System generated</span></span> |  |
| <span data-ttu-id="cfdd0-128">**Значение идентификатора задания должности**</span><span class="sxs-lookup"><span data-stu-id="cfdd0-128">**Position job ID value**</span></span><br><span data-ttu-id="cfdd0-129">_mshr_fk_positionjob_id_value</span><span class="sxs-lookup"><span data-stu-id="cfdd0-129">_mshr_fk_positionjob_id_value</span></span><br><span data-ttu-id="cfdd0-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="cfdd0-130">*GUID*</span></span> | <span data-ttu-id="cfdd0-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cfdd0-131">Read-only</span></span><br><span data-ttu-id="cfdd0-132">Требуется</span><span class="sxs-lookup"><span data-stu-id="cfdd0-132">Required</span></span><br><span data-ttu-id="cfdd0-133">Внешний ключ:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span><span class="sxs-lookup"><span data-stu-id="cfdd0-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span></span> |<span data-ttu-id="cfdd0-134">ИД задания, связанный с должностью.</span><span class="sxs-lookup"><span data-stu-id="cfdd0-134">The ID of the job associated with the position.</span></span>|
| <span data-ttu-id="cfdd0-135">**Значение идентификатора План фиксированной компенсации**</span><span class="sxs-lookup"><span data-stu-id="cfdd0-135">**Fixed compensation plan ID value**</span></span><br><span data-ttu-id="cfdd0-136">_mshr_fk_fixedcompplan_id_value</span><span class="sxs-lookup"><span data-stu-id="cfdd0-136">_mshr_fk_fixedcompplan_id_value</span></span><br><span data-ttu-id="cfdd0-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="cfdd0-137">*GUID*</span></span> | <span data-ttu-id="cfdd0-138">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cfdd0-138">Read-only</span></span><br><span data-ttu-id="cfdd0-139">Требуется</span><span class="sxs-lookup"><span data-stu-id="cfdd0-139">Required</span></span><br><span data-ttu-id="cfdd0-140">Внешний ключ: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span><span class="sxs-lookup"><span data-stu-id="cfdd0-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span></span>  | <span data-ttu-id="cfdd0-141">ИД плана фиксированной компенсации, связанный с должностью.</span><span class="sxs-lookup"><span data-stu-id="cfdd0-141">The ID of the fixed compensation plan associated with the position.</span></span> |
| <span data-ttu-id="cfdd0-142">**ИД цикли оплаты**</span><span class="sxs-lookup"><span data-stu-id="cfdd0-142">**Pay cycle ID**</span></span><br><span data-ttu-id="cfdd0-143">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="cfdd0-143">mshr_primaryfield</span></span><br><span data-ttu-id="cfdd0-144">*Строка*</span><span class="sxs-lookup"><span data-stu-id="cfdd0-144">*String*</span></span> | <span data-ttu-id="cfdd0-145">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cfdd0-145">Read-only</span></span><br><span data-ttu-id="cfdd0-146">Требуется</span><span class="sxs-lookup"><span data-stu-id="cfdd0-146">Required</span></span> | <span data-ttu-id="cfdd0-147">Цикл оплаты, определенный для данной должности.</span><span class="sxs-lookup"><span data-stu-id="cfdd0-147">The pay cycle defined on the position.</span></span> |
| <span data-ttu-id="cfdd0-148">**Оплачивается юридическим лицом**</span><span class="sxs-lookup"><span data-stu-id="cfdd0-148">**Paid by legal entity**</span></span><br><span data-ttu-id="cfdd0-149">paidbylegalentity</span><span class="sxs-lookup"><span data-stu-id="cfdd0-149">paidbylegalentity</span></span><br><span data-ttu-id="cfdd0-150">*Строка*</span><span class="sxs-lookup"><span data-stu-id="cfdd0-150">*String*</span></span> | <span data-ttu-id="cfdd0-151">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cfdd0-151">Read-only</span></span><br><span data-ttu-id="cfdd0-152">Требуется</span><span class="sxs-lookup"><span data-stu-id="cfdd0-152">Required</span></span> | <span data-ttu-id="cfdd0-153">Юридическое лицо, определенное в должности, ответственной за осуществление платежа.</span><span class="sxs-lookup"><span data-stu-id="cfdd0-153">The legal entity defined on the positoin responsible for issuing payment.</span></span> |
| <span data-ttu-id="cfdd0-154">**Код должности**</span><span class="sxs-lookup"><span data-stu-id="cfdd0-154">**Position ID**</span></span><br><span data-ttu-id="cfdd0-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="cfdd0-155">mshr_positionid</span></span><br><span data-ttu-id="cfdd0-156">*Строка*</span><span class="sxs-lookup"><span data-stu-id="cfdd0-156">*String*</span></span> | <span data-ttu-id="cfdd0-157">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cfdd0-157">Read-only</span></span><br><span data-ttu-id="cfdd0-158">Требуется</span><span class="sxs-lookup"><span data-stu-id="cfdd0-158">Required</span></span> | <span data-ttu-id="cfdd0-159">Код должности.</span><span class="sxs-lookup"><span data-stu-id="cfdd0-159">The ID of the position.</span></span> |
| <span data-ttu-id="cfdd0-160">**Действительно до**</span><span class="sxs-lookup"><span data-stu-id="cfdd0-160">**Valid to**</span></span><br><span data-ttu-id="cfdd0-161">validto</span><span class="sxs-lookup"><span data-stu-id="cfdd0-161">validto</span></span><br><span data-ttu-id="cfdd0-162">*Смещение даты и времени*</span><span class="sxs-lookup"><span data-stu-id="cfdd0-162">*Date Time Offset*</span></span> | <span data-ttu-id="cfdd0-163">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cfdd0-163">Read-only</span></span><br><span data-ttu-id="cfdd0-164">Требуется</span><span class="sxs-lookup"><span data-stu-id="cfdd0-164">Required</span></span> |<span data-ttu-id="cfdd0-165">Дата, начиная с которой будут действительны сведения о должности.</span><span class="sxs-lookup"><span data-stu-id="cfdd0-165">The date the position details are valid from.</span></span>  |
| <span data-ttu-id="cfdd0-166">**Действительно с**</span><span class="sxs-lookup"><span data-stu-id="cfdd0-166">**Valid from**</span></span><br><span data-ttu-id="cfdd0-167">validfrom</span><span class="sxs-lookup"><span data-stu-id="cfdd0-167">validfrom</span></span><br><span data-ttu-id="cfdd0-168">*Смещение даты и времени*</span><span class="sxs-lookup"><span data-stu-id="cfdd0-168">*Date Time Offset*</span></span> | <span data-ttu-id="cfdd0-169">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cfdd0-169">Read-only</span></span><br><span data-ttu-id="cfdd0-170">Требуется</span><span class="sxs-lookup"><span data-stu-id="cfdd0-170">Required</span></span> |<span data-ttu-id="cfdd0-171">Дата, до которой будут действительны сведения о должности.</span><span class="sxs-lookup"><span data-stu-id="cfdd0-171">The date the position details are valid to.</span></span>  |

<span data-ttu-id="cfdd0-172">**Запрос**</span><span class="sxs-lookup"><span data-stu-id="cfdd0-172">**Query**</span></span>

<span data-ttu-id="cfdd0-173">**Запрос**</span><span class="sxs-lookup"><span data-stu-id="cfdd0-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

<span data-ttu-id="cfdd0-174">**Отклик**</span><span class="sxs-lookup"><span data-stu-id="cfdd0-174">**Response**</span></span>

```json
{
            "mshr_positionid": "000276",
            "mshr_paycycleid": "w",
            "mshr_annualregularhours": 3000,
            "mshr_paidbylegalentity": "USMF",
            "mshr_validfrom": "2021-03-14T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_primaryfield": "000276 | 3/14/2021",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```
