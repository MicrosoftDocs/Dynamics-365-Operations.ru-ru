---
title: Устранение неполадок интеграции с LinkedIn и Microsoft Dynamics 365 Talent - Attract
description: В этой теме объясняется, как устранять неполадки при попытке публикации объявлений о вакансиях в LinkedIn из Microsoft Dynamics 365 Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: ec095642f556b8d0087dd22f35097671a30047a6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462317"
---
# <a name="troubleshoot-integration-with-linkedin-and-attract"></a><span data-ttu-id="2167c-103">Устранение неполадок интеграции с LinkedIn и Attract</span><span class="sxs-lookup"><span data-stu-id="2167c-103">Troubleshoot integration with LinkedIn and Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2167c-104">Следующие сведения помогут в устранении неполадок, которые могут возникнуть при попытке публикации объявлений о вакансиях в LinkedIn из Microsoft Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="2167c-104">Use the following information to help troubleshoot issues that you might have when you try to post jobs to LinkedIn from Microsoft Dynamics 365 Talent: Attract.</span></span>

## <a name="you-cant-sign-in-to-linkedin-from-attract"></a><span data-ttu-id="2167c-105">Нельзя войти в LinkedIn из Attract</span><span class="sxs-lookup"><span data-stu-id="2167c-105">You can't sign in to LinkedIn from Attract</span></span>

<span data-ttu-id="2167c-106">Если вы не можете войти в LinkedIn из Attract, попробуйте следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2167c-106">If you're having trouble signing in to LinkedIn from Attract, try these steps:</span></span>

1. <span data-ttu-id="2167c-107">Убедитесь, что учетные данные LinkedIn, введенные в Attract, действительные и правильные.</span><span class="sxs-lookup"><span data-stu-id="2167c-107">Verify that the LinkedIn credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="2167c-108">Если учетные данные действительные и правильные, обратитесь в [службу поддержки LinkedIn](https://www.linkedin.com/help/linkedin).</span><span class="sxs-lookup"><span data-stu-id="2167c-108">If the credentials are valid and correct, contact [LinkedIn support](https://www.linkedin.com/help/linkedin).</span></span>
3. <span data-ttu-id="2167c-109">Если неполадка не устранена, обратитесь в [службу поддержки Майкрософт](./talent-support.md).</span><span class="sxs-lookup"><span data-stu-id="2167c-109">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>

## <a name="job-posts-from-attract-dont-appear-on-linkedin"></a><span data-ttu-id="2167c-110">Объявления о вакансиях из Attract не отображаются в LinkedIn</span><span class="sxs-lookup"><span data-stu-id="2167c-110">Job posts from Attract don't appear on LinkedIn</span></span>

<span data-ttu-id="2167c-111">Если вакансия не появилось в LinkedIn через 24 часа, попробуйте выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2167c-111">If your job hasn't appeared on LinkedIn after 24 hours, try these steps:</span></span>

1. <span data-ttu-id="2167c-112">Убедитесь, что код LinkedIn вашей компании отображается на странице компании LinkedIn и правильно введен в центре администрирования Attract.</span><span class="sxs-lookup"><span data-stu-id="2167c-112">Make sure that your LinkedIn Company ID maps to your LinkedIn company page and is correctly entered in the Attract Admin center.</span></span> <span data-ttu-id="2167c-113">Дополнительные сведения об изменении настроек LinkedIn в центре администрирования см. в разделе [Настройка интеграции с LinkedIn для Microsoft Dynamics 365 Talent — Attract](attract-admin-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="2167c-113">For more information about how to change LinkedIn settings in the Admin center, see [Set up integration with LinkedIn for Microsoft Dynamics 365 Talent - Attract](attract-admin-linkedin.md).</span></span> <span data-ttu-id="2167c-114">Дополнительные сведения о кодах компании LinkedIn см. в разделе [Назначение кода компании LinkedIn с доской вакансий LinkedIn — часто задаваемые вопросы](https://www.linkedin.com/help/linkedin/answer/98972).</span><span class="sxs-lookup"><span data-stu-id="2167c-114">For more information about LinkedIn Company IDs, see [Associating your LinkedIn Company ID with the LinkedIn Job Board - Frequently Asked Questions](https://www.linkedin.com/help/linkedin/answer/98972).</span></span>
2. <span data-ttu-id="2167c-115">Проверьте сведения о вакансии в LinkedIn, чтобы убедиться в том, что адрес заполнен.</span><span class="sxs-lookup"><span data-stu-id="2167c-115">Check the job details on LinkedIn to make sure that the address is complete.</span></span> <span data-ttu-id="2167c-116">Для успешной публикации объявления о вакансии в LinkedIn требуется, по крайней мере, город и страна или регион вакансии.</span><span class="sxs-lookup"><span data-stu-id="2167c-116">To post a job successfully, LinkedIn needs at least the city and country or region of the job.</span></span>
3. <span data-ttu-id="2167c-117">Убедитесь, что вакансия не дублирует другую вакансию, которая была опубликована в LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="2167c-117">Make sure that the job doesn't duplicate another job that has been posted on LinkedIn.</span></span> <span data-ttu-id="2167c-118">LinkedIn не публикует вакансии, которые являются дубликатами премиальных рекламных мест вакансий или ограниченных списков LinkedIn из другого источника.</span><span class="sxs-lookup"><span data-stu-id="2167c-118">LinkedIn won't post jobs that are duplicates of either LinkedIn Premium Job Slots or Limited Listings from another source.</span></span> <span data-ttu-id="2167c-119">Убедитесь, что другой сотрудник компании не опубликовал эту вакансию вручную.</span><span class="sxs-lookup"><span data-stu-id="2167c-119">Verify that another person at your company didn't already post the job manually.</span></span>

## <a name="see-also"></a><span data-ttu-id="2167c-120">См. также</span><span class="sxs-lookup"><span data-stu-id="2167c-120">See also</span></span>

[<span data-ttu-id="2167c-121">Вопросы и ответы по интеграции Attract с LinkedIn</span><span class="sxs-lookup"><span data-stu-id="2167c-121">Attract integration with LinkedIn FAQ</span></span>](./attract-linkedin-faq.md)

[<span data-ttu-id="2167c-122">Публикация вакансий в LinkedIn из Microsoft Dynamics 365 Talent — Attract</span><span class="sxs-lookup"><span data-stu-id="2167c-122">Post jobs to LinkedIn from Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-post-jobs-to-linkedin.md)

[<span data-ttu-id="2167c-123">Поиск кандидатов с помощью LinkedIn Recruiter в Microsoft Dynamics 365 Talent — Attract</span><span class="sxs-lookup"><span data-stu-id="2167c-123">Source candidates with LinkedIn Recruiter in Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-linkedin-recruiter.md)

[<span data-ttu-id="2167c-124">Создание, утверждение и публикация вакансий в Attract</span><span class="sxs-lookup"><span data-stu-id="2167c-124">Create, approve, and post jobs in Attract</span></span>](./creating-jobs-attract.md)

[<span data-ttu-id="2167c-125">Устранение неполадок интеграции с LinkedIn и Microsoft Dynamics 365 Talent — Attract</span><span class="sxs-lookup"><span data-stu-id="2167c-125">Troubleshooting integration with LinkedIn and Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-troubleshoot-linkedin.md)
