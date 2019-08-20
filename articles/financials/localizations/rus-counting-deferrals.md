---
title: Инвентаризация РБП (Россия)
description: В этом разделе описывается, как проводится инвентаризация расходов будущих периодов (РБП).
author: anasyash
manager: AnnBe
ms.date: 06/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Russia
ms.author: anasyash
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 025cc19f4451bb93a80dce9ddcc1246ca8d6df98
ms.sourcegitcommit: 4fd51830be21b95a1398dc80d5429a74bcec73fc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2019
ms.locfileid: "1736976"
---
# <a name="deferrals-counting--russia"></a><span data-ttu-id="6cd8b-103">Инвентаризация РБП (Россия)</span><span class="sxs-lookup"><span data-stu-id="6cd8b-103">Deferrals counting  (Russia)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6cd8b-104">Функциональность РБП поддерживает процесс инвентаризации РБП и позволяет печатать отчет **Акт инвентаризации (ИНВ-11)**.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-104">The deferrals functionality supports the process of deferrals counting and lets you print the **Inventory act (INV-11)** report.</span></span>

<span data-ttu-id="6cd8b-105">Перед созданием отчета **Акт инвентаризации (ИНВ-11)** необходимо создать РБП и разнести проводки списания в журнале РБП.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-105">Before you generate the **Inventory act (INV-11)** report, you must create deferrals and post writing-off transactions in the deferrals journal.</span></span>

1. <span data-ttu-id="6cd8b-106">Перейдите к **Главная книга** \> **Периодические задачи** \> **Расходы будущих периодов** \> **Журнал инвентаризации РБП**.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-106">Go to **General ledger** \> **Periodic tasks** \> **Deferrals** \> **Deferrals counting journal**.</span></span>

    <span data-ttu-id="6cd8b-107">Можно использовать страницу **Журнал инвентаризации РБП** для создания журнала инвентаризации РБП и печати отчета **Акт инвентаризации (ИНВ-11)**.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-107">You can use the **Deferrals counting journal** page to create a Deferrals counting journal and print the **Inventory act (INV-11)** report.</span></span>

    <span data-ttu-id="6cd8b-108">В следующей таблице описаны вкладки на странице **Журнал инвентаризации РБП**.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-108">The following table describes the tabs on the **Deferrals counting journal** page.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="6cd8b-109">Вкладка</span><span class="sxs-lookup"><span data-stu-id="6cd8b-109">Tab</span></span></th>
    <th><span data-ttu-id="6cd8b-110">Описание</span><span class="sxs-lookup"><span data-stu-id="6cd8b-110">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="6cd8b-111">Обзор</span><span class="sxs-lookup"><span data-stu-id="6cd8b-111">Overview</span></span></td>
    <td><span data-ttu-id="6cd8b-112">Создать новый журнал инвентаризации РБП.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-112">Create a new Deferrals counting journal.</span></span>
    <p><span data-ttu-id="6cd8b-113"><strong>Примечание:</strong> Вы не можете создать более одного журнала с одинаковой датой инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-113"><strong>Note:</strong> You can't create more than one journal that has the same counting date.</span></span></p>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="6cd8b-114">Должностные лица</span><span class="sxs-lookup"><span data-stu-id="6cd8b-114">Officials</span></span></td>
    <td><span data-ttu-id="6cd8b-115">Укажите имена, должности и звания должностных лиц.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-115">Specify the names, positions, and titles of the officials.</span></span></td>
    </tr>
    </tbody>
    </table>

    <span data-ttu-id="6cd8b-116">В следующей таблице описаны кнопки на панели операций страницы **Журнал инвентаризации РБП**.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-116">The following table describes the buttons on the Action Pane of the **Deferrals counting journal** page.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="6cd8b-117">Кнопка</span><span class="sxs-lookup"><span data-stu-id="6cd8b-117">Button</span></span></th>
    <th><span data-ttu-id="6cd8b-118">Описание</span><span class="sxs-lookup"><span data-stu-id="6cd8b-118">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="6cd8b-119">Линии</span><span class="sxs-lookup"><span data-stu-id="6cd8b-119">Lines</span></span></td>
    <td><span data-ttu-id="6cd8b-120">Откройте страницу <strong>Строка журнала инвентаризации РБП</strong>, где можно создавать строки журналов.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-120">Open the <strong>Deferrals counting journal line</strong> page, where you can create journal lines.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="6cd8b-121">Близкие</span><span class="sxs-lookup"><span data-stu-id="6cd8b-121">Close</span></span></td>
    <td><span data-ttu-id="6cd8b-122">Откройте диалоговое окно <strong>Завершить инвентаризацию РБП</strong>.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-122">Open the <strong>End deferrals counting</strong> dialog box.</span></span> <span data-ttu-id="6cd8b-123">В поле <strong>Дата окончания инвентаризации</strong> можно ввести дату, когда требуется закрыть журнал.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-123">In the <strong>Counting end date</strong> field, you can then enter the date when you want to close the journal.</span></span> <span data-ttu-id="6cd8b-124">Указанная вами дата отображается в поле <strong>Дата окончания инвентаризации</strong> страницы <strong>Журнал инвентаризации РБП</strong>.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-124">The date that you specify is shown in the <strong>Counting end date</strong> field on the <strong>Deferrals counting journal</strong> page.</span></span>
    <p><span data-ttu-id="6cd8b-125"><strong>Примечание:</strong> Вы не можете закрыть журнал, если строки журнала не созданы.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-125"><strong>Note:</strong> You can't close the journal if journal lines aren't created.</span></span></p>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="6cd8b-126">Печать</span><span class="sxs-lookup"><span data-stu-id="6cd8b-126">Print</span></span></td>
    <td><span data-ttu-id="6cd8b-127">Откройте диалоговое окно <strong>Инвентаризация РБП</strong>, где можно распечатать отчет <strong>Акт инвентаризации (ИНВ-11)</strong>, используя шаблон Microsoft Excel для номера выбранной модели.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-127">Open the <strong>Deferrals counting</strong> dialog box, where you can print the <strong>Inventory act (INV-11)</strong> report by using the Microsoft Excel template for the selected model number.</span></span></td>
    </tr>
    </tbody>
    </table>

    <span data-ttu-id="6cd8b-128">В следующей таблице описаны поля на странице **Журнал инвентаризации РБП**.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-128">The following table describes the fields on the **Deferrals counting journal** page.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="6cd8b-129">Поле</span><span class="sxs-lookup"><span data-stu-id="6cd8b-129">Field</span></span></th>
    <th><span data-ttu-id="6cd8b-130">Описание</span><span class="sxs-lookup"><span data-stu-id="6cd8b-130">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="6cd8b-131">Отображение</span><span class="sxs-lookup"><span data-stu-id="6cd8b-131">Show</span></span></td>
    <td><span data-ttu-id="6cd8b-132">Выберите, какие ваучеры или журналы отображаются на странице, на основе статуса разноски:</span><span class="sxs-lookup"><span data-stu-id="6cd8b-132">Select which vouchers or journals are shown on the page, based on the posting status:</span></span> <ul>
    <li><span data-ttu-id="6cd8b-133"><strong>Все</strong> — показать все журналы.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-133"><strong>All</strong> – Show all journals.</span></span></li>
    <li><span data-ttu-id="6cd8b-134"><strong>Открыто</strong> — Показать только журналы, которые не разнесены.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-134"><strong>Open</strong> – Show only journals that aren't posted.</span></span></li>
    <li><span data-ttu-id="6cd8b-135"><strong>Разнесено</strong> — Показать только журналы, которые разнесены.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-135"><strong>Posted</strong> – Show only journals that are posted.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="6cd8b-136">Номер партии журнала</span><span class="sxs-lookup"><span data-stu-id="6cd8b-136">Journal batch number</span></span></td>
    <td><span data-ttu-id="6cd8b-137">Номер журнала РБП.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-137">The deferral journal number.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="6cd8b-138">Название</span><span class="sxs-lookup"><span data-stu-id="6cd8b-138">Name</span></span></td>
    <td><span data-ttu-id="6cd8b-139">Выберите наименование журнала, которое имеет тип журнала <strong>Расходы будущих периодов</strong>.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-139">Select the journal name that has the <strong>Deferrals</strong> journal type.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="6cd8b-140">Номер распоряжения</span><span class="sxs-lookup"><span data-stu-id="6cd8b-140">Resolution number</span></span></td>
    <td><span data-ttu-id="6cd8b-141">Введите номер разрешения для журнала инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-141">Enter the resolution number for the counting journal.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="6cd8b-142">Дата приказа</span><span class="sxs-lookup"><span data-stu-id="6cd8b-142">Resolution date</span></span></td>
    <td><span data-ttu-id="6cd8b-143">Выберите дату разрешения для журнала инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-143">Select the resolution date for the counting journal.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="6cd8b-144">Дата начала инвентаризации</span><span class="sxs-lookup"><span data-stu-id="6cd8b-144">Counting start date</span></span></td>
    <td><span data-ttu-id="6cd8b-145">Выберите дату начала периода инвентаризации РБП.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-145">Select the start date of the deferrals counting period.</span></span> <span data-ttu-id="6cd8b-146">По умолчанию для этого поля задана текущая дата.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-146">By default, this field is set to the current date.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="6cd8b-147">Дата окончания инвентаризации</span><span class="sxs-lookup"><span data-stu-id="6cd8b-147">Counting end date</span></span></td>
    <td><span data-ttu-id="6cd8b-148">Дата окончания периода инвентаризации РБП.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-148">The end date of the deferrals counting period.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="6cd8b-149">Закрытый</span><span class="sxs-lookup"><span data-stu-id="6cd8b-149">Closed</span></span></td>
    <td><span data-ttu-id="6cd8b-150">Этот флажок автоматически выбирается после завершения инвентаризации РБП и закрытия журнала.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-150">This check box is automatically selected when the deferral counting is completed and the journal is closed.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="6cd8b-151">Занимаемая должность</span><span class="sxs-lookup"><span data-stu-id="6cd8b-151">Position</span></span></td>
    <td><span data-ttu-id="6cd8b-152">Выберите название должности должностного лица.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-152">Select the position title of the official.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="6cd8b-153">Имя сотрудника</span><span class="sxs-lookup"><span data-stu-id="6cd8b-153">Employee name</span></span></td>
    <td><span data-ttu-id="6cd8b-154">Выберите имя должностного лица в списке сотрудников компании.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-154">Select the name of the official in the list of company employees.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="6cd8b-155">Название должности</span><span class="sxs-lookup"><span data-stu-id="6cd8b-155">Title</span></span></td>
    <td><span data-ttu-id="6cd8b-156">Выберите название должности сотрудника.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-156">Select the job title of the employee.</span></span></td>
    </tr>
    </tbody>
    </table>

2. <span data-ttu-id="6cd8b-157">Выполните следующие действия, чтобы создать новый журнал инвентаризации РБП:</span><span class="sxs-lookup"><span data-stu-id="6cd8b-157">To create a new Deferrals counting journal, follow these steps:</span></span>

    1. <span data-ttu-id="6cd8b-158">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-158">On the Action Pane, select **New**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="6cd8b-159">Вы не можете создать более одного журнала инвентаризации РБП с одинаковой датой инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-159">You can't create more than one Deferrals counting journal that has the same counting date.</span></span>

    2. <span data-ttu-id="6cd8b-160">В поле **Имя** выберите наименование журнала, которое имеет тип журнала **Расходы будущих периодов**.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-160">In the **Name** field, select the journal name that has the **Deferrals** journal type.</span></span>
    3. <span data-ttu-id="6cd8b-161">В поле **Номер разрешения** вводится номер разрешения для журнала инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-161">In the **Resolution number** field, enter the resolution number for the counting journal.</span></span>
    4. <span data-ttu-id="6cd8b-162">В поле **Дата разрешения** выберите дату разрешения для журнала инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-162">In the **Resolution date** field, select the resolution date for the counting journal.</span></span>
    5. <span data-ttu-id="6cd8b-163">В поле **Дата начала инвентаризации** выберите дату начала периода инвентаризации РБП.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-163">In the **Counting start date** field, select the start date of the deferrals counting period.</span></span> <span data-ttu-id="6cd8b-164">По умолчанию для этого поля задана текущая дата.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-164">By default, this field is set to the current date.</span></span>

        <span data-ttu-id="6cd8b-165">Поле **Дата окончания инвентаризации** установлена на дату окончания, которая была установлена для периода инвентаризации РБП в диалоговом окне **Завершить инвентаризацию РБП**.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-165">The **Counting end date** field is set to the end date that was set for the deferrals counting period in the **End deferrals counting** dialog box.</span></span>

    6. <span data-ttu-id="6cd8b-166">Выберите вкладку **Должностные лица** для настройки имен, должностей и званий должностных лиц.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-166">Select the **Officials** tab to set up the names, positions, and titles of the officials.</span></span>
    7. <span data-ttu-id="6cd8b-167">В поле **Должность** выберите название должности должностного лица.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-167">In the **Position** field, select the position title of the official.</span></span>
    8. <span data-ttu-id="6cd8b-168">В поле **Имя сотрудника** выберите имя должностного лица в списке сотрудников компании.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-168">In the **Employee name** field, select the name of the official in the list of company employees.</span></span>
    9. <span data-ttu-id="6cd8b-169">В поле **Название должности** выберите название должности сотрудника.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-169">In the **Job title** field, select the job title of the employee.</span></span>

3. <span data-ttu-id="6cd8b-170">На панели операций выберите **Строки**, чтобы открыть страницу **Строка журнала инвентаризации РБП**.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-170">On the Action Pane, select **Lines** to open the **Deferrals counting journal line** page.</span></span>

    <span data-ttu-id="6cd8b-171">Можно использовать страницу **Строка журнала инвентаризации РБП** для просмотра или изменения существующих строк журнала или для создания вручную новых строк.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-171">You can use the **Deferrals counting journal line** page to view or modify existing journal lines, or to manually create new lines.</span></span>

    <span data-ttu-id="6cd8b-172">В следующей таблице описаны поля на странице **Строка журнала инвентаризации РБП**.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-172">The following table describes the fields on the **Deferrals counting journal line** page.</span></span>

    | <span data-ttu-id="6cd8b-173">Поле</span><span class="sxs-lookup"><span data-stu-id="6cd8b-173">Field</span></span>               | <span data-ttu-id="6cd8b-174">Описание</span><span class="sxs-lookup"><span data-stu-id="6cd8b-174">Description</span></span>                                                                                                         |
    |---------------------|---------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="6cd8b-175">Код модели</span><span class="sxs-lookup"><span data-stu-id="6cd8b-175">Model number</span></span>        | <span data-ttu-id="6cd8b-176">Выберите номер модели РБП.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-176">Select the deferral model number.</span></span>                                                                                   |
    | <span data-ttu-id="6cd8b-177">Дата начала инвентаризации</span><span class="sxs-lookup"><span data-stu-id="6cd8b-177">Counting start date</span></span> | <span data-ttu-id="6cd8b-178">Дата начала, указанная для периода инвентаризации РБП на странице **Журнал инвентаризации РБП**.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-178">The start date that is specified for the deferral counting period on the **Deferrals counting journal** page.</span></span>       |
    | <span data-ttu-id="6cd8b-179">Дата окончания инвентаризации</span><span class="sxs-lookup"><span data-stu-id="6cd8b-179">Counting end date</span></span>   | <span data-ttu-id="6cd8b-180">Дата окончания, указанная для периода инвентаризации РБП на странице **Журнал инвентаризации РБП**.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-180">The end date that is specified for the deferral counting period on the **Deferrals counting journal** page.</span></span>         |
    | <span data-ttu-id="6cd8b-181">Идентификатор расхода</span><span class="sxs-lookup"><span data-stu-id="6cd8b-181">Deferral ID</span></span>         | <span data-ttu-id="6cd8b-182">Выберите идентификационный код, связанный с РБП.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-182">Select the identification code that is associated with deferral.</span></span>                                                    |
    | <span data-ttu-id="6cd8b-183">Название</span><span class="sxs-lookup"><span data-stu-id="6cd8b-183">Name</span></span>                | <span data-ttu-id="6cd8b-184">Введите имя расхода будущего периода.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-184">Enter the deferral name.</span></span>                                                                                            |
    | <span data-ttu-id="6cd8b-185">Дата вложения</span><span class="sxs-lookup"><span data-stu-id="6cd8b-185">Date attached</span></span>       | <span data-ttu-id="6cd8b-186">Выберите дату создания расхода будущего периода.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-186">Select the deferral creation date.</span></span>                                                                                  |
    | <span data-ttu-id="6cd8b-187">Срок списания</span><span class="sxs-lookup"><span data-stu-id="6cd8b-187">Writing off time</span></span>    | <span data-ttu-id="6cd8b-188">Выберите период списания для расхода будущего периода.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-188">Select the write-off period for the deferral.</span></span>                                                                       |
    | <span data-ttu-id="6cd8b-189">Сумма списания</span><span class="sxs-lookup"><span data-stu-id="6cd8b-189">Writing off amount</span></span>  | <span data-ttu-id="6cd8b-190">Введите сумму, списанную между созданием РБП и началом периода инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-190">Enter the amount that is written off between the creation of the deferral and the beginning of the counting period.</span></span> |
    | <span data-ttu-id="6cd8b-191">Оставшаяся сумма</span><span class="sxs-lookup"><span data-stu-id="6cd8b-191">Remaining amount</span></span>    | <span data-ttu-id="6cd8b-192">Введите сумму, которая должна быть списана в будущем.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-192">Enter the amount that must be written off in the future.</span></span>                                                            |
    | <span data-ttu-id="6cd8b-193">Сумма РБП</span><span class="sxs-lookup"><span data-stu-id="6cd8b-193">Deferrals amount</span></span>    | <span data-ttu-id="6cd8b-194">Выберите сумму РБП в валюте по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-194">Select the deferral amount in the default currency.</span></span>                                                                 |

4. <span data-ttu-id="6cd8b-195">Выполните следующие действия, чтобы изменить существующие строки журнала инвентаризации РБП:</span><span class="sxs-lookup"><span data-stu-id="6cd8b-195">To modify existing Deferrals counting journal lines, follow these steps:</span></span>

    1. <span data-ttu-id="6cd8b-196">В поле **Номер модели** выберите номер модели РБП из строк журнала.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-196">In the **Model number** field, select the deferral model number of the journal lines.</span></span>

        > [!NOTE]
        > <span data-ttu-id="6cd8b-197">Поля **Дата начала инвентаризации** и **Дата окончания инвентаризации** настроены на даты начала и окончания, которые были установлены для периода инвентаризации РБП на странице **Журнал инвентаризации РБП**.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-197">The **Counting start date** and **Counting end date** fields are set to the start and end dates that were set for the deferrals counting period on the **Deferrals counting journal** page.</span></span>

    2. <span data-ttu-id="6cd8b-198">В поле **Идентификатор РБП** измените код РБП.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-198">In the **Deferral ID** field, modify the deferral code.</span></span>
    3. <span data-ttu-id="6cd8b-199">В поле **Имя** измените имя РБП.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-199">In the **Name** field, modify the deferral name.</span></span>
    4. <span data-ttu-id="6cd8b-200">В поле **Дата присоединения** выберите дату, когда был создан РБП.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-200">In the **Date attached** field, select the deferral creation date.</span></span>
    5. <span data-ttu-id="6cd8b-201">В поле **Время списания** выберите период списания для РБП.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-201">In the **Writing off time** field, select the write-off period for the deferral.</span></span>
    6. <span data-ttu-id="6cd8b-202">В поле **Сумма списания** введите сумму, списанную между созданием РБП и началом периода инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-202">In the **Writing off amount** field, enter the amount that is written off between the creation of the deferral and the beginning of the counting period.</span></span>
    7. <span data-ttu-id="6cd8b-203">В поле **Сумма остатка** введите сумму, которая должна быть списана в будущем.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-203">In the **Remaining amount** field, enter the amount that must be written off in the future.</span></span>
    8. <span data-ttu-id="6cd8b-204">В поле **Сумма РБП** выберите сумму РБП в валюте по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-204">In the **Deferrals amount** field, select the deferral amount in the default currency.</span></span>
    9. <span data-ttu-id="6cd8b-205">Закройте страницу **Строка журнала инвентаризации РБП**.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-205">Close the **Deferrals counting journal line** page.</span></span>

    ![Страница строки журнала инвентаризации РБП](media/rus-counting-deferrals-01.jpg)

5. <span data-ttu-id="6cd8b-207">Чтобы распечатать отчет **Акт инвентаризации (ИНВ-11)**, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="6cd8b-207">To print the **Inventory act (INV-11)** report, follow these steps:</span></span>

    1. <span data-ttu-id="6cd8b-208">На панели операций выберите **Закрыть**, чтобы открыть диалоговое окно **Завершить инвентаризацию РБП**.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-208">On the Action Pane, select **Close** to open the **End deferrals counting** dialog box.</span></span>
    2. <span data-ttu-id="6cd8b-209">В поле **Дата окончания инвентаризации** введите дату, когда требуется закрыть журнал.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-209">In the **Counting end date** field, enter the date when you want to close the journal.</span></span>

        > [!NOTE]
        > <span data-ttu-id="6cd8b-210">Указанная вами дата отображается в поле **Дата окончания инвентаризации** страницы **Журнал инвентаризации РБП**.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-210">The date that you specify is shown in the **Counting end date** field on the **Deferrals counting journal** page.</span></span>

    3. <span data-ttu-id="6cd8b-211">Нажмите кнопку **ОК**, чтобы закрыть журнал.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-211">Select **OK** to close the journal.</span></span>
    4. <span data-ttu-id="6cd8b-212">На панели операций выберите **Печать**, чтобы открыть диалоговое окно **Инвентаризация РБП**.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-212">On the Action Pane, select **Print** to open the **Deferrals counting** dialog box.</span></span>
    5. <span data-ttu-id="6cd8b-213">В поле **Код модели** выберите код модели Расхода будущего периода.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-213">In the **Model number** field, select the deferral model number.</span></span>
    6. <span data-ttu-id="6cd8b-214">Выберите **OK** для печати **Акта инвентаризации (ИНВ-11)** с помощью шаблона Excel для номера выбранной модели.</span><span class="sxs-lookup"><span data-stu-id="6cd8b-214">Select **OK** to print the **Inventory act (INV-11)** by using the Excel template for the selected model number.</span></span>
