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
ms.openlocfilehash: 1d2d53a628ef43d50bd83fd6b62807f44eddd653
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125721"
---
# <a name="certificate-type"></a><span data-ttu-id="ea74b-103">Тип сертификата</span><span class="sxs-lookup"><span data-stu-id="ea74b-103">Certificate type</span></span>

<span data-ttu-id="ea74b-104">В этом разделе описывается сущность типа сертификата для Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ea74b-104">This topic describes the Certificate type entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="ea74b-105">Физическое имя: mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="ea74b-105">Physical name: mshr_hcmcertificatetypeentity</span></span>

## <a name="description"></a><span data-ttu-id="ea74b-106">описание</span><span class="sxs-lookup"><span data-stu-id="ea74b-106">Description</span></span>

<span data-ttu-id="ea74b-107">Эта сущность определяет список профессиональных типов сертификатов, настроенных в Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ea74b-107">This entity defines the list of professional certificate types set up in Human Resources.</span></span> <span data-ttu-id="ea74b-108">Эта сущность не связана с конкретным юридическим лицом (компанией).</span><span class="sxs-lookup"><span data-stu-id="ea74b-108">The entity isn't specific to a legal entity (company).</span></span>

## <a name="json-representation"></a><span data-ttu-id="ea74b-109">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="ea74b-109">JSON representation</span></span>

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="ea74b-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="ea74b-110">Properties</span></span>

| <span data-ttu-id="ea74b-111">Свойство</span><span class="sxs-lookup"><span data-stu-id="ea74b-111">Property</span></span><br><span data-ttu-id="ea74b-112">**Физическое имя**</span><span class="sxs-lookup"><span data-stu-id="ea74b-112">**Physical name**</span></span><br><span data-ttu-id="ea74b-113">**_Вид_**</span><span class="sxs-lookup"><span data-stu-id="ea74b-113">**_Type_**</span></span> | <span data-ttu-id="ea74b-114">Использование</span><span class="sxs-lookup"><span data-stu-id="ea74b-114">Use</span></span> | <span data-ttu-id="ea74b-115">описание</span><span class="sxs-lookup"><span data-stu-id="ea74b-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ea74b-116">**Код сущности типа сертификата**</span><span class="sxs-lookup"><span data-stu-id="ea74b-116">**Certificate Type Entity ID**</span></span><br><span data-ttu-id="ea74b-117">mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="ea74b-117">mshr_hcmcertificatetypeentityid</span></span><br><span data-ttu-id="ea74b-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="ea74b-118">*GUID*</span></span> | <span data-ttu-id="ea74b-119">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="ea74b-119">Read-only</span></span><br><span data-ttu-id="ea74b-120">Требуется</span><span class="sxs-lookup"><span data-stu-id="ea74b-120">Required</span></span> 
<span data-ttu-id="ea74b-121">Создано системой</span><span class="sxs-lookup"><span data-stu-id="ea74b-121">System-generated</span></span> | <span data-ttu-id="ea74b-122">Уникальный первичный идентификатор для типа сертификата.</span><span class="sxs-lookup"><span data-stu-id="ea74b-122">Unique primary identifier for the certificate type.</span></span> |
| <span data-ttu-id="ea74b-123">**Тип сертификата**</span><span class="sxs-lookup"><span data-stu-id="ea74b-123">**Certificate Type**</span></span><br><span data-ttu-id="ea74b-124">mshr_certificatetype</span><span class="sxs-lookup"><span data-stu-id="ea74b-124">mshr_certificatetype</span></span><br><span data-ttu-id="ea74b-125">*Строка*</span><span class="sxs-lookup"><span data-stu-id="ea74b-125">*String*</span></span> | <span data-ttu-id="ea74b-126">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ea74b-126">Read/write</span></span><br><span data-ttu-id="ea74b-127">Требуется</span><span class="sxs-lookup"><span data-stu-id="ea74b-127">Required</span></span> | <span data-ttu-id="ea74b-128">Уникальный определенный пользователем идентификатор для типа сертификата.</span><span class="sxs-lookup"><span data-stu-id="ea74b-128">Unique user-readable identifier for the certificate type.</span></span> |
| <span data-ttu-id="ea74b-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ea74b-129">**Description**</span></span><br><span data-ttu-id="ea74b-130">mshr_description</span><span class="sxs-lookup"><span data-stu-id="ea74b-130">mshr_description</span></span><br><span data-ttu-id="ea74b-131">*Строка*</span><span class="sxs-lookup"><span data-stu-id="ea74b-131">*String*</span></span> | <span data-ttu-id="ea74b-132">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ea74b-132">Read/write</span></span><br><span data-ttu-id="ea74b-133">Требуется</span><span class="sxs-lookup"><span data-stu-id="ea74b-133">Required</span></span> | <span data-ttu-id="ea74b-134">Описание типа сертификата.</span><span class="sxs-lookup"><span data-stu-id="ea74b-134">Description of the certificate type.</span></span> |
| <span data-ttu-id="ea74b-135">**Требует возобновления**</span><span class="sxs-lookup"><span data-stu-id="ea74b-135">**Require Renewal**</span></span><br><span data-ttu-id="ea74b-136">mshr_requirerenewal</span><span class="sxs-lookup"><span data-stu-id="ea74b-136">mshr_requirerenewal</span></span><br><span data-ttu-id="ea74b-137">*Набор параметров mshr_noyes*</span><span class="sxs-lookup"><span data-stu-id="ea74b-137">*mshr_noyes option set*</span></span> | <span data-ttu-id="ea74b-138">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ea74b-138">Read/write</span></span><br><span data-ttu-id="ea74b-139">Необязательный</span><span class="sxs-lookup"><span data-stu-id="ea74b-139">Optional</span></span> | <span data-ttu-id="ea74b-140">Указывает, требуется ли обновление для сертификата.</span><span class="sxs-lookup"><span data-stu-id="ea74b-140">Indicates whether renewal is required for the certificate.</span></span> |

## <a name="see-also"></a><span data-ttu-id="ea74b-141">См. также</span><span class="sxs-lookup"><span data-stu-id="ea74b-141">See also</span></span>

[<span data-ttu-id="ea74b-142">Введение в интерфейс API интеграции системы отслеживания кандидатов</span><span class="sxs-lookup"><span data-stu-id="ea74b-142">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="ea74b-143">Пример запроса кандидата для приема на работу</span><span class="sxs-lookup"><span data-stu-id="ea74b-143">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

