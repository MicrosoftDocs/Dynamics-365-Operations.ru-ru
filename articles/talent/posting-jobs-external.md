---
title: Публикация вакансий на внешних сайтах вакансий из Attract
description: В этом разделе объясняется, как использовать Dynamics 365 Talent - Attract для публикации объявлений о вакансиях на внешних сайтах трудоустройства
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
ms.openlocfilehash: 2c822a1f799144bb9240fc0cbdeb6c5441e278af
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551411"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a><span data-ttu-id="82190-103">Публикация вакансий на внешних сайтах вакансий из Attract</span><span class="sxs-lookup"><span data-stu-id="82190-103">Post jobs to external career sites from Attract</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82190-104">Microsoft Dynamics 365 Talent: Attract помогает получить нужных специалистов, позволяя размещать объявления о вакансиях непосредственно из Attract в Broadbean.</span><span class="sxs-lookup"><span data-stu-id="82190-104">Microsoft Dynamics 365 Talent: Attract helps you get the talent you need by letting you post your jobs directly from Attract to Broadbean.</span></span> <span data-ttu-id="82190-105">После [создания вакансии](./creating-jobs-attract.md) достаточно нажать кнопку, чтобы эта вакансия стала доступна для всех потенциальных кандидатов на вакансию в Broadbean.</span><span class="sxs-lookup"><span data-stu-id="82190-105">After you [create a job](./creating-jobs-attract.md), all you have to do is click a button to put your job in front of all the potential job candidates on Broadbean.</span></span>

<span data-ttu-id="82190-106">Для размещения вакансий в Broadbean требуется соответствующая лицензия Broadbean.</span><span class="sxs-lookup"><span data-stu-id="82190-106">Posting jobs to Broadbean requires an appropriate Broadbean license.</span></span> <span data-ttu-id="82190-107">Broadbean предлагает различные продукты и планы.</span><span class="sxs-lookup"><span data-stu-id="82190-107">Broadbean offers various products and plans.</span></span> <span data-ttu-id="82190-108">Для получения дополнительных сведений о лицензиях и ценах Broadbean [обратитесь в Broadbean](https://www.broadbean.com/contact-us/).</span><span class="sxs-lookup"><span data-stu-id="82190-108">For more information about Broadbean licensing and pricing, [contact Broadbean](https://www.broadbean.com/contact-us/).</span></span>

<span data-ttu-id="82190-109">Если вы являетесь администратором, которому требуются дополнительные сведения о настройке интеграции Broadbean с Attract, см. раздел [Ввод настроек для внешних досок вакансий](./attract-admin-job-board-settings.md).</span><span class="sxs-lookup"><span data-stu-id="82190-109">If you're an admin who needs more information about how to configure Broadbean integration with Attract, see [Enter settings for external job boards](./attract-admin-job-board-settings.md).</span></span>

## <a name="post-jobs-to-broadbean"></a><span data-ttu-id="82190-110">Публикация вакансий в Broadbean</span><span class="sxs-lookup"><span data-stu-id="82190-110">Post jobs to Broadbean</span></span>

<span data-ttu-id="82190-111">После включения Broadbean агенты по найму и администраторы могут размещать на этом сайте объявления о вакансиях.</span><span class="sxs-lookup"><span data-stu-id="82190-111">After Broadbean has been turned on, recruiters and admins can post a job to it.</span></span> <span data-ttu-id="82190-112">Необходимо иметь URL-адрес подачи заявления для вакансии.</span><span class="sxs-lookup"><span data-stu-id="82190-112">You must have an apply URL for the job.</span></span>

1. <span data-ttu-id="82190-113">Откройте в Attract вакансию, которую необходимо разместить на сайте Broadbean.</span><span class="sxs-lookup"><span data-stu-id="82190-113">In Attract, open the job that you want to post to Broadbean.</span></span>
2. <span data-ttu-id="82190-114">В разделе **Объявления** выберите кнопку **Опубликовать**, которая соответствует Broadbean.</span><span class="sxs-lookup"><span data-stu-id="82190-114">In the **Postings** section, select the **Post Now** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="82190-115">Следуйте указаниям в окне Broadbean.</span><span class="sxs-lookup"><span data-stu-id="82190-115">Follow the instructions in the Broadbean window.</span></span>

<span data-ttu-id="82190-116">Attract передает следующую информацию в Broadbean:</span><span class="sxs-lookup"><span data-stu-id="82190-116">Attract passes the following information to Broadbean:</span></span>

- <span data-ttu-id="82190-117">Код запроса</span><span class="sxs-lookup"><span data-stu-id="82190-117">Request ID</span></span>
- <span data-ttu-id="82190-118">Название вакансии</span><span class="sxs-lookup"><span data-stu-id="82190-118">Job title</span></span>
- <span data-ttu-id="82190-119">Описание задания</span><span class="sxs-lookup"><span data-stu-id="82190-119">Job description</span></span>
- <span data-ttu-id="82190-120">Местонахождение вакансии</span><span class="sxs-lookup"><span data-stu-id="82190-120">Job location</span></span>
- <span data-ttu-id="82190-121">URL-адрес подачи заявления</span><span class="sxs-lookup"><span data-stu-id="82190-121">Apply URL</span></span>
- <span data-ttu-id="82190-122">Сведения агентства по найму</span><span class="sxs-lookup"><span data-stu-id="82190-122">Recruiter information</span></span>

<span data-ttu-id="82190-123">После того как сайт Broadbean успешно завершит подачу, раздел **Объявления** вакансии в Attract показывает статус Broadbean как **Опубликовано**.</span><span class="sxs-lookup"><span data-stu-id="82190-123">After Broadbean successfully completes the posting, the **Postings** section of the job in Attract shows the Broadbean status as **Posted**.</span></span>

> [!NOTE]
> - <span data-ttu-id="82190-124">Для Broadbean требуется поле **Отрасль**.</span><span class="sxs-lookup"><span data-stu-id="82190-124">Broadbean requires the **Industry** field.</span></span> <span data-ttu-id="82190-125">В настоящее время по умолчанию это поле имеет значение **ИТ**.</span><span class="sxs-lookup"><span data-stu-id="82190-125">Currently, this field is set to **IT** by default.</span></span> <span data-ttu-id="82190-126">Однако можно изменить это значение для правильной отрасли в окне объявления о вакансии сайта Broadbean.</span><span class="sxs-lookup"><span data-stu-id="82190-126">However, you can change the value to the correct industry in the window for Broadbean job posting.</span></span>
> - <span data-ttu-id="82190-127">Необходимо время необходимо Broadbean, чтобы завершить размещение объявления о вакансии на всех выбранных досках объявлений.</span><span class="sxs-lookup"><span data-stu-id="82190-127">It takes some time for Broadbean to finish posting your job to all the job boards that you selected.</span></span> <span data-ttu-id="82190-128">Поэтому может существовать небольшая задержка, прежде чем Attract предоставит статус обновления для вакансии.</span><span class="sxs-lookup"><span data-stu-id="82190-128">Therefore, there might be a slight delay before Attract provides a status update for the job.</span></span>

### <a name="view-a-broadbean-job-posting"></a><span data-ttu-id="82190-129">Просмотр объявления о вакансии на сайте Broadbean</span><span class="sxs-lookup"><span data-stu-id="82190-129">View a Broadbean job posting</span></span>

<span data-ttu-id="82190-130">После подачи объявления о вакансии на сайт Broadbean его можно просмотреть из Attract.</span><span class="sxs-lookup"><span data-stu-id="82190-130">After you post a job to Broadbean, you can view it from Attract.</span></span>

1. <span data-ttu-id="82190-131">Откройте в Attract вакансию, которую необходимо просмотреть на сайте Broadbean.</span><span class="sxs-lookup"><span data-stu-id="82190-131">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="82190-132">На вкладке **Объявления** выберите кнопку с многоточием (**...**), которая соответствует Broadbean, затем выберите **Просмотреть**.</span><span class="sxs-lookup"><span data-stu-id="82190-132">On the **Postings** tab, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>

<span data-ttu-id="82190-133">Объявление о вакансии на сайте Broadbean отображается в новом окне.</span><span class="sxs-lookup"><span data-stu-id="82190-133">The Broadbean job posting appears in a new window.</span></span>

### <a name="update-a-broadbean-job-posting"></a><span data-ttu-id="82190-134">Обновление объявления о вакансии на сайте Broadbean</span><span class="sxs-lookup"><span data-stu-id="82190-134">Update a Broadbean job posting</span></span>

<span data-ttu-id="82190-135">Можно обновить объявление о вакансии на сайте Broadbean одним из двух способов.</span><span class="sxs-lookup"><span data-stu-id="82190-135">You can update a Broadbean job posting in two ways.</span></span>

1. <span data-ttu-id="82190-136">Откройте в Attract вакансию, которую необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="82190-136">In Attract, open the job that you want to update.</span></span>
2. <span data-ttu-id="82190-137">В разделе **Объявления** выберите кнопку **Обновить запись**, которая соответствует Broadbean.</span><span class="sxs-lookup"><span data-stu-id="82190-137">In the **Postings** section, select the **Update Post** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="82190-138">Измените объявление в окне Broadbean.</span><span class="sxs-lookup"><span data-stu-id="82190-138">Edit the posting in the Broadbean window.</span></span>

<span data-ttu-id="82190-139">–или–</span><span class="sxs-lookup"><span data-stu-id="82190-139">–or–</span></span>

1. <span data-ttu-id="82190-140">Откройте в Attract вакансию, которую необходимо просмотреть на сайте Broadbean.</span><span class="sxs-lookup"><span data-stu-id="82190-140">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="82190-141">В разделе **Объявления** выберите кнопку с многоточием (**...**), которая соответствует Broadbean, затем выберите **Просмотреть**.</span><span class="sxs-lookup"><span data-stu-id="82190-141">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>
3. <span data-ttu-id="82190-142">В окне Broadbean измените сведения о должности, затем повторно опубликуйте объявление о вакансии.</span><span class="sxs-lookup"><span data-stu-id="82190-142">In the Broadbean window, edit the job details, and then repost the job.</span></span> <span data-ttu-id="82190-143">Сведения о должности в Attract не изменяются.</span><span class="sxs-lookup"><span data-stu-id="82190-143">The job details in Attract aren't changed.</span></span>

### <a name="remove-a-broadbean-job-posting"></a><span data-ttu-id="82190-144">Удаление объявления о вакансии с сайта Broadbean</span><span class="sxs-lookup"><span data-stu-id="82190-144">Remove a Broadbean job posting</span></span>

<span data-ttu-id="82190-145">Если требуется, можно удалить объявление о вакансии с сайта Broadbean.</span><span class="sxs-lookup"><span data-stu-id="82190-145">You can remove a job posting from Broadbean as you require.</span></span>

1. <span data-ttu-id="82190-146">Откройте в Attract вакансию, которую необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="82190-146">In Attract, open the job that you want to remove.</span></span>
2. <span data-ttu-id="82190-147">В разделе **Объявления** выберите кнопку с многоточием (**...**), которая соответствует Broadbean, затем выберите **Удалить запись**.</span><span class="sxs-lookup"><span data-stu-id="82190-147">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **Remove Post**.</span></span>

<span data-ttu-id="82190-148">После того как сайт Broadbean удалит объявление о вакансии, у элемента Broadbean в Attract появится кнопка **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="82190-148">After Broadbean removes the job, the Broadbean item in Attract has a **Post Now** button.</span></span> <span data-ttu-id="82190-149">Наличие этой кнопки указывает, что вакансия была удалена и может быть опубликована снова.</span><span class="sxs-lookup"><span data-stu-id="82190-149">The presence of this button indicates that the job has been removed and can be posted again.</span></span>

### <a name="troubleshoot-job-posting-to-broadbean"></a><span data-ttu-id="82190-150">Устранение неполадок размещения объявлений о вакансиях в Broadbean</span><span class="sxs-lookup"><span data-stu-id="82190-150">Troubleshoot job posting to Broadbean</span></span>

<span data-ttu-id="82190-151">Если возникают трудности при публикации объявления о вакансии на сайте Broadbean, попробуйте выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="82190-151">If you're having trouble posting a job to Broadbean, try these steps.</span></span>

1. <span data-ttu-id="82190-152">Убедитесь, что учетные данные Broadbean, введенные в Attract, действительные и правильные.</span><span class="sxs-lookup"><span data-stu-id="82190-152">Verify that the Broadbean credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="82190-153">Если учетные данные действительные и правильные, обратитесь в [службу поддержки Broadbean](https://www.broadbean.com/resources/support/).</span><span class="sxs-lookup"><span data-stu-id="82190-153">If the credentials are valid and correct, contact [Broadbean support](https://www.broadbean.com/resources/support/).</span></span>
3. <span data-ttu-id="82190-154">Если неполадка не устранена, обратитесь в [службу поддержки Майкрософт](./talent-support.md).</span><span class="sxs-lookup"><span data-stu-id="82190-154">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="82190-155">См. также</span><span class="sxs-lookup"><span data-stu-id="82190-155">See also</span></span>

[<span data-ttu-id="82190-156">Создание вакансий</span><span class="sxs-lookup"><span data-stu-id="82190-156">Create jobs</span></span>](./creating-jobs-attract.md)

[<span data-ttu-id="82190-157">Ввод настроек для внешних досок вакансий</span><span class="sxs-lookup"><span data-stu-id="82190-157">Enter settings for external job boards</span></span>](./attract-admin-job-board-settings.md)
