---
title: Публикация вакансий в LinkedIn из Attract
description: В этом разделе объясняется, как использовать Dynamics 365 Talent - Attract для публикации объявлений о вакансиях на LinkedIn.
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
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
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 782a2e5de6edf0e85c4d32a0910f5f3c01981a01
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462320"
---
# <a name="post-jobs-to-linkedin-from-attract"></a><span data-ttu-id="6507c-103">Публикация вакансий в LinkedIn из Attract</span><span class="sxs-lookup"><span data-stu-id="6507c-103">Post jobs to LinkedIn from Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6507c-104">LinkedIn — это крупнейшая профессиональная сеть в Интернете, предоставляющая вам доступ к лучшим специалистам в мире.</span><span class="sxs-lookup"><span data-stu-id="6507c-104">LinkedIn is the largest online professional network, giving you access to the world's top talent.</span></span> <span data-ttu-id="6507c-105">Microsoft Dynamics 365 Talent: Attract помогает получить нужных специалистов, позволяя размещать объявления о вакансиях непосредственно из Attract в LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="6507c-105">Microsoft Dynamics 365 Talent: Attract helps you get the talent that you need by letting you post your jobs directly from Attract to LinkedIn.</span></span>

<span data-ttu-id="6507c-106">Attract позволяет размещать объявления в ограниченных списках в LinkedIn без дополнительных затрат.</span><span class="sxs-lookup"><span data-stu-id="6507c-106">Attract lets you post Limited Listings to LinkedIn at no extra cost.</span></span> <span data-ttu-id="6507c-107">Эти списки доступны только через партнеров программного обеспечения LinkedIn, таких как Attract.</span><span class="sxs-lookup"><span data-stu-id="6507c-107">These listings are available only through LinkedIn software partners such as Attract.</span></span> <span data-ttu-id="6507c-108">Они не отображаются в панели **Вакансии** на странице LinkedIn вашей компании, поскольку там отображаются только оплаченные списки.</span><span class="sxs-lookup"><span data-stu-id="6507c-108">They don't appear in the **Careers** panel on your company's LinkedIn page, because only paid listings appear there.</span></span> <span data-ttu-id="6507c-109">Однако они отображаются, когда потенциальные кандидаты просматривают все доступные вакансии.</span><span class="sxs-lookup"><span data-stu-id="6507c-109">However, they are shown when potential candidates view all available jobs.</span></span> <span data-ttu-id="6507c-110">Ограниченные списки также отображаются в результатах поиска вакансий в LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="6507c-110">Limited Listings are also shown in LinkedIn job searches.</span></span>

<span data-ttu-id="6507c-111">После [создания вакансии](./creating-jobs-attract.md) в приложении Attract достаточно выбрать кнопку, чтобы эта вакансия стала доступна тысячами потенциальных кандидатов в LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="6507c-111">After you [create a job](./creating-jobs-attract.md) in Attract, you just have to select a button to put your job in front of thousands of potential candidates on LinkedIn.</span></span>

<span data-ttu-id="6507c-112">В следующей таблице показаны действия, которые можно выполнить с LinkedIn в зависимости от роли пользователя.</span><span class="sxs-lookup"><span data-stu-id="6507c-112">The following table shows the actions that you can perform on LinkedIn, depending on your user role.</span></span>

| <span data-ttu-id="6507c-113">Роль</span><span class="sxs-lookup"><span data-stu-id="6507c-113">Role</span></span> | <span data-ttu-id="6507c-114">Действия, которые можно выполнить</span><span class="sxs-lookup"><span data-stu-id="6507c-114">Actions that you can take</span></span> |
|---|---|
| <span data-ttu-id="6507c-115">Администрирование</span><span class="sxs-lookup"><span data-stu-id="6507c-115">Admin</span></span> | <span data-ttu-id="6507c-116">Размещение, повторное размещение и отмена размещения</span><span class="sxs-lookup"><span data-stu-id="6507c-116">Post, repost, and unpost</span></span> |
| <span data-ttu-id="6507c-117">Специалист по комплектации штата</span><span class="sxs-lookup"><span data-stu-id="6507c-117">Hiring manager</span></span> | <span data-ttu-id="6507c-118">Только чтение</span><span class="sxs-lookup"><span data-stu-id="6507c-118">Read only</span></span> |
| <span data-ttu-id="6507c-119">Наниматель</span><span class="sxs-lookup"><span data-stu-id="6507c-119">Recruiter</span></span> | <span data-ttu-id="6507c-120">Размещение, повторное размещение и отмена размещения</span><span class="sxs-lookup"><span data-stu-id="6507c-120">Post, repost, and unpost</span></span> |
| <span data-ttu-id="6507c-121">Проводящий собеседование</span><span class="sxs-lookup"><span data-stu-id="6507c-121">Interviewer</span></span> | <span data-ttu-id="6507c-122">Нет доступа</span><span class="sxs-lookup"><span data-stu-id="6507c-122">No access</span></span> |
| <span data-ttu-id="6507c-123">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="6507c-123">Read-only</span></span> | <span data-ttu-id="6507c-124">Только чтение</span><span class="sxs-lookup"><span data-stu-id="6507c-124">Read only</span></span> |

<span data-ttu-id="6507c-125">Дополнительные сведения о ролях пользователей в Attract см. в разделе [Безопасность и управление ролями в Attract](./security-attract.md).</span><span class="sxs-lookup"><span data-stu-id="6507c-125">For more information about user roles in Attract, see [Security and role management in Attract](./security-attract.md).</span></span>

<span data-ttu-id="6507c-126">Если вы являетесь администратором и вам нужны дополнительные сведения о настройке интеграции LinkedIn с Attract, см. раздел [Настройка интеграции с LinkedIn для Microsoft Dynamics 365 Talent — Attract](./attract-admin-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="6507c-126">If you're an admin and need more information about how to configure LinkedIn integration with Attract, see [Set up integration with LinkedIn for Microsoft Dynamics 365 Talent - Attract](./attract-admin-linkedin.md).</span></span>

<span data-ttu-id="6507c-127">Вакансии, опубликованные в LinkedIn, отображаются на действующем сайте LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="6507c-127">Jobs that are posted to LinkedIn appear on the live LinkedIn site.</span></span> <span data-ttu-id="6507c-128">В LinkedIn отсутствует тестовая среда для публикации вакансий.</span><span class="sxs-lookup"><span data-stu-id="6507c-128">LinkedIn doesn't have a test environment for posting jobs.</span></span> <span data-ttu-id="6507c-129">Таким образом, следите, чтобы случайно не опубликовать тестовые объявления о вакансиях.</span><span class="sxs-lookup"><span data-stu-id="6507c-129">Therefore, make sure that you don't accidentally post any test jobs.</span></span>

## <a name="post-jobs-to-linkedin"></a><span data-ttu-id="6507c-130">Публикация вакансий в LinkedIn</span><span class="sxs-lookup"><span data-stu-id="6507c-130">Post jobs to LinkedIn</span></span>

1. <span data-ttu-id="6507c-131">Откройте в Attract вакансию, которую необходимо разместить на сайте LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="6507c-131">In Attract, open the job that you want to post to LinkedIn.</span></span>
2. <span data-ttu-id="6507c-132">На вкладке **Объявления** выберите кнопку **Опубликовать**, которая соответствует LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="6507c-132">On the **Postings** tab, select the **Post Now** button that corresponds to LinkedIn.</span></span>

    <span data-ttu-id="6507c-133">[![Публикация вакансий из Attract в LinkedIn](./media/attract-post-job-to-linkedin.png)](./media/attract-post-job-to-linkedin.png)</span><span class="sxs-lookup"><span data-stu-id="6507c-133">[![Attract post job to LinkedIn](./media/attract-post-job-to-linkedin.png)](./media/attract-post-job-to-linkedin.png)</span></span>

3. <span data-ttu-id="6507c-134">В диалоговом окне **Создание веб-адреса "Подать заявление"** выберите параметр в разделе **Кандидаты могут подавать заявление при помощи**.</span><span class="sxs-lookup"><span data-stu-id="6507c-134">In the **Create an "Apply now" web address** dialog box, select an option under **Candidates can apply using a**.</span></span> <span data-ttu-id="6507c-135">Рекомендуется выбирать **Ссылка в Attract**.</span><span class="sxs-lookup"><span data-stu-id="6507c-135">We recommend that you select **Link in Attract**.</span></span>
4. <span data-ttu-id="6507c-136">Выберите **Готово**.</span><span class="sxs-lookup"><span data-stu-id="6507c-136">Select **Done**.</span></span>
5. <span data-ttu-id="6507c-137">В окне сообщения **Отправить для размещения** выберите **Подтвердить**.</span><span class="sxs-lookup"><span data-stu-id="6507c-137">In the **Submit for posting** message box, select **Confirm**.</span></span>

<span data-ttu-id="6507c-138">После того как сайт LinkedIn успешно завершит подачу, раздел **Объявления** вакансии в Attract показывает статус LinkedIn как **Опубликовано**.</span><span class="sxs-lookup"><span data-stu-id="6507c-138">After LinkedIn successfully completes the posting, the **Postings** section of the job in Attract shows the LinkedIn status as **Posted**.</span></span> <span data-ttu-id="6507c-139">Вакансия может появиться в LinkedIn с задержкой до 48 часов.</span><span class="sxs-lookup"><span data-stu-id="6507c-139">It can take up to 48 hours for your job to appear in LinkedIn.</span></span>

<span data-ttu-id="6507c-140">Когда заинтересованные кандидаты выбирают **Просмотр** рядом со списком, они увидят полные сведения о вакансии вместе со сведениями о том, как подать заявление.</span><span class="sxs-lookup"><span data-stu-id="6507c-140">When interested candidates select **View** next to your listing, they will see the full job details, together with your information about how to apply.</span></span>

<span data-ttu-id="6507c-141">Все вакансий, опубликованные через приложение Attract, публикуются в ограниченных списках.</span><span class="sxs-lookup"><span data-stu-id="6507c-141">All job postings that are done through Attract are Limited Listings.</span></span> <span data-ttu-id="6507c-142">Дополнительные сведения об ограниченных списках в LinkedIn см. в разделе [Ограниченные списки и премиальные рекламные места вакансий для сканирования объявлений о вакансиях](https://www.linkedin.com/help/recruiter/answer/79049).</span><span class="sxs-lookup"><span data-stu-id="6507c-142">For more information about Limited Listings on LinkedIn, see [Limited Listings vs Premium Job Slots for Job Wrapping](https://www.linkedin.com/help/recruiter/answer/79049).</span></span>

<span data-ttu-id="6507c-143">Если вы не можете опубликовать объявления о вакансиях в LinkedIn, см. раздел [Устранение неполадок интеграции с LinkedIn и Microsoft Dynamics 365 Talent — Attract](./attract-troubleshoot-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="6507c-143">If you're having trouble posting jobs to LinkedIn, see [Troubleshooting integration with LinkedIn and Microsoft Dynamics 365 Talent - Attract](./attract-troubleshoot-linkedin.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="6507c-144">См. также</span><span class="sxs-lookup"><span data-stu-id="6507c-144">See also</span></span>

[<span data-ttu-id="6507c-145">Вопросы и ответы по интеграции Attract с LinkedIn</span><span class="sxs-lookup"><span data-stu-id="6507c-145">Attract integration with LinkedIn FAQ</span></span>](./attract-linkedin-faq.md)

[<span data-ttu-id="6507c-146">Настройка интеграции с LinkedIn для Microsoft Dynamics 365 Talent — Attract</span><span class="sxs-lookup"><span data-stu-id="6507c-146">Set up integration with LinkedIn for Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-admin-linkedin.md)

[<span data-ttu-id="6507c-147">Создание, утверждение и публикация вакансий в Attract</span><span class="sxs-lookup"><span data-stu-id="6507c-147">Create, approve, and post jobs in Attract</span></span>](./creating-jobs-attract.md)

[<span data-ttu-id="6507c-148">Поиск кандидатов с помощью LinkedIn Recruiter</span><span class="sxs-lookup"><span data-stu-id="6507c-148">Source candidates with LinkedIn Recruiter</span></span>](./attract-linkedin-recruiter.md)

[<span data-ttu-id="6507c-149">Устранение неполадок интеграции с LinkedIn</span><span class="sxs-lookup"><span data-stu-id="6507c-149">Troubleshoot integration with LinkedIn</span></span>](./attract-troubleshoot-linkedin.md)
