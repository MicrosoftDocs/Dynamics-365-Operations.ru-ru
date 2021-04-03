---
title: Состояние освобождения должности от доплат за сверхурочное время
description: В этом разделе описывается набор параметров состояния освобождения должности от доплат за сверхурочное время для Dynamics 365 Human Resources.
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
ms.openlocfilehash: 1f211002468384227acb2343ed6cbc6ae2a215d1
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464460"
---
# <a name="job-exempt-status"></a><span data-ttu-id="f901b-103">Состояние освобождения должности от доплат за сверхурочное время</span><span class="sxs-lookup"><span data-stu-id="f901b-103">Job exempt status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f901b-104">В этом разделе описывается набор параметров состояния освобождения должности от доплат за сверхурочное время для Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f901b-104">This topic describes the Job exempt status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="f901b-105">Физическое имя: cdm_jobexemptstatus</span><span class="sxs-lookup"><span data-stu-id="f901b-105">Physical name: cdm_jobexemptstatus</span></span>

<span data-ttu-id="f901b-106">Это перечисление указывает набор параметров для значений состояния освобождения должности от доплат за сверхурочное время в соответствии с FLSA.</span><span class="sxs-lookup"><span data-stu-id="f901b-106">This enumeration specifies the option set for FLSA job exempt status values.</span></span> <span data-ttu-id="f901b-107">Это предусмотрено в существующем наборе параметров cdm_jobexemptstatus.</span><span class="sxs-lookup"><span data-stu-id="f901b-107">This is provided in the existing cdm_jobexemptstatus option set.</span></span>

| <span data-ttu-id="f901b-108">значение</span><span class="sxs-lookup"><span data-stu-id="f901b-108">Value</span></span> | <span data-ttu-id="f901b-109">Этикетка</span><span class="sxs-lookup"><span data-stu-id="f901b-109">Label</span></span> | <span data-ttu-id="f901b-110">описание</span><span class="sxs-lookup"><span data-stu-id="f901b-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="f901b-111">200000000</span><span class="sxs-lookup"><span data-stu-id="f901b-111">200000000</span></span> | <span data-ttu-id="f901b-112">Освобождается</span><span class="sxs-lookup"><span data-stu-id="f901b-112">Exempt</span></span> | <span data-ttu-id="f901b-113">Должность имеет статус освобожденной от доплат за сверхурочное время в соответствии с рекомендациями FLSA.</span><span class="sxs-lookup"><span data-stu-id="f901b-113">The job has an exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="f901b-114">200000001</span><span class="sxs-lookup"><span data-stu-id="f901b-114">200000001</span></span> | <span data-ttu-id="f901b-115">NonExempt</span><span class="sxs-lookup"><span data-stu-id="f901b-115">NonExempt</span></span> | <span data-ttu-id="f901b-116">Должность имеет статус не освобожденной от доплат за сверхурочное время в соответствии с рекомендациями FLSA.</span><span class="sxs-lookup"><span data-stu-id="f901b-116">The job has a non-exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="f901b-117">200000002</span><span class="sxs-lookup"><span data-stu-id="f901b-117">200000002</span></span> | <span data-ttu-id="f901b-118">Не применяется</span><span class="sxs-lookup"><span data-stu-id="f901b-118">Does Not Apply</span></span> | <span data-ttu-id="f901b-119">Рекомендации по статусу FLSA не относятся к этой должности.</span><span class="sxs-lookup"><span data-stu-id="f901b-119">FLSA status guidelines do not apply to the job.</span></span> |

## <a name="see-also"></a><span data-ttu-id="f901b-120">См. также</span><span class="sxs-lookup"><span data-stu-id="f901b-120">See also</span></span>

[<span data-ttu-id="f901b-121">Введение в интерфейс API интеграции системы отслеживания кандидатов</span><span class="sxs-lookup"><span data-stu-id="f901b-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="f901b-122">Пример запроса для запроса на набор персонала</span><span class="sxs-lookup"><span data-stu-id="f901b-122">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]