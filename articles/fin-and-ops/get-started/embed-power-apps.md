---
title: "Внедрение PowerApps"
description: "В этом разделе описывается, как внедрить PowerApps в клиент Finance and Operations для расширения функциональных возможностей продукта."
author: jasongre
manager: AnnBe
ms.date: 03/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.translationtype: HT
ms.sourcegitcommit: 454368ab5a467002ebf973db97fd98e31885dfe0
ms.openlocfilehash: 0fd0b1e5f94e39455b3c0799c89eea5a59444ad7
ms.contentlocale: ru-ru
ms.lasthandoff: 03/23/2018

---

# <a name="embed-powerapps"></a><span data-ttu-id="e5146-103">Внедрение PowerApps</span><span class="sxs-lookup"><span data-stu-id="e5146-103">Embed PowerApps</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/pre-release.md)] 

<span data-ttu-id="e5146-104">В обновлении платформы 14 Microsoft Dynamics 365 for Finance and Operations поддерживает интеграцию с Microsoft PowerApps, службой, которая позволяет разработчикам и обычным пользователям создавать пользовательские бизнес-приложения для мобильных устройств, планшетов и интернета без написания кода.</span><span class="sxs-lookup"><span data-stu-id="e5146-104">In Platform update 14, Microsoft Dynamics 365 for Finance and Operations supports integration with Microsoft PowerApps, a service for developers and non-technical users to build custom business apps for mobile devices, tablets, and the web without writing code.</span></span> <span data-ttu-id="e5146-105">Затем приложения PowerApps, разработанные вами, вашей организации или более широкой экосистемой можно внедрить в клиент Finance and Operations для расширения функциональности продукта.</span><span class="sxs-lookup"><span data-stu-id="e5146-105">PowerApps developed by you, your organization, or the broader ecosystem can then be embedded in the Finance and Operations client to augment the product's functionality.</span></span> <span data-ttu-id="e5146-106">Например, можно построить приложение PowerApp для дополнения Finance and Operations информацией, извлеченной из другой системы.</span><span class="sxs-lookup"><span data-stu-id="e5146-106">For example, you might build a PowerApp to supplement Finance and Operations with information retrieved from another system.</span></span>  

## <a name="adding-an-embedded-powerapp-to-a-page"></a><span data-ttu-id="e5146-107">Добавление внедренного приложения PowerApp на страницу</span><span class="sxs-lookup"><span data-stu-id="e5146-107">Adding an embedded PowerApp to a page</span></span>
### <a name="overview"></a><span data-ttu-id="e5146-108">Обзор</span><span class="sxs-lookup"><span data-stu-id="e5146-108">Overview</span></span>
<span data-ttu-id="e5146-109">Перед внедрением приложения PowerApp в клиент Finance and Operations необходимо сначала найти или построить приложение PowerApp с требуемыми визуальными элементами и/или функциональными возможностями.</span><span class="sxs-lookup"><span data-stu-id="e5146-109">Before embedding a PowerApp into the Finance and Operations client, you first need to find or build a PowerApp with the desired visuals and/or functionality.</span></span> <span data-ttu-id="e5146-110">Мы не будет здесь подробно описывать процесс построения приложения PowerApp.</span><span class="sxs-lookup"><span data-stu-id="e5146-110">We will not describe the detailed process for building a PowerApp here.</span></span> <span data-ttu-id="e5146-111">Раздел [Знакомство с PowerApps](https://docs.microsoft.com/en-us/powerapps/getting-started) является хорошей начальной точкой, если вы не знакомы с PowerApps.</span><span class="sxs-lookup"><span data-stu-id="e5146-111">The [Introduction to PowerApps](https://docs.microsoft.com/en-us/powerapps/getting-started) topic is a good starting point if you are new to PowerApps.</span></span>

<span data-ttu-id="e5146-112">Когда вы готовы для внедрения определенного приложения PowerApp, можно выбрать один из двух способов доступа к приложению PowerApp на странице, который лучше подходит для вашего сценария.</span><span class="sxs-lookup"><span data-stu-id="e5146-112">When you are ready to embed a specific PowerApp, you can choose between one of two ways of accessing the PowerApp on a page, whichever route better fits your scenario.</span></span> <span data-ttu-id="e5146-113">Первый способ — через кнопку PowerApps, которая была добавлена в стандартной области действий.</span><span class="sxs-lookup"><span data-stu-id="e5146-113">The first way is through the PowerApps button that has been added to the standard Action Pane.</span></span> <span data-ttu-id="e5146-114">Добавленные с помощью этого механизма приложения PowerApps будут отображаться как пункты меню внутри меню кнопки PowerApps.</span><span class="sxs-lookup"><span data-stu-id="e5146-114">PowerApps added using this mechanism will appear as menu items inside the PowerApps menu button.</span></span> <span data-ttu-id="e5146-115">При выборе каждый их этих пунктов меню открывает боковую область, содержащую внедренное приложение PowerApp.</span><span class="sxs-lookup"><span data-stu-id="e5146-115">When selected, each of these menu items will open a side pane that contains the embedded PowerApp.</span></span> <span data-ttu-id="e5146-116">Можно также выбрать отображение приложения PowerApp непосредственно на странице в виде новой вкладки, экспресс-вкладки, колонки или нового раздела в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e5146-116">Alternatively, you may choose to show a PowerApp directly on a page as a new tab, FastTab, blade, or as a new section in a workspace.</span></span> 

<span data-ttu-id="e5146-117">При настройке вашего внедренного приложения PowerApp в Finance and Operations можно выбрать одно поле, которое необходимо отправить в качестве входных данных в приложение PowerApp.</span><span class="sxs-lookup"><span data-stu-id="e5146-117">When configuring your embedded PowerApp in Finance and Operations, you can select a single field that you want to send as input to the PowerApp.</span></span> <span data-ttu-id="e5146-118">Это позволяет приложению PowerApp реагировать на основе данных, просматриваемых в данный момент в Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e5146-118">This allows the PowerApp to be responsive based on the data that you are currently viewing in Finance and Operations.</span></span>  

### <a name="details"></a><span data-ttu-id="e5146-119">Подробности</span><span class="sxs-lookup"><span data-stu-id="e5146-119">Details</span></span>
<span data-ttu-id="e5146-120">Приведенные ниже инструкции демонстрируют, как внедрить в веб-клиент Finance and Operations приложение PowerApp.</span><span class="sxs-lookup"><span data-stu-id="e5146-120">The following instructions show how to embed a PowerApp into the Finance and Operations web client.</span></span>  

1. <span data-ttu-id="e5146-121">Перейдите на страницу, на которой вы хотите внедрить приложение PowerApp.</span><span class="sxs-lookup"><span data-stu-id="e5146-121">Go to the page where you would like to embed the PowerApp.</span></span> <span data-ttu-id="e5146-122">Это будет та же страница, которая содержит любые данные, который должны быть переданы в приложение PowerApp в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="e5146-122">This will be the same page that contains any data that needs to be passed to the PowerApp as input.</span></span>  
2. <span data-ttu-id="e5146-123">Откройте область **Вставить PowerApp**:</span><span class="sxs-lookup"><span data-stu-id="e5146-123">Open the **Insert a PowerApp** pane:</span></span>
   - <span data-ttu-id="e5146-124">Щелкните **Параметры**, затем выберите **Персонализировать эту форму**.</span><span class="sxs-lookup"><span data-stu-id="e5146-124">Click **Options**, and then select **Personalize this form**.</span></span> <span data-ttu-id="e5146-125">В меню **Вставить** выберите **PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="e5146-125">Under the **Insert** menu, choose **PowerApp**.</span></span> <span data-ttu-id="e5146-126">Наконец, выберите область, в которой вы хотите добавить приложение PowerApp.</span><span class="sxs-lookup"><span data-stu-id="e5146-126">Finally, select the region where you would like to add the PowerApp.</span></span> <span data-ttu-id="e5146-127">Если требуется внедрить приложение PowerApp в меню кнопки PowerApps, выберите область действий.</span><span class="sxs-lookup"><span data-stu-id="e5146-127">If you want to embed the PowerApp under the PowerApps menu button, choose the Action Pane.</span></span> <span data-ttu-id="e5146-128">Если требуется внедрить приложение PowerApp непосредственно на страницу, выберите соответствующую вкладку, экспресс-вкладку, колонку или раздела (если вы находитесь в рабочей области).</span><span class="sxs-lookup"><span data-stu-id="e5146-128">If you want to embed the PowerApp directly onto the page, choose the appropriate tab, FastTab, blade, or section (if you're on a workspace).</span></span>   
   - <span data-ttu-id="e5146-129">Если доступ к приложению PowerApp будет осуществляться с помощью меню кнопки PowerApps, можно также щелкнуть кнопку меню **PowerApps** на стандартной панели действий, а затем выбрать **Вставить PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="e5146-129">If the PowerApp will be accessed using the PowerApps menu button, you can alternatively click the **PowerApps** menu button in the standard Action Pane, and then select **Insert a PowerApp**.</span></span>  
3. <span data-ttu-id="e5146-130">Настройка внедренного приложения PowerApp:</span><span class="sxs-lookup"><span data-stu-id="e5146-130">Configure the embedded PowerApp:</span></span>
   - <span data-ttu-id="e5146-131">Поле **Имя** показывает текст, отображаемый для кнопки или вкладки, которая будет содержать внедренное приложение PowerApp.</span><span class="sxs-lookup"><span data-stu-id="e5146-131">The **Name** field indicates the text shown for the button or tab that will contain the embedded PowerApp.</span></span> <span data-ttu-id="e5146-132">Часто требуется повторить имя приложения PowerApp в этом поле.</span><span class="sxs-lookup"><span data-stu-id="e5146-132">Oftentimes, you may want to repeat the name of the PowerApp in this field.</span></span>  
   - <span data-ttu-id="e5146-133">**Код приложения** — это идентификатор GUID для приложения PowerApp, которое требуется внедрить.</span><span class="sxs-lookup"><span data-stu-id="e5146-133">**App ID** is the GUID for the PowerApp that you want to embed.</span></span> <span data-ttu-id="e5146-134">Чтобы получить это значение, найдите приложение PowerApp на сайте [web.powerapps.com](https://web.powerapps.com), затем найдите поле **Код приложения** в разделе **Сведения**.</span><span class="sxs-lookup"><span data-stu-id="e5146-134">To retrieve this value, find the PowerApp on [web.powerapps.com](https://web.powerapps.com) and then locate the **App ID** field under **Details**.</span></span>  
   - <span data-ttu-id="e5146-135">Для **Входные данные для PowerApp** можно при необходимости выбрать поле, которое содержит данные, которые необходимо передать приложению PowerApp в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="e5146-135">For **Input data for the PowerApp**, you can optionally select the field that contains the data that you want to pass to the PowerApp as input.</span></span> <span data-ttu-id="e5146-136">См. пункт ниже в этом разделе под названием [Построение приложения PowerApp, которое использует данные из Finance and Operations](#building-a-powerapp-that-leverages-data-sent-from-finance-and-operations) для получения сведений о том, как приложение PowerApp может получить доступ к данным, отправленным из Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e5146-136">See the section later in this topic titled [Building a PowerApp that leverages data from Finance and Operations](#building-a-powerapp-that-leverages-data-sent-from-finance-and-operations) for details on how the PowerApp can access the data sent from Finance and Operations.</span></span>  
   - <span data-ttu-id="e5146-137">Выберите **Размер приложения**, соответствующий типу внедряемого приложения PowerApp.</span><span class="sxs-lookup"><span data-stu-id="e5146-137">Choose the **Application size** that matches the type of PowerApp that you're embedding.</span></span> <span data-ttu-id="e5146-138">Выберите **Узкий** для приложений PowerApps, созданного для мобильных устройств, и **Широкий** для приложений PowerApps, созданных для планшетов.</span><span class="sxs-lookup"><span data-stu-id="e5146-138">Select **Thin** for PowerApps built for mobile devices, and **Wide** for PowerApps built for tablets.</span></span> <span data-ttu-id="e5146-139">Это гарантирует, что достаточное количество места будет выделено для внедренного приложения PowerApp.</span><span class="sxs-lookup"><span data-stu-id="e5146-139">This ensures a sufficient amount of space is allotted for the embedded PowerApp.</span></span>
   - <span data-ttu-id="e5146-140">Экспресс-вкладка **Юридические лица** предоставляет возможность выбора, для какого юридического лица доступно приложение PowerApp.</span><span class="sxs-lookup"><span data-stu-id="e5146-140">The **Legal entities** FastTab provides the ability to choose which legal entities the PowerApp is available for.</span></span> <span data-ttu-id="e5146-141">По умолчанию приложение PowerApp отображается во всех юридических лицах.</span><span class="sxs-lookup"><span data-stu-id="e5146-141">The default is to show the PowerApp in all legal entities.</span></span>  
4. <span data-ttu-id="e5146-142">После подтверждения, что настройка выполнена верно, нажмите кнопку **Вставить** для внедрения приложения PowerApp на страницу.</span><span class="sxs-lookup"><span data-stu-id="e5146-142">After confirming that the configuration is correct, click **Insert** to embed the PowerApp on the page.</span></span> <span data-ttu-id="e5146-143">Будет предложено обновить браузер, чтобы появилось внедренное приложение PowerApp.</span><span class="sxs-lookup"><span data-stu-id="e5146-143">You will be prompted to refresh the browser in order to see the embedded PowerApp.</span></span> 

## <a name="sharing-an-embedded-powerapp"></a><span data-ttu-id="e5146-144">Совместное использование внедренного приложения PowerApp</span><span class="sxs-lookup"><span data-stu-id="e5146-144">Sharing an embedded PowerApp</span></span>
<span data-ttu-id="e5146-145">После внедрения приложения PowerApp на страницу и проверки правильности его работы с любым контекстом данных, которые передаются со страницы, можно предоставить доступ к этому внедренному приложению PowerApp другим пользователям в системе.</span><span class="sxs-lookup"><span data-stu-id="e5146-145">After you have embedded a PowerApp on a page and confirmed that it is working correctly with any data context passed from the page, you might want to share this embedded PowerApp with other users in the system.</span></span> <span data-ttu-id="e5146-146">Это можно сделать двумя разными способами с помощью функций персонализации продукта:</span><span class="sxs-lookup"><span data-stu-id="e5146-146">This can be accomplished in two different ways using the personalization capabilities of the product:</span></span>

- <span data-ttu-id="e5146-147">Рекомендуется делать это через системного администратора, который может принудительно отправлять персонализации всеми пользователями или части пользователей.</span><span class="sxs-lookup"><span data-stu-id="e5146-147">The recommended scenario is through the system administrator, who can push a personalization to all users or a subset of users.</span></span> 

- <span data-ttu-id="e5146-148">Кроме того, можно экспортировать персонализации страницы, отправить их одному или нескольким пользователям, и каждый из этих пользователей может импортировать эти изменения.</span><span class="sxs-lookup"><span data-stu-id="e5146-148">Alternatively, you can export your page's personalizations, send them to one or more users, and have each of those users import those changes.</span></span> <span data-ttu-id="e5146-149">Параметр Управление на панели инструментов персонализации позволяет экспортировать и импортировать персонализации.</span><span class="sxs-lookup"><span data-stu-id="e5146-149">The Manage option on the personalization toolbar enables you to export and import personalizations.</span></span>

<span data-ttu-id="e5146-150">См. раздел [Персонализация работы пользователя](personalize-user-experience.md), в котором приведены более подробных сведения о возможностях персонализации в продукте и порядке их использования.</span><span class="sxs-lookup"><span data-stu-id="e5146-150">See [Personalize the user experience](personalize-user-experience.md) for more details about the personalization capabilities in the product and how to use them.</span></span>

## <a name="building-a-powerapp-that-leverages-data-sent-from-finance-and-operations"></a><span data-ttu-id="e5146-151">Создание приложения PowerApp, которое использует данные, отправляемые из Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e5146-151">Building a PowerApp that leverages data sent from Finance and Operations</span></span>
<span data-ttu-id="e5146-152">Важная часть построения приложения PowerApp, которое будет внедрено в Finance and Operations, — это использования входных данных из Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e5146-152">An important part of building a PowerApp that will be embedded in Finance and Operations is utilizing the input data from Finance and Operations.</span></span> <span data-ttu-id="e5146-153">Внутри приложения PowerApp доступ к этим данным можно получить с помощью переменной Param("EntityId").</span><span class="sxs-lookup"><span data-stu-id="e5146-153">Inside the PowerApp, that input data can be accessed using the Param("EntityId") variable.</span></span>  

<span data-ttu-id="e5146-154">Например, в функции OnStart приложения PowerApp можно задать входные данные из Finance and Operations для переменной следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e5146-154">For example, in the OnStart function of the PowerApp, you could set the input data from Finance and Operations to a variable like this:</span></span>

<span data-ttu-id="e5146-155">If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));</span><span class="sxs-lookup"><span data-stu-id="e5146-155">If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));</span></span> 

## <a name="viewing-an-embedded-powerapp"></a><span data-ttu-id="e5146-156">Просмотр внедренного приложения PowerApp</span><span class="sxs-lookup"><span data-stu-id="e5146-156">Viewing an embedded PowerApp</span></span>
<span data-ttu-id="e5146-157">Для просмотра внедренного приложения PowerApp на странице в Finance and Operations просто перейдите на страницу с внедренным приложением PowerApp.</span><span class="sxs-lookup"><span data-stu-id="e5146-157">To view an embedded PowerApp on a page in Finance and Operations, simply go to a page with an embedded PowerApp.</span></span> <span data-ttu-id="e5146-158">Помните, что приложения PowerApps можно открывать с помощью кнопки PowerApps на стандартной панели действий или они могут отображаться прямо на странице как новая вкладка, экспресс-вкладка, колонка или новый раздел в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e5146-158">Recall that PowerApps can be accessed through the PowerApps button in the standard Action Pane, or can appear directly on the page as a new tab, FastTab, blade, or as a new section in a workspace.</span></span> <span data-ttu-id="e5146-159">Когда пользователь в первый раз пытается загрузить приложение PowerApp на странице, ему или ей будет предложено выполнить вход в PowerApps, чтобы убедиться, что пользователь имеет соответствующие разрешения для использования приложения PowerApp.</span><span class="sxs-lookup"><span data-stu-id="e5146-159">When a user first attempts to load a PowerApp on a page, he or she will be prompted to sign in to PowerApps to ensure the user has the approrpiate permissions to use the PowerApp.</span></span>   

## <a name="editing-an-embedded-powerapp"></a><span data-ttu-id="e5146-160">Изменение внедренного приложения PowerApp</span><span class="sxs-lookup"><span data-stu-id="e5146-160">Editing an embedded PowerApp</span></span>
<span data-ttu-id="e5146-161">После того как приложение PowerApp внедрено на страницу, может потребоваться внести изменения в конфигурацию этого приложения PowerApp.</span><span class="sxs-lookup"><span data-stu-id="e5146-161">After a PowerApp has been embedded onto a page, you may need to make some changes to the configuration of that PowerApp.</span></span> <span data-ttu-id="e5146-162">Например, может потребоваться изменить метку, связанную с внедренным приложением PowerApp, или была создана новая версии приложения PowerApp и необходимо обновить идентификатор приложения для указания в последней версии приложения PowerApp.</span><span class="sxs-lookup"><span data-stu-id="e5146-162">For example, perhaps you want to modify the label associated with the embedded PowerApp or a new version of a PowerApp has been created and you need to update the App ID to point at the latest PowerApp.</span></span> 

<span data-ttu-id="e5146-163">Выполните следующие действия, чтобы изменить конфигурацию внедренного приложения PowerApp.</span><span class="sxs-lookup"><span data-stu-id="e5146-163">Follow these steps to edit the configuration of an embedded PowerApp:</span></span>
1. <span data-ttu-id="e5146-164">Перейдите в область **Редактировать PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="e5146-164">Go to the **Edit a PowerApp** pane.</span></span> 
   - <span data-ttu-id="e5146-165">Если доступ к внедренному приложению PowerApp осуществляется с помощью кнопки меню PowerApps, щелкните правой кнопкой мыши кнопку меню PowerApps и выберите **Персонализация**.</span><span class="sxs-lookup"><span data-stu-id="e5146-165">If the embedded PowerApp is accessed through the PowerApps menu button, right-click on the PowerApps menu button and select **Personalize**.</span></span> <span data-ttu-id="e5146-166">Выберите приложение PowerApp, которое требуется настроить, в раскрывающемся меню **Выбрать PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="e5146-166">Select the PowerApp that you want to configure from the **Select PowerApp** drop-down menu.</span></span>  
   - <span data-ttu-id="e5146-167">Если внедренное приложение PowerApp отображается непосредственно на странице, выберите **Параметры**, затем выберите **Персонализировать эту форму**.</span><span class="sxs-lookup"><span data-stu-id="e5146-167">If the embedded PowerApp appears directly on the page, select **Options**, and then select **Personalize this form**.</span></span> <span data-ttu-id="e5146-168">С помощью инструмента **Выбрать** щелкните внедренное приложение PowerApp.</span><span class="sxs-lookup"><span data-stu-id="e5146-168">Using the **Select** tool, click the embedded PowerApp.</span></span>  
2. <span data-ttu-id="e5146-169">Внесите необходимые изменения в конфигурацию PowerApps, затем щелкните **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="e5146-169">Make the needed modifications to the PowerApps configuration, and then click **Save**.</span></span>  

## <a name="removing-an-embedded-powerapp"></a><span data-ttu-id="e5146-170">Удаление внедренного приложения PowerApp</span><span class="sxs-lookup"><span data-stu-id="e5146-170">Removing an embedded PowerApp</span></span>
<span data-ttu-id="e5146-171">После того как приложение PowerApp было внедрено на страницу, существует два способа удаления его при необходимости:</span><span class="sxs-lookup"><span data-stu-id="e5146-171">After a PowerApp has been embedded onto a page, there are two ways to remove it if needed:</span></span> 

- <span data-ttu-id="e5146-172">Перейдите в область **Редактировать PowerApp**, используя инструкции из пункта [Изменение внедренного приложения PowerApp](#editing-an-embedded-powerapp) ранее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="e5146-172">Go to the **Edit a PowerApp** pane using the instructions from the [Editing an embedded PowerApp](#editing-an-embedded-powerapp) section earlier in this topic.</span></span> <span data-ttu-id="e5146-173">Убедитесь, что в области отображается информация для внедренного приложения PowerApp, которое вы хотите удалить, затем нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="e5146-173">Confirm that the pane displays information for the embedded PowerApp that you would like to remove, and then click the **Delete** button.</span></span> 

- <span data-ttu-id="e5146-174">Поскольку внедренное приложение PowerApp сохраняется как данные персонализации, очистка персонализации страницы также приведет к удалению всех внедренных приложений PowerApps на этой странице.</span><span class="sxs-lookup"><span data-stu-id="e5146-174">Because an embedded PowerApp is saved as personalization data, clearing your page's personalization will also remove any embedded PowerApps on that page.</span></span> <span data-ttu-id="e5146-175">Обратите внимание, что очистка персонализации страницы является необратимой и не может быть отменена.</span><span class="sxs-lookup"><span data-stu-id="e5146-175">Note that clearing the page's personalization is permanent and cannot be undone.</span></span> <span data-ttu-id="e5146-176">Чтобы удалить вашу персонализацию на странице, выберите **Параметры**, затем щелкните **Персонализировать эту форму**.</span><span class="sxs-lookup"><span data-stu-id="e5146-176">To remove your personalizations on a page, select **Options** and then click **Personalize this form**.</span></span> <span data-ttu-id="e5146-177">В меню **Управление** выберите пункт **Очистить**.</span><span class="sxs-lookup"><span data-stu-id="e5146-177">Under the **Manage** menu, select the **Clear** button.</span></span> <span data-ttu-id="e5146-178">После обновления браузера все предыдущие персонализации для этой страницы будут удалены.</span><span class="sxs-lookup"><span data-stu-id="e5146-178">After refreshing your browser, all the previous personalizations for this page will be removed.</span></span> <span data-ttu-id="e5146-179">Дополнительные сведения об оптимизации страниц с помощью персонализации см. в разделе [Персонализация работы пользователя](personalize-user-experience.md).</span><span class="sxs-lookup"><span data-stu-id="e5146-179">See [Personalization the user experience](personalize-user-experience.md) for more information about how to optimize pages using personalization.</span></span>  

## <a name="appendix"></a><span data-ttu-id="e5146-180">Приложение</span><span class="sxs-lookup"><span data-stu-id="e5146-180">Appendix</span></span> 
### <a name="developer-control-over-where-a-powerapp-can-be-embedded"></a><span data-ttu-id="e5146-181">Контроль разработчика над тем, где возможно внедрение приложения PowerApp</span><span class="sxs-lookup"><span data-stu-id="e5146-181">Developer control over where a PowerApp can be embedded</span></span>
<span data-ttu-id="e5146-182">По умолчанию пользователи могут внедрять приложения PowerApps на любой странице, как в кнопку меню PowerApps, так и непосредственно на страницу в виде вкладки, экспресс-вкладки, колонки или нового раздела в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e5146-182">By default, users can embed PowerApps on any page, either under the PowerApps menu button or directly on the page as a tab, FastTab, blade or as a new section in a workspace.</span></span> <span data-ttu-id="e5146-183">Тем не менее при необходимости разработчики также могут настроить эту возможность, чтобы разрешить только внедрение приложений PowerApps на некоторых страницах путем реализации следующих методов:</span><span class="sxs-lookup"><span data-stu-id="e5146-183">However, if required, developers can also configure this feature to only allow embedding of PowerApps on certain pages by implementing the following methods:</span></span> 

- <span data-ttu-id="e5146-184">**isPowerAppPersonalizationEnabled** — если этот метод возвращает значение false для конкретной страницы, то кнопка меню PowerApps не будет отображаться и пользователи не смогут внедрять приложения PowerApps ни в каком месте на этой странице, в том числе в виде вкладки.</span><span class="sxs-lookup"><span data-stu-id="e5146-184">**isPowerAppPersonalizationEnabled** - If this method returns false for a specific page, then the PowerApps menu button will not be shown, and users will not be able to embed PowerApps anywhere on this page, including as a tab.</span></span> 

- <span data-ttu-id="e5146-185">**isPowerAppTabPersonalizationEnabled** — если этот метод возвращает значение false для конкретной страницы, то пользователи не смогут внедрять приложения PowerApps непосредственно на странице в качестве вкладки, экспресс-вкладки или раздела панорамы.</span><span class="sxs-lookup"><span data-stu-id="e5146-185">**isPowerAppTabPersonalizationEnabled** - If this method returns false for a specific page, then users will not be able to embed PowerApps directly on the page as a tab, FastTab, or panorama section.</span></span> <span data-ttu-id="e5146-186">Пользователи по-прежнему будут иметь возможность внедрять приложения PowerApps через кнопку меню PowerApps, если внедрение разрешено на странице.</span><span class="sxs-lookup"><span data-stu-id="e5146-186">Users will still be able to embed PowerApps through the PowerApps menu button if embedding is allowed on the page.</span></span>  

<span data-ttu-id="e5146-187">Следующий пример показывает новый класс с двумя методами, необходимый для настройки того, где могут быть внедрены приложения PowerApps.</span><span class="sxs-lookup"><span data-stu-id="e5146-187">The following example shows a new class with the two methods needed to configure where PowerApps can be embedded.</span></span>  

```
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{

    public static boolean isPowerAppPresonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPresonalizationEnabled(pageName);
        return true;
    }

    public static boolean isPowerAppTabPresonalizationEnabled(str pageName)   
    {
        var result = next isPowerAppTabPresonalizationEnabled(pageName);
        return true;
    }
    ```

}

