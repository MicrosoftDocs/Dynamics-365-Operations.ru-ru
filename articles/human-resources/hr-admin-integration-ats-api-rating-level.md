---
title: Уровень рейтинга
description: В этом разделе описывается сущность уровня рейтинга для Dynamics 365 Human Resources.
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
ms.openlocfilehash: 8bbd10bcc47a928070da7cd82e6d996f71c65698
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054844"
---
# <a name="rating-level"></a><span data-ttu-id="9dc30-103">Уровень рейтинга</span><span class="sxs-lookup"><span data-stu-id="9dc30-103">Rating level</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9dc30-104">В этом разделе описывается сущность уровня рейтинга для Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9dc30-104">This topic describes the Rating level entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="9dc30-105">Физическое имя: mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="9dc30-105">Physical name: mshr_hcmratinglevelentity</span></span>

## <a name="description"></a><span data-ttu-id="9dc30-106">описание</span><span class="sxs-lookup"><span data-stu-id="9dc30-106">Description</span></span>

<span data-ttu-id="9dc30-107">Эта сущность предоставляет доступные уровни рейтинга для навыков.</span><span class="sxs-lookup"><span data-stu-id="9dc30-107">This entity provides the available rating levels for skills.</span></span> <span data-ttu-id="9dc30-108">Уровни рейтинга применяются для всех юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="9dc30-108">Rating levels apply across all legal entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="9dc30-109">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="9dc30-109">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="9dc30-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="9dc30-110">Properties</span></span>

| <span data-ttu-id="9dc30-111">Свойство</span><span class="sxs-lookup"><span data-stu-id="9dc30-111">Property</span></span><br><span data-ttu-id="9dc30-112">**Физическое имя**</span><span class="sxs-lookup"><span data-stu-id="9dc30-112">**Physical name**</span></span><br><span data-ttu-id="9dc30-113">**_Вид_**</span><span class="sxs-lookup"><span data-stu-id="9dc30-113">**_Type_**</span></span> | <span data-ttu-id="9dc30-114">Использование</span><span class="sxs-lookup"><span data-stu-id="9dc30-114">Use</span></span> | <span data-ttu-id="9dc30-115">описание</span><span class="sxs-lookup"><span data-stu-id="9dc30-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="9dc30-116">**ИД сущности уровня рейтинга**</span><span class="sxs-lookup"><span data-stu-id="9dc30-116">**Rating Level Entity ID**</span></span><br><span data-ttu-id="9dc30-117">mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="9dc30-117">mshr_hcmratinglevelentityid</span></span><br><span data-ttu-id="9dc30-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="9dc30-118">*GUID*</span></span> | <span data-ttu-id="9dc30-119">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="9dc30-119">Read-only</span></span><br><span data-ttu-id="9dc30-120">Требуется</span><span class="sxs-lookup"><span data-stu-id="9dc30-120">Required</span></span><br><span data-ttu-id="9dc30-121">Создано системой</span><span class="sxs-lookup"><span data-stu-id="9dc30-121">System-generated</span></span> | <span data-ttu-id="9dc30-122">Созданный системой уникальный идентификатор для уровня.</span><span class="sxs-lookup"><span data-stu-id="9dc30-122">The system-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="9dc30-123">**Код уровня оценки**</span><span class="sxs-lookup"><span data-stu-id="9dc30-123">**Rating Level ID**</span></span><br><span data-ttu-id="9dc30-124">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="9dc30-124">mshr_ratinglevelid</span></span><br><span data-ttu-id="9dc30-125">*Строка*</span><span class="sxs-lookup"><span data-stu-id="9dc30-125">*String*</span></span> | <span data-ttu-id="9dc30-126">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="9dc30-126">Read/write</span></span><br><span data-ttu-id="9dc30-127">Требуется</span><span class="sxs-lookup"><span data-stu-id="9dc30-127">Required</span></span> | <span data-ttu-id="9dc30-128">Понятный пользователю уникальный идентификатор для уровня.</span><span class="sxs-lookup"><span data-stu-id="9dc30-128">User-readable unique identifier for the level.</span></span> |
| <span data-ttu-id="9dc30-129">**ИД модели рейтинга**</span><span class="sxs-lookup"><span data-stu-id="9dc30-129">**Rating Model ID**</span></span><br><span data-ttu-id="9dc30-130">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="9dc30-130">mshr_ratingmodelid</span></span><br><span data-ttu-id="9dc30-131">*Строка*</span><span class="sxs-lookup"><span data-stu-id="9dc30-131">*String*</span></span> | <span data-ttu-id="9dc30-132">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="9dc30-132">Read/write</span></span><br><span data-ttu-id="9dc30-133">Требуется</span><span class="sxs-lookup"><span data-stu-id="9dc30-133">Required</span></span> | <span data-ttu-id="9dc30-134">Модель рейтинга, к которой принадлежит уровень рейтинга.</span><span class="sxs-lookup"><span data-stu-id="9dc30-134">The rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="9dc30-135">**ИД сущности модели рейтинга**</span><span class="sxs-lookup"><span data-stu-id="9dc30-135">**Rating Model Entity ID**</span></span><br><span data-ttu-id="9dc30-136">_mshr_fk_ratingmodelentity_id_value</span><span class="sxs-lookup"><span data-stu-id="9dc30-136">_mshr_fk_ratingmodelentity_id_value</span></span><br><span data-ttu-id="9dc30-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="9dc30-137">*GUID*</span></span> | <span data-ttu-id="9dc30-138">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="9dc30-138">Read-only</span></span><br><span data-ttu-id="9dc30-139">Требуется</span><span class="sxs-lookup"><span data-stu-id="9dc30-139">Required</span></span><br><span data-ttu-id="9dc30-140">Внешний ключ: mshr_hcmratingmodelentityid сущности mshr_hcmratingmodelentity</span><span class="sxs-lookup"><span data-stu-id="9dc30-140">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span></span> | <span data-ttu-id="9dc30-141">Созданный системой идентификатор модели рейтинга, к которой принадлежит уровень рейтинга.</span><span class="sxs-lookup"><span data-stu-id="9dc30-141">The system-generated identifier for the rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="9dc30-142">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9dc30-142">**Description**</span></span><br><span data-ttu-id="9dc30-143">mshr_description</span><span class="sxs-lookup"><span data-stu-id="9dc30-143">mshr_description</span></span><br><span data-ttu-id="9dc30-144">*Строка*</span><span class="sxs-lookup"><span data-stu-id="9dc30-144">*String*</span></span> | <span data-ttu-id="9dc30-145">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="9dc30-145">Read/write</span></span><br><span data-ttu-id="9dc30-146">Требуется</span><span class="sxs-lookup"><span data-stu-id="9dc30-146">Required</span></span> | <span data-ttu-id="9dc30-147">Описание выбранного уровня рейтинга.</span><span class="sxs-lookup"><span data-stu-id="9dc30-147">The description of the rating level.</span></span> |
| <span data-ttu-id="9dc30-148">**Множитель**</span><span class="sxs-lookup"><span data-stu-id="9dc30-148">**Factor**</span></span><br><span data-ttu-id="9dc30-149">mshr_factor</span><span class="sxs-lookup"><span data-stu-id="9dc30-149">mshr_factor</span></span><br><span data-ttu-id="9dc30-150">*Целое число*</span><span class="sxs-lookup"><span data-stu-id="9dc30-150">*Integer*</span></span> | <span data-ttu-id="9dc30-151">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="9dc30-151">Read/write</span></span><br><span data-ttu-id="9dc30-152">Требуется</span><span class="sxs-lookup"><span data-stu-id="9dc30-152">Required</span></span> | <span data-ttu-id="9dc30-153">Коэффициент для уровня рейтинга.</span><span class="sxs-lookup"><span data-stu-id="9dc30-153">The factor for the rating level.</span></span> <span data-ttu-id="9dc30-154">Если сравнить номенклатуры с разным числом уровней рейтинга, этот коэффициент используется для нормализации оценок.</span><span class="sxs-lookup"><span data-stu-id="9dc30-154">When you compare items with a different number of rating levels, the factor is used to normalize the scores.</span></span> <span data-ttu-id="9dc30-155">Значение должно быть целым числом от 0 до 9.</span><span class="sxs-lookup"><span data-stu-id="9dc30-155">The value must be an integer between 0 and 9.</span></span> |
| <span data-ttu-id="9dc30-156">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="9dc30-156">**Note**</span></span><br><span data-ttu-id="9dc30-157">mshr_note</span><span class="sxs-lookup"><span data-stu-id="9dc30-157">mshr_note</span></span><br><span data-ttu-id="9dc30-158">*Строка*</span><span class="sxs-lookup"><span data-stu-id="9dc30-158">*String*</span></span> | <span data-ttu-id="9dc30-159">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="9dc30-159">Read/write</span></span><br><span data-ttu-id="9dc30-160">Необязательный</span><span class="sxs-lookup"><span data-stu-id="9dc30-160">Optional</span></span> | <span data-ttu-id="9dc30-161">Любые замечания, связанные с уровнем рейтинга.</span><span class="sxs-lookup"><span data-stu-id="9dc30-161">Any notes associated with the rating level.</span></span> |
| <span data-ttu-id="9dc30-162">**Основное поле**</span><span class="sxs-lookup"><span data-stu-id="9dc30-162">**Primary Field**</span></span><br><span data-ttu-id="9dc30-163">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="9dc30-163">mshr_primaryfield</span></span><br><span data-ttu-id="9dc30-164">*Строка*</span><span class="sxs-lookup"><span data-stu-id="9dc30-164">*String*</span></span> | <span data-ttu-id="9dc30-165">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="9dc30-165">Read-only</span></span><br><span data-ttu-id="9dc30-166">Требуется</span><span class="sxs-lookup"><span data-stu-id="9dc30-166">Required</span></span> | <span data-ttu-id="9dc30-167">Поле для, использования в качестве идентификатора записи сущности.</span><span class="sxs-lookup"><span data-stu-id="9dc30-167">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="9dc30-168">Комбинация кода уровня рейтинга и кода модели рейтинга.</span><span class="sxs-lookup"><span data-stu-id="9dc30-168">Combination of rating level ID and rating model ID.</span></span> |

## <a name="see-also"></a><span data-ttu-id="9dc30-169">См. также</span><span class="sxs-lookup"><span data-stu-id="9dc30-169">See also</span></span>

[<span data-ttu-id="9dc30-170">Введение в интерфейс API интеграции системы отслеживания кандидатов</span><span class="sxs-lookup"><span data-stu-id="9dc30-170">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="9dc30-171">Пример запроса кандидата для приема на работу</span><span class="sxs-lookup"><span data-stu-id="9dc30-171">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]