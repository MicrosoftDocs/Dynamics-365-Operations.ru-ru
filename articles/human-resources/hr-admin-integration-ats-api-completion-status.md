---
title: Статус выполнения
description: В этом разделе описывается набор параметров статуса выполнения для Dynamics 365 Human Resources.
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
ms.openlocfilehash: d8ea90785f303301a21a4ac799578b08cabd0e3d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468211"
---
# <a name="completion-status"></a><span data-ttu-id="dd421-103">Статус выполнения</span><span class="sxs-lookup"><span data-stu-id="dd421-103">Completion status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="dd421-104">В этом разделе описывается набор параметров статуса выполнения для Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="dd421-104">This topic describes the Completion status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="dd421-105">Физическое имя: mshr_hcmcompletionstatus</span><span class="sxs-lookup"><span data-stu-id="dd421-105">Physical name: mshr_hcmcompletionstatus</span></span>

<span data-ttu-id="dd421-106">Это перечисление предоставляет набор параметров значений статуса для отбора (осмотра) кандидатов.</span><span class="sxs-lookup"><span data-stu-id="dd421-106">This enumeration provides the option set of status values for candidate screenings.</span></span> 

| <span data-ttu-id="dd421-107">значение</span><span class="sxs-lookup"><span data-stu-id="dd421-107">Value</span></span> | <span data-ttu-id="dd421-108">Этикетка</span><span class="sxs-lookup"><span data-stu-id="dd421-108">Label</span></span> | <span data-ttu-id="dd421-109">описание</span><span class="sxs-lookup"><span data-stu-id="dd421-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="dd421-110">200000000</span><span class="sxs-lookup"><span data-stu-id="dd421-110">200000000</span></span> | <span data-ttu-id="dd421-111">Не завершено</span><span class="sxs-lookup"><span data-stu-id="dd421-111">Not Complete</span></span> | <span data-ttu-id="dd421-112">Этот кандидат еще не проходил отбор.</span><span class="sxs-lookup"><span data-stu-id="dd421-112">The candidate has not yet completed the screening.</span></span> |
| <span data-ttu-id="dd421-113">200000001</span><span class="sxs-lookup"><span data-stu-id="dd421-113">200000001</span></span> | <span data-ttu-id="dd421-114">Пропустить</span><span class="sxs-lookup"><span data-stu-id="dd421-114">Pass</span></span> | <span data-ttu-id="dd421-115">Кандидат прошел отбор.</span><span class="sxs-lookup"><span data-stu-id="dd421-115">The candidate has passed the screening.</span></span> |
| <span data-ttu-id="dd421-116">200000002</span><span class="sxs-lookup"><span data-stu-id="dd421-116">200000002</span></span> | <span data-ttu-id="dd421-117">Сбой</span><span class="sxs-lookup"><span data-stu-id="dd421-117">Fail</span></span> | <span data-ttu-id="dd421-118">Кандидат не смог пройти отбор.</span><span class="sxs-lookup"><span data-stu-id="dd421-118">The candidate has failed the screening.</span></span> |

## <a name="see-also"></a><span data-ttu-id="dd421-119">См. также</span><span class="sxs-lookup"><span data-stu-id="dd421-119">See also</span></span>

[<span data-ttu-id="dd421-120">Введение в интерфейс API интеграции системы отслеживания кандидатов</span><span class="sxs-lookup"><span data-stu-id="dd421-120">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="dd421-121">Пример запроса кандидата для приема на работу</span><span class="sxs-lookup"><span data-stu-id="dd421-121">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]