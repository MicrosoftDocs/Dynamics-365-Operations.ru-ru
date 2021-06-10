---
title: Отбор для лица
description: В этом разделе описывается сущность отбора физического лица для Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9d29b26094e307c3f68d57f297ab3614f3a5ccae
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059288"
---
# <a name="person-screening"></a><span data-ttu-id="436d5-103">Отбор для лица</span><span class="sxs-lookup"><span data-stu-id="436d5-103">Person screening</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="436d5-104">В этом разделе описывается сущность отбора физического лица для Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="436d5-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="436d5-105">Физическое имя: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="436d5-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="436d5-106">описание</span><span class="sxs-lookup"><span data-stu-id="436d5-106">Description</span></span>

<span data-ttu-id="436d5-107">Эта сущность описывает отборы, которые кандидат прошел или должен пройти для приема на работу.</span><span class="sxs-lookup"><span data-stu-id="436d5-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="436d5-108">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="436d5-108">JSON representation</span></span>

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a><span data-ttu-id="436d5-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="436d5-109">Properties</span></span>

| <span data-ttu-id="436d5-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="436d5-110">Property</span></span><br><span data-ttu-id="436d5-111">**Физическое имя**</span><span class="sxs-lookup"><span data-stu-id="436d5-111">**Physical name**</span></span><br><span data-ttu-id="436d5-112">**_Вид_**</span><span class="sxs-lookup"><span data-stu-id="436d5-112">**_Type_**</span></span> | <span data-ttu-id="436d5-113">Использование</span><span class="sxs-lookup"><span data-stu-id="436d5-113">Use</span></span> | <span data-ttu-id="436d5-114">описание</span><span class="sxs-lookup"><span data-stu-id="436d5-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="436d5-115">**Код сущности отбора для физического лица**</span><span class="sxs-lookup"><span data-stu-id="436d5-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="436d5-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="436d5-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="436d5-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="436d5-117">*GUID*</span></span> | <span data-ttu-id="436d5-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="436d5-118">Read-only</span></span><br><span data-ttu-id="436d5-119">Требуется</span><span class="sxs-lookup"><span data-stu-id="436d5-119">Required</span></span><br><span data-ttu-id="436d5-120">Создано системой</span><span class="sxs-lookup"><span data-stu-id="436d5-120">System-generated</span></span> | <span data-ttu-id="436d5-121">Уникальный первичный идентификатор записи отбора физического лица.</span><span class="sxs-lookup"><span data-stu-id="436d5-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="436d5-122">**Номер субъекта**</span><span class="sxs-lookup"><span data-stu-id="436d5-122">**Party Number**</span></span><br><span data-ttu-id="436d5-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="436d5-123">mshr_partynumber</span></span><br><span data-ttu-id="436d5-124">*Строка*</span><span class="sxs-lookup"><span data-stu-id="436d5-124">*String*</span></span> | <span data-ttu-id="436d5-125">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="436d5-125">Read/write</span></span><br><span data-ttu-id="436d5-126">Требуется</span><span class="sxs-lookup"><span data-stu-id="436d5-126">Required</span></span> | <span data-ttu-id="436d5-127">Номер субъекта (лица), связанный с кандидатом.</span><span class="sxs-lookup"><span data-stu-id="436d5-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="436d5-128">**Значение ИД физического лица**</span><span class="sxs-lookup"><span data-stu-id="436d5-128">**Person ID Value**</span></span><br><span data-ttu-id="436d5-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="436d5-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="436d5-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="436d5-130">*GUID*</span></span> | <span data-ttu-id="436d5-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="436d5-131">Read-only</span></span><br><span data-ttu-id="436d5-132">Требуется</span><span class="sxs-lookup"><span data-stu-id="436d5-132">Required</span></span><br><span data-ttu-id="436d5-133">Внешний ключ: mshr_dirpersonentityid сущности mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="436d5-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="436d5-134">Созданный системой уникальный идентификатор записи сущности субъекта (физического лица).</span><span class="sxs-lookup"><span data-stu-id="436d5-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="436d5-135">**ИД типа отбора**</span><span class="sxs-lookup"><span data-stu-id="436d5-135">**Screening Type ID**</span></span><br><span data-ttu-id="436d5-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="436d5-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="436d5-137">*Строка*</span><span class="sxs-lookup"><span data-stu-id="436d5-137">*String*</span></span> | <span data-ttu-id="436d5-138">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="436d5-138">Read/write</span></span><br><span data-ttu-id="436d5-139">Требуется</span><span class="sxs-lookup"><span data-stu-id="436d5-139">Required</span></span><br><span data-ttu-id="436d5-140">Внешний ключ: ScreeningType</span><span class="sxs-lookup"><span data-stu-id="436d5-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="436d5-141">Идентификатор типа отбора, определенный в модуле Human Resources.</span><span class="sxs-lookup"><span data-stu-id="436d5-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="436d5-142">**Значение ИД типа отбора**</span><span class="sxs-lookup"><span data-stu-id="436d5-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="436d5-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="436d5-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="436d5-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="436d5-144">*GUID*</span></span> | <span data-ttu-id="436d5-145">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="436d5-145">Read-only</span></span><br><span data-ttu-id="436d5-146">Требуется</span><span class="sxs-lookup"><span data-stu-id="436d5-146">Required</span></span><br><span data-ttu-id="436d5-147">Внешний ключ: mshr_hcmscreeningtypeentityid сущности mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="436d5-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="436d5-148">Созданный системой идентификатор для записи типа отбора в связанной сущности.</span><span class="sxs-lookup"><span data-stu-id="436d5-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="436d5-149">**Требуется к**</span><span class="sxs-lookup"><span data-stu-id="436d5-149">**Required By**</span></span><br><span data-ttu-id="436d5-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="436d5-150">mshr_requiredby</span></span><br><span data-ttu-id="436d5-151">*Дата и время*</span><span class="sxs-lookup"><span data-stu-id="436d5-151">*Datetime*</span></span> | <span data-ttu-id="436d5-152">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="436d5-152">Read/write</span></span><br><span data-ttu-id="436d5-153">Необязательный</span><span class="sxs-lookup"><span data-stu-id="436d5-153">Optional</span></span> | <span data-ttu-id="436d5-154">Дата, к которой требуется завершить отбор.</span><span class="sxs-lookup"><span data-stu-id="436d5-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="436d5-155">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="436d5-155">**Status**</span></span><br><span data-ttu-id="436d5-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="436d5-156">mshr_status</span></span><br><span data-ttu-id="436d5-157">*Набор параметров mshr_hcmcompletionstatus*</span><span class="sxs-lookup"><span data-stu-id="436d5-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="436d5-158">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="436d5-158">Read/write</span></span><br><span data-ttu-id="436d5-159">Требуется</span><span class="sxs-lookup"><span data-stu-id="436d5-159">Required</span></span> | <span data-ttu-id="436d5-160">Предоставляет статус кандидата для отбора.</span><span class="sxs-lookup"><span data-stu-id="436d5-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="436d5-161">**Дата завершения**</span><span class="sxs-lookup"><span data-stu-id="436d5-161">**Completed Date**</span></span><br><span data-ttu-id="436d5-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="436d5-162">mshr_completeddate</span></span><br><span data-ttu-id="436d5-163">*Дата и время*</span><span class="sxs-lookup"><span data-stu-id="436d5-163">*Datetime*</span></span> | <span data-ttu-id="436d5-164">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="436d5-164">Read/write</span></span><br><span data-ttu-id="436d5-165">Необязательный</span><span class="sxs-lookup"><span data-stu-id="436d5-165">Optional</span></span> | <span data-ttu-id="436d5-166">Дата завершения отбора.</span><span class="sxs-lookup"><span data-stu-id="436d5-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="436d5-167">**Основание**</span><span class="sxs-lookup"><span data-stu-id="436d5-167">**Notes**</span></span><br><span data-ttu-id="436d5-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="436d5-168">mshr_note</span></span><br><span data-ttu-id="436d5-169">*Строка*</span><span class="sxs-lookup"><span data-stu-id="436d5-169">*String*</span></span> | <span data-ttu-id="436d5-170">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="436d5-170">Read/write</span></span><br><span data-ttu-id="436d5-171">Необязательный</span><span class="sxs-lookup"><span data-stu-id="436d5-171">Optional</span></span> | <span data-ttu-id="436d5-172">Примечания для использования сотрудниками или менеджерами по найму персонала.</span><span class="sxs-lookup"><span data-stu-id="436d5-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="436d5-173">См. также</span><span class="sxs-lookup"><span data-stu-id="436d5-173">See also</span></span>

[<span data-ttu-id="436d5-174">Введение в интерфейс API интеграции системы отслеживания кандидатов</span><span class="sxs-lookup"><span data-stu-id="436d5-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="436d5-175">Пример запроса кандидата для приема на работу</span><span class="sxs-lookup"><span data-stu-id="436d5-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]