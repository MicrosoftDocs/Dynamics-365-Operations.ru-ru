---
title: Синхронизация оценок продуктов в Dynamics 365 Retail
description: В этом разделе описывается синхронизация оценок продуктов в Microsoft Dynamics 365 Retail.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: db5a4e1f78797d20ded2274cc99bef422fd50acc
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698173"
---
# <a name="sync-product-ratings-in-dynamics-365-retail"></a><span data-ttu-id="62d51-103">Синхронизация оценок продуктов в Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="62d51-103">Sync product ratings in Dynamics 365 Retail</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="62d51-104">В этом разделе описывается синхронизация оценок продуктов в Microsoft Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="62d51-104">This topic describes how to sync product ratings in Microsoft Dynamics 365 Retail.</span></span>

## <a name="overview"></a><span data-ttu-id="62d51-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="62d51-105">Overview</span></span>

<span data-ttu-id="62d51-106">Для использования оценок продуктов в омниканалах, таких как POS-терминалы и центры обработки вызовов, необходимо импортировать оценки продуктов из службы оценок и отзывов в базу данных канала Retail.</span><span class="sxs-lookup"><span data-stu-id="62d51-106">To consume product ratings in omnichannels, such as at the point of sale (POS) and in call centers, product ratings from the ratings and reviews service must be imported into the Retail channel database.</span></span> <span data-ttu-id="62d51-107">Когда оценки продукта доступны в омниканалах, они могут помочь клиентам косвенным образом в ходе их взаимодействия с продавцами-консультантами.</span><span class="sxs-lookup"><span data-stu-id="62d51-107">When product ratings are made available in omnichannels, they can help customers indirectly during their interactions with sales associates.</span></span>

<span data-ttu-id="62d51-108">Данный раздел описывает следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="62d51-108">This topic describes following tasks:</span></span>

1. <span data-ttu-id="62d51-109">Настройка пакетного задания Retail для импорта оценок продуктов.</span><span class="sxs-lookup"><span data-stu-id="62d51-109">Configure a Retail batch job to import product ratings.</span></span>
1. <span data-ttu-id="62d51-110">Проверка того, что пакетное задание для синхронизации оценок продукта прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="62d51-110">Verify that the batch job for product rating synchronization was successful.</span></span>
1. <span data-ttu-id="62d51-111">Обеспечение доступности оценок продукта на POS-терминале.</span><span class="sxs-lookup"><span data-stu-id="62d51-111">Make product ratings available at the POS.</span></span>

## <a name="configure-a-retail-batch-job-to-import-product-ratings"></a><span data-ttu-id="62d51-112">Настройка пакетного задания Retail для импорта оценок продуктов</span><span class="sxs-lookup"><span data-stu-id="62d51-112">Configure a Retail batch job to import product ratings</span></span>

> [!IMPORTANT]
> <span data-ttu-id="62d51-113">Прежде чем начать, убедитесь, что установлена версия Retail 10.0.6 или более поздняя.</span><span class="sxs-lookup"><span data-stu-id="62d51-113">Before you start, make sure that version 10.0.6 or later of Retail is installed.</span></span>

### <a name="initialize-the-retail-scheduler"></a><span data-ttu-id="62d51-114">Инициализация планировщика Retail</span><span class="sxs-lookup"><span data-stu-id="62d51-114">Initialize the retail scheduler</span></span>

<span data-ttu-id="62d51-115">Чтобы инициализировать планировщик Retail, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="62d51-115">To initialize the retail scheduler, follow these steps.</span></span>

1. <span data-ttu-id="62d51-116">Перейдите в **Retail \> Настройка центрального офиса \> Розничная сеть - Планировщик \> Инициализация планировщика Retail**.</span><span class="sxs-lookup"><span data-stu-id="62d51-116">Go to **Retail \> Headquarters setup \> Retail scheduler \> Initialize retail scheduler**.</span></span> <span data-ttu-id="62d51-117">Либо выполните поиск "Инициализация планировщика Retail".</span><span class="sxs-lookup"><span data-stu-id="62d51-117">Alternatively, search for "Initialize retail scheduler."</span></span>
1. <span data-ttu-id="62d51-118">В диалоговом окне **Инициализация планировщика Retail** убедитесь, что параметр **Удалить существующую конфигурацию** имеет значение **Нет**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="62d51-118">In the **Initialize retail scheduler** dialog box, make sure that the **Delete existing configuration** option is set to **No**, and then select **OK**.</span></span>

### <a name="verify-the-retailproductrating-subjob"></a><span data-ttu-id="62d51-119">Проверка подзадания RetailProductRating</span><span class="sxs-lookup"><span data-stu-id="62d51-119">Verify the RetailProductRating subjob</span></span>

<span data-ttu-id="62d51-120">Чтобы убедиться в наличии подзадания **RetailProductRating**, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="62d51-120">To verify that the **RetailProductRating** subjob exists, follow these steps.</span></span>

1. <span data-ttu-id="62d51-121">Перейдите в **Retail \> Настройка центрального офиса \> Розничная сеть - Планировщик \> Подзадания планировщика**.</span><span class="sxs-lookup"><span data-stu-id="62d51-121">Go to **Retail \> Headquarters setup \> Retail scheduler \> Scheduler subjobs**.</span></span> <span data-ttu-id="62d51-122">Или выполните поиск "Подзадания планировщика".</span><span class="sxs-lookup"><span data-stu-id="62d51-122">Alternatively, search for "Scheduler subjobs."</span></span>
1. <span data-ttu-id="62d51-123">В списке подзаданий найдите или выполните поиск подзадания **RetailProductRating**.</span><span class="sxs-lookup"><span data-stu-id="62d51-123">In the subjob list, find or search for the **RetailProductRating** subjob.</span></span>

<span data-ttu-id="62d51-124">На следующем рисунке показан пример сведений о подзаданиях в Retail.</span><span class="sxs-lookup"><span data-stu-id="62d51-124">The following illustration shows an example of the subjob details in Retail.</span></span>

![Сведения о подзадании RetailProductRating](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> <span data-ttu-id="62d51-126">Если подзадание **RetailProductRating** не удается найти, возможно, вы уже запустили задание **Синхронизация оценок продуктов** и задание **1040 CDX** перед инициализацией модуля "Розничная сеть-планировщик".</span><span class="sxs-lookup"><span data-stu-id="62d51-126">If you don't find the **RetailProductRating** subjob, you might already have run the **Sync product ratings** job and the **1040 CDX** job before you initialized the retail scheduler.</span></span> <span data-ttu-id="62d51-127">В этом случае выполните следующие шаги, чтобы выполнить задание **Полная синхронизация данных**.</span><span class="sxs-lookup"><span data-stu-id="62d51-127">In this case, follow these steps to run the **Full data sync** job.</span></span>
>
> 1. <span data-ttu-id="62d51-128">Перейдите в **Retail \> Настройка центрального офиса \> Розничная сеть - Планировщик \> База данных канала**.</span><span class="sxs-lookup"><span data-stu-id="62d51-128">Go to **Retail \> Headquarters setup \> Retail scheduler \> Channel database**.</span></span> <span data-ttu-id="62d51-129">Или же выполните поиск по словам "База данных канала".</span><span class="sxs-lookup"><span data-stu-id="62d51-129">Alternatively, search for "Channel database."</span></span>
> 1. <span data-ttu-id="62d51-130">Выберите базу данных канала для синхронизации.</span><span class="sxs-lookup"><span data-stu-id="62d51-130">Select the channel database to sync.</span></span>
> 1. <span data-ttu-id="62d51-131">На панели операций выберите **Полная синхронизация данных**.</span><span class="sxs-lookup"><span data-stu-id="62d51-131">On the Action Pane, select **Full data sync**.</span></span>
> 1. <span data-ttu-id="62d51-132">В раскрывающемся диалоговом окне **Выбор графика распределения** выберите **1040 — продукты**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="62d51-132">In the **Select a distribution schedule** drop-down dialog box, select **1040 - products**, and then select **OK**.</span></span>
> 1. <span data-ttu-id="62d51-133">Повторите шаги предыдущей процедуры для проверки создания подзадания **RetailProductRating**.</span><span class="sxs-lookup"><span data-stu-id="62d51-133">Repeat the steps of the previous procedure to verify that the **RetailProductRating** subjob has been created.</span></span>

### <a name="import-product-ratings"></a><span data-ttu-id="62d51-134">Импорт оценок продуктов</span><span class="sxs-lookup"><span data-stu-id="62d51-134">Import product ratings</span></span>

<span data-ttu-id="62d51-135">Чтобы импортировать оценки продуктов в Retail из службы оценок и отзывов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="62d51-135">To import product ratings into Retail from the ratings and reviews service, follow these steps.</span></span>

1. <span data-ttu-id="62d51-136">Перейдите в **Retail \> Настройка центрального офиса \> Розничная сеть - Планировщик \> Задание синхронизации оценок продуктов**.</span><span class="sxs-lookup"><span data-stu-id="62d51-136">Go to **Retail \> Headquarters setup \> Retail scheduler \> Sync product ratings job**.</span></span> <span data-ttu-id="62d51-137">Или выполните поиск по запросу "Задание синхронизации оценок продуктов".</span><span class="sxs-lookup"><span data-stu-id="62d51-137">Alternatively, search for "Sync product ratings job."</span></span>
1. <span data-ttu-id="62d51-138">В диалоговом окне **Извлечь оценки продуктов** на экспресс-вкладке **Выполнять в фоновом режиме** выберите **Повторение**.</span><span class="sxs-lookup"><span data-stu-id="62d51-138">In the **Pull product ratings** dialog box, on the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="62d51-139">В диалоговом окне **Определение повторения** настройте шаблон повторения.</span><span class="sxs-lookup"><span data-stu-id="62d51-139">In the **Define recurrence** dialog box, set up a recurrence pattern.</span></span> <span data-ttu-id="62d51-140">(Предлагаемое значение — 2 часа.) Не планируйте повторение, которое меньше одного часа.</span><span class="sxs-lookup"><span data-stu-id="62d51-140">(The suggested value is two hours.) Don't schedule a recurrence that is less than one hour.</span></span>
1. <span data-ttu-id="62d51-141">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="62d51-141">Select **OK**.</span></span>
1. <span data-ttu-id="62d51-142">Установите для параметра **Процесс пакетной обработки** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="62d51-142">Set the **Batch process** option to **Yes**.</span></span> <span data-ttu-id="62d51-143">Эта настройка гарантирует, что можно будет выполнять аудит журналов и проверять статус запуска пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="62d51-143">This setting helps guarantee that you will be able to audit the logs and verify the status of batch job runs.</span></span>
1. <span data-ttu-id="62d51-144">Выберите **ОК**, чтобы запланировать пакетное задание.</span><span class="sxs-lookup"><span data-stu-id="62d51-144">Select **OK** to schedule the batch job.</span></span>

<span data-ttu-id="62d51-145">На следующем рисунке показан пример конфигурации пакетного задания в Retail.</span><span class="sxs-lookup"><span data-stu-id="62d51-145">The following illustration shows an example of batch job configuration in Retail.</span></span>

![Конфигурация пакетного задания синхронизации оценок продуктов](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a><span data-ttu-id="62d51-147">Проверка того, что пакетное задание для синхронизации оценок продукта прошло успешно</span><span class="sxs-lookup"><span data-stu-id="62d51-147">Verify that the batch job for product rating synchronization was successful</span></span>

<span data-ttu-id="62d51-148">Чтобы убедиться, что пакетное задание **Синхронизация оценок продуктов** прошло успешно, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="62d51-148">To verify that the **Sync product ratings** batch job was successful, follow these steps.</span></span>

1. <span data-ttu-id="62d51-149">Откройте **Retail \> Системный администратор \> Запросы \> Пакетные задания** или, если используется только единица складского хранения (SKU) Retail, выберите **Retail \> Запросы и отчеты \> Пакетные задания**.</span><span class="sxs-lookup"><span data-stu-id="62d51-149">Go to **Retail \> System administrator \> Inquiries \> Batch jobs** or, if you're using a Retail-only stock keeping unit (SKU), **Retail \> Inquiries and reports \> Batch jobs** instead.</span></span> <span data-ttu-id="62d51-150">Или выполните поиск по словам "Пакетные задания".</span><span class="sxs-lookup"><span data-stu-id="62d51-150">Alternatively, search for "Batch jobs."</span></span>
1. <span data-ttu-id="62d51-151">Чтобы просмотреть сведения о пакетном задании, в списке пакетных заданий в столбце **Описание задания** выполните поиск описания, которое содержит слова "Извлечение оценок продуктов".</span><span class="sxs-lookup"><span data-stu-id="62d51-151">To view the details of the batch job, in the batch job list, in the **Job description** column, search for a description that contains "Pull product ratings."</span></span>
1. <span data-ttu-id="62d51-152">Выберите код задания, чтобы просмотреть сведения о пакетном задании, такие как запланированные начальные даты и время и текст повторения.</span><span class="sxs-lookup"><span data-stu-id="62d51-152">Select the job ID to view the batch job details, such as the scheduled start date/time and the recurrence text.</span></span>

<span data-ttu-id="62d51-153">На следующем рисунке показан пример сведений пакетного задания в Retail, когда запланировано выполнение пакетного задания с интервалом два часа.</span><span class="sxs-lookup"><span data-stu-id="62d51-153">The following illustration shows an example of the batch job details in Retail when the batch job is scheduled to run at two-hour intervals.</span></span>

![Сведения о пакетном задании синхронизации оценки продукта](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a><span data-ttu-id="62d51-155">Обеспечение доступности оценок продукта на POS-терминале</span><span class="sxs-lookup"><span data-stu-id="62d51-155">Make product ratings available at the POS</span></span>

<span data-ttu-id="62d51-156">Решение оценок и отзывов в Dynamics 365 Commerce является омниканальным решением.</span><span class="sxs-lookup"><span data-stu-id="62d51-156">The ratings and reviews solution in Dynamics 365 Commerce is an omnichannel solution.</span></span> <span data-ttu-id="62d51-157">Однако по умолчанию оценки продуктов не отображаются на POS-терминале.</span><span class="sxs-lookup"><span data-stu-id="62d51-157">However, products ratings aren't shown at the POS by default.</span></span> <span data-ttu-id="62d51-158">Чтобы помочь клиентам в магазинах просматривать оценки и отзывы, когда им помогают торговые консультанты, необходимо включить рейтинги продуктов на POS-терминале.</span><span class="sxs-lookup"><span data-stu-id="62d51-158">To help customers in stores see ratings and reviews when they are being helped by sales associates, you must turn on product ratings at the POS.</span></span>

<span data-ttu-id="62d51-159">Чтобы включить рейтинги продуктов в POS-терминале, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="62d51-159">To turn on product ratings at the POS, follow these steps.</span></span>

1. <span data-ttu-id="62d51-160">Перейдите в раздел **Retail \> Настройка Retail \> Параметры \> Параметры Retail**.</span><span class="sxs-lookup"><span data-stu-id="62d51-160">Go to **Retail \> Retail setup \> Parameters \> Retail parameters**.</span></span> <span data-ttu-id="62d51-161">Или выполните поиск "Параметры Retail".</span><span class="sxs-lookup"><span data-stu-id="62d51-161">Alternatively, search for "Retail parameters."</span></span>
1. <span data-ttu-id="62d51-162">На вкладке **Параметры конфигурации** выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="62d51-162">On the **Configuration parameters** tab, select **New**.</span></span>
1. <span data-ttu-id="62d51-163">Введите имя, например **RatingsAndReviews.EnableProductRatingsForRetailStores**, и установите значение **true**.</span><span class="sxs-lookup"><span data-stu-id="62d51-163">Enter a name such as **RatingsAndReviews.EnableProductRatingsForRetailStores**, and set the value to **true**.</span></span>
1. <span data-ttu-id="62d51-164">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="62d51-164">Select **Save**.</span></span>
1. <span data-ttu-id="62d51-165">Выберите **Розничная торговля \> ИТ розничной торговли \> График распределения**.</span><span class="sxs-lookup"><span data-stu-id="62d51-165">Go to **Retail \> Retail IT \> Distribution schedule**.</span></span> <span data-ttu-id="62d51-166">Или выполните поиск по словам "График распределения".</span><span class="sxs-lookup"><span data-stu-id="62d51-166">Alternatively, search for "Distribution schedule."</span></span>
1. <span data-ttu-id="62d51-167">В списке заданий выберите **1110** (**Глобальная конфигурация**), затем выберите **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="62d51-167">In the job list, select **1110** (**Global configuration**), and then select **Run now**.</span></span>
1. <span data-ttu-id="62d51-168">После успешного выполнения задания убедитесь, что оценки продуктов сейчас отображаются на POS-терминале.</span><span class="sxs-lookup"><span data-stu-id="62d51-168">After the job has successfully run, verify that products ratings are now shown at the POS.</span></span>

<span data-ttu-id="62d51-169">На следующем рисунке показан пример настройки параметров Retail для включения оценок продуктов в POS-терминале.</span><span class="sxs-lookup"><span data-stu-id="62d51-169">The following illustration shows an example of the configuration of the Retail parameters to turn on product ratings at the POS.</span></span>

![Конфигурация параметров Retail для оценок продуктов на POS-терминале](media/rnr-hq-enable-ratings-in-pos.png)

<span data-ttu-id="62d51-171">На следующем рисунке приведен пример оценок продуктов в POS-терминале.</span><span class="sxs-lookup"><span data-stu-id="62d51-171">The following illustration shows an example of product ratings at the POS.</span></span>

![Оценки продуктов в POS-терминале](media/rnr-pos-catalog-ratings.png)

<span data-ttu-id="62d51-173">На следующем рисунке приведен пример оценок продуктов в каналах центра обработки вызовов.</span><span class="sxs-lookup"><span data-stu-id="62d51-173">The following illustration shows an example of product ratings in call center channels.</span></span>

![Рейтинги продуктов в канале центра обработки вызовов](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a><span data-ttu-id="62d51-175">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="62d51-175">Additional resources</span></span>

[<span data-ttu-id="62d51-176">Обзор оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="62d51-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="62d51-177">Соглашение на использование оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="62d51-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="62d51-178">Управление оценками и отзывами</span><span class="sxs-lookup"><span data-stu-id="62d51-178">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="62d51-179">Настройка оценок и отзывов</span><span class="sxs-lookup"><span data-stu-id="62d51-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)
