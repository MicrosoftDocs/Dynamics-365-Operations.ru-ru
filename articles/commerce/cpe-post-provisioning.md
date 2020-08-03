---
title: Настройка ознакомительной среды Dynamics 365 Commerce
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
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6a1ae960f0f530104af7bdea9a8fcb78b01571f5
ms.sourcegitcommit: 5175e3fae432016246244cf70fe05465f43de88c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/17/2020
ms.locfileid: "3599732"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="28a71-103">Настройка ознакомительной среды Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="28a71-103">Configure a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="28a71-104">В этой теме объясняется, как настроить ознакомительную среду Microsoft Dynamics 365 Commerce после ее предоставления.</span><span class="sxs-lookup"><span data-stu-id="28a71-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce evaluation environment after it's provisioned.</span></span>

## <a name="overview"></a><span data-ttu-id="28a71-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="28a71-105">Overview</span></span>

<span data-ttu-id="28a71-106">Выполните процедуры в этой теме только после того, как ваша ознакомительная среда Commerce была создана.</span><span class="sxs-lookup"><span data-stu-id="28a71-106">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned.</span></span> <span data-ttu-id="28a71-107">Для получения информации о том, как предоставить ознакомительную среду Commerce, см. в [Обеспечение ознакомительной среды Commerce](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="28a71-107">For information about how to provision your Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

<span data-ttu-id="28a71-108">После того как ознакомительная среда Commerce была полностью подготовлена, необходимо завершить дополнительные этапы конфигурации после подготовки, прежде чем вы сможете приступить к оценке среды.</span><span class="sxs-lookup"><span data-stu-id="28a71-108">After your Commerce evaluation environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="28a71-109">Для выполнения этих шагов необходимо использовать Microsoft Dynamics Lifecycle Services (LCS) и Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="28a71-109">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS) and Dynamics 365 Commerce.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="28a71-110">Перед началом</span><span class="sxs-lookup"><span data-stu-id="28a71-110">Before you start</span></span>

1. <span data-ttu-id="28a71-111">Выполните вход на [портал LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="28a71-111">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="28a71-112">Перейдите к своему проекту.</span><span class="sxs-lookup"><span data-stu-id="28a71-112">Go to your project.</span></span>
1. <span data-ttu-id="28a71-113">В верхнем меню выберите **Размещенные в облаке среды**.</span><span class="sxs-lookup"><span data-stu-id="28a71-113">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="28a71-114">Выберите среду из списка.</span><span class="sxs-lookup"><span data-stu-id="28a71-114">Select your environment in the list.</span></span>
1. <span data-ttu-id="28a71-115">Щелкните **Войти в среду** в сведениях о среде с правой стороны.</span><span class="sxs-lookup"><span data-stu-id="28a71-115">In the environment information on the right, select **Log on to environment**.</span></span> <span data-ttu-id="28a71-116">Вы будете отправлены в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="28a71-116">You will be sent to Commerce headquarters.</span></span>
1. <span data-ttu-id="28a71-117">Убедитесь, что выбрано юридическое лицо **USRT** (верхний правый угол).</span><span class="sxs-lookup"><span data-stu-id="28a71-117">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

<span data-ttu-id="28a71-118">Во время действий после подготовки в модуле Commerce Headquarters убедитесь, что всегда выбрано юридическое лицо **USRT**.</span><span class="sxs-lookup"><span data-stu-id="28a71-118">During post-provisioning activities in Commerce headquarters, make sure that the **USRT** legal entity is always selected.</span></span>

## <a name="configure-the-point-of-sale"></a><span data-ttu-id="28a71-119">Настройка POS</span><span class="sxs-lookup"><span data-stu-id="28a71-119">Configure the point of sale</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="28a71-120">Связывание работника с вашим удостоверением</span><span class="sxs-lookup"><span data-stu-id="28a71-120">Associate a worker with your identity</span></span>

<span data-ttu-id="28a71-121">Чтобы связать работника с вашим удостоверением, выполните следующие действия в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="28a71-121">To associate a worker with your identity, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="28a71-122">Используя меню в левой части, перейдите к **Модули \> Retail и commerce \> Сотрудники \> Работники**.</span><span class="sxs-lookup"><span data-stu-id="28a71-122">Use the menu on the left to go to **Modules \> Retail and commerce \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="28a71-123">В списке найдите и выберите следующую запись **000713 - Эндрю Колетт (Andrew Collette)**.</span><span class="sxs-lookup"><span data-stu-id="28a71-123">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="28a71-124">На панели операций выберите **Commerce**.</span><span class="sxs-lookup"><span data-stu-id="28a71-124">On the Action Pane, select **Commerce**.</span></span>
1. <span data-ttu-id="28a71-125">Выберите **Ассоциировать существующее удостоверение**.</span><span class="sxs-lookup"><span data-stu-id="28a71-125">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="28a71-126">В поле **Адрес электронной почты**, справа от **Поиск по электронной почте**, введите свой адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="28a71-126">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="28a71-127">Выберите **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="28a71-127">Select **Search**.</span></span>
1. <span data-ttu-id="28a71-128">Выберите запись с вашим именем.</span><span class="sxs-lookup"><span data-stu-id="28a71-128">Select the record that has your name.</span></span>
1. <span data-ttu-id="28a71-129">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="28a71-129">Select **OK**.</span></span>
1. <span data-ttu-id="28a71-130">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="28a71-130">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="28a71-131">Активация облачного POS</span><span class="sxs-lookup"><span data-stu-id="28a71-131">Activate Cloud POS</span></span>

<span data-ttu-id="28a71-132">Чтобы активировать Cloud POS, выполните следующие действия в LCS.</span><span class="sxs-lookup"><span data-stu-id="28a71-132">To activate Cloud POS, follow these steps in LCS.</span></span>

1. <span data-ttu-id="28a71-133">В верхнем меню выберите **Размещенные в облаке среды**.</span><span class="sxs-lookup"><span data-stu-id="28a71-133">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="28a71-134">Выберите среду из списка.</span><span class="sxs-lookup"><span data-stu-id="28a71-134">Select your environment in the list.</span></span>
1. <span data-ttu-id="28a71-135">Щелкните **Войти в Cloud POS** в сведениях о среде с правой стороны.</span><span class="sxs-lookup"><span data-stu-id="28a71-135">In the environment information on the right, select **Log on to Cloud Point of Sale**.</span></span>
1. <span data-ttu-id="28a71-136">Выберите **Далее**, чтобы открыть диалоговое окно **Перед началом**.</span><span class="sxs-lookup"><span data-stu-id="28a71-136">Select **Next** to open the **Before you start** dialog box.</span></span>
1. <span data-ttu-id="28a71-137">Оставьте поле **URL-адрес сервера** без изменений.</span><span class="sxs-lookup"><span data-stu-id="28a71-137">Leave the **Server URL** field as it is.</span></span> <span data-ttu-id="28a71-138">Выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="28a71-138">Select **Next**.</span></span>
1. <span data-ttu-id="28a71-139">Войдите в систему с учетной записью Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="28a71-139">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="28a71-140">В области **Имя магазина** выберите **Сан-Франциско**, затем выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="28a71-140">Under **Store name**, select **San Francisco**, and then select **Next**.</span></span>
1. <span data-ttu-id="28a71-141">В области **Регистрация и устройство** выберите **SANFRAN-1**.</span><span class="sxs-lookup"><span data-stu-id="28a71-141">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="28a71-142">Выберите **Активировать**.</span><span class="sxs-lookup"><span data-stu-id="28a71-142">Select **Activate**.</span></span> <span data-ttu-id="28a71-143">Вы вышли, открылась страница входа POS.</span><span class="sxs-lookup"><span data-stu-id="28a71-143">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="28a71-144">Теперь можно войти во взаимодействие Cloud POS, используя код оператора **000713** и пароль **123**.</span><span class="sxs-lookup"><span data-stu-id="28a71-144">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="28a71-145">Настройка сайта в Commerce</span><span class="sxs-lookup"><span data-stu-id="28a71-145">Set up your site in Commerce</span></span>

<span data-ttu-id="28a71-146">Чтобы начать настраивать ознакомительный сайт в Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="28a71-146">To start to set up your evaluation site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="28a71-147">Войдите в конструктор сайтов, используя URL-адрес, который вы записали при инициализации электронной коммерции во время подготовки (см. [Инициализация электронной коммерции](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="28a71-147">Sign in to site builder by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="28a71-148">Выберите сайт **Fabrikam**, чтобы открыть диалоговое окно настройки сайта.</span><span class="sxs-lookup"><span data-stu-id="28a71-148">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="28a71-149">Выберите домен, в который вы вошли при инициализации электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="28a71-149">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="28a71-150">В качестве канала по умолчанию выберите **Расширенный интернет-магазин Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="28a71-150">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="28a71-151">(Убедитесь, что выбран **расширенный** интернет-магазин.)</span><span class="sxs-lookup"><span data-stu-id="28a71-151">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="28a71-152">В качестве языка по умолчанию выберите **en-us**.</span><span class="sxs-lookup"><span data-stu-id="28a71-152">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="28a71-153">Оставьте значение поля **Путь** как есть.</span><span class="sxs-lookup"><span data-stu-id="28a71-153">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="28a71-154">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="28a71-154">Select **OK**.</span></span> <span data-ttu-id="28a71-155">Появляется список страниц на сайте.</span><span class="sxs-lookup"><span data-stu-id="28a71-155">The list of pages on the site appears.</span></span>

## <a name="enable-jobs"></a><span data-ttu-id="28a71-156">Включение заданий</span><span class="sxs-lookup"><span data-stu-id="28a71-156">Enable jobs</span></span>

<span data-ttu-id="28a71-157">Чтобы включить задания в Commerce, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="28a71-157">To enable jobs in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="28a71-158">Выполните вход в среду (HQ).</span><span class="sxs-lookup"><span data-stu-id="28a71-158">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="28a71-159">Используя меню, расположенное в левой части, перейдите в раздел **Retail и Commerce \> Запросы и отчеты \> Пакетные задания**.</span><span class="sxs-lookup"><span data-stu-id="28a71-159">Use the menu on the left to go to **Retail and commerce \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="28a71-160">Остальные этапы этой процедуры должны быть завершены для каждого из следующих заданий:</span><span class="sxs-lookup"><span data-stu-id="28a71-160">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="28a71-161">Обработать уведомление по электронной почте о заказе розничной торговли</span><span class="sxs-lookup"><span data-stu-id="28a71-161">Process retail order email notification</span></span>
    * <span data-ttu-id="28a71-162">Доступность продукта</span><span class="sxs-lookup"><span data-stu-id="28a71-162">Product availability</span></span>
    * <span data-ttu-id="28a71-163">P-0001</span><span class="sxs-lookup"><span data-stu-id="28a71-163">P-0001</span></span>
    * <span data-ttu-id="28a71-164">Задание синхронизации заказов</span><span class="sxs-lookup"><span data-stu-id="28a71-164">Synchronize orders job</span></span>

1. <span data-ttu-id="28a71-165">Используйте быструю фильтрацию для поиска задания по его названию.</span><span class="sxs-lookup"><span data-stu-id="28a71-165">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="28a71-166">Если статус задания — **Выполняется**, выполните следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="28a71-166">If the status of the job is **Executing**, follow these steps:</span></span>

    1. <span data-ttu-id="28a71-167">Выберите запись.</span><span class="sxs-lookup"><span data-stu-id="28a71-167">Select the record.</span></span>
    1. <span data-ttu-id="28a71-168">В области действий щелкните вкладку **Пакетное задание**, выберите **Изменить статус**.</span><span class="sxs-lookup"><span data-stu-id="28a71-168">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="28a71-169">Выберите **Отменяется**, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="28a71-169">Select **Canceling**, and then select **OK**.</span></span>

<span data-ttu-id="28a71-170">Кроме того, можно установить интервал повторения равным одной (1) минуте для следующих заданий:</span><span class="sxs-lookup"><span data-stu-id="28a71-170">Optionally, you can also set the recurrence interval to one (1) minute for the following jobs:</span></span>

* <span data-ttu-id="28a71-171">Задание обработки уведомления по электронной почте о заказе розничной торговли</span><span class="sxs-lookup"><span data-stu-id="28a71-171">Process retail order email notification job</span></span>
* <span data-ttu-id="28a71-172">Задание P-0001</span><span class="sxs-lookup"><span data-stu-id="28a71-172">P-0001 job</span></span>
* <span data-ttu-id="28a71-173">Задание синхронизации заказов</span><span class="sxs-lookup"><span data-stu-id="28a71-173">Synchronize orders job</span></span>

### <a name="run-full-data-synchronization"></a><span data-ttu-id="28a71-174">Выполнение полной синхронизации данных</span><span class="sxs-lookup"><span data-stu-id="28a71-174">Run full data synchronization</span></span>

<span data-ttu-id="28a71-175">Чтобы запустить полную синхронизацию данных в Commerce, выполните следующие действия в Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="28a71-175">To run full data synchronization in Commerce, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="28a71-176">Используя меню в левой части, перейдите к пункту **Модули \> Retail и Commerce \> Настройка центрального офиса \> Планировщик Commerce \> База данных канала**.</span><span class="sxs-lookup"><span data-stu-id="28a71-176">Use the menu on the left to go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="28a71-177">Выберите канал с именем **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="28a71-177">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="28a71-178">На панели операций выберите **Полная синхронизация данных**.</span><span class="sxs-lookup"><span data-stu-id="28a71-178">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="28a71-179">Введите график распределения **9999**.</span><span class="sxs-lookup"><span data-stu-id="28a71-179">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="28a71-180">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="28a71-180">Select **OK**.</span></span>
1. <span data-ttu-id="28a71-181">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="28a71-181">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="28a71-182">Проверьте сведения о кредитной карте для тестирования покупок</span><span class="sxs-lookup"><span data-stu-id="28a71-182">Test credit card information to do test purchases</span></span>

<span data-ttu-id="28a71-183">Для выполнения проверочных проводок на сайте можно использовать следующие данные пробной кредитной карты:</span><span class="sxs-lookup"><span data-stu-id="28a71-183">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="28a71-184">**Номер карты:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="28a71-184">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="28a71-185">**Дата окончания срока действия:** 10/20</span><span class="sxs-lookup"><span data-stu-id="28a71-185">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="28a71-186">**Контрольный код карты (CVV):** 737</span><span class="sxs-lookup"><span data-stu-id="28a71-186">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="28a71-187">Никогда не следует пытаться использовать фактические сведения кредитной карты на тестовых сайтах при любых обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="28a71-187">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="28a71-188">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="28a71-188">Next steps</span></span>

<span data-ttu-id="28a71-189">После завершения этапов подготовки и конфигурации вы можете начать использовать ознакомительную среду.</span><span class="sxs-lookup"><span data-stu-id="28a71-189">After the provisioning and configuration steps are completed, you can start to use your evaluation environment.</span></span> <span data-ttu-id="28a71-190">Используйте URL-адрес конструктора сайтов Commerce, чтобы перейти к взаимодействию разработки.</span><span class="sxs-lookup"><span data-stu-id="28a71-190">Use the Commerce site builder URL to go to the authoring experience.</span></span> <span data-ttu-id="28a71-191">Используйте URL-адрес сайта Commerce, чтобы перейти к взаимодействию с сайтом клиента Retail.</span><span class="sxs-lookup"><span data-stu-id="28a71-191">Use the Commerce site URL to go to the retail customer site experience.</span></span>

<span data-ttu-id="28a71-192">Чтобы настроить дополнительные функции для ознакомительной среды Commerce, см. [Настройка дополнительных функций для ознакомительной среды Commerce](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="28a71-192">To configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="28a71-193">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="28a71-193">Additional resources</span></span>

[<span data-ttu-id="28a71-194">Обзор ознакомительной среды Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="28a71-194">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="28a71-195">Подготовка ознакомительной среды Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="28a71-195">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="28a71-196">Настройка дополнительных функций ознакомительной среды Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="28a71-196">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="28a71-197">Настройка BOPIS в ознакомительной среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="28a71-197">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="28a71-198">Вопросы и ответы по ознакомительной среде Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="28a71-198">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="28a71-199">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="28a71-199">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="28a71-200">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="28a71-200">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="28a71-201">Портал Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="28a71-201">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="28a71-202">Веб-сайт Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="28a71-202">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
