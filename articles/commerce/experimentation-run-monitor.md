---
title: Запуск и контроль эксперимента
description: В этом разделе описывается, как выполнять и отслеживать эксперимент в сторонней службе. В нем также описывается, как вносить изменения в вариации после запуска эксперимента.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: ba6fb94033e227790e01676819308bb4f0cd6868
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965230"
---
# <a name="run-and-monitor-an-experiment"></a><span data-ttu-id="3199c-104">Запуск и контроль эксперимента</span><span class="sxs-lookup"><span data-stu-id="3199c-104">Run and monitor an experiment</span></span>

<span data-ttu-id="3199c-105">В этом разделе описывается, как выполнять и отслеживать свой эксперимент в приложении стороннего производителя и изменять вариации, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="3199c-105">This topic describes how to run and monitor your experiment in a third-party app, and change variations if needed.</span></span> <span data-ttu-id="3199c-106">Перед выполнением шагов, описанных в этом разделе, необходимо сначала [опубликовать](experimentation-preview-publish.md) ваш эксперимент в модуле Commerce.</span><span class="sxs-lookup"><span data-stu-id="3199c-106">Before you complete the steps in this topic, you'll first need to [publish](experimentation-preview-publish.md) your experiment in Commerce.</span></span> 

<span data-ttu-id="3199c-107">На следующей схеме показаны все шаги настройки и запуска эксперимента на веб-сайте электронной коммерции в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3199c-107">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="3199c-108">Дополнительные шаги описаны в отдельных разделах.</span><span class="sxs-lookup"><span data-stu-id="3199c-108">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="3199c-109">[ ![Путь взаимодействия пользователя с экспериментами — запуск и контроль](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="3199c-109">[ ![Experimentation user journey - Run & Monitor](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span></span>

<span data-ttu-id="3199c-110">После публикации вариаций выполняются все этапы, необходимые для выполнения эксперимента в модуле Commerce.</span><span class="sxs-lookup"><span data-stu-id="3199c-110">After you publish your variations, all of the steps you need to do in Commerce to run your experiment are complete.</span></span> <span data-ttu-id="3199c-111">Следующим шагом является определение вариации, которая будет отображаться для каждого пользователя при запросе страницы.</span><span class="sxs-lookup"><span data-stu-id="3199c-111">The next step is determining which variation to show to each user when they request a page.</span></span> <span data-ttu-id="3199c-112">Сторонняя служба выполняет эту определение, но сначала необходимо активировать эксперимент внутри службы.</span><span class="sxs-lookup"><span data-stu-id="3199c-112">The third-party service makes that determination, but first you have to activate the experiment within the service.</span></span> <span data-ttu-id="3199c-113">Так как шаги по активации эксперимента могут различаться в зависимости от службы, необходимо следовать инструкциям, прилагаемым к службе или поставщику услуг.</span><span class="sxs-lookup"><span data-stu-id="3199c-113">Since the steps for activating an experiment vary from service to service, you'll need to follow the instructions included with your service or provider.</span></span> <span data-ttu-id="3199c-114">Если эксперимент не активирован, пользователи будут видеть только версию страницы по умолчанию (никакие вариации не будут отображаться).</span><span class="sxs-lookup"><span data-stu-id="3199c-114">If the experiment is not activated, users will only see the default version of the page (no variations will be displayed).</span></span>

<span data-ttu-id="3199c-115">Необходимо обеспечить достаточное время выполнения эксперимента, чтобы собрать данные для получения статистически значимых результатов.</span><span class="sxs-lookup"><span data-stu-id="3199c-115">You'll need to keep the experiment running long enough to gather data for statistically valid results.</span></span> <span data-ttu-id="3199c-116">Воспользуйтесь сторонней службой для отслеживания данных и аналитики, относящихся к эксперименту, в ходе выполнения эксперимента.</span><span class="sxs-lookup"><span data-stu-id="3199c-116">Use the third-party service to monitor the experiment-related data and analytics while the experiment is running.</span></span>

## <a name="adjust-your-variations"></a><span data-ttu-id="3199c-117">Корректировка вариантов</span><span class="sxs-lookup"><span data-stu-id="3199c-117">Adjust your variations</span></span>
<span data-ttu-id="3199c-118">Если по какой-либо причине необходимо изменить ваши вариации, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3199c-118">If for any reason you need to modify your variations, follow the steps below.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3199c-119">При внесении изменений в действующий эксперимент в модуле Commerce или в сторонней службе могут быть значительные воздействия на результаты.</span><span class="sxs-lookup"><span data-stu-id="3199c-119">If you make changes to a live experiment in Commerce or the third-party service, your results may be significantly impacted.</span></span> <span data-ttu-id="3199c-120">Попробуйте позволить эксперименту выполнить свою программу, а затем создать новый эксперимент для внесения серьезных изменений.</span><span class="sxs-lookup"><span data-stu-id="3199c-120">Consider letting the experiment run its course and then creating a new experiment for major changes.</span></span>

1. <span data-ttu-id="3199c-121">В конструкторе сайта Commerce выберите **Эксперименты** в левой области переходов, затем выберите эксперимент.</span><span class="sxs-lookup"><span data-stu-id="3199c-121">In Commerce site builder, select **Experiments** in the left navigation pane, and then select the experiment.</span></span> 
1. <span data-ttu-id="3199c-122">В раскрывающемся меню выберите вариант, который необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="3199c-122">Select the variation you want to update from the drop-down menu.</span></span>
1. <span data-ttu-id="3199c-123">Внесите все необходимые изменения, а затем просмотрите и опубликуйте варианты.</span><span class="sxs-lookup"><span data-stu-id="3199c-123">Make any needed changes, and then preview and publish the variations.</span></span> <span data-ttu-id="3199c-124">Дополнительные сведения см. в разделе [Предварительный просмотр и публикация эксперимента](experimentation-preview-publish.md).</span><span class="sxs-lookup"><span data-stu-id="3199c-124">For more information, see [Preview and publish an experiment](experimentation-preview-publish.md).</span></span>
1. <span data-ttu-id="3199c-125">Перейдите к сторонней службе, чтобы внести любые изменения, связанные с настройкой эксперимента.</span><span class="sxs-lookup"><span data-stu-id="3199c-125">Go to the third-party service to make any experiment setup-related changes.</span></span>
    
## <a name="previous-step"></a><span data-ttu-id="3199c-126">Предыдущий шаг</span><span class="sxs-lookup"><span data-stu-id="3199c-126">Previous step</span></span>
[<span data-ttu-id="3199c-127">Предварительный просмотр и публикация эксперимента</span><span class="sxs-lookup"><span data-stu-id="3199c-127">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)

## <a name="next-step"></a><span data-ttu-id="3199c-128">Далее</span><span class="sxs-lookup"><span data-stu-id="3199c-128">Next step</span></span>
[<span data-ttu-id="3199c-129">Повышение вариации и завершение эксперимента</span><span class="sxs-lookup"><span data-stu-id="3199c-129">Promote a variation and complete an experiment</span></span>](experimentation-review-complete.md)
