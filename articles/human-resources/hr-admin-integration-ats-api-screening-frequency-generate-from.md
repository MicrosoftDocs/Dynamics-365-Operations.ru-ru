---
title: Начальная дата создаваемой периодичности отбора
description: В этом разделе описывается набор параметров начальной даты создаваемой частоты отбора для Dynamics 365 Human Resources.
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
ms.openlocfilehash: bee0522ea244cab2f5d6864b2a763df6e314e02d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805162"
---
# <a name="screening-frequency-generate-from"></a><span data-ttu-id="cd181-103">Начальная дата создаваемой периодичности отбора</span><span class="sxs-lookup"><span data-stu-id="cd181-103">Screening frequency generate from</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="cd181-104">В этом разделе описывается набор параметров начальной даты создаваемой частоты отбора для Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="cd181-104">This topic describes the Screening frequency generate from option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="cd181-105">Физическое имя: mshr_hcmfrequencygeneratefrom</span><span class="sxs-lookup"><span data-stu-id="cd181-105">Physical name: mshr_hcmfrequencygeneratefrom</span></span>

<span data-ttu-id="cd181-106">Это перечисление предоставляет набор параметров со значениями, определяющими начальную дату вычисления для следующего необходимого отбора.</span><span class="sxs-lookup"><span data-stu-id="cd181-106">This enumeration provides the option set of values for determining the start date of the calculation for the next required screening.</span></span>

| <span data-ttu-id="cd181-107">значение</span><span class="sxs-lookup"><span data-stu-id="cd181-107">Value</span></span> | <span data-ttu-id="cd181-108">Этикетка</span><span class="sxs-lookup"><span data-stu-id="cd181-108">Label</span></span> | <span data-ttu-id="cd181-109">описание</span><span class="sxs-lookup"><span data-stu-id="cd181-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="cd181-110">200000000 Не выбрано</span><span class="sxs-lookup"><span data-stu-id="cd181-110">200000000 Not selected</span></span> | <span data-ttu-id="cd181-111">Значение не было выбрано.</span><span class="sxs-lookup"><span data-stu-id="cd181-111">No value has been selected.</span></span> |
| <span data-ttu-id="cd181-112">200000001 Дата завершения</span><span class="sxs-lookup"><span data-stu-id="cd181-112">200000001 Date completed</span></span> | <span data-ttu-id="cd181-113">Расчет выполняется по последней дате выполнения отбора.</span><span class="sxs-lookup"><span data-stu-id="cd181-113">Calculation is done from the last screening date completed.</span></span> |
| <span data-ttu-id="cd181-114">200000002 Требуемая дата</span><span class="sxs-lookup"><span data-stu-id="cd181-114">200000002 Date required</span></span> | <span data-ttu-id="cd181-115">Расчет выполняется по последней требуемой дате отбора.</span><span class="sxs-lookup"><span data-stu-id="cd181-115">Calculation is done from the last screening date required.</span></span> |

## <a name="see-also"></a><span data-ttu-id="cd181-116">См. также</span><span class="sxs-lookup"><span data-stu-id="cd181-116">See also</span></span>

[<span data-ttu-id="cd181-117">Введение в интерфейс API интеграции системы отслеживания кандидатов</span><span class="sxs-lookup"><span data-stu-id="cd181-117">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="cd181-118">Пример запроса кандидата для приема на работу</span><span class="sxs-lookup"><span data-stu-id="cd181-118">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]