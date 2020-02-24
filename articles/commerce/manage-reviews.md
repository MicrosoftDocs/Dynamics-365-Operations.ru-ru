---
title: Управление оценками и отзывами
description: В этой теме объясняется, как управлять оценками и отзывами с помощью средства модерации оценок и отзывов в Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a7fa2ae3124a0a68b3890987c5dce2730e5c2183
ms.sourcegitcommit: 1e6c8163da5818196769eb278afb3a2335d0cbe3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027250"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="b9f1a-103">Управление оценками и отзывами</span><span class="sxs-lookup"><span data-stu-id="b9f1a-103">Manage ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b9f1a-104">В этой теме объясняется, как управлять оценками и отзывами с помощью средства модерации оценок и отзывов в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-104">This topic explains how to manage ratings and reviews by using the Microsoft Dynamics 365 Commerce ratings and reviews moderation tool.</span></span>

## <a name="overview"></a><span data-ttu-id="b9f1a-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="b9f1a-105">Overview</span></span>

<span data-ttu-id="b9f1a-106">Dynamics 365 Commerce использует Microsoft Azure Cognitive Service для автоматической модерации текста отзыва с помощью редактирования нецензурных слов.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="b9f1a-107">Кроме того, модераторы могут использовать средство модерации оценок и отзывов для следующих ручных задач:</span><span class="sxs-lookup"><span data-stu-id="b9f1a-107">In addition, moderators can use the ratings and reviews moderation tool for the following manual tasks:</span></span>

- <span data-ttu-id="b9f1a-108">Модерация отзывов путем ответа на них или их удаления.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="b9f1a-109">Удаление отзывов клиентов по их запросу.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="b9f1a-110">Массовый импорт данных оценок и отзывов для всех продуктов в шаблон Microsoft Power BI, чтобы можно было анализировать тенденции для оценок и отзывов.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="access-ratings-and-reviews-moderation-features"></a><span data-ttu-id="b9f1a-111">Доступ функциям модерации оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="b9f1a-111">Access ratings and reviews moderation features</span></span>

<span data-ttu-id="b9f1a-112">Чтобы получить доступ к оценкам и отзывам в средстве управления электронной коммерцией, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-112">To access ratings and reviews moderation features in the e-Commerce site management tool, follow these steps.</span></span>

1. <span data-ttu-id="b9f1a-113">Выполните вход [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="b9f1a-113">Sign in to [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="b9f1a-114">Откройте проект, содержащий среду, в которой необходимо инициализировать электронную коммерцию.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-114">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="b9f1a-115">В разделе **Среды** выберите среду.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-115">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="b9f1a-116">В **Компоненты среды** выберите **Управление розничной торговлей**.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-116">Under **Environment features**, select **Retail manage**.</span></span>
1. <span data-ttu-id="b9f1a-117">На вкладке **Электронная коммерция** в **Ссылки** выберите **Средство управления сайтом электронной коммерции**.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-117">On the **e-Commerce** tab under **Links**, select **e-Commerce Site management tool**.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="b9f1a-118">Чтение отзыва</span><span class="sxs-lookup"><span data-stu-id="b9f1a-118">Read a review</span></span> 

1. <span data-ttu-id="b9f1a-119">Выберите **Домашняя страница \> Отзывы \> Модерация**.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-119">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="b9f1a-120">Используйте поле поиска в правом верхнем углу страницы, чтобы отфильтровать отзывы, которые отображаются, с помощью кода продукта, наименования продукта или текста отзыва.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-120">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="b9f1a-121">Дополнительные фильтры позволяют ограничить отзывы по периоду, рейтингу, каналу или статусу проблемы (сняты, отправлен ответ или сообщено).</span><span class="sxs-lookup"><span data-stu-id="b9f1a-121">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Домашняя страница модерации](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="b9f1a-123">Ответ на отзыв</span><span class="sxs-lookup"><span data-stu-id="b9f1a-123">Respond to a review</span></span> 

<span data-ttu-id="b9f1a-124">Иногда клиенты, которые приобрели продукт, выражают свою удовлетворенность или неудовлетворенность, либо не понимают, как использовать продукт.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-124">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="b9f1a-125">В качестве модератора можно опубликовать ответ на отзыв.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-125">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="b9f1a-126">Этот ответ появляется вместе с отзывом на сайте.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-126">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="b9f1a-127">Чтобы ответить на отзыв, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-127">To respond to a review, follow these steps.</span></span>

1. <span data-ttu-id="b9f1a-128">Выберите **Домашняя страница \> Отзывы \> Модерация**.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-128">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="b9f1a-129">Найдите и выберите отзыв, требующей ответа.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-129">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="b9f1a-130">В области свойств справа выберите **Добавить ответ**.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-130">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="b9f1a-131">Введите текст ответа и имя, которое должно отображаться для респондента.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-131">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="b9f1a-132">Имя респондента по умолчанию — **Модератор**.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-132">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="b9f1a-133">Закончив, выберите **Опубликовать ответ**.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-133">When you've finished, select **Post response**.</span></span>

![Ответ на отзыв](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="b9f1a-135">Снятие отзыва</span><span class="sxs-lookup"><span data-stu-id="b9f1a-135">Take down a review</span></span> 

<span data-ttu-id="b9f1a-136">В некоторых случаях для модераторов имеется бизнес-обоснование, которое позволяет снимать отзывы клиентов.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-136">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="b9f1a-137">Чтобы снять отзыв, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-137">To take down a review, follow these steps.</span></span>

1. <span data-ttu-id="b9f1a-138">Выберите **Домашняя страница \> Отзывы \> Модерация**.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-138">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="b9f1a-139">Найдите и выберите отзыв, который необходимо снять.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-139">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="b9f1a-140">В области свойств справа выберите причину снятия, затем выберите **Снять**.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-140">In the properties pane on the right, select a takedown reason, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="b9f1a-141">Удаление отзывов клиентов по их запросу</span><span class="sxs-lookup"><span data-stu-id="b9f1a-141">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="b9f1a-142">Иногда клиенты хотят навсегда удалить свои данные оценок и отзывов с веб-сайта электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-142">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="b9f1a-143">Модератор, получивший запрос на удаление от клиента, может удалить данные клиента, используя функцию удаления отзыва.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-143">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="b9f1a-144">Чтобы найти и удалить данные клиента, модератору необходим адрес электронной почты, который использовался клиентом для входа в систему и предоставления отзыва.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-144">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="b9f1a-145">Чтобы найти и удалить данные клиента, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-145">To find and delete customer data, follow these steps.</span></span>

1. <span data-ttu-id="b9f1a-146">Выберите **Домашняя страница \> Отзывы \> Удалить**.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-146">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="b9f1a-147">В поле **Поиск пользователей по адресу электронной почты** введите адрес электронной почты клиента, затем выберите **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-147">In the **Search for users by email address** field, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="b9f1a-148">Если у клиента имеются какие-либо действия отзывов (например, отправка отзывов, голосование о полезности отзывов других клиентов или комментарии к отзывам других клиентов), результаты отображаются.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-148">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="b9f1a-149">Для каждого элемента имеется кнопка **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-149">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="b9f1a-150">Для каждого элемента, который необходимо удалить, выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-150">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="b9f1a-151">При появлении запроса на подтверждение выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-151">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Удаление данных клиента](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="b9f1a-153">Для полного удаления данных из системы может потребоваться до семи дней.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-153">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="b9f1a-154">Модераторы должны уведомлять клиентов об этой задержке.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-154">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="b9f1a-155">Если клиенты изменили свои имена в параметрах своей учетной записи, в результатах поиска могут отображаться несколько элементов.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-155">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="b9f1a-156">В этом случае для полного удаления данных клиента модератор должен выбрать **Удалить** для каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-156">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="b9f1a-157">Загрузка данных оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="b9f1a-157">Download ratings and reviews data</span></span>

<span data-ttu-id="b9f1a-158">Средство модерирования оценок и отзывов позволяет модераторам массово импортировать данные оценок и отзывов, чтобы они могли анализировать тенденции.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-158">The ratings and reviews moderation tool lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="b9f1a-159">Доступен шаблон Power BI, содержащий базовые метрики.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-159">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="b9f1a-160">Модераторы могут использовать этот шаблон для подключения к массовому импорту данных и просмотра панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-160">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="b9f1a-161">Им не требуется создавать пользовательскую панель мониторинга.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-161">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="b9f1a-162">Модераторы могут также настраивать шаблон Power BI в соответствии с конкретными потребностями.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-162">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="b9f1a-163">Чтобы загрузить данные рейтингов и отзывов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-163">To download ratings and reviews data, follow these steps.</span></span>

1. <span data-ttu-id="b9f1a-164">Выберите **Домашняя страница \> Отзывы \> Отчетность**.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-164">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="b9f1a-165">Выберите **Загрузить данные отзывов** для массовой загрузки данных оценок и отзывов в формате значений с запятыми в качестве разделителей (CSV).</span><span class="sxs-lookup"><span data-stu-id="b9f1a-165">Select **Download reviews data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="b9f1a-166">Просмотр тенденций оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="b9f1a-166">View ratings and reviews trends</span></span>

<span data-ttu-id="b9f1a-167">Модераторы могут загрузить шаблон Power BI, чтобы они могли просматривать тенденции на панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-167">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="b9f1a-168">Чтобы просмотреть тенденции рейтингов и отзывов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-168">To view ratings and reviews trends, follow these steps.</span></span>

1. <span data-ttu-id="b9f1a-169">Выберите **Домашняя страница \> Отзывы \> Отчетность**.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-169">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="b9f1a-170">Выберите **Шаблон PowerBI**, чтобы загрузить этот шаблон.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-170">Select **PowerBI template** to download the template.</span></span>

    ![Загрузка шаблона Power BI](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="b9f1a-172">Откройте загруженный шаблон с помощью приложения Power BI.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-172">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="b9f1a-173">Закройте диалоговое окно **Доступ к веб-содержимому**, затем закройте появившееся сообщение об ошибке "Обновить".</span><span class="sxs-lookup"><span data-stu-id="b9f1a-173">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="b9f1a-174">Перейдите на **Домашнюю страницу**, выберите **Изменить запросы**, затем выберите **Параметры источника данных**.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-174">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="b9f1a-175">В диалоговом окне **Параметры источника данных** выберите **Изменить источник**.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-175">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="b9f1a-176">В поле **URL** введите путь к данным отзыва, загруженным в ходе предыдущей процедуры (например, **c:\\reviews\\ReviewsData.csv**).</span><span class="sxs-lookup"><span data-stu-id="b9f1a-176">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![Поле URL в диалоговом окне значений с разделителями-запятыми](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="b9f1a-178">Выберите **OK**, затем выберите **Применить изменения**.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-178">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="b9f1a-179">Применение изменений к источнику данных займет от одной до двух минут.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-179">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="b9f1a-180">Выберите **Лист тенденций**, чтобы просмотреть тенденции оценок и отзывов.</span><span class="sxs-lookup"><span data-stu-id="b9f1a-180">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Тенденции оценок и отзывов](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="b9f1a-182">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b9f1a-182">Additional resources</span></span>

[<span data-ttu-id="b9f1a-183">Обзор оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="b9f1a-183">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="b9f1a-184">Соглашение на использование оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="b9f1a-184">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="b9f1a-185">Настройка оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="b9f1a-185">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="b9f1a-186">Синхронизация оценок продуктов в Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="b9f1a-186">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
