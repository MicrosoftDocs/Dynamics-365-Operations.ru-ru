---
title: Повышение вариации и завершение эксперимента
description: В этом разделе описывается, как повысить успешную вариацию и завершить эксперимент в Dynamics 365 Commerce.
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
ms.openlocfilehash: 25cccbeae5c263a3032eeebf2fc5335e22c1415a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009939"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="bb6e6-103">Повышение вариации и завершение эксперимента</span><span class="sxs-lookup"><span data-stu-id="bb6e6-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="bb6e6-104">В этом разделе описывается, как повысить вариацию, которая дает наилучший результат в эксперименте, и как завершить эксперимент.</span><span class="sxs-lookup"><span data-stu-id="bb6e6-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="bb6e6-105">На следующей схеме показаны все шаги настройки и запуска эксперимента на веб-сайте электронной коммерции в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bb6e6-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="bb6e6-106">Дополнительные шаги описаны в отдельных разделах.</span><span class="sxs-lookup"><span data-stu-id="bb6e6-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="bb6e6-107">[ ![Путь взаимодействия пользователя с экспериментами — проверка и завершение](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="bb6e6-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="bb6e6-108">После [выполнения эксперимента](experimentation-run-monitor.md) и сбора необходимых данных для определения вариации, которую вы хотите использовать на своем веб-сайте, вы сможете повысить вариацию и завершить эксперимент.</span><span class="sxs-lookup"><span data-stu-id="bb6e6-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="bb6e6-109">Повышение вариации</span><span class="sxs-lookup"><span data-stu-id="bb6e6-109">Promote a variation</span></span>
<span data-ttu-id="bb6e6-110">Воспользуйтесь данными и аналитикой, относящимися к эксперименту в сторонней службе, чтобы определить, какая из вариантов дает наилучший результат.</span><span class="sxs-lookup"><span data-stu-id="bb6e6-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="bb6e6-111">Затем можно повысить его, заменив текущее содержимое действующего сайта на измененный вариант, чтобы он был доступен всем пользователям веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="bb6e6-111">You can then promote it by replacing the current content on the live site with the winning variation so that it's available to all users of your website.</span></span>

<span data-ttu-id="bb6e6-112">Чтобы повысить уровень выигравшего варианта, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="bb6e6-112">To promote the winning variation, follow these steps.</span></span> 

1. <span data-ttu-id="bb6e6-113">В конструкторе сайта Commerce выберите **Эксперименты** в левой области переходов, затем выберите эксперимент.</span><span class="sxs-lookup"><span data-stu-id="bb6e6-113">In Commerce site builder, select **Experiments** in the left navigation pane, and then select the experiment.</span></span>
1. <span data-ttu-id="bb6e6-114">На панели команд выберите **Завершить эксперимент**.</span><span class="sxs-lookup"><span data-stu-id="bb6e6-114">On the command bar, select **Complete experiment**.</span></span>
1. <span data-ttu-id="bb6e6-115">В диалоговом окне **Завершение эксперимента** выберите **Просмотреть данные эксперимента**.</span><span class="sxs-lookup"><span data-stu-id="bb6e6-115">In the **Complete the experiment** dialog box, select **Review the experiment data**.</span></span> <span data-ttu-id="bb6e6-116">Открывается сторонняя служба, в которой можно проверить метрики и определить, какой вариант работает наилучшим образом.</span><span class="sxs-lookup"><span data-stu-id="bb6e6-116">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="bb6e6-117">В диалоговом окне **Завершение эксперимента** в конфигураторе сайтов выберите лучший вариант, затем выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="bb6e6-117">In the **Complete the experiment** dialog box, select the winning variation, and then select **Next**.</span></span>
1. <span data-ttu-id="bb6e6-118">Откройте стороннюю службу и остановите эксперимент.</span><span class="sxs-lookup"><span data-stu-id="bb6e6-118">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="bb6e6-119">В конфигураторе сайтов выберите **Завершить**, чтобы переписать исходную действующую страницу и опубликовать победивший вариант, чтобы он был доступен всем пользователям веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="bb6e6-119">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="bb6e6-120">Если вы решили сохранить текущую действующую страницу и не опубликовать вариант, выберите **Повторно опубликовать исходную страницу**.</span><span class="sxs-lookup"><span data-stu-id="bb6e6-120">If you choose to keep the current live page and not publish a variation, select **Republish the original page**.</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="bb6e6-121">Удаление эксперимента</span><span class="sxs-lookup"><span data-stu-id="bb6e6-121">Delete your experiment</span></span>
<span data-ttu-id="bb6e6-122">Хотя не требуется удалять завершенный эксперимент в Commerce, можно удалить его, чтобы сэкономить место или очистить рабочую область.</span><span class="sxs-lookup"><span data-stu-id="bb6e6-122">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> 

<span data-ttu-id="bb6e6-123">Чтобы удалить эксперимент в конфигураторе сайта Commerce, выполните следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="bb6e6-123">To delete an experiment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="bb6e6-124">Выберите **Эксперименты** в левой области переходов, затем выберите эксперимент.</span><span class="sxs-lookup"><span data-stu-id="bb6e6-124">Select **Experiments** in the left navigation pane, and then select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="bb6e6-125">Если эксперимент все еще активен, перед продолжением остановите выполнение эксперимента в сторонней службе.</span><span class="sxs-lookup"><span data-stu-id="bb6e6-125">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="bb6e6-126">На панели команд выберите **Отменить публикацию**, чтобы удалить содержимое варианта с действующего сайта.</span><span class="sxs-lookup"><span data-stu-id="bb6e6-126">On the command bar, select **Unpublish**  to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="bb6e6-127">Выберите **Удалить**, чтобы удалить эксперимент.</span><span class="sxs-lookup"><span data-stu-id="bb6e6-127">Select **Delete** to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="bb6e6-128">Предыдущий шаг</span><span class="sxs-lookup"><span data-stu-id="bb6e6-128">Previous step</span></span>
[<span data-ttu-id="bb6e6-129">Запуск эксперимента и контроль за ним</span><span class="sxs-lookup"><span data-stu-id="bb6e6-129">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
