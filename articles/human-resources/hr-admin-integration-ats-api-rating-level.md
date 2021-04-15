---
title: Уровень рейтинга
description: В этом разделе описывается сущность уровня рейтинга для Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: eac80599de07a045aa233f1cdfd16fe0db8733a2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800341"
---
# <a name="rating-level"></a><span data-ttu-id="2a098-103">Уровень рейтинга</span><span class="sxs-lookup"><span data-stu-id="2a098-103">Rating level</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="2a098-104">В этом разделе описывается сущность уровня рейтинга для Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2a098-104">This topic describes the Rating level entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="2a098-105">Физическое имя: mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="2a098-105">Physical name: mshr_hcmratinglevelentity</span></span>

## <a name="description"></a><span data-ttu-id="2a098-106">описание</span><span class="sxs-lookup"><span data-stu-id="2a098-106">Description</span></span>

<span data-ttu-id="2a098-107">Эта сущность предоставляет доступные уровни рейтинга для навыков.</span><span class="sxs-lookup"><span data-stu-id="2a098-107">This entity provides the available rating levels for skills.</span></span> <span data-ttu-id="2a098-108">Уровни рейтинга применяются для всех юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="2a098-108">Rating levels apply across all legal entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="2a098-109">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="2a098-109">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="2a098-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="2a098-110">Properties</span></span>

| <span data-ttu-id="2a098-111">Свойство</span><span class="sxs-lookup"><span data-stu-id="2a098-111">Property</span></span><br><span data-ttu-id="2a098-112">**Физическое имя**</span><span class="sxs-lookup"><span data-stu-id="2a098-112">**Physical name**</span></span><br><span data-ttu-id="2a098-113">**_Вид_**</span><span class="sxs-lookup"><span data-stu-id="2a098-113">**_Type_**</span></span> | <span data-ttu-id="2a098-114">Использование</span><span class="sxs-lookup"><span data-stu-id="2a098-114">Use</span></span> | <span data-ttu-id="2a098-115">описание</span><span class="sxs-lookup"><span data-stu-id="2a098-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="2a098-116">**ИД сущности уровня рейтинга**</span><span class="sxs-lookup"><span data-stu-id="2a098-116">**Rating Level Entity ID**</span></span><br><span data-ttu-id="2a098-117">mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="2a098-117">mshr_hcmratinglevelentityid</span></span><br><span data-ttu-id="2a098-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="2a098-118">*GUID*</span></span> | <span data-ttu-id="2a098-119">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a098-119">Read-only</span></span><br><span data-ttu-id="2a098-120">Требуется</span><span class="sxs-lookup"><span data-stu-id="2a098-120">Required</span></span><br><span data-ttu-id="2a098-121">Создано системой</span><span class="sxs-lookup"><span data-stu-id="2a098-121">System-generated</span></span> | <span data-ttu-id="2a098-122">Созданный системой уникальный идентификатор для уровня.</span><span class="sxs-lookup"><span data-stu-id="2a098-122">The system-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="2a098-123">**Код уровня оценки**</span><span class="sxs-lookup"><span data-stu-id="2a098-123">**Rating Level ID**</span></span><br><span data-ttu-id="2a098-124">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="2a098-124">mshr_ratinglevelid</span></span><br><span data-ttu-id="2a098-125">*Строка*</span><span class="sxs-lookup"><span data-stu-id="2a098-125">*String*</span></span> | <span data-ttu-id="2a098-126">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="2a098-126">Read/write</span></span><br><span data-ttu-id="2a098-127">Требуется</span><span class="sxs-lookup"><span data-stu-id="2a098-127">Required</span></span> | <span data-ttu-id="2a098-128">Понятный пользователю уникальный идентификатор для уровня.</span><span class="sxs-lookup"><span data-stu-id="2a098-128">User-readable unique identifier for the level.</span></span> |
| <span data-ttu-id="2a098-129">**ИД модели рейтинга**</span><span class="sxs-lookup"><span data-stu-id="2a098-129">**Rating Model ID**</span></span><br><span data-ttu-id="2a098-130">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="2a098-130">mshr_ratingmodelid</span></span><br><span data-ttu-id="2a098-131">*Строка*</span><span class="sxs-lookup"><span data-stu-id="2a098-131">*String*</span></span> | <span data-ttu-id="2a098-132">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="2a098-132">Read/write</span></span><br><span data-ttu-id="2a098-133">Требуется</span><span class="sxs-lookup"><span data-stu-id="2a098-133">Required</span></span> | <span data-ttu-id="2a098-134">Модель рейтинга, к которой принадлежит уровень рейтинга.</span><span class="sxs-lookup"><span data-stu-id="2a098-134">The rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="2a098-135">**ИД сущности модели рейтинга**</span><span class="sxs-lookup"><span data-stu-id="2a098-135">**Rating Model Entity ID**</span></span><br><span data-ttu-id="2a098-136">_mshr_fk_ratingmodelentity_id_value</span><span class="sxs-lookup"><span data-stu-id="2a098-136">_mshr_fk_ratingmodelentity_id_value</span></span><br><span data-ttu-id="2a098-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="2a098-137">*GUID*</span></span> | <span data-ttu-id="2a098-138">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a098-138">Read-only</span></span><br><span data-ttu-id="2a098-139">Требуется</span><span class="sxs-lookup"><span data-stu-id="2a098-139">Required</span></span><br><span data-ttu-id="2a098-140">Внешний ключ: mshr_hcmratingmodelentityid сущности mshr_hcmratingmodelentity</span><span class="sxs-lookup"><span data-stu-id="2a098-140">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span></span> | <span data-ttu-id="2a098-141">Созданный системой идентификатор модели рейтинга, к которой принадлежит уровень рейтинга.</span><span class="sxs-lookup"><span data-stu-id="2a098-141">The system-generated identifier for the rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="2a098-142">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2a098-142">**Description**</span></span><br><span data-ttu-id="2a098-143">mshr_description</span><span class="sxs-lookup"><span data-stu-id="2a098-143">mshr_description</span></span><br><span data-ttu-id="2a098-144">*Строка*</span><span class="sxs-lookup"><span data-stu-id="2a098-144">*String*</span></span> | <span data-ttu-id="2a098-145">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="2a098-145">Read/write</span></span><br><span data-ttu-id="2a098-146">Требуется</span><span class="sxs-lookup"><span data-stu-id="2a098-146">Required</span></span> | <span data-ttu-id="2a098-147">Описание выбранного уровня рейтинга.</span><span class="sxs-lookup"><span data-stu-id="2a098-147">The description of the rating level.</span></span> |
| <span data-ttu-id="2a098-148">**Множитель**</span><span class="sxs-lookup"><span data-stu-id="2a098-148">**Factor**</span></span><br><span data-ttu-id="2a098-149">mshr_factor</span><span class="sxs-lookup"><span data-stu-id="2a098-149">mshr_factor</span></span><br><span data-ttu-id="2a098-150">*Целое число*</span><span class="sxs-lookup"><span data-stu-id="2a098-150">*Integer*</span></span> | <span data-ttu-id="2a098-151">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="2a098-151">Read/write</span></span><br><span data-ttu-id="2a098-152">Требуется</span><span class="sxs-lookup"><span data-stu-id="2a098-152">Required</span></span> | <span data-ttu-id="2a098-153">Коэффициент для уровня рейтинга.</span><span class="sxs-lookup"><span data-stu-id="2a098-153">The factor for the rating level.</span></span> <span data-ttu-id="2a098-154">Если сравнить номенклатуры с разным числом уровней рейтинга, этот коэффициент используется для нормализации оценок.</span><span class="sxs-lookup"><span data-stu-id="2a098-154">When you compare items with a different number of rating levels, the factor is used to normalize the scores.</span></span> <span data-ttu-id="2a098-155">Значение должно быть целым числом от 0 до 9.</span><span class="sxs-lookup"><span data-stu-id="2a098-155">The value must be an integer between 0 and 9.</span></span> |
| <span data-ttu-id="2a098-156">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="2a098-156">**Note**</span></span><br><span data-ttu-id="2a098-157">mshr_note</span><span class="sxs-lookup"><span data-stu-id="2a098-157">mshr_note</span></span><br><span data-ttu-id="2a098-158">*Строка*</span><span class="sxs-lookup"><span data-stu-id="2a098-158">*String*</span></span> | <span data-ttu-id="2a098-159">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="2a098-159">Read/write</span></span><br><span data-ttu-id="2a098-160">Необязательный</span><span class="sxs-lookup"><span data-stu-id="2a098-160">Optional</span></span> | <span data-ttu-id="2a098-161">Любые замечания, связанные с уровнем рейтинга.</span><span class="sxs-lookup"><span data-stu-id="2a098-161">Any notes associated with the rating level.</span></span> |
| <span data-ttu-id="2a098-162">**Основное поле**</span><span class="sxs-lookup"><span data-stu-id="2a098-162">**Primary Field**</span></span><br><span data-ttu-id="2a098-163">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="2a098-163">mshr_primaryfield</span></span><br><span data-ttu-id="2a098-164">*Строка*</span><span class="sxs-lookup"><span data-stu-id="2a098-164">*String*</span></span> | <span data-ttu-id="2a098-165">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="2a098-165">Read-only</span></span><br><span data-ttu-id="2a098-166">Требуется</span><span class="sxs-lookup"><span data-stu-id="2a098-166">Required</span></span> | <span data-ttu-id="2a098-167">Поле для, использования в качестве идентификатора записи сущности.</span><span class="sxs-lookup"><span data-stu-id="2a098-167">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="2a098-168">Комбинация кода уровня рейтинга и кода модели рейтинга.</span><span class="sxs-lookup"><span data-stu-id="2a098-168">Combination of rating level ID and rating model ID.</span></span> |

## <a name="see-also"></a><span data-ttu-id="2a098-169">См. также</span><span class="sxs-lookup"><span data-stu-id="2a098-169">See also</span></span>

[<span data-ttu-id="2a098-170">Введение в интерфейс API интеграции системы отслеживания кандидатов</span><span class="sxs-lookup"><span data-stu-id="2a098-170">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="2a098-171">Пример запроса кандидата для приема на работу</span><span class="sxs-lookup"><span data-stu-id="2a098-171">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]