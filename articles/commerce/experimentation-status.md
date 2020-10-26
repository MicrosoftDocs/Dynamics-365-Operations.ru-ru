---
title: Проверка статуса эксперимента
description: В этой теме объясняется, какой статус эксперимента имеет жизненный цикл экспериментов в Dynamics 365 Commerce.
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
ms.openlocfilehash: 097206c0aa487e14499bdf3907465e17b7d337e2
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930273"
---
# <a name="review-the-status-of-an-experiment"></a><span data-ttu-id="0b924-103">Проверка статуса эксперимента</span><span class="sxs-lookup"><span data-stu-id="0b924-103">Review the status of an experiment</span></span>
<span data-ttu-id="0b924-104">Имеется множество шагов, связанных с настройкой и запуском эксперимента в Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0b924-104">There are many steps involved in setting up and running an experiment in Dynamics 365 Commerce.</span></span> <span data-ttu-id="0b924-105">Сведения о жизненном цикле экспериментов см. в разделе [Эксперименты в Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0b924-105">For information about the experimentation lifecycle, see [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="0b924-106">Чтобы узнать, где находится эксперимент в жизненном цикле, перейдите на вкладку **Эксперименты** в конфигураторе сайтов.</span><span class="sxs-lookup"><span data-stu-id="0b924-106">To learn where an experiment is in the lifecycle, go to the **Experiments** tab in site builder.</span></span> <span data-ttu-id="0b924-107">Отображается список экспериментов со статусом каждого эксперимента в Commerce и сторонней службой, которая используется для создания экспериментов, назначения вариаций и анализа данных.</span><span class="sxs-lookup"><span data-stu-id="0b924-107">A list of experiments is displayed with the status of each experiment in both Commerce and the third-party service that is being used to enable the creation of experiments, assign variations, and analyze data.</span></span>

<span data-ttu-id="0b924-108">В столбце **Статус Commerce** могут отображаться следующие значения.</span><span class="sxs-lookup"><span data-stu-id="0b924-108">In the **Commerce status** column, the following values may be displayed.</span></span> 
- <span data-ttu-id="0b924-109">**Черновик** — эксперимент связан со страницей или фрагментом в модуле Commerce и редактируется в данный момент.</span><span class="sxs-lookup"><span data-stu-id="0b924-109">**Draft** - The experiment is connected to a page or fragment in Commerce and is being edited.</span></span>
- <span data-ttu-id="0b924-110">**Опубликовано** — варианты экспериментов готовы для отображения на веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="0b924-110">**Published** - The experiment variations are ready to be displayed on your website.</span></span> <span data-ttu-id="0b924-111">Если эксперимент запущен в сторонней службе, пользователи веб-сайта увидят вариант страницы или фрагмента, выбранный в сторонней службе.</span><span class="sxs-lookup"><span data-stu-id="0b924-111">If the experiment is running in the third-party service, website users will see a variation of the page or fragment as selected by the third-party service.</span></span>
- <span data-ttu-id="0b924-112">**Не опубликовано** — эксперимент более не доступен на вашем веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="0b924-112">**Unpublished** - The experiment is no longer available on your website.</span></span> <span data-ttu-id="0b924-113">Пользователи веб-сайта увидят только вариант по умолчанию страницы или фрагмента, даже если эксперимент запущен в сторонней службе.</span><span class="sxs-lookup"><span data-stu-id="0b924-113">Website users will only see the default version of the page or fragment even if the experiment is running in the third-party service.</span></span>
- <span data-ttu-id="0b924-114">**Завершено** — эксперимент прошел свое выполнение, и вариант был повышен до действующего для всех пользователей веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="0b924-114">**Completed** - The experiment has run its course and a variation was promoted to live for all website users.</span></span>

<span data-ttu-id="0b924-115">Аналогично, в столбце **статуса третьей стороны** могут отображаться следующие значения, показывающие, какой статус экспериментов имеются в сторонней службой.</span><span class="sxs-lookup"><span data-stu-id="0b924-115">Similarly, in the **third-party status** column, the following values may be displayed to indicate what status the experiments are in the third-party service.</span></span>
- <span data-ttu-id="0b924-116">**Черновик** — эксперимент настроен в сторонней службе, но еще не запущен.</span><span class="sxs-lookup"><span data-stu-id="0b924-116">**Draft** - The experiment is set up in the third-party service but hasn't been started.</span></span>
- <span data-ttu-id="0b924-117">**Запущен** — эксперимент был запущен в сторонней службе и собирает данные.</span><span class="sxs-lookup"><span data-stu-id="0b924-117">**Running** - The experiment was started in the third-party service and is collecting data.</span></span>
- <span data-ttu-id="0b924-118">**Приостановлено** — эксперимент приостановлен и не собирает данные.</span><span class="sxs-lookup"><span data-stu-id="0b924-118">**Paused** - The experiment is paused and not collecting data.</span></span> <span data-ttu-id="0b924-119">Необходимо возобновить эксперимент, чтобы он снова начал собирать данные.</span><span class="sxs-lookup"><span data-stu-id="0b924-119">You must resume the experiment for it to collect data again.</span></span>
- <span data-ttu-id="0b924-120">**Архивный** — программа эксперимента выполнена и он был зарегистрирован в сторонней службе для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="0b924-120">**Archived** - The experiment has run its course and has been cataloged in the third-party service for future reference.</span></span>

<span data-ttu-id="0b924-121">На приведенной ниже диаграмме показаны как наборы статусов, так и их связь друг с другом.</span><span class="sxs-lookup"><span data-stu-id="0b924-121">The diagram below shows both sets of statuses and how they relate to each other.</span></span>

<span data-ttu-id="0b924-122">[ ![Статусы экспериментирования](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="0b924-122">[ ![Experimentation statuses](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span></span>
