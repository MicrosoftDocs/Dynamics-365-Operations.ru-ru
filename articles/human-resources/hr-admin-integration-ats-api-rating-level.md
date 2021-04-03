---
title: Уровень рейтинга
description: В этом разделе описывается сущность уровня рейтинга для Dynamics 365 Human Resources.
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
ms.openlocfilehash: 2dbdbea7087d8bca8563da10d1bf9a97df24e8b3
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464750"
---
# <a name="rating-level"></a><span data-ttu-id="51887-103">Уровень рейтинга</span><span class="sxs-lookup"><span data-stu-id="51887-103">Rating level</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="51887-104">В этом разделе описывается сущность уровня рейтинга для Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="51887-104">This topic describes the Rating level entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="51887-105">Физическое имя: mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="51887-105">Physical name: mshr_hcmratinglevelentity</span></span>

## <a name="description"></a><span data-ttu-id="51887-106">описание</span><span class="sxs-lookup"><span data-stu-id="51887-106">Description</span></span>

<span data-ttu-id="51887-107">Эта сущность предоставляет доступные уровни рейтинга для навыков.</span><span class="sxs-lookup"><span data-stu-id="51887-107">This entity provides the available rating levels for skills.</span></span> <span data-ttu-id="51887-108">Уровни рейтинга применяются для всех юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="51887-108">Rating levels apply across all legal entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="51887-109">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="51887-109">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="51887-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="51887-110">Properties</span></span>

| <span data-ttu-id="51887-111">Свойство</span><span class="sxs-lookup"><span data-stu-id="51887-111">Property</span></span><br><span data-ttu-id="51887-112">**Физическое имя**</span><span class="sxs-lookup"><span data-stu-id="51887-112">**Physical name**</span></span><br><span data-ttu-id="51887-113">**_Вид_**</span><span class="sxs-lookup"><span data-stu-id="51887-113">**_Type_**</span></span> | <span data-ttu-id="51887-114">Использование</span><span class="sxs-lookup"><span data-stu-id="51887-114">Use</span></span> | <span data-ttu-id="51887-115">описание</span><span class="sxs-lookup"><span data-stu-id="51887-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="51887-116">**ИД сущности уровня рейтинга**</span><span class="sxs-lookup"><span data-stu-id="51887-116">**Rating Level Entity ID**</span></span><br><span data-ttu-id="51887-117">mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="51887-117">mshr_hcmratinglevelentityid</span></span><br><span data-ttu-id="51887-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="51887-118">*GUID*</span></span> | <span data-ttu-id="51887-119">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="51887-119">Read-only</span></span><br><span data-ttu-id="51887-120">Требуется</span><span class="sxs-lookup"><span data-stu-id="51887-120">Required</span></span><br><span data-ttu-id="51887-121">Создано системой</span><span class="sxs-lookup"><span data-stu-id="51887-121">System-generated</span></span> | <span data-ttu-id="51887-122">Созданный системой уникальный идентификатор для уровня.</span><span class="sxs-lookup"><span data-stu-id="51887-122">The system-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="51887-123">**Код уровня оценки**</span><span class="sxs-lookup"><span data-stu-id="51887-123">**Rating Level ID**</span></span><br><span data-ttu-id="51887-124">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="51887-124">mshr_ratinglevelid</span></span><br><span data-ttu-id="51887-125">*Строка*</span><span class="sxs-lookup"><span data-stu-id="51887-125">*String*</span></span> | <span data-ttu-id="51887-126">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="51887-126">Read/write</span></span><br><span data-ttu-id="51887-127">Требуется</span><span class="sxs-lookup"><span data-stu-id="51887-127">Required</span></span> | <span data-ttu-id="51887-128">Понятный пользователю уникальный идентификатор для уровня.</span><span class="sxs-lookup"><span data-stu-id="51887-128">User-readable unique identifier for the level.</span></span> |
| <span data-ttu-id="51887-129">**ИД модели рейтинга**</span><span class="sxs-lookup"><span data-stu-id="51887-129">**Rating Model ID**</span></span><br><span data-ttu-id="51887-130">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="51887-130">mshr_ratingmodelid</span></span><br><span data-ttu-id="51887-131">*Строка*</span><span class="sxs-lookup"><span data-stu-id="51887-131">*String*</span></span> | <span data-ttu-id="51887-132">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="51887-132">Read/write</span></span><br><span data-ttu-id="51887-133">Требуется</span><span class="sxs-lookup"><span data-stu-id="51887-133">Required</span></span> | <span data-ttu-id="51887-134">Модель рейтинга, к которой принадлежит уровень рейтинга.</span><span class="sxs-lookup"><span data-stu-id="51887-134">The rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="51887-135">**ИД сущности модели рейтинга**</span><span class="sxs-lookup"><span data-stu-id="51887-135">**Rating Model Entity ID**</span></span><br><span data-ttu-id="51887-136">_mshr_fk_ratingmodelentity_id_value</span><span class="sxs-lookup"><span data-stu-id="51887-136">_mshr_fk_ratingmodelentity_id_value</span></span><br><span data-ttu-id="51887-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="51887-137">*GUID*</span></span> | <span data-ttu-id="51887-138">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="51887-138">Read-only</span></span><br><span data-ttu-id="51887-139">Требуется</span><span class="sxs-lookup"><span data-stu-id="51887-139">Required</span></span><br><span data-ttu-id="51887-140">Внешний ключ: mshr_hcmratingmodelentityid сущности mshr_hcmratingmodelentity</span><span class="sxs-lookup"><span data-stu-id="51887-140">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span></span> | <span data-ttu-id="51887-141">Созданный системой идентификатор модели рейтинга, к которой принадлежит уровень рейтинга.</span><span class="sxs-lookup"><span data-stu-id="51887-141">The system-generated identifier for the rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="51887-142">**Описание**</span><span class="sxs-lookup"><span data-stu-id="51887-142">**Description**</span></span><br><span data-ttu-id="51887-143">mshr_description</span><span class="sxs-lookup"><span data-stu-id="51887-143">mshr_description</span></span><br><span data-ttu-id="51887-144">*Строка*</span><span class="sxs-lookup"><span data-stu-id="51887-144">*String*</span></span> | <span data-ttu-id="51887-145">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="51887-145">Read/write</span></span><br><span data-ttu-id="51887-146">Требуется</span><span class="sxs-lookup"><span data-stu-id="51887-146">Required</span></span> | <span data-ttu-id="51887-147">Описание выбранного уровня рейтинга.</span><span class="sxs-lookup"><span data-stu-id="51887-147">The description of the rating level.</span></span> |
| <span data-ttu-id="51887-148">**Множитель**</span><span class="sxs-lookup"><span data-stu-id="51887-148">**Factor**</span></span><br><span data-ttu-id="51887-149">mshr_factor</span><span class="sxs-lookup"><span data-stu-id="51887-149">mshr_factor</span></span><br><span data-ttu-id="51887-150">*Целое число*</span><span class="sxs-lookup"><span data-stu-id="51887-150">*Integer*</span></span> | <span data-ttu-id="51887-151">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="51887-151">Read/write</span></span><br><span data-ttu-id="51887-152">Требуется</span><span class="sxs-lookup"><span data-stu-id="51887-152">Required</span></span> | <span data-ttu-id="51887-153">Коэффициент для уровня рейтинга.</span><span class="sxs-lookup"><span data-stu-id="51887-153">The factor for the rating level.</span></span> <span data-ttu-id="51887-154">Если сравнить номенклатуры с разным числом уровней рейтинга, этот коэффициент используется для нормализации оценок.</span><span class="sxs-lookup"><span data-stu-id="51887-154">When you compare items with a different number of rating levels, the factor is used to normalize the scores.</span></span> <span data-ttu-id="51887-155">Значение должно быть целым числом от 0 до 9.</span><span class="sxs-lookup"><span data-stu-id="51887-155">The value must be an integer between 0 and 9.</span></span> |
| <span data-ttu-id="51887-156">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="51887-156">**Note**</span></span><br><span data-ttu-id="51887-157">mshr_note</span><span class="sxs-lookup"><span data-stu-id="51887-157">mshr_note</span></span><br><span data-ttu-id="51887-158">*Строка*</span><span class="sxs-lookup"><span data-stu-id="51887-158">*String*</span></span> | <span data-ttu-id="51887-159">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="51887-159">Read/write</span></span><br><span data-ttu-id="51887-160">Необязательный</span><span class="sxs-lookup"><span data-stu-id="51887-160">Optional</span></span> | <span data-ttu-id="51887-161">Любые замечания, связанные с уровнем рейтинга.</span><span class="sxs-lookup"><span data-stu-id="51887-161">Any notes associated with the rating level.</span></span> |
| <span data-ttu-id="51887-162">**Основное поле**</span><span class="sxs-lookup"><span data-stu-id="51887-162">**Primary Field**</span></span><br><span data-ttu-id="51887-163">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="51887-163">mshr_primaryfield</span></span><br><span data-ttu-id="51887-164">*Строка*</span><span class="sxs-lookup"><span data-stu-id="51887-164">*String*</span></span> | <span data-ttu-id="51887-165">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="51887-165">Read-only</span></span><br><span data-ttu-id="51887-166">Требуется</span><span class="sxs-lookup"><span data-stu-id="51887-166">Required</span></span> | <span data-ttu-id="51887-167">Поле для, использования в качестве идентификатора записи сущности.</span><span class="sxs-lookup"><span data-stu-id="51887-167">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="51887-168">Комбинация кода уровня рейтинга и кода модели рейтинга.</span><span class="sxs-lookup"><span data-stu-id="51887-168">Combination of rating level ID and rating model ID.</span></span> |

## <a name="see-also"></a><span data-ttu-id="51887-169">См. также</span><span class="sxs-lookup"><span data-stu-id="51887-169">See also</span></span>

[<span data-ttu-id="51887-170">Введение в интерфейс API интеграции системы отслеживания кандидатов</span><span class="sxs-lookup"><span data-stu-id="51887-170">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="51887-171">Пример запроса кандидата для приема на работу</span><span class="sxs-lookup"><span data-stu-id="51887-171">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]