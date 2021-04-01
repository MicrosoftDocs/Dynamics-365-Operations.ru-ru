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
ms.search.region: Russia
ms.author: anasyash
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 1076cdd3dad5322497fb1a26969565afb1d4f725
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240563"
---
# <a name="deferrals-counting-russia"></a><span data-ttu-id="38081-103">Инвентаризация РБП (Россия)</span><span class="sxs-lookup"><span data-stu-id="38081-103">Deferrals counting (Russia)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="38081-104">Функциональность РБП поддерживает процесс инвентаризации РБП и позволяет печатать отчет **Акт инвентаризации (ИНВ-11)**.</span><span class="sxs-lookup"><span data-stu-id="38081-104">The deferrals functionality supports the process of deferrals counting and lets you print the **Inventory act (INV-11)** report.</span></span>

<span data-ttu-id="38081-105">Перед созданием отчета **Акт инвентаризации (ИНВ-11)** необходимо создать РБП и разнести проводки списания в журнале РБП.</span><span class="sxs-lookup"><span data-stu-id="38081-105">Before you generate the **Inventory act (INV-11)** report, you must create deferrals and post writing-off transactions in the deferrals journal.</span></span>

1. <span data-ttu-id="38081-106">Перейдите к **Главная книга** \> **Периодические задачи** \> **Расходы будущих периодов** \> **Журнал инвентаризации РБП**.</span><span class="sxs-lookup"><span data-stu-id="38081-106">Go to **General ledger** \> **Periodic tasks** \> **Deferrals** \> **Deferrals counting journal**.</span></span>

    <span data-ttu-id="38081-107">Можно использовать страницу **Журнал инвентаризации РБП** для создания журнала инвентаризации РБП и печати отчета **Акт инвентаризации (ИНВ-11)**.</span><span class="sxs-lookup"><span data-stu-id="38081-107">You can use the **Deferrals counting journal** page to create a Deferrals counting journal and print the **Inventory act (INV-11)** report.</span></span>

    <span data-ttu-id="38081-108">В следующей таблице описаны вкладки на странице **Журнал инвентаризации РБП**.</span><span class="sxs-lookup"><span data-stu-id="38081-108">The following table describes the tabs on the **Deferrals counting journal** page.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="38081-109">Вкладка</span><span class="sxs-lookup"><span data-stu-id="38081-109">Tab</span></span></th>
    <th><span data-ttu-id="38081-110">Описание</span><span class="sxs-lookup"><span data-stu-id="38081-110">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="38081-111">Обзор</span><span class="sxs-lookup"><span data-stu-id="38081-111">Overview</span></span></td>
    <td><span data-ttu-id="38081-112">Создать новый журнал инвентаризации РБП.</span><span class="sxs-lookup"><span data-stu-id="38081-112">Create a new Deferrals counting journal.</span></span>
    <p><span data-ttu-id="38081-113"><strong>Примечание:</strong> Вы не можете создать более одного журнала с одинаковой датой инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="38081-113"><strong>Note:</strong> You can't create more than one journal that has the same counting date.</span></span></p>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="38081-114">Должностные лица</span><span class="sxs-lookup"><span data-stu-id="38081-114">Officials</span></span></td>
    <td><span data-ttu-id="38081-115">Укажите имена, должности и звания должностных лиц.</span><span class="sxs-lookup"><span data-stu-id="38081-115">Specify the names, positions, and titles of the officials.</span></span></td>
    </tr>
    </tbody>
    </table>

    <span data-ttu-id="38081-116">В следующей таблице описаны кнопки на панели операций страницы **Журнал инвентаризации РБП**.</span><span class="sxs-lookup"><span data-stu-id="38081-116">The following table describes the buttons on the Action Pane of the **Deferrals counting journal** page.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="38081-117">Кнопка</span><span class="sxs-lookup"><span data-stu-id="38081-117">Button</span></span></th>
    <th><span data-ttu-id="38081-118">Описание</span><span class="sxs-lookup"><span data-stu-id="38081-118">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="38081-119">Линии</span><span class="sxs-lookup"><span data-stu-id="38081-119">Lines</span></span></td>
    <td><span data-ttu-id="38081-120">Откройте страницу <strong>Строка журнала инвентаризации РБП</strong>, где можно создавать строки журналов.</span><span class="sxs-lookup"><span data-stu-id="38081-120">Open the <strong>Deferrals counting journal line</strong> page, where you can create journal lines.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="38081-121">Близкие</span><span class="sxs-lookup"><span data-stu-id="38081-121">Close</span></span></td>
    <td><span data-ttu-id="38081-122">Откройте диалоговое окно <strong>Завершить инвентаризацию РБП</strong>.</span><span class="sxs-lookup"><span data-stu-id="38081-122">Open the <strong>End deferrals counting</strong> dialog box.</span></span> <span data-ttu-id="38081-123">В поле <strong>Дата окончания инвентаризации</strong> можно ввести дату, когда требуется закрыть журнал.</span><span class="sxs-lookup"><span data-stu-id="38081-123">In the <strong>Counting end date</strong> field, you can then enter the date when you want to close the journal.</span></span> <span data-ttu-id="38081-124">Указанная вами дата отображается в поле <strong>Дата окончания инвентаризации</strong> страницы <strong>Журнал инвентаризации РБП</strong>.</span><span class="sxs-lookup"><span data-stu-id="38081-124">The date that you specify is shown in the <strong>Counting end date</strong> field on the <strong>Deferrals counting journal</strong> page.</span></span>
    <p><span data-ttu-id="38081-125"><strong>Примечание:</strong> Вы не можете закрыть журнал, если строки журнала не созданы.</span><span class="sxs-lookup"><span data-stu-id="38081-125"><strong>Note:</strong> You can't close the journal if journal lines aren't created.</span></span></p>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="38081-126">Печать</span><span class="sxs-lookup"><span data-stu-id="38081-126">Print</span></span></td>
    <td><span data-ttu-id="38081-127">Откройте диалоговое окно <strong>Инвентаризация РБП</strong>, где можно распечатать отчет <strong>Акт инвентаризации (ИНВ-11)</strong>, используя шаблон Microsoft Excel для номера выбранной модели.</span><span class="sxs-lookup"><span data-stu-id="38081-127">Open the <strong>Deferrals counting</strong> dialog box, where you can print the <strong>Inventory act (INV-11)</strong> report by using the Microsoft Excel template for the selected model number.</span></span></td>
    </tr>
    </tbody>
    </table>

    <span data-ttu-id="38081-128">В следующей таблице описаны поля на странице **Журнал инвентаризации РБП**.</span><span class="sxs-lookup"><span data-stu-id="38081-128">The following table describes the fields on the **Deferrals counting journal** page.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="38081-129">Поле</span><span class="sxs-lookup"><span data-stu-id="38081-129">Field</span></span></th>
    <th><span data-ttu-id="38081-130">Описание</span><span class="sxs-lookup"><span data-stu-id="38081-130">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="38081-131">Отображение</span><span class="sxs-lookup"><span data-stu-id="38081-131">Show</span></span></td>
    <td><span data-ttu-id="38081-132">Выберите, какие ваучеры или журналы отображаются на странице, на основе статуса разноски:</span><span class="sxs-lookup"><span data-stu-id="38081-132">Select which vouchers or journals are shown on the page, based on the posting status:</span></span> <ul>
    <li><span data-ttu-id="38081-133"><strong>Все</strong> — показать все журналы.</span><span class="sxs-lookup"><span data-stu-id="38081-133"><strong>All</strong> – Show all journals.</span></span></li>
    <li><span data-ttu-id="38081-134"><strong>Открыто</strong> — Показать только журналы, которые не разнесены.</span><span class="sxs-lookup"><span data-stu-id="38081-134"><strong>Open</strong> – Show only journals that aren't posted.</span></span></li>
    <li><span data-ttu-id="38081-135"><strong>Разнесено</strong> — Показать только журналы, которые разнесены.</span><span class="sxs-lookup"><span data-stu-id="38081-135"><strong>Posted</strong> – Show only journals that are posted.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="38081-136">Номер партии журнала</span><span class="sxs-lookup"><span data-stu-id="38081-136">Journal batch number</span></span></td>
    <td><span data-ttu-id="38081-137">Номер журнала РБП.</span><span class="sxs-lookup"><span data-stu-id="38081-137">The deferral journal number.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="38081-138">Название</span><span class="sxs-lookup"><span data-stu-id="38081-138">Name</span></span></td>
    <td><span data-ttu-id="38081-139">Выберите наименование журнала, которое имеет тип журнала <strong>Расходы будущих периодов</strong>.</span><span class="sxs-lookup"><span data-stu-id="38081-139">Select the journal name that has the <strong>Deferrals</strong> journal type.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="38081-140">Номер распоряжения</span><span class="sxs-lookup"><span data-stu-id="38081-140">Resolution number</span></span></td>
    <td><span data-ttu-id="38081-141">Введите номер разрешения для журнала инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="38081-141">Enter the resolution number for the counting journal.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="38081-142">Дата приказа</span><span class="sxs-lookup"><span data-stu-id="38081-142">Resolution date</span></span></td>
    <td><span data-ttu-id="38081-143">Выберите дату разрешения для журнала инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="38081-143">Select the resolution date for the counting journal.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="38081-144">Дата начала инвентаризации</span><span class="sxs-lookup"><span data-stu-id="38081-144">Counting start date</span></span></td>
    <td><span data-ttu-id="38081-145">Выберите дату начала периода инвентаризации РБП.</span><span class="sxs-lookup"><span data-stu-id="38081-145">Select the start date of the deferrals counting period.</span></span> <span data-ttu-id="38081-146">По умолчанию для этого поля задана текущая дата.</span><span class="sxs-lookup"><span data-stu-id="38081-146">By default, this field is set to the current date.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="38081-147">Дата окончания инвентаризации</span><span class="sxs-lookup"><span data-stu-id="38081-147">Counting end date</span></span></td>
    <td><span data-ttu-id="38081-148">Дата окончания периода инвентаризации РБП.</span><span class="sxs-lookup"><span data-stu-id="38081-148">The end date of the deferrals counting period.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="38081-149">Закрытый</span><span class="sxs-lookup"><span data-stu-id="38081-149">Closed</span></span></td>
    <td><span data-ttu-id="38081-150">Этот флажок автоматически выбирается после завершения инвентаризации РБП и закрытия журнала.</span><span class="sxs-lookup"><span data-stu-id="38081-150">This check box is automatically selected when the deferral counting is completed and the journal is closed.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="38081-151">Занимаемая должность</span><span class="sxs-lookup"><span data-stu-id="38081-151">Position</span></span></td>
    <td><span data-ttu-id="38081-152">Выберите название должности должностного лица.</span><span class="sxs-lookup"><span data-stu-id="38081-152">Select the position title of the official.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="38081-153">Имя сотрудника</span><span class="sxs-lookup"><span data-stu-id="38081-153">Employee name</span></span></td>
    <td><span data-ttu-id="38081-154">Выберите имя должностного лица в списке сотрудников компании.</span><span class="sxs-lookup"><span data-stu-id="38081-154">Select the name of the official in the list of company employees.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="38081-155">Название должности</span><span class="sxs-lookup"><span data-stu-id="38081-155">Title</span></span></td>
    <td><span data-ttu-id="38081-156">Выберите название должности сотрудника.</span><span class="sxs-lookup"><span data-stu-id="38081-156">Select the job title of the employee.</span></span></td>
    </tr>
    </tbody>
    </table>

2. <span data-ttu-id="38081-157">Выполните следующие действия, чтобы создать новый журнал инвентаризации РБП:</span><span class="sxs-lookup"><span data-stu-id="38081-157">To create a new Deferrals counting journal, follow these steps:</span></span>

    1. <span data-ttu-id="38081-158">В области действий выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="38081-158">On the Action Pane, select **New**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="38081-159">Вы не можете создать более одного журнала инвентаризации РБП с одинаковой датой инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="38081-159">You can't create more than one Deferrals counting journal that has the same counting date.</span></span>

    2. <span data-ttu-id="38081-160">В поле **Имя** выберите наименование журнала, которое имеет тип журнала **Расходы будущих периодов**.</span><span class="sxs-lookup"><span data-stu-id="38081-160">In the **Name** field, select the journal name that has the **Deferrals** journal type.</span></span>
    3. <span data-ttu-id="38081-161">В поле **Номер разрешения** вводится номер разрешения для журнала инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="38081-161">In the **Resolution number** field, enter the resolution number for the counting journal.</span></span>
    4. <span data-ttu-id="38081-162">В поле **Дата разрешения** выберите дату разрешения для журнала инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="38081-162">In the **Resolution date** field, select the resolution date for the counting journal.</span></span>
    5. <span data-ttu-id="38081-163">В поле **Дата начала инвентаризации** выберите дату начала периода инвентаризации РБП.</span><span class="sxs-lookup"><span data-stu-id="38081-163">In the **Counting start date** field, select the start date of the deferrals counting period.</span></span> <span data-ttu-id="38081-164">По умолчанию для этого поля задана текущая дата.</span><span class="sxs-lookup"><span data-stu-id="38081-164">By default, this field is set to the current date.</span></span>

        <span data-ttu-id="38081-165">Поле **Дата окончания инвентаризации** установлена на дату окончания, которая была установлена для периода инвентаризации РБП в диалоговом окне **Завершить инвентаризацию РБП**.</span><span class="sxs-lookup"><span data-stu-id="38081-165">The **Counting end date** field is set to the end date that was set for the deferrals counting period in the **End deferrals counting** dialog box.</span></span>

    6. <span data-ttu-id="38081-166">Выберите вкладку **Должностные лица** для настройки имен, должностей и званий должностных лиц.</span><span class="sxs-lookup"><span data-stu-id="38081-166">Select the **Officials** tab to set up the names, positions, and titles of the officials.</span></span>
    7. <span data-ttu-id="38081-167">В поле **Должность** выберите название должности должностного лица.</span><span class="sxs-lookup"><span data-stu-id="38081-167">In the **Position** field, select the position title of the official.</span></span>
    8. <span data-ttu-id="38081-168">В поле **Имя сотрудника** выберите имя должностного лица в списке сотрудников компании.</span><span class="sxs-lookup"><span data-stu-id="38081-168">In the **Employee name** field, select the name of the official in the list of company employees.</span></span>
    9. <span data-ttu-id="38081-169">В поле **Название должности** выберите название должности сотрудника.</span><span class="sxs-lookup"><span data-stu-id="38081-169">In the **Job title** field, select the job title of the employee.</span></span>

3. <span data-ttu-id="38081-170">На панели операций выберите **Строки**, чтобы открыть страницу **Строка журнала инвентаризации РБП**.</span><span class="sxs-lookup"><span data-stu-id="38081-170">On the Action Pane, select **Lines** to open the **Deferrals counting journal line** page.</span></span>

    <span data-ttu-id="38081-171">Можно использовать страницу **Строка журнала инвентаризации РБП** для просмотра или изменения существующих строк журнала или для создания вручную новых строк.</span><span class="sxs-lookup"><span data-stu-id="38081-171">You can use the **Deferrals counting journal line** page to view or modify existing journal lines, or to manually create new lines.</span></span>

    <span data-ttu-id="38081-172">В следующей таблице описаны поля на странице **Строка журнала инвентаризации РБП**.</span><span class="sxs-lookup"><span data-stu-id="38081-172">The following table describes the fields on the **Deferrals counting journal line** page.</span></span>

    | <span data-ttu-id="38081-173">Поле</span><span class="sxs-lookup"><span data-stu-id="38081-173">Field</span></span>               | <span data-ttu-id="38081-174">Описание</span><span class="sxs-lookup"><span data-stu-id="38081-174">Description</span></span>                                                                                                         |
    |---------------------|---------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="38081-175">Код модели</span><span class="sxs-lookup"><span data-stu-id="38081-175">Model number</span></span>        | <span data-ttu-id="38081-176">Выберите номер модели РБП.</span><span class="sxs-lookup"><span data-stu-id="38081-176">Select the deferral model number.</span></span>                                                                                   |
    | <span data-ttu-id="38081-177">Дата начала инвентаризации</span><span class="sxs-lookup"><span data-stu-id="38081-177">Counting start date</span></span> | <span data-ttu-id="38081-178">Дата начала, указанная для периода инвентаризации РБП на странице **Журнал инвентаризации РБП**.</span><span class="sxs-lookup"><span data-stu-id="38081-178">The start date that is specified for the deferral counting period on the **Deferrals counting journal** page.</span></span>       |
    | <span data-ttu-id="38081-179">Дата окончания инвентаризации</span><span class="sxs-lookup"><span data-stu-id="38081-179">Counting end date</span></span>   | <span data-ttu-id="38081-180">Дата окончания, указанная для периода инвентаризации РБП на странице **Журнал инвентаризации РБП**.</span><span class="sxs-lookup"><span data-stu-id="38081-180">The end date that is specified for the deferral counting period on the **Deferrals counting journal** page.</span></span>         |
    | <span data-ttu-id="38081-181">Идентификатор расхода</span><span class="sxs-lookup"><span data-stu-id="38081-181">Deferral ID</span></span>         | <span data-ttu-id="38081-182">Выберите идентификационный код, связанный с РБП.</span><span class="sxs-lookup"><span data-stu-id="38081-182">Select the identification code that is associated with deferral.</span></span>                                                    |
    | <span data-ttu-id="38081-183">Название</span><span class="sxs-lookup"><span data-stu-id="38081-183">Name</span></span>                | <span data-ttu-id="38081-184">Введите имя расхода будущего периода.</span><span class="sxs-lookup"><span data-stu-id="38081-184">Enter the deferral name.</span></span>                                                                                            |
    | <span data-ttu-id="38081-185">Дата вложения</span><span class="sxs-lookup"><span data-stu-id="38081-185">Date attached</span></span>       | <span data-ttu-id="38081-186">Выберите дату создания расхода будущего периода.</span><span class="sxs-lookup"><span data-stu-id="38081-186">Select the deferral creation date.</span></span>                                                                                  |
    | <span data-ttu-id="38081-187">Срок списания</span><span class="sxs-lookup"><span data-stu-id="38081-187">Writing off time</span></span>    | <span data-ttu-id="38081-188">Выберите период списания для расхода будущего периода.</span><span class="sxs-lookup"><span data-stu-id="38081-188">Select the write-off period for the deferral.</span></span>                                                                       |
    | <span data-ttu-id="38081-189">Сумма списания</span><span class="sxs-lookup"><span data-stu-id="38081-189">Writing off amount</span></span>  | <span data-ttu-id="38081-190">Введите сумму, списанную между созданием РБП и началом периода инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="38081-190">Enter the amount that is written off between the creation of the deferral and the beginning of the counting period.</span></span> |
    | <span data-ttu-id="38081-191">Оставшаяся сумма</span><span class="sxs-lookup"><span data-stu-id="38081-191">Remaining amount</span></span>    | <span data-ttu-id="38081-192">Введите сумму, которая должна быть списана в будущем.</span><span class="sxs-lookup"><span data-stu-id="38081-192">Enter the amount that must be written off in the future.</span></span>                                                            |
    | <span data-ttu-id="38081-193">Сумма РБП</span><span class="sxs-lookup"><span data-stu-id="38081-193">Deferrals amount</span></span>    | <span data-ttu-id="38081-194">Выберите сумму РБП в валюте по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="38081-194">Select the deferral amount in the default currency.</span></span>                                                                 |

4. <span data-ttu-id="38081-195">Выполните следующие действия, чтобы изменить существующие строки журнала инвентаризации РБП:</span><span class="sxs-lookup"><span data-stu-id="38081-195">To modify existing Deferrals counting journal lines, follow these steps:</span></span>

    1. <span data-ttu-id="38081-196">В поле **Номер модели** выберите номер модели РБП из строк журнала.</span><span class="sxs-lookup"><span data-stu-id="38081-196">In the **Model number** field, select the deferral model number of the journal lines.</span></span>

        > [!NOTE]
        > <span data-ttu-id="38081-197">Поля **Дата начала инвентаризации** и **Дата окончания инвентаризации** настроены на даты начала и окончания, которые были установлены для периода инвентаризации РБП на странице **Журнал инвентаризации РБП**.</span><span class="sxs-lookup"><span data-stu-id="38081-197">The **Counting start date** and **Counting end date** fields are set to the start and end dates that were set for the deferrals counting period on the **Deferrals counting journal** page.</span></span>

    2. <span data-ttu-id="38081-198">В поле **Идентификатор РБП** измените код РБП.</span><span class="sxs-lookup"><span data-stu-id="38081-198">In the **Deferral ID** field, modify the deferral code.</span></span>
    3. <span data-ttu-id="38081-199">В поле **Имя** измените имя РБП.</span><span class="sxs-lookup"><span data-stu-id="38081-199">In the **Name** field, modify the deferral name.</span></span>
    4. <span data-ttu-id="38081-200">В поле **Дата присоединения** выберите дату, когда был создан РБП.</span><span class="sxs-lookup"><span data-stu-id="38081-200">In the **Date attached** field, select the deferral creation date.</span></span>
    5. <span data-ttu-id="38081-201">В поле **Время списания** выберите период списания для РБП.</span><span class="sxs-lookup"><span data-stu-id="38081-201">In the **Writing off time** field, select the write-off period for the deferral.</span></span>
    6. <span data-ttu-id="38081-202">В поле **Сумма списания** введите сумму, списанную между созданием РБП и началом периода инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="38081-202">In the **Writing off amount** field, enter the amount that is written off between the creation of the deferral and the beginning of the counting period.</span></span>
    7. <span data-ttu-id="38081-203">В поле **Сумма остатка** введите сумму, которая должна быть списана в будущем.</span><span class="sxs-lookup"><span data-stu-id="38081-203">In the **Remaining amount** field, enter the amount that must be written off in the future.</span></span>
    8. <span data-ttu-id="38081-204">В поле **Сумма РБП** выберите сумму РБП в валюте по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="38081-204">In the **Deferrals amount** field, select the deferral amount in the default currency.</span></span>
    9. <span data-ttu-id="38081-205">Закройте страницу **Строка журнала инвентаризации РБП**.</span><span class="sxs-lookup"><span data-stu-id="38081-205">Close the **Deferrals counting journal line** page.</span></span>

    ![Страница строки журнала инвентаризации РБП](media/rus-counting-deferrals-01.jpg)

5. <span data-ttu-id="38081-207">Чтобы распечатать отчет **Акт инвентаризации (ИНВ-11)**, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="38081-207">To print the **Inventory act (INV-11)** report, follow these steps:</span></span>

    1. <span data-ttu-id="38081-208">На панели операций выберите **Закрыть**, чтобы открыть диалоговое окно **Завершить инвентаризацию РБП**.</span><span class="sxs-lookup"><span data-stu-id="38081-208">On the Action Pane, select **Close** to open the **End deferrals counting** dialog box.</span></span>
    2. <span data-ttu-id="38081-209">В поле **Дата окончания инвентаризации** введите дату, когда требуется закрыть журнал.</span><span class="sxs-lookup"><span data-stu-id="38081-209">In the **Counting end date** field, enter the date when you want to close the journal.</span></span>

        > [!NOTE]
        > <span data-ttu-id="38081-210">Указанная вами дата отображается в поле **Дата окончания инвентаризации** страницы **Журнал инвентаризации РБП**.</span><span class="sxs-lookup"><span data-stu-id="38081-210">The date that you specify is shown in the **Counting end date** field on the **Deferrals counting journal** page.</span></span>

    3. <span data-ttu-id="38081-211">Нажмите кнопку **ОК**, чтобы закрыть журнал.</span><span class="sxs-lookup"><span data-stu-id="38081-211">Select **OK** to close the journal.</span></span>
    4. <span data-ttu-id="38081-212">На панели операций выберите **Печать**, чтобы открыть диалоговое окно **Инвентаризация РБП**.</span><span class="sxs-lookup"><span data-stu-id="38081-212">On the Action Pane, select **Print** to open the **Deferrals counting** dialog box.</span></span>
    5. <span data-ttu-id="38081-213">В поле **Код модели** выберите код модели Расхода будущего периода.</span><span class="sxs-lookup"><span data-stu-id="38081-213">In the **Model number** field, select the deferral model number.</span></span>
    6. <span data-ttu-id="38081-214">Выберите **OK** для печати **Акта инвентаризации (ИНВ-11)** с помощью шаблона Excel для номера выбранной модели.</span><span class="sxs-lookup"><span data-stu-id="38081-214">Select **OK** to print the **Inventory act (INV-11)** by using the Excel template for the selected model number.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]