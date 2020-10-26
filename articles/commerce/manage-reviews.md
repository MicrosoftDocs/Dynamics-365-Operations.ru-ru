---
title: Управление оценками и отзывами
description: В этой теме объясняется, как управлять оценками и отзывами в конструкторе веб-сайтов Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 10/09/2020
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
ms.openlocfilehash: 3fc88bc5a5868dce7c0539bf3f0ddc5b751e7b75
ms.sourcegitcommit: 83ec80382bfeb693d5c5949b6f65296bd50eed12
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2020
ms.locfileid: "3974014"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="fe901-103">Управление оценками и отзывами</span><span class="sxs-lookup"><span data-stu-id="fe901-103">Manage ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fe901-104">В этой теме объясняется, как управлять оценками и отзывами в конструкторе веб-сайтов Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fe901-104">This topic explains how to manage ratings and reviews in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="fe901-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="fe901-105">Overview</span></span>

<span data-ttu-id="fe901-106">Dynamics 365 Commerce использует Microsoft Azure Cognitive Service для автоматической модерации текста отзыва с помощью редактирования нецензурных слов.</span><span class="sxs-lookup"><span data-stu-id="fe901-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="fe901-107">Кроме того, модераторы могут использовать конструктор веб-сайтов Dynamics 365 Commerce для выполнения следующих ручных задач:</span><span class="sxs-lookup"><span data-stu-id="fe901-107">In addition, moderators can use Dynamics 365 Commerce site builder to implement the following manual tasks:</span></span>

- <span data-ttu-id="fe901-108">Модерация отзывов путем ответа на них или их удаления.</span><span class="sxs-lookup"><span data-stu-id="fe901-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="fe901-109">Удаление отзывов клиентов по их запросу.</span><span class="sxs-lookup"><span data-stu-id="fe901-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="fe901-110">Массовый импорт данных оценок и отзывов для всех продуктов в шаблон Microsoft Power BI, чтобы можно было анализировать тенденции для оценок и отзывов.</span><span class="sxs-lookup"><span data-stu-id="fe901-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="fe901-111">Чтение отзыва</span><span class="sxs-lookup"><span data-stu-id="fe901-111">Read a review</span></span> 

<span data-ttu-id="fe901-112">Чтобы прочитать обзор в конфигураторе сайта Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fe901-112">To read to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="fe901-113">Выберите **Домашняя страница \> Отзывы \> Модерация**.</span><span class="sxs-lookup"><span data-stu-id="fe901-113">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="fe901-114">Используйте поле поиска в правом верхнем углу страницы, чтобы отфильтровать отзывы, которые отображаются, с помощью кода продукта, наименования продукта или текста отзыва.</span><span class="sxs-lookup"><span data-stu-id="fe901-114">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="fe901-115">Дополнительные фильтры позволяют ограничить отзывы по периоду, рейтингу, каналу или статусу проблемы (сняты, отправлен ответ или сообщено).</span><span class="sxs-lookup"><span data-stu-id="fe901-115">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Домашняя страница модерации](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="fe901-117">Ответ на отзыв</span><span class="sxs-lookup"><span data-stu-id="fe901-117">Respond to a review</span></span> 

<span data-ttu-id="fe901-118">Иногда клиенты, которые приобрели продукт, выражают свою удовлетворенность или неудовлетворенность, либо не понимают, как использовать продукт.</span><span class="sxs-lookup"><span data-stu-id="fe901-118">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="fe901-119">В качестве модератора можно опубликовать ответ на отзыв.</span><span class="sxs-lookup"><span data-stu-id="fe901-119">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="fe901-120">Этот ответ появляется вместе с отзывом на сайте.</span><span class="sxs-lookup"><span data-stu-id="fe901-120">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="fe901-121">Чтобы ответить на обзор в конфигураторе сайта Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fe901-121">To respond to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="fe901-122">Выберите **Домашняя страница \> Отзывы \> Модерация**.</span><span class="sxs-lookup"><span data-stu-id="fe901-122">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="fe901-123">Найдите и выберите отзыв, требующей ответа.</span><span class="sxs-lookup"><span data-stu-id="fe901-123">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="fe901-124">В области свойств справа выберите **Добавить ответ**.</span><span class="sxs-lookup"><span data-stu-id="fe901-124">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="fe901-125">Введите текст ответа и имя, которое должно отображаться для респондента.</span><span class="sxs-lookup"><span data-stu-id="fe901-125">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="fe901-126">Имя респондента по умолчанию — **Модератор**.</span><span class="sxs-lookup"><span data-stu-id="fe901-126">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="fe901-127">Закончив, выберите **Опубликовать ответ**.</span><span class="sxs-lookup"><span data-stu-id="fe901-127">When you've finished, select **Post response**.</span></span>

![Ответ на отзыв](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="fe901-129">Снятие отзыва</span><span class="sxs-lookup"><span data-stu-id="fe901-129">Take down a review</span></span> 

<span data-ttu-id="fe901-130">В некоторых случаях для модераторов имеется бизнес-обоснование, которое позволяет снимать отзывы клиентов.</span><span class="sxs-lookup"><span data-stu-id="fe901-130">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="fe901-131">Чтобы снять обзор в конфигураторе сайта Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fe901-131">To take down a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="fe901-132">Выберите **Домашняя страница \> Отзывы \> Модерация**.</span><span class="sxs-lookup"><span data-stu-id="fe901-132">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="fe901-133">Найдите и выберите отзыв, который необходимо снять.</span><span class="sxs-lookup"><span data-stu-id="fe901-133">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="fe901-134">В области свойств справа выберите причину снятия в пункте **Снять отзыв**, затем выберите **Снять**.</span><span class="sxs-lookup"><span data-stu-id="fe901-134">In the properties pane on the right, select a takedown reason under **Takedown Review**, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="fe901-135">Удаление отзывов клиентов по их запросу</span><span class="sxs-lookup"><span data-stu-id="fe901-135">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="fe901-136">Иногда клиенты хотят навсегда удалить свои данные оценок и отзывов с веб-сайта электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="fe901-136">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="fe901-137">Модератор, получивший запрос на удаление от клиента, может удалить данные клиента, используя функцию удаления отзыва.</span><span class="sxs-lookup"><span data-stu-id="fe901-137">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="fe901-138">Чтобы найти и удалить данные клиента, модератору необходим адрес электронной почты, который использовался клиентом для входа в систему и предоставления отзыва.</span><span class="sxs-lookup"><span data-stu-id="fe901-138">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="fe901-139">Чтобы найти и удалить данные о клиенте в конфигураторе сайта Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fe901-139">To find and delete customer data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="fe901-140">Выберите **Домашняя страница \> Отзывы \> Удалить**.</span><span class="sxs-lookup"><span data-stu-id="fe901-140">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="fe901-141">В поле **Поиск пользователей по адресу электронной почты** введите адрес электронной почты клиента, затем выберите **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="fe901-141">In the **Search for users by email address** box, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="fe901-142">Если у клиента имеются какие-либо действия отзывов (например, отправка отзывов, голосование о полезности отзывов других клиентов или комментарии к отзывам других клиентов), результаты отображаются.</span><span class="sxs-lookup"><span data-stu-id="fe901-142">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="fe901-143">Для каждого элемента имеется кнопка **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="fe901-143">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="fe901-144">Для каждого элемента, который необходимо удалить, выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="fe901-144">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="fe901-145">При появлении запроса на подтверждение выберите **Да**.</span><span class="sxs-lookup"><span data-stu-id="fe901-145">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Удаление данных клиента](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="fe901-147">Для полного удаления данных из системы может потребоваться до семи дней.</span><span class="sxs-lookup"><span data-stu-id="fe901-147">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="fe901-148">Модераторы должны уведомлять клиентов об этой задержке.</span><span class="sxs-lookup"><span data-stu-id="fe901-148">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="fe901-149">Если клиенты изменили свои имена в параметрах своей учетной записи, в результатах поиска могут отображаться несколько элементов.</span><span class="sxs-lookup"><span data-stu-id="fe901-149">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="fe901-150">В этом случае для полного удаления данных клиента модератор должен выбрать **Удалить** для каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="fe901-150">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="fe901-151">Загрузка данных оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="fe901-151">Download ratings and reviews data</span></span>

<span data-ttu-id="fe901-152">Конструктор сайтов Commerce позволяет модераторам массово импортировать данные оценок и отзывов, чтобы они могли анализировать тенденции.</span><span class="sxs-lookup"><span data-stu-id="fe901-152">Commerce site builder lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="fe901-153">Доступен шаблон Power BI, содержащий базовые метрики.</span><span class="sxs-lookup"><span data-stu-id="fe901-153">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="fe901-154">Модераторы могут использовать этот шаблон для подключения к массовому импорту данных и просмотра панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="fe901-154">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="fe901-155">Им не требуется создавать пользовательскую панель мониторинга.</span><span class="sxs-lookup"><span data-stu-id="fe901-155">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="fe901-156">Модераторы могут также настраивать шаблон Power BI в соответствии с конкретными потребностями.</span><span class="sxs-lookup"><span data-stu-id="fe901-156">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="fe901-157">Чтобы загрузить данные оценок и отзывов в конфигуратор сайта Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fe901-157">To download ratings and reviews data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="fe901-158">Выберите **Домашняя страница \> Отзывы \> Отчетность**.</span><span class="sxs-lookup"><span data-stu-id="fe901-158">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="fe901-159">Выберите **Загрузить данные отзывов** для массовой загрузки данных оценок и отзывов в формате значений с запятыми в качестве разделителей (CSV).</span><span class="sxs-lookup"><span data-stu-id="fe901-159">Select **Download review data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="fe901-160">Просмотр тенденций оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="fe901-160">View ratings and reviews trends</span></span>

<span data-ttu-id="fe901-161">Модераторы могут загрузить шаблон Power BI, чтобы они могли просматривать тенденции на панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="fe901-161">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="fe901-162">Чтобы просмотреть тенденции оценок и отзывов в конфигураторе сайта Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fe901-162">To view ratings and reviews trends in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="fe901-163">Выберите **Домашняя страница \> Отзывы \> Отчетность**.</span><span class="sxs-lookup"><span data-stu-id="fe901-163">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="fe901-164">Выберите **Шаблон PowerBI**, чтобы загрузить этот шаблон.</span><span class="sxs-lookup"><span data-stu-id="fe901-164">Select **PowerBI template** to download the template.</span></span>

    ![Загрузка шаблона Power BI](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="fe901-166">Откройте загруженный шаблон с помощью приложения Power BI.</span><span class="sxs-lookup"><span data-stu-id="fe901-166">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="fe901-167">Закройте диалоговое окно **Доступ к веб-содержимому**, затем закройте появившееся сообщение об ошибке "Обновить".</span><span class="sxs-lookup"><span data-stu-id="fe901-167">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="fe901-168">Перейдите на **Домашнюю страницу**, выберите **Изменить запросы**, затем выберите **Параметры источника данных**.</span><span class="sxs-lookup"><span data-stu-id="fe901-168">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="fe901-169">В диалоговом окне **Параметры источника данных** выберите **Изменить источник**.</span><span class="sxs-lookup"><span data-stu-id="fe901-169">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="fe901-170">В поле **URL** введите путь к данным отзыва, загруженным в ходе предыдущей процедуры (например, **c:\\reviews\\ReviewsData.csv**).</span><span class="sxs-lookup"><span data-stu-id="fe901-170">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![Поле URL в диалоговом окне значений с разделителями-запятыми](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="fe901-172">Выберите **OK**, затем выберите **Применить изменения**.</span><span class="sxs-lookup"><span data-stu-id="fe901-172">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="fe901-173">Применение изменений к источнику данных займет от одной до двух минут.</span><span class="sxs-lookup"><span data-stu-id="fe901-173">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="fe901-174">Выберите **Лист тенденций**, чтобы просмотреть тенденции оценок и отзывов.</span><span class="sxs-lookup"><span data-stu-id="fe901-174">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Тенденции оценок и отзывов](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="fe901-176">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="fe901-176">Additional resources</span></span>

[<span data-ttu-id="fe901-177">Обзор оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="fe901-177">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="fe901-178">Соглашение на использование оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="fe901-178">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="fe901-179">Настройка оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="fe901-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="fe901-180">Синхронизация оценок продуктов в Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="fe901-180">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
