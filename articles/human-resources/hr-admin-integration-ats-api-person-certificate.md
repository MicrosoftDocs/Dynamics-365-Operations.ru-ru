---
title: Сертификат физического лица
description: В этом разделе описывается сущность сертификата физического лица для Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4587337d8fd52828309826f3301b6f053b267819
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466528"
---
# <a name="person-certificate"></a><span data-ttu-id="09668-103">Сертификат физического лица</span><span class="sxs-lookup"><span data-stu-id="09668-103">Person certificate</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="09668-104">В этом разделе описывается сущность сертификата физического лица для Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="09668-104">This topic describes the Person certificate entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="09668-105">Физическое имя: mshr_hcmpersoncertificateentity</span><span class="sxs-lookup"><span data-stu-id="09668-105">Physical name: mshr_hcmpersoncertificateentity</span></span>

## <a name="description"></a><span data-ttu-id="09668-106">описание</span><span class="sxs-lookup"><span data-stu-id="09668-106">Description</span></span>

<span data-ttu-id="09668-107">Эта сущность описывает профессиональные сертификаты кандидата.</span><span class="sxs-lookup"><span data-stu-id="09668-107">This entity describes the professional certificates of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="09668-108">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="09668-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="09668-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="09668-109">Properties</span></span>

| <span data-ttu-id="09668-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="09668-110">Property</span></span><br><span data-ttu-id="09668-111">**Физическое имя**</span><span class="sxs-lookup"><span data-stu-id="09668-111">**Physical name**</span></span><br><span data-ttu-id="09668-112">**_Вид_**</span><span class="sxs-lookup"><span data-stu-id="09668-112">**_Type_**</span></span> | <span data-ttu-id="09668-113">Использование</span><span class="sxs-lookup"><span data-stu-id="09668-113">Use</span></span> | <span data-ttu-id="09668-114">описание</span><span class="sxs-lookup"><span data-stu-id="09668-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="09668-115">**Код сущности сертификата физического лица**</span><span class="sxs-lookup"><span data-stu-id="09668-115">**Person Certificate Entity ID**</span></span><br><span data-ttu-id="09668-116">mshr_hcmpersoncertificateentityid</span><span class="sxs-lookup"><span data-stu-id="09668-116">mshr_hcmpersoncertificateentityid</span></span><br><span data-ttu-id="09668-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="09668-117">*GUID*</span></span> | <span data-ttu-id="09668-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="09668-118">Read-only</span></span><br><span data-ttu-id="09668-119">Требуется</span><span class="sxs-lookup"><span data-stu-id="09668-119">Required</span></span> | <span data-ttu-id="09668-120">Созданный системой уникальный идентификатор для записи сущности сертификата физического лица.</span><span class="sxs-lookup"><span data-stu-id="09668-120">System-generated unique identifier for the person certificate entity record.</span></span> |
| <span data-ttu-id="09668-121">**Номер субъекта**</span><span class="sxs-lookup"><span data-stu-id="09668-121">**Party Number**</span></span><br><span data-ttu-id="09668-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="09668-122">mshr_partynumber</span></span><br><span data-ttu-id="09668-123">*Строка*</span><span class="sxs-lookup"><span data-stu-id="09668-123">*String*</span></span> | <span data-ttu-id="09668-124">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="09668-124">Read/write</span></span><br><span data-ttu-id="09668-125">Требуется</span><span class="sxs-lookup"><span data-stu-id="09668-125">Required</span></span> | <span data-ttu-id="09668-126">ИД субъекта (физического лица) кандидата.</span><span class="sxs-lookup"><span data-stu-id="09668-126">The party (person) ID of the candidate.</span></span> |
| <span data-ttu-id="09668-127">**Значение ИД физического лица**</span><span class="sxs-lookup"><span data-stu-id="09668-127">**Person ID Value**</span></span><br><span data-ttu-id="09668-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="09668-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="09668-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="09668-129">*GUID*</span></span> | <span data-ttu-id="09668-130">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="09668-130">Read-only</span></span><br><span data-ttu-id="09668-131">Требуется</span><span class="sxs-lookup"><span data-stu-id="09668-131">Required</span></span><br><span data-ttu-id="09668-132">Внешний ключ: mshr_dirpersonentityid сущности mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="09668-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="09668-133">Созданный системой уникальный идентификатор записи сущности субъекта (физического лица).</span><span class="sxs-lookup"><span data-stu-id="09668-133">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="09668-134">**ИД типа сертификата**</span><span class="sxs-lookup"><span data-stu-id="09668-134">**Certificate Type ID**</span></span><br><span data-ttu-id="09668-135">mshr_certificatetypeid</span><span class="sxs-lookup"><span data-stu-id="09668-135">mshr_certificatetypeid</span></span><br><span data-ttu-id="09668-136">*Строка*</span><span class="sxs-lookup"><span data-stu-id="09668-136">*String*</span></span> | <span data-ttu-id="09668-137">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="09668-137">Read/write</span></span><br><span data-ttu-id="09668-138">Требуется</span><span class="sxs-lookup"><span data-stu-id="09668-138">Required</span></span> |  <span data-ttu-id="09668-139">Идентификатор типа сертификата, определенный в модуле Human Resources.</span><span class="sxs-lookup"><span data-stu-id="09668-139">The identifier of the certificate type defined in Human Resources.</span></span> |
| <span data-ttu-id="09668-140">**Значение ИД типа сертификата**</span><span class="sxs-lookup"><span data-stu-id="09668-140">**Certificate Type ID Value**</span></span><br><span data-ttu-id="09668-141">_mshr_fk_certificatetype_id_value</span><span class="sxs-lookup"><span data-stu-id="09668-141">_mshr_fk_certificatetype_id_value</span></span><br><span data-ttu-id="09668-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="09668-142">*GUID*</span></span> | <span data-ttu-id="09668-143">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="09668-143">Read-only</span></span><br><span data-ttu-id="09668-144">Требуется</span><span class="sxs-lookup"><span data-stu-id="09668-144">Required</span></span><br><span data-ttu-id="09668-145">Внешний ключ: mshr_hcmcertificatetypeentityid сущности mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="09668-145">Foreign key: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity</span></span> | <span data-ttu-id="09668-146">Созданный системой уникальный идентификатор типа сертификата в связанной сущности.</span><span class="sxs-lookup"><span data-stu-id="09668-146">System-generated unique identifier of the certificate type in the associated entity.</span></span> |
| <span data-ttu-id="09668-147">**Дата начала**</span><span class="sxs-lookup"><span data-stu-id="09668-147">**Start Date**</span></span><br><span data-ttu-id="09668-148">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="09668-148">mshr_startdate</span></span><br><span data-ttu-id="09668-149">*Дата и время*</span><span class="sxs-lookup"><span data-stu-id="09668-149">*Datetime*</span></span> | <span data-ttu-id="09668-150">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="09668-150">Read/write</span></span><br><span data-ttu-id="09668-151">Требуется</span><span class="sxs-lookup"><span data-stu-id="09668-151">Required</span></span> | <span data-ttu-id="09668-152">Дата выпуска сертификата.</span><span class="sxs-lookup"><span data-stu-id="09668-152">The date at which the certificate was issued.</span></span> |
| <span data-ttu-id="09668-153">**Дата окончания**</span><span class="sxs-lookup"><span data-stu-id="09668-153">**End Date**</span></span><br><span data-ttu-id="09668-154">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="09668-154">mshr_enddate</span></span><br><span data-ttu-id="09668-155">*Дата и время*</span><span class="sxs-lookup"><span data-stu-id="09668-155">*Datetime*</span></span> | <span data-ttu-id="09668-156">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="09668-156">Read/write</span></span><br><span data-ttu-id="09668-157">Необязательный</span><span class="sxs-lookup"><span data-stu-id="09668-157">Optional</span></span> | <span data-ttu-id="09668-158">Дата окончания срока действия сертификата.</span><span class="sxs-lookup"><span data-stu-id="09668-158">The date at which the certificate will expire.</span></span> |
| <span data-ttu-id="09668-159">**Основание**</span><span class="sxs-lookup"><span data-stu-id="09668-159">**Notes**</span></span><br><span data-ttu-id="09668-160">mshr_notes</span><span class="sxs-lookup"><span data-stu-id="09668-160">mshr_notes</span></span><br><span data-ttu-id="09668-161">*Строка*</span><span class="sxs-lookup"><span data-stu-id="09668-161">*String*</span></span> | <span data-ttu-id="09668-162">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="09668-162">Read/write</span></span><br><span data-ttu-id="09668-163">Необязательный</span><span class="sxs-lookup"><span data-stu-id="09668-163">Optional</span></span> | <span data-ttu-id="09668-164">Примечания для использования сотрудниками или менеджерами по найму персонала.</span><span class="sxs-lookup"><span data-stu-id="09668-164">Notes for use by hiring managers and recruiters.</span></span> |
| <span data-ttu-id="09668-165">**Основное поле**</span><span class="sxs-lookup"><span data-stu-id="09668-165">**Primary Field**</span></span><br><span data-ttu-id="09668-166">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="09668-166">mshr_primaryfield</span></span><br><span data-ttu-id="09668-167">*Строка*</span><span class="sxs-lookup"><span data-stu-id="09668-167">*String*</span></span> | <span data-ttu-id="09668-168">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="09668-168">Read-only</span></span><br><span data-ttu-id="09668-169">Требуется</span><span class="sxs-lookup"><span data-stu-id="09668-169">Required</span></span> |  <span data-ttu-id="09668-170">Поле для, использования в качестве идентификатора записи сущности.</span><span class="sxs-lookup"><span data-stu-id="09668-170">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="09668-171">Комбинация номера субъекта, ИД типа сертификата и даты начала.</span><span class="sxs-lookup"><span data-stu-id="09668-171">Combination of party number, certificate type ID, and start date.</span></span> |

## <a name="see-also"></a><span data-ttu-id="09668-172">См. также</span><span class="sxs-lookup"><span data-stu-id="09668-172">See also</span></span>

[<span data-ttu-id="09668-173">Введение в интерфейс API интеграции системы отслеживания кандидатов</span><span class="sxs-lookup"><span data-stu-id="09668-173">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="09668-174">Пример запроса кандидата для приема на работу</span><span class="sxs-lookup"><span data-stu-id="09668-174">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]