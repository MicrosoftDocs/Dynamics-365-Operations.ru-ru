---
title: Предварительный просмотр и публикация эксперимента
description: В этом разделе описывается, как выполнить предварительный просмотр и публикацию эксперимента из Dynamics 365 Commerce.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 52ca23e5aaeb7058853fed2241d5804180fa7f8d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798971"
---
# <a name="preview-and-publish-an-experiment"></a><span data-ttu-id="447e9-103">Предварительный просмотр и публикация эксперимента</span><span class="sxs-lookup"><span data-stu-id="447e9-103">Preview and publish an experiment</span></span>

<span data-ttu-id="447e9-104">В этой теме описывается предварительный просмотр и публикация эксперимента в Dynamics 365 Commerce после [подключения эксперимента и изменения ваших вариаций](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="447e9-104">This topic describes how to preview and publish your experiment in Dynamics 365 Commerce after you've [connected your experiment and edited your variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="447e9-105">На следующей схеме показаны все шаги настройки и запуска эксперимента на веб-сайте электронной коммерции в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="447e9-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="447e9-106">Дополнительные шаги описаны в отдельных разделах.</span><span class="sxs-lookup"><span data-stu-id="447e9-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="447e9-107">[ ![Путь взаимодействия пользователя с экспериментами — предварительный просмотр и публикация](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="447e9-107">[ ![Experimentation user journey - Preview & Publish](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span></span>

## <a name="preview-your-experiment-variations"></a><span data-ttu-id="447e9-108">Предварительный просмотр вариантов экспериментов</span><span class="sxs-lookup"><span data-stu-id="447e9-108">Preview your experiment variations</span></span>
<span data-ttu-id="447e9-109">Можно просмотреть вариации и продолжить их редактирование до тех пор, пока они не будут выглядеть так, как необходимо.</span><span class="sxs-lookup"><span data-stu-id="447e9-109">You can preview your variations and continue editing them until they look the way you want them to.</span></span>

<span data-ttu-id="447e9-110">Чтобы просмотреть вариации эксперимента в конфигураторе сайта Commerce, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="447e9-110">To preview your experiment variations in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="447e9-111">Из раскрывающегося меню вариаций, расположенного под панелью команд, выберите содержимое, которое требуется предварительно просмотреть.</span><span class="sxs-lookup"><span data-stu-id="447e9-111">From the variations drop-down menu below the command bar, select the content you want to preview.</span></span> 
1. <span data-ttu-id="447e9-112">На панели команд выберите **Предварительный просмотр**.</span><span class="sxs-lookup"><span data-stu-id="447e9-112">On the command bar, select **Preview**.</span></span> <span data-ttu-id="447e9-113">Отображается предварительный просмотр того, как будет выглядеть содержимое после его публикации.</span><span class="sxs-lookup"><span data-stu-id="447e9-113">A preview of what the content will look like when it's published is displayed.</span></span>
1. <span data-ttu-id="447e9-114">Для предварительного просмотра других вариаций выберите ее в раскрывающемся меню списке вариаций и снова выберите **Предварительный просмотр**.</span><span class="sxs-lookup"><span data-stu-id="447e9-114">To preview a different variation, select it from the variation drop-down menu and select **Preview** again.</span></span>

## <a name="publish-your-experiment"></a><span data-ttu-id="447e9-115">Публикация эксперимента</span><span class="sxs-lookup"><span data-stu-id="447e9-115">Publish your experiment</span></span>
<span data-ttu-id="447e9-116">Если вы не используете группу публикации для планирования, когда ваш эксперимент будет введен в действие, и необходимо опубликовать немедленно, выберите **Опубликовать** на панели команд.</span><span class="sxs-lookup"><span data-stu-id="447e9-116">If you aren't using a publish group to schedule when your experiment goes live and you want to publish immediately, select **Publish** in the command bar.</span></span> <span data-ttu-id="447e9-117">Будут опубликованы все вариации, относящиеся к эксперименту.</span><span class="sxs-lookup"><span data-stu-id="447e9-117">All variations that belong to the experiment will be published.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="447e9-118">Если страница имеет неопубликованный URL-адрес, необходимо сначала опубликовать URL-адрес, иначе он не будет виден пользователям веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="447e9-118">If the page has an unpublished URL, you must first publish the URL or it won't be visible to your website users.</span></span> <span data-ttu-id="447e9-119">Подробные сведения см. в разделе [Сохранение, предварительный просмотр и публикация страницы](save-preview-publish-page.md).</span><span class="sxs-lookup"><span data-stu-id="447e9-119">For details, see [Save, preview, and publish a page](save-preview-publish-page.md).</span></span>
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a><span data-ttu-id="447e9-120">Использование группы публикации для планирования, когда ваш эксперимент будет введен в действие</span><span class="sxs-lookup"><span data-stu-id="447e9-120">Use publish groups to schedule when your experiment goes live</span></span>
<span data-ttu-id="447e9-121">Варианты, созданные в конфигураторе сайта, могут быть запланированы для публикации с помощью группы публикации.</span><span class="sxs-lookup"><span data-stu-id="447e9-121">Variations created in site builder can be scheduled for publishing by using a publish group.</span></span> <span data-ttu-id="447e9-122">В группе публикаций можно связать страницу или фрагмент с экспериментом, выбрав **Эксперименты** в левой области переходов.</span><span class="sxs-lookup"><span data-stu-id="447e9-122">Within a publish group, you can connect a page or fragment to your experiment by selecting **Experiments** in the left navigation pane.</span></span> <span data-ttu-id="447e9-123">Это можно также сделать, выбрав **Страницы** или **Фрагменты** и следуя инструкциям в разделе [Подключение эксперимента и изменение вариантов](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="447e9-123">You can also do this by selecting **Pages** or **Fragments** and following the instructions in [Connect an experiment and edit variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="447e9-124">Сведения о группах публикации см. в разделе [Работа с группами публикации](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="447e9-124">For information about publish groups, see [Work with publish groups](publish-groups.md).</span></span>

<span data-ttu-id="447e9-125">При использовании групп публикации с экспериментами необходимо знать о некоторых важных вопросах.</span><span class="sxs-lookup"><span data-stu-id="447e9-125">When using publish groups with experiments, there are some important considerations to be aware of.</span></span>
- <span data-ttu-id="447e9-126">При добавлении страницы или фрагмента, для которых выполняется эксперимент, к группе публикации эксперимент будет удален со страницы или фрагмента в группе публикации.</span><span class="sxs-lookup"><span data-stu-id="447e9-126">When you add a page or fragment that has an experiment running on it to a publish group, the experiment will be removed from the page or fragment in the publish group.</span></span>
- <span data-ttu-id="447e9-127">Эксперименты, связанные со страницами на реальном сайте, недоступны для страниц в группах публикации и наоборот.</span><span class="sxs-lookup"><span data-stu-id="447e9-127">Experiments that are connected to pages in a live site aren't available to pages within publish groups and vice-versa.</span></span> <span data-ttu-id="447e9-128">Аналогично, страницы, на которых выполняются эксперименты на действующем сайте, недоступны для других экспериментов в группах публикации и наоборот.</span><span class="sxs-lookup"><span data-stu-id="447e9-128">Similarly, pages that have experiments running on them in a live site aren't available to other experiments in publish groups and vice versa.</span></span>
- <span data-ttu-id="447e9-129">При публикации или планировании группы публикации публикуется все содержимое группы публикации, независимо от того, связан ли эксперимент с группой публикации.</span><span class="sxs-lookup"><span data-stu-id="447e9-129">When you publish or schedule a publish group, all content in the publish group is published, regardless of whether there's an experiment associated with the publish group.</span></span>
- <span data-ttu-id="447e9-130">Так как группа публикации продолжает сохраняться после ее публикации на действующем веб-сайте, эксперименты в группе публикации также будут сохраняться.</span><span class="sxs-lookup"><span data-stu-id="447e9-130">Because a publish group continues to persist after it's been published to a live site, experiments in the publish group will also persist.</span></span> <span data-ttu-id="447e9-131">Таким образом, вы не сможете связать другие эксперименты с той же страницей или фрагментом.</span><span class="sxs-lookup"><span data-stu-id="447e9-131">Therefore, you won't be able to associate other experiments with the same page or fragment.</span></span> <span data-ttu-id="447e9-132">Чтобы избежать этого ограничения, удалите все группы публикации с сохраненными экспериментами.</span><span class="sxs-lookup"><span data-stu-id="447e9-132">To avoid this limitation, delete any publish groups with persisting experiments.</span></span> <span data-ttu-id="447e9-133">Аналогичным образом, если необходимо удалить эксперимент на действующем сайте, который также существует в группе публикации, удалите его из группы публикации в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="447e9-133">Similarly, if you want to delete an experiment in a live site that also exists in a publish group, delete it from the publish group first.</span></span>

## <a name="previous-step"></a><span data-ttu-id="447e9-134">Предыдущий шаг</span><span class="sxs-lookup"><span data-stu-id="447e9-134">Previous step</span></span>
[<span data-ttu-id="447e9-135">Подключение и редактирование эксперимента</span><span class="sxs-lookup"><span data-stu-id="447e9-135">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)

## <a name="next-step"></a><span data-ttu-id="447e9-136">Далее</span><span class="sxs-lookup"><span data-stu-id="447e9-136">Next step</span></span>
[<span data-ttu-id="447e9-137">Запуск и контроль эксперимента</span><span class="sxs-lookup"><span data-stu-id="447e9-137">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]