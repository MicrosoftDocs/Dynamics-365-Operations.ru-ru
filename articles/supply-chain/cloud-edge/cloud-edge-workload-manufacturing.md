---
title: Рабочие нагрузки управления производством для облачных и пограничных единиц масштабирования
description: В этой теме описывается, как рабочие нагрузки выполнения производства работают с облачными и пограничными единицами масштабирования.
author: cabeln
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9cd7dd8b9241171bdfdb3cc1379211a2fe99bbe1
ms.sourcegitcommit: 8d50c905a0c9d4347519549b587bdebab8ffc628
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2021
ms.locfileid: "6184004"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a><span data-ttu-id="53404-103">Производственные рабочие нагрузки для облачных и пограничных единиц масштабирования</span><span class="sxs-lookup"><span data-stu-id="53404-103">Manufacturing execution workloads for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="53404-104">Рабочая нагрузка выполнения производства доступна в предварительной версии на данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="53404-104">The manufacturing execution workload is available in preview at this point in time.</span></span>
> <span data-ttu-id="53404-105">Некоторые бизнес-функции не полностью поддерживаются в общедоступной предварительной версии, когда используются единицы масштабирования рабочей нагрузки.</span><span class="sxs-lookup"><span data-stu-id="53404-105">Some business functionality isn't fully supported in the public preview when workload scale units are used.</span></span>

<span data-ttu-id="53404-106">В управлении производством единицы масштабирования доставляют следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="53404-106">In manufacturing execution, scale units deliver the following capabilities:</span></span>

- <span data-ttu-id="53404-107">У операторов компьютеров и руководителей цеха есть доступ к рабочему плану производства.</span><span class="sxs-lookup"><span data-stu-id="53404-107">Machine operators and shop floor supervisors can access the operational production plan.</span></span>
- <span data-ttu-id="53404-108">Операторы компьютеров могут сохранять план актуальным, выполняя дискретные и обрабатывающие производственные задания.</span><span class="sxs-lookup"><span data-stu-id="53404-108">Machine operators can keep the plan up to date by running discrete and process manufacturing jobs.</span></span>
- <span data-ttu-id="53404-109">Начальник цеха может скорректировать план операций.</span><span class="sxs-lookup"><span data-stu-id="53404-109">The shop floor supervisor can adjust the operational plan.</span></span>
- <span data-ttu-id="53404-110">Работники могут получить доступ к времени и посещаемости для прихода на работу и ухода с работы в пограничном модуле, чтобы обеспечить правильный расчет оплаты работника.</span><span class="sxs-lookup"><span data-stu-id="53404-110">Workers can access time and attendance for clock-in and clock-out on the edge, to ensure correct worker pay calculation.</span></span>

<span data-ttu-id="53404-111">В этой теме описывается, как рабочие нагрузки выполнения производства работают с облачными и пограничными единицами масштабирования.</span><span class="sxs-lookup"><span data-stu-id="53404-111">This topic describes how manufacturing execution workloads work with cloud and edge scale units.</span></span>

## <a name="the-manufacturing-lifecycle"></a><span data-ttu-id="53404-112">Жизненный цикл производства</span><span class="sxs-lookup"><span data-stu-id="53404-112">The manufacturing lifecycle</span></span>

<span data-ttu-id="53404-113">Как показано на следующем рисунке, жизненный цикл производства делится на три этапа: *Планирование*, *Выполнение* и *Завершение*.</span><span class="sxs-lookup"><span data-stu-id="53404-113">As the following illustration shows, the manufacturing lifecycle is divided into three phases: *Plan*, *Execute*, and *Finalize*.</span></span>

<span data-ttu-id="53404-114">[![Этапы выполнения производства, когда используется одна среда](media/mes-phases.png "Этапы выполнения производства, когда используется одна среда")](media/mes-phases-large.png)</span><span class="sxs-lookup"><span data-stu-id="53404-114">[![Manufacturing execution phases when a single environment is used](media/mes-phases.png "Manufacturing execution phases when a single environment is used")](media/mes-phases-large.png)</span></span>

<span data-ttu-id="53404-115">Стадия _Планирование_ включает в себя определение продукта, планирование, создание заказа и планирование, а также выпуск.</span><span class="sxs-lookup"><span data-stu-id="53404-115">The _Plan_ phase includes product definition, planning, order creation and scheduling, and release.</span></span> <span data-ttu-id="53404-116">Шаг выпуска указывает переход с этапа _Планирование_ на этап _Выполнение_.</span><span class="sxs-lookup"><span data-stu-id="53404-116">The release step indicates the transition from the _Plan_ phase to the _Execute_ phase.</span></span> <span data-ttu-id="53404-117">Когда выпускается производственный заказ, задания производственного заказа будут видны в производственном цехе и готовы к выполнению.</span><span class="sxs-lookup"><span data-stu-id="53404-117">When a production order is released, the production order jobs will be visible on the production floor and ready for execution.</span></span>

<span data-ttu-id="53404-118">Когда производственное задание помечается как завершенное, оно перемещается с этапа _Выполнение_ на этап _Завершение_.</span><span class="sxs-lookup"><span data-stu-id="53404-118">When a production job is marked as completed, it moves from the _Execute_ phase to the _Finalize_ phase.</span></span> <span data-ttu-id="53404-119">На этапе _Завершение_ регистрации из этапа *Выполнение* проходят через рабочий процесс утверждения, где они рассчитываются, утверждаются и переносятся.</span><span class="sxs-lookup"><span data-stu-id="53404-119">In the _Finalize_ phase, the registrations from the *Execute* phase go through an approval workflow, where they are calculated, approved, and transferred.</span></span> <span data-ttu-id="53404-120">В этот момент производственный заказ завершается.</span><span class="sxs-lookup"><span data-stu-id="53404-120">At that point, the production order is completed.</span></span> <span data-ttu-id="53404-121">Таким образом создается основа для оплаты сотрудников.</span><span class="sxs-lookup"><span data-stu-id="53404-121">Therefore, the basis for the workers' pay is generated.</span></span>

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a><span data-ttu-id="53404-122">Разбиение этапа выполнения на отдельную рабочую нагрузку</span><span class="sxs-lookup"><span data-stu-id="53404-122">Splitting the Execute phase into a separate workload</span></span>

<span data-ttu-id="53404-123">Как показано на следующем рисунке, при использовании единицы масштабирования этап _Выполнение_ разделяется как отдельная рабочая нагрузка.</span><span class="sxs-lookup"><span data-stu-id="53404-123">As the following illustration shows, when scale units are used, the _Execute_ phase is split out as a separate workload.</span></span>

<span data-ttu-id="53404-124">[![Этапы выполнения производства при использовании единиц масштабирования](media/mes-phases-workloads.png "Этапы выполнения производства при использовании единиц масштабирования")](media/mes-phases-workloads-large.png)</span><span class="sxs-lookup"><span data-stu-id="53404-124">[![Manufacturing execution phases when scale units are used](media/mes-phases-workloads.png "Manufacturing execution phases when scale units are used")](media/mes-phases-workloads-large.png)</span></span>

<span data-ttu-id="53404-125">Модель теперь переходит из установки с одним экземпляром на модель, основанную на концентраторе и модулях масштабирования.</span><span class="sxs-lookup"><span data-stu-id="53404-125">The model now goes from a single-instance installation to a model that is based on the hub and scale units.</span></span> <span data-ttu-id="53404-126">Этапы _Планирование_ и _Завершение_ выполняются как операции бэк-офиса на концентраторе, а рабочая нагрузка управления производством выполняется на единицах масштабирования.</span><span class="sxs-lookup"><span data-stu-id="53404-126">The _Plan_ and _Finalize_ phases run as back-office operations on the hub, and the manufacturing execution workload runs on the scale units.</span></span> <span data-ttu-id="53404-127">Данные передаются асинхронно между концентратором и единицами масштабирования.</span><span class="sxs-lookup"><span data-stu-id="53404-127">Data is transferred asynchronously between the hub and scale units.</span></span>

<span data-ttu-id="53404-128">Когда производственный заказ выпускается на концентраторе, все данные, необходимые для обработки производственных заданий, переносятся в единицу масштабирования.</span><span class="sxs-lookup"><span data-stu-id="53404-128">When a production order is released on the hub, all data that is required to process production jobs is transferred to the scale unit.</span></span> <span data-ttu-id="53404-129">Эти данные включают в себя производственные заказы, маршруты производства, спецификации и продукты.</span><span class="sxs-lookup"><span data-stu-id="53404-129">This data includes production orders, production routes, bills of materials, and products.</span></span> <span data-ttu-id="53404-130">Данные, не имеющие отношения к производственному заказу (например, дополнительные мероприятия, коды отсутствия и производственные параметры), также переносятся из концентратора в единицу масштабирования.</span><span class="sxs-lookup"><span data-stu-id="53404-130">Data that isn't related to a production order (such as indirect activities, absence codes, and production parameters) is also transferred from the hub to the scale unit.</span></span> <span data-ttu-id="53404-131">Как правило, данные, поступающие от концентратора, которые передаются в единицу масштабирования, могут быть созданы или обновлены только в концентраторе.</span><span class="sxs-lookup"><span data-stu-id="53404-131">As a rule, data that originates from the hub and that is transferred to the scale unit can be created or updated only on the hub.</span></span> <span data-ttu-id="53404-132">Например, невозможно создать новый код отсутствия или дополнительное мероприятие в единице масштабирования, &mdash; они могут использоваться только для регистрации.</span><span class="sxs-lookup"><span data-stu-id="53404-132">For example, a new absence code or indirect activity can't be created on the scale unit&mdash;they can be used only for registration.</span></span> <span data-ttu-id="53404-133">Регистрации, сделанные в единицах масштабирования во время выполнения, затем переносятся на концентратор, где обрабатываются утверждение времени и посещаемости, запасы и финансовые обновления.</span><span class="sxs-lookup"><span data-stu-id="53404-133">The registrations that are made on the scale unit during execution are then transferred to the hub, where time and attendance approval, inventory, and financial updates are processed.</span></span>

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a><span data-ttu-id="53404-134">Задачи выполнения производства, которые могут выполняться на рабочих нагрузках</span><span class="sxs-lookup"><span data-stu-id="53404-134">Manufacturing execution tasks that can be run on workloads</span></span>

<span data-ttu-id="53404-135">При использовании единиц масштабирования на рабочих нагрузках в настоящее время могут выполняться следующие задачи выполнения производства:</span><span class="sxs-lookup"><span data-stu-id="53404-135">The following manufacturing execution tasks can currently be run on workloads when scale units are used:</span></span>

- <span data-ttu-id="53404-136">Время прихода, вход, время ухода и отсутствие</span><span class="sxs-lookup"><span data-stu-id="53404-136">Clock-in, log-in, clock-out, and absence</span></span>
- <span data-ttu-id="53404-137">Запустить задание</span><span class="sxs-lookup"><span data-stu-id="53404-137">Start job</span></span>
- <span data-ttu-id="53404-138">Объединение заданий</span><span class="sxs-lookup"><span data-stu-id="53404-138">Bundle jobs</span></span>
- <span data-ttu-id="53404-139">Проверить ход выполнения</span><span class="sxs-lookup"><span data-stu-id="53404-139">Report progress</span></span>
- <span data-ttu-id="53404-140">Сообщить об отходах</span><span class="sxs-lookup"><span data-stu-id="53404-140">Report scrap</span></span>
- <span data-ttu-id="53404-141">Дополнительное мероприятие</span><span class="sxs-lookup"><span data-stu-id="53404-141">Indirect activity</span></span>
- <span data-ttu-id="53404-142">Перерыв</span><span class="sxs-lookup"><span data-stu-id="53404-142">Break</span></span>
- <span data-ttu-id="53404-143">Приемка и размещение (требует также запуска рабочей нагрузки выполнения склада в единице масштабирования, см. также раздел [Приемка и размещение в единице масштабирования](#RAF))</span><span class="sxs-lookup"><span data-stu-id="53404-143">Report as finished and putaway (requires that you also run the warehouse execution workload on your scale unit, see also [Report as finished and putaway on a scale unit](#RAF))</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a><span data-ttu-id="53404-144">Работа с рабочими нагрузками управления производством в концентраторе</span><span class="sxs-lookup"><span data-stu-id="53404-144">Working with manufacturing execution workloads on the hub</span></span>

<span data-ttu-id="53404-145">Обычно процессы, необходимые для запуска рабочих нагрузок в модуле управления производством, запускаются автоматически для обеспечения синхронизации концентратора и всех единиц масштабирования в соответствии с требованиями.</span><span class="sxs-lookup"><span data-stu-id="53404-145">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="53404-146">Однако при возникновении проблем можно вручную запустить обработку регистраций сырья, полученных из рабочих нагрузок, и/или проверить журнал обработки регистрации.</span><span class="sxs-lookup"><span data-stu-id="53404-146">However, if you're having trouble, you can manually trigger the processing of raw registrations that are received from workloads and/or check the registration processing log.</span></span>

### <a name="manually-process-raw-registrations"></a><span data-ttu-id="53404-147">Обработка регистраций сырья вручную</span><span class="sxs-lookup"><span data-stu-id="53404-147">Manually process raw registrations</span></span>

<span data-ttu-id="53404-148">Пакетное задание в Supply Chain Management запускается автоматически для обработки всех регистраций, полученных из рабочих нагрузок.</span><span class="sxs-lookup"><span data-stu-id="53404-148">A batch job in Supply Chain Management runs automatically to process all the registrations that have been received from the workloads.</span></span> <span data-ttu-id="53404-149">Это задание создает необходимые производственные журналы и записи регистрационного журнала, когда регистрация обрабатывается для завершенного задания в рабочей нагрузке.</span><span class="sxs-lookup"><span data-stu-id="53404-149">This job creates the required production journals and logbook entries when a registration is processed for a completed job on the workload.</span></span>

<span data-ttu-id="53404-150">Хотя задание обычно запускается автоматически, его можно запускать вручную в любое время, войдя в концентратор и перейдя в раздел **Управление производством \> Периодические задачи \> Управление рабочей нагрузкой бэк-офиса \> Обработка регистраций сырья**.</span><span class="sxs-lookup"><span data-stu-id="53404-150">Although the job usually runs automatically, you can run it manually at any time by signing in to the hub and going to **Production control \> Periodic tasks \> Backoffice workload management \> Process raw registrations**.</span></span>

### <a name="check-the-raw-registration-processing-log"></a><span data-ttu-id="53404-151">Проверка журнала обработки регистраций сырья</span><span class="sxs-lookup"><span data-stu-id="53404-151">Check the raw registration processing log</span></span>

<span data-ttu-id="53404-152">Чтобы просмотреть журнал обработки регистрации, выполните вход на концентратор и перейдите в раздел **Управление производством \> Периодические задачи \> Управление рабочей нагрузкой бэк-офиса \> Журнал обработки регистраций сырья**.</span><span class="sxs-lookup"><span data-stu-id="53404-152">To review the registration processing log, sign in to the hub, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Raw registration processing log**.</span></span> <span data-ttu-id="53404-153">Страница **Журнал обработки регистраций сырья** содержит список обработанных регистраций сырья и статус каждой регистрации.</span><span class="sxs-lookup"><span data-stu-id="53404-153">The **Raw registration processing log** page shows a list of processed raw registrations and the status of each registration.</span></span>

<span data-ttu-id="53404-154">![Страница журнала обработки регистраций сырья](media/mes-processing-log.png "Страница журнала обработки регистраций сырья")</span><span class="sxs-lookup"><span data-stu-id="53404-154">![Raw registration processing log page](media/mes-processing-log.png "Raw registration processing log page")</span></span>

<span data-ttu-id="53404-155">Можно работать с любой регистрацией в списке, выбрав ее, затем выбрав одну из следующих кнопок на панели операций:</span><span class="sxs-lookup"><span data-stu-id="53404-155">You can work on any registration in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="53404-156">**Обработать** — обработка выбранной регистрации вручную.</span><span class="sxs-lookup"><span data-stu-id="53404-156">**Process** – Manually process the selected registration.</span></span> <span data-ttu-id="53404-157">Это действие может быть полезным, если задание _Обработка регистраций сырья_ не было выполнено или завершилось сбоем.</span><span class="sxs-lookup"><span data-stu-id="53404-157">This action can be useful if the _Process raw registrations_ job hasn't run, or if it failed.</span></span>
- <span data-ttu-id="53404-158">**Отмена** — отмена выбранной регистрации.</span><span class="sxs-lookup"><span data-stu-id="53404-158">**Cancel** – Cancel the selected registration.</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a><span data-ttu-id="53404-159">Работа с рабочими нагрузками управления производством в единице масштабирования</span><span class="sxs-lookup"><span data-stu-id="53404-159">Working with manufacturing execution workloads on a scale unit</span></span>

<span data-ttu-id="53404-160">Обычно процессы, необходимые для запуска рабочих нагрузок в модуле управления производством, запускаются автоматически для обеспечения синхронизации концентратора и всех единиц масштабирования в соответствии с требованиями.</span><span class="sxs-lookup"><span data-stu-id="53404-160">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="53404-161">Однако при возникновении проблем можно просмотреть историю заказов, которые были обработаны в единицах масштабирования, или вручную выполнить задание _Процессор сообщений из концентратора производства в единицы масштабирования_.</span><span class="sxs-lookup"><span data-stu-id="53404-161">However, if you're having trouble, you can check the history of orders that have been processed on a scale unit or manually run the _Manufacturing hub to scale unit message processor_ job.</span></span>

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a><span data-ttu-id="53404-162">Просмотр истории производственных заданий, обработанных в единице масштабирования</span><span class="sxs-lookup"><span data-stu-id="53404-162">View the history of manufacturing jobs that have been processed on a scale unit</span></span>

<span data-ttu-id="53404-163">Чтобы просмотреть историю производственных заданий, которые были обработаны в единицах масштабирования, выполните вход на компьютер единицы масштабирования и перейдите на страницу **Управление производством \> Периодические задания \> Управление рабочей нагрузкой бэк-офиса \> История обработки производственных заданий**.</span><span class="sxs-lookup"><span data-stu-id="53404-163">To review the history of manufacturing jobs that have been processed on a scale unit, sign in to the scale unit machine, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing jobs processing history**.</span></span> <span data-ttu-id="53404-164">Страница **История обработки производственных заданий** показывает историю обработки производственных заказов в единицах масштабирования.</span><span class="sxs-lookup"><span data-stu-id="53404-164">The **Manufacturing jobs processing history** page shows the processing history of the production orders on the scale unit.</span></span> <span data-ttu-id="53404-165">Можно работать с любым производственным заказом в списке, выбрав его, затем выбрав одну из следующих кнопок на панели операций:</span><span class="sxs-lookup"><span data-stu-id="53404-165">You can work on any production order in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="53404-166">**Обработать** — обработка выбранного производственного заказа вручную.</span><span class="sxs-lookup"><span data-stu-id="53404-166">**Process** – Manually process the selected production order.</span></span>
- <span data-ttu-id="53404-167">**Отмена** — отмена выбранного производственного заказа.</span><span class="sxs-lookup"><span data-stu-id="53404-167">**Cancel** – Cancel the selected production order.</span></span>

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a><span data-ttu-id="53404-168">Задание обработчика сообщений из концентратора в единицы масштабирования</span><span class="sxs-lookup"><span data-stu-id="53404-168">Manufacturing hub to scale unit message processor job</span></span>

<span data-ttu-id="53404-169">Задание _Обработчик сообщений от концентратора в единицы масштабирования_ обрабатывает данные с концентратора в единицы масштабирования.</span><span class="sxs-lookup"><span data-stu-id="53404-169">The _Manufacturing hub to scale unit message processor_ job processes data from the hub to the scale unit.</span></span> <span data-ttu-id="53404-170">Это задание автоматически запускается, когда выполняется развертывание рабочей нагрузки для выполнения производственного процесса.</span><span class="sxs-lookup"><span data-stu-id="53404-170">This job is automatically started when the manufacturing execution workload is deployed.</span></span> <span data-ttu-id="53404-171">Однако его можно выполнить вручную в любое время, перейдя на страницу **Управление производством \> Периодические задачи \> Управление рабочей нагрузкой бэк-офиса \> Обработчик сообщений из концентратора в единицы масштабирования**.</span><span class="sxs-lookup"><span data-stu-id="53404-171">However, you can run it manually at any time by going to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing hub to scale unit message processor**.</span></span>

<a name="RAF"></a>

## <a name="report-as-finished-and-putaway-on-a-scale-unit"></a><span data-ttu-id="53404-172">Приемка и размещение в единице масштабирования</span><span class="sxs-lookup"><span data-stu-id="53404-172">Report as finished and putaway on a scale unit</span></span>

<!-- KFM: 
This section describes how to enable the abilities to report as finished and then putaway finished items when you are using to a scale unit.

### Enable and use report as finished and putaway on a scale unit -->

<span data-ttu-id="53404-173">В текущем выпуске операции приемки и размещения (для готовых продуктов, сопутствующих продуктов и побочных продуктов) поддерживаются [рабочей нагрузкой выполнения склада](cloud-edge-workload-warehousing.md) (не рабочей нагрузкой производства).</span><span class="sxs-lookup"><span data-stu-id="53404-173">In the current release, report as finished and putaway operations (for finished products, co-products, and by-products) are supported by the [warehouse execution workload](cloud-edge-workload-warehousing.md) (not the manufacturing execution workload).</span></span> <span data-ttu-id="53404-174">Таким образом, чтобы использовать эту функцию при соединении с единицей масштабирования, необходимо выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="53404-174">Therefore, to use this functionality when connected to a scale unit, you must do the following:</span></span>

- <span data-ttu-id="53404-175">Установите рабочую нагрузку выполнения склада и рабочую нагрузку выполнения производства в единице масштабирования.</span><span class="sxs-lookup"><span data-stu-id="53404-175">Install both the warehouse execution workload and the manufacturing execution workload on your scale unit.</span></span>
- <span data-ttu-id="53404-176">Используйте мобильное приложение Warehouse Management для приемки и обработки работы размещения.</span><span class="sxs-lookup"><span data-stu-id="53404-176">Use the Warehouse Management mobile app to report as finished and process the putaway work.</span></span> <span data-ttu-id="53404-177">Интерфейс выполнения производственного цеха в настоящее время не поддерживает эти процессы.</span><span class="sxs-lookup"><span data-stu-id="53404-177">The production floor execution interface does not currently support these processes.</span></span>

<!-- KFM: API details needed

### Customize report as finished and putaway functionality

 -->

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
