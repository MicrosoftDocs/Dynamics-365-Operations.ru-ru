---
title: Предварительный просмотр и публикация эксперимента
description: В этом разделе описывается, как выполнить предварительный просмотр и публикацию эксперимента из Dynamics 365 Commerce.
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
ms.openlocfilehash: 91e2e4840a2d53f195d881279050b6415d48b070
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930277"
---
# <a name="preview-and-publish-an-experiment"></a><span data-ttu-id="9cb5a-103">Предварительный просмотр и публикация эксперимента</span><span class="sxs-lookup"><span data-stu-id="9cb5a-103">Preview and publish an experiment</span></span>

<span data-ttu-id="9cb5a-104">В этой теме описывается предварительный просмотр и публикация эксперимента в Dynamics 365 Commerce после [подключения эксперимента и изменения ваших вариаций](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="9cb5a-104">This topic describes how to preview and publish your experiment in Dynamics 365 Commerce after you've [connected your experiment and edited your variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="9cb5a-105">На следующей схеме показаны все шаги настройки и запуска эксперимента на веб-сайте электронной коммерции в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9cb5a-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="9cb5a-106">Дополнительные шаги описаны в отдельных разделах.</span><span class="sxs-lookup"><span data-stu-id="9cb5a-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="9cb5a-107">[ ![Путь взаимодействия пользователя с экспериментами — предварительный просмотр и публикация](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="9cb5a-107">[ ![Experimentation user journey - Preview & Publish](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span></span>

## <a name="preview-your-experiment-variations"></a><span data-ttu-id="9cb5a-108">Предварительный просмотр вариантов экспериментов</span><span class="sxs-lookup"><span data-stu-id="9cb5a-108">Preview your experiment variations</span></span>
<span data-ttu-id="9cb5a-109">Можно просмотреть вариации и продолжить их редактирование до тех пор, пока они не будут выглядеть так, как необходимо.</span><span class="sxs-lookup"><span data-stu-id="9cb5a-109">You can preview your variations and continue editing them until they look the way you want them to.</span></span>

1. <span data-ttu-id="9cb5a-110">В конфигураторе сайтов используйте раскрывающееся меню вариаций, расположенное под панелью команд, для выбора содержимого, которое требуется предварительно просмотреть.</span><span class="sxs-lookup"><span data-stu-id="9cb5a-110">In site builder, use the variations drop-down menu below the command bar to select the content you want to preview.</span></span> 
1. <span data-ttu-id="9cb5a-111">В верхней панели выберите **Предварительный просмотр**.</span><span class="sxs-lookup"><span data-stu-id="9cb5a-111">Select **Preview** in the top bar.</span></span> <span data-ttu-id="9cb5a-112">Отображается предварительный просмотр того, как будет выглядеть содержимое после его публикации.</span><span class="sxs-lookup"><span data-stu-id="9cb5a-112">A preview of what the content will look like when it's published is displayed.</span></span>
1. <span data-ttu-id="9cb5a-113">Для предварительного просмотра других вариаций выберите ее в раскрывающемся списке вариаций и снова выберите **Предварительный просмотр**.</span><span class="sxs-lookup"><span data-stu-id="9cb5a-113">To preview a different variation, select it from the variation drop-down and select **Preview** again.</span></span>

## <a name="publish-your-experiment"></a><span data-ttu-id="9cb5a-114">Публикация эксперимента</span><span class="sxs-lookup"><span data-stu-id="9cb5a-114">Publish your experiment</span></span>
<span data-ttu-id="9cb5a-115">Если вы не используете группу публикации для планирования, когда ваш эксперимент будет введен в действие, и необходимо опубликовать немедленно, выберите **Опубликовать** на панели команд.</span><span class="sxs-lookup"><span data-stu-id="9cb5a-115">If you aren't using a publish group to schedule when your experiment goes live and you want to publish immediately, select **Publish** in the command bar.</span></span> <span data-ttu-id="9cb5a-116">Будут опубликованы все вариации, относящиеся к эксперименту.</span><span class="sxs-lookup"><span data-stu-id="9cb5a-116">All variations that belong to the experiment will be published.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="9cb5a-117">Если страница имеет неопубликованный URL-адрес, необходимо сначала опубликовать URL-адрес, иначе он не будет виден пользователям веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="9cb5a-117">If the page has an unpublished URL, you must first publish the URL or it won't be visible to your website users.</span></span> <span data-ttu-id="9cb5a-118">Подробные сведения см. в разделе [Сохранение, предварительный просмотр и публикация страницы](save-preview-publish-page.md).</span><span class="sxs-lookup"><span data-stu-id="9cb5a-118">For details, see [Save, preview, and publish a page](save-preview-publish-page.md).</span></span>
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a><span data-ttu-id="9cb5a-119">Использование группы публикации для планирования, когда ваш эксперимент будет введен в действие</span><span class="sxs-lookup"><span data-stu-id="9cb5a-119">Use publish groups to schedule when your experiment goes live</span></span>
<span data-ttu-id="9cb5a-120">Варианты, созданные в конфигураторе сайта, могут быть запланированы для публикации с помощью группы публикации.</span><span class="sxs-lookup"><span data-stu-id="9cb5a-120">Variations created in site builder can be scheduled for publishing by using a publish group.</span></span> <span data-ttu-id="9cb5a-121">В группе публикации можно подключить страницу или фрагмент к эксперименту, перейдя на вкладку **Эксперименты**, **Страницы** или **Фрагменты**. Дополнительные сведения см. в разделе [Подключение эксперимента и изменение вариантов](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="9cb5a-121">Within a publish group, you can connect a page or fragment to your experiment by going to the **Experiments** tab or the **Pages** or **Fragments** tab. For more information, see [Connect an experiment and edit variations](experimentation-connect-edit.md) topic.</span></span> <span data-ttu-id="9cb5a-122">Сведения о группах публикации см. в разделе [Работа с группами публикации](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="9cb5a-122">For information about publish groups, see [Work with publish groups](publish-groups.md).</span></span>

<span data-ttu-id="9cb5a-123">При использовании групп публикации с экспериментами необходимо знать о некоторых важных вопросах.</span><span class="sxs-lookup"><span data-stu-id="9cb5a-123">When using publish groups with experiments, there are some important considerations to be aware of.</span></span>
- <span data-ttu-id="9cb5a-124">При добавлении страницы или фрагмента, для которых выполняется эксперимент, к группе публикации эксперимент будет удален со страницы или фрагмента в группе публикации.</span><span class="sxs-lookup"><span data-stu-id="9cb5a-124">When you add a page or fragment that has an experiment running on it to a publish group, the experiment will be removed from the page or fragment in the publish group.</span></span>
- <span data-ttu-id="9cb5a-125">Эксперименты, связанные со страницами на реальном сайте, недоступны для страниц в группах публикации и наоборот.</span><span class="sxs-lookup"><span data-stu-id="9cb5a-125">Experiments that are connected to pages in a live site aren't available to pages within publish groups and vice-versa.</span></span> <span data-ttu-id="9cb5a-126">Аналогично, страницы, на которых выполняются эксперименты на действующем сайте, недоступны для других экспериментов в группах публикации и наоборот.</span><span class="sxs-lookup"><span data-stu-id="9cb5a-126">Similarly, pages that have experiments running on them in a live site aren't available to other experiments in publish groups and vice versa.</span></span>
- <span data-ttu-id="9cb5a-127">При публикации или планировании группы публикации публикуется все содержимое группы публикации, независимо от того, связан ли эксперимент с группой публикации.</span><span class="sxs-lookup"><span data-stu-id="9cb5a-127">When you publish or schedule a publish group, all content in the publish group is published, regardless of whether there's an experiment associated with the publish group.</span></span>
- <span data-ttu-id="9cb5a-128">Так как группа публикации продолжает сохраняться после ее публикации на действующем веб-сайте, эксперименты в группе публикации также будут сохраняться.</span><span class="sxs-lookup"><span data-stu-id="9cb5a-128">Because a publish group continues to persist after it's been published to a live site, experiments in the publish group will also persist.</span></span> <span data-ttu-id="9cb5a-129">Таким образом, вы не сможете связать другие эксперименты с той же страницей или фрагментом.</span><span class="sxs-lookup"><span data-stu-id="9cb5a-129">Therefore, you won't be able to associate other experiments with the same page or fragment.</span></span> <span data-ttu-id="9cb5a-130">Чтобы избежать этого ограничения, удалите все группы публикации с сохраненными экспериментами.</span><span class="sxs-lookup"><span data-stu-id="9cb5a-130">To avoid this limitation, delete any publish groups with persisting experiments.</span></span> <span data-ttu-id="9cb5a-131">Аналогичным образом, если необходимо удалить эксперимент на действующем сайте, который также существует в группе публикации, удалите его из группы публикации в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="9cb5a-131">Similarly, if you want to delete an experiment in a live site that also exists in a publish group, delete it from the publish group first.</span></span>

## <a name="previous-step"></a><span data-ttu-id="9cb5a-132">Предыдущий шаг</span><span class="sxs-lookup"><span data-stu-id="9cb5a-132">Previous step</span></span>
[<span data-ttu-id="9cb5a-133">Подключение и редактирование эксперимента</span><span class="sxs-lookup"><span data-stu-id="9cb5a-133">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)

## <a name="next-step"></a><span data-ttu-id="9cb5a-134">Далее</span><span class="sxs-lookup"><span data-stu-id="9cb5a-134">Next step</span></span>
[<span data-ttu-id="9cb5a-135">Запуск и контроль эксперимента</span><span class="sxs-lookup"><span data-stu-id="9cb5a-135">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
