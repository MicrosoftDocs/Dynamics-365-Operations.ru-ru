---
title: Экспорт данных из Attract и Onboard
description: Экспорт данных из Dynamics 365 Talent — Attract и Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462297"
---
# <a name="export-data-from-attract-and-onboard"></a><span data-ttu-id="da52f-103">Экспорт данных из Attract и Onboard</span><span class="sxs-lookup"><span data-stu-id="da52f-103">Export data from Attract and Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="da52f-104">Как указано в разделе [Окончание использования приложений Dynamics 365 Talent: Attract и Dynamics 365 Talent: Onboard](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), использование Dynamics 365 Talent: Attract и Dynamics 365 Talent: Onboard прекращается с 1 февраля 2022 года.</span><span class="sxs-lookup"><span data-stu-id="da52f-104">As announced in [Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), we're retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard on February 1, 2022.</span></span> <span data-ttu-id="da52f-105">Чтобы помочь выполнить миграцию на другой продукт, для обоих приложений будет предусмотрен экспорт данных.</span><span class="sxs-lookup"><span data-stu-id="da52f-105">To help with your migration to another product, both apps now provide data export capabilities.</span></span>

## <a name="export-data-from-attract"></a><span data-ttu-id="da52f-106">Экспорт данных из Attract</span><span class="sxs-lookup"><span data-stu-id="da52f-106">Export data from Attract</span></span>

<span data-ttu-id="da52f-107">Данные можно экспортировать без ограничения доступа к среде.</span><span class="sxs-lookup"><span data-stu-id="da52f-107">You can export your data without restricting access to your environment.</span></span> <span data-ttu-id="da52f-108">Это может потребоваться для тестирования или понимания нашей структуры данных.</span><span class="sxs-lookup"><span data-stu-id="da52f-108">You might want to do this for testing purposes or to understand our data structure.</span></span> <span data-ttu-id="da52f-109">Когда все готово для миграции, ограничьте доступ к своей среде Attract, выполнив инструкции, приведенные после этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="da52f-109">When you're ready to migrate, restrict access to your Attract environment using the instructions after this procedure.</span></span> <span data-ttu-id="da52f-110">Обязательно экспортируйте данные повторно.</span><span class="sxs-lookup"><span data-stu-id="da52f-110">Be sure to export your data again.</span></span> 

1. <span data-ttu-id="da52f-111">Перейдите на страницу [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span><span class="sxs-lookup"><span data-stu-id="da52f-111">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="da52f-112">В разделе **Экспорт данных** выберите **Запрос на экспорт данных**.</span><span class="sxs-lookup"><span data-stu-id="da52f-112">Under **Data export**, select **Request a data export**.</span></span>

   ![[<span data-ttu-id="da52f-113">Запрос на экспорт данных из Attract</span><span class="sxs-lookup"><span data-stu-id="da52f-113">Request a data export from Attract</span></span>](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. <span data-ttu-id="da52f-114">После появления окна сообщений **Ваш запрос обрабатывается** нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="da52f-114">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="da52f-115">Экспорт данных может занять до 20 минут в зависимости от размера экспорта.</span><span class="sxs-lookup"><span data-stu-id="da52f-115">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="da52f-116">После завершения экспорта нажмите кнопку **Загрузить** рядом.</span><span class="sxs-lookup"><span data-stu-id="da52f-116">When your export completes, select the **Download** button next to it.</span></span> 

   >[!NOTE]
   ><span data-ttu-id="da52f-117">Все экспортируемые данные доступны в течение семи дней, после чего срок действия ссылки **Загрузить** истекает.</span><span class="sxs-lookup"><span data-stu-id="da52f-117">All data exports are available for seven days, at which point the **Download** link expires.</span></span></br>
   
<span data-ttu-id="da52f-118">Загрузка содержит ZIP-файл с вашими данными Attract, включая следующие папки:</span><span class="sxs-lookup"><span data-stu-id="da52f-118">The download contains a .zip file with your Attract data, including the following folders:</span></span>

| <span data-ttu-id="da52f-119">Имя папки</span><span class="sxs-lookup"><span data-stu-id="da52f-119">Folder name</span></span> | <span data-ttu-id="da52f-120">Описание</span><span class="sxs-lookup"><span data-stu-id="da52f-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="da52f-121">Параметры администрирования</span><span class="sxs-lookup"><span data-stu-id="da52f-121">Admin settings</span></span> | <span data-ttu-id="da52f-122">Конфигурации центра администрирования Attract.</span><span class="sxs-lookup"><span data-stu-id="da52f-122">Attract admin center configurations.</span></span> |
| <span data-ttu-id="da52f-123">Кандидаты</span><span class="sxs-lookup"><span data-stu-id="da52f-123">Candidates</span></span> | <span data-ttu-id="da52f-124">Все кандидаты, которые были добавлены в задания или кадровые пулы.</span><span class="sxs-lookup"><span data-stu-id="da52f-124">All candidates that were added to jobs or talent pools.</span></span> |
| <span data-ttu-id="da52f-125">Шаблоны электронной почты</span><span class="sxs-lookup"><span data-stu-id="da52f-125">Email templates</span></span> | <span data-ttu-id="da52f-126">Все шаблоны электронной почты, которые были настроены для среды.</span><span class="sxs-lookup"><span data-stu-id="da52f-126">All email templates that were configured for the environment.</span></span> |
| <span data-ttu-id="da52f-127">Шаблоны пакетов предложений работы</span><span class="sxs-lookup"><span data-stu-id="da52f-127">Job offer package templates</span></span> | <span data-ttu-id="da52f-128">Все созданные шаблоны пакетов предложений работы и связанные с ними конфигурации.</span><span class="sxs-lookup"><span data-stu-id="da52f-128">All job offer package templates that were created, plus their associated configurations.</span></span> |
| <span data-ttu-id="da52f-129">Наборы правил для предложений работы</span><span class="sxs-lookup"><span data-stu-id="da52f-129">Job offer rule sets</span></span> |  <span data-ttu-id="da52f-130">Все файлы наборов правил, отправленные для управления предложениями.</span><span class="sxs-lookup"><span data-stu-id="da52f-130">All rule set files that were uploaded for offer management.</span></span> |
| <span data-ttu-id="da52f-131">Шаблоны предложений работы</span><span class="sxs-lookup"><span data-stu-id="da52f-131">Job offer templates</span></span> | <span data-ttu-id="da52f-132">Все шаблоны документов для предложений работы, созданные для среды.</span><span class="sxs-lookup"><span data-stu-id="da52f-132">All job offer document templates created for the environment.</span></span> |
| <span data-ttu-id="da52f-133">Вакансии</span><span class="sxs-lookup"><span data-stu-id="da52f-133">Job openings</span></span> | <span data-ttu-id="da52f-134">Все созданные вакансии.</span><span class="sxs-lookup"><span data-stu-id="da52f-134">All created jobs.</span></span> <span data-ttu-id="da52f-135">Удаленные работы не экспортируются.</span><span class="sxs-lookup"><span data-stu-id="da52f-135">Deleted jobs aren't exported.</span></span> <span data-ttu-id="da52f-136">Подпапки содержат заявления кандидатов, подпапки для приложении заявлений кандидатов, а также пакеты предложений, если это применимо.</span><span class="sxs-lookup"><span data-stu-id="da52f-136">The sub-folders contain candidate applications, with sub-folders for candidate application attachments and offer packages, where applicable.</span></span> |
| <span data-ttu-id="da52f-137">Шаблоны вакансий</span><span class="sxs-lookup"><span data-stu-id="da52f-137">Job opening templates</span></span> | <span data-ttu-id="da52f-138">Шаблоны процесса работ, которые были настроены в среде.</span><span class="sxs-lookup"><span data-stu-id="da52f-138">Job process templates that were configured in the environment.</span></span> |
| <span data-ttu-id="da52f-139">Кадровые пулы</span><span class="sxs-lookup"><span data-stu-id="da52f-139">Talent pools</span></span> | <span data-ttu-id="da52f-140">Все созданные кадровые пулы, их списки участников и списки кандидатов для кадровых пулов.</span><span class="sxs-lookup"><span data-stu-id="da52f-140">All created talent pools, their contributors lists, and the candidates lists for the talent pools.</span></span> |
| <span data-ttu-id="da52f-141">Работники</span><span class="sxs-lookup"><span data-stu-id="da52f-141">Workers</span></span> | <span data-ttu-id="da52f-142">Список всех сотрудников, которые присутствуют в среде, и их роли.</span><span class="sxs-lookup"><span data-stu-id="da52f-142">List of all the workers who are present in the environment, plus their roles.</span></span> |
| <span data-ttu-id="da52f-143">(корневая папка)</span><span class="sxs-lookup"><span data-stu-id="da52f-143">(root folder)</span></span> | <span data-ttu-id="da52f-144">Файл схемы JSON, описывающий поля структуры данных.</span><span class="sxs-lookup"><span data-stu-id="da52f-144">A JSON schema file that describes the data structure fields.</span></span> |

### <a name="restrict-access-to-attract"></a><span data-ttu-id="da52f-145">Ограничение доступа для Attract</span><span class="sxs-lookup"><span data-stu-id="da52f-145">Restrict access to Attract</span></span>

<span data-ttu-id="da52f-146">Когда все готово для миграции, ограничьте доступ к среде Attract и экспортируйте данные.</span><span class="sxs-lookup"><span data-stu-id="da52f-146">When you're ready to migrate, restrict non-admins from accessing your Attract environment and export your data.</span></span>

>[!IMPORTANT]
><span data-ttu-id="da52f-147">Ограничение доступа к Attract необратимо и не может быть отменено.</span><span class="sxs-lookup"><span data-stu-id="da52f-147">Restricting access to your Attract environment is permanent and can't be undone.</span></span> <span data-ttu-id="da52f-148">Если вы хотите, чтобы пользователи, не являющиеся администраторами, продолжили доступ к среде, пропустите этот шаг.</span><span class="sxs-lookup"><span data-stu-id="da52f-148">If you want non-admin users to continue accessing your environment, skip this step.</span></span>

1. <span data-ttu-id="da52f-149">Перейдите на страницу [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span><span class="sxs-lookup"><span data-stu-id="da52f-149">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="da52f-150">Чтобы запретить неадминистраторам доступ к среде Attract, в **Ограничить доступ к этому приложению** выберите **Ограничить доступ**.</span><span class="sxs-lookup"><span data-stu-id="da52f-150">To restrict non-admins from accessing your Attract environment, under **Restrict access to this app**, select **Restrict access now**.</span></span> <span data-ttu-id="da52f-151">Ограничение доступа также отменяет разноску всех активных заданий, которые были разнесены.</span><span class="sxs-lookup"><span data-stu-id="da52f-151">Restricting access also unposts any active jobs that have been posted.</span></span>

   ![[<span data-ttu-id="da52f-152">Ограничение доступа для неадминистраторов Attract</span><span class="sxs-lookup"><span data-stu-id="da52f-152">Restrict non-admin access to Attract</span></span>](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. <span data-ttu-id="da52f-153">Когда появится предупреждение **Это необратимое изменение**, выберите **Ограничить доступ** для постоянного ограничения доступа пользователей, не являющихся администраторами, для этой среды.</span><span class="sxs-lookup"><span data-stu-id="da52f-153">When you see the warning **This is a permanent change**, select **Restrict access** to permanently restrict non-admin users from this environment.</span></span> <span data-ttu-id="da52f-154">Если вы не готовы выполнить этот шаг, нажмите **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="da52f-154">If you're not ready to complete this step, select **Cancel**.</span></span>

   ![[<span data-ttu-id="da52f-155">Предупреждение о том, что ограничение доступа является необратимым</span><span class="sxs-lookup"><span data-stu-id="da52f-155">Warning that restricting access is a permanent change</span></span>](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   ><span data-ttu-id="da52f-156">После ограничения доступа к среде Attract у администраторов может остаться доступ к страницам экспорта и отчетности по людям.</span><span class="sxs-lookup"><span data-stu-id="da52f-156">Admins can continue to access the data export and person report pages after you restrict access to the Attract environment.</span></span>

## <a name="export-data-from-onboard"></a><span data-ttu-id="da52f-157">Экспорт данных из Onboard</span><span class="sxs-lookup"><span data-stu-id="da52f-157">Export data from Onboard</span></span>

<span data-ttu-id="da52f-158">Когда вы будете готовы, вы можете загрузить шаблоны, руководства и данные кандидатов из Onboard.</span><span class="sxs-lookup"><span data-stu-id="da52f-158">When you're ready, you can download templates, guides, and candidate data from Onboard.</span></span>

1. <span data-ttu-id="da52f-159">Перейдите на страницу [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).</span><span class="sxs-lookup"><span data-stu-id="da52f-159">Go to [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).</span></span>

2. <span data-ttu-id="da52f-160">В разделе **Экспорт данных** выберите **Запрос на экспорт данных**.</span><span class="sxs-lookup"><span data-stu-id="da52f-160">Under **Data export**, select **Request a data export**.</span></span> 

   ![[<span data-ttu-id="da52f-161">Запрос на экспорт данных из Onboard</span><span class="sxs-lookup"><span data-stu-id="da52f-161">Request a data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. <span data-ttu-id="da52f-162">После появления окна сообщений **Ваш запрос обрабатывается** нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="da52f-162">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="da52f-163">Экспорт данных может занять до 20 минут в зависимости от размера экспорта.</span><span class="sxs-lookup"><span data-stu-id="da52f-163">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="da52f-164">После завершения экспорта нажмите кнопку **Загрузить** рядом.</span><span class="sxs-lookup"><span data-stu-id="da52f-164">When your export completes, select the **Download** button next to it.</span></span> 

   ![[<span data-ttu-id="da52f-165">Загрузка экспорта данных из Onboard</span><span class="sxs-lookup"><span data-stu-id="da52f-165">Download data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   ><span data-ttu-id="da52f-166">Экспорт данных доступен в течение семи дней.</span><span class="sxs-lookup"><span data-stu-id="da52f-166">Your data export is available for seven days.</span></span> <span data-ttu-id="da52f-167">Через семь дней истечет срок действия ссылки **Загрузить**, и если требуется снова загрузить данные, необходимо запросить новый экспорт.</span><span class="sxs-lookup"><span data-stu-id="da52f-167">After seven days, the **Download** link expires, and you must request a new export if you need to download your data again.</span></span> <span data-ttu-id="da52f-168">При начале нового экспорта данных срок всех существующих загрузок истекает после того, как новый экспорт будет завершен успешно.</span><span class="sxs-lookup"><span data-stu-id="da52f-168">When you start a new data export, any existing downloads will expire after the new export succeeds.</span></span>

<span data-ttu-id="da52f-169">Файл с расширением ZIP, содержащий:</span><span class="sxs-lookup"><span data-stu-id="da52f-169">The download is a .zip file that contains:</span></span>

- <span data-ttu-id="da52f-170">Папка **Шаблоны**, содержащая шаблоны Onboard в формате документов Word.</span><span class="sxs-lookup"><span data-stu-id="da52f-170">A **Templates** folder that contains your Onboard templates in Word document format.</span></span>

- <span data-ttu-id="da52f-171">Папка **Руководства**, содержащая руководства Onboard в формате документов Word.</span><span class="sxs-lookup"><span data-stu-id="da52f-171">A **Guides** folder that contains your Onboard guides in Word document format.</span></span>

## <a name="see-also"></a><span data-ttu-id="da52f-172">См. также</span><span class="sxs-lookup"><span data-stu-id="da52f-172">See also</span></span>

[<span data-ttu-id="da52f-173">Прекращение использования приложений Dynamics 365 Talent: Attract и Dynamics 365 Talent: Onboard</span><span class="sxs-lookup"><span data-stu-id="da52f-173">Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)