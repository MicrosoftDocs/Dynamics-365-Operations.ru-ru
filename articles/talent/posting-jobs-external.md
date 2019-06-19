---
title: Публикация вакансий на внешних сайтах вакансий из Attract
description: В этом разделе объясняется, как использовать Dynamics 365 for Talent - Attract для публикации объявлений о вакансиях на внешних сайтах трудоустройства
author: pganapmsft
manager: AnnBe
ms.date: 05/16/2019
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
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 9c27d1810a89ed7d7a7745e41c5f118dbdfe5dda
ms.sourcegitcommit: cadce85ca3004d53caf6bc49147a524c1bfd421f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/16/2019
ms.locfileid: "1590490"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a><span data-ttu-id="1aa98-103">Публикация вакансий на внешних сайтах вакансий из Attract</span><span class="sxs-lookup"><span data-stu-id="1aa98-103">Post jobs to external career sites from Attract</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1aa98-104">Вы хотите получить свои открытые вакансии перед как можно большим количеством квалифицированных кандидатов.</span><span class="sxs-lookup"><span data-stu-id="1aa98-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="1aa98-105">Сайты трудоустройства, такие как Broadbean, помогают достичь этой цели.</span><span class="sxs-lookup"><span data-stu-id="1aa98-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="1aa98-106">Microsoft Dynamics 365 Talent: Attract теперь позволяет вам публиковать объявления о вакансиях на сайте Broadbean, и Microsoft постоянно предоставляет новые предложения в этой области.</span><span class="sxs-lookup"><span data-stu-id="1aa98-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

## <a name="post-jobs-to-broadbean"></a><span data-ttu-id="1aa98-107">Размещение объявлений о вакансии на Broadbean</span><span class="sxs-lookup"><span data-stu-id="1aa98-107">Post jobs to Broadbean</span></span>

<span data-ttu-id="1aa98-108">Чтобы можно было размещать объявления о вакансиях на сайте Broadbean, необходимо настроить интеграцию Broadbean.</span><span class="sxs-lookup"><span data-stu-id="1aa98-108">Before you can post jobs to Broadbean, you must configure the Broadbean integration.</span></span>

> [!NOTE]
> - <span data-ttu-id="1aa98-109">Чтобы размещать объявления о вакансиях на внешних сайтах, необходима [надстройка Comprehensive Hiring](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="1aa98-109">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="1aa98-110">Для публикации вакансий в Broadbean через Attract необходимо иметь подписку на Broadbean.</span><span class="sxs-lookup"><span data-stu-id="1aa98-110">To post jobs to Broadbean through Attract, you must have a Broadbean subscription.</span></span>
> - <span data-ttu-id="1aa98-111">Эта функция в данный момент находится в режиме предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="1aa98-111">This feature is currently in preview.</span></span> <span data-ttu-id="1aa98-112">Если вы хотите попробовать его, необходимо [включить его в настройках администратора Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="1aa98-112">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

### <a name="configure-broadbean-integration"></a><span data-ttu-id="1aa98-113">Настройка интеграции Broadbean</span><span class="sxs-lookup"><span data-stu-id="1aa98-113">Configure Broadbean integration</span></span>

1. <span data-ttu-id="1aa98-114">Выполните вход в Attract в качестве администратора.</span><span class="sxs-lookup"><span data-stu-id="1aa98-114">Sign in to Attract as an admin.</span></span>
2. <span data-ttu-id="1aa98-115">Выберите кнопку **Параметры** (символ шестеренки) в верхнем правом углу страницы, затем выберите **Центр администрирования**.</span><span class="sxs-lookup"><span data-stu-id="1aa98-115">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>
3. <span data-ttu-id="1aa98-116">На вкладке **Параметры доски объявлений** в разделе **Включить интеграцию Broadbean** включите интеграцию.</span><span class="sxs-lookup"><span data-stu-id="1aa98-116">On the **Job board settings** tab, in the **Enable Broadbean integration** section, turn on the integration.</span></span>
4. <span data-ttu-id="1aa98-117">Обратитесь в Broadbean и введите сведения в **Имя пользователя, идентификатор клиента, токен шифрования**.</span><span class="sxs-lookup"><span data-stu-id="1aa98-117">Contact Broadbean, and enter your information in **Username, Client ID, Encryption Token**.</span></span>

> [!WARNING]
> <span data-ttu-id="1aa98-118">Ваши учетные данные Broadbean являются важными и конфиденциальными.</span><span class="sxs-lookup"><span data-stu-id="1aa98-118">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="1aa98-119">Поэтому храните и совместно используйте их ответственно.</span><span class="sxs-lookup"><span data-stu-id="1aa98-119">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="1aa98-120">Любой пользователь с ролью администратора в Attract можно просмотреть эти учетные данные.</span><span class="sxs-lookup"><span data-stu-id="1aa98-120">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="1aa98-121">Корпорация Майкрософт и Attract не участвуют в создании и ведении этих значений.</span><span class="sxs-lookup"><span data-stu-id="1aa98-121">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="1aa98-122">Вашей обязанностью является их обновление в Attract и работа с Broadbean для устранения любых проблем с вашими учетными данными.</span><span class="sxs-lookup"><span data-stu-id="1aa98-122">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>

### <a name="post-a-job-to-broadbean"></a><span data-ttu-id="1aa98-123">Размещение объявления о вакансии на Broadbean</span><span class="sxs-lookup"><span data-stu-id="1aa98-123">Post a job to Broadbean</span></span>

<span data-ttu-id="1aa98-124">После включения Broadbean агенты по найму и администраторы могут размещать на этом сайте объявления о вакансиях.</span><span class="sxs-lookup"><span data-stu-id="1aa98-124">After Broadbean has been turned on, recruiters and admins can post a job to it.</span></span> <span data-ttu-id="1aa98-125">Необходимо иметь URL-адрес подачи заявления для вакансии.</span><span class="sxs-lookup"><span data-stu-id="1aa98-125">You must have an apply URL for the job.</span></span>

1. <span data-ttu-id="1aa98-126">Откройте в Attract вакансию, которую необходимо разместить на сайте Broadbean.</span><span class="sxs-lookup"><span data-stu-id="1aa98-126">In Attract, open the job that you want to post to Broadbean.</span></span>
2. <span data-ttu-id="1aa98-127">В разделе **Объявления** выберите кнопку **Опубликовать**, которая соответствует Broadbean.</span><span class="sxs-lookup"><span data-stu-id="1aa98-127">In the **Postings** section, select the **Post Now** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="1aa98-128">Следуйте указаниям в окне Broadbean.</span><span class="sxs-lookup"><span data-stu-id="1aa98-128">Follow the instructions in the Broadbean window.</span></span>

<span data-ttu-id="1aa98-129">Attract передает следующую информацию в Broadbean:</span><span class="sxs-lookup"><span data-stu-id="1aa98-129">Attract passes the following information to Broadbean:</span></span>

- <span data-ttu-id="1aa98-130">Код запроса</span><span class="sxs-lookup"><span data-stu-id="1aa98-130">Request ID</span></span>
- <span data-ttu-id="1aa98-131">Название вакансии</span><span class="sxs-lookup"><span data-stu-id="1aa98-131">Job title</span></span>
- <span data-ttu-id="1aa98-132">Описание задания</span><span class="sxs-lookup"><span data-stu-id="1aa98-132">Job description</span></span>
- <span data-ttu-id="1aa98-133">Местонахождение вакансии</span><span class="sxs-lookup"><span data-stu-id="1aa98-133">Job location</span></span>
- <span data-ttu-id="1aa98-134">URL-адрес подачи заявления</span><span class="sxs-lookup"><span data-stu-id="1aa98-134">Apply URL</span></span>
- <span data-ttu-id="1aa98-135">Сведения агентства по найму</span><span class="sxs-lookup"><span data-stu-id="1aa98-135">Recruiter information</span></span>

<span data-ttu-id="1aa98-136">После того как сайт Broadbean успешно завершит подачу, раздел **Объявления** вакансии в Attract показывает статус Broadbean как **Опубликовано**.</span><span class="sxs-lookup"><span data-stu-id="1aa98-136">After Broadbean successfully completes the posting, the **Postings** section of the job in Attract shows the Broadbean status as **Posted**.</span></span>

> [!NOTE]
> - <span data-ttu-id="1aa98-137">Для Broadbean требуется поле **Отрасль**.</span><span class="sxs-lookup"><span data-stu-id="1aa98-137">Broadbean requires the **Industry** field.</span></span> <span data-ttu-id="1aa98-138">В настоящее время по умолчанию это поле имеет значение **ИТ**.</span><span class="sxs-lookup"><span data-stu-id="1aa98-138">Currently, this field is set to **IT** by default.</span></span> <span data-ttu-id="1aa98-139">Однако можно изменить это значение для правильной отрасли в окне объявления о вакансии сайта Broadbean.</span><span class="sxs-lookup"><span data-stu-id="1aa98-139">However, you can change the value to the correct industry in the window for Broadbean job posting.</span></span>
> - <span data-ttu-id="1aa98-140">Необходимо время необходимо Broadbean, чтобы завершить размещение объявления о вакансии на всех выбранных досках объявлений.</span><span class="sxs-lookup"><span data-stu-id="1aa98-140">It takes some time for Broadbean to finish posting your job to all the job boards that you selected.</span></span> <span data-ttu-id="1aa98-141">Поэтому может существовать небольшая задержка, прежде чем Attract предоставит статус обновления для вакансии.</span><span class="sxs-lookup"><span data-stu-id="1aa98-141">Therefore, there might be a slight delay before Attract provides a status update for the job.</span></span>

### <a name="view-a-broadbean-job-posting"></a><span data-ttu-id="1aa98-142">Просмотр объявления о вакансии на сайте Broadbean</span><span class="sxs-lookup"><span data-stu-id="1aa98-142">View a Broadbean job posting</span></span>

<span data-ttu-id="1aa98-143">После подачи объявления о вакансии на сайт Broadbean его можно просмотреть из Attract.</span><span class="sxs-lookup"><span data-stu-id="1aa98-143">After you post a job to Broadbean, you can view it from Attract.</span></span>

1. <span data-ttu-id="1aa98-144">Откройте в Attract вакансию, которую необходимо просмотреть на сайте Broadbean.</span><span class="sxs-lookup"><span data-stu-id="1aa98-144">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="1aa98-145">В разделе **Объявления** выберите кнопку с многоточием (**...**), которая соответствует Broadbean, затем выберите **Просмотреть**.</span><span class="sxs-lookup"><span data-stu-id="1aa98-145">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>

<span data-ttu-id="1aa98-146">Объявление о вакансии на сайте Broadbean отображается в новом окне.</span><span class="sxs-lookup"><span data-stu-id="1aa98-146">The Broadbean job posting appears in a new window.</span></span>

### <a name="update-a-broadbean-job-posting"></a><span data-ttu-id="1aa98-147">Обновление объявления о вакансии на сайте Broadbean</span><span class="sxs-lookup"><span data-stu-id="1aa98-147">Update a Broadbean job posting</span></span>

<span data-ttu-id="1aa98-148">Можно обновить объявление о вакансии на сайте Broadbean одним из двух способов.</span><span class="sxs-lookup"><span data-stu-id="1aa98-148">You can update a Broadbean job posting in two ways.</span></span>

1. <span data-ttu-id="1aa98-149">Откройте в Attract вакансию, которую необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="1aa98-149">In Attract, open the job that you want to update.</span></span>
2. <span data-ttu-id="1aa98-150">В разделе **Объявления** выберите кнопку **Обновить запись**, которая соответствует Broadbean.</span><span class="sxs-lookup"><span data-stu-id="1aa98-150">In the **Postings** section, select the **Update Post** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="1aa98-151">Измените объявление в окне Broadbean.</span><span class="sxs-lookup"><span data-stu-id="1aa98-151">Edit the posting in the Broadbean window.</span></span>

<span data-ttu-id="1aa98-152">–или–</span><span class="sxs-lookup"><span data-stu-id="1aa98-152">–or–</span></span>

1. <span data-ttu-id="1aa98-153">Откройте в Attract вакансию, которую необходимо просмотреть на сайте Broadbean.</span><span class="sxs-lookup"><span data-stu-id="1aa98-153">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="1aa98-154">В разделе **Объявления** выберите кнопку с многоточием (**...**), которая соответствует Broadbean, затем выберите **Просмотреть**.</span><span class="sxs-lookup"><span data-stu-id="1aa98-154">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>
3. <span data-ttu-id="1aa98-155">В окне Broadbean измените сведения о должности, затем повторно опубликуйте объявление о вакансии.</span><span class="sxs-lookup"><span data-stu-id="1aa98-155">In the Broadbean window, edit the job details, and then repost the job.</span></span> <span data-ttu-id="1aa98-156">Сведения о должности в Attract не изменяются.</span><span class="sxs-lookup"><span data-stu-id="1aa98-156">The job details in Attract aren't changed.</span></span>

### <a name="remove-a-broadbean-job-posting"></a><span data-ttu-id="1aa98-157">Удаление объявления о вакансии с сайта Broadbean</span><span class="sxs-lookup"><span data-stu-id="1aa98-157">Remove a Broadbean job posting</span></span>

<span data-ttu-id="1aa98-158">Если требуется, можно удалить объявление о вакансии с сайта Broadbean.</span><span class="sxs-lookup"><span data-stu-id="1aa98-158">You can remove a job posting from Broadbean as you require.</span></span>

1. <span data-ttu-id="1aa98-159">Откройте в Attract вакансию, которую необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="1aa98-159">In Attract, open the job that you want to remove.</span></span>
2. <span data-ttu-id="1aa98-160">В разделе **Объявления** выберите кнопку с многоточием (**...**), которая соответствует Broadbean, затем выберите **Удалить запись**.</span><span class="sxs-lookup"><span data-stu-id="1aa98-160">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **Remove Post**.</span></span>

<span data-ttu-id="1aa98-161">После того как сайт Broadbean удалит объявление о вакансии, у элемента Broadbean в Attract появится кнопка **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="1aa98-161">After Broadbean removes the job, the Broadbean item in Attract has a **Post Now** button.</span></span> <span data-ttu-id="1aa98-162">Наличие этой кнопки указывает, что вакансия была удалена и может быть опубликована снова.</span><span class="sxs-lookup"><span data-stu-id="1aa98-162">The presence of this button indicates that the job has been removed and can be posted again.</span></span>

### <a name="troubleshoot-the-broadbean-integration"></a><span data-ttu-id="1aa98-163">Устранение неполадок интеграции с Broadbean</span><span class="sxs-lookup"><span data-stu-id="1aa98-163">Troubleshoot the Broadbean integration</span></span>

<span data-ttu-id="1aa98-164">Если возникают трудности при публикации объявления о вакансии на сайте Broadbean, попробуйте выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1aa98-164">If you're having trouble posting a job to Broadbean, try these steps.</span></span>

1. <span data-ttu-id="1aa98-165">Убедитесь, что учетные данные Broadbean, введенные в Attract, действительные и правильные.</span><span class="sxs-lookup"><span data-stu-id="1aa98-165">Verify that the Broadbean credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="1aa98-166">Если учетные данные действительные и правильные, обратитесь в [службу поддержки Broadbean](https://www.broadbean.com/resources/support/).</span><span class="sxs-lookup"><span data-stu-id="1aa98-166">If the credentials are valid and correct, contact [Broadbean support](https://www.broadbean.com/resources/support/).</span></span>
3. <span data-ttu-id="1aa98-167">Если неполадка не устранена, обратитесь в [службу поддержки Майкрософт](./talent-support.md).</span><span class="sxs-lookup"><span data-stu-id="1aa98-167">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>
