---
title: Подключение эксперимента и изменение вариантов
description: В этом разделе описывается, как связать эксперимент в сторонней службе с Dynamics 365 Commerce и изменить вариации для эксперимента.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: ea1da0a7dc90b7197f3ee532bccc55d2ddbe4ddd
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930278"
---
# <a name="connect-an-experiment-and-edit-variations"></a><span data-ttu-id="869ee-103">Подключение эксперимента и изменение вариантов</span><span class="sxs-lookup"><span data-stu-id="869ee-103">Connect an experiment and edit variations</span></span>

<span data-ttu-id="869ee-104">В этом разделе описывается, как подключить эксперимент в Commerce и внести изменения в вариации, чтобы они были согласованы с вашей гипотезой.</span><span class="sxs-lookup"><span data-stu-id="869ee-104">This topic describes how to connect your experiment in Commerce and make changes to your variations so they align with your hypothesis.</span></span> <span data-ttu-id="869ee-105">На следующей схеме показаны все шаги настройки и запуска эксперимента на веб-сайте электронной коммерции в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="869ee-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="869ee-106">Дополнительные шаги описаны в отдельных разделах.</span><span class="sxs-lookup"><span data-stu-id="869ee-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="869ee-107">[ ![Путь взаимодействия пользователя с экспериментами — подключение и редактирование](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="869ee-107">[ ![Experimentation user journey - Connect & Edit](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span></span>

<span data-ttu-id="869ee-108">После [настройки эксперимента](experimentation-setup.md) в сторонней службе вы будете подключать эксперимент в Dynamics 365 Commerce и редактировать варианты эксперимента.</span><span class="sxs-lookup"><span data-stu-id="869ee-108">After you've [set up your experiment](experimentation-setup.md) in a third-party service, you'll connect the experiment in Dynamics 365 Commerce and edit the experiment variations.</span></span>

## <a name="planning-considerations"></a><span data-ttu-id="869ee-109">Вопросы планирования</span><span class="sxs-lookup"><span data-stu-id="869ee-109">Planning considerations</span></span>

<span data-ttu-id="869ee-110">Перед тем как подключиться к эксперименту в Commerce, необходимо принять некоторые решения, которые повлияют на то, как Commerce управляет вашим содержимым.</span><span class="sxs-lookup"><span data-stu-id="869ee-110">Before you connect your experiment in Commerce, you'll need to make some decisions that impact the way Commerce manages your content.</span></span>

### <a name="determine-the-scope-of-your-experiment"></a><span data-ttu-id="869ee-111">Определение области действия эксперимента</span><span class="sxs-lookup"><span data-stu-id="869ee-111">Determine the scope of your experiment</span></span>
<span data-ttu-id="869ee-112">При подключении эксперимента будет предложено указать область действия эксперимента.</span><span class="sxs-lookup"><span data-stu-id="869ee-112">When you connect an experiment, you are prompted to define the scope of the experiment.</span></span> <span data-ttu-id="869ee-113">Эксперименты определяются как **частичная** область или **вся** область.</span><span class="sxs-lookup"><span data-stu-id="869ee-113">Experiments are defined as **partial** scope or **entire** scope.</span></span>
- <span data-ttu-id="869ee-114">Выберите вариант **частичная**, если вы хотите провести эксперимент по определенной части страницы.</span><span class="sxs-lookup"><span data-stu-id="869ee-114">Choose **partial** if you want to conduct an experiment on a specific portion of a page.</span></span> <span data-ttu-id="869ee-115">При выборе этого параметра необходимо определить, какие модули включены в эксперимент.</span><span class="sxs-lookup"><span data-stu-id="869ee-115">If you select this option, you must identify which modules are included in the experiment.</span></span> <span data-ttu-id="869ee-116">Изменения, вносимые в части страницы или фрагмента по умолчанию, не имеющие отношения к эксперименту, автоматически синхронизируются по вариантам.</span><span class="sxs-lookup"><span data-stu-id="869ee-116">Changes that are made to parts of the default page or fragment that aren't related to the experiment are automatically synchronized across variations.</span></span>
- <span data-ttu-id="869ee-117">Если вы хотите провести эксперимент на всей странице или фрагменте, выберите **все**.</span><span class="sxs-lookup"><span data-stu-id="869ee-117">Choose **entire** if you want to conduct an experiment on an entire page or fragment.</span></span> <span data-ttu-id="869ee-118">Создаются отдельные копии страницы или фрагмента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="869ee-118">Separate copies of the default page or fragment are created.</span></span> <span data-ttu-id="869ee-119">Вам не придется выбирать модули, включенные в эксперимент, так как вся поверхность редактирования доступна для изменения.</span><span class="sxs-lookup"><span data-stu-id="869ee-119">You won't have to select which modules are included in the experiment because the whole editing surface is available to change.</span></span> <span data-ttu-id="869ee-120">При необходимости модули можно добавлять, удалять и изменять их порядок.</span><span class="sxs-lookup"><span data-stu-id="869ee-120">You can add, delete, and re-order modules as needed.</span></span> <span data-ttu-id="869ee-121">Однако если какие-либо изменения вносятся в страницу или фрагмент по умолчанию, с которым связан эксперимент, эти изменения должны быть синхронизированы вручную во всех вариациях.</span><span class="sxs-lookup"><span data-stu-id="869ee-121">However, if any changes are made to the default page or fragment that the experiment is associated with, those changes have to be manually synchronized across all variations.</span></span>

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> <span data-ttu-id="869ee-122">Если вы связываете эксперимент со страницей, использующей макет, вы можете использовать только эксперименты с областью **вся**.</span><span class="sxs-lookup"><span data-stu-id="869ee-122">If you associate your experiment with a page that uses a layout, you can only scope the experiment as **entire**.</span></span>

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a><span data-ttu-id="869ee-123">Определение, нужно ли планировать время публикации эксперимента</span><span class="sxs-lookup"><span data-stu-id="869ee-123">Decide if you want to schedule when your experiment is published</span></span>
<span data-ttu-id="869ee-124">Если вы хотите запланировать, когда ваш эксперимент будет опубликован на вашем работающем сайте, *перед* подключением эксперимента убедитесь, что содержимое, которое необходимо связать с экспериментом, имеется в группе публикации.</span><span class="sxs-lookup"><span data-stu-id="869ee-124">If you want to schedule when your experiment is published to your live site, make sure the content you want to associate with the experiment is available in a publish group *before* you connect the experiment.</span></span> 

<span data-ttu-id="869ee-125">Дополнительные сведения о группах публикации см. в разделе [Работа с группами публикации](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="869ee-125">For more information about publish groups, refer to [Work with publish groups](publish-groups.md).</span></span>


## <a name="connect-your-experiment"></a><span data-ttu-id="869ee-126">Подключение эксперимента</span><span class="sxs-lookup"><span data-stu-id="869ee-126">Connect your experiment</span></span>
<span data-ttu-id="869ee-127">Чтобы подключить эксперимент, запустите мастер **Подключение эксперимента**.</span><span class="sxs-lookup"><span data-stu-id="869ee-127">To connect your experiment, you'll launch the **Connect experiment** wizard.</span></span> <span data-ttu-id="869ee-128">Мастер поможет выполнить шаги, необходимые для подключения эксперимента.</span><span class="sxs-lookup"><span data-stu-id="869ee-128">The wizard walks you through the steps required to connect your experiment.</span></span> <span data-ttu-id="869ee-129">По завершении работы мастера ваш эксперимент будет подключен, а варианты будут созданы и готовы к изменению.</span><span class="sxs-lookup"><span data-stu-id="869ee-129">When you complete the wizard, your experiment is connected and variations are created and ready to be edited.</span></span>

1. <span data-ttu-id="869ee-130">Для запуска мастера выберите вкладку **Эксперименты** в конструкторе сайтов, затем выберите **Подключить**.</span><span class="sxs-lookup"><span data-stu-id="869ee-130">To launch the wizard, select the **Experiments** tab in site builder and then select **Connect**.</span></span> <span data-ttu-id="869ee-131">Кроме того, в мастер можно перейти из редактора страниц или фрагментов.</span><span class="sxs-lookup"><span data-stu-id="869ee-131">Alternatively, the wizard can be accessed from a page or fragment editor.</span></span> <span data-ttu-id="869ee-132">В режиме редактирования выберите на панели команд **Подключить эксперимент**.</span><span class="sxs-lookup"><span data-stu-id="869ee-132">In edit mode, select **Connect experiment** in the command bar.</span></span>

> [!NOTE]
> <span data-ttu-id="869ee-133">Страница может быть подключена только к одному эксперименту в каждый момент времени.</span><span class="sxs-lookup"><span data-stu-id="869ee-133">A page can only be connected to one experiment at a time.</span></span> <span data-ttu-id="869ee-134">Чтобы подключить страницу к другому эксперименту, сначала удалите эксперимент, к которому в данный момент подключена страница.</span><span class="sxs-lookup"><span data-stu-id="869ee-134">To connect a page to a different experiment, first delete the experiment that the page is currently connected to.</span></span>

1. <span data-ttu-id="869ee-135">Выберите страницу или фрагмент, на котором необходимо выполнить эксперимент.</span><span class="sxs-lookup"><span data-stu-id="869ee-135">Choose the page or fragment you want to run your experiment on.</span></span>
1. <span data-ttu-id="869ee-136">Задайте для области эксперимента значение **частичная** или **вся** в зависимости от выбора, сделанного в разделе [Определение области действия эксперимента](#determine-the-scope-of-your-experiment) выше.</span><span class="sxs-lookup"><span data-stu-id="869ee-136">Set the experimentation scope to **partial** or **entire**, based on the choice you made in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>
    > [!NOTE]
    > <span data-ttu-id="869ee-137">Флаг функции **Эксперимент на страницах или фрагментах** должен быть включен, если необходимо экспериментировать с полной страницей или фрагментом.</span><span class="sxs-lookup"><span data-stu-id="869ee-137">The **Experiment on pages or fragments** feature flag must be enabled if you want to experiment on a full page or fragment.</span></span> <span data-ttu-id="869ee-138">Дополнительные сведения см. в теме [Экспериментирование в Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="869ee-138">Refer to the [Experimentation in Dynamics 365 Commerce](experimentation-overview.md) topic for more information.</span></span>
    
1. <span data-ttu-id="869ee-139">На заключительном шаге мастера выберите **Создать варианты и завершить работу мастера**.</span><span class="sxs-lookup"><span data-stu-id="869ee-139">In the final step of the wizard, select **Generate variations and exit wizard**.</span></span> <span data-ttu-id="869ee-140">Для эксперимента созданы варианты.</span><span class="sxs-lookup"><span data-stu-id="869ee-140">Variations are created for the experiment.</span></span> 

## <a name="edit-your-variations"></a><span data-ttu-id="869ee-141">Редактирование вариантов</span><span class="sxs-lookup"><span data-stu-id="869ee-141">Edit your variations</span></span>
<span data-ttu-id="869ee-142">При выходе из мастера для вас создаются варианты.</span><span class="sxs-lookup"><span data-stu-id="869ee-142">When you exit the wizard, variations are created for you.</span></span> 

<span data-ttu-id="869ee-143">Затем отредактируйте варианты, чтобы они соответствовали вариантам, необходимым для проверки гипотезы в ходе эксперимента.</span><span class="sxs-lookup"><span data-stu-id="869ee-143">Next, you'll edit the variations so they reflect the choices that you need to verify in the experiment hypothesis.</span></span> <span data-ttu-id="869ee-144">Выберите одну из следующих процедур, которая соответствует области, выбранной для эксперимента, в разделе [Определение области эксперимента](#determine-the-scope-of-your-experiment) выше.</span><span class="sxs-lookup"><span data-stu-id="869ee-144">Choose one of following procedures that corresponds to the scope you chose for your experiment in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>

### <a name="edit-variations-for-experiments-with-partial-scope"></a><span data-ttu-id="869ee-145">Изменение вариантов для экспериментов с частичной областью действия</span><span class="sxs-lookup"><span data-stu-id="869ee-145">Edit variations for experiments with partial scope</span></span>
<span data-ttu-id="869ee-146">Выполните следующие шаги, если вы определили область действия эксперимента как **частичная** в мастере **Подключение эксперимента**.</span><span class="sxs-lookup"><span data-stu-id="869ee-146">Follow these steps if you defined the scope of your experiment as **partial** in the **Connect experiment** wizard.</span></span>

1. <span data-ttu-id="869ee-147">В представлении редактора с помощью раскрывающегося меню вариантов, расположенного под панелью команд, измените каждый из вариантов на основе исходной гипотезы.</span><span class="sxs-lookup"><span data-stu-id="869ee-147">In editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> <span data-ttu-id="869ee-148">Вам также может потребоваться установить контрольный или базовый вариант, оставив один из вариантов без изменений.</span><span class="sxs-lookup"><span data-stu-id="869ee-148">You may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>
1. <span data-ttu-id="869ee-149">Выберите модуль, на котором будет выполняться эксперимент, выберите многоточие (...), затем выберите **Добавить в эксперимент**.</span><span class="sxs-lookup"><span data-stu-id="869ee-149">Select the module to be experimented on, select the ellipsis (...), and then select **Add to experiment**.</span></span>

### <a name="edit-variations-for-experiments-with-entire-scope"></a><span data-ttu-id="869ee-150">Изменение вариантов для экспериментов с полной областью действия</span><span class="sxs-lookup"><span data-stu-id="869ee-150">Edit variations for experiments with entire scope</span></span>
<span data-ttu-id="869ee-151">Если вы определили область действия эксперимента **вся** в мастере **Подключение эксперимента**, в режиме редактирования используйте раскрывающееся меню вариантов, расположенное под панелью команд, для редактирования каждого варианта на основе исходной гипотезы.</span><span class="sxs-lookup"><span data-stu-id="869ee-151">If you defined the scope of your experiment as **entire** in the **Connect experiment** wizard, while in editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> 

> [!NOTE]
> <span data-ttu-id="869ee-152">В обоих случаях вам также может потребоваться установить контрольный или базовый вариант, оставив один из вариантов без изменений.</span><span class="sxs-lookup"><span data-stu-id="869ee-152">In either case, you may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>

## <a name="previous-step"></a><span data-ttu-id="869ee-153">Предыдущий шаг</span><span class="sxs-lookup"><span data-stu-id="869ee-153">Previous step</span></span>
[<span data-ttu-id="869ee-154">Настройка эксперимента</span><span class="sxs-lookup"><span data-stu-id="869ee-154">Set up an experiment</span></span>](experimentation-setup.md) 


## <a name="next-step"></a><span data-ttu-id="869ee-155">Далее</span><span class="sxs-lookup"><span data-stu-id="869ee-155">Next step</span></span>
[<span data-ttu-id="869ee-156">Предварительный просмотр и публикация эксперимента</span><span class="sxs-lookup"><span data-stu-id="869ee-156">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)
