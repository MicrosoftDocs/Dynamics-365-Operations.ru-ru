---
title: Настройка расходов будущих периодов (Россия)
description: В этом разделе описывается, как настроить расходы будущих периодов.
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
ms.openlocfilehash: 22a242244cfd2f041e513005cefce2114a302f81
ms.sourcegitcommit: 4fd51830be21b95a1398dc80d5429a74bcec73fc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2019
ms.locfileid: "1736979"
---
# <a name="set-up-deferrals-russia"></a><span data-ttu-id="86b4e-103">Настройка расходов будущих периодов (Россия)</span><span class="sxs-lookup"><span data-stu-id="86b4e-103">Set up deferrals (Russia)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="86b4e-104">Расходы будущих периодов – это типы расходов, которые хранятся по-разному в общих учетных политиках и принципах налогового учета.</span><span class="sxs-lookup"><span data-stu-id="86b4e-104">Deferrals are expense types that are stored differently in general accounting principles and tax accounting principles.</span></span> <span data-ttu-id="86b4e-105">Чтобы использовать функциональность расходов будущего периода в Microsoft Dynamics 365 for Finance and Operations, вы должны завершить следующую настройку:</span><span class="sxs-lookup"><span data-stu-id="86b4e-105">To use the deferral functionality in Microsoft Dynamics 365 for Finance and Operations, you must complete the following setup:</span></span>

- [<span data-ttu-id="86b4e-106">Методы списания</span><span class="sxs-lookup"><span data-stu-id="86b4e-106">Write-off methods</span></span>](#write-off-methods)
- [<span data-ttu-id="86b4e-107">Модели учета</span><span class="sxs-lookup"><span data-stu-id="86b4e-107">Value models</span></span>](#value-models)
- [<span data-ttu-id="86b4e-108">Профили разноски</span><span class="sxs-lookup"><span data-stu-id="86b4e-108">Posting profiles</span></span>](#posting-profiles)
- [<span data-ttu-id="86b4e-109">Последовательности расчета</span><span class="sxs-lookup"><span data-stu-id="86b4e-109">Sequence of calculation</span></span>](#sequence-of-calculation)
- [<span data-ttu-id="86b4e-110">Группы РБП</span><span class="sxs-lookup"><span data-stu-id="86b4e-110">Deferrals groups</span></span>](#deferrals-groups)
- [<span data-ttu-id="86b4e-111">Параметры главной книги</span><span class="sxs-lookup"><span data-stu-id="86b4e-111">General ledger parameters</span></span>](#general-ledger-parameters)
- [<span data-ttu-id="86b4e-112">РБП</span><span class="sxs-lookup"><span data-stu-id="86b4e-112">Deferrals</span></span>](#deferrals)

## <a name="write-off-methods"></a><span data-ttu-id="86b4e-113">Методы списания</span><span class="sxs-lookup"><span data-stu-id="86b4e-113">Write-off methods</span></span>

<span data-ttu-id="86b4e-114">Выполните следующие действия, чтобы создать методы списания для расходов будущих периодов.</span><span class="sxs-lookup"><span data-stu-id="86b4e-114">Follow these steps to create write-off methods for deferred expenses.</span></span>

1. <span data-ttu-id="86b4e-115">Перейти к **главная книга** \> **Настройка расходов будущих периодов** \> **Методы списания**.</span><span class="sxs-lookup"><span data-stu-id="86b4e-115">Go to **General ledger** \> **Deferrals setup** \> **Writing off methods**.</span></span>
2. <span data-ttu-id="86b4e-116">На панели операций выберите **Новый** для создания метода списания расходов будущих периодов.</span><span class="sxs-lookup"><span data-stu-id="86b4e-116">On the Action Pane, select **New** to create a write-off method for deferred expenses.</span></span>

    <span data-ttu-id="86b4e-117">В следующей таблице описаны поля на странице **Методы списания**.</span><span class="sxs-lookup"><span data-stu-id="86b4e-117">The following table describes the fields on the **Writing off methods** page.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="86b4e-118">Поле</span><span class="sxs-lookup"><span data-stu-id="86b4e-118">Field</span></span></th>
    <th><span data-ttu-id="86b4e-119">Описание</span><span class="sxs-lookup"><span data-stu-id="86b4e-119">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="86b4e-120">Метод списания</span><span class="sxs-lookup"><span data-stu-id="86b4e-120">Writing off method</span></span></td>
    <td><span data-ttu-id="86b4e-121">Введите код метода списания.</span><span class="sxs-lookup"><span data-stu-id="86b4e-121">Enter the code for the write-off method.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-122">Название</span><span class="sxs-lookup"><span data-stu-id="86b4e-122">Name</span></span></td>
    <td><span data-ttu-id="86b4e-123">Введите описание метода списания.</span><span class="sxs-lookup"><span data-stu-id="86b4e-123">Enter a description of the write-off method.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-124">Вид</span><span class="sxs-lookup"><span data-stu-id="86b4e-124">Type</span></span></td>
    <td><span data-ttu-id="86b4e-125">Выберите тип списания:</span><span class="sxs-lookup"><span data-stu-id="86b4e-125">Select the type of write-off:</span></span> <ul>
    <li><span data-ttu-id="86b4e-126"><strong>Линейный</strong> — Равномерно разделить сумму списания на все интервалы в определенный период.</span><span class="sxs-lookup"><span data-stu-id="86b4e-126"><strong>Linear</strong> – Evenly divide the write-off amount across all intervals in the defined period.</span></span></li>
    <li><span data-ttu-id="86b4e-127"><strong>Ручной</strong> — Вручную введите либо процент от общей суммы, либо сумму для списания в каждом периоде, в зависимости от выбранного типа расчета в поле <strong>Тип расчета</strong> .</span><span class="sxs-lookup"><span data-stu-id="86b4e-127"><strong>Manual</strong> – Manually enter either a percentage of the total or the amount to write off in each period, depending on the calculation type that you select in the <strong>Calculation type</strong> field.</span></span> <span data-ttu-id="86b4e-128">На странице <strong>Графики списания</strong> можно настроить другой процент для каждого периода списания.</span><span class="sxs-lookup"><span data-stu-id="86b4e-128">On the <strong>Manual schedules</strong> page, you can set up a different percentage for each write-off period.</span></span> <span data-ttu-id="86b4e-129">На странице <strong>Сумма списания</strong> можно настроить другую сумму для каждого периода списания.</span><span class="sxs-lookup"><span data-stu-id="86b4e-129">On the <strong>Writing off sum</strong> page, you can set up a different amount for each write-off period.</span></span></li>
    <li><span data-ttu-id="86b4e-130"><strong>Линейный с коэффициентом</strong> — вычисляемый результат умножается на расчетный коэффициент.</span><span class="sxs-lookup"><span data-stu-id="86b4e-130"><strong>Linear with factor</strong> – Multiply the calculated result by a calculated factor.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-131">Период списания</span><span class="sxs-lookup"><span data-stu-id="86b4e-131">Writing off period</span></span></td>
    <td><span data-ttu-id="86b4e-132">Выберите период списания для расхода будущих периодов:</span><span class="sxs-lookup"><span data-stu-id="86b4e-132">Select the write-off period for the deferred expense:</span></span> <ul>
    <li><span data-ttu-id="86b4e-133">Месяц</span><span class="sxs-lookup"><span data-stu-id="86b4e-133">Month</span></span></li>
    <li><span data-ttu-id="86b4e-134">Квартал</span><span class="sxs-lookup"><span data-stu-id="86b4e-134">Quarter</span></span></li>
    <li><span data-ttu-id="86b4e-135">Полгода</span><span class="sxs-lookup"><span data-stu-id="86b4e-135">Half-Yearly</span></span></li>
    <li><span data-ttu-id="86b4e-136">Годы</span><span class="sxs-lookup"><span data-stu-id="86b4e-136">Years</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-137">Расчетный период</span><span class="sxs-lookup"><span data-stu-id="86b4e-137">Calculation period</span></span></td>
    <td><span data-ttu-id="86b4e-138">Выберите расчетный период для расхода будущих периодов:</span><span class="sxs-lookup"><span data-stu-id="86b4e-138">Select the calculation period for the deferred expense:</span></span> <ul>
    <li><span data-ttu-id="86b4e-139"><strong>Месяц</strong> — расчет списания расходов будущих периодов выполняется пропорционально количеству месяцев в заданном периоде.</span><span class="sxs-lookup"><span data-stu-id="86b4e-139"><strong>Month</strong> – The deferrals write-off calculation is done proportionately over the number of months in the given period.</span></span></li>
    <li><span data-ttu-id="86b4e-140"><strong>День</strong> — расчет списания расходов будущих периодов выполняется пропорционально количеству дней в заданном периоде.</span><span class="sxs-lookup"><span data-stu-id="86b4e-140"><strong>Day</strong> – The deferrals write-off calculation is done proportionately over the number of days in the given period.</span></span> <span data-ttu-id="86b4e-141">Этот параметр позволяет рассчитывать сумму списания расходов будущих периодов в течение неполного отчетного периода в зависимости от количества календарных дней.</span><span class="sxs-lookup"><span data-stu-id="86b4e-141">This option lets you calculate the deferred expense write-off amount for an incomplete reporting period, based on the number of calendar days in the period.</span></span></li>
    <li><span data-ttu-id="86b4e-142"><strong>Период</strong> — расчет выполняется пропорционально количеству периодов, которые определены в поле <strong>Период списания</strong>.</span><span class="sxs-lookup"><span data-stu-id="86b4e-142"><strong>Period</strong> – The calculation is done proportionately for the number of periods that are defined in the <strong>Writing off period</strong> field.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-143">Тип расчета</span><span class="sxs-lookup"><span data-stu-id="86b4e-143">Calculation type</span></span></td>
    <td><span data-ttu-id="86b4e-144">Если вы выбрали <strong>Ручной</strong> в поле <strong>Тип</strong>, выберите тип расчета для списания вручную:</span><span class="sxs-lookup"><span data-stu-id="86b4e-144">If you selected <strong>Manual</strong> in the <strong>Type</strong> field, select the calculation type for the manual write-off:</span></span> <ul>
    <li><span data-ttu-id="86b4e-145"><strong>Процент</strong> — Процент от общей суммы списывается в каждом периоде.</span><span class="sxs-lookup"><span data-stu-id="86b4e-145"><strong>Percent</strong> – A percentage of the total is written off in each period.</span></span> <span data-ttu-id="86b4e-146">Вы вручную вводите этот процент на странице <strong>Графики списания</strong>.</span><span class="sxs-lookup"><span data-stu-id="86b4e-146">You manually enter this percentage on the <strong>Manual schedules</strong> page.</span></span></li>
    <li><span data-ttu-id="86b4e-147"><strong>Сумма</strong> — Сумма списывается.</span><span class="sxs-lookup"><span data-stu-id="86b4e-147"><strong>Amount</strong> – An amount is written off.</span></span> <span data-ttu-id="86b4e-148">На странице <strong>Сумма списания</strong> можно настроить отдельную сумму для каждого периода списания.</span><span class="sxs-lookup"><span data-stu-id="86b4e-148">On the <strong>Writing off sum</strong> page, you can set up a separate amount for each write-off period.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-149">Округление</span><span class="sxs-lookup"><span data-stu-id="86b4e-149">Round-off</span></span></td>
    <td><span data-ttu-id="86b4e-150">Введите значение округления для суммы списания отложенного счета.</span><span class="sxs-lookup"><span data-stu-id="86b4e-150">Enter the round-off value for the deferred expense write-off amount.</span></span></td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="86b4e-151">Если вы выбрали **Ручной** в поле **Тип** и **Сумма** в поле **Тип расчета**, на панели операций выберите **Графики списания** для создания графиков списания.</span><span class="sxs-lookup"><span data-stu-id="86b4e-151">If you selected **Manual** in the **Type** field and **Amount** in the **Calculation type** field, on the Action Pane, select **Manual schedules** to create write-off schedules.</span></span>

![Страница методы списания](media/rus-set-up-deferral-01.png)

## <a name="value-models"></a><span data-ttu-id="86b4e-153">Модели учета</span><span class="sxs-lookup"><span data-stu-id="86b4e-153">Value models</span></span>

1. <span data-ttu-id="86b4e-154">Перейти к **главная книга** \> **Настройка расходов будущих периодов** \> **Модели стоимости**.</span><span class="sxs-lookup"><span data-stu-id="86b4e-154">Go to **General ledger** \> **Deferrals setup** \> **Value models**.</span></span>
2. <span data-ttu-id="86b4e-155">На панели операций выберите **Новый** для создания моделей стоимости для учета расходов будущих периодов.</span><span class="sxs-lookup"><span data-stu-id="86b4e-155">On the Action Pane, select **New** to create value models for deferrals accounting.</span></span>

    <span data-ttu-id="86b4e-156">В следующей таблице описаны поля на странице **Модели стоимости**.</span><span class="sxs-lookup"><span data-stu-id="86b4e-156">The following table describes the fields on the **Value models** page.</span></span>

    | <span data-ttu-id="86b4e-157">Поле</span><span class="sxs-lookup"><span data-stu-id="86b4e-157">Field</span></span>         | <span data-ttu-id="86b4e-158">Описание</span><span class="sxs-lookup"><span data-stu-id="86b4e-158">Description</span></span>                                               |
    |---------------|-----------------------------------------------------------|
    | <span data-ttu-id="86b4e-159">Код модели</span><span class="sxs-lookup"><span data-stu-id="86b4e-159">Model number</span></span>  | <span data-ttu-id="86b4e-160">Введите модель расходов будущего периода, чтобы связать с расходом будущего периода.</span><span class="sxs-lookup"><span data-stu-id="86b4e-160">Enter the deferrals model to associate with the deferral.</span></span> |
    | <span data-ttu-id="86b4e-161">Название</span><span class="sxs-lookup"><span data-stu-id="86b4e-161">Name</span></span>          | <span data-ttu-id="86b4e-162">Введите имя модели стоимости.</span><span class="sxs-lookup"><span data-stu-id="86b4e-162">Enter a name for value model.</span></span>                             |
    | <span data-ttu-id="86b4e-163">Слой разноски</span><span class="sxs-lookup"><span data-stu-id="86b4e-163">Posting layer</span></span> | <span data-ttu-id="86b4e-164">Выбирается слой разноски для модель стоимости.</span><span class="sxs-lookup"><span data-stu-id="86b4e-164">Select a posting layer for the value model.</span></span>               |

3. <span data-ttu-id="86b4e-165">В панели операций выберите **Группы расходов будущих периодов** для настройки групп расходов будущих периодов, связанных с выбранной моделью стоимости.</span><span class="sxs-lookup"><span data-stu-id="86b4e-165">On the Action Pane, select **Deferrals groups** to set up deferrals groups that are related to the selected value model.</span></span>

![Страница моделей стоимости](media/rus-set-up-deferral-02.png)

## <a name="posting-profiles"></a><span data-ttu-id="86b4e-167">Профили разноски</span><span class="sxs-lookup"><span data-stu-id="86b4e-167">Posting profiles</span></span>

1. <span data-ttu-id="86b4e-168">Перейти к **главная книга** \> **Настройка расходов будущих периодов** \> **Профили разноски**.</span><span class="sxs-lookup"><span data-stu-id="86b4e-168">Go to **General ledger** \> **Deferrals setup** \> **Posting profiles**.</span></span>
2. <span data-ttu-id="86b4e-169">На панели операций выберите **Новый** для создания профилей разноски для расходов будущих периодов.</span><span class="sxs-lookup"><span data-stu-id="86b4e-169">On the Action Pane, select **New** to create posting profiles for deferred expenses.</span></span>

    <span data-ttu-id="86b4e-170">В следующей таблице описаны общие поля на странице **Профили разноски расходов будущих периодов**.</span><span class="sxs-lookup"><span data-stu-id="86b4e-170">The following table describes the fields on the **Deferrals posting profiles** page.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="86b4e-171">Поле</span><span class="sxs-lookup"><span data-stu-id="86b4e-171">Field</span></span></th>
    <th><span data-ttu-id="86b4e-172">Описание</span><span class="sxs-lookup"><span data-stu-id="86b4e-172">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="86b4e-173">Профиль разноски</span><span class="sxs-lookup"><span data-stu-id="86b4e-173">Posting profile</span></span></td>
    <td><span data-ttu-id="86b4e-174">Введите имя профиля разноски.</span><span class="sxs-lookup"><span data-stu-id="86b4e-174">Enter a name for the posting profile.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-175">Описание</span><span class="sxs-lookup"><span data-stu-id="86b4e-175">Description</span></span></td>
    <td><span data-ttu-id="86b4e-176">Введите описание профиля разноски.</span><span class="sxs-lookup"><span data-stu-id="86b4e-176">Enter a description of the posting profile.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-177">Списание</span><span class="sxs-lookup"><span data-stu-id="86b4e-177">Writing off</span></span></td>
    <td><span data-ttu-id="86b4e-178">Выберите этот параметр для настройки счетов ГК, которые используются для списания стоимости актива.</span><span class="sxs-lookup"><span data-stu-id="86b4e-178">Select this option to set up ledger accounts that are used to write off the value of the asset.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-179">Выбытие</span><span class="sxs-lookup"><span data-stu-id="86b4e-179">Disposal</span></span></td>
    <td><span data-ttu-id="86b4e-180">Выберите этот параметр для настройки счетов ГК, которые используются для выбытия актива.</span><span class="sxs-lookup"><span data-stu-id="86b4e-180">Select this option to set up ledger accounts that are used to dispose of the asset.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-181">Приход</span><span class="sxs-lookup"><span data-stu-id="86b4e-181">Receipt</span></span></td>
    <td><span data-ttu-id="86b4e-182">Выберите этот параметр для настройки счетов ГК, которые используются для разнесения проводок прихода, связанных с расходами будущих периодов.</span><span class="sxs-lookup"><span data-stu-id="86b4e-182">Select this option to set up ledger accounts that are used to post receipt transactions for deferrals.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-183">Группировки</span><span class="sxs-lookup"><span data-stu-id="86b4e-183">Groupings</span></span></td>
    <td><span data-ttu-id="86b4e-184">Выберите метод группировки для профиля расходов будущих периодов:</span><span class="sxs-lookup"><span data-stu-id="86b4e-184">Select the grouping method for the deferred expense profile:</span></span> <ul>
    <li><span data-ttu-id="86b4e-185"><strong>Все</strong> — Поля <strong>Счет ГК</strong> и <strong>Корр.счет</strong> применимые для всех расходов будущих периодов.</span><span class="sxs-lookup"><span data-stu-id="86b4e-185"><strong>All</strong> – The <strong>Main account</strong> and <strong>Offset account</strong> fields are applicable to all deferrals.</span></span></li>
    <li><span data-ttu-id="86b4e-186"><strong>Модель стоимости</strong> — Поля <strong>Счет ГК</strong> и <strong>Корр.счет</strong>, применимые к модели стоимости, выбранной в поле <strong>Номер счета/группы</strong>.</span><span class="sxs-lookup"><span data-stu-id="86b4e-186"><strong>Value model</strong> – The <strong>Main account</strong> and <strong>Offset account</strong> fields are applicable to the value model that is selected in the <strong>Account/Group number</strong> field.</span></span></li>
    <li><span data-ttu-id="86b4e-187"><strong>Группа</strong> — Поля <strong>Счет ГК</strong> и <strong>Корр.счет</strong>, применимые к группе расходов будущих периодов, выбранной в поле <strong>Номер счета/группы</strong>.</span><span class="sxs-lookup"><span data-stu-id="86b4e-187"><strong>Group</strong> – The <strong>Main account</strong> and <strong>Offset account</strong> fields are applicable to the deferrals group that is selected in the <strong>Account/Group number</strong> field.</span></span></li>
    <li><span data-ttu-id="86b4e-188"><strong>Таблица</strong> — Поля <strong>Счет ГК</strong> и <strong>Корр.счет</strong>, применимые к расходу будущих периодов, выбранному в поле <strong>Номер счета/группы</strong>.</span><span class="sxs-lookup"><span data-stu-id="86b4e-188"><strong>Table</strong> – The <strong>Main account</strong> and <strong>Offset account</strong> fields are applicable to the deferral that is selected in the <strong>Account/Group number</strong> field.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-189">Номер счета/группы</span><span class="sxs-lookup"><span data-stu-id="86b4e-189">Account/Group number</span></span></td>
    <td><span data-ttu-id="86b4e-190">Выберите модель стоимости, группу расходов будущих периодов или расход будущих периодов, в зависимости от значения, выбранного в поле <strong>Группировки</strong>.</span><span class="sxs-lookup"><span data-stu-id="86b4e-190">Select a value model, deferrals group, or deferral, depending on the value that you selected in the <strong>Groupings</strong> field.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-191">Счет ГК</span><span class="sxs-lookup"><span data-stu-id="86b4e-191">Main account</span></span></td>
    <td><span data-ttu-id="86b4e-192">Выберите счет ГК для разноски списания или удаления расходов будущих периодов.</span><span class="sxs-lookup"><span data-stu-id="86b4e-192">Select the main account for write-off posting or deferred expense disposal.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-193">Корр. счет</span><span class="sxs-lookup"><span data-stu-id="86b4e-193">Offset account</span></span></td>
    <td><span data-ttu-id="86b4e-194">Выберите корр.счет для разноски списания или удаления расходов будущих периодов.</span><span class="sxs-lookup"><span data-stu-id="86b4e-194">Select the offset account for write-off posting or deferred expense disposal.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-195">Сумма к разноске</span><span class="sxs-lookup"><span data-stu-id="86b4e-195">Post value</span></span></td>
    <td><span data-ttu-id="86b4e-196">Выбор значения для разноски:</span><span class="sxs-lookup"><span data-stu-id="86b4e-196">Select the value to post:</span></span> <ul>
    <li><span data-ttu-id="86b4e-197">Оставшаяся сумма</span><span class="sxs-lookup"><span data-stu-id="86b4e-197">Remaining amount</span></span></li>
    <li><span data-ttu-id="86b4e-198">Первоначальная сумма</span><span class="sxs-lookup"><span data-stu-id="86b4e-198">Initial amount</span></span></li>
    <li><span data-ttu-id="86b4e-199">Списанная сумма</span><span class="sxs-lookup"><span data-stu-id="86b4e-199">Amount written off</span></span></li>
    </ul>
    <p><span data-ttu-id="86b4e-200"><strong>Примечание:</strong> Это поле доступно только в том случае, если выбрано значение <strong>Выбытие</strong>.</span><span class="sxs-lookup"><span data-stu-id="86b4e-200"><strong>Note:</strong> This field is available only if you select the <strong>Disposal</strong> option.</span></span></p>
    </td>
    </tr>
    </tbody>
    </table>

![Страница профилей разноски расходов будущих периодов](media/rus-set-up-deferral-03.png)

## <a name="deferrals-groups"></a><span data-ttu-id="86b4e-202">Группы РБП</span><span class="sxs-lookup"><span data-stu-id="86b4e-202">Deferrals groups</span></span>

1. <span data-ttu-id="86b4e-203">Перейти к **главная книга** \> **Расходы будущих периодов** \> **Группы расходов будущих периодов**.</span><span class="sxs-lookup"><span data-stu-id="86b4e-203">Go to **General ledger** \> **Deferrals** \> **Deferrals groups**.</span></span>
2. <span data-ttu-id="86b4e-204">На панели операций выберите **Новый** для создания групп для расходов будущих периодов.</span><span class="sxs-lookup"><span data-stu-id="86b4e-204">On the Action Pane, select **New** to create groups for deferred expenses.</span></span>

    <span data-ttu-id="86b4e-205">В следующей таблице описаны общие поля на странице **Группы расходов будущих периодов**.</span><span class="sxs-lookup"><span data-stu-id="86b4e-205">The following table describes the fields on the **Deferrals groups** page.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="86b4e-206">Поле</span><span class="sxs-lookup"><span data-stu-id="86b4e-206">Field</span></span></th>
    <th><span data-ttu-id="86b4e-207">Описание</span><span class="sxs-lookup"><span data-stu-id="86b4e-207">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="86b4e-208">Группа расходов</span><span class="sxs-lookup"><span data-stu-id="86b4e-208">Deferrals group</span></span></td>
    <td><span data-ttu-id="86b4e-209">Введите идентификационный код для группы расходов будущих периодов.</span><span class="sxs-lookup"><span data-stu-id="86b4e-209">Enter the identification code for the deferrals group.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-210">Название</span><span class="sxs-lookup"><span data-stu-id="86b4e-210">Name</span></span></td>
    <td><span data-ttu-id="86b4e-211">Введите имя группы расходов будущих периодов.</span><span class="sxs-lookup"><span data-stu-id="86b4e-211">Enter the name of the deferrals group.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-212">Код модели</span><span class="sxs-lookup"><span data-stu-id="86b4e-212">Model number</span></span></td>
    <td><span data-ttu-id="86b4e-213">Выберите номер модели РБП.</span><span class="sxs-lookup"><span data-stu-id="86b4e-213">Select the deferral model number.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-214">Имя модели</span><span class="sxs-lookup"><span data-stu-id="86b4e-214">Model name</span></span></td>
    <td><span data-ttu-id="86b4e-215">Имя модели стоимости.</span><span class="sxs-lookup"><span data-stu-id="86b4e-215">The name of the value model.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-216">Метод списания</span><span class="sxs-lookup"><span data-stu-id="86b4e-216">Writing off method</span></span></td>
    <td><span data-ttu-id="86b4e-217">Выберите метода списания для расходов будущих периодов.</span><span class="sxs-lookup"><span data-stu-id="86b4e-217">Select the write-off method for the deferrals.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-218">Срок списания</span><span class="sxs-lookup"><span data-stu-id="86b4e-218">Writing off time</span></span></td>
    <td><span data-ttu-id="86b4e-219">Введите период списания для расходов будущих периодов.</span><span class="sxs-lookup"><span data-stu-id="86b4e-219">Enter the write-off period for the deferrals.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-220">Дата начала списания</span><span class="sxs-lookup"><span data-stu-id="86b4e-220">Beginning date of writing off</span></span></td>
    <td><span data-ttu-id="86b4e-221">Выберите начальную дату для списания.</span><span class="sxs-lookup"><span data-stu-id="86b4e-221">Select the start date for the write-off.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-222">Дата выбытия</span><span class="sxs-lookup"><span data-stu-id="86b4e-222">Disposal date</span></span></td>
    <td><span data-ttu-id="86b4e-223">Выберите дату выбытия.</span><span class="sxs-lookup"><span data-stu-id="86b4e-223">Select the date of disposal.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-224">Профиль разноски</span><span class="sxs-lookup"><span data-stu-id="86b4e-224">Posting profile</span></span></td>
    <td><span data-ttu-id="86b4e-225">Выбор профиль разноски для проводок.</span><span class="sxs-lookup"><span data-stu-id="86b4e-225">Select the posting profile for the transactions.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-226">Метод зачета НДС по РБП</span><span class="sxs-lookup"><span data-stu-id="86b4e-226">VAT offset method for deferrals</span></span></td>
    <td><span data-ttu-id="86b4e-227">Выберите метод вычета налога на добавленную стоимость (НДС) для расходов будущих периодов:</span><span class="sxs-lookup"><span data-stu-id="86b4e-227">Select the value-added tax (VAT) deduction method for deferrals:</span></span> <ul>
    <li><span data-ttu-id="86b4e-228"><strong>Стандарт</strong> — используйте стандартный метод вычета НДС для обработки входящего НДС для счетов-фактур, связанных с расходами будущих периодов.</span><span class="sxs-lookup"><span data-stu-id="86b4e-228"><strong>Standard</strong> – Use the standard VAT deduction method to process incoming VAT for factures that are related to deferrals.</span></span></li>
    <li><span data-ttu-id="86b4e-229"><strong>Пропорциональный</strong> — используйте пропорциональный метод вычета НДС для обработки входящего НДС для счетов-фактур, связанных с расходами будущих периодов.</span><span class="sxs-lookup"><span data-stu-id="86b4e-229"><strong>Proportionate</strong> – Use the proportional VAT deduction method to process incoming VAT for factures that are related to deferrals.</span></span></li>
    </ul>
    </td>
    </tr>
    </tbody>
    </table>

<span data-ttu-id="86b4e-230">Настраиваемая группа расходов будущих периодов имеет отношение «один к одному» (1:1) к модели стоимости, связанной с настройкой профилей разнесения.</span><span class="sxs-lookup"><span data-stu-id="86b4e-230">The deferrals group that is set up has a one-to-one (1:1) relation to value model that is related to the posting profiles setup.</span></span>

![Страница групп расходов будущих периодов](media/rus-set-up-deferral-04.png)

## <a name="sequence-of-calculation"></a><span data-ttu-id="86b4e-232">Последовательности расчета</span><span class="sxs-lookup"><span data-stu-id="86b4e-232">Sequence of calculation</span></span>

<span data-ttu-id="86b4e-233">Для создания последовательностей расчета, используемых для создания расходов будущих периодов для накладных поставщика, используйте страницы **Нормативные расходы — последовательности** и **Настройка счетчиков**.</span><span class="sxs-lookup"><span data-stu-id="86b4e-233">You use the **Standard expenses sequence** and **Counter setup** pages to create calculation sequences that are used to create deferrals for vendor invoices.</span></span>

> [!NOTE]
> <span data-ttu-id="86b4e-234">Прежде чем настроить последовательность расчетов и счетчики, необходимо настроить коды расходов на странице **Коды расходов и доходов**.</span><span class="sxs-lookup"><span data-stu-id="86b4e-234">Before you can set up the calculation sequence and counters, you must set up expense codes on the **Expense and income codes** page.</span></span>

1. <span data-ttu-id="86b4e-235">Перейти к **главная книга** \> **Настройка расходов будущих периодов** \> **Последовательность расчета**.</span><span class="sxs-lookup"><span data-stu-id="86b4e-235">Go to **General ledger** \> **Deferrals setup** \> **Sequence of calculation**.</span></span>
2. <span data-ttu-id="86b4e-236">На панели операций выберите **Новый** для настройки последовательности расчета доходов или расходов.</span><span class="sxs-lookup"><span data-stu-id="86b4e-236">On the Action Pane, select **New** to set up revenue or expense calculation sequences.</span></span>

    <span data-ttu-id="86b4e-237">В следующей таблице описаны общие поля на странице **Нормативные расходы — последовательности**.</span><span class="sxs-lookup"><span data-stu-id="86b4e-237">The following table describes the fields on the **Standard expenses sequence** page.</span></span>

    | <span data-ttu-id="86b4e-238">Поле</span><span class="sxs-lookup"><span data-stu-id="86b4e-238">Field</span></span>             | <span data-ttu-id="86b4e-239">Описание</span><span class="sxs-lookup"><span data-stu-id="86b4e-239">Description</span></span>                                                             |
    |-------------------|-------------------------------------------------------------------------|
    | <span data-ttu-id="86b4e-240">Последовательность</span><span class="sxs-lookup"><span data-stu-id="86b4e-240">Sequence</span></span>          | <span data-ttu-id="86b4e-241">Введите порядковый номер.</span><span class="sxs-lookup"><span data-stu-id="86b4e-241">Enter the sequence number.</span></span>                                              |
    | <span data-ttu-id="86b4e-242">Описание</span><span class="sxs-lookup"><span data-stu-id="86b4e-242">Description</span></span>       | <span data-ttu-id="86b4e-243">Ввод описания последовательности расчета.</span><span class="sxs-lookup"><span data-stu-id="86b4e-243">Enter a description of the calculation sequence.</span></span>                        |
    | <span data-ttu-id="86b4e-244">Канал</span><span class="sxs-lookup"><span data-stu-id="86b4e-244">Channel</span></span>           | <span data-ttu-id="86b4e-245">Выберите выходной формат расхода будущего периода для результатов расчета.</span><span class="sxs-lookup"><span data-stu-id="86b4e-245">Select the deferral output format for the calculation results.</span></span>          |
    | <span data-ttu-id="86b4e-246">Ссылка на канал</span><span class="sxs-lookup"><span data-stu-id="86b4e-246">Channel reference</span></span> | <span data-ttu-id="86b4e-247">Выберите группу расходов будущих периодов для записи результатов расчета.</span><span class="sxs-lookup"><span data-stu-id="86b4e-247">Select the deferred expense group to record the calculation results to.</span></span> |

    ![Страница «Нормативные расходы — последовательности»](media/rus-set-up-deferral-05.png)

3. <span data-ttu-id="86b4e-249">На панели операций выберите **Счетчики**, чтобы открыть страницу **Настройка счетчиков**.</span><span class="sxs-lookup"><span data-stu-id="86b4e-249">On the Action Pane, select **Counters** to open the **Counter setup** page.</span></span>
4. <span data-ttu-id="86b4e-250">На панели операций выберите **Новый** для создания счетчиков для последовательность расчета.</span><span class="sxs-lookup"><span data-stu-id="86b4e-250">On the Action Pane, select **New** to create counters for the calculation sequence.</span></span>

    <span data-ttu-id="86b4e-251">В следующей таблице описаны поля на странице **Настройка счетчиков**.</span><span class="sxs-lookup"><span data-stu-id="86b4e-251">The following table describes the fields on the **Counter setup** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="86b4e-252">Необходимо выбрать код расхода.</span><span class="sxs-lookup"><span data-stu-id="86b4e-252">You must select an expense code.</span></span> <span data-ttu-id="86b4e-253">При использовании периодической обработки для генерации расходов будущего периода, код расхода, определенный для счетчика, используется для создания расходов будущего периода для накладных поставщика с таким же кодом расхода.</span><span class="sxs-lookup"><span data-stu-id="86b4e-253">When you use the periodic process to generate deferrals, the expense code that is specified for a counter is used to generate deferrals for vendor invoices that have the same expense code.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="86b4e-254">Поле</span><span class="sxs-lookup"><span data-stu-id="86b4e-254">Field</span></span></th>
    <th><span data-ttu-id="86b4e-255">Описание</span><span class="sxs-lookup"><span data-stu-id="86b4e-255">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="86b4e-256">Последовательность</span><span class="sxs-lookup"><span data-stu-id="86b4e-256">Sequence</span></span></td>
    <td><span data-ttu-id="86b4e-257">Выберите код последовательности расчета.</span><span class="sxs-lookup"><span data-stu-id="86b4e-257">Select the calculation sequence code.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-258">Описание</span><span class="sxs-lookup"><span data-stu-id="86b4e-258">Description</span></span></td>
    <td><span data-ttu-id="86b4e-259">Введите имя для счетчика.</span><span class="sxs-lookup"><span data-stu-id="86b4e-259">Enter a name for the counter.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-260">Код расходов</span><span class="sxs-lookup"><span data-stu-id="86b4e-260">Expense code</span></span></td>
    <td><span data-ttu-id="86b4e-261">Выберите код расхода.</span><span class="sxs-lookup"><span data-stu-id="86b4e-261">Select an expense code.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-262">Описание</span><span class="sxs-lookup"><span data-stu-id="86b4e-262">Description</span></span></td>
    <td><span data-ttu-id="86b4e-263">Описание кода расхода.</span><span class="sxs-lookup"><span data-stu-id="86b4e-263">The description of the expense code.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-264">Номер строки</span><span class="sxs-lookup"><span data-stu-id="86b4e-264">Line number</span></span></td>
    <td><span data-ttu-id="86b4e-265">Введите уникальный номер строки.</span><span class="sxs-lookup"><span data-stu-id="86b4e-265">Enter a unique line number.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-266">Оператор</span><span class="sxs-lookup"><span data-stu-id="86b4e-266">Operator</span></span></td>
    <td><span data-ttu-id="86b4e-267">Выберите математического или логический оператор для последовательности расчета:</span><span class="sxs-lookup"><span data-stu-id="86b4e-267">Select the mathematical or logical operator for the calculation sequence:</span></span> <ul>
    <li><span data-ttu-id="86b4e-268"><strong>+ (знак «плюс»)</strong> — Добавление значений в диапазоне, определяемом полями <strong>От</strong> и <strong>До</strong> для типа строки, выбранного в поле <strong>Тип строки</strong>.</span><span class="sxs-lookup"><span data-stu-id="86b4e-268"><strong>+ (plus sign)</strong> – Add the values in the range that is defined by the <strong>From</strong> and <strong>To</strong> fields for the line type that is selected in the <strong>Line type</strong> field.</span></span> <span data-ttu-id="86b4e-269">Полученное значение используется для последовательности расчета.</span><span class="sxs-lookup"><span data-stu-id="86b4e-269">The resulting value is used for the calculation sequence.</span></span></li>
    <li><span data-ttu-id="86b4e-270"><strong>– (знак «минус»)</strong> — Вычитание значений в диапазоне, определяемом полями <strong>От</strong> и <strong>До</strong> для типа строки, выбранного в поле <strong>Тип строки</strong>.</span><span class="sxs-lookup"><span data-stu-id="86b4e-270"><strong>– (minus sign)</strong> – Subtract the values in the range that is defined by the <strong>From</strong> and <strong>To</strong> fields for the line type that is selected in the <strong>Line type</strong> field.</span></span> <span data-ttu-id="86b4e-271">Полученное значение используется для последовательности расчета.</span><span class="sxs-lookup"><span data-stu-id="86b4e-271">The resulting value is used for the calculation sequence.</span></span></li>
    <li><span data-ttu-id="86b4e-272"><strong>\* (знак «звездочка»)</strong> — Умножение значений в диапазоне, определяемом полями <strong>От</strong> и <strong>До</strong> для типа строки, выбранного в поле <strong>Тип строки</strong>.</span><span class="sxs-lookup"><span data-stu-id="86b4e-272"><strong>\* (asterisk)</strong> – Multiply the values in the range that is defined by the <strong>From</strong> and <strong>To</strong> fields for the line type that is selected in the <strong>Line type</strong> field.</span></span> <span data-ttu-id="86b4e-273">Полученное значение используется для последовательности расчета.</span><span class="sxs-lookup"><span data-stu-id="86b4e-273">The resulting value is used for the calculation sequence.</span></span></li>
    <li><span data-ttu-id="86b4e-274"><strong>/ (знак «косая черта»)</strong> — Деление значений в диапазоне, определяемом полями <strong>От</strong> и <strong>До</strong> для типа строки, выбранного в поле <strong>Тип строки</strong>.</span><span class="sxs-lookup"><span data-stu-id="86b4e-274"><strong>/ (slash)</strong> – Divide the values in the range that is defined by the <strong>From</strong> and <strong>To</strong> fields for the line type that is selected in the <strong>Line type</strong> field.</span></span> <span data-ttu-id="86b4e-275">Полученное значение используется для последовательности расчета.</span><span class="sxs-lookup"><span data-stu-id="86b4e-275">The resulting value is used for the calculation sequence.</span></span></li>
    <li><span data-ttu-id="86b4e-276"><strong>Мин.</strong> — Используйте минимальное значение в диапазоне, определяемом полями <strong>От</strong> и <strong>До</strong> для типа строки, выбранного в поле <strong>Тип строки</strong> для последовательности расчета.</span><span class="sxs-lookup"><span data-stu-id="86b4e-276"><strong>Min</strong> – Use the minimum value in the range that is defined by the <strong>From</strong> and <strong>To</strong> fields for the line type that is selected in the <strong>Line type</strong> field for the calculation sequence.</span></span></li>
    <li><span data-ttu-id="86b4e-277"><strong>Макс.</strong> — Используйте максимальное значение в диапазоне, определяемом полями <strong>От</strong> и <strong>До</strong> для типа строки, выбранного в поле <strong>Тип строки</strong> для последовательности расчета.</span><span class="sxs-lookup"><span data-stu-id="86b4e-277"><strong>Max</strong> – Use the maximum value in the range that is defined by the <strong>From</strong> and <strong>To</strong> fields for the line type that is selected in the <strong>Line type</strong> field for the calculation sequence.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-278">Tип строки</span><span class="sxs-lookup"><span data-stu-id="86b4e-278">Line type</span></span></td>
    <td><span data-ttu-id="86b4e-279">Выберите тип строки.</span><span class="sxs-lookup"><span data-stu-id="86b4e-279">Select a line type.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-280">Списание</span><span class="sxs-lookup"><span data-stu-id="86b4e-280">From</span></span></td>
    <td><span data-ttu-id="86b4e-281">Выберите первое значение в диапазоне значений, используемых для последовательности расчета.</span><span class="sxs-lookup"><span data-stu-id="86b4e-281">Select the first value in the range of values that is used for the calculation sequence.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-282">Зачисление</span><span class="sxs-lookup"><span data-stu-id="86b4e-282">To</span></span></td>
    <td><span data-ttu-id="86b4e-283">Выберите последнее значение в диапазоне значений, используемых для последовательности расчета.</span><span class="sxs-lookup"><span data-stu-id="86b4e-283">Select the last value in the range of values that is used for the calculation sequence.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-284">Поле регистра</span><span class="sxs-lookup"><span data-stu-id="86b4e-284">Register field</span></span></td>
    <td><span data-ttu-id="86b4e-285">Выберите поле регистра для использования для последовательности расчета.</span><span class="sxs-lookup"><span data-stu-id="86b4e-285">Select the register field to use for the calculation sequence.</span></span>
    <p><span data-ttu-id="86b4e-286"><strong>Примечание:</strong> Это поле доступно только в том случае, если выбрано значение <strong>Регистр</strong> в поле <strong>Канал</strong> на странице <strong>Нормативные расходы — последовательности</strong>.</span><span class="sxs-lookup"><span data-stu-id="86b4e-286"><strong>Note:</strong> This field is available only if you selected <strong>Register</strong> in the <strong>Channel</strong> field on the <strong>Standard expenses sequence</strong> page.</span></span></p>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-287">Поле таблицы</span><span class="sxs-lookup"><span data-stu-id="86b4e-287">Table field</span></span></td>
    <td><span data-ttu-id="86b4e-288">Выберите поле таблицы.</span><span class="sxs-lookup"><span data-stu-id="86b4e-288">Select a table field.</span></span>
    <p><span data-ttu-id="86b4e-289"><strong>Примечание:</strong> Это поле доступно только в том случае, если выбрано значение <strong>Коэффициент</strong> в поле <strong>Канал</strong> на странице <strong>Нормативные расходы — последовательности</strong>.</span><span class="sxs-lookup"><span data-stu-id="86b4e-289"><strong>Note:</strong> This field is available only if you selected <strong>Ratio</strong> in the <strong>Channel</strong> field on the <strong>Standard expenses sequence</strong> page.</span></span></p>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-290">FieldID</span><span class="sxs-lookup"><span data-stu-id="86b4e-290">Field ID</span></span></td>
    <td><span data-ttu-id="86b4e-291">Идентификационный номер поля регистра.</span><span class="sxs-lookup"><span data-stu-id="86b4e-291">The identification number of the register field.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-292">Примечание</span><span class="sxs-lookup"><span data-stu-id="86b4e-292">Note</span></span></td>
    <td><span data-ttu-id="86b4e-293">Введите необязательный комментарий о настройке счетчика.</span><span class="sxs-lookup"><span data-stu-id="86b4e-293">Enter an optional comment about the counter setup.</span></span></td>
    </tr>
    </tbody>
    </table>

    ![Страница настройки счетчиков](media/rus-set-up-deferral-06.png)

5. <span data-ttu-id="86b4e-295">Чтобы скопировать настройки счетчика от одной последовательности расчета в другую, на панели операций выберите **Копирование счетчика**, чтобы открыть диалоговое окно **Копирование прохода**.</span><span class="sxs-lookup"><span data-stu-id="86b4e-295">To copy the counter settings from one calculation sequence to another, on the Action Pane, select **Copy counter** to open the **Copy aisle** dialog box.</span></span>

    <span data-ttu-id="86b4e-296">Следующая таблица описывает поля в диалоговом окне **Копирование прохода**.</span><span class="sxs-lookup"><span data-stu-id="86b4e-296">The following table describes the fields in the **Copy aisle** dialog box.</span></span>

    | <span data-ttu-id="86b4e-297">Поле</span><span class="sxs-lookup"><span data-stu-id="86b4e-297">Field</span></span>                                       | <span data-ttu-id="86b4e-298">Описание</span><span class="sxs-lookup"><span data-stu-id="86b4e-298">Description</span></span>                                                |
    |---------------------------------------------|------------------------------------------------------------|
    | <span data-ttu-id="86b4e-299">Последовательность (в разделе **Копировать из**)</span><span class="sxs-lookup"><span data-stu-id="86b4e-299">Sequence (in the **Copy from** section)</span></span>     | <span data-ttu-id="86b4e-300">Выберите последовательность, из которой вы хотите скопировать настройки счетчика.</span><span class="sxs-lookup"><span data-stu-id="86b4e-300">Select the sequence to copy the counter settings from.</span></span>     |
    | <span data-ttu-id="86b4e-301">Код расхода (в разделе **Копировать из**)</span><span class="sxs-lookup"><span data-stu-id="86b4e-301">Expense code (in the **Copy from** section)</span></span> | <span data-ttu-id="86b4e-302">Выберите код расхода, из которого вы хотите скопировать настройки счетчика.</span><span class="sxs-lookup"><span data-stu-id="86b4e-302">Select the expense code to copy the counter settings from.</span></span> |
    | <span data-ttu-id="86b4e-303">Последовательность (в разделе **Копировать в**)</span><span class="sxs-lookup"><span data-stu-id="86b4e-303">Sequence (in the **Copy to** section)</span></span>       | <span data-ttu-id="86b4e-304">Выберите последовательность, в которую вы хотите скопировать настройки счетчика.</span><span class="sxs-lookup"><span data-stu-id="86b4e-304">Select the sequence to copy the counter settings to.</span></span>       |
    | <span data-ttu-id="86b4e-305">Код расхода (в разделе **Копировать в**)</span><span class="sxs-lookup"><span data-stu-id="86b4e-305">Expense code (in the **Copy to** section)</span></span>   | <span data-ttu-id="86b4e-306">Выберите код расхода, в который вы хотите скопировать настройки счетчика.</span><span class="sxs-lookup"><span data-stu-id="86b4e-306">Select the expense code to copy the counter settings to.</span></span>   |

## <a name="general-ledger-parameters"></a><span data-ttu-id="86b4e-307">Параметры главной книги</span><span class="sxs-lookup"><span data-stu-id="86b4e-307">General ledger parameters</span></span>

1. <span data-ttu-id="86b4e-308">Перейдите в раздел **Главная книга** \> **Настройка главной книги** \> **Параметры главной книги**.</span><span class="sxs-lookup"><span data-stu-id="86b4e-308">Go to **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span>
2. <span data-ttu-id="86b4e-309">На вкладке **Расходы будущих периодов** задайте поля, используя информацию в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="86b4e-309">On the **Deferrals** tab, set the fields by using the information in the following table.</span></span>

    | <span data-ttu-id="86b4e-310">Поле</span><span class="sxs-lookup"><span data-stu-id="86b4e-310">Field</span></span>                           | <span data-ttu-id="86b4e-311">Описание</span><span class="sxs-lookup"><span data-stu-id="86b4e-311">Description</span></span> |
    |---------------------------------|-------------|
    | <span data-ttu-id="86b4e-312">Профиль разноски</span><span class="sxs-lookup"><span data-stu-id="86b4e-312">Posting profile</span></span>                 | <span data-ttu-id="86b4e-313">Выберите профиль разноски, который используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="86b4e-313">Select the posting profile that is used by default.</span></span> <span data-ttu-id="86b4e-314">Профиль разноски отображается автоматически в ваучере расхода будущего периода при его регистрации.</span><span class="sxs-lookup"><span data-stu-id="86b4e-314">The posting profile is automatically shown on the deferral voucher when it's registered.</span></span> |
    | <span data-ttu-id="86b4e-315">Округление</span><span class="sxs-lookup"><span data-stu-id="86b4e-315">Round-off</span></span>                       | <span data-ttu-id="86b4e-316">Определите сумму округления по умолчанию для методов списания расходов будущего периода.</span><span class="sxs-lookup"><span data-stu-id="86b4e-316">Define the default round-off amount for the deferral write-off methods.</span></span> <span data-ttu-id="86b4e-317">Например, если ввести **0,01**, значения округляются до двух десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="86b4e-317">For example, if you enter **0.01**, values are rounded to two decimal places.</span></span> |
    | <span data-ttu-id="86b4e-318">Код расходов и доходов</span><span class="sxs-lookup"><span data-stu-id="86b4e-318">Expense and income code</span></span>         | <span data-ttu-id="86b4e-319">Выберите коды расходов и доходов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="86b4e-319">Select default expense and income codes.</span></span> |
    | <span data-ttu-id="86b4e-320">Рабочий</span><span class="sxs-lookup"><span data-stu-id="86b4e-320">Worker</span></span>                          | <span data-ttu-id="86b4e-321">Выберите работника по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="86b4e-321">Select a default worker.</span></span> |
    | <span data-ttu-id="86b4e-322">Базовая модель учета</span><span class="sxs-lookup"><span data-stu-id="86b4e-322">Base value model</span></span>                | <span data-ttu-id="86b4e-323">Выберите модель стоимости по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="86b4e-323">Select a default value model.</span></span> |
    | <span data-ttu-id="86b4e-324">Метод зачета НДС по РБП</span><span class="sxs-lookup"><span data-stu-id="86b4e-324">VAT offset method for deferrals</span></span> | <span data-ttu-id="86b4e-325">Выберите метод компенсации НДС по умолчанию для расходов будущего периода.</span><span class="sxs-lookup"><span data-stu-id="86b4e-325">Select a default VAT offset method for deferrals.</span></span> |

    ![Вкладка расходов будущего периода на странице параметров главной книги](media/rus-set-up-deferral-07.png)

3. <span data-ttu-id="86b4e-327">На вкладке **Номерные серии** в поле **Код номерной серии** выберите код номерной серии для ссылки **Идентификатор расхода будущего периода**.</span><span class="sxs-lookup"><span data-stu-id="86b4e-327">On the **Number sequences** tab, in the **Number sequence code** field, select the number sequence code for the **Deferral ID** reference.</span></span>

    ![Вкладка «Номерные серии» на странице параметров главной книги](media/rus-set-up-deferral-08.png)

4. <span data-ttu-id="86b4e-329">Перейдите в раздел **Главная книга** \> **Настройка журнала** \> **Наименования журналов**.</span><span class="sxs-lookup"><span data-stu-id="86b4e-329">Go to **General ledger** \> **Journal setup** \> **Journal names**.</span></span>
5. <span data-ttu-id="86b4e-330">На панели операций выберите **Новый** для создания журнала типа **Расходы будущих периодов** для работы с расходами будущих периодов.</span><span class="sxs-lookup"><span data-stu-id="86b4e-330">On the Action Pane, select **New** to create a journal of the **Deferrals** type to work with deferrals.</span></span>
6. <span data-ttu-id="86b4e-331">В поле **Имя** введите имя журнала.</span><span class="sxs-lookup"><span data-stu-id="86b4e-331">In the **Name** field, enter the name of the journal.</span></span>
7. <span data-ttu-id="86b4e-332">В поле **Описание** введите краткое описание журнала.</span><span class="sxs-lookup"><span data-stu-id="86b4e-332">In the **Description** field, enter a short description of the journal.</span></span>
8. <span data-ttu-id="86b4e-333">В поле **Тип журнала** выберите **Расходы будущих периодов**.</span><span class="sxs-lookup"><span data-stu-id="86b4e-333">In the **Journal type** field, select **Deferrals**.</span></span>
9. <span data-ttu-id="86b4e-334">В поле **Серия операций** выберите номерную серию, используемую для нумерации операций.</span><span class="sxs-lookup"><span data-stu-id="86b4e-334">In the **Voucher series** field, select the number sequence that is used for voucher numbering.</span></span>

    ![Страница наименований журналов](media/rus-set-up-deferral-09.png)

## <a name="deferrals"></a><span data-ttu-id="86b4e-336">РБП</span><span class="sxs-lookup"><span data-stu-id="86b4e-336">Deferrals</span></span>

<span data-ttu-id="86b4e-337">Расходы будущих периодов могут быть созданы вручную, или они могут быть автоматически сгенерированы с помощью периодической операции.</span><span class="sxs-lookup"><span data-stu-id="86b4e-337">Deferrals can be created manually, or they can be automatically generated by using a periodic operation.</span></span> <span data-ttu-id="86b4e-338">Для получения дополнительной информации о том, как создать расход будущего периода, см. [Создание расходов будущих периодов (Россия)](rus-create-generate-deferrals.md).</span><span class="sxs-lookup"><span data-stu-id="86b4e-338">For more information about how to create a deferral, see [Create or generate deferrals (Russia)](rus-create-generate-deferrals.md).</span></span>

1. <span data-ttu-id="86b4e-339">Перейти к **главная книга** \> **Расходы будущих периодов** \> **Расходы будущих периодов**.</span><span class="sxs-lookup"><span data-stu-id="86b4e-339">Go to **General ledger** \> **Deferrals** \> **Deferrals**.</span></span>
2. <span data-ttu-id="86b4e-340">Страницу **Расходы будущих периодов** можно использовать для создания расходов будущих периодов или для просмотра и работы с расходами будущих периодов.</span><span class="sxs-lookup"><span data-stu-id="86b4e-340">You can use the **Deferrals** page to manually create deferrals, or to review and work with deferrals.</span></span>

    <span data-ttu-id="86b4e-341">В следующей таблице описаны поля на странице **Расходы будущих периодов**.</span><span class="sxs-lookup"><span data-stu-id="86b4e-341">The following table describes the fields on the **Deferrals** page.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="86b4e-342">Поле</span><span class="sxs-lookup"><span data-stu-id="86b4e-342">Field</span></span></th>
    <th><span data-ttu-id="86b4e-343">Описание</span><span class="sxs-lookup"><span data-stu-id="86b4e-343">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="86b4e-344">Идентификатор расхода</span><span class="sxs-lookup"><span data-stu-id="86b4e-344">Deferral ID</span></span></td>
    <td><span data-ttu-id="86b4e-345">Идентификационный код для РБП.</span><span class="sxs-lookup"><span data-stu-id="86b4e-345">The identification code for the deferral.</span></span> <span data-ttu-id="86b4e-346">Этот код обновляется в соответствии с настроенной номерной серией.</span><span class="sxs-lookup"><span data-stu-id="86b4e-346">This code is updated according to the configured number sequence.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-347">Название</span><span class="sxs-lookup"><span data-stu-id="86b4e-347">Name</span></span></td>
    <td><span data-ttu-id="86b4e-348">Введите имя расхода будущего периода.</span><span class="sxs-lookup"><span data-stu-id="86b4e-348">Enter a name for the deferral.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-349">Комментарий</span><span class="sxs-lookup"><span data-stu-id="86b4e-349">Comment</span></span></td>
    <td><span data-ttu-id="86b4e-350">Введите подробное описание расхода будущего периода.</span><span class="sxs-lookup"><span data-stu-id="86b4e-350">Enter a detailed description of the deferral.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-351">Дата вложения</span><span class="sxs-lookup"><span data-stu-id="86b4e-351">Date attached</span></span></td>
    <td><span data-ttu-id="86b4e-352">Выберите дату создания расхода будущего периода.</span><span class="sxs-lookup"><span data-stu-id="86b4e-352">Select the creation date of the deferral.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-353">Имя таблицы</span><span class="sxs-lookup"><span data-stu-id="86b4e-353">Table name</span></span></td>
    <td><span data-ttu-id="86b4e-354">Имя таблицы, из которой берутся исходные данные для создания расхода будущего периода.</span><span class="sxs-lookup"><span data-stu-id="86b4e-354">The name of the table that provides the source data that is used to generate the deferral.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-355">Справка</span><span class="sxs-lookup"><span data-stu-id="86b4e-355">Reference</span></span></td>
    <td><span data-ttu-id="86b4e-356">Идентификатор таблицы данных, из которой берутся исходные данные для создания расхода будущего периода.</span><span class="sxs-lookup"><span data-stu-id="86b4e-356">The identifier of the data table that provides the source data that is used to generate the deferral.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-357">Код расходов</span><span class="sxs-lookup"><span data-stu-id="86b4e-357">Expense code</span></span></td>
    <td><span data-ttu-id="86b4e-358">Выберите код расхода для расхода будущего периода.</span><span class="sxs-lookup"><span data-stu-id="86b4e-358">Select the expense code for the deferral.</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="86b4e-359">Метод зачета НДС по РБП</span><span class="sxs-lookup"><span data-stu-id="86b4e-359">VAT offset method for deferrals</span></span></td>
    <td><span data-ttu-id="86b4e-360">Выберите метод вычета НДС для расходов будущих периодов:</span><span class="sxs-lookup"><span data-stu-id="86b4e-360">Select the VAT deduction method for deferrals:</span></span> <ul>
    <li><span data-ttu-id="86b4e-361"><strong>Стандарт</strong> — обработка входящего НДС для счетов-фактур, связанных с расходами будущих периодов с использованием стандартного метода вычета НДС.</span><span class="sxs-lookup"><span data-stu-id="86b4e-361"><strong>Standard</strong> – Process the incoming VAT for factures that are related to deferrals by using the standard VAT deduction method.</span></span></li>
    <li><span data-ttu-id="86b4e-362"><strong>Пропорциональный</strong> — обработка входящего НДС для счетов-фактур, связанных с расходами будущих периодов с использованием пропорционального метода вычета НДС.</span><span class="sxs-lookup"><span data-stu-id="86b4e-362"><strong>Proportionate</strong> – Process the incoming VAT for factures that are related to deferrals by using the proportional VAT deduction method.</span></span></li>
    </ul>
    </td>
    </tr>
    </tbody>
    </table>

    <span data-ttu-id="86b4e-363">В следующей таблице описаны кнопки на панели операций страницы **Расходы будущих периодов**.</span><span class="sxs-lookup"><span data-stu-id="86b4e-363">The following table describes the buttons on the Action Pane of the **Deferrals** page.</span></span>

    | <span data-ttu-id="86b4e-364">Кнопка</span><span class="sxs-lookup"><span data-stu-id="86b4e-364">Button</span></span>           | <span data-ttu-id="86b4e-365">Описание</span><span class="sxs-lookup"><span data-stu-id="86b4e-365">Description</span></span>                                                             |
    |------------------|-------------------------------------------------------------------------|
    | <span data-ttu-id="86b4e-366">Копировать РБП</span><span class="sxs-lookup"><span data-stu-id="86b4e-366">Copy deferral</span></span>    | <span data-ttu-id="86b4e-367">Создайте расход будущего периода, идентичный выбранному расходу будущего периода.</span><span class="sxs-lookup"><span data-stu-id="86b4e-367">Create a deferral that is identical to the selected deferral.</span></span>           |
    | <span data-ttu-id="86b4e-368">Модели учета расходов будущих периодов</span><span class="sxs-lookup"><span data-stu-id="86b4e-368">Deferrals models</span></span> | <span data-ttu-id="86b4e-369">Определите модели расходов будущих периодов для выбранного расхода будущего периода.</span><span class="sxs-lookup"><span data-stu-id="86b4e-369">Define deferrals models for the selected deferral.</span></span>                      |
    | <span data-ttu-id="86b4e-370">Источник</span><span class="sxs-lookup"><span data-stu-id="86b4e-370">Source</span></span>           | <span data-ttu-id="86b4e-371">Просмотр источника, из которого создается ваучер регистрации расхода будущего периода.</span><span class="sxs-lookup"><span data-stu-id="86b4e-371">View the source that the deferral registration voucher is created from.</span></span> |