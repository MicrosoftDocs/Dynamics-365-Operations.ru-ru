---
title: Управление оценками и отзывами
description: В этой теме объясняется, как управлять оценками и отзывами с помощью средства модерации оценок и отзывов в Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: e9becdce5ae36ac637043b9d0febfbbff2392aa9
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698034"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="62988-103">Управление оценками и отзывами</span><span class="sxs-lookup"><span data-stu-id="62988-103">Manage ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="62988-104">В этой теме объясняется, как управлять оценками и отзывами с помощью средства модерации оценок и отзывов в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="62988-104">This topic explains how to manage ratings and reviews by using the Microsoft Dynamics 365 Commerce ratings and reviews moderation tool.</span></span>

## <a name="overview"></a><span data-ttu-id="62988-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="62988-105">Overview</span></span>

<span data-ttu-id="62988-106">Dynamics 365 Commerce использует Microsoft Azure Cognitive Service для автоматической модерации текста отзыва с помощью редактирования нецензурных слов.</span><span class="sxs-lookup"><span data-stu-id="62988-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="62988-107">Кроме того, модераторы могут использовать средство модерации оценок и отзывов для следующих ручных задач:</span><span class="sxs-lookup"><span data-stu-id="62988-107">In addition, moderators can use the ratings and reviews moderation tool for the following manual tasks:</span></span>

- <span data-ttu-id="62988-108">Модерация отзывов путем ответа на них или их удаления.</span><span class="sxs-lookup"><span data-stu-id="62988-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="62988-109">Удаление отзывов клиентов по их запросу.</span><span class="sxs-lookup"><span data-stu-id="62988-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="62988-110">Массовый импорт данных оценок и отзывов для всех продуктов в шаблон Microsoft Power BI, чтобы можно было анализировать тенденции для оценок и отзывов.</span><span class="sxs-lookup"><span data-stu-id="62988-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="62988-111">Чтение отзыва</span><span class="sxs-lookup"><span data-stu-id="62988-111">Read a review</span></span> 

1. <span data-ttu-id="62988-112">Выберите **Домашняя страница \> Отзывы \> Модерация**.</span><span class="sxs-lookup"><span data-stu-id="62988-112">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="62988-113">Используйте поле поиска в правом верхнем углу страницы, чтобы отфильтровать отзывы, которые отображаются, с помощью кода продукта, наименования продукта или текста отзыва.</span><span class="sxs-lookup"><span data-stu-id="62988-113">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="62988-114">Дополнительные фильтры позволяют ограничить отзывы по периоду, рейтингу, каналу или статусу проблемы (сняты, отправлен ответ или сообщено).</span><span class="sxs-lookup"><span data-stu-id="62988-114">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Домашняя страница модерации](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="62988-116">Ответ на отзыв</span><span class="sxs-lookup"><span data-stu-id="62988-116">Respond to a review</span></span> 

<span data-ttu-id="62988-117">Иногда клиенты, которые приобрели продукт, выражают свою удовлетворенность или неудовлетворенность, либо не понимают, как использовать продукт.</span><span class="sxs-lookup"><span data-stu-id="62988-117">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="62988-118">В качестве модератора можно опубликовать ответ на отзыв.</span><span class="sxs-lookup"><span data-stu-id="62988-118">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="62988-119">Этот ответ появляется вместе с отзывом на сайте.</span><span class="sxs-lookup"><span data-stu-id="62988-119">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="62988-120">Чтобы ответить на отзыв, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="62988-120">To respond to a review, follow these steps.</span></span>

1. <span data-ttu-id="62988-121">Выберите **Домашняя страница \> Отзывы \> Модерация**.</span><span class="sxs-lookup"><span data-stu-id="62988-121">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="62988-122">Найдите и выберите отзыв, требующей ответа.</span><span class="sxs-lookup"><span data-stu-id="62988-122">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="62988-123">В области свойств справа выберите **Добавить ответ**.</span><span class="sxs-lookup"><span data-stu-id="62988-123">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="62988-124">Введите текст ответа и имя, которое должно отображаться для респондента.</span><span class="sxs-lookup"><span data-stu-id="62988-124">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="62988-125">Имя респондента по умолчанию — **Модератор**.</span><span class="sxs-lookup"><span data-stu-id="62988-125">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="62988-126">Закончив, выберите **Опубликовать ответ**.</span><span class="sxs-lookup"><span data-stu-id="62988-126">When you've finished, select **Post response**.</span></span>

![Ответ на отзыв](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="62988-128">Снятие отзыва</span><span class="sxs-lookup"><span data-stu-id="62988-128">Take down a review</span></span> 

<span data-ttu-id="62988-129">В некоторых случаях для модераторов имеется бизнес-обоснование, которое позволяет снимать отзывы клиентов.</span><span class="sxs-lookup"><span data-stu-id="62988-129">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="62988-130">Чтобы снять отзыв, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="62988-130">To take down a review, follow these steps.</span></span>

1. <span data-ttu-id="62988-131">Выберите **Домашняя страница \> Отзывы \> Модерация**.</span><span class="sxs-lookup"><span data-stu-id="62988-131">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="62988-132">Найдите и выберите отзыв, который необходимо снять.</span><span class="sxs-lookup"><span data-stu-id="62988-132">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="62988-133">В области свойств справа выберите причину снятия, затем выберите **Снять**.</span><span class="sxs-lookup"><span data-stu-id="62988-133">In the properties pane on the right, select a takedown reason, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="62988-134">Удаление отзывов клиентов по их запросу</span><span class="sxs-lookup"><span data-stu-id="62988-134">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="62988-135">Иногда клиенты хотят навсегда удалить свои данные оценок и отзывов с веб-сайта электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="62988-135">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="62988-136">Модератор, получивший запрос на удаление от клиента, может удалить данные клиента, используя функцию удаления отзыва.</span><span class="sxs-lookup"><span data-stu-id="62988-136">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="62988-137">Чтобы найти и удалить данные клиента, модератору необходим адрес электронной почты, который использовался клиентом для входа в систему и предоставления отзыва.</span><span class="sxs-lookup"><span data-stu-id="62988-137">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="62988-138">Чтобы найти и удалить данные клиента, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="62988-138">To find and delete customer data, follow these steps.</span></span>

1. <span data-ttu-id="62988-139">Выберите **Домашняя страница \> Отзывы \> Удалить**.</span><span class="sxs-lookup"><span data-stu-id="62988-139">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="62988-140">В поле **Поиск пользователей по адресу электронной почты** введите адрес электронной почты клиента, затем выберите **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="62988-140">In the **Search for users by email address** field, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="62988-141">Если у клиента имеются какие-либо действия отзывов (например, отправка отзывов, голосование о полезности отзывов других клиентов или комментарии к отзывам других клиентов), результаты отображаются.</span><span class="sxs-lookup"><span data-stu-id="62988-141">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="62988-142">Для каждого элемента имеется кнопка **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="62988-142">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="62988-143">Для каждого элемента, который необходимо удалить, выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="62988-143">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="62988-144">При появлении запроса на подтверждение выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="62988-144">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Удаление данных клиента](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="62988-146">Для полного удаления данных из системы может потребоваться до семи дней.</span><span class="sxs-lookup"><span data-stu-id="62988-146">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="62988-147">Модераторы должны уведомлять клиентов об этой задержке.</span><span class="sxs-lookup"><span data-stu-id="62988-147">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="62988-148">Если клиенты изменили свои имена в параметрах своей учетной записи, в результатах поиска могут отображаться несколько элементов.</span><span class="sxs-lookup"><span data-stu-id="62988-148">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="62988-149">В этом случае для полного удаления данных клиента модератор должен выбрать **Удалить** для каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="62988-149">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="62988-150">Загрузка данных оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="62988-150">Download ratings and reviews data</span></span>

<span data-ttu-id="62988-151">Средство модерирования оценок и отзывов позволяет модераторам массово импортировать данные оценок и отзывов, чтобы они могли анализировать тенденции.</span><span class="sxs-lookup"><span data-stu-id="62988-151">The ratings and reviews moderation tool lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="62988-152">Доступен шаблон Power BI, содержащий базовые метрики.</span><span class="sxs-lookup"><span data-stu-id="62988-152">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="62988-153">Модераторы могут использовать этот шаблон для подключения к массовому импорту данных и просмотра панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="62988-153">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="62988-154">Им не требуется создавать пользовательскую панель мониторинга.</span><span class="sxs-lookup"><span data-stu-id="62988-154">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="62988-155">Модераторы могут также настраивать шаблон Power BI в соответствии с конкретными потребностями.</span><span class="sxs-lookup"><span data-stu-id="62988-155">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="62988-156">Чтобы загрузить данные рейтингов и отзывов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="62988-156">To download ratings and reviews data, follow these steps.</span></span>

1. <span data-ttu-id="62988-157">Выберите **Домашняя страница \> Отзывы \> Отчетность**.</span><span class="sxs-lookup"><span data-stu-id="62988-157">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="62988-158">Выберите **Загрузить данные отзывов** для массовой загрузки данных оценок и отзывов в формате значений с запятыми в качестве разделителей (CSV).</span><span class="sxs-lookup"><span data-stu-id="62988-158">Select **Download reviews data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="62988-159">Просмотр тенденций оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="62988-159">View ratings and reviews trends</span></span>

<span data-ttu-id="62988-160">Модераторы могут загрузить шаблон Power BI, чтобы они могли просматривать тенденции на панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="62988-160">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="62988-161">Чтобы просмотреть тенденции рейтингов и отзывов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="62988-161">To view ratings and reviews trends, follow these steps.</span></span>

1. <span data-ttu-id="62988-162">Выберите **Домашняя страница \> Отзывы \> Отчетность**.</span><span class="sxs-lookup"><span data-stu-id="62988-162">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="62988-163">Выберите **Шаблон PowerBI**, чтобы загрузить этот шаблон.</span><span class="sxs-lookup"><span data-stu-id="62988-163">Select **PowerBI template** to download the template.</span></span>

    ![Загрузка шаблона Power BI](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="62988-165">Откройте загруженный шаблон с помощью приложения Power BI.</span><span class="sxs-lookup"><span data-stu-id="62988-165">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="62988-166">Закройте диалоговое окно **Доступ к веб-содержимому**, затем закройте появившееся сообщение об ошибке "Обновить".</span><span class="sxs-lookup"><span data-stu-id="62988-166">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="62988-167">Перейдите на **Домашнюю страницу**, выберите **Изменить запросы**, затем выберите **Параметры источника данных**.</span><span class="sxs-lookup"><span data-stu-id="62988-167">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="62988-168">В диалоговом окне **Параметры источника данных** выберите **Изменить источник**.</span><span class="sxs-lookup"><span data-stu-id="62988-168">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="62988-169">В поле **URL** введите путь к данным отзыва, загруженным в ходе предыдущей процедуры (например, **c:\\reviews\\ReviewsData.csv**).</span><span class="sxs-lookup"><span data-stu-id="62988-169">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![Поле URL в диалоговом окне значений с разделителями-запятыми](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="62988-171">Выберите **OK**, затем выберите **Применить изменения**.</span><span class="sxs-lookup"><span data-stu-id="62988-171">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="62988-172">Применение изменений к источнику данных займет от одной до двух минут.</span><span class="sxs-lookup"><span data-stu-id="62988-172">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="62988-173">Выберите **Лист тенденций**, чтобы просмотреть тенденции оценок и отзывов.</span><span class="sxs-lookup"><span data-stu-id="62988-173">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Тенденции оценок и отзывов](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="62988-175">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="62988-175">Additional resources</span></span>

[<span data-ttu-id="62988-176">Обзор оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="62988-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="62988-177">Соглашение на использование оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="62988-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="62988-178">Настройка оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="62988-178">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="62988-179">Синхронизация оценок продуктов в Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="62988-179">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
