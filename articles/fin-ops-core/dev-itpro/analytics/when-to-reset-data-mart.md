---
title: Когда следует сбрасывать киоск данных
description: В этой теме перечислены обстоятельства, которые могут быть улучшены путем сброса киоска данных, и ситуации, в которых сброс киоска данных вряд ли будет помогать.
author: jinniew
ms.date: 05/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: bc2c4ee490f3bebd6e7c91609a06f8dfedfcb628
ms.sourcegitcommit: 5916ea2a94ab9af7aac21f0fc44e194d5ce82917
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2021
ms.locfileid: "5989000"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="f9758-103">Когда следует сбрасывать киоск данных</span><span class="sxs-lookup"><span data-stu-id="f9758-103">When to reset a data mart</span></span>

<span data-ttu-id="f9758-104">Сброс киоска данных может занять много времени.</span><span class="sxs-lookup"><span data-stu-id="f9758-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="f9758-105">В зависимости от обстоятельств, это действие может не быть требуемым решением.</span><span class="sxs-lookup"><span data-stu-id="f9758-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="f9758-106">В этой теме перечислены обстоятельства, которые могут быть улучшены путем сброса киоска данных, а также ситуации, в которых сброс киоска данных вряд ли будет помогать.</span><span class="sxs-lookup"><span data-stu-id="f9758-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-i-need-to-do-a-data-mart-reset"></a><span data-ttu-id="f9758-107">Когда необходимо выполнить сброс киоска данных?</span><span class="sxs-lookup"><span data-stu-id="f9758-107">When do I need to do a data mart reset?</span></span>
<span data-ttu-id="f9758-108">Прежде чем выполнять сброс киоска данных, следует рассмотреть следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="f9758-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="f9758-109">Ответ да на один или несколько вопросов может указывать на то, что организация может получить преимущества, выполнив сброс киоска данных.</span><span class="sxs-lookup"><span data-stu-id="f9758-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="f9758-110">Была ли база данных приложения восстановлена?</span><span class="sxs-lookup"><span data-stu-id="f9758-110">Was the application database restored?</span></span>
- <span data-ttu-id="f9758-111">Если вы открыли инцидент поддержки, а специалист службы технической поддержки дал вам инструкцию выполнить сброс киоска данных в рамках шага устранения неполадок?</span><span class="sxs-lookup"><span data-stu-id="f9758-111">If you've opened a support incident that and a support engineer has instructed you to reset the data mart as part of a troubleshooting step?</span></span>
 
## <a name="when-is-it-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="f9758-112">Когда не нужно сбрасывать киоск данных?</span><span class="sxs-lookup"><span data-stu-id="f9758-112">When is it not appropriate to reset a data mart?</span></span>
<span data-ttu-id="f9758-113">В некоторых случаях не рекомендуется выполнять сброс киоска данных.</span><span class="sxs-lookup"><span data-stu-id="f9758-113">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="f9758-114">К ним относится следующие.</span><span class="sxs-lookup"><span data-stu-id="f9758-114">These include the following.</span></span> 

- <span data-ttu-id="f9758-115">У вас возникли проблемы с производительностью, связанные с синхронизацией данных.</span><span class="sxs-lookup"><span data-stu-id="f9758-115">You're experiencing performance issues that are associated with a data sync.</span></span> 
- <span data-ttu-id="f9758-116">Если имеется повторяющийся шаблон перезапуска по одной из следующих причин:</span><span class="sxs-lookup"><span data-stu-id="f9758-116">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="f9758-117">**Отсутствующие данные**</span><span class="sxs-lookup"><span data-stu-id="f9758-117">**Missing data**</span></span> 
  - <span data-ttu-id="f9758-118">**Состояние зависшей интеграции**</span><span class="sxs-lookup"><span data-stu-id="f9758-118">**Stuck integration state**</span></span> 
  - <span data-ttu-id="f9758-119">**Устаревшие записи** — устаревшие записи сами по себе не обязательно оправдывают сброс киоска данных.</span><span class="sxs-lookup"><span data-stu-id="f9758-119">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="f9758-120">Если имеется большой набор данных, выполнение процесса сброса займет некоторое время, но маловероятно, что это приведет к улучшению.</span><span class="sxs-lookup"><span data-stu-id="f9758-120">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="f9758-121">Что такое сброс киоска данных?</span><span class="sxs-lookup"><span data-stu-id="f9758-121">What is a data mart reset?</span></span>
- <span data-ttu-id="f9758-122">Сброс начнет выполняться только после завершения существующих задач.</span><span class="sxs-lookup"><span data-stu-id="f9758-122">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="f9758-123">Это гарантирует, что старые данные не вставляются.</span><span class="sxs-lookup"><span data-stu-id="f9758-123">This ensures that old data is not inserted.</span></span> <span data-ttu-id="f9758-124">На этом этапе может появиться сообщение, такое как "Не удалось обработать сброс киоска данных из-за активной задачи.</span><span class="sxs-lookup"><span data-stu-id="f9758-124">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="f9758-125">Повторите попытку позже".</span><span class="sxs-lookup"><span data-stu-id="f9758-125">Please try again later.”</span></span>
- <span data-ttu-id="f9758-126">Сброс отключит задачи интеграции и удалит все данные киоска данных.</span><span class="sxs-lookup"><span data-stu-id="f9758-126">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="f9758-127">Интеграция повторно включается.</span><span class="sxs-lookup"><span data-stu-id="f9758-127">The integration is re-enabled.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="f9758-128">Если я сбрасываю киоск данных, я потеряю уже разработанные мной отчеты?</span><span class="sxs-lookup"><span data-stu-id="f9758-128">If I reset the data mart, will I lose reports that I've already designed?</span></span> 
<span data-ttu-id="f9758-129">Нет, отчеты хранятся в таблицах SQL, которые не влияют на сброс киоска данных.</span><span class="sxs-lookup"><span data-stu-id="f9758-129">No, your reports are stored in SQL tables that are not impacted by a reset of the data mart.</span></span> <span data-ttu-id="f9758-130">Если вы не уверены в том, что все созданные отчеты были удалены, можно создать резервные копии проектов, которые важно не потерять.</span><span class="sxs-lookup"><span data-stu-id="f9758-130">If you are concerned about losing any reports you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="f9758-131">Чтобы создать резервные копии, откройте конструктор отчетов и перейдите **Компания > Компании > Шаблоны > Экспорт**.</span><span class="sxs-lookup"><span data-stu-id="f9758-131">To back them up, open Report Designer and go to **Company > Companies > Building Blocks > Export**.</span></span>
 
## <a name="is-it-necessary-for-all-users-to-exit-the-system-to-reset-the-data-mart"></a><span data-ttu-id="f9758-132">Необходимо ли для всех пользователей выходить из системы, чтобы сбросить киоск данных?</span><span class="sxs-lookup"><span data-stu-id="f9758-132">Is it necessary for all users to exit the system to reset the data mart?</span></span>
<span data-ttu-id="f9758-133">Нет, пользователи могут продолжать работать в системе во время сброса киоска данных.</span><span class="sxs-lookup"><span data-stu-id="f9758-133">No, users can continue working in the system during the data mart reset.</span></span> <span data-ttu-id="f9758-134">Однако они не смогут получить доступ к отчетам, созданным с помощью Financial Reporter, пока не будет завершен сброс.</span><span class="sxs-lookup"><span data-stu-id="f9758-134">However, they won’t be able to access any reports that were created with Financial Reporter until the reset is finished.</span></span> 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
