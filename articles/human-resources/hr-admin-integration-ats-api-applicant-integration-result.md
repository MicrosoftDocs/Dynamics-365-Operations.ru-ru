---
title: Результат интеграции кандидата
description: В этом разделе описывается набор параметров результата интеграции заявителя для Dynamics 365 Human Resources.
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
ms.openlocfilehash: 157864cd0eee879013724615ce31306c99c5aa68
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125817"
---
# <a name="applicant-integration-result"></a><span data-ttu-id="c077c-103">Результат интеграции кандидата</span><span class="sxs-lookup"><span data-stu-id="c077c-103">Applicant integration result</span></span>

<span data-ttu-id="c077c-104">В этом разделе описывается набор параметров результата интеграции заявителя для Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c077c-104">This topic describes the Applicant integration result option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="c077c-105">Физическое имя: mshr_hcmapplicantintegrationresult</span><span class="sxs-lookup"><span data-stu-id="c077c-105">Physical name: mshr_hcmapplicantintegrationresult</span></span>

<span data-ttu-id="c077c-106">Это перечисление предоставляет статус для записи кандидата.</span><span class="sxs-lookup"><span data-stu-id="c077c-106">This enumeration provides status for a candidate record.</span></span>

| <span data-ttu-id="c077c-107">значение</span><span class="sxs-lookup"><span data-stu-id="c077c-107">Value</span></span> | <span data-ttu-id="c077c-108">Этикетка</span><span class="sxs-lookup"><span data-stu-id="c077c-108">Label</span></span> | <span data-ttu-id="c077c-109">описание</span><span class="sxs-lookup"><span data-stu-id="c077c-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="c077c-110">200000000</span><span class="sxs-lookup"><span data-stu-id="c077c-110">200000000</span></span> | <span data-ttu-id="c077c-111">Не обработано</span><span class="sxs-lookup"><span data-stu-id="c077c-111">Not processed</span></span> | <span data-ttu-id="c077c-112">Кандидат все еще находится в процессе рассмотрения.</span><span class="sxs-lookup"><span data-stu-id="c077c-112">Candidate is still under consideration.</span></span> |
| <span data-ttu-id="c077c-113">200000001</span><span class="sxs-lookup"><span data-stu-id="c077c-113">200000001</span></span> | <span data-ttu-id="c077c-114">Принят</span><span class="sxs-lookup"><span data-stu-id="c077c-114">Hired</span></span> | <span data-ttu-id="c077c-115">Кандидат был принят на работу.</span><span class="sxs-lookup"><span data-stu-id="c077c-115">The candidate has been hired.</span></span> |
| <span data-ttu-id="c077c-116">200000002</span><span class="sxs-lookup"><span data-stu-id="c077c-116">200000002</span></span> | <span data-ttu-id="c077c-117">Не принят на работу</span><span class="sxs-lookup"><span data-stu-id="c077c-117">Not hired</span></span> | <span data-ttu-id="c077c-118">Принято решение не нанимать кандидата.</span><span class="sxs-lookup"><span data-stu-id="c077c-118">Decision was made to not hire the candidate.</span></span> |
| <span data-ttu-id="c077c-119">200000003</span><span class="sxs-lookup"><span data-stu-id="c077c-119">200000003</span></span> | <span data-ttu-id="c077c-120">Отменено</span><span class="sxs-lookup"><span data-stu-id="c077c-120">Dismissed</span></span> | <span data-ttu-id="c077c-121">Кандидат был исключен из рассмотрения.</span><span class="sxs-lookup"><span data-stu-id="c077c-121">The candidate was dismissed from consideration.</span></span> |

## <a name="see-also"></a><span data-ttu-id="c077c-122">См. также</span><span class="sxs-lookup"><span data-stu-id="c077c-122">See also</span></span>

[<span data-ttu-id="c077c-123">Введение в интерфейс API интеграции системы отслеживания кандидатов</span><span class="sxs-lookup"><span data-stu-id="c077c-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="c077c-124">Пример запроса кандидата для приема на работу</span><span class="sxs-lookup"><span data-stu-id="c077c-124">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
