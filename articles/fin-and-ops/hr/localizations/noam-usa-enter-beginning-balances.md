---
title: "Ввод начальных сальдо зарплат"
description: "В разделе описываются шаги, необходимые для ввода начальных сальдо для кодов дохода, вычетов, льгот и налогов. Эта информация полезна для партнеров, которые выполняют миграцию или перенос данных для новой реализации зарплаты из другой системы."
author: kherr75
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ceaf56573c99bb257aed127af5e15ee2a7a961a5
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="a4405-104">Ввод начальных сальдо зарплат</span><span class="sxs-lookup"><span data-stu-id="a4405-104">Enter payroll beginning balances</span></span>

[!include[banner](../../includes/banner.md)]

<span data-ttu-id="a4405-105">В разделе описываются шаги, необходимые для ввода начальных сальдо для кодов дохода, вычетов, льгот и налогов.</span><span class="sxs-lookup"><span data-stu-id="a4405-105">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="a4405-106">Эта информация полезна для партнеров, которые выполняют перенос данных для новой реализации зарплаты из другой системы.</span><span class="sxs-lookup"><span data-stu-id="a4405-106">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="a4405-107">Чтобы подготовиться к вводу начальных сальдо заработной платы, мы проверяем следующее:</span><span class="sxs-lookup"><span data-stu-id="a4405-107">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

> * <span data-ttu-id="a4405-108">Записи сотрудников введены и доступны в системе</span><span class="sxs-lookup"><span data-stu-id="a4405-108">Employee records are entered and available in the system</span></span>
> * <span data-ttu-id="a4405-109">Следующие После данные настроены и назначены сотрудникам:</span><span class="sxs-lookup"><span data-stu-id="a4405-109">The following data is set up and assigned to employees:</span></span>

> > * <span data-ttu-id="a4405-110">Циклы оплаты и платежные периоды</span><span class="sxs-lookup"><span data-stu-id="a4405-110">Pay cycles and pay periods</span></span>
> > * <span data-ttu-id="a4405-111">Коды прибыли</span><span class="sxs-lookup"><span data-stu-id="a4405-111">Earning codes</span></span>
> > * <span data-ttu-id="a4405-112">Налоги</span><span class="sxs-lookup"><span data-stu-id="a4405-112">Taxes</span></span>
> > * <span data-ttu-id="a4405-113">Льготы и вычеты</span><span class="sxs-lookup"><span data-stu-id="a4405-113">Benefits and deductions</span></span>

> * <span data-ttu-id="a4405-114">Компании должны выбрать дату, где можно настроить начальные сальдо заработной платы.</span><span class="sxs-lookup"><span data-stu-id="a4405-114">The company should have chosen a date where payroll beginning balances can be set.</span></span>

> * <span data-ttu-id="a4405-115">Сведения были собраны по всем доходам, льготами или вычетами, льготным вкладам, налогам сотрудников и налогам работодателя и их суммы с начала года из старой системы.</span><span class="sxs-lookup"><span data-stu-id="a4405-115">Information were gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="a4405-116">Перед вводом начальных сальдо решите, насколько подробные данные должны быть.</span><span class="sxs-lookup"><span data-stu-id="a4405-116">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="a4405-117">Большинство компаний вводят единую, консолидированную сумму с начала года.</span><span class="sxs-lookup"><span data-stu-id="a4405-117">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="a4405-118">Однако если требуется более подробная информация, сальдо можно вводить с шагом по кварталам.</span><span class="sxs-lookup"><span data-stu-id="a4405-118">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="a4405-119">Для каждого сотрудника необходимо выбрать уровень детализации, который определит количество выписок об оплате, создаваемых вручную.</span><span class="sxs-lookup"><span data-stu-id="a4405-119">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="a4405-120">Для единой суммы с начала года для сотрудника требуется только одна выписка по оплате.</span><span class="sxs-lookup"><span data-stu-id="a4405-120">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="a4405-121">Для этого используйте суммы с начала года из окончательной выписки по оплате из предыдущей системы как сумму, введенную в новую систему учета зарплаты.</span><span class="sxs-lookup"><span data-stu-id="a4405-121">To do this use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="a4405-122">В следующем примере показано, каким образом вводятся начальные сальдо зарплаты сотрудников, включая коды дохода, льготы или вычеты и налоги.</span><span class="sxs-lookup"><span data-stu-id="a4405-122">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="a4405-123">В примере реальной ситуации у вас будет элемент строки для каждого кода дохода, льготного вычета, льготного вклада, налога сотрудника и налога работодателя с введенной суммой, которая будет являться суммой с начала года.</span><span class="sxs-lookup"><span data-stu-id="a4405-123">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="a4405-124">С помощью этого списка кодов и сумм выполните действия по созданию выписки до доходах и оплате вручную с отключенным учетом для начальных сальдо для целей зарплаты.</span><span class="sxs-lookup"><span data-stu-id="a4405-124">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span>  <span data-ttu-id="a4405-125">Учет отключается, поскольку не требуется выполнять разноску этой выписки по оплате для начального сальдо в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="a4405-125">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="a4405-126">Эта делалось в старой системе и перейдет в новую систему при настройке начальных сальдо в главной книге.</span><span class="sxs-lookup"><span data-stu-id="a4405-126">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="a4405-127">A.</span><span class="sxs-lookup"><span data-stu-id="a4405-127">A.</span></span> <span data-ttu-id="a4405-128">Порядок настройки кодов доходов для использования на начальных сальдо зарплаты</span><span class="sxs-lookup"><span data-stu-id="a4405-128">How to set up earnings codes to be used on payroll beginning balances</span></span>
<span data-ttu-id="a4405-129">При вводе начальных сальдо заработной платы убедитесь, что используемые коды дохода настроены с включенным параметром "Разрешить изменение ставок выписки по оплате".</span><span class="sxs-lookup"><span data-stu-id="a4405-129">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="a4405-130">Это позволит вручную ввести сумму из старой системы.</span><span class="sxs-lookup"><span data-stu-id="a4405-130">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="a4405-131">B.</span><span class="sxs-lookup"><span data-stu-id="a4405-131">B.</span></span> <span data-ttu-id="a4405-132">Создание выписки о доходах для сотрудника для начального сальдо</span><span class="sxs-lookup"><span data-stu-id="a4405-132">Create earnings statement for an employee to have a beginning balance</span></span>
<span data-ttu-id="a4405-133">Этот шаг вручную создает выписку о доходах для каждого работника за последний период оплаты старой системы, которая создает строки выписки о доходах в новой системе расчета зарплаты.</span><span class="sxs-lookup"><span data-stu-id="a4405-133">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="a4405-134">Введите одну строку на код дохода, сумму с начала года и часы.</span><span class="sxs-lookup"><span data-stu-id="a4405-134">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="a4405-135">Операции из примера:</span><span class="sxs-lookup"><span data-stu-id="a4405-135">The sample steps are as follows:</span></span>

1. <span data-ttu-id="a4405-136">Откройте страницу **Выписки о всех доходах** и нажмите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="a4405-136">Open the **All earnings statements** page and click **New**.</span></span>  

<span data-ttu-id="a4405-137">Введите следующее:</span><span class="sxs-lookup"><span data-stu-id="a4405-137">Enter the following:</span></span> 

| <span data-ttu-id="a4405-138">Поле</span><span class="sxs-lookup"><span data-stu-id="a4405-138">Field</span></span>      | <span data-ttu-id="a4405-139">Стоимость</span><span class="sxs-lookup"><span data-stu-id="a4405-139">Value</span></span>                 |
|------------|-----------------------|
| <span data-ttu-id="a4405-140">Рабочий</span><span class="sxs-lookup"><span data-stu-id="a4405-140">Worker</span></span>     | <span data-ttu-id="a4405-141">Майкл Редмонд</span><span class="sxs-lookup"><span data-stu-id="a4405-141">Michael Redmond</span></span>       |
| <span data-ttu-id="a4405-142">Цикл оплаты</span><span class="sxs-lookup"><span data-stu-id="a4405-142">Pay cycle</span></span>  | <span data-ttu-id="a4405-143">sm</span><span class="sxs-lookup"><span data-stu-id="a4405-143">sm</span></span>                    |
| <span data-ttu-id="a4405-144">Платежный период</span><span class="sxs-lookup"><span data-stu-id="a4405-144">Pay period</span></span> | <span data-ttu-id="a4405-145">6.16.2017 - 6.30.2017</span><span class="sxs-lookup"><span data-stu-id="a4405-145">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="a4405-146">На вкладке **Строка выписки о доходах** введите следующее:</span><span class="sxs-lookup"><span data-stu-id="a4405-146">In the **Earnings statement line** tab, enter the following:</span></span>

<span data-ttu-id="a4405-147">Строка 1: вкладка **Строка выписки о доходах**</span><span class="sxs-lookup"><span data-stu-id="a4405-147">Line 1: **Earning statement line** tab</span></span>

| <span data-ttu-id="a4405-148">Поле</span><span class="sxs-lookup"><span data-stu-id="a4405-148">Field</span></span>            | <span data-ttu-id="a4405-149">Стоимость</span><span class="sxs-lookup"><span data-stu-id="a4405-149">Value</span></span>       |
|------------------|-------------|
| <span data-ttu-id="a4405-150">Код доходов</span><span class="sxs-lookup"><span data-stu-id="a4405-150">Earnings code</span></span>    | <span data-ttu-id="a4405-151">Обычная оплата</span><span class="sxs-lookup"><span data-stu-id="a4405-151">Regular pay</span></span> |
| <span data-ttu-id="a4405-152">Количество</span><span class="sxs-lookup"><span data-stu-id="a4405-152">Quantity</span></span>         | <span data-ttu-id="a4405-153">1.00</span><span class="sxs-lookup"><span data-stu-id="a4405-153">1.00</span></span>        |
| <span data-ttu-id="a4405-154">Rage</span><span class="sxs-lookup"><span data-stu-id="a4405-154">Rage</span></span>             | <span data-ttu-id="a4405-155">30 000</span><span class="sxs-lookup"><span data-stu-id="a4405-155">30,000</span></span>      |
| <span data-ttu-id="a4405-156">Вкладка "Сведения по строке"</span><span class="sxs-lookup"><span data-stu-id="a4405-156">Line details tab</span></span> |             |
| <span data-ttu-id="a4405-157">Руководство</span><span class="sxs-lookup"><span data-stu-id="a4405-157">Manual</span></span>           | <span data-ttu-id="a4405-158">(отмечено)</span><span class="sxs-lookup"><span data-stu-id="a4405-158">(marked)</span></span>    |

<span data-ttu-id="a4405-159">Строка 2: вкладка **Строка выписки о доходах**</span><span class="sxs-lookup"><span data-stu-id="a4405-159">Line 2: **Earning statement line** tab</span></span>

| <span data-ttu-id="a4405-160">Поле</span><span class="sxs-lookup"><span data-stu-id="a4405-160">Field</span></span>            | <span data-ttu-id="a4405-161">Стоимость</span><span class="sxs-lookup"><span data-stu-id="a4405-161">Value</span></span>    |
|------------------|----------|
| <span data-ttu-id="a4405-162">Код доходов</span><span class="sxs-lookup"><span data-stu-id="a4405-162">Earnings code</span></span>    | <span data-ttu-id="a4405-163">Премия</span><span class="sxs-lookup"><span data-stu-id="a4405-163">Bonus</span></span>    |
| <span data-ttu-id="a4405-164">Количество</span><span class="sxs-lookup"><span data-stu-id="a4405-164">Quantity</span></span>         | <span data-ttu-id="a4405-165">1.0000</span><span class="sxs-lookup"><span data-stu-id="a4405-165">1.0000</span></span>   |
| <span data-ttu-id="a4405-166">По норме</span><span class="sxs-lookup"><span data-stu-id="a4405-166">Rate</span></span>             | <span data-ttu-id="a4405-167">4250.00</span><span class="sxs-lookup"><span data-stu-id="a4405-167">4250.00</span></span>  |
| <span data-ttu-id="a4405-168">Вкладка "Сведения по строке"</span><span class="sxs-lookup"><span data-stu-id="a4405-168">Line details tab</span></span> |          |
| <span data-ttu-id="a4405-169">Руководство</span><span class="sxs-lookup"><span data-stu-id="a4405-169">Manual</span></span>           | <span data-ttu-id="a4405-170">(отмечено)</span><span class="sxs-lookup"><span data-stu-id="a4405-170">(marked)</span></span> |

<span data-ttu-id="a4405-171">Строка 3: вкладка **Строка выписки о доходах**</span><span class="sxs-lookup"><span data-stu-id="a4405-171">Line 3: **Earning statement line** tab</span></span>

| <span data-ttu-id="a4405-172">Поле</span><span class="sxs-lookup"><span data-stu-id="a4405-172">Field</span></span>           | <span data-ttu-id="a4405-173">Стоимость</span><span class="sxs-lookup"><span data-stu-id="a4405-173">Value</span></span>      |
|-----------------|------------|
| <span data-ttu-id="a4405-174">Код доходов</span><span class="sxs-lookup"><span data-stu-id="a4405-174">Earnings code</span></span>   | <span data-ttu-id="a4405-175">Комиссия</span><span class="sxs-lookup"><span data-stu-id="a4405-175">Commission</span></span> |
| <span data-ttu-id="a4405-176">Количество</span><span class="sxs-lookup"><span data-stu-id="a4405-176">Quantity</span></span>        | <span data-ttu-id="a4405-177">1.0000</span><span class="sxs-lookup"><span data-stu-id="a4405-177">1.0000</span></span>     |
| <span data-ttu-id="a4405-178">По норме</span><span class="sxs-lookup"><span data-stu-id="a4405-178">Rate</span></span>            | <span data-ttu-id="a4405-179">!,299.00</span><span class="sxs-lookup"><span data-stu-id="a4405-179">!,299.00</span></span>   |
| <span data-ttu-id="a4405-180">По норме</span><span class="sxs-lookup"><span data-stu-id="a4405-180">Rate</span></span>            | <span data-ttu-id="a4405-181">1,299.00</span><span class="sxs-lookup"><span data-stu-id="a4405-181">1,299.00</span></span>   |
| <span data-ttu-id="a4405-182">Вкладка "Сведения по строке"</span><span class="sxs-lookup"><span data-stu-id="a4405-182">Line detail tab</span></span> |            |
| <span data-ttu-id="a4405-183">Руководство</span><span class="sxs-lookup"><span data-stu-id="a4405-183">Manual</span></span>          | <span data-ttu-id="a4405-184">(отмечено)</span><span class="sxs-lookup"><span data-stu-id="a4405-184">(Marked)</span></span>   |

> [!NOTE]
> <span data-ttu-id="a4405-185">Установка ползунка **Вручную** на значение **Да** на вкладке **Сведения по строке** для каждой строки выписки о доходах требуется для того, чтобы начальные сальдо зарплаты были введены для каждого работника.</span><span class="sxs-lookup"><span data-stu-id="a4405-185">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="a4405-186">В области **Действия** нажмите **Запустить выписку о доходах** USA-FED-ER-FICA.</span><span class="sxs-lookup"><span data-stu-id="a4405-186">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>

4. <span data-ttu-id="a4405-187">В области **Действия** щелкните **Выписка по оплате** для открытия страницы **Создать выписки по оплате** и настройте следующее:</span><span class="sxs-lookup"><span data-stu-id="a4405-187">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

| <span data-ttu-id="a4405-188">Поле</span><span class="sxs-lookup"><span data-stu-id="a4405-188">Field</span></span>              | <span data-ttu-id="a4405-189">Стоимость</span><span class="sxs-lookup"><span data-stu-id="a4405-189">Value</span></span>     |
|--------------------|-----------|
| <span data-ttu-id="a4405-190">Дата оплаты</span><span class="sxs-lookup"><span data-stu-id="a4405-190">Payment date</span></span>       | <span data-ttu-id="a4405-191">6.30.2017</span><span class="sxs-lookup"><span data-stu-id="a4405-191">6/30/2017</span></span> |
| <span data-ttu-id="a4405-192">Тип выполнения платежа</span><span class="sxs-lookup"><span data-stu-id="a4405-192">Payment run type</span></span>   | <span data-ttu-id="a4405-193">Руководство</span><span class="sxs-lookup"><span data-stu-id="a4405-193">Manual</span></span>    |
| <span data-ttu-id="a4405-194">Отключить учет</span><span class="sxs-lookup"><span data-stu-id="a4405-194">Disable accounting</span></span> |   <span data-ttu-id="a4405-195">Да</span><span class="sxs-lookup"><span data-stu-id="a4405-195">Yes</span></span>     |

> [!NOTE] 
> <span data-ttu-id="a4405-196">Это доступно, только если тип выполнения платежа — "вручную" и если пользователь хочет отключить учет на период оплаты.</span><span class="sxs-lookup"><span data-stu-id="a4405-196">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

<span data-ttu-id="a4405-197">Щелкните **ОК** и закройте **Infolog**.</span><span class="sxs-lookup"><span data-stu-id="a4405-197">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="a4405-198">Почему ползунок "Отключить учет" необходимо установить на значение "Да" при создании выписок по оплате?</span><span class="sxs-lookup"><span data-stu-id="a4405-198">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>
<span data-ttu-id="a4405-199">Установка ползунка на значение **Да** предотвращает распределение строк в выписке по оплате в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="a4405-199">Setting the slider to **Yes** prevents lines in the pay statement from being districuted to General ledger.</span></span> <span data-ttu-id="a4405-200">Суммы главной книги были обновлены ранее при вводе сальдо из старой системы.</span><span class="sxs-lookup"><span data-stu-id="a4405-200">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="a4405-201">Ввод начальных сальдо для заработной платы позволяет создавать отчеты, которые включают сведения из предыдущего года, а также для определения ограничений для льгот и в налоговых целях.</span><span class="sxs-lookup"><span data-stu-id="a4405-201">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>   

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="a4405-202">C.</span><span class="sxs-lookup"><span data-stu-id="a4405-202">C.</span></span> <span data-ttu-id="a4405-203">Создание выписок по оплате для сотрудников</span><span class="sxs-lookup"><span data-stu-id="a4405-203">Create pay statements for employees</span></span>
<span data-ttu-id="a4405-204">После создания выписок по оплате с начальными сальдо необходимо проверить, что выписки по оплате точно отражают данные о заработной плате.</span><span class="sxs-lookup"><span data-stu-id="a4405-204">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="a4405-205">Необходимо также вручную обновить сведения о льготах и налогах, чтобы они соответствовали значения в предыдущей системе зарплаты.</span><span class="sxs-lookup"><span data-stu-id="a4405-205">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="a4405-206">Убедившись, что суммы из предыдущей системы заработной платы соответствуют суммам по текущим выпискам по оплате, необходимо финализировать выписки по оплате.</span><span class="sxs-lookup"><span data-stu-id="a4405-206">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="a4405-207">Откройте страницу **Все выписки по оплате**.</span><span class="sxs-lookup"><span data-stu-id="a4405-207">Open the **All pay statements** page.</span></span>

2. <span data-ttu-id="a4405-208">Выделите для последнюю созданную выписку по оплате для Майкла Редмонда</span><span class="sxs-lookup"><span data-stu-id="a4405-208">Highlight the last generated pay statement for Michael Redmond</span></span>

3. <span data-ttu-id="a4405-209">Щелкните **Изменит ь**, чтобы открыть страницу **Выписка по оплате**.</span><span class="sxs-lookup"><span data-stu-id="a4405-209">Click **Edit** to open the **Pay statement** page.</span></span>

4. <span data-ttu-id="a4405-210">Откройте вкладку **Льготные вычеты** и введите следующее:</span><span class="sxs-lookup"><span data-stu-id="a4405-210">Open the **Benefit deductions** tab and enter the following:</span></span>

| <span data-ttu-id="a4405-211">Поле</span><span class="sxs-lookup"><span data-stu-id="a4405-211">Field</span></span>                           | <span data-ttu-id="a4405-212">Стоимость</span><span class="sxs-lookup"><span data-stu-id="a4405-212">Value</span></span>            |
|---------------------------------|------------------|
| <span data-ttu-id="a4405-213">Льгота</span><span class="sxs-lookup"><span data-stu-id="a4405-213">Benefit</span></span>                         | <span data-ttu-id="a4405-214">Сумма вычета</span><span class="sxs-lookup"><span data-stu-id="a4405-214">Deduction amount</span></span> |
| <span data-ttu-id="a4405-215">401K</span><span class="sxs-lookup"><span data-stu-id="a4405-215">401K</span></span> | <span data-ttu-id="a4405-216">Участие</span><span class="sxs-lookup"><span data-stu-id="a4405-216">Participate</span></span>              | <span data-ttu-id="a4405-217">3000.00</span><span class="sxs-lookup"><span data-stu-id="a4405-217">3000.00</span></span>          |
| <span data-ttu-id="a4405-218">Dental</span><span class="sxs-lookup"><span data-stu-id="a4405-218">Dental</span></span> | <span data-ttu-id="a4405-219">SubSp</span><span class="sxs-lookup"><span data-stu-id="a4405-219">SubSp</span></span>                  | <span data-ttu-id="a4405-220">495,00</span><span class="sxs-lookup"><span data-stu-id="a4405-220">495.00</span></span>           |
| <span data-ttu-id="a4405-221">Расходы на вуз care</span><span class="sxs-lookup"><span data-stu-id="a4405-221">Dep care spending</span></span> | <span data-ttu-id="a4405-222">Участие</span><span class="sxs-lookup"><span data-stu-id="a4405-222">Participate</span></span> | <span data-ttu-id="a4405-223">2500.00</span><span class="sxs-lookup"><span data-stu-id="a4405-223">2500.00</span></span>          |
| <span data-ttu-id="a4405-224">Vision</span><span class="sxs-lookup"><span data-stu-id="a4405-224">Vision</span></span> | <span data-ttu-id="a4405-225">SupSp</span><span class="sxs-lookup"><span data-stu-id="a4405-225">SupSp</span></span>                  | <span data-ttu-id="a4405-226">500.00</span><span class="sxs-lookup"><span data-stu-id="a4405-226">500.00</span></span>           |

5. <span data-ttu-id="a4405-227">На вкладке **Льготные вклады** и введите следующее:</span><span class="sxs-lookup"><span data-stu-id="a4405-227">In the **Benefit contributions** tab and enter the following:</span></span>

| <span data-ttu-id="a4405-228">Поле</span><span class="sxs-lookup"><span data-stu-id="a4405-228">Field</span></span>              | <span data-ttu-id="a4405-229">Стоимость</span><span class="sxs-lookup"><span data-stu-id="a4405-229">Value</span></span>               |
|--------------------|---------------------|
| <span data-ttu-id="a4405-230">Льгота</span><span class="sxs-lookup"><span data-stu-id="a4405-230">Benefit</span></span>            | <span data-ttu-id="a4405-231">Сумма вклада</span><span class="sxs-lookup"><span data-stu-id="a4405-231">Contribution amount</span></span> |
| <span data-ttu-id="a4405-232">401K</span><span class="sxs-lookup"><span data-stu-id="a4405-232">401K</span></span> | <span data-ttu-id="a4405-233">Участие</span><span class="sxs-lookup"><span data-stu-id="a4405-233">Participate</span></span> | <span data-ttu-id="a4405-234">3000,00</span><span class="sxs-lookup"><span data-stu-id="a4405-234">3000,00</span></span>             |
| <span data-ttu-id="a4405-235">Dental</span><span class="sxs-lookup"><span data-stu-id="a4405-235">Dental</span></span> | <span data-ttu-id="a4405-236">SubSp</span><span class="sxs-lookup"><span data-stu-id="a4405-236">SubSp</span></span>     | <span data-ttu-id="a4405-237">495,00</span><span class="sxs-lookup"><span data-stu-id="a4405-237">495.00</span></span>              |
| <span data-ttu-id="a4405-238">Vision</span><span class="sxs-lookup"><span data-stu-id="a4405-238">Vision</span></span> | <span data-ttu-id="a4405-239">SubSp</span><span class="sxs-lookup"><span data-stu-id="a4405-239">SubSp</span></span>     | <span data-ttu-id="a4405-240">500.00</span><span class="sxs-lookup"><span data-stu-id="a4405-240">500.00</span></span>              |

6. <span data-ttu-id="a4405-241">На вкладке **Налоговые вычеты** введите следующее:</span><span class="sxs-lookup"><span data-stu-id="a4405-241">In the **Tax deductions** tab, enter the following:</span></span>

| <span data-ttu-id="a4405-242">Поле</span><span class="sxs-lookup"><span data-stu-id="a4405-242">Field</span></span>           | <span data-ttu-id="a4405-243">Стоимость</span><span class="sxs-lookup"><span data-stu-id="a4405-243">Value</span></span>            |
|-----------------|------------------|
| <span data-ttu-id="a4405-244">Код налога</span><span class="sxs-lookup"><span data-stu-id="a4405-244">Tax code</span></span>        | <span data-ttu-id="a4405-245">Сумма вычета</span><span class="sxs-lookup"><span data-stu-id="a4405-245">Deduction amount</span></span> |
| <span data-ttu-id="a4405-246">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="a4405-246">USA-FED-ER-FICA</span></span> | <span data-ttu-id="a4405-247">1600.00</span><span class="sxs-lookup"><span data-stu-id="a4405-247">1600.00</span></span>          |
| <span data-ttu-id="a4405-248">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="a4405-248">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="a4405-249">825.75</span><span class="sxs-lookup"><span data-stu-id="a4405-249">825.75</span></span>           |

7. <span data-ttu-id="a4405-250">На вкладке **Налоговые вклады** введите следующее:</span><span class="sxs-lookup"><span data-stu-id="a4405-250">In the **Tax contributions** tab enter the following:</span></span>

8. <span data-ttu-id="a4405-251">Щелкните **Рассчитать**.</span><span class="sxs-lookup"><span data-stu-id="a4405-251">Click **Calculate**.</span></span>
> [!IMPORTANT] 
> <span data-ttu-id="a4405-252">Проверьте итоги в выписке по оплате,чтобы они соответствовали значениям с начала года в старой системе для работника.</span><span class="sxs-lookup"><span data-stu-id="a4405-252">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="a4405-253">Можно не торопиться с финализацией на следующем шаге, чтобы выполнить общую проверку всех выписок по оплате в совокупности.</span><span class="sxs-lookup"><span data-stu-id="a4405-253">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="a4405-254">После проверки просмотрите все выписки по оплате и финализируйте их.</span><span class="sxs-lookup"><span data-stu-id="a4405-254">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="a4405-255">При необходимости такой же процесс может выполняться с шагом по кварталу для всех предыдущих кварталов каждого года.</span><span class="sxs-lookup"><span data-stu-id="a4405-255">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="a4405-256">Это необходим только в том случае, если клиенту нужно просмотреть данные по кварталам без возвращения к старой системе.</span><span class="sxs-lookup"><span data-stu-id="a4405-256">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="a4405-257">Если была допущена ошибка при вводе начальных сальдо для сотрудника</span><span class="sxs-lookup"><span data-stu-id="a4405-257">If you make a mistake Entering Beginning Balances for an Employee</span></span>
<span data-ttu-id="a4405-258">Имеется возможность отменить ввод и повторить проводки.</span><span class="sxs-lookup"><span data-stu-id="a4405-258">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="a4405-259">Чтобы отменить проводку, необходимо выполнить следующие действия на странице **Все выписки по оплате**.</span><span class="sxs-lookup"><span data-stu-id="a4405-259">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="a4405-260">Щелкните **Отменить**.</span><span class="sxs-lookup"><span data-stu-id="a4405-260">Click **Reverse**.</span></span>

2. <span data-ttu-id="a4405-261">Щелкните **Да** при появлении сообщения "При сторнировании этой выписки по оплате будет создана сторнирующая выписка по оплате, корреспондирующая с данной выпиской.</span><span class="sxs-lookup"><span data-stu-id="a4405-261">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="a4405-262">Ни одну из выписок по оплате нельзя будет изменить.</span><span class="sxs-lookup"><span data-stu-id="a4405-262">Neither pay statement can be edited.</span></span> <span data-ttu-id="a4405-263">Вы действительно хотите сторнировать эту выписку по оплате?</span><span class="sxs-lookup"><span data-stu-id="a4405-263">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="a4405-264">.</span><span class="sxs-lookup"><span data-stu-id="a4405-264">displays.</span></span> 

<span data-ttu-id="a4405-265">После реверсирования выписки по оплате можно создать новую выписку по оплате для работника из выписке о доходах, созданной ранее.</span><span class="sxs-lookup"><span data-stu-id="a4405-265">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="a4405-266">Не забудьте исправить все неправильные строки в выписке о доходах перед созданием новой выписки по оплате, а затем создайте новую выписку по оплате с правильными суммами.</span><span class="sxs-lookup"><span data-stu-id="a4405-266">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 

