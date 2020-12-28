---
title: Поддержка доски переноса канбана для сканеров штрих-кодов
description: Доска переноса канбана поддерживает ввод данных сканера из мини-приложения сканера штрих-кодов для выбора операции начала, завершения и очистки задания канбана.
author: ChristianRytt
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1bd6f1bdd847f74cee7d3594d19b72454063c0cb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4436265"
---
# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="5a8a4-103">Поддержка доски переноса канбана для сканеров штрих-кодов</span><span class="sxs-lookup"><span data-stu-id="5a8a4-103">Kanban transfer board support for barcode scanners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a8a4-104">Доска переноса канбана поддерживает ввод данных сканера из мини-приложения сканера штрих-кодов для выбора операции начала, завершения и очистки задания канбана.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="5a8a4-105">Режимы регистрации</span><span class="sxs-lookup"><span data-stu-id="5a8a4-105">Registration modes</span></span>
------------------

<span data-ttu-id="5a8a4-106">На экспресс-вкладке **Регистрация сканера** вы можете выбрать режим регистрации, который контролирует действие, когда вы сканируете номер карты канбана или вручную вводите номер в поле "Номер карты канбана".</span><span class="sxs-lookup"><span data-stu-id="5a8a4-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>

| <span data-ttu-id="5a8a4-107">Задать режим регистрации</span><span class="sxs-lookup"><span data-stu-id="5a8a4-107">Set registration mode</span></span> | <span data-ttu-id="5a8a4-108">Описание</span><span class="sxs-lookup"><span data-stu-id="5a8a4-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a8a4-109">Начать</span><span class="sxs-lookup"><span data-stu-id="5a8a4-109">Start</span></span>                 | <span data-ttu-id="5a8a4-110">Регистрация задания переноса канбана как находящегося в обработке.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="5a8a4-111">Выполнено</span><span class="sxs-lookup"><span data-stu-id="5a8a4-111">Complete</span></span>              | <span data-ttu-id="5a8a4-112">Регистрация задания переноса канбана как завершенного.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="5a8a4-113">Пусто</span><span class="sxs-lookup"><span data-stu-id="5a8a4-113">Empty</span></span>                 | <span data-ttu-id="5a8a4-114">Регистрация единицы обработки материалов, на которую ссылается карта канбана, как пустой.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="5a8a4-115">Выбрать</span><span class="sxs-lookup"><span data-stu-id="5a8a4-115">Select</span></span>                | <span data-ttu-id="5a8a4-116">Регистрация номера карты канбана и автоматический выбор задания по ссылке в списке канбана.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<span data-ttu-id="5a8a4-117">Выбор режима регистрации</span><span class="sxs-lookup"><span data-stu-id="5a8a4-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="5a8a4-118">При использовании считывателя штрих-кода для выбора задания, режим отображения доски канбан меняется.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span><span data-ttu-id="5a8a4-119"> В этом режиме действуют следующие условия:</span><span class="sxs-lookup"><span data-stu-id="5a8a4-119"> In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="5a8a4-120">Отображается только отсканированное задание канбан.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="5a8a4-121">Подробные сведения о выбранном задании отображаются на экспресс-вкладке **Сведения**.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="5a8a4-122">На экспресс-вкладке **Сообщения** отображаются только сообщения для выбранного задания.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="5a8a4-123">Можно изменить статус задания с помощью функций, доступных в Панель операций.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="5a8a4-124">Доска переноса канбана продолжает показывать только одно задание в течение этого периода.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="5a8a4-125">Можно обновить сведения в списке заданий вручную, щелкнув **Обновить** (Shift+F5) на панели операций.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="5a8a4-126">После обновления сведений общие результаты для фильтра задания отображаются еще раз.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="5a8a4-127">Статус задания и возможные действия</span><span class="sxs-lookup"><span data-stu-id="5a8a4-127">Job status and possible actions</span></span>
<span data-ttu-id="5a8a4-128">Статус выбранного задания и статус всех прикрепленных заданий для событий канбана определяют, можно ли обрабатывать задание далее.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="5a8a4-129">В следующей таблице представлены сведения об этих статусах и задачах:</span><span class="sxs-lookup"><span data-stu-id="5a8a4-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="5a8a4-130">Статусы, которые доступны для заданий или для единиц обработки, на которые ссылаются эти задания.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="5a8a4-131">Каждая задача, которую можно выполнить для задания.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-131">Each task that you can perform for the job.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5a8a4-132">Тип задания</span><span class="sxs-lookup"><span data-stu-id="5a8a4-132">Job type</span></span></th>
<th><span data-ttu-id="5a8a4-133">Статус задания или состояние обработки единицы</span><span class="sxs-lookup"><span data-stu-id="5a8a4-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="5a8a4-134">Обновление отгрузочной накладной</span><span class="sxs-lookup"><span data-stu-id="5a8a4-134">Update picking list</span></span></th>
<th><span data-ttu-id="5a8a4-135">Начать</span><span class="sxs-lookup"><span data-stu-id="5a8a4-135">Start</span></span></th>
<th><span data-ttu-id="5a8a4-136">Обновить регистрацию</span><span class="sxs-lookup"><span data-stu-id="5a8a4-136">Update registration</span></span></th>
<th><span data-ttu-id="5a8a4-137">Выполнено</span><span class="sxs-lookup"><span data-stu-id="5a8a4-137">Complete</span></span></th>
<th><span data-ttu-id="5a8a4-138">Пусто</span><span class="sxs-lookup"><span data-stu-id="5a8a4-138">Empty</span></span></th>
<th><span data-ttu-id="5a8a4-139">Создать канбаны событий</span><span class="sxs-lookup"><span data-stu-id="5a8a4-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5a8a4-140">Перевод данных</span><span class="sxs-lookup"><span data-stu-id="5a8a4-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="5a8a4-141">Не запланировано</span><span class="sxs-lookup"><span data-stu-id="5a8a4-141">Not planned</span></span></li>
<li><span data-ttu-id="5a8a4-142">Нет прикрепленных заданий или прикрепленные задания имеют статус "Завершено"</span><span class="sxs-lookup"><span data-stu-id="5a8a4-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="5a8a4-143">Да</span><span class="sxs-lookup"><span data-stu-id="5a8a4-143">Yes</span></span></td>
<td><span data-ttu-id="5a8a4-144">Да</span><span class="sxs-lookup"><span data-stu-id="5a8a4-144">Yes</span></span></td>
<td><span data-ttu-id="5a8a4-145">Да</span><span class="sxs-lookup"><span data-stu-id="5a8a4-145">Yes</span></span></td>
<td><span data-ttu-id="5a8a4-146">Да</span><span class="sxs-lookup"><span data-stu-id="5a8a4-146">Yes</span></span></td>
<td><span data-ttu-id="5a8a4-147">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-147">No</span></span></td>
<td><span data-ttu-id="5a8a4-148">Да</span><span class="sxs-lookup"><span data-stu-id="5a8a4-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a8a4-149">Перевод данных</span><span class="sxs-lookup"><span data-stu-id="5a8a4-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="5a8a4-150">Не запланировано</span><span class="sxs-lookup"><span data-stu-id="5a8a4-150">Not planned</span></span></li>
<li><span data-ttu-id="5a8a4-151">Прикрепленное задание — не "Завершено"</span><span class="sxs-lookup"><span data-stu-id="5a8a4-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="5a8a4-152">Да</span><span class="sxs-lookup"><span data-stu-id="5a8a4-152">Yes</span></span></td>
<td><span data-ttu-id="5a8a4-153">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-153">No</span></span></td>
<td><span data-ttu-id="5a8a4-154">Да</span><span class="sxs-lookup"><span data-stu-id="5a8a4-154">Yes</span></span></td>
<td><span data-ttu-id="5a8a4-155">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-155">No</span></span></td>
<td><span data-ttu-id="5a8a4-156">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-156">No</span></span></td>
<td><span data-ttu-id="5a8a4-157">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a8a4-158">Перевод данных</span><span class="sxs-lookup"><span data-stu-id="5a8a4-158">Transfer</span></span></td>
<td><span data-ttu-id="5a8a4-159">В обработке</span><span class="sxs-lookup"><span data-stu-id="5a8a4-159">In progress</span></span></td>
<td><span data-ttu-id="5a8a4-160">Да</span><span class="sxs-lookup"><span data-stu-id="5a8a4-160">Yes</span></span></td>
<td><span data-ttu-id="5a8a4-161">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-161">No</span></span></td>
<td><span data-ttu-id="5a8a4-162">Да</span><span class="sxs-lookup"><span data-stu-id="5a8a4-162">Yes</span></span></td>
<td><span data-ttu-id="5a8a4-163">Да</span><span class="sxs-lookup"><span data-stu-id="5a8a4-163">Yes</span></span></td>
<td><span data-ttu-id="5a8a4-164">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-164">No</span></span></td>
<td><span data-ttu-id="5a8a4-165">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a8a4-166">Перевод данных</span><span class="sxs-lookup"><span data-stu-id="5a8a4-166">Transfer</span></span></td>
<td><span data-ttu-id="5a8a4-167">Завершено</span><span class="sxs-lookup"><span data-stu-id="5a8a4-167">Completed</span></span></td>
<td><span data-ttu-id="5a8a4-168">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-168">No</span></span></td>
<td><span data-ttu-id="5a8a4-169">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-169">No</span></span></td>
<td><span data-ttu-id="5a8a4-170">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-170">No</span></span></td>
<td><span data-ttu-id="5a8a4-171">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-171">No</span></span></td>
<td><span data-ttu-id="5a8a4-172">Да</span><span class="sxs-lookup"><span data-stu-id="5a8a4-172">Yes</span></span></td>
<td><span data-ttu-id="5a8a4-173">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a8a4-174">Перенос или обработка</span><span class="sxs-lookup"><span data-stu-id="5a8a4-174">Transfer or process</span></span></td>
<td><span data-ttu-id="5a8a4-175">Пусто</span><span class="sxs-lookup"><span data-stu-id="5a8a4-175">Empty</span></span></td>
<td><span data-ttu-id="5a8a4-176">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-176">No</span></span></td>
<td><span data-ttu-id="5a8a4-177">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-177">No</span></span></td>
<td><span data-ttu-id="5a8a4-178">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-178">No</span></span></td>
<td><span data-ttu-id="5a8a4-179">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-179">No</span></span></td>
<td><span data-ttu-id="5a8a4-180">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-180">No</span></span></td>
<td><span data-ttu-id="5a8a4-181">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a8a4-182">Перенос или обработка</span><span class="sxs-lookup"><span data-stu-id="5a8a4-182">Transfer or process</span></span></td>
<td><span data-ttu-id="5a8a4-183">Карта канбана не найдена</span><span class="sxs-lookup"><span data-stu-id="5a8a4-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="5a8a4-184">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-184">No</span></span></td>
<td><span data-ttu-id="5a8a4-185">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-185">No</span></span></td>
<td><span data-ttu-id="5a8a4-186">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-186">No</span></span></td>
<td><span data-ttu-id="5a8a4-187">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-187">No</span></span></td>
<td><span data-ttu-id="5a8a4-188">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-188">No</span></span></td>
<td><span data-ttu-id="5a8a4-189">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a8a4-190">Перенос или обработка</span><span class="sxs-lookup"><span data-stu-id="5a8a4-190">Transfer or process</span></span></td>
<td><span data-ttu-id="5a8a4-191">Карта канбана найдена, но она не назначена канбану</span><span class="sxs-lookup"><span data-stu-id="5a8a4-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="5a8a4-192">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-192">No</span></span></td>
<td><span data-ttu-id="5a8a4-193">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-193">No</span></span></td>
<td><span data-ttu-id="5a8a4-194">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-194">No</span></span></td>
<td><span data-ttu-id="5a8a4-195">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-195">No</span></span></td>
<td><span data-ttu-id="5a8a4-196">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-196">No</span></span></td>
<td><span data-ttu-id="5a8a4-197">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a8a4-198">Обработать</span><span class="sxs-lookup"><span data-stu-id="5a8a4-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="5a8a4-199">Не запланировано</span><span class="sxs-lookup"><span data-stu-id="5a8a4-199">Not planned</span></span></li>
<li><span data-ttu-id="5a8a4-200">Подготовлено</span><span class="sxs-lookup"><span data-stu-id="5a8a4-200">Prepared</span></span></li>
<li><span data-ttu-id="5a8a4-201">В обработке</span><span class="sxs-lookup"><span data-stu-id="5a8a4-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="5a8a4-202">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-202">No</span></span></td>
<td><span data-ttu-id="5a8a4-203">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-203">No</span></span></td>
<td><span data-ttu-id="5a8a4-204">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-204">No</span></span></td>
<td><span data-ttu-id="5a8a4-205">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-205">No</span></span></td>
<td><span data-ttu-id="5a8a4-206">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-206">No</span></span></td>
<td><span data-ttu-id="5a8a4-207">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a8a4-208">Обработать</span><span class="sxs-lookup"><span data-stu-id="5a8a4-208">Process</span></span></td>
<td><span data-ttu-id="5a8a4-209">Завершено</span><span class="sxs-lookup"><span data-stu-id="5a8a4-209">Completed</span></span></td>
<td><span data-ttu-id="5a8a4-210">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-210">No</span></span></td>
<td><span data-ttu-id="5a8a4-211">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-211">No</span></span></td>
<td><span data-ttu-id="5a8a4-212">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-212">No</span></span></td>
<td><span data-ttu-id="5a8a4-213">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-213">No</span></span></td>
<td><span data-ttu-id="5a8a4-214">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-214">No</span></span></td>
<td><span data-ttu-id="5a8a4-215">Нет</span><span class="sxs-lookup"><span data-stu-id="5a8a4-215">No</span></span></td>
</tr>
</tbody>
</table>





