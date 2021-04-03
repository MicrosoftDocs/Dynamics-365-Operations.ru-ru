---
title: Тип сертификата
description: В этом разделе описывается сущность типа сертификата для Dynamics 365 Human Resources.
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
ms.openlocfilehash: 962bccb3aaab16322d072417660ec3aac821183b
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467489"
---
# <a name="certificate-type"></a><span data-ttu-id="acf35-103">Тип сертификата</span><span class="sxs-lookup"><span data-stu-id="acf35-103">Certificate type</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="acf35-104">В этом разделе описывается сущность типа сертификата для Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="acf35-104">This topic describes the Certificate type entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="acf35-105">Физическое имя: mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="acf35-105">Physical name: mshr_hcmcertificatetypeentity</span></span>

## <a name="description"></a><span data-ttu-id="acf35-106">описание</span><span class="sxs-lookup"><span data-stu-id="acf35-106">Description</span></span>

<span data-ttu-id="acf35-107">Эта сущность определяет список профессиональных типов сертификатов, настроенных в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="acf35-107">This entity defines the list of professional certificate types set up in Human Resources.</span></span> <span data-ttu-id="acf35-108">Эта сущность не связана с конкретным юридическим лицом (компанией).</span><span class="sxs-lookup"><span data-stu-id="acf35-108">The entity isn't specific to a legal entity (company).</span></span>

## <a name="json-representation"></a><span data-ttu-id="acf35-109">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="acf35-109">JSON representation</span></span>

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="acf35-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="acf35-110">Properties</span></span>

| <span data-ttu-id="acf35-111">Свойство</span><span class="sxs-lookup"><span data-stu-id="acf35-111">Property</span></span><br><span data-ttu-id="acf35-112">**Физическое имя**</span><span class="sxs-lookup"><span data-stu-id="acf35-112">**Physical name**</span></span><br><span data-ttu-id="acf35-113">**_Вид_**</span><span class="sxs-lookup"><span data-stu-id="acf35-113">**_Type_**</span></span> | <span data-ttu-id="acf35-114">Использование</span><span class="sxs-lookup"><span data-stu-id="acf35-114">Use</span></span> | <span data-ttu-id="acf35-115">описание</span><span class="sxs-lookup"><span data-stu-id="acf35-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="acf35-116">**Код сущности типа сертификата**</span><span class="sxs-lookup"><span data-stu-id="acf35-116">**Certificate Type Entity ID**</span></span><br><span data-ttu-id="acf35-117">mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="acf35-117">mshr_hcmcertificatetypeentityid</span></span><br><span data-ttu-id="acf35-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="acf35-118">*GUID*</span></span> | <span data-ttu-id="acf35-119">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="acf35-119">Read-only</span></span><br><span data-ttu-id="acf35-120">Требуется</span><span class="sxs-lookup"><span data-stu-id="acf35-120">Required</span></span> 
<span data-ttu-id="acf35-121">Создано системой</span><span class="sxs-lookup"><span data-stu-id="acf35-121">System-generated</span></span> | <span data-ttu-id="acf35-122">Уникальный первичный идентификатор для типа сертификата.</span><span class="sxs-lookup"><span data-stu-id="acf35-122">Unique primary identifier for the certificate type.</span></span> |
| <span data-ttu-id="acf35-123">**Тип сертификата**</span><span class="sxs-lookup"><span data-stu-id="acf35-123">**Certificate Type**</span></span><br><span data-ttu-id="acf35-124">mshr_certificatetype</span><span class="sxs-lookup"><span data-stu-id="acf35-124">mshr_certificatetype</span></span><br><span data-ttu-id="acf35-125">*Строка*</span><span class="sxs-lookup"><span data-stu-id="acf35-125">*String*</span></span> | <span data-ttu-id="acf35-126">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="acf35-126">Read/write</span></span><br><span data-ttu-id="acf35-127">Требуется</span><span class="sxs-lookup"><span data-stu-id="acf35-127">Required</span></span> | <span data-ttu-id="acf35-128">Уникальный определенный пользователем идентификатор для типа сертификата.</span><span class="sxs-lookup"><span data-stu-id="acf35-128">Unique user-readable identifier for the certificate type.</span></span> |
| <span data-ttu-id="acf35-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="acf35-129">**Description**</span></span><br><span data-ttu-id="acf35-130">mshr_description</span><span class="sxs-lookup"><span data-stu-id="acf35-130">mshr_description</span></span><br><span data-ttu-id="acf35-131">*Строка*</span><span class="sxs-lookup"><span data-stu-id="acf35-131">*String*</span></span> | <span data-ttu-id="acf35-132">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="acf35-132">Read/write</span></span><br><span data-ttu-id="acf35-133">Требуется</span><span class="sxs-lookup"><span data-stu-id="acf35-133">Required</span></span> | <span data-ttu-id="acf35-134">Описание типа сертификата.</span><span class="sxs-lookup"><span data-stu-id="acf35-134">Description of the certificate type.</span></span> |
| <span data-ttu-id="acf35-135">**Требует возобновления**</span><span class="sxs-lookup"><span data-stu-id="acf35-135">**Require Renewal**</span></span><br><span data-ttu-id="acf35-136">mshr_requirerenewal</span><span class="sxs-lookup"><span data-stu-id="acf35-136">mshr_requirerenewal</span></span><br><span data-ttu-id="acf35-137">*Набор параметров mshr_noyes*</span><span class="sxs-lookup"><span data-stu-id="acf35-137">*mshr_noyes option set*</span></span> | <span data-ttu-id="acf35-138">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="acf35-138">Read/write</span></span><br><span data-ttu-id="acf35-139">Необязательный</span><span class="sxs-lookup"><span data-stu-id="acf35-139">Optional</span></span> | <span data-ttu-id="acf35-140">Указывает, требуется ли обновление для сертификата.</span><span class="sxs-lookup"><span data-stu-id="acf35-140">Indicates whether renewal is required for the certificate.</span></span> |

## <a name="see-also"></a><span data-ttu-id="acf35-141">См. также</span><span class="sxs-lookup"><span data-stu-id="acf35-141">See also</span></span>

[<span data-ttu-id="acf35-142">Введение в интерфейс API интеграции системы отслеживания кандидатов</span><span class="sxs-lookup"><span data-stu-id="acf35-142">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="acf35-143">Пример запроса кандидата для приема на работу</span><span class="sxs-lookup"><span data-stu-id="acf35-143">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]