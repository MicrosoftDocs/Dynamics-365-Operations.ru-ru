---
title: Сертификат физического лица
description: В этом разделе описывается сущность сертификата физического лица для Dynamics 365 Human Resources.
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
ms.openlocfilehash: 5cdd742d6d36ccd7136f95e416507ed6e5e5a75a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055204"
---
# <a name="person-certificate"></a><span data-ttu-id="0d56b-103">Сертификат физического лица</span><span class="sxs-lookup"><span data-stu-id="0d56b-103">Person certificate</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0d56b-104">В этом разделе описывается сущность сертификата физического лица для Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0d56b-104">This topic describes the Person certificate entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="0d56b-105">Физическое имя: mshr_hcmpersoncertificateentity</span><span class="sxs-lookup"><span data-stu-id="0d56b-105">Physical name: mshr_hcmpersoncertificateentity</span></span>

## <a name="description"></a><span data-ttu-id="0d56b-106">описание</span><span class="sxs-lookup"><span data-stu-id="0d56b-106">Description</span></span>

<span data-ttu-id="0d56b-107">Эта сущность описывает профессиональные сертификаты кандидата.</span><span class="sxs-lookup"><span data-stu-id="0d56b-107">This entity describes the professional certificates of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="0d56b-108">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="0d56b-108">JSON representation</span></span>

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="0d56b-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="0d56b-109">Properties</span></span>

| <span data-ttu-id="0d56b-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="0d56b-110">Property</span></span><br><span data-ttu-id="0d56b-111">**Физическое имя**</span><span class="sxs-lookup"><span data-stu-id="0d56b-111">**Physical name**</span></span><br><span data-ttu-id="0d56b-112">**_Вид_**</span><span class="sxs-lookup"><span data-stu-id="0d56b-112">**_Type_**</span></span> | <span data-ttu-id="0d56b-113">Использование</span><span class="sxs-lookup"><span data-stu-id="0d56b-113">Use</span></span> | <span data-ttu-id="0d56b-114">описание</span><span class="sxs-lookup"><span data-stu-id="0d56b-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="0d56b-115">**Код сущности сертификата физического лица**</span><span class="sxs-lookup"><span data-stu-id="0d56b-115">**Person Certificate Entity ID**</span></span><br><span data-ttu-id="0d56b-116">mshr_hcmpersoncertificateentityid</span><span class="sxs-lookup"><span data-stu-id="0d56b-116">mshr_hcmpersoncertificateentityid</span></span><br><span data-ttu-id="0d56b-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="0d56b-117">*GUID*</span></span> | <span data-ttu-id="0d56b-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d56b-118">Read-only</span></span><br><span data-ttu-id="0d56b-119">Требуется</span><span class="sxs-lookup"><span data-stu-id="0d56b-119">Required</span></span> | <span data-ttu-id="0d56b-120">Созданный системой уникальный идентификатор для записи сущности сертификата физического лица.</span><span class="sxs-lookup"><span data-stu-id="0d56b-120">System-generated unique identifier for the person certificate entity record.</span></span> |
| <span data-ttu-id="0d56b-121">**Номер субъекта**</span><span class="sxs-lookup"><span data-stu-id="0d56b-121">**Party Number**</span></span><br><span data-ttu-id="0d56b-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="0d56b-122">mshr_partynumber</span></span><br><span data-ttu-id="0d56b-123">*Строка*</span><span class="sxs-lookup"><span data-stu-id="0d56b-123">*String*</span></span> | <span data-ttu-id="0d56b-124">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="0d56b-124">Read/write</span></span><br><span data-ttu-id="0d56b-125">Требуется</span><span class="sxs-lookup"><span data-stu-id="0d56b-125">Required</span></span> | <span data-ttu-id="0d56b-126">ИД субъекта (физического лица) кандидата.</span><span class="sxs-lookup"><span data-stu-id="0d56b-126">The party (person) ID of the candidate.</span></span> |
| <span data-ttu-id="0d56b-127">**Значение ИД физического лица**</span><span class="sxs-lookup"><span data-stu-id="0d56b-127">**Person ID Value**</span></span><br><span data-ttu-id="0d56b-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="0d56b-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="0d56b-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="0d56b-129">*GUID*</span></span> | <span data-ttu-id="0d56b-130">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d56b-130">Read-only</span></span><br><span data-ttu-id="0d56b-131">Требуется</span><span class="sxs-lookup"><span data-stu-id="0d56b-131">Required</span></span><br><span data-ttu-id="0d56b-132">Внешний ключ: mshr_dirpersonentityid сущности mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="0d56b-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="0d56b-133">Созданный системой уникальный идентификатор записи сущности субъекта (физического лица).</span><span class="sxs-lookup"><span data-stu-id="0d56b-133">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="0d56b-134">**ИД типа сертификата**</span><span class="sxs-lookup"><span data-stu-id="0d56b-134">**Certificate Type ID**</span></span><br><span data-ttu-id="0d56b-135">mshr_certificatetypeid</span><span class="sxs-lookup"><span data-stu-id="0d56b-135">mshr_certificatetypeid</span></span><br><span data-ttu-id="0d56b-136">*Строка*</span><span class="sxs-lookup"><span data-stu-id="0d56b-136">*String*</span></span> | <span data-ttu-id="0d56b-137">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="0d56b-137">Read/write</span></span><br><span data-ttu-id="0d56b-138">Требуется</span><span class="sxs-lookup"><span data-stu-id="0d56b-138">Required</span></span> |  <span data-ttu-id="0d56b-139">Идентификатор типа сертификата, определенный в модуле Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0d56b-139">The identifier of the certificate type defined in Human Resources.</span></span> |
| <span data-ttu-id="0d56b-140">**Значение ИД типа сертификата**</span><span class="sxs-lookup"><span data-stu-id="0d56b-140">**Certificate Type ID Value**</span></span><br><span data-ttu-id="0d56b-141">_mshr_fk_certificatetype_id_value</span><span class="sxs-lookup"><span data-stu-id="0d56b-141">_mshr_fk_certificatetype_id_value</span></span><br><span data-ttu-id="0d56b-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="0d56b-142">*GUID*</span></span> | <span data-ttu-id="0d56b-143">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d56b-143">Read-only</span></span><br><span data-ttu-id="0d56b-144">Требуется</span><span class="sxs-lookup"><span data-stu-id="0d56b-144">Required</span></span><br><span data-ttu-id="0d56b-145">Внешний ключ: mshr_hcmcertificatetypeentityid сущности mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="0d56b-145">Foreign key: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity</span></span> | <span data-ttu-id="0d56b-146">Созданный системой уникальный идентификатор типа сертификата в связанной сущности.</span><span class="sxs-lookup"><span data-stu-id="0d56b-146">System-generated unique identifier of the certificate type in the associated entity.</span></span> |
| <span data-ttu-id="0d56b-147">**Дата начала**</span><span class="sxs-lookup"><span data-stu-id="0d56b-147">**Start Date**</span></span><br><span data-ttu-id="0d56b-148">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="0d56b-148">mshr_startdate</span></span><br><span data-ttu-id="0d56b-149">*Дата и время*</span><span class="sxs-lookup"><span data-stu-id="0d56b-149">*Datetime*</span></span> | <span data-ttu-id="0d56b-150">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="0d56b-150">Read/write</span></span><br><span data-ttu-id="0d56b-151">Требуется</span><span class="sxs-lookup"><span data-stu-id="0d56b-151">Required</span></span> | <span data-ttu-id="0d56b-152">Дата выпуска сертификата.</span><span class="sxs-lookup"><span data-stu-id="0d56b-152">The date at which the certificate was issued.</span></span> |
| <span data-ttu-id="0d56b-153">**Дата окончания**</span><span class="sxs-lookup"><span data-stu-id="0d56b-153">**End Date**</span></span><br><span data-ttu-id="0d56b-154">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="0d56b-154">mshr_enddate</span></span><br><span data-ttu-id="0d56b-155">*Дата и время*</span><span class="sxs-lookup"><span data-stu-id="0d56b-155">*Datetime*</span></span> | <span data-ttu-id="0d56b-156">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="0d56b-156">Read/write</span></span><br><span data-ttu-id="0d56b-157">Необязательный</span><span class="sxs-lookup"><span data-stu-id="0d56b-157">Optional</span></span> | <span data-ttu-id="0d56b-158">Дата окончания срока действия сертификата.</span><span class="sxs-lookup"><span data-stu-id="0d56b-158">The date at which the certificate will expire.</span></span> |
| <span data-ttu-id="0d56b-159">**Основание**</span><span class="sxs-lookup"><span data-stu-id="0d56b-159">**Notes**</span></span><br><span data-ttu-id="0d56b-160">mshr_notes</span><span class="sxs-lookup"><span data-stu-id="0d56b-160">mshr_notes</span></span><br><span data-ttu-id="0d56b-161">*Строка*</span><span class="sxs-lookup"><span data-stu-id="0d56b-161">*String*</span></span> | <span data-ttu-id="0d56b-162">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="0d56b-162">Read/write</span></span><br><span data-ttu-id="0d56b-163">Необязательный</span><span class="sxs-lookup"><span data-stu-id="0d56b-163">Optional</span></span> | <span data-ttu-id="0d56b-164">Примечания для использования сотрудниками или менеджерами по найму персонала.</span><span class="sxs-lookup"><span data-stu-id="0d56b-164">Notes for use by hiring managers and recruiters.</span></span> |
| <span data-ttu-id="0d56b-165">**Основное поле**</span><span class="sxs-lookup"><span data-stu-id="0d56b-165">**Primary Field**</span></span><br><span data-ttu-id="0d56b-166">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="0d56b-166">mshr_primaryfield</span></span><br><span data-ttu-id="0d56b-167">*Строка*</span><span class="sxs-lookup"><span data-stu-id="0d56b-167">*String*</span></span> | <span data-ttu-id="0d56b-168">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d56b-168">Read-only</span></span><br><span data-ttu-id="0d56b-169">Требуется</span><span class="sxs-lookup"><span data-stu-id="0d56b-169">Required</span></span> |  <span data-ttu-id="0d56b-170">Поле для, использования в качестве идентификатора записи сущности.</span><span class="sxs-lookup"><span data-stu-id="0d56b-170">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="0d56b-171">Комбинация номера субъекта, ИД типа сертификата и даты начала.</span><span class="sxs-lookup"><span data-stu-id="0d56b-171">Combination of party number, certificate type ID, and start date.</span></span> |

## <a name="see-also"></a><span data-ttu-id="0d56b-172">См. также</span><span class="sxs-lookup"><span data-stu-id="0d56b-172">See also</span></span>

[<span data-ttu-id="0d56b-173">Введение в интерфейс API интеграции системы отслеживания кандидатов</span><span class="sxs-lookup"><span data-stu-id="0d56b-173">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="0d56b-174">Пример запроса кандидата для приема на работу</span><span class="sxs-lookup"><span data-stu-id="0d56b-174">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]