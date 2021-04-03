---
title: Типы отбора
description: В этом разделе описываются типы отбора для Dynamics 365 Human Resources.
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
ms.openlocfilehash: d3a45d802ab6b574338a09e77d432357cb9df507
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465926"
---
# <a name="screening-types"></a><span data-ttu-id="ae49d-103">Типы отбора</span><span class="sxs-lookup"><span data-stu-id="ae49d-103">Screening types</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ae49d-104">В этом разделе описываются типы отбора для Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ae49d-104">This topic describes the Screening types entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="ae49d-105">Физическое имя: mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="ae49d-105">Physical name: mshr_hcmscreeningtypeentity</span></span>

## <a name="description"></a><span data-ttu-id="ae49d-106">описание</span><span class="sxs-lookup"><span data-stu-id="ae49d-106">Description</span></span>

<span data-ttu-id="ae49d-107">Эта сущность описывает типы отбора, которые настраиваются компанией для процессов отбора сотрудников перед приемом на работу и текущего отбора.</span><span class="sxs-lookup"><span data-stu-id="ae49d-107">This entity describes the screening types set up by the company for pre-employment and ongoing employee screening processes.</span></span>

## <a name="json-representation"></a><span data-ttu-id="ae49d-108">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="ae49d-108">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="ae49d-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="ae49d-109">Properties</span></span>

| <span data-ttu-id="ae49d-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="ae49d-110">Property</span></span><br><span data-ttu-id="ae49d-111">**Физическое имя**</span><span class="sxs-lookup"><span data-stu-id="ae49d-111">**Physical name**</span></span><br><span data-ttu-id="ae49d-112">**_Вид_**</span><span class="sxs-lookup"><span data-stu-id="ae49d-112">**_Type_**</span></span> | <span data-ttu-id="ae49d-113">Использование</span><span class="sxs-lookup"><span data-stu-id="ae49d-113">Use</span></span> | <span data-ttu-id="ae49d-114">описание</span><span class="sxs-lookup"><span data-stu-id="ae49d-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ae49d-115">**ИД сущности типа отбора**</span><span class="sxs-lookup"><span data-stu-id="ae49d-115">**Screening Type Entity ID**</span></span><br><span data-ttu-id="ae49d-116">mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="ae49d-116">mshr_hcmscreeningtypeentityid</span></span><br><span data-ttu-id="ae49d-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="ae49d-117">*GUID*</span></span> | <span data-ttu-id="ae49d-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae49d-118">Read-only</span></span><br><span data-ttu-id="ae49d-119">Требуется</span><span class="sxs-lookup"><span data-stu-id="ae49d-119">Required</span></span><br><span data-ttu-id="ae49d-120">Создано системой</span><span class="sxs-lookup"><span data-stu-id="ae49d-120">System-generated</span></span> | <span data-ttu-id="ae49d-121">Уникальный первичный идентификатор записи типа отбора.</span><span class="sxs-lookup"><span data-stu-id="ae49d-121">Unique primary identifier for the screening type record.</span></span> |
| <span data-ttu-id="ae49d-122">**ИД типа отбора**</span><span class="sxs-lookup"><span data-stu-id="ae49d-122">**Screening Type ID**</span></span><br><span data-ttu-id="ae49d-123">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="ae49d-123">mshr_screeningtypeid</span></span><br><span data-ttu-id="ae49d-124">*Строка*</span><span class="sxs-lookup"><span data-stu-id="ae49d-124">*String*</span></span> | <span data-ttu-id="ae49d-125">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ae49d-125">Read/write</span></span><br><span data-ttu-id="ae49d-126">Требуется</span><span class="sxs-lookup"><span data-stu-id="ae49d-126">Required</span></span> | <span data-ttu-id="ae49d-127">Определенный пользователем уникальный идентификатор для типа отбора.</span><span class="sxs-lookup"><span data-stu-id="ae49d-127">User-defined unique identifier for the screening type.</span></span> |
| <span data-ttu-id="ae49d-128">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ae49d-128">**Description**</span></span><br><span data-ttu-id="ae49d-129">mshr_description</span><span class="sxs-lookup"><span data-stu-id="ae49d-129">mshr_description</span></span><br><span data-ttu-id="ae49d-130">*Строка*</span><span class="sxs-lookup"><span data-stu-id="ae49d-130">*String*</span></span> | <span data-ttu-id="ae49d-131">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ae49d-131">Read/write</span></span><br><span data-ttu-id="ae49d-132">Требуется</span><span class="sxs-lookup"><span data-stu-id="ae49d-132">Required</span></span> | <span data-ttu-id="ae49d-133">Описание типа отбора.</span><span class="sxs-lookup"><span data-stu-id="ae49d-133">The description of the screening type.</span></span> |
| <span data-ttu-id="ae49d-134">**Единица частоты**</span><span class="sxs-lookup"><span data-stu-id="ae49d-134">**Frequency Unit**</span></span><br><span data-ttu-id="ae49d-135">mshr_frequencyunit</span><span class="sxs-lookup"><span data-stu-id="ae49d-135">mshr_frequencyunit</span></span><br><span data-ttu-id="ae49d-136">*Набор параметров mshr_hcmfrequencyunit*</span><span class="sxs-lookup"><span data-stu-id="ae49d-136">*mshr_hcmfrequencyunit option set*</span></span> | <span data-ttu-id="ae49d-137">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ae49d-137">Read/write</span></span><br><span data-ttu-id="ae49d-138">Требуется</span><span class="sxs-lookup"><span data-stu-id="ae49d-138">Required</span></span> | <span data-ttu-id="ae49d-139">Описывает частоту, с которой необходимо выполнять отбор (обследование) для назначенного физического лица.</span><span class="sxs-lookup"><span data-stu-id="ae49d-139">Describes the frequency with which the screening must be completed for the assigned person.</span></span> |
| <span data-ttu-id="ae49d-140">**Создать на основе**</span><span class="sxs-lookup"><span data-stu-id="ae49d-140">**Generate From**</span></span><br><span data-ttu-id="ae49d-141">mshr_generatefrom</span><span class="sxs-lookup"><span data-stu-id="ae49d-141">mshr_generatefrom</span></span><br><span data-ttu-id="ae49d-142">*Набор параметров mshr_hcmfrequencygeneratefrom*</span><span class="sxs-lookup"><span data-stu-id="ae49d-142">*mshr_hcmfrequencygeneratefrom option set*</span></span> | <span data-ttu-id="ae49d-143">Чтение-запись</span><span class="sxs-lookup"><span data-stu-id="ae49d-143">Read-write</span></span><br><span data-ttu-id="ae49d-144">Требуется</span><span class="sxs-lookup"><span data-stu-id="ae49d-144">Required</span></span> | <span data-ttu-id="ae49d-145">Если значением частоты является любое значение, отличное от "Только однократно", значение GenerateFrom определяет дату, начиная с которой будет рассчитываться следующее событие отбора (обследования).</span><span class="sxs-lookup"><span data-stu-id="ae49d-145">If the Frequency value is any value other than “One-time only”, the GenerateFrom value determines the date from which to calculate the next screening event.</span></span> |
| <span data-ttu-id="ae49d-146">**Интервал частот**</span><span class="sxs-lookup"><span data-stu-id="ae49d-146">**Frequency Interval**</span></span><br><span data-ttu-id="ae49d-147">mshr_frequencyinterval</span><span class="sxs-lookup"><span data-stu-id="ae49d-147">mshr_frequencyinterval</span></span><br><span data-ttu-id="ae49d-148">*Целое число*</span><span class="sxs-lookup"><span data-stu-id="ae49d-148">*Integer*</span></span> | <span data-ttu-id="ae49d-149">Чтение-запись</span><span class="sxs-lookup"><span data-stu-id="ae49d-149">Read-write</span></span><br><span data-ttu-id="ae49d-150">Требуется</span><span class="sxs-lookup"><span data-stu-id="ae49d-150">Required</span></span> | <span data-ttu-id="ae49d-151">Если значением частоты является любое значение, отличное от "Только однократно", необходимо определить интервал для единиц измерения времени между каждым событием отбора (обследования).</span><span class="sxs-lookup"><span data-stu-id="ae49d-151">If the Frequency value is any value other than “One-time only”, you must define an interval for the units of time between each screening event.</span></span> |

## <a name="see-also"></a><span data-ttu-id="ae49d-152">См. также</span><span class="sxs-lookup"><span data-stu-id="ae49d-152">See also</span></span>

[<span data-ttu-id="ae49d-153">Введение в интерфейс API интеграции системы отслеживания кандидатов</span><span class="sxs-lookup"><span data-stu-id="ae49d-153">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="ae49d-154">Пример запроса кандидата для приема на работу</span><span class="sxs-lookup"><span data-stu-id="ae49d-154">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]