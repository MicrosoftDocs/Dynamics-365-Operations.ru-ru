---
title: Статус выполнения
description: В этом разделе описывается набор параметров статуса выполнения для Dynamics 365 Human Resources.
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
ms.openlocfilehash: f1b0c61ac9d9dc611d2a4700a1a004e3d15b4445
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798377"
---
# <a name="completion-status"></a><span data-ttu-id="bdcb4-103">Статус выполнения</span><span class="sxs-lookup"><span data-stu-id="bdcb4-103">Completion status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="bdcb4-104">В этом разделе описывается набор параметров статуса выполнения для Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="bdcb4-104">This topic describes the Completion status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="bdcb4-105">Физическое имя: mshr_hcmcompletionstatus</span><span class="sxs-lookup"><span data-stu-id="bdcb4-105">Physical name: mshr_hcmcompletionstatus</span></span>

<span data-ttu-id="bdcb4-106">Это перечисление предоставляет набор параметров значений статуса для отбора (осмотра) кандидатов.</span><span class="sxs-lookup"><span data-stu-id="bdcb4-106">This enumeration provides the option set of status values for candidate screenings.</span></span> 

| <span data-ttu-id="bdcb4-107">значение</span><span class="sxs-lookup"><span data-stu-id="bdcb4-107">Value</span></span> | <span data-ttu-id="bdcb4-108">Этикетка</span><span class="sxs-lookup"><span data-stu-id="bdcb4-108">Label</span></span> | <span data-ttu-id="bdcb4-109">описание</span><span class="sxs-lookup"><span data-stu-id="bdcb4-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="bdcb4-110">200000000</span><span class="sxs-lookup"><span data-stu-id="bdcb4-110">200000000</span></span> | <span data-ttu-id="bdcb4-111">Не завершено</span><span class="sxs-lookup"><span data-stu-id="bdcb4-111">Not Complete</span></span> | <span data-ttu-id="bdcb4-112">Этот кандидат еще не проходил отбор.</span><span class="sxs-lookup"><span data-stu-id="bdcb4-112">The candidate has not yet completed the screening.</span></span> |
| <span data-ttu-id="bdcb4-113">200000001</span><span class="sxs-lookup"><span data-stu-id="bdcb4-113">200000001</span></span> | <span data-ttu-id="bdcb4-114">Пропустить</span><span class="sxs-lookup"><span data-stu-id="bdcb4-114">Pass</span></span> | <span data-ttu-id="bdcb4-115">Кандидат прошел отбор.</span><span class="sxs-lookup"><span data-stu-id="bdcb4-115">The candidate has passed the screening.</span></span> |
| <span data-ttu-id="bdcb4-116">200000002</span><span class="sxs-lookup"><span data-stu-id="bdcb4-116">200000002</span></span> | <span data-ttu-id="bdcb4-117">Сбой</span><span class="sxs-lookup"><span data-stu-id="bdcb4-117">Fail</span></span> | <span data-ttu-id="bdcb4-118">Кандидат не смог пройти отбор.</span><span class="sxs-lookup"><span data-stu-id="bdcb4-118">The candidate has failed the screening.</span></span> |

## <a name="see-also"></a><span data-ttu-id="bdcb4-119">См. также</span><span class="sxs-lookup"><span data-stu-id="bdcb4-119">See also</span></span>

[<span data-ttu-id="bdcb4-120">Введение в интерфейс API интеграции системы отслеживания кандидатов</span><span class="sxs-lookup"><span data-stu-id="bdcb4-120">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="bdcb4-121">Пример запроса кандидата для приема на работу</span><span class="sxs-lookup"><span data-stu-id="bdcb4-121">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]