---
title: Доступ к метаданным приложения с помощью подключенных приложений
description: В этом разделе описывается, как пользователь службы Regulatory Configuration Service (RCS) может создать новое сопоставление модели электронной отчетности (ER) с помощью метаданных в Finance and Operations.
author: NickSelin
manager: AnnBe
ms.date: 06/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a476163ba6f66ab60ed8bfea6198d02f13ac5136
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182723"
---
# <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="307c7-103">Доступ к метаданным приложения с помощью подключенных приложений</span><span class="sxs-lookup"><span data-stu-id="307c7-103">Access application metadata by using connected applications</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="307c7-104">В следующих шагах поясняется, как пользователь службы Regulatory Configuration Service (RCS) с ролью "Системный администратор" или "Разработчик электронной отчетности" может создать новое сопоставление модели электронной отчетности с помощью метаданных в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="307c7-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using metadata in Finance and Operations.</span></span> <span data-ttu-id="307c7-105">Доступ к метаданным приложения производится в сети с помощью подключенного приложения RCS.</span><span class="sxs-lookup"><span data-stu-id="307c7-105">Application metadata will be accessed online by using the RCS connected application.</span></span> <span data-ttu-id="307c7-106">Образец сопоставления модели ER будет настроен для доступа к проводкам внешней торговли.</span><span class="sxs-lookup"><span data-stu-id="307c7-106">Sample ER model mapping will be configured to access foreign trade transactions.</span></span> <span data-ttu-id="307c7-107">Для выполнения этих шагов в RCS необходимо сначала выполнить шаги в теме [Создание поставщика конфигурации и установка его в качестве активного](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="307c7-107">To complete these steps, in RCS you must first complete the steps in the topic, [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="307c7-108">Если вы не выполнили шаги в теме [Доступ к метаданным приложения с помощью конфигурации электронной отчетности](access-application-metadata-er-configuration.md), перейдите на [страницу примеров электронной отчетности](https://go.microsoft.com/fwlink/?linkid=862266), чтобы загрузить и сохранить следующие конфигурации электронной отчетности: Метаданные внешней торговли.xml; Модель внешней торговли.xml; Сопоставление внешней торговли.xml, а затем выполните шаги из процедуры.</span><span class="sxs-lookup"><span data-stu-id="307c7-108">If you have not completed the steps in the topic, [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md), go to the [Electronic reporting examples page](https://go.microsoft.com/fwlink/?linkid=862266) to download and save the following ER configurations: Foreign trade metadata.xml; Foreign trade model.xml; Foreign trade mapping.xml, and then complete the steps in the procedure.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="307c7-109">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="307c7-109">Prerequisites</span></span>
1. <span data-ttu-id="307c7-110">Перейдите в раздел **Все рабочие области** > **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="307c7-110">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="307c7-111">Убедитесь, что поставщик конфигурации для демонстрационной компании Litware, Inc. доступен и помечен как **Активный**.</span><span class="sxs-lookup"><span data-stu-id="307c7-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="307c7-112">Если вы не видите этого поставщика конфигурации, необходимо сначала выполнить шаги в процедуре [Создание поставщика конфигурации и пометка его как активного](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="307c7-112">If you don’t see this configuration provider, complete the steps in the procedure [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="get-required-er-configurations"></a><span data-ttu-id="307c7-113">Получение необходимых конфигураций электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="307c7-113">Get required ER configurations</span></span>
1. <span data-ttu-id="307c7-114">Щелкните **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="307c7-114">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="307c7-115">Если вы уже выполнили шаги из процедуры [(RCS) Доступ к метаданным приложения с помощью конфигурации электронной отчетности](access-application-metadata-er-configuration.md), у вас уже имеются все необходимые конфигурации ER (конфигурации метаданных, моделей и сопоставлений внешней торговли) в текущем экземпляре RCS.</span><span class="sxs-lookup"><span data-stu-id="307c7-115">If you already completed the steps in the [(RCS) Access application metadata by using ER configuration](access-application-metadata-er-configuration.md) procedure, you already have all necessary ER configurations (foreign trade metadata, model and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="307c7-116">Все остальные шаги в этой подзадаче можно пропустить.</span><span class="sxs-lookup"><span data-stu-id="307c7-116">You can skip all the remaining steps of this sub-task.</span></span> 
3. <span data-ttu-id="307c7-117">Щелкните **Обменять**.</span><span class="sxs-lookup"><span data-stu-id="307c7-117">Click **Exchange**.</span></span> 
4. <span data-ttu-id="307c7-118">Щелкните **Загрузить из XML-файла**.</span><span class="sxs-lookup"><span data-stu-id="307c7-118">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="307c7-119">Щелкните **Обзор** и выберите файл **Метаданные внешней торговли.xml**.</span><span class="sxs-lookup"><span data-stu-id="307c7-119">Click **Browse** and select the **Foreign trade metadata.xml** file.</span></span> 
6. <span data-ttu-id="307c7-120">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="307c7-120">Click **OK**.</span></span> 
7. <span data-ttu-id="307c7-121">Щелкните **Обменять**.</span><span class="sxs-lookup"><span data-stu-id="307c7-121">Click **Exchange**.</span></span> 
8. <span data-ttu-id="307c7-122">Щелкните **Загрузить из XML-файла**.</span><span class="sxs-lookup"><span data-stu-id="307c7-122">Click **Load from XML file**.</span></span> 
9. <span data-ttu-id="307c7-123">Щелкните **Обзор** и выберите файл **Модель внешней торговли.xml**.</span><span class="sxs-lookup"><span data-stu-id="307c7-123">Click **Browse** and select the **Foreign trade model.xml** file.</span></span> 
10. <span data-ttu-id="307c7-124">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="307c7-124">Click **OK**.</span></span> 
11. <span data-ttu-id="307c7-125">Щелкните **Обменять**.</span><span class="sxs-lookup"><span data-stu-id="307c7-125">Click **Exchange**.</span></span> 
12. <span data-ttu-id="307c7-126">Щелкните **Загрузить из XML-файла**.</span><span class="sxs-lookup"><span data-stu-id="307c7-126">Click **Load from XML file**.</span></span> 
13. <span data-ttu-id="307c7-127">Щелкните **Обзор** и выберите файл **Сопоставление внешней торговли.xml**.</span><span class="sxs-lookup"><span data-stu-id="307c7-127">Click **Browse** and select the **Foreign trade mapping.xml** file.</span></span> 
14. <span data-ttu-id="307c7-128">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="307c7-128">Click **OK**.</span></span> 

## <a name="register-a-connected-application"></a><span data-ttu-id="307c7-129">Регистрация подключенного приложения</span><span class="sxs-lookup"><span data-stu-id="307c7-129">Register a connected application</span></span>
1. <span data-ttu-id="307c7-130">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="307c7-130">Close the page.</span></span> 
2. <span data-ttu-id="307c7-131">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="307c7-131">Close the page.</span></span> 
3. <span data-ttu-id="307c7-132">Перейдите в раздел **Все рабочие области** > **Электронная отчетность**.</span><span class="sxs-lookup"><span data-stu-id="307c7-132">Go to **All workspaces** > **Electronic reporting**.</span></span> 
4. <span data-ttu-id="307c7-133">Щелкните **Подключенные приложения**.</span><span class="sxs-lookup"><span data-stu-id="307c7-133">Click **Connected applications**.</span></span> 
5. <span data-ttu-id="307c7-134">Убедитесь, что настроенное приложение основано на Azura, и что оно доступно для текущего пользователя RCS.</span><span class="sxs-lookup"><span data-stu-id="307c7-134">Make sure that the configured application is Azura based and accessible for the current RCS user.</span></span> <span data-ttu-id="307c7-135">Также необходимо, чтобы текущий пользователь RCS имел доступ к выбранному приложению и был зарегистрирован в качестве пользователя данного приложения в роли, которая дает ему право доступа к метаданным приложения.</span><span class="sxs-lookup"><span data-stu-id="307c7-135">It is also required that the current RCS user has access to the selected application and has been registered as a user of this application playing a role giving him privileges to access application’s metadata.</span></span> 
6. <span data-ttu-id="307c7-136">Нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="307c7-136">Click **New**.</span></span> 
7. <span data-ttu-id="307c7-137">В поле **Имя** введите "MyConnectedApp".</span><span class="sxs-lookup"><span data-stu-id="307c7-137">In the **Name** field, type 'MyConnectedApp'.</span></span> 
8. <span data-ttu-id="307c7-138">В поле **Приложение** введите "https:// mycompany.operations.dynamics.com".</span><span class="sxs-lookup"><span data-stu-id="307c7-138">In the **Application** field, type 'https:// mycompany.operations.dynamics.com'.</span></span> 
9. <span data-ttu-id="307c7-139">В поле **Клиент** введите "mycompany.onmicrosoft.com".</span><span class="sxs-lookup"><span data-stu-id="307c7-139">In the **Tenant** field, type ‘mycompany.onmicrosoft.com’.</span></span> 
10. <span data-ttu-id="307c7-140">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="307c7-140">Click **Save**.</span></span> 
11. <span data-ttu-id="307c7-141">При проверке подключения к настроенному приложению на странице **Подключение к удаленному приложению** щелкните **Щелкните здесь, чтобы подключиться к выбранному удаленному приложению**.</span><span class="sxs-lookup"><span data-stu-id="307c7-141">When you check connection to configured application, on the **Connect to remote application** page click **Click here to connect to selected remote application** link.</span></span> 
12. <span data-ttu-id="307c7-142">Щелкните **Проверить подключение**.</span><span class="sxs-lookup"><span data-stu-id="307c7-142">Click **Check connection**.</span></span> 
13. <span data-ttu-id="307c7-143">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="307c7-143">Click **Close**.</span></span> 
14. <span data-ttu-id="307c7-144">После успешной проверки подключения сведения о версии и клиенте будут обновлены для настроенного приложения в текущей сетке.</span><span class="sxs-lookup"><span data-stu-id="307c7-144">When the connection validation succeeded, version and tenant details will be updated for the configured application in the current grid.</span></span> 

## <a name="review-existing-model-mapping-configuration"></a><span data-ttu-id="307c7-145">Проверка существующей конфигурации сопоставлений модели</span><span class="sxs-lookup"><span data-stu-id="307c7-145">Review existing model mapping configuration</span></span>
1. <span data-ttu-id="307c7-146">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="307c7-146">Close the page.</span></span> 
2. <span data-ttu-id="307c7-147">Щелкните **Конфигурации отчетности**.</span><span class="sxs-lookup"><span data-stu-id="307c7-147">Click **Reporting configurations**.</span></span> 
3. <span data-ttu-id="307c7-148">В дереве разверните узел **Модель внешней торговли**.</span><span class="sxs-lookup"><span data-stu-id="307c7-148">In the tree, expand **Foreign trade model**.</span></span> 
4. <span data-ttu-id="307c7-149">В дереве выберите **Модель внешней торговли\Сопоставление внешней торговли**.</span><span class="sxs-lookup"><span data-stu-id="307c7-149">In the tree, select **Foreign trade model\Foreign trade mapping**.</span></span> 
5. <span data-ttu-id="307c7-150">Разверните раздел **Необходимые условия**.</span><span class="sxs-lookup"><span data-stu-id="307c7-150">Expand the **Prerequisites** section.</span></span> 

> [!NOTE]
> <span data-ttu-id="307c7-151">В настоящее время это сопоставление ссылается на конфигурацию метаданных.</span><span class="sxs-lookup"><span data-stu-id="307c7-151">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="307c7-152">Метаданные приложения из этой конфигурации будут предлагаться при разработке этого сопоставления моделей.</span><span class="sxs-lookup"><span data-stu-id="307c7-152">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

6. <span data-ttu-id="307c7-153">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="307c7-153">Click **Designer**.</span></span> 
7. <span data-ttu-id="307c7-154">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="307c7-154">Click **Designer**.</span></span> 
8. <span data-ttu-id="307c7-155">В дереве выберите узел **Dynamics 365 for Operations\Записи таблиц**.</span><span class="sxs-lookup"><span data-stu-id="307c7-155">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
9. <span data-ttu-id="307c7-156">Щелкните **Добавить корень**.</span><span class="sxs-lookup"><span data-stu-id="307c7-156">Click **Add root**.</span></span> 
10. <span data-ttu-id="307c7-157">В поле **Таблица** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="307c7-157">In the **Table** field, enter or select a value.</span></span> 

> [!NOTE]
> <span data-ttu-id="307c7-158">В настоящее время это сопоставление ссылается на конфигурацию метаданных.</span><span class="sxs-lookup"><span data-stu-id="307c7-158">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="307c7-159">Метаданные приложения из этой конфигурации будут предлагаться при разработке этого сопоставления моделей.</span><span class="sxs-lookup"><span data-stu-id="307c7-159">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

11. <span data-ttu-id="307c7-160">Щелкните **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="307c7-160">Click **Cancel**.</span></span> 
12. <span data-ttu-id="307c7-161">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="307c7-161">Close the page.</span></span> 
13. <span data-ttu-id="307c7-162">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="307c7-162">Close the page.</span></span> 

## <a name="assign-connected-application-to-model-mapping"></a><span data-ttu-id="307c7-163">Назначение подключенного приложения сопоставлению модели</span><span class="sxs-lookup"><span data-stu-id="307c7-163">Assign connected application to model mapping</span></span> 
1. <span data-ttu-id="307c7-164">Выберите **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="307c7-164">Click **Edit**.</span></span> 
2. <span data-ttu-id="307c7-165">Выберите приложение **MyConnectedApp**.</span><span class="sxs-lookup"><span data-stu-id="307c7-165">Select **MyConnectedApp** application.</span></span> 

> [!NOTE]
> <span data-ttu-id="307c7-166">В настоящее время это сопоставление ссылается на метаданные выбранного подключенного приложения.</span><span class="sxs-lookup"><span data-stu-id="307c7-166">Currently, this mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="307c7-167">Если это же сопоставление ссылается одновременно на конфигурацию метаданных и подключенное приложение, будут использоваться метаданные подключенного приложения.</span><span class="sxs-lookup"><span data-stu-id="307c7-167">When the same mapping refers to metadata configuration and connected application at the same time, metadata of the connected application will be used.</span></span> 

3. <span data-ttu-id="307c7-168">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="307c7-168">Click **Designer**.</span></span> 
4. <span data-ttu-id="307c7-169">Выберите **Конструктор**.</span><span class="sxs-lookup"><span data-stu-id="307c7-169">Click **Designer**.</span></span> 
5. <span data-ttu-id="307c7-170">В дереве выберите узел **Dynamics 365 for Operations\Записи таблиц**.</span><span class="sxs-lookup"><span data-stu-id="307c7-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
6. <span data-ttu-id="307c7-171">Щелкните **Добавить корень**.</span><span class="sxs-lookup"><span data-stu-id="307c7-171">Click **Add root**.</span></span> 
7. <span data-ttu-id="307c7-172">В поле **Таблица** введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="307c7-172">In the **Table** field, enter or select a value.</span></span> 

> [!NOTE]
> <span data-ttu-id="307c7-173">Теперь предлагается более двух таблиц приложений, поскольку в этом сопоставлении используются все метаданные подключенного приложения, которое было назначено для него.</span><span class="sxs-lookup"><span data-stu-id="307c7-173">More than two application tables were offered now as this mapping uses all the metadata of the connected application that has been assigned for it.</span></span> 

8. <span data-ttu-id="307c7-174">Щелкните **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="307c7-174">Click **Cancel**.</span></span> 
9. <span data-ttu-id="307c7-175">Щелкните **Проверить**.</span><span class="sxs-lookup"><span data-stu-id="307c7-175">Click **Validate**.</span></span> 

> [!NOTE]
> <span data-ttu-id="307c7-176">Мы успешно привязали элементы модели данных к элементам источников данных, которые описаны с помощью подробных сведений метаданных подключенного приложения, которое было назначено для этого сопоставления.</span><span class="sxs-lookup"><span data-stu-id="307c7-176">We successfully bound elements of data model with items of data sources that are described by using details of metadata of the connected application that has been assigned for this mapping.</span></span> 

10. <span data-ttu-id="307c7-177">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="307c7-177">Close the page.</span></span> 
11. <span data-ttu-id="307c7-178">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="307c7-178">Close the page.</span></span> 

<span data-ttu-id="307c7-179">Когда необходимо оценить сопоставление модели с помощью метаданных другой версии приложения, зарегистрируйте другое подключенное приложение, назначьте его этому сопоставлению модели и проверьте его по новым метаданным.</span><span class="sxs-lookup"><span data-stu-id="307c7-179">When you need to evaluate this model mapping by using metadata of a different version application, register another connected application, assign it to this model mapping and validate it against new metadata.</span></span>
