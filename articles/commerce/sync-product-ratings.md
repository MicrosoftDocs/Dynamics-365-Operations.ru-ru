---
title: Синхронизация оценок продуктов в Dynamics 365 Commerce
description: В этом разделе описывается синхронизация оценок продуктов в Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1ab6de4bfa619df74bafc5511affddd516bdb34f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260317"
---
# <a name="sync-product-ratings-in-dynamics-365-commerce"></a><span data-ttu-id="d55f5-103">Синхронизация оценок продуктов в Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d55f5-103">Sync product ratings in Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d55f5-104">В этом разделе описывается синхронизация оценок продуктов в Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d55f5-104">This topic describes how to sync product ratings in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d55f5-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="d55f5-105">Overview</span></span>

<span data-ttu-id="d55f5-106">Для использования оценок продуктов в омниканалах, таких как POS-терминалы и центры обработки вызовов, необходимо импортировать оценки продуктов из службы оценок и отзывов в базу данных канала Commerce.</span><span class="sxs-lookup"><span data-stu-id="d55f5-106">To consume product ratings in omnichannels, such as at the point of sale (POS) and in call centers, product ratings from the ratings and reviews service must be imported into the Commerce channel database.</span></span> <span data-ttu-id="d55f5-107">Когда оценки продукта доступны в омниканалах, они могут помочь клиентам косвенным образом в ходе их взаимодействия с продавцами-консультантами.</span><span class="sxs-lookup"><span data-stu-id="d55f5-107">When product ratings are made available in omnichannels, they can help customers indirectly during their interactions with sales associates.</span></span>

<span data-ttu-id="d55f5-108">Данный раздел описывает следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="d55f5-108">This topic describes following tasks:</span></span>

1. <span data-ttu-id="d55f5-109">Настройте **Задание синхронизации оценок продукта** как пакетное задание для синхронизации оценок продуктов в **службе оценок и отзывов**.</span><span class="sxs-lookup"><span data-stu-id="d55f5-109">Configure **Product ratings sync job** as a batch job to synchronize product ratings from the **Ratings and Reviews service**.</span></span>
1. <span data-ttu-id="d55f5-110">Проверка того, что пакетное задание для синхронизации оценок продукта прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="d55f5-110">Verify that the batch job for product rating synchronization was successful.</span></span>
1. <span data-ttu-id="d55f5-111">Обеспечение доступности оценок продукта на POS-терминале.</span><span class="sxs-lookup"><span data-stu-id="d55f5-111">Make product ratings available at the POS.</span></span>

## <a name="configure-a-batch-job-to-synchronize-product-ratings"></a><span data-ttu-id="d55f5-112">Настройка пакетного задания для синхронизации оценок продуктов</span><span class="sxs-lookup"><span data-stu-id="d55f5-112">Configure a batch job to synchronize product ratings</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d55f5-113">Прежде чем начать, убедитесь, что установлена версия Dynamics 365 Commerce 10.0.6 или более поздняя.</span><span class="sxs-lookup"><span data-stu-id="d55f5-113">Before you start, make sure that version 10.0.6 or later of Dynamics 365 Commerce is installed.</span></span>

### <a name="initialize-the-commerce-scheduler"></a><span data-ttu-id="d55f5-114">Инициализация планировщика Commerce</span><span class="sxs-lookup"><span data-stu-id="d55f5-114">Initialize the commerce scheduler</span></span>

<span data-ttu-id="d55f5-115">Чтобы инициализировать планировщик Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d55f5-115">To initialize the commerce scheduler, follow these steps.</span></span>

1. <span data-ttu-id="d55f5-116">Перейдите к **Retail и Commerce \> Настройка Headquarters \> Планировщик Commerce \> Инициализация планировщика Commerce**.</span><span class="sxs-lookup"><span data-stu-id="d55f5-116">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Initialize commerce scheduler**.</span></span> <span data-ttu-id="d55f5-117">Либо выполните поиск "Инициализация планировщика Commerce".</span><span class="sxs-lookup"><span data-stu-id="d55f5-117">Alternatively, search for "Initialize commerce scheduler."</span></span>
1. <span data-ttu-id="d55f5-118">В диалоговом окне **Инициализация планировщика Commerce** убедитесь, что параметр **Удалить существующую конфигурацию** имеет значение **Нет**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d55f5-118">In the **Initialize commerce scheduler** dialog box, make sure that the **Delete existing configuration** option is set to **No**, and then select **OK**.</span></span>

### <a name="verify-the-retailproductrating-subjob"></a><span data-ttu-id="d55f5-119">Проверка подзадания RetailProductRating</span><span class="sxs-lookup"><span data-stu-id="d55f5-119">Verify the RetailProductRating subjob</span></span>

<span data-ttu-id="d55f5-120">Чтобы убедиться в наличии подзадания **RetailProductRating**, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d55f5-120">To verify that the **RetailProductRating** subjob exists, follow these steps.</span></span>

1. <span data-ttu-id="d55f5-121">Перейдите к **Retail и Commerce \> Настройка Headquarters \> Планировщик Commerce \> Подзадания планировщика**.</span><span class="sxs-lookup"><span data-stu-id="d55f5-121">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Scheduler subjobs**.</span></span> <span data-ttu-id="d55f5-122">Или выполните поиск "Подзадания планировщика".</span><span class="sxs-lookup"><span data-stu-id="d55f5-122">Alternatively, search for "Scheduler subjobs."</span></span>
1. <span data-ttu-id="d55f5-123">В списке подзаданий найдите или выполните поиск подзадания **RetailProductRating**.</span><span class="sxs-lookup"><span data-stu-id="d55f5-123">In the subjob list, find or search for the **RetailProductRating** subjob.</span></span>

<span data-ttu-id="d55f5-124">На следующем рисунке показан пример сведений о подзаданиях в Commerce.</span><span class="sxs-lookup"><span data-stu-id="d55f5-124">The following illustration shows an example of the subjob details in Commerce.</span></span>

![Сведения о подзадании RetailProductRating](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> <span data-ttu-id="d55f5-126">Если подзадание **RetailProductRating** не удается найти, возможно, вы уже запустили задание **Синхронизация оценок продуктов** и задание **1040 CDX** перед инициализацией планировщика Commerce.</span><span class="sxs-lookup"><span data-stu-id="d55f5-126">If you don't find the **RetailProductRating** subjob, you might already have run the **Sync product ratings** job and the **1040 CDX** job before you initialized the Commerce scheduler.</span></span> <span data-ttu-id="d55f5-127">В этом случае выполните следующие шаги, чтобы выполнить задание **Полная синхронизация данных**.</span><span class="sxs-lookup"><span data-stu-id="d55f5-127">In this case, follow these steps to run the **Full data sync** job.</span></span>

> 1. <span data-ttu-id="d55f5-128">Перейдите к **Retail и Commerce \> Настройка Headquarters \> Планировщик Commerce \> База данных канала**.</span><span class="sxs-lookup"><span data-stu-id="d55f5-128">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span> <span data-ttu-id="d55f5-129">Или же выполните поиск по словам "База данных канала".</span><span class="sxs-lookup"><span data-stu-id="d55f5-129">Alternatively, search for "Channel database."</span></span>
> 1. <span data-ttu-id="d55f5-130">Выберите базу данных канала для синхронизации.</span><span class="sxs-lookup"><span data-stu-id="d55f5-130">Select the channel database to sync.</span></span>
> 1. <span data-ttu-id="d55f5-131">На панели операций выберите **Полная синхронизация данных**.</span><span class="sxs-lookup"><span data-stu-id="d55f5-131">On the action pane, select **Full data sync**.</span></span>
> 1. <span data-ttu-id="d55f5-132">В раскрывающемся диалоговом окне **Выбор графика распределения** выберите **1040 — продукты**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d55f5-132">In the **Select a distribution schedule** drop-down dialog box, select **1040 - products**, and then select **OK**.</span></span>
> 1. <span data-ttu-id="d55f5-133">Повторите шаги предыдущей процедуры для проверки создания подзадания **RetailProductRating**.</span><span class="sxs-lookup"><span data-stu-id="d55f5-133">Repeat the steps of the previous procedure to verify that the **RetailProductRating** subjob has been created.</span></span>

### <a name="import-product-ratings"></a><span data-ttu-id="d55f5-134">Импорт оценок продуктов</span><span class="sxs-lookup"><span data-stu-id="d55f5-134">Import product ratings</span></span>

<span data-ttu-id="d55f5-135">Чтобы импортировать оценки продуктов в Commerce из службы оценок и отзывов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d55f5-135">To import product ratings into Commerce from the ratings and reviews service, follow these steps.</span></span>

1. <span data-ttu-id="d55f5-136">Перейдите в **Retail и Commerce \> Настройка Headquarters \> Планировщик Commerce \> Задание синхронизации оценок продуктов**.</span><span class="sxs-lookup"><span data-stu-id="d55f5-136">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Sync product ratings job**.</span></span> <span data-ttu-id="d55f5-137">Или выполните поиск по запросу "Задание синхронизации оценок продуктов".</span><span class="sxs-lookup"><span data-stu-id="d55f5-137">Alternatively, search for "Sync product ratings job."</span></span>
1. <span data-ttu-id="d55f5-138">В диалоговом окне **Извлечь оценки продуктов** на экспресс-вкладке **Выполнять в фоновом режиме** выберите **Повторение**.</span><span class="sxs-lookup"><span data-stu-id="d55f5-138">In the **Pull product ratings** dialog box, on the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="d55f5-139">В диалоговом окне **Определение повторения** настройте шаблон повторения.</span><span class="sxs-lookup"><span data-stu-id="d55f5-139">In the **Define recurrence** dialog box, set up a recurrence pattern.</span></span> <span data-ttu-id="d55f5-140">(Предлагаемое значение — 2 часа.) Не планируйте повторение, которое меньше одного часа.</span><span class="sxs-lookup"><span data-stu-id="d55f5-140">(The suggested value is two hours.) Don't schedule a recurrence that is less than one hour.</span></span>
1. <span data-ttu-id="d55f5-141">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d55f5-141">Select **OK**.</span></span>
1. <span data-ttu-id="d55f5-142">Установите для параметра **Процесс пакетной обработки** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="d55f5-142">Set the **Batch process** option to **Yes**.</span></span> <span data-ttu-id="d55f5-143">Эта настройка гарантирует, что можно будет выполнять аудит журналов и проверять статус запуска пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="d55f5-143">This setting helps guarantee that you will be able to audit the logs and verify the status of batch job runs.</span></span>
1. <span data-ttu-id="d55f5-144">Выберите **ОК**, чтобы запланировать пакетное задание.</span><span class="sxs-lookup"><span data-stu-id="d55f5-144">Select **OK** to schedule the batch job.</span></span>

<span data-ttu-id="d55f5-145">На следующем рисунке показан пример конфигурации пакетного задания в Commerce.</span><span class="sxs-lookup"><span data-stu-id="d55f5-145">The following illustration shows an example of batch job configuration in Commerce.</span></span>

![Конфигурация пакетного задания синхронизации оценок продуктов](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a><span data-ttu-id="d55f5-147">Проверка того, что пакетное задание для синхронизации оценок продукта прошло успешно</span><span class="sxs-lookup"><span data-stu-id="d55f5-147">Verify that the batch job for product rating synchronization was successful</span></span>

<span data-ttu-id="d55f5-148">Чтобы убедиться, что пакетное задание **Синхронизация оценок продуктов** прошло успешно, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d55f5-148">To verify that the **Sync product ratings** batch job was successful, follow these steps.</span></span>

1. <span data-ttu-id="d55f5-149">Откройте **Retail и Commerce \> Системный администратор \> Запросы \> Пакетные задания** или, если используется только единица складского хранения (SKU) Commerce, выберите **Retail и Commerce \> Запросы и отчеты \> Пакетные задания**.</span><span class="sxs-lookup"><span data-stu-id="d55f5-149">Go to **Retail and Commerce \> System administrator \> Inquiries \> Batch jobs** or, if you're using a Commerce-only stock keeping unit (SKU), **Retail and Commerce \> Inquiries and reports \> Batch jobs** instead.</span></span> <span data-ttu-id="d55f5-150">Или выполните поиск по словам "Пакетные задания".</span><span class="sxs-lookup"><span data-stu-id="d55f5-150">Alternatively, search for "Batch jobs."</span></span>
1. <span data-ttu-id="d55f5-151">Чтобы просмотреть сведения о пакетном задании, в списке пакетных заданий в столбце **Описание задания** выполните поиск описания, которое содержит слова "Извлечение оценок продуктов".</span><span class="sxs-lookup"><span data-stu-id="d55f5-151">To view the details of the batch job, in the batch job list, in the **Job description** column, search for a description that contains "Pull product ratings."</span></span>
1. <span data-ttu-id="d55f5-152">Выберите код задания, чтобы просмотреть сведения о пакетном задании, такие как запланированные начальные даты и время и текст повторения.</span><span class="sxs-lookup"><span data-stu-id="d55f5-152">Select the job ID to view the batch job details, such as the scheduled start date/time and the recurrence text.</span></span>

<span data-ttu-id="d55f5-153">На следующем рисунке показан пример сведений пакетного задания в Commerce, когда запланировано выполнение пакетного задания с интервалом два часа.</span><span class="sxs-lookup"><span data-stu-id="d55f5-153">The following illustration shows an example of the batch job details in Commerce when the batch job is scheduled to run at two-hour intervals.</span></span>

![Сведения о пакетном задании синхронизации оценки продукта](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a><span data-ttu-id="d55f5-155">Обеспечение доступности оценок продукта на POS-терминале</span><span class="sxs-lookup"><span data-stu-id="d55f5-155">Make product ratings available at the POS</span></span>

<span data-ttu-id="d55f5-156">Решение оценок и отзывов в Dynamics 365 Commerce является омниканальным решением.</span><span class="sxs-lookup"><span data-stu-id="d55f5-156">The ratings and reviews solution in Dynamics 365 Commerce is an omnichannel solution.</span></span> <span data-ttu-id="d55f5-157">Однако по умолчанию оценки продуктов не отображаются на POS-терминале.</span><span class="sxs-lookup"><span data-stu-id="d55f5-157">However, products ratings aren't shown at the POS by default.</span></span> <span data-ttu-id="d55f5-158">Чтобы помочь клиентам в магазинах просматривать оценки и отзывы, когда им помогают торговые консультанты, необходимо включить рейтинги продуктов на POS-терминале.</span><span class="sxs-lookup"><span data-stu-id="d55f5-158">To help customers in stores see ratings and reviews when they are being helped by sales associates, you must turn on product ratings at the POS.</span></span>

<span data-ttu-id="d55f5-159">Чтобы включить рейтинги продуктов в POS-терминале, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d55f5-159">To turn on product ratings at the POS, follow these steps.</span></span>

1. <span data-ttu-id="d55f5-160">Перейдите в раздел **Retail и Commerce \> Настройка Commerce \> Параметры \> Параметры Commerce**.</span><span class="sxs-lookup"><span data-stu-id="d55f5-160">Go to **Retail and Commerce \> Commerce setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="d55f5-161">Или выполните поиск "Параметры Commerce".</span><span class="sxs-lookup"><span data-stu-id="d55f5-161">Alternatively, search for "Commerce parameters."</span></span>
1. <span data-ttu-id="d55f5-162">На вкладке **Параметры конфигурации** выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="d55f5-162">On the **Configuration parameters** tab, select **New**.</span></span>
1. <span data-ttu-id="d55f5-163">Введите имя, например **RatingsAndReviews.EnableProductRatingsForRetailStores**, и установите значение **true**.</span><span class="sxs-lookup"><span data-stu-id="d55f5-163">Enter a name such as **RatingsAndReviews.EnableProductRatingsForRetailStores**, and set the value to **true**.</span></span>
1. <span data-ttu-id="d55f5-164">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d55f5-164">Select **Save**.</span></span>
1. <span data-ttu-id="d55f5-165">Перейдите в раздел **Retail и Commerce \> ИТ Retail и Commerce \> График распределения**.</span><span class="sxs-lookup"><span data-stu-id="d55f5-165">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span> <span data-ttu-id="d55f5-166">Или выполните поиск по словам "График распределения".</span><span class="sxs-lookup"><span data-stu-id="d55f5-166">Alternatively, search for "Distribution schedule."</span></span>
1. <span data-ttu-id="d55f5-167">В списке заданий выберите **1110** (**Глобальная конфигурация**), затем выберите **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="d55f5-167">In the job list, select **1110** (**Global configuration**), and then select **Run now**.</span></span>
1. <span data-ttu-id="d55f5-168">После успешного выполнения задания убедитесь, что оценки продуктов сейчас отображаются на POS-терминале.</span><span class="sxs-lookup"><span data-stu-id="d55f5-168">After the job has successfully run, verify that products ratings are now shown at the POS.</span></span>

<span data-ttu-id="d55f5-169">На следующем рисунке показан пример настройки параметров Commerce для включения оценок продуктов в POS-терминале.</span><span class="sxs-lookup"><span data-stu-id="d55f5-169">The following illustration shows an example of the configuration of the Commerce parameters to turn on product ratings at the POS.</span></span>

![Конфигурация параметров Commerce для оценок продуктов на POS-терминале](media/rnr-hq-enable-ratings-in-pos.png)

<span data-ttu-id="d55f5-171">На следующем рисунке приведен пример оценок продуктов в POS-терминале.</span><span class="sxs-lookup"><span data-stu-id="d55f5-171">The following illustration shows an example of product ratings at the POS.</span></span>

![Оценки продуктов в POS-терминале](media/rnr-pos-catalog-ratings.png)

<span data-ttu-id="d55f5-173">На следующем рисунке приведен пример оценок продуктов в каналах центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="d55f5-173">The following illustration shows an example of product ratings in call center channels.</span></span>

![Рейтинги продуктов в канале центра обработки вызовов](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a><span data-ttu-id="d55f5-175">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d55f5-175">Additional resources</span></span>

[<span data-ttu-id="d55f5-176">Обзор оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="d55f5-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="d55f5-177">Соглашение на использование оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="d55f5-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="d55f5-178">Управление оценками и отзывами</span><span class="sxs-lookup"><span data-stu-id="d55f5-178">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="d55f5-179">Настройка оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="d55f5-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]