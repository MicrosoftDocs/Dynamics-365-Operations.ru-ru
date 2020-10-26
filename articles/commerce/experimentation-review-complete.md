---
title: Повышение вариации и завершение эксперимента
description: В этом разделе описывается, как повысить успешную вариацию и завершить эксперимент в Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 09/15/2020
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
ms.openlocfilehash: 2e011f10e908d6a2efe2e928fc5e0abc7659cb8b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930272"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="cbb06-103">Повышение вариации и завершение эксперимента</span><span class="sxs-lookup"><span data-stu-id="cbb06-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="cbb06-104">В этом разделе описывается, как повысить вариацию, которая дает наилучший результат в эксперименте, и как завершить эксперимент.</span><span class="sxs-lookup"><span data-stu-id="cbb06-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="cbb06-105">На следующей схеме показаны все шаги настройки и запуска эксперимента на веб-сайте электронной коммерции в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cbb06-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="cbb06-106">Дополнительные шаги описаны в отдельных разделах.</span><span class="sxs-lookup"><span data-stu-id="cbb06-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="cbb06-107">[ ![Путь взаимодействия пользователя с экспериментами — проверка и завершение](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="cbb06-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="cbb06-108">После [выполнения эксперимента](experimentation-run-monitor.md) и сбора необходимых данных для определения вариации, которую вы хотите использовать на своем веб-сайте, вы сможете повысить вариацию и завершить эксперимент.</span><span class="sxs-lookup"><span data-stu-id="cbb06-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="cbb06-109">Повышение вариации</span><span class="sxs-lookup"><span data-stu-id="cbb06-109">Promote a variation</span></span>
<span data-ttu-id="cbb06-110">Воспользуйтесь данными и аналитикой, относящимися к эксперименту в сторонней службе, чтобы определить, какая из вариантов дает наилучший результат.</span><span class="sxs-lookup"><span data-stu-id="cbb06-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="cbb06-111">Чтобы заменить текущее содержимое действующего сайта на измененный вариант, чтобы он был доступен всем пользователям веб-сайта, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cbb06-111">To replace the current content on the live site with the winning variation so that it's available to all users of your website, do the following.</span></span> 

1. <span data-ttu-id="cbb06-112">Перейдите на вкладку **Эксперименты** в конфигураторе сайтов и выберите эксперимент.</span><span class="sxs-lookup"><span data-stu-id="cbb06-112">Go to the **Experiments** tab in site builder and select the experiment.</span></span>
1. <span data-ttu-id="cbb06-113">Выберите **Завершить эксперимент** на верхней панели.</span><span class="sxs-lookup"><span data-stu-id="cbb06-113">Select **Complete experiment** on the top bar.</span></span>
1. <span data-ttu-id="cbb06-114">В диалоговом окне **Завершение эксперимента** выберите **Просмотреть данные эксперимента**.</span><span class="sxs-lookup"><span data-stu-id="cbb06-114">In the **Complete the experiment** dialog menu, select **Review the experiment data**.</span></span> <span data-ttu-id="cbb06-115">Открывается сторонняя служба, в которой можно проверить метрики и определить, какой вариант работает наилучшим образом.</span><span class="sxs-lookup"><span data-stu-id="cbb06-115">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="cbb06-116">В диалоговом меню **Завершение эксперимента** в конфигураторе сайтов выберите лучший вариант, затем выберите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="cbb06-116">In the **Complete the experiment** dialog menu in site builder, select the winning variation and then select **Next**.</span></span>
1. <span data-ttu-id="cbb06-117">Откройте стороннюю службу и остановите эксперимент.</span><span class="sxs-lookup"><span data-stu-id="cbb06-117">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="cbb06-118">В конфигураторе сайтов выберите **Завершить**, чтобы переписать исходную действующую страницу и опубликовать победивший вариант, чтобы он был доступен всем пользователям веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="cbb06-118">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="cbb06-119">Если вы решили сохранить текущую действующую страницу и не опубликовать вариант, выберите **Повторно опубликовать исходную страницу**.</span><span class="sxs-lookup"><span data-stu-id="cbb06-119">If you choose to keep the current live page and not publish a variation, select **Republish the original page**.</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="cbb06-120">Удаление эксперимента</span><span class="sxs-lookup"><span data-stu-id="cbb06-120">Delete your experiment</span></span>
<span data-ttu-id="cbb06-121">Хотя не требуется удалять завершенный эксперимент в Commerce, можно удалить его, чтобы сэкономить место или очистить рабочую область.</span><span class="sxs-lookup"><span data-stu-id="cbb06-121">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> <span data-ttu-id="cbb06-122">Чтобы удалить эксперимент, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cbb06-122">To delete an experiment, do the following.</span></span>

1. <span data-ttu-id="cbb06-123">Перейдите на вкладку **Эксперименты** в конфигураторе сайтов и выберите эксперимент.</span><span class="sxs-lookup"><span data-stu-id="cbb06-123">Go to the **Experiments** tab in site builder and select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="cbb06-124">Если эксперимент все еще активен, перед продолжением остановите выполнение эксперимента в сторонней службе.</span><span class="sxs-lookup"><span data-stu-id="cbb06-124">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="cbb06-125">На панели команд выберите **Отменить публикацию**, чтобы удалить содержимое варианта с действующего сайта.</span><span class="sxs-lookup"><span data-stu-id="cbb06-125">Select **Unpublish** in the command bar to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="cbb06-126">Выберите **Удалить** на панели команд, чтобы удалить эксперимент.</span><span class="sxs-lookup"><span data-stu-id="cbb06-126">Select **Delete** in the command bar to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="cbb06-127">Предыдущий шаг</span><span class="sxs-lookup"><span data-stu-id="cbb06-127">Previous step</span></span>
[<span data-ttu-id="cbb06-128">Запуск и контроль эксперимента</span><span class="sxs-lookup"><span data-stu-id="cbb06-128">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
