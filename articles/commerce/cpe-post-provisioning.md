---
title: Настройка среды предварительной версии Dynamics 365 Commerce
description: В этой теме объясняется, как настроить среду предварительного просмотра Microsoft Dynamics 365 Commerce после ее предоставления.
author: psimolin
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 12d3a86698e9250f5d1645de51e0749c8d929f75
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024714"
---
# <a name="configure-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="5b138-103">Настройка среды предварительной версии Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="5b138-103">Configure a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5b138-104">В этой теме объясняется, как настроить среду предварительного просмотра Microsoft Dynamics 365 Commerce после ее предоставления.</span><span class="sxs-lookup"><span data-stu-id="5b138-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce preview environment after it's provisioned.</span></span>

## <a name="overview"></a><span data-ttu-id="5b138-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="5b138-105">Overview</span></span>

<span data-ttu-id="5b138-106">Выполните процедуры в этой теме только после того, как ваша среда предварительного просмотра Commerce была создана.</span><span class="sxs-lookup"><span data-stu-id="5b138-106">Complete the procedures in this topic only after your Commerce preview environment has been provisioned.</span></span> <span data-ttu-id="5b138-107">Для получения информации о том, как предоставить среду предварительного просмотра Commerce, см. в [Обеспечение среды предварительного просмотра Commerce](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="5b138-107">For information about how to provision your Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

<span data-ttu-id="5b138-108">После того как среда предварительного просмотра Commerce была полностью подготовлена, необходимо завершить дополнительные этапы конфигурации после подготовки, прежде чем вы сможете приступить к оценке среды.</span><span class="sxs-lookup"><span data-stu-id="5b138-108">After your Commerce preview environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="5b138-109">Для выполнения этих шагов необходимо использовать Lifecycle Services Microsoft Dynamics (LCS), Dynamics 365 Commerce и Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="5b138-109">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS), Dynamics 365 Commerce, and Dynamics 365 Retail.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="5b138-110">Перед началом</span><span class="sxs-lookup"><span data-stu-id="5b138-110">Before you start</span></span>

1. <span data-ttu-id="5b138-111">Выполните вход на [портал LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="5b138-111">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="5b138-112">Перейдите к своему проекту.</span><span class="sxs-lookup"><span data-stu-id="5b138-112">Go to your project.</span></span>
1. <span data-ttu-id="5b138-113">В верхнем меню выберите **Размещенные в облаке среды**.</span><span class="sxs-lookup"><span data-stu-id="5b138-113">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="5b138-114">Выберите среду из списка.</span><span class="sxs-lookup"><span data-stu-id="5b138-114">Select your environment in the list.</span></span>
1. <span data-ttu-id="5b138-115">Щелкните **Полные сведения** в сведениях о среде с правой стороны.</span><span class="sxs-lookup"><span data-stu-id="5b138-115">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="5b138-116">Выберите **Вход**, чтобы открыть меню, затем выберите **Войти в среду**.</span><span class="sxs-lookup"><span data-stu-id="5b138-116">Select **Login** to open a menu, and then select **Log on to environment**.</span></span>
1. <span data-ttu-id="5b138-117">Убедитесь, что выбрано юридическое лицо **USRT** (верхний правый угол).</span><span class="sxs-lookup"><span data-stu-id="5b138-117">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

## <a name="configure-the-point-of-sale-in-lcs"></a><span data-ttu-id="5b138-118">Настройка POS в LCS</span><span class="sxs-lookup"><span data-stu-id="5b138-118">Configure the point of sale in LCS</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="5b138-119">Связывание работника с вашим удостоверением</span><span class="sxs-lookup"><span data-stu-id="5b138-119">Associate a worker with your identity</span></span>

<span data-ttu-id="5b138-120">Чтобы связать работника с вашим удостоверением в LCS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5b138-120">To associate a worker with your identity in LCS, follow these steps.</span></span>

1. <span data-ttu-id="5b138-121">Используя меню в левой части, перейдите к **Модули \> Retail \> Сотрудники \> Работники**.</span><span class="sxs-lookup"><span data-stu-id="5b138-121">Use the menu on the left to go to **Modules \> Retail \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="5b138-122">В списке найдите и выберите следующую запись **000713 - Эндрю Колетт (Andrew Collette)**.</span><span class="sxs-lookup"><span data-stu-id="5b138-122">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="5b138-123">В области действий выберите **Retail**.</span><span class="sxs-lookup"><span data-stu-id="5b138-123">On the Action Pane, select **Retail**.</span></span>
1. <span data-ttu-id="5b138-124">Выберите **Ассоциировать существующее удостоверение**.</span><span class="sxs-lookup"><span data-stu-id="5b138-124">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="5b138-125">В поле **Адрес электронной почты**, справа от **Поиск по электронной почте**, введите свой адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="5b138-125">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="5b138-126">Выберите **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="5b138-126">Select **Search**.</span></span>
1. <span data-ttu-id="5b138-127">Выберите запись с вашим именем.</span><span class="sxs-lookup"><span data-stu-id="5b138-127">Select the record that has your name.</span></span>
1. <span data-ttu-id="5b138-128">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5b138-128">Select **OK**.</span></span>
1. <span data-ttu-id="5b138-129">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="5b138-129">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="5b138-130">Активация облачного POS</span><span class="sxs-lookup"><span data-stu-id="5b138-130">Activate Cloud POS</span></span>

<span data-ttu-id="5b138-131">Чтобы активировать Cloud POS в LCS, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5b138-131">To activate Cloud POS in LCS, follow these steps.</span></span>

1. <span data-ttu-id="5b138-132">В верхнем меню выберите **Размещенные в облаке среды**.</span><span class="sxs-lookup"><span data-stu-id="5b138-132">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="5b138-133">Выберите среду из списка.</span><span class="sxs-lookup"><span data-stu-id="5b138-133">Select your environment in the list.</span></span>
1. <span data-ttu-id="5b138-134">Щелкните **Полные сведения** в сведениях о среде с правой стороны.</span><span class="sxs-lookup"><span data-stu-id="5b138-134">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="5b138-135">Выберите **Вход**, чтобы открыть меню, а затем выберите **Войти в Cloud POS**, чтобы открыть POS.</span><span class="sxs-lookup"><span data-stu-id="5b138-135">Select **Login** to open a menu, and then select **Log on to Cloud Point of Sale** to open the point of sale (POS).</span></span>
1. <span data-ttu-id="5b138-136">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="5b138-136">Select **Next**.</span></span>
1. <span data-ttu-id="5b138-137">Войдите в систему с учетной записью Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="5b138-137">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="5b138-138">В области **Имя магазина** выберите **Сан-Франциско**.</span><span class="sxs-lookup"><span data-stu-id="5b138-138">Under **Store name**, select **San Francisco**.</span></span>
1. <span data-ttu-id="5b138-139">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="5b138-139">Select **Next**.</span></span>
1. <span data-ttu-id="5b138-140">В области **Регистрация и устройство** выберите **SANFRAN-1**.</span><span class="sxs-lookup"><span data-stu-id="5b138-140">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="5b138-141">Выберите **Активировать**.</span><span class="sxs-lookup"><span data-stu-id="5b138-141">Select **Activate**.</span></span> <span data-ttu-id="5b138-142">Вы вышли, открылась страница входа POS.</span><span class="sxs-lookup"><span data-stu-id="5b138-142">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="5b138-143">Теперь можно войти во взаимодействие Cloud POS, используя код оператора **000713** и пароль **123**.</span><span class="sxs-lookup"><span data-stu-id="5b138-143">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="5b138-144">Настройка сайта в Commerce</span><span class="sxs-lookup"><span data-stu-id="5b138-144">Set up your site in Commerce</span></span>

<span data-ttu-id="5b138-145">Чтобы начать настраивать сайт предварительного просмотра в Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5b138-145">To start to set up your preview site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="5b138-146">Войдите в инструмент управления сайтом, используя URL-адрес, который вы записали при инициализации электронной коммерции во время подготовки (см. [Инициализация электронной коммерции](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="5b138-146">Sign in to the site management tool by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="5b138-147">Выберите сайт **Fabrikam**, чтобы открыть диалоговое окно настройки сайта.</span><span class="sxs-lookup"><span data-stu-id="5b138-147">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="5b138-148">Выберите домен, в который вы вошли при инициализации электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="5b138-148">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="5b138-149">В качестве канала по умолчанию выберите **Расширенный интернет-магазин Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="5b138-149">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="5b138-150">(Убедитесь, что выбран **расширенный** интернет-магазин.)</span><span class="sxs-lookup"><span data-stu-id="5b138-150">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="5b138-151">В качестве языка по умолчанию выберите **en-us**.</span><span class="sxs-lookup"><span data-stu-id="5b138-151">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="5b138-152">Оставьте значение поля **Путь** как есть.</span><span class="sxs-lookup"><span data-stu-id="5b138-152">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="5b138-153">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5b138-153">Select **OK**.</span></span> <span data-ttu-id="5b138-154">Появляется список страниц на сайте.</span><span class="sxs-lookup"><span data-stu-id="5b138-154">The list of pages on the site appears.</span></span>

## <a name="enable-jobs-in-retail"></a><span data-ttu-id="5b138-155">Включение заданий в Retail</span><span class="sxs-lookup"><span data-stu-id="5b138-155">Enable jobs in Retail</span></span>

<span data-ttu-id="5b138-156">Чтобы включить задания в Retail, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5b138-156">To enable jobs in Retail, follow these steps.</span></span>

1. <span data-ttu-id="5b138-157">Выполните вход в среду (HQ).</span><span class="sxs-lookup"><span data-stu-id="5b138-157">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="5b138-158">Используя меню, расположенное в левой части, перейдите в раздел **Retail \> Запросы и отчеты \> Пакетные задания**.</span><span class="sxs-lookup"><span data-stu-id="5b138-158">Use the menu on the left to go to **Retail \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="5b138-159">Остальные этапы этой процедуры должны быть завершены для каждого из следующих заданий:</span><span class="sxs-lookup"><span data-stu-id="5b138-159">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="5b138-160">Обработать уведомление по электронной почте о заказе розничной торговли</span><span class="sxs-lookup"><span data-stu-id="5b138-160">Process retail order email notification</span></span>
    * <span data-ttu-id="5b138-161">Доступность продукта</span><span class="sxs-lookup"><span data-stu-id="5b138-161">Product availability</span></span>
    * <span data-ttu-id="5b138-162">P-0001</span><span class="sxs-lookup"><span data-stu-id="5b138-162">P-0001</span></span>
    * <span data-ttu-id="5b138-163">Задание синхронизации заказов</span><span class="sxs-lookup"><span data-stu-id="5b138-163">Synchronize orders job</span></span>

1. <span data-ttu-id="5b138-164">Используйте быструю фильтрацию для поиска задания по его названию.</span><span class="sxs-lookup"><span data-stu-id="5b138-164">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="5b138-165">Если статус задания — **Отложено**, выполните следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="5b138-165">If the status of the job is **Withhold**, follow these steps:</span></span>

    1. <span data-ttu-id="5b138-166">Выберите запись.</span><span class="sxs-lookup"><span data-stu-id="5b138-166">Select the record.</span></span>
    1. <span data-ttu-id="5b138-167">В области действий щелкните вкладку **Пакетное задание**, выберите **Изменить статус**.</span><span class="sxs-lookup"><span data-stu-id="5b138-167">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="5b138-168">Выберите **Ожидание**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5b138-168">Select **Waiting**, and then select **OK**.</span></span>

### <a name="run-full-data-synchronization-in-retail"></a><span data-ttu-id="5b138-169">Запуск полной синхронизации данных в Retail</span><span class="sxs-lookup"><span data-stu-id="5b138-169">Run full data synchronization in Retail</span></span>

<span data-ttu-id="5b138-170">Чтобы запустить полную синхронизацию данных в Retail, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5b138-170">To run full data synchronization in Retail, follow these steps.</span></span>

1. <span data-ttu-id="5b138-171">Используя меню в левой части, перейдите к пункту **Модули \> Retail \> Настройка центрального офиса \> Розничная сеть - Планировщик \> База данных канала**.</span><span class="sxs-lookup"><span data-stu-id="5b138-171">Use the menu on the left to go to **Modules \> Retail \> Headquarters setup \> Retail scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="5b138-172">Канал **По умолчанию** выбирается из списка слева.</span><span class="sxs-lookup"><span data-stu-id="5b138-172">In the list on the left, the **Default** channel is selected.</span></span> <span data-ttu-id="5b138-173">Выберите другой доступный канал.</span><span class="sxs-lookup"><span data-stu-id="5b138-173">Select the other available channel.</span></span> <span data-ttu-id="5b138-174">Этот канал называется **scXXXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="5b138-174">This channel is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="5b138-175">На панели операций выберите **Полная синхронизация данных**.</span><span class="sxs-lookup"><span data-stu-id="5b138-175">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="5b138-176">Введите график распределения **9999**.</span><span class="sxs-lookup"><span data-stu-id="5b138-176">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="5b138-177">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5b138-177">Select **OK**.</span></span>
1. <span data-ttu-id="5b138-178">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="5b138-178">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="5b138-179">Проверьте сведения о кредитной карте для тестирования покупок</span><span class="sxs-lookup"><span data-stu-id="5b138-179">Test credit card information to do test purchases</span></span>

<span data-ttu-id="5b138-180">Для выполнения проверочных проводок на сайте можно использовать следующие данные пробной кредитной карты:</span><span class="sxs-lookup"><span data-stu-id="5b138-180">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="5b138-181">**Номер карты:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="5b138-181">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="5b138-182">**Дата окончания срока действия:** 10/20</span><span class="sxs-lookup"><span data-stu-id="5b138-182">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="5b138-183">**Контрольный код карты (CVV):** 737</span><span class="sxs-lookup"><span data-stu-id="5b138-183">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5b138-184">Никогда не следует пытаться использовать фактические сведения кредитной карты на тестовых сайтах при любых обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="5b138-184">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="5b138-185">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="5b138-185">Next steps</span></span>

<span data-ttu-id="5b138-186">После завершения этапов подготовки и конфигурации вы готовы оценить среду предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="5b138-186">After the provisioning and configuration steps are completed, you're ready to evaluate your preview environment.</span></span> <span data-ttu-id="5b138-187">Используйте URL-адрес инструмента управления сайтом Commerce, чтобы перейти к взаимодействию разработки.</span><span class="sxs-lookup"><span data-stu-id="5b138-187">Use the URL of the Commerce site management tool to go to the authoring experience.</span></span> <span data-ttu-id="5b138-188">Используйте URL-адрес инструмента управления сайтом Commerce, чтобы перейти к взаимодействию с сайтом клиента Retail.</span><span class="sxs-lookup"><span data-stu-id="5b138-188">Use the URL of the Commerce site to go to the retail customer site experience.</span></span>

<span data-ttu-id="5b138-189">Чтобы настроить дополнительные функции для среды предварительного просмотра Commerce, см. [Настройка дополнительных функций для среды предварительного просмотра Commerce](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="5b138-189">To configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5b138-190">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="5b138-190">Additional resources</span></span>

[<span data-ttu-id="5b138-191">Обзор среды предварительной версии Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="5b138-191">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="5b138-192">Обеспечение среды предварительной версии Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="5b138-192">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="5b138-193">Настройка дополнительных функций среды предварительной версии Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="5b138-193">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="5b138-194">Вопросы и ответы по среде предварительной версии Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="5b138-194">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="5b138-195">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="5b138-195">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="5b138-196">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="5b138-196">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="5b138-197">Портал Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="5b138-197">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="5b138-198">Веб-сайт Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="5b138-198">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
