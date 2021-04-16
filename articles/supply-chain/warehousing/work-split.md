---
title: Разделение работ
description: В этом разделе приводятся сведения о функции разделения работ. Эти функции позволяют разделять крупные заказы на работу на несколько меньших заказов на работу, которые затем можно назначить нескольким складским сотрудникам. Таким образом, одна и та же работа может быть скомплектована сразу нескольким складским работникам.
author: mirzaab
ms.date: 10/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: WHSWorkTableListPage
ms.author: mirzaab
ms.search.validFrom: 2020-10-15
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: eae1e722a7c4d819cbca398eb14a2b36fa04eec5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830770"
---
# <a name="work-split"></a><span data-ttu-id="b032c-105">Разделение работ</span><span class="sxs-lookup"><span data-stu-id="b032c-105">Work split</span></span>

<span data-ttu-id="b032c-106">Функция разделения работ позволяют разделять коды крупных работ (т. е., заказы на работу, содержащие несколько строк) на несколько кодов меньших работ, которые затем можно назначить нескольким складским сотрудникам.</span><span class="sxs-lookup"><span data-stu-id="b032c-106">Work split functionality lets you split large work IDs (that is, work orders that have several lines) into several smaller work IDs that you can then assign to multiple warehouse workers.</span></span> <span data-ttu-id="b032c-107">Таким образом, один и тот же номер создания работы может быть скомплектован сразу нескольким складским работникам.</span><span class="sxs-lookup"><span data-stu-id="b032c-107">In this way, the same work creation number can be picked simultaneously by several warehouse workers.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b032c-108">Можно разбить только те заказы на работу, которые имеют статус *Открыто* или *В обработке*.</span><span class="sxs-lookup"><span data-stu-id="b032c-108">You can split only work orders that have a status of *Open* or *In-progress*.</span></span>

## <a name="turn-on-the-work-split-functionality"></a><span data-ttu-id="b032c-109">Включение функции разделения работ</span><span class="sxs-lookup"><span data-stu-id="b032c-109">Turn on the work split functionality</span></span>

<span data-ttu-id="b032c-110">Прежде чем можно будет использовать функцию разделения работ, необходимо включить эту функцию и ее обязательные функции в системе.</span><span class="sxs-lookup"><span data-stu-id="b032c-110">Before you can use the work split functionality, you must turn on the feature and its prerequisite feature in your system.</span></span> <span data-ttu-id="b032c-111">Администраторы могут использовать параметры [управления компонентами](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса функций и их включения, если это требуется.</span><span class="sxs-lookup"><span data-stu-id="b032c-111">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on as required.</span></span>

<span data-ttu-id="b032c-112">Прежде всего включите требуемую функцию *Блокирование работы на уровне организации*, если она еще не включена.</span><span class="sxs-lookup"><span data-stu-id="b032c-112">First, turn on the prerequisite *Organization-wide work blocking* feature if it isn't already turned on.</span></span> <span data-ttu-id="b032c-113">В рабочей области **Управление функциями** эта функция перечисляется следующими способами:</span><span class="sxs-lookup"><span data-stu-id="b032c-113">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="b032c-114">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="b032c-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="b032c-115">**Имя функции:** *Блокировка работ для всей организации*</span><span class="sxs-lookup"><span data-stu-id="b032c-115">**Feature name:** *Organization-wide work blocking*</span></span>

> [!NOTE]
> <span data-ttu-id="b032c-116">Когда эта функция активирована, обновление данных применяется автоматически после включения функции для всех юридических лиц.</span><span class="sxs-lookup"><span data-stu-id="b032c-116">When this feature is activated, a data upgrade is automatically applied after the feature is turned on across all legal entities.</span></span>

<span data-ttu-id="b032c-117">Затем включите функцию *Разделение работ*, которая указана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b032c-117">Next, turn on the *Work split* feature, which is listed in the following way:</span></span>

- <span data-ttu-id="b032c-118">**Модуль:** *Управление складом*</span><span class="sxs-lookup"><span data-stu-id="b032c-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="b032c-119">**Имя функции:** *Разделение работ*</span><span class="sxs-lookup"><span data-stu-id="b032c-119">**Feature name:** *Work split*</span></span>

## <a name="enhancements-to-the-work-details-and-all-work-pages"></a><span data-ttu-id="b032c-120">Улучшения страниц сведений о работе и всех работ</span><span class="sxs-lookup"><span data-stu-id="b032c-120">Enhancements to the Work details and All work pages</span></span>

<span data-ttu-id="b032c-121">Функция *Разделение работ* добавляет следующие две кнопки на вкладку **Работы** в области действий страниц **Сведения о работе** и **Вся работа**:</span><span class="sxs-lookup"><span data-stu-id="b032c-121">The *Work split* feature adds the following two buttons to the **Work** tab on the Action Pane of the **Work details** and **All work** pages:</span></span>

- <span data-ttu-id="b032c-122">**Разделить работу** — разделение кода текущей работы на несколько кодов меньших работ, которые могут обрабатываться разными работниками.</span><span class="sxs-lookup"><span data-stu-id="b032c-122">**Split work** – Split the current work ID into multiple smaller work IDs that can be processed by separate workers.</span></span>
- <span data-ttu-id="b032c-123">**Отменить сеанс разделения работ** — отменяет сеанс разделения работ и делают работу доступной для обработки.</span><span class="sxs-lookup"><span data-stu-id="b032c-123">**Cancel work split session** – Cancel the work split session, and make the work available for processing.</span></span>

<span data-ttu-id="b032c-124">![Кнопки разделения работы и отмена сеанса разделения работы](media/Work_split_buttons.png "Кнопки разделения работы и отмена сеанса разделения работы")</span><span class="sxs-lookup"><span data-stu-id="b032c-124">![Split work and Cancel work split session buttons](media/Work_split_buttons.png "Split work and Cancel work split session buttons")</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b032c-125">Кнопка **Разделить работу** будет недоступна, если выполняется любое из следующих условий:</span><span class="sxs-lookup"><span data-stu-id="b032c-125">The **Split work** button won't be available if any of the following conditions are met:</span></span>
>
> - <span data-ttu-id="b032c-126">Статус работы отличается от *Открыто* или *Выполняется*.</span><span class="sxs-lookup"><span data-stu-id="b032c-126">The work status is something other than *Open* or *In progress*.</span></span>
> - <span data-ttu-id="b032c-127">Код контейнера связан с кодом работы.</span><span class="sxs-lookup"><span data-stu-id="b032c-127">A container ID is associated with the work ID.</span></span> <span data-ttu-id="b032c-128">(Контейнер не может быть систематически разделен, так как для него требуются физические операции.)</span><span class="sxs-lookup"><span data-stu-id="b032c-128">(A container can't be systematically split, because it requires physical actions.)</span></span>
> - <span data-ttu-id="b032c-129">Работа связана с кластером.</span><span class="sxs-lookup"><span data-stu-id="b032c-129">The work is associated with a cluster.</span></span>
> - <span data-ttu-id="b032c-130">Тип заказа на работу не относится к одному из следующих типов:</span><span class="sxs-lookup"><span data-stu-id="b032c-130">The work order type is something other than one of the following types:</span></span>
>
>    - <span data-ttu-id="b032c-131">Заказы на продажу</span><span class="sxs-lookup"><span data-stu-id="b032c-131">Sales orders</span></span>
>    - <span data-ttu-id="b032c-132">Комплектация сырья</span><span class="sxs-lookup"><span data-stu-id="b032c-132">Raw material picking</span></span>
>    - <span data-ttu-id="b032c-133">Выдача на перемещение</span><span class="sxs-lookup"><span data-stu-id="b032c-133">Transfer issue</span></span>
>
> - <span data-ttu-id="b032c-134">Работа в данный момент разделяется другим пользователем.</span><span class="sxs-lookup"><span data-stu-id="b032c-134">The work is currently being split by another user.</span></span> <span data-ttu-id="b032c-135">При попытке открыть страницу разделения для работы, которая уже разделяется другим пользователем, появляется следующее сообщение об ошибке: "Работа с кодом \#\#\#\# в данный момент разделена.</span><span class="sxs-lookup"><span data-stu-id="b032c-135">If you try to open the splitting page for work that is already being split by another user, you receive the following error message: "The work with ID \#\#\#\# is currently being split.</span></span> <span data-ttu-id="b032c-136">Повторите попытку через несколько минут.</span><span class="sxs-lookup"><span data-stu-id="b032c-136">Retry in a few minutes.</span></span> <span data-ttu-id="b032c-137">Если вы продолжаете получать это сообщение, обратитесь к супервизору."</span><span class="sxs-lookup"><span data-stu-id="b032c-137">If you continue to receive this message, contact a supervisor."</span></span>

<span data-ttu-id="b032c-138">Новая причина блокировки работы, *Разделение работы*, указывает, когда код работы находится в процессе разделения.</span><span class="sxs-lookup"><span data-stu-id="b032c-138">A new work blocking reason, *Split work*, indicates when the work ID is in the process of being split.</span></span> <span data-ttu-id="b032c-139">Это отображается на странице **Разделение работы** и в мобильном приложении управления складом, если пользователь пытается выполнить работу.</span><span class="sxs-lookup"><span data-stu-id="b032c-139">It's shown both on the **Split work** page and in the Warehouse Management mobile app if a user tries to run the work.</span></span> <span data-ttu-id="b032c-140">При использовании причин блокировки имя поля **Заблокированная волна** из кода работы изменяется на **Заблокировано**.</span><span class="sxs-lookup"><span data-stu-id="b032c-140">When blocking reasons are used, the name of the **Blocked wave** field from the work ID is changed to **Blocked**.</span></span>

## <a name="initiate-a-work-split"></a><span data-ttu-id="b032c-141">Инициализация разделения работы</span><span class="sxs-lookup"><span data-stu-id="b032c-141">Initiate a work split</span></span>

<span data-ttu-id="b032c-142">Функция добавляет новую страницу **Разделение работы**, позволяющую пользователям разбивать строки работы из кода работы.</span><span class="sxs-lookup"><span data-stu-id="b032c-142">The feature adds a new **Split work** page that lets users split work lines from the work ID.</span></span> <span data-ttu-id="b032c-143">При первом открытии страницы отображаются строки, имеющие статус работы *Открыто* и доступные для разбиения.</span><span class="sxs-lookup"><span data-stu-id="b032c-143">When the page is first opened, it shows lines that have a work status of *Open* and that are available to be split.</span></span> <span data-ttu-id="b032c-144">На панели операций выберите **Разделить работу**, чтобы обработать выбранную работу.</span><span class="sxs-lookup"><span data-stu-id="b032c-144">On the Action Pane, select **Split work** to process the selected work.</span></span>

<span data-ttu-id="b032c-145">Чтобы разделить работу, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b032c-145">To split work, follow these steps.</span></span>

1. <span data-ttu-id="b032c-146">Откройте одну из следующих страниц работы:</span><span class="sxs-lookup"><span data-stu-id="b032c-146">Open one of the following work pages:</span></span>

    - <span data-ttu-id="b032c-147">**Сведения о работе** (**Управление складом \> Работа \> Сведения о работе**)</span><span class="sxs-lookup"><span data-stu-id="b032c-147">**Work details** (**Warehouse management \> Work \> Work details**)</span></span>
    - <span data-ttu-id="b032c-148">**Вся работа** (**Управление складом \> Работа \> Вся работа**)</span><span class="sxs-lookup"><span data-stu-id="b032c-148">**All work** (**Warehouse management \> Work \> All work**)</span></span>

1. <span data-ttu-id="b032c-149">В сетке выберите код работы, который необходимо разделить.</span><span class="sxs-lookup"><span data-stu-id="b032c-149">In the grid, select a work ID to split.</span></span> <span data-ttu-id="b032c-150">В поле **Тип заказа на работу** должно быть указано одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="b032c-150">The **Work order type** field must be set to one of the following values:</span></span>

    - <span data-ttu-id="b032c-151">Заказы на продажу</span><span class="sxs-lookup"><span data-stu-id="b032c-151">Sales orders</span></span>
    - <span data-ttu-id="b032c-152">Комплектация сырья</span><span class="sxs-lookup"><span data-stu-id="b032c-152">Raw material picking</span></span>
    - <span data-ttu-id="b032c-153">Выдача на перемещение</span><span class="sxs-lookup"><span data-stu-id="b032c-153">Transfer issue</span></span>

1. <span data-ttu-id="b032c-154">В области действий на вкладке **Работа** в группе **Работа** выберите **Разделить работу**.</span><span class="sxs-lookup"><span data-stu-id="b032c-154">On the Action Pane, on the **Work** tab, in the **Work** group, select **Split work**.</span></span>

    <span data-ttu-id="b032c-155">Отображается страница **Разделить работу**, в которой отображаются открытые и доступные для разделения строки работ.</span><span class="sxs-lookup"><span data-stu-id="b032c-155">The **Split work** page appears and shows the work lines that are open and available to be split.</span></span> <span data-ttu-id="b032c-156">По умолчанию отображаются только доступные строки работ.</span><span class="sxs-lookup"><span data-stu-id="b032c-156">By default, only available work lines are shown.</span></span> <span data-ttu-id="b032c-157">Чтобы просмотреть все строки для кода работы (например, строки, имеющих тип работы *Разместить*), установите флажок **Показать все строки** над сеткой.</span><span class="sxs-lookup"><span data-stu-id="b032c-157">To view all lines for the work ID (for example, lines that have a work type of *Put*), select the **Show all lines** check box above the grid.</span></span>

    <span data-ttu-id="b032c-158">Отображается следующее сообщение: "Пользователи не могут обрабатывать строки работы до завершения разделения и закрытия этой страницы."</span><span class="sxs-lookup"><span data-stu-id="b032c-158">The following message is shown: "Users can't process lines of the work until you finish splitting and close this page."</span></span>

    <span data-ttu-id="b032c-159">В поле **Причина блокировки работ** для текущей работы будет установлено значение *Разделить работу*, и работа будет заблокирована.</span><span class="sxs-lookup"><span data-stu-id="b032c-159">The **Work blocking reason** field for the current work will be set to *Split work*, and the work will be blocked.</span></span>

    <span data-ttu-id="b032c-160">![Причина блокировки](media/Blocking_reason.png "Причина блокировки")</span><span class="sxs-lookup"><span data-stu-id="b032c-160">![Blocking reason](media/Blocking_reason.png "Blocking reason")</span></span>

1. <span data-ttu-id="b032c-161">Выберите строки, которые необходимо удалить из текущего кода работы, и добавить к новому коду работы.</span><span class="sxs-lookup"><span data-stu-id="b032c-161">Select the lines to remove from the current work ID and add to a new work ID.</span></span> <span data-ttu-id="b032c-162">Имеют место следующие события:</span><span class="sxs-lookup"><span data-stu-id="b032c-162">The following events occur:</span></span>

    - <span data-ttu-id="b032c-163">При разделении работы выбранная строка или строки исходного кода работы отменяются, а затем копируются в новый код работы.</span><span class="sxs-lookup"><span data-stu-id="b032c-163">When you split the work, the selected line or lines from the original work ID are canceled and then copied to a new work ID.</span></span>
    - <span data-ttu-id="b032c-164">Будет сохранена существующая структура шаблонов работ и местоположение размещения (и также будущие пары комплектации/размещения).</span><span class="sxs-lookup"><span data-stu-id="b032c-164">The existing work template structure and the location of the put (and also future pick/put pairs) are preserved.</span></span> <span data-ttu-id="b032c-165">Значения для следующих полей кода работ копируются из исходной работы в новую работу:</span><span class="sxs-lookup"><span data-stu-id="b032c-165">Values for the following work ID fields are copied from the original work to the new work:</span></span>

        - <span data-ttu-id="b032c-166">Код загрузки</span><span class="sxs-lookup"><span data-stu-id="b032c-166">Load ID</span></span>
        - <span data-ttu-id="b032c-167">Код отгрузки</span><span class="sxs-lookup"><span data-stu-id="b032c-167">Shipment ID</span></span>
        - <span data-ttu-id="b032c-168">Тип заказа на выполнение работ</span><span class="sxs-lookup"><span data-stu-id="b032c-168">Work order type</span></span>
        - <span data-ttu-id="b032c-169">Порядковый номер</span><span class="sxs-lookup"><span data-stu-id="b032c-169">Order number</span></span>
        - <span data-ttu-id="b032c-170">Место</span><span class="sxs-lookup"><span data-stu-id="b032c-170">Site</span></span>
        - <span data-ttu-id="b032c-171">Склад</span><span class="sxs-lookup"><span data-stu-id="b032c-171">Warehouse</span></span>
        - <span data-ttu-id="b032c-172">Приоритет работы</span><span class="sxs-lookup"><span data-stu-id="b032c-172">Work priority</span></span>
        - <span data-ttu-id="b032c-173">Код пула работ</span><span class="sxs-lookup"><span data-stu-id="b032c-173">Work pool ID</span></span>
        - <span data-ttu-id="b032c-174">Код волны</span><span class="sxs-lookup"><span data-stu-id="b032c-174">Wave ID</span></span>
        - <span data-ttu-id="b032c-175">Номер создания работы</span><span class="sxs-lookup"><span data-stu-id="b032c-175">Work creation number</span></span>

    - <span data-ttu-id="b032c-176">Следующие поля не копируются в новый код работы:</span><span class="sxs-lookup"><span data-stu-id="b032c-176">The following fields aren't copied to the new work ID:</span></span>

        - <span data-ttu-id="b032c-177">**Код работы** — новый код работы создается из соответствующей номерной серии.</span><span class="sxs-lookup"><span data-stu-id="b032c-177">**Work ID** – A new work ID is generated from the appropriate number sequence.</span></span>
        - <span data-ttu-id="b032c-178">**Статус работы** — для этого поля установлено значение *Открыто*.</span><span class="sxs-lookup"><span data-stu-id="b032c-178">**Work status** – This field is set to *Open*.</span></span>
        - <span data-ttu-id="b032c-179">**Заблокировано** — для этого поля первоначально установлено пустое значение.</span><span class="sxs-lookup"><span data-stu-id="b032c-179">**Locked by** – This field is initially set to blank.</span></span>
        - <span data-ttu-id="b032c-180">**Код целевого грузоместа** — это поле остается пустым.</span><span class="sxs-lookup"><span data-stu-id="b032c-180">**Target license plate ID** – This field is left blank.</span></span>
        - <span data-ttu-id="b032c-181">**Дата и время создания** — в этом поле задается текущая дата и время.</span><span class="sxs-lookup"><span data-stu-id="b032c-181">**Created date and time** – This field is set to the current date and time.</span></span>
        - <span data-ttu-id="b032c-182">**Заблокированная волна/заморожено** — это поле пересчитывается для исходного кода работы и нового кода работы.</span><span class="sxs-lookup"><span data-stu-id="b032c-182">**Blocked wave/frozen** – This field is recomputed for the original work ID and the new work ID.</span></span>

1. <span data-ttu-id="b032c-183">В панели операций выберите **Разделить работу**.</span><span class="sxs-lookup"><span data-stu-id="b032c-183">On the Action Pane, select **Split work**.</span></span>

<span data-ttu-id="b032c-184">В процессе разделения работы отображается следующее сообщение: "Обработка операции — разделение работы".</span><span class="sxs-lookup"><span data-stu-id="b032c-184">While the work is being split, the following message is shown: "Processing operation - Split work".</span></span> <span data-ttu-id="b032c-185">Пока это сообщение отображается, можно отменить операцию, выбрав **Отмена** в окне сообщения.</span><span class="sxs-lookup"><span data-stu-id="b032c-185">While this message is visible, you can cancel the operation by selecting **Cancel** in the message box.</span></span>

<span data-ttu-id="b032c-186">Если флажок **Показать все строки** снят, строка, которая была разбита и отменена, больше не будет отображаться в сетке.</span><span class="sxs-lookup"><span data-stu-id="b032c-186">If the **Show all lines** check box is cleared, the line that was split off and canceled will no longer appear in the grid.</span></span> <span data-ttu-id="b032c-187">Если установлен флажок, вы должны увидеть, что значение поля **Статус работы** для этой строки изменилось на *Отменено*.</span><span class="sxs-lookup"><span data-stu-id="b032c-187">If the check box is selected, you should see that the value of the **Work status** field for that line has changed to *Canceled*.</span></span>

<span data-ttu-id="b032c-188">Отображается следующее уведомление, указывающее на то, что новый код работы был создан: "Работа \#\#\#\# была создана путем разделения из исходной работы \#\#\#\#."</span><span class="sxs-lookup"><span data-stu-id="b032c-188">The following notification is shown to indicate that the new work ID has been created: "Work \#\#\#\# has been created by splitting off from original work \#\#\#\#."</span></span>

<span data-ttu-id="b032c-189">Другие строки работы из исходного кода работы (например, строки *Разместить*) будут скорректированы по мере необходимости для отображения строк отмененной работы.</span><span class="sxs-lookup"><span data-stu-id="b032c-189">Other work lines from the original work ID (such as *Put* lines) will be adjusted as required to reflect the lines of work that have been canceled.</span></span> <span data-ttu-id="b032c-190">Например, если у исходного кода работы имелась строка *Разместить* для количества 15, а строки *Комплектация* с общим количеством 10 были отменены, новое количество *Разместить* в исходном коде работы теперь будет иметь значение 5.</span><span class="sxs-lookup"><span data-stu-id="b032c-190">For example, if the original work ID had a *Put* line for a quantity of 15, and *Pick* lines that have a total quantity of 10 were canceled, the new *Put* quantity on the original work ID will now be 5.</span></span>

<span data-ttu-id="b032c-191">Новая работа не будет сразу назначена никакому пользователю.</span><span class="sxs-lookup"><span data-stu-id="b032c-191">The new work won't immediately be assigned to any user.</span></span> <span data-ttu-id="b032c-192">Однако при необходимости теперь можно назначить ее пользователю, используя стандартную функциональность страницы **Сведения о работе**.</span><span class="sxs-lookup"><span data-stu-id="b032c-192">However, you can assign it to a user now, as required, by using the standard functionality of the **Work details** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b032c-193">Можно разбить только коды работ, содержащие две или более доступных строк работы.</span><span class="sxs-lookup"><span data-stu-id="b032c-193">You can split only work IDs that contain two or more available work lines.</span></span> <span data-ttu-id="b032c-194">Если выбрать **Разделить работу**, когда имеется только одна строка работы, будет выведено следующее сообщение об ошибке: "По крайней мере одна строка работы должна оставаться в исходной работе."</span><span class="sxs-lookup"><span data-stu-id="b032c-194">If you select **Split work** when there is only one work line, you will receive the following error message: "At least one work line must remain on initial work."</span></span> <span data-ttu-id="b032c-195">В этом случае разбиение производиться не будет.</span><span class="sxs-lookup"><span data-stu-id="b032c-195">In this case, no splitting will occur.</span></span>

## <a name="finish-a-work-split"></a><span data-ttu-id="b032c-196">Завершение разделения работы</span><span class="sxs-lookup"><span data-stu-id="b032c-196">Finish a work split</span></span>

<span data-ttu-id="b032c-197">Для завершения разделения работы должна быть удалена причина блокировки *Разделить работу*.</span><span class="sxs-lookup"><span data-stu-id="b032c-197">To finish splitting work, the *Split work* blocking reason must be removed.</span></span> <span data-ttu-id="b032c-198">Существует два способа выполнения этого шага:</span><span class="sxs-lookup"><span data-stu-id="b032c-198">There are two ways to complete this step:</span></span>

- <span data-ttu-id="b032c-199">Пользователь, выполняющий разбиение работы, закрывает страницу **Разделить работу**, выбирая кнопку **Закрыть** (**X**) в верхнем правом углу.</span><span class="sxs-lookup"><span data-stu-id="b032c-199">The user who is splitting the work closes the **Split work** page by selecting the **Close** button (**X**) in the upper-right corner.</span></span> <span data-ttu-id="b032c-200">При закрытии страницы причина блокировки *Разделение работы* будет удалена.</span><span class="sxs-lookup"><span data-stu-id="b032c-200">When the page is closed, the *Split Work* blocking reason will be removed.</span></span> <span data-ttu-id="b032c-201">Состояние *Заблокировано* этой работы будет пересчитано, и, если для этой работы нет оставшихся причин блокировки, работа будет разблокирована.</span><span class="sxs-lookup"><span data-stu-id="b032c-201">The *Blocked* state of this work will be recomputed and, if there are no remaining blocking reasons for this work, the work will be unblocked.</span></span>
- <span data-ttu-id="b032c-202">Любой пользователь открывает код работы и выбирает кнопку **Отмена сеанса разделения работы** на панели операций.</span><span class="sxs-lookup"><span data-stu-id="b032c-202">Any user opens the work ID and selects the **Cancel work split session** button on the Action Pane.</span></span> <span data-ttu-id="b032c-203">Причина блокировки *Разделение работы* будет удалена, и состояние *Заблокировано* этой работы будет пересчитано, точно так же, как и при закрытии страницы **Разделить работу**.</span><span class="sxs-lookup"><span data-stu-id="b032c-203">The *Split work* blocking reason will be removed, and the *Blocked* state of this work will be recomputed, just as when the **Split work** page is closed.</span></span>

<span data-ttu-id="b032c-204">После удаления причины блокирования *Разделение работы* можно выполнить работу на мобильном устройстве, при условии, что состояние **Заблокировано** установлено на значение *Нет* в коде работы.</span><span class="sxs-lookup"><span data-stu-id="b032c-204">After the *Split work* blocking reason is removed, the work can be run on the mobile device, provided that the **Blocked** state is set to *No* on the work ID.</span></span>

## <a name="user-blocking-on-the-warehouse-management-mobile-app"></a><span data-ttu-id="b032c-205">Блокировка пользователей в мобильном приложении управления складом</span><span class="sxs-lookup"><span data-stu-id="b032c-205">User blocking on the Warehouse Management mobile app</span></span>

<span data-ttu-id="b032c-206">При попытке использовать мобильное приложение управления складом для выполнения работы комплектации по коду работы, которая была разделена, вы получите следующее сообщение об ошибке: "Работа с кодом \#\#\#\# в данный момент разделена."</span><span class="sxs-lookup"><span data-stu-id="b032c-206">If you try to use the Warehouse Management mobile app to run picking work against a work ID that is being split, you will receive the following error message: "The work with ID \#\#\#\# is currently being split."</span></span> <span data-ttu-id="b032c-207">Если получено это сообщение, выберите **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="b032c-207">If you receive this message, select **Cancel**.</span></span> <span data-ttu-id="b032c-208">После этого можно продолжить обработку другой работы.</span><span class="sxs-lookup"><span data-stu-id="b032c-208">You can then continue to process other work.</span></span>

## <a name="other-blocked-operations"></a><span data-ttu-id="b032c-209">Другие заблокированные операции</span><span class="sxs-lookup"><span data-stu-id="b032c-209">Other blocked operations</span></span>

<span data-ttu-id="b032c-210">Любые операции, которые изменяют строки работы, проводки по запасам работы или ссылки пополнения, которые связаны с разделяемой работой, не будут работать, и будет показано следующее сообщение об ошибке: "Работа с кодом \#\#\#\# в данный момент разделена."</span><span class="sxs-lookup"><span data-stu-id="b032c-210">Any operations that modify work lines, work inventory transactions, or replenishment links that are related to work that is being split will fail, and the following error message will be shown: "The work with ID \#\#\#\# is currently being split."</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]