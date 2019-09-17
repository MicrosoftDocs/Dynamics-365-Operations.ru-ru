---
title: Устранение неполадок интеграции с LinkedIn и Microsoft Dynamics 365 for Talent - Attract
description: В этой теме объясняется, как устранять неполадки при попытке публикации объявлений о вакансиях в LinkedIn из Microsoft Dynamics 365 for Talent - Attract.
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
ms.openlocfilehash: 82ba7c505ba09e47f3c517c74c22e6aef7cd4e65
ms.sourcegitcommit: 7c49475402632069685df714546770d30804af7f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/11/2019
ms.locfileid: "1739365"
---
# <a name="troubleshoot-integration-with-linkedin"></a><span data-ttu-id="7b955-103">Устранение неполадок интеграции с LinkedIn</span><span class="sxs-lookup"><span data-stu-id="7b955-103">Troubleshoot integration with LinkedIn</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7b955-104">Следующие сведения помогут в устранении неполадок, которые могут возникнуть при попытке публикации объявлений о вакансиях в LinkedIn из Microsoft Dynamics 365 for Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="7b955-104">Use the following information to help troubleshoot issues that you might have when you try to post jobs to LinkedIn from Microsoft Dynamics 365 for Talent: Attract.</span></span>

## <a name="you-cant-sign-in-to-linkedin-from-attract"></a><span data-ttu-id="7b955-105">Нельзя войти в LinkedIn из Attract</span><span class="sxs-lookup"><span data-stu-id="7b955-105">You can't sign in to LinkedIn from Attract</span></span>

<span data-ttu-id="7b955-106">Если вы не можете войти в LinkedIn из Attract, попробуйте следующие действия:</span><span class="sxs-lookup"><span data-stu-id="7b955-106">If you're having trouble signing in to LinkedIn from Attract, try these steps:</span></span>

1. <span data-ttu-id="7b955-107">Убедитесь, что учетные данные LinkedIn, введенные в Attract, действительные и правильные.</span><span class="sxs-lookup"><span data-stu-id="7b955-107">Verify that the LinkedIn credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="7b955-108">Если учетные данные действительные и правильные, обратитесь в [службу поддержки LinkedIn](https://www.linkedin.com/help/linkedin).</span><span class="sxs-lookup"><span data-stu-id="7b955-108">If the credentials are valid and correct, contact [LinkedIn support](https://www.linkedin.com/help/linkedin).</span></span>
3. <span data-ttu-id="7b955-109">Если неполадка не устранена, обратитесь в [службу поддержки Майкрософт](./talent-support.md).</span><span class="sxs-lookup"><span data-stu-id="7b955-109">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>

## <a name="job-posts-from-attract-dont-appear-on-linkedin"></a><span data-ttu-id="7b955-110">Объявления о вакансиях из Attract не отображаются в LinkedIn</span><span class="sxs-lookup"><span data-stu-id="7b955-110">Job posts from Attract don't appear on LinkedIn</span></span>

<span data-ttu-id="7b955-111">Если вакансия не появилось в LinkedIn через 24 часа, попробуйте выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="7b955-111">If your job hasn't appeared on LinkedIn after 24 hours, try these steps:</span></span>

1. <span data-ttu-id="7b955-112">Убедитесь, что код LinkedIn вашей компании отображается на странице компании LinkedIn и правильно введен в центре администрирования Attract.</span><span class="sxs-lookup"><span data-stu-id="7b955-112">Make sure that your LinkedIn Company ID maps to your LinkedIn company page and is correctly entered in the Attract Admin center.</span></span> <span data-ttu-id="7b955-113">Дополнительные сведения об изменении настроек LinkedIn в центре администрирования см. в разделе [Настройка интеграции с LinkedIn](attract-admin-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="7b955-113">For more information about how to change LinkedIn settings in the Admin center, see [Set up integration with LinkedIn](attract-admin-linkedin.md).</span></span> <span data-ttu-id="7b955-114">Дополнительные сведения о кодах компании LinkedIn см. в разделе [Назначение кода компании LinkedIn с доской вакансий LinkedIn — часто задаваемые вопросы](https://www.linkedin.com/help/linkedin/answer/98972).</span><span class="sxs-lookup"><span data-stu-id="7b955-114">For more information about LinkedIn Company IDs, see [Associating your LinkedIn Company ID with the LinkedIn Job Board - Frequently Asked Questions](https://www.linkedin.com/help/linkedin/answer/98972).</span></span>
2. <span data-ttu-id="7b955-115">Проверьте сведения о вакансии в LinkedIn, чтобы убедиться в том, что адрес заполнен.</span><span class="sxs-lookup"><span data-stu-id="7b955-115">Check the job details on LinkedIn to make sure that the address is complete.</span></span> <span data-ttu-id="7b955-116">Для успешной публикации объявления о вакансии в LinkedIn требуется, по крайней мере, город и страна или регион вакансии.</span><span class="sxs-lookup"><span data-stu-id="7b955-116">To post a job successfully, LinkedIn needs at least the city and country or region of the job.</span></span>
3. <span data-ttu-id="7b955-117">Убедитесь, что вакансия не дублирует другую вакансию, которая была опубликована в LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="7b955-117">Make sure that the job doesn't duplicate another job that has been posted on LinkedIn.</span></span> <span data-ttu-id="7b955-118">LinkedIn не публикует вакансии, которые являются дубликатами премиальных рекламных мест вакансий или ограниченных списков LinkedIn из другого источника.</span><span class="sxs-lookup"><span data-stu-id="7b955-118">LinkedIn won't post jobs that are duplicates of either LinkedIn Premium Job Slots or Limited Listings from another source.</span></span> <span data-ttu-id="7b955-119">Убедитесь, что другой сотрудник компании не опубликовал эту вакансию вручную.</span><span class="sxs-lookup"><span data-stu-id="7b955-119">Verify that another person at your company didn't already post the job manually.</span></span>

## <a name="see-also"></a><span data-ttu-id="7b955-120">См. также</span><span class="sxs-lookup"><span data-stu-id="7b955-120">See also</span></span>

[<span data-ttu-id="7b955-121">Вопросы и ответы по LinkedIn</span><span class="sxs-lookup"><span data-stu-id="7b955-121">LinkedIn FAQ</span></span>](./attract-linkedin-faq.md)

[<span data-ttu-id="7b955-122">Публикация вакансий в LinkedIn из Attract</span><span class="sxs-lookup"><span data-stu-id="7b955-122">Post jobs to LinkedIn from Attract</span></span>](./attract-post-jobs-to-linkedin.md)

[<span data-ttu-id="7b955-123">Поиск кандидатов с помощью LinkedIn Recruiter</span><span class="sxs-lookup"><span data-stu-id="7b955-123">Source candidates with LinkedIn Recruiter</span></span>](./attract-linkedin-recruiter.md)

[<span data-ttu-id="7b955-124">Создание вакансий</span><span class="sxs-lookup"><span data-stu-id="7b955-124">Create jobs</span></span>](./creating-jobs-attract.md)

[<span data-ttu-id="7b955-125">Устранение неполадок интеграции с LinkedIn</span><span class="sxs-lookup"><span data-stu-id="7b955-125">Troubleshoot integration with LinkedIn</span></span>](./attract-troubleshoot-linkedin.md)
