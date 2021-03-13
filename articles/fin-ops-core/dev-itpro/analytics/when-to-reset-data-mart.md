---
title: Когда следует сбрасывать киоск данных
description: В этой теме перечислены обстоятельства, которые могут быть улучшены путем сброса киоска данных, и ситуации, в которых сброс киоска данных вряд ли будет помогать.
author: jinniew
manager: AnnBe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1c1524c7a1a3fbe71c51b23571996d87641cdf7e
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093220"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="c93ab-103">Когда следует сбрасывать киоск данных</span><span class="sxs-lookup"><span data-stu-id="c93ab-103">When to reset a data mart</span></span>

<span data-ttu-id="c93ab-104">Сброс киоска данных может занять много времени.</span><span class="sxs-lookup"><span data-stu-id="c93ab-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="c93ab-105">В зависимости от обстоятельств, это действие может не быть требуемым решением.</span><span class="sxs-lookup"><span data-stu-id="c93ab-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="c93ab-106">В этой теме перечислены обстоятельства, которые могут быть улучшены путем сброса киоска данных, а также ситуации, в которых сброс киоска данных вряд ли будет помогать.</span><span class="sxs-lookup"><span data-stu-id="c93ab-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-you-need-to-do-a-data-mart-reset"></a><span data-ttu-id="c93ab-107">Когда необходимо выполнить сброс киоска данных?</span><span class="sxs-lookup"><span data-stu-id="c93ab-107">When do you need to do a data mart reset?</span></span>
<span data-ttu-id="c93ab-108">Прежде чем выполнять сброс киоска данных, следует рассмотреть следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="c93ab-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="c93ab-109">Ответ да на один или несколько вопросов может указывать на то, что организация может получить преимущества, выполнив сброс киоска данных.</span><span class="sxs-lookup"><span data-stu-id="c93ab-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="c93ab-110">База данных приложения была восстановлена, но база данных киоска данных не была восстановлена.</span><span class="sxs-lookup"><span data-stu-id="c93ab-110">The application database was restored, but the data mart database was not restored.</span></span>
- <span data-ttu-id="c93ab-111">Отображаются неверные данные для учетного периода, которые не являются результатом проблемы с дизайном отчета.</span><span class="sxs-lookup"><span data-stu-id="c93ab-111">You see incorrect data for an accounting period, which isn't the result of an issue with the report design.</span></span>
- <span data-ttu-id="c93ab-112">Отображаются неправильные данные для учетного периода, а записи, перечисленные для попыток интеграции на странице **Состояние интеграции** в конструкторе отчетов (запустите конструктор отчетов и выберите **Сервис > Состояние интеграции**).</span><span class="sxs-lookup"><span data-stu-id="c93ab-112">You see incorrect data for an accounting period, and records are listed under Integration attempts on the **Integration status** page in Report Designer (start the Report Designer and select **Tools > Integration status**).</span></span>
- <span data-ttu-id="c93ab-113">Вы открыли инцидент поддержки, а специалист службы технической поддержки дал вам инструкцию выполнить сброс киоска данных в рамках шага устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="c93ab-113">You've opened a support incident and a support engineer has instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-its-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="c93ab-114">Когда не нужно сбрасывать киоск данных?</span><span class="sxs-lookup"><span data-stu-id="c93ab-114">When it's not appropriate to reset a data mart?</span></span>
<span data-ttu-id="c93ab-115">В некоторых случаях не рекомендуется выполнять сброс киоска данных.</span><span class="sxs-lookup"><span data-stu-id="c93ab-115">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="c93ab-116">К ним относится следующие.</span><span class="sxs-lookup"><span data-stu-id="c93ab-116">These include the following.</span></span> 

- <span data-ttu-id="c93ab-117">Когда причина не представлена в этой теме.</span><span class="sxs-lookup"><span data-stu-id="c93ab-117">Anytime the reason isn’t listed in this topic.</span></span>
- <span data-ttu-id="c93ab-118">У вас возникли проблемы с производительностью, связанные с синхронизацией данных. В этом случае сброс киоска данных, скорее всего, не поможет.</span><span class="sxs-lookup"><span data-stu-id="c93ab-118">You're experiencing performance issues that are associated with a data sync. In this circumstance, resetting the data mart probably won't help.</span></span>
- <span data-ttu-id="c93ab-119">Если имеется повторяющийся шаблон перезапуска по одной из следующих причин:</span><span class="sxs-lookup"><span data-stu-id="c93ab-119">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="c93ab-120">**Отсутствующие данные** — во-первых, устраните ошибки дизайна отчета и синхронизации данных. Например, вы наблюдаете, что сопоставление фактов не было выполнено с момента разноски отсутствующих данных.</span><span class="sxs-lookup"><span data-stu-id="c93ab-120">**Missing data** - First, eliminate report design issues and data sync timing issues, for example, you observe that the fact map hasn’t run since missing data was posted.</span></span>
  - <span data-ttu-id="c93ab-121">**Состояние зависшей интеграции** — если интеграция работает медленно или кажется зависшей, выполнение сброса киоска данных вряд ли поможет устранить проблему.</span><span class="sxs-lookup"><span data-stu-id="c93ab-121">**Stuck integration state** - If the integration is slow or seems stuck, resetting the data mart is unlikely to resolve the issue.</span></span>
  - <span data-ttu-id="c93ab-122">**Попытки сброса были выполнены неудачно** — если было сделано несколько попыток выполнить сброс, и они не были выполнены из-за отсутствия данных, рекомендуется открыть обращение в службу поддержки и работать со специалистом службы поддержки, чтобы проанализировать ситуацию перед повторной попыткой сбросить киоск данных.</span><span class="sxs-lookup"><span data-stu-id="c93ab-122">**Attempts to reset have been unsuccessful** - If a number of attempts to complete a reset have been made, and have been unsuccessful because of missing data, we recommend opening a support incident and working with a support engineer to analyze your situation before attempting to reset the data mart again.</span></span>
  - <span data-ttu-id="c93ab-123">**Устаревшие записи** — устаревшие записи сами по себе не обязательно оправдывают сброс киоска данных.</span><span class="sxs-lookup"><span data-stu-id="c93ab-123">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="c93ab-124">Если имеется большой набор данных, выполнение процесса сброса займет некоторое время, но маловероятно, что это приведет к улучшению.</span><span class="sxs-lookup"><span data-stu-id="c93ab-124">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-a-data-mart-reset-does-not-do"></a><span data-ttu-id="c93ab-125">Что не выполняет сброс киоска данных</span><span class="sxs-lookup"><span data-stu-id="c93ab-125">What a data mart reset does not do</span></span>  
- <span data-ttu-id="c93ab-126">Сброс начнет выполняться только после завершения существующих задач.</span><span class="sxs-lookup"><span data-stu-id="c93ab-126">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="c93ab-127">Это гарантирует, что старые данные не вставляются.</span><span class="sxs-lookup"><span data-stu-id="c93ab-127">This ensures that old data is not inserted.</span></span> <span data-ttu-id="c93ab-128">На этом этапе может появиться сообщение, такое как "Не удалось обработать сброс киоска данных из-за активной задачи.</span><span class="sxs-lookup"><span data-stu-id="c93ab-128">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="c93ab-129">Повторите попытку позже".</span><span class="sxs-lookup"><span data-stu-id="c93ab-129">Please try again later.”</span></span>
- <span data-ttu-id="c93ab-130">Сброс отключит задачи интеграции и удалит все данные киоска данных.</span><span class="sxs-lookup"><span data-stu-id="c93ab-130">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="c93ab-131">Интеграция повторно включается.</span><span class="sxs-lookup"><span data-stu-id="c93ab-131">The integration is re-enabled.</span></span>

> [!NOTE]
> <span data-ttu-id="c93ab-132">В следующих пунктах указываются две вещи, которые сброс киоска данных *не* делает.</span><span class="sxs-lookup"><span data-stu-id="c93ab-132">The following points specify two things that resetting a data mart will *not* do.</span></span> <br>
> - <span data-ttu-id="c93ab-133">Сбросы не очищают дизайны отчетов.</span><span class="sxs-lookup"><span data-stu-id="c93ab-133">Resets do not clear report designs.</span></span> <br>
> - <span data-ttu-id="c93ab-134">Сбросы не удаляют данные компании или данные пользователя, если они не выбраны.</span><span class="sxs-lookup"><span data-stu-id="c93ab-134">Resets do not clear company data or user data unless selected.</span></span>
