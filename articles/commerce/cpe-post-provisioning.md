---
title: Настройка среды оценки Dynamics 365 Commerce
description: В этой теме объясняется, как настроить ознакомительную среду Microsoft Dynamics 365 Commerce после ее предоставления.
author: psimolin
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 9b11ab600bb2aa17cf330947304f5b22dd522081
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477981"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="15772-103">Настройка среды оценки Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="15772-103">Configure a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="15772-104">В этой теме объясняется, как настроить ознакомительную среду Microsoft Dynamics 365 Commerce после ее предоставления.</span><span class="sxs-lookup"><span data-stu-id="15772-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce evaluation environment after it's provisioned.</span></span>

<span data-ttu-id="15772-105">Выполните процедуры в этой теме только после того, как ваша ознакомительная среда Commerce была создана.</span><span class="sxs-lookup"><span data-stu-id="15772-105">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned.</span></span> <span data-ttu-id="15772-106">Для получения информации о том, как предоставить ознакомительную среду Commerce, см. в [Обеспечение ознакомительной среды Commerce](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="15772-106">For information about how to provision your Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

<span data-ttu-id="15772-107">После того как ознакомительная среда Commerce была полностью подготовлена, необходимо завершить дополнительные этапы конфигурации после подготовки, прежде чем вы сможете приступить к оценке среды.</span><span class="sxs-lookup"><span data-stu-id="15772-107">After your Commerce evaluation environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="15772-108">Для выполнения этих шагов необходимо использовать Microsoft Dynamics Lifecycle Services (LCS) и Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="15772-108">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS) and Dynamics 365 Commerce.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="15772-109">Перед началом</span><span class="sxs-lookup"><span data-stu-id="15772-109">Before you start</span></span>

1. <span data-ttu-id="15772-110">Выполните вход на [портал LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="15772-110">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="15772-111">Перейдите к своему проекту.</span><span class="sxs-lookup"><span data-stu-id="15772-111">Go to your project.</span></span>
1. <span data-ttu-id="15772-112">В верхнем меню выберите **Размещенные в облаке среды**.</span><span class="sxs-lookup"><span data-stu-id="15772-112">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="15772-113">Выберите среду из списка.</span><span class="sxs-lookup"><span data-stu-id="15772-113">Select your environment in the list.</span></span>
1. <span data-ttu-id="15772-114">Щелкните **Войти в среду** в сведениях о среде с правой стороны.</span><span class="sxs-lookup"><span data-stu-id="15772-114">In the environment information on the right, select **Log on to environment**.</span></span> <span data-ttu-id="15772-115">Вы будете отправлены в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="15772-115">You will be sent to Commerce headquarters.</span></span>
1. <span data-ttu-id="15772-116">Убедитесь, что выбрано юридическое лицо **USRT** (верхний правый угол).</span><span class="sxs-lookup"><span data-stu-id="15772-116">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

<span data-ttu-id="15772-117">Во время действий после подготовки в модуле Commerce Headquarters убедитесь, что всегда выбрано юридическое лицо **USRT**.</span><span class="sxs-lookup"><span data-stu-id="15772-117">During post-provisioning activities in Commerce headquarters, make sure that the **USRT** legal entity is always selected.</span></span>

## <a name="configure-the-point-of-sale"></a><span data-ttu-id="15772-118">Настройка POS</span><span class="sxs-lookup"><span data-stu-id="15772-118">Configure the point of sale</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="15772-119">Связывание работника с вашим удостоверением</span><span class="sxs-lookup"><span data-stu-id="15772-119">Associate a worker with your identity</span></span>

<span data-ttu-id="15772-120">Чтобы связать работника с вашим удостоверением, выполните следующие действия в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="15772-120">To associate a worker with your identity, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="15772-121">Используя меню в левой части, перейдите к **Модули \> Retail и commerce \> Сотрудники \> Работники**.</span><span class="sxs-lookup"><span data-stu-id="15772-121">Use the menu on the left to go to **Modules \> Retail and commerce \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="15772-122">В списке найдите и выберите следующую запись **000713 - Эндрю Колетт (Andrew Collette)**.</span><span class="sxs-lookup"><span data-stu-id="15772-122">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="15772-123">На панели операций выберите **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="15772-123">On the Action Pane, select **Commerce**.</span></span>
1. <span data-ttu-id="15772-124">Выберите **Ассоциировать существующее удостоверение**.</span><span class="sxs-lookup"><span data-stu-id="15772-124">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="15772-125">В поле **Адрес электронной почты**, справа от **Поиск по электронной почте**, введите свой адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="15772-125">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="15772-126">Выберите **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="15772-126">Select **Search**.</span></span>
1. <span data-ttu-id="15772-127">Выберите запись с вашим именем.</span><span class="sxs-lookup"><span data-stu-id="15772-127">Select the record that has your name.</span></span>
1. <span data-ttu-id="15772-128">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="15772-128">Select **OK**.</span></span>
1. <span data-ttu-id="15772-129">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="15772-129">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="15772-130">Активация облачного POS</span><span class="sxs-lookup"><span data-stu-id="15772-130">Activate Cloud POS</span></span>

<span data-ttu-id="15772-131">Чтобы активировать Cloud POS, выполните следующие действия в LCS.</span><span class="sxs-lookup"><span data-stu-id="15772-131">To activate Cloud POS, follow these steps in LCS.</span></span>

1. <span data-ttu-id="15772-132">В верхнем меню выберите **Размещенные в облаке среды**.</span><span class="sxs-lookup"><span data-stu-id="15772-132">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="15772-133">Выберите среду из списка.</span><span class="sxs-lookup"><span data-stu-id="15772-133">Select your environment in the list.</span></span>
1. <span data-ttu-id="15772-134">Щелкните **Войти в Cloud POS** в сведениях о среде с правой стороны.</span><span class="sxs-lookup"><span data-stu-id="15772-134">In the environment information on the right, select **Log on to Cloud Point of Sale**.</span></span>
1. <span data-ttu-id="15772-135">Выберите **Далее**, чтобы открыть диалоговое окно **Перед началом**.</span><span class="sxs-lookup"><span data-stu-id="15772-135">Select **Next** to open the **Before you start** dialog box.</span></span>
1. <span data-ttu-id="15772-136">Оставьте поле **URL-адрес сервера** без изменений.</span><span class="sxs-lookup"><span data-stu-id="15772-136">Leave the **Server URL** field as it is.</span></span> <span data-ttu-id="15772-137">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="15772-137">Select **Next**.</span></span>
1. <span data-ttu-id="15772-138">Войдите в систему с учетной записью Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="15772-138">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="15772-139">В области **Имя магазина** выберите **Сан-Франциско**, затем выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="15772-139">Under **Store name**, select **San Francisco**, and then select **Next**.</span></span>
1. <span data-ttu-id="15772-140">В области **Регистрация и устройство** выберите **SANFRAN-1**.</span><span class="sxs-lookup"><span data-stu-id="15772-140">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="15772-141">Выберите **Активировать**.</span><span class="sxs-lookup"><span data-stu-id="15772-141">Select **Activate**.</span></span> <span data-ttu-id="15772-142">Вы вышли, открылась страница входа POS.</span><span class="sxs-lookup"><span data-stu-id="15772-142">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="15772-143">Теперь можно войти во взаимодействие Cloud POS, используя код оператора **000713** и пароль **123**.</span><span class="sxs-lookup"><span data-stu-id="15772-143">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="15772-144">Настройка сайта в Commerce</span><span class="sxs-lookup"><span data-stu-id="15772-144">Set up your site in Commerce</span></span>

<span data-ttu-id="15772-145">Чтобы начать настраивать ознакомительный сайт в Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="15772-145">To start to set up your evaluation site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="15772-146">Войдите в конструктор сайтов, используя URL-адрес, который вы записали при инициализации электронной коммерции во время подготовки (см. [Инициализация электронной коммерции](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="15772-146">Sign in to site builder by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="15772-147">Выберите сайт **Fabrikam**, чтобы открыть диалоговое окно настройки сайта.</span><span class="sxs-lookup"><span data-stu-id="15772-147">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="15772-148">Выберите домен, в который вы вошли при инициализации электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="15772-148">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="15772-149">В качестве канала по умолчанию выберите **Расширенный интернет-магазин Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="15772-149">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="15772-150">(Убедитесь, что выбран **расширенный** интернет-магазин.)</span><span class="sxs-lookup"><span data-stu-id="15772-150">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="15772-151">В качестве языка по умолчанию выберите **en-us**.</span><span class="sxs-lookup"><span data-stu-id="15772-151">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="15772-152">Оставьте значение поля **Путь** как есть.</span><span class="sxs-lookup"><span data-stu-id="15772-152">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="15772-153">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="15772-153">Select **OK**.</span></span> <span data-ttu-id="15772-154">Появляется список страниц на сайте.</span><span class="sxs-lookup"><span data-stu-id="15772-154">The list of pages on the site appears.</span></span>

## <a name="enable-jobs"></a><span data-ttu-id="15772-155">Включение заданий</span><span class="sxs-lookup"><span data-stu-id="15772-155">Enable jobs</span></span>

<span data-ttu-id="15772-156">Чтобы включить задания в Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="15772-156">To enable jobs in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="15772-157">Выполните вход в среду (HQ).</span><span class="sxs-lookup"><span data-stu-id="15772-157">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="15772-158">Используя меню, расположенное в левой части, перейдите в раздел **Retail и Commerce \> Запросы и отчеты \> Пакетные задания**.</span><span class="sxs-lookup"><span data-stu-id="15772-158">Use the menu on the left to go to **Retail and commerce \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="15772-159">Остальные этапы этой процедуры должны быть завершены для каждого из следующих заданий:</span><span class="sxs-lookup"><span data-stu-id="15772-159">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="15772-160">Обработать уведомление по электронной почте о заказе розничной торговли</span><span class="sxs-lookup"><span data-stu-id="15772-160">Process retail order email notification</span></span>
    * <span data-ttu-id="15772-161">Доступность продукта</span><span class="sxs-lookup"><span data-stu-id="15772-161">Product availability</span></span>
    * <span data-ttu-id="15772-162">P-0001</span><span class="sxs-lookup"><span data-stu-id="15772-162">P-0001</span></span>
    * <span data-ttu-id="15772-163">Задание синхронизации заказов</span><span class="sxs-lookup"><span data-stu-id="15772-163">Synchronize orders job</span></span>

1. <span data-ttu-id="15772-164">Используйте быструю фильтрацию для поиска задания по его названию.</span><span class="sxs-lookup"><span data-stu-id="15772-164">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="15772-165">Если статус задания — **Выполняется**, выполните следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="15772-165">If the status of the job is **Executing**, follow these steps:</span></span>

    1. <span data-ttu-id="15772-166">Выберите запись.</span><span class="sxs-lookup"><span data-stu-id="15772-166">Select the record.</span></span>
    1. <span data-ttu-id="15772-167">В области действий щелкните вкладку **Пакетное задание**, выберите **Изменить статус**.</span><span class="sxs-lookup"><span data-stu-id="15772-167">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="15772-168">Выберите **Отменяется**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="15772-168">Select **Canceling**, and then select **OK**.</span></span>

<span data-ttu-id="15772-169">Кроме того, можно установить интервал повторения равным одной (1) минуте для следующих заданий:</span><span class="sxs-lookup"><span data-stu-id="15772-169">Optionally, you can also set the recurrence interval to one (1) minute for the following jobs:</span></span>

* <span data-ttu-id="15772-170">Задание обработки уведомления по электронной почте о заказе розничной торговли</span><span class="sxs-lookup"><span data-stu-id="15772-170">Process retail order email notification job</span></span>
* <span data-ttu-id="15772-171">Задание P-0001</span><span class="sxs-lookup"><span data-stu-id="15772-171">P-0001 job</span></span>
* <span data-ttu-id="15772-172">Задание синхронизации заказов</span><span class="sxs-lookup"><span data-stu-id="15772-172">Synchronize orders job</span></span>

### <a name="run-full-data-synchronization"></a><span data-ttu-id="15772-173">Выполнение полной синхронизации данных</span><span class="sxs-lookup"><span data-stu-id="15772-173">Run full data synchronization</span></span>

<span data-ttu-id="15772-174">Чтобы запустить полную синхронизацию данных в Commerce, выполните следующие действия в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="15772-174">To run full data synchronization in Commerce, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="15772-175">Используя меню в левой части, перейдите к пункту **Модули \> Retail и Commerce \> Настройка центрального офиса \> Планировщик Commerce \> База данных канала**.</span><span class="sxs-lookup"><span data-stu-id="15772-175">Use the menu on the left to go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="15772-176">Выберите канал с именем **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="15772-176">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="15772-177">На панели операций выберите **Полная синхронизация данных**.</span><span class="sxs-lookup"><span data-stu-id="15772-177">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="15772-178">Введите график распределения **9999**.</span><span class="sxs-lookup"><span data-stu-id="15772-178">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="15772-179">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="15772-179">Select **OK**.</span></span>
1. <span data-ttu-id="15772-180">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="15772-180">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="15772-181">Проверьте сведения о кредитной карте для тестирования покупок</span><span class="sxs-lookup"><span data-stu-id="15772-181">Test credit card information to do test purchases</span></span>

<span data-ttu-id="15772-182">Для выполнения проверочных проводок на сайте можно использовать следующие данные пробной кредитной карты:</span><span class="sxs-lookup"><span data-stu-id="15772-182">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="15772-183">**Номер карты:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="15772-183">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="15772-184">**Дата окончания срока действия:** 10/20</span><span class="sxs-lookup"><span data-stu-id="15772-184">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="15772-185">**Контрольный код карты (CVV):** 737</span><span class="sxs-lookup"><span data-stu-id="15772-185">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="15772-186">Никогда не следует пытаться использовать фактические сведения кредитной карты на тестовых сайтах при любых обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="15772-186">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="15772-187">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="15772-187">Next steps</span></span>

<span data-ttu-id="15772-188">После завершения этапов подготовки и конфигурации вы можете начать использовать ознакомительную среду.</span><span class="sxs-lookup"><span data-stu-id="15772-188">After the provisioning and configuration steps are completed, you can start to use your evaluation environment.</span></span> <span data-ttu-id="15772-189">Используйте URL-адрес конструктора сайтов Commerce, чтобы перейти к взаимодействию разработки.</span><span class="sxs-lookup"><span data-stu-id="15772-189">Use the Commerce site builder URL to go to the authoring experience.</span></span> <span data-ttu-id="15772-190">Используйте URL-адрес сайта Commerce, чтобы перейти к взаимодействию с сайтом клиента Retail.</span><span class="sxs-lookup"><span data-stu-id="15772-190">Use the Commerce site URL to go to the retail customer site experience.</span></span>

<span data-ttu-id="15772-191">Чтобы настроить дополнительные функции для ознакомительной среды Commerce, см. [Настройка дополнительных функций для ознакомительной среды Commerce](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="15772-191">To configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="15772-192">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="15772-192">Additional resources</span></span>

[<span data-ttu-id="15772-193">Обзор ознакомительной среды Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="15772-193">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="15772-194">Подготовка ознакомительной среды Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="15772-194">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="15772-195">Настройка дополнительных функций ознакомительной среды Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="15772-195">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="15772-196">Настройка BOPIS в ознакомительной среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="15772-196">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="15772-197">Вопросы и ответы по ознакомительной среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="15772-197">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="15772-198">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="15772-198">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="15772-199">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="15772-199">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="15772-200">Портал Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="15772-200">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="15772-201">Веб-сайт Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="15772-201">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
