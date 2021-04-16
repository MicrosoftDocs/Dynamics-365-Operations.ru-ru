---
title: Запуск и контроль эксперимента
description: В этом разделе описывается, как выполнять и отслеживать эксперимент в сторонней службе. В нем также описывается, как вносить изменения в вариации после запуска эксперимента.
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
ms.openlocfilehash: 4afc19ed103f204fec61ab20b88f767ad5f05b38
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792543"
---
# <a name="run-and-monitor-an-experiment"></a><span data-ttu-id="be122-104">Запуск и контроль эксперимента</span><span class="sxs-lookup"><span data-stu-id="be122-104">Run and monitor an experiment</span></span>

<span data-ttu-id="be122-105">В этом разделе описывается, как выполнять и отслеживать свой эксперимент в приложении стороннего производителя и изменять вариации, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="be122-105">This topic describes how to run and monitor your experiment in a third-party app, and change variations if needed.</span></span> <span data-ttu-id="be122-106">Перед выполнением шагов, описанных в этом разделе, необходимо сначала [опубликовать](experimentation-preview-publish.md) ваш эксперимент в модуле Commerce.</span><span class="sxs-lookup"><span data-stu-id="be122-106">Before you complete the steps in this topic, you'll first need to [publish](experimentation-preview-publish.md) your experiment in Commerce.</span></span> 

<span data-ttu-id="be122-107">На следующей схеме показаны все шаги настройки и запуска эксперимента на веб-сайте электронной коммерции в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="be122-107">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="be122-108">Дополнительные шаги описаны в отдельных разделах.</span><span class="sxs-lookup"><span data-stu-id="be122-108">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="be122-109">[ ![Путь взаимодействия пользователя с экспериментами — запуск и контроль](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="be122-109">[ ![Experimentation user journey - Run & Monitor](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span></span>

<span data-ttu-id="be122-110">После публикации вариаций выполняются все этапы, необходимые для выполнения эксперимента в модуле Commerce.</span><span class="sxs-lookup"><span data-stu-id="be122-110">After you publish your variations, all of the steps you need to do in Commerce to run your experiment are complete.</span></span> <span data-ttu-id="be122-111">Следующим шагом является определение вариации, которая будет отображаться для каждого пользователя при запросе страницы.</span><span class="sxs-lookup"><span data-stu-id="be122-111">The next step is determining which variation to show to each user when they request a page.</span></span> <span data-ttu-id="be122-112">Сторонняя служба выполняет эту определение, но сначала необходимо активировать эксперимент внутри службы.</span><span class="sxs-lookup"><span data-stu-id="be122-112">The third-party service makes that determination, but first you have to activate the experiment within the service.</span></span> <span data-ttu-id="be122-113">Так как шаги по активации эксперимента могут различаться в зависимости от службы, необходимо следовать инструкциям, прилагаемым к службе или поставщику услуг.</span><span class="sxs-lookup"><span data-stu-id="be122-113">Since the steps for activating an experiment vary from service to service, you'll need to follow the instructions included with your service or provider.</span></span> <span data-ttu-id="be122-114">Если эксперимент не активирован, пользователи будут видеть только версию страницы по умолчанию (никакие вариации не будут отображаться).</span><span class="sxs-lookup"><span data-stu-id="be122-114">If the experiment is not activated, users will only see the default version of the page (no variations will be displayed).</span></span>

<span data-ttu-id="be122-115">Необходимо обеспечить достаточное время выполнения эксперимента, чтобы собрать данные для получения статистически значимых результатов.</span><span class="sxs-lookup"><span data-stu-id="be122-115">You'll need to keep the experiment running long enough to gather data for statistically valid results.</span></span> <span data-ttu-id="be122-116">Воспользуйтесь сторонней службой для отслеживания данных и аналитики, относящихся к эксперименту, в ходе выполнения эксперимента.</span><span class="sxs-lookup"><span data-stu-id="be122-116">Use the third-party service to monitor the experiment-related data and analytics while the experiment is running.</span></span>

## <a name="adjust-your-variations"></a><span data-ttu-id="be122-117">Корректировка вариантов</span><span class="sxs-lookup"><span data-stu-id="be122-117">Adjust your variations</span></span>
<span data-ttu-id="be122-118">Если по какой-либо причине необходимо изменить ваши вариации, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="be122-118">If for any reason you need to modify your variations, follow the steps below.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="be122-119">При внесении изменений в действующий эксперимент в модуле Commerce или в сторонней службе могут быть значительные воздействия на результаты.</span><span class="sxs-lookup"><span data-stu-id="be122-119">If you make changes to a live experiment in Commerce or the third-party service, your results may be significantly impacted.</span></span> <span data-ttu-id="be122-120">Попробуйте позволить эксперименту выполнить свою программу, а затем создать новый эксперимент для внесения серьезных изменений.</span><span class="sxs-lookup"><span data-stu-id="be122-120">Consider letting the experiment run its course and then creating a new experiment for major changes.</span></span>

1. <span data-ttu-id="be122-121">В конструкторе сайта Commerce выберите **Эксперименты** в левой области переходов, затем выберите эксперимент.</span><span class="sxs-lookup"><span data-stu-id="be122-121">In Commerce site builder, select **Experiments** in the left navigation pane, and then select the experiment.</span></span> 
1. <span data-ttu-id="be122-122">В раскрывающемся меню выберите вариант, который необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="be122-122">Select the variation you want to update from the drop-down menu.</span></span>
1. <span data-ttu-id="be122-123">Внесите все необходимые изменения, а затем просмотрите и опубликуйте варианты.</span><span class="sxs-lookup"><span data-stu-id="be122-123">Make any needed changes, and then preview and publish the variations.</span></span> <span data-ttu-id="be122-124">Дополнительные сведения см. в разделе [Предварительный просмотр и публикация эксперимента](experimentation-preview-publish.md).</span><span class="sxs-lookup"><span data-stu-id="be122-124">For more information, see [Preview and publish an experiment](experimentation-preview-publish.md).</span></span>
1. <span data-ttu-id="be122-125">Перейдите к сторонней службе, чтобы внести любые изменения, связанные с настройкой эксперимента.</span><span class="sxs-lookup"><span data-stu-id="be122-125">Go to the third-party service to make any experiment setup-related changes.</span></span>
    
## <a name="previous-step"></a><span data-ttu-id="be122-126">Предыдущий шаг</span><span class="sxs-lookup"><span data-stu-id="be122-126">Previous step</span></span>
[<span data-ttu-id="be122-127">Предварительный просмотр и публикация эксперимента</span><span class="sxs-lookup"><span data-stu-id="be122-127">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)

## <a name="next-step"></a><span data-ttu-id="be122-128">Далее</span><span class="sxs-lookup"><span data-stu-id="be122-128">Next step</span></span>
[<span data-ttu-id="be122-129">Повышение вариации и завершение эксперимента</span><span class="sxs-lookup"><span data-stu-id="be122-129">Promote a variation and complete an experiment</span></span>](experimentation-review-complete.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]