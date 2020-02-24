---
title: Ввод начальных сальдо зарплат
description: В разделе описываются шаги, необходимые для ввода начальных сальдо для кодов дохода, вычетов, льгот и налогов. Эта информация полезна для партнеров, которые выполняют миграцию или перенос данных для новой реализации зарплаты из другой системы.
author: kherr75
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e4bb8f565f5bf5630a7c5f8602b96e569692bc7c
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2020
ms.locfileid: "3005686"
---
# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="31f23-104">Ввод начальных сальдо зарплат</span><span class="sxs-lookup"><span data-stu-id="31f23-104">Enter payroll beginning balances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="31f23-105">В разделе описываются шаги, необходимые для ввода начальных сальдо для кодов дохода, вычетов, льгот и налогов.</span><span class="sxs-lookup"><span data-stu-id="31f23-105">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="31f23-106">Эта информация полезна для партнеров, которые выполняют перенос данных для новой реализации зарплаты из другой системы.</span><span class="sxs-lookup"><span data-stu-id="31f23-106">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="31f23-107">Чтобы подготовиться к вводу начальных сальдо заработной платы, мы проверяем следующее:</span><span class="sxs-lookup"><span data-stu-id="31f23-107">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

- <span data-ttu-id="31f23-108">Записи сотрудников введены и доступны в системе</span><span class="sxs-lookup"><span data-stu-id="31f23-108">Employee records are entered and available in the system</span></span>
- <span data-ttu-id="31f23-109">Следующие После данные настроены и назначены сотрудникам:</span><span class="sxs-lookup"><span data-stu-id="31f23-109">The following data is set up and assigned to employees:</span></span>

    - <span data-ttu-id="31f23-110">Циклы оплаты и платежные периоды</span><span class="sxs-lookup"><span data-stu-id="31f23-110">Pay cycles and pay periods</span></span>
    - <span data-ttu-id="31f23-111">Коды прибыли</span><span class="sxs-lookup"><span data-stu-id="31f23-111">Earning codes</span></span>
    - <span data-ttu-id="31f23-112">Налоги</span><span class="sxs-lookup"><span data-stu-id="31f23-112">Taxes</span></span>
    - <span data-ttu-id="31f23-113">Льготы и вычеты</span><span class="sxs-lookup"><span data-stu-id="31f23-113">Benefits and deductions</span></span>

- <span data-ttu-id="31f23-114">Компании должны выбрать дату, где можно настроить начальные сальдо заработной платы.</span><span class="sxs-lookup"><span data-stu-id="31f23-114">The company should have chosen a date where payroll beginning balances can be set.</span></span>
- <span data-ttu-id="31f23-115">Сведения были собраны по всем доходам, льготами или вычетами, льготным вкладам, налогам сотрудников и налогам работодателя и их суммы с начала года из старой системы.</span><span class="sxs-lookup"><span data-stu-id="31f23-115">Information were gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="31f23-116">Перед вводом начальных сальдо решите, насколько подробные данные должны быть.</span><span class="sxs-lookup"><span data-stu-id="31f23-116">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="31f23-117">Большинство компаний вводят единую, консолидированную сумму с начала года.</span><span class="sxs-lookup"><span data-stu-id="31f23-117">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="31f23-118">Однако если требуется более подробная информация, сальдо можно вводить с шагом по кварталам.</span><span class="sxs-lookup"><span data-stu-id="31f23-118">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="31f23-119">Для каждого сотрудника необходимо выбрать уровень детализации, который определит количество выписок об оплате, создаваемых вручную.</span><span class="sxs-lookup"><span data-stu-id="31f23-119">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="31f23-120">Для единой суммы с начала года для сотрудника требуется только одна выписка по оплате.</span><span class="sxs-lookup"><span data-stu-id="31f23-120">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="31f23-121">Для этого используйте суммы с начала года из окончательной выписки по оплате из предыдущей системы как сумму, введенную в новую систему учета зарплаты.</span><span class="sxs-lookup"><span data-stu-id="31f23-121">To do this use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="31f23-122">В следующем примере показано, каким образом вводятся начальные сальдо зарплаты сотрудников, включая коды дохода, льготы или вычеты и налоги.</span><span class="sxs-lookup"><span data-stu-id="31f23-122">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="31f23-123">В примере реальной ситуации у вас будет элемент строки для каждого кода дохода, льготного вычета, льготного вклада, налога сотрудника и налога работодателя с введенной суммой, которая будет являться суммой с начала года.</span><span class="sxs-lookup"><span data-stu-id="31f23-123">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="31f23-124">С помощью этого списка кодов и сумм выполните действия по созданию выписки до доходах и оплате вручную с отключенным учетом для начальных сальдо для целей зарплаты.</span><span class="sxs-lookup"><span data-stu-id="31f23-124">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span> <span data-ttu-id="31f23-125">Учет отключается, поскольку не требуется выполнять разноску этой выписки по оплате для начального сальдо в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="31f23-125">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="31f23-126">Эта делалось в старой системе и перейдет в новую систему при настройке начальных сальдо в главной книге.</span><span class="sxs-lookup"><span data-stu-id="31f23-126">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="31f23-127">A.</span><span class="sxs-lookup"><span data-stu-id="31f23-127">A.</span></span> <span data-ttu-id="31f23-128">Порядок настройки кодов доходов для использования на начальных сальдо зарплаты</span><span class="sxs-lookup"><span data-stu-id="31f23-128">How to set up earnings codes to be used on payroll beginning balances</span></span>

<span data-ttu-id="31f23-129">При вводе начальных сальдо заработной платы убедитесь, что используемые коды дохода настроены с включенным параметром "Разрешить изменение ставок выписки по оплате".</span><span class="sxs-lookup"><span data-stu-id="31f23-129">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="31f23-130">Это позволит вручную ввести сумму из старой системы.</span><span class="sxs-lookup"><span data-stu-id="31f23-130">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="31f23-131">B.</span><span class="sxs-lookup"><span data-stu-id="31f23-131">B.</span></span> <span data-ttu-id="31f23-132">Создание выписки о доходах для сотрудника для начального сальдо</span><span class="sxs-lookup"><span data-stu-id="31f23-132">Create earnings statement for an employee to have a beginning balance</span></span>

<span data-ttu-id="31f23-133">Этот шаг вручную создает выписку о доходах для каждого работника за последний период оплаты старой системы, которая создает строки выписки о доходах в новой системе расчета зарплаты.</span><span class="sxs-lookup"><span data-stu-id="31f23-133">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="31f23-134">Введите одну строку на код дохода, сумму с начала года и часы.</span><span class="sxs-lookup"><span data-stu-id="31f23-134">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="31f23-135">Операции из примера:</span><span class="sxs-lookup"><span data-stu-id="31f23-135">The sample steps are as follows:</span></span>

1. <span data-ttu-id="31f23-136">Откройте страницу **Выписки о всех доходах** и нажмите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="31f23-136">Open the **All earnings statements** page and click **New**.</span></span>

    <span data-ttu-id="31f23-137">Введите следующее:</span><span class="sxs-lookup"><span data-stu-id="31f23-137">Enter the following:</span></span> 

    | <span data-ttu-id="31f23-138">Поле</span><span class="sxs-lookup"><span data-stu-id="31f23-138">Field</span></span>      | <span data-ttu-id="31f23-139">Стоимость</span><span class="sxs-lookup"><span data-stu-id="31f23-139">Value</span></span>                 |
    |------------|-----------------------|
    | <span data-ttu-id="31f23-140">Рабочий</span><span class="sxs-lookup"><span data-stu-id="31f23-140">Worker</span></span>     | <span data-ttu-id="31f23-141">Майкл Редмонд</span><span class="sxs-lookup"><span data-stu-id="31f23-141">Michael Redmond</span></span>       |
    | <span data-ttu-id="31f23-142">Цикл оплаты</span><span class="sxs-lookup"><span data-stu-id="31f23-142">Pay cycle</span></span>  | <span data-ttu-id="31f23-143">sm</span><span class="sxs-lookup"><span data-stu-id="31f23-143">sm</span></span>                    |
    | <span data-ttu-id="31f23-144">Платежный период</span><span class="sxs-lookup"><span data-stu-id="31f23-144">Pay period</span></span> | <span data-ttu-id="31f23-145">6.16.2017 - 6.30.2017</span><span class="sxs-lookup"><span data-stu-id="31f23-145">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="31f23-146">На вкладке **Строка выписки о доходах** введите следующее:</span><span class="sxs-lookup"><span data-stu-id="31f23-146">In the **Earnings statement line** tab, enter the following:</span></span>

    <span data-ttu-id="31f23-147">Строка 1: вкладка **Строка выписки о доходах**</span><span class="sxs-lookup"><span data-stu-id="31f23-147">Line 1: **Earning statement line** tab</span></span>

    | <span data-ttu-id="31f23-148">Поле</span><span class="sxs-lookup"><span data-stu-id="31f23-148">Field</span></span>            | <span data-ttu-id="31f23-149">Стоимость</span><span class="sxs-lookup"><span data-stu-id="31f23-149">Value</span></span>       |
    |------------------|-------------|
    | <span data-ttu-id="31f23-150">Код доходов</span><span class="sxs-lookup"><span data-stu-id="31f23-150">Earnings code</span></span>    | <span data-ttu-id="31f23-151">Обычная оплата</span><span class="sxs-lookup"><span data-stu-id="31f23-151">Regular pay</span></span> |
    | <span data-ttu-id="31f23-152">Количество</span><span class="sxs-lookup"><span data-stu-id="31f23-152">Quantity</span></span>         | <span data-ttu-id="31f23-153">1.00</span><span class="sxs-lookup"><span data-stu-id="31f23-153">1.00</span></span>        |
    | <span data-ttu-id="31f23-154">Курс</span><span class="sxs-lookup"><span data-stu-id="31f23-154">Rate</span></span>             | <span data-ttu-id="31f23-155">30,000</span><span class="sxs-lookup"><span data-stu-id="31f23-155">30,000</span></span>      |
    | <span data-ttu-id="31f23-156">Вкладка "Сведения по строке"</span><span class="sxs-lookup"><span data-stu-id="31f23-156">Line details tab</span></span> |             |
    | <span data-ttu-id="31f23-157">Руководство</span><span class="sxs-lookup"><span data-stu-id="31f23-157">Manual</span></span>           | <span data-ttu-id="31f23-158">(отмечено)</span><span class="sxs-lookup"><span data-stu-id="31f23-158">(marked)</span></span>    |

    <span data-ttu-id="31f23-159">Строка 2: вкладка **Строка выписки о доходах**</span><span class="sxs-lookup"><span data-stu-id="31f23-159">Line 2: **Earning statement line** tab</span></span>

    | <span data-ttu-id="31f23-160">Поле</span><span class="sxs-lookup"><span data-stu-id="31f23-160">Field</span></span>            | <span data-ttu-id="31f23-161">Стоимость</span><span class="sxs-lookup"><span data-stu-id="31f23-161">Value</span></span>    |
    |------------------|----------|
    | <span data-ttu-id="31f23-162">Код доходов</span><span class="sxs-lookup"><span data-stu-id="31f23-162">Earnings code</span></span>    | <span data-ttu-id="31f23-163">Премия</span><span class="sxs-lookup"><span data-stu-id="31f23-163">Bonus</span></span>    |
    | <span data-ttu-id="31f23-164">Количество</span><span class="sxs-lookup"><span data-stu-id="31f23-164">Quantity</span></span>         | <span data-ttu-id="31f23-165">1.0000</span><span class="sxs-lookup"><span data-stu-id="31f23-165">1.0000</span></span>   |
    | <span data-ttu-id="31f23-166">По норме</span><span class="sxs-lookup"><span data-stu-id="31f23-166">Rate</span></span>             | <span data-ttu-id="31f23-167">4250.00</span><span class="sxs-lookup"><span data-stu-id="31f23-167">4250.00</span></span>  |
    | <span data-ttu-id="31f23-168">Вкладка "Сведения по строке"</span><span class="sxs-lookup"><span data-stu-id="31f23-168">Line details tab</span></span> |          |
    | <span data-ttu-id="31f23-169">Руководство</span><span class="sxs-lookup"><span data-stu-id="31f23-169">Manual</span></span>           | <span data-ttu-id="31f23-170">(отмечено)</span><span class="sxs-lookup"><span data-stu-id="31f23-170">(marked)</span></span> |

    <span data-ttu-id="31f23-171">Строка 3: вкладка **Строка выписки о доходах**</span><span class="sxs-lookup"><span data-stu-id="31f23-171">Line 3: **Earning statement line** tab</span></span>

    | <span data-ttu-id="31f23-172">Поле</span><span class="sxs-lookup"><span data-stu-id="31f23-172">Field</span></span>           | <span data-ttu-id="31f23-173">Стоимость</span><span class="sxs-lookup"><span data-stu-id="31f23-173">Value</span></span>      |
    |-----------------|------------|
    | <span data-ttu-id="31f23-174">Код доходов</span><span class="sxs-lookup"><span data-stu-id="31f23-174">Earnings code</span></span>   | <span data-ttu-id="31f23-175">Комиссия</span><span class="sxs-lookup"><span data-stu-id="31f23-175">Commission</span></span> |
    | <span data-ttu-id="31f23-176">Количество</span><span class="sxs-lookup"><span data-stu-id="31f23-176">Quantity</span></span>        | <span data-ttu-id="31f23-177">1.0000</span><span class="sxs-lookup"><span data-stu-id="31f23-177">1.0000</span></span>     |
    | <span data-ttu-id="31f23-178">По норме</span><span class="sxs-lookup"><span data-stu-id="31f23-178">Rate</span></span>            | <span data-ttu-id="31f23-179">!,299.00</span><span class="sxs-lookup"><span data-stu-id="31f23-179">!,299.00</span></span>   |
    | <span data-ttu-id="31f23-180">По норме</span><span class="sxs-lookup"><span data-stu-id="31f23-180">Rate</span></span>            | <span data-ttu-id="31f23-181">1,299.00</span><span class="sxs-lookup"><span data-stu-id="31f23-181">1,299.00</span></span>   |
    | <span data-ttu-id="31f23-182">Вкладка "Сведения по строке"</span><span class="sxs-lookup"><span data-stu-id="31f23-182">Line detail tab</span></span> |            |
    | <span data-ttu-id="31f23-183">Руководство</span><span class="sxs-lookup"><span data-stu-id="31f23-183">Manual</span></span>          | <span data-ttu-id="31f23-184">(отмечено)</span><span class="sxs-lookup"><span data-stu-id="31f23-184">(Marked)</span></span>   |

    > [!NOTE]
    > <span data-ttu-id="31f23-185">Установка ползунка **Вручную** на значение **Да** на вкладке **Сведения по строке** для каждой строки выписки о доходах требуется для того, чтобы начальные сальдо зарплаты были введены для каждого работника.</span><span class="sxs-lookup"><span data-stu-id="31f23-185">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="31f23-186">В области **Действия** нажмите **Запустить выписку о доходах** USA-FED-ER-FICA.</span><span class="sxs-lookup"><span data-stu-id="31f23-186">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>
4. <span data-ttu-id="31f23-187">В области **Действия** щелкните **Выписка по оплате** для открытия страницы **Создать выписки по оплате** и настройте следующее:</span><span class="sxs-lookup"><span data-stu-id="31f23-187">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

    | <span data-ttu-id="31f23-188">Поле</span><span class="sxs-lookup"><span data-stu-id="31f23-188">Field</span></span>              | <span data-ttu-id="31f23-189">Стоимость</span><span class="sxs-lookup"><span data-stu-id="31f23-189">Value</span></span>     |
    |--------------------|-----------|
    | <span data-ttu-id="31f23-190">Дата оплаты</span><span class="sxs-lookup"><span data-stu-id="31f23-190">Payment date</span></span>       | <span data-ttu-id="31f23-191">6.30.2017</span><span class="sxs-lookup"><span data-stu-id="31f23-191">6/30/2017</span></span> |
    | <span data-ttu-id="31f23-192">Тип выполнения платежа</span><span class="sxs-lookup"><span data-stu-id="31f23-192">Payment run type</span></span>   | <span data-ttu-id="31f23-193">Руководство</span><span class="sxs-lookup"><span data-stu-id="31f23-193">Manual</span></span>    |
    | <span data-ttu-id="31f23-194">Отключить учет</span><span class="sxs-lookup"><span data-stu-id="31f23-194">Disable accounting</span></span> |   <span data-ttu-id="31f23-195">Да</span><span class="sxs-lookup"><span data-stu-id="31f23-195">Yes</span></span>     |

    > [!NOTE] 
    > <span data-ttu-id="31f23-196">Это доступно, только если тип выполнения платежа — "вручную" и если пользователь хочет отключить учет на период оплаты.</span><span class="sxs-lookup"><span data-stu-id="31f23-196">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

    <span data-ttu-id="31f23-197">Щелкните **ОК** и закройте **Infolog**.</span><span class="sxs-lookup"><span data-stu-id="31f23-197">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="31f23-198">Почему ползунок "Отключить учет" необходимо установить на значение "Да" при создании выписок по оплате?</span><span class="sxs-lookup"><span data-stu-id="31f23-198">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>

<span data-ttu-id="31f23-199">Установка ползунка на значение **Да** предотвращает распределение строк в выписке по оплате в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="31f23-199">Setting the slider to **Yes** prevents lines in the pay statement from being districuted to General ledger.</span></span> <span data-ttu-id="31f23-200">Суммы главной книги были обновлены ранее при вводе сальдо из старой системы.</span><span class="sxs-lookup"><span data-stu-id="31f23-200">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="31f23-201">Ввод начальных сальдо для заработной платы позволяет создавать отчеты, которые включают сведения из предыдущего года, а также для определения ограничений для льгот и в налоговых целях.</span><span class="sxs-lookup"><span data-stu-id="31f23-201">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="31f23-202">C.</span><span class="sxs-lookup"><span data-stu-id="31f23-202">C.</span></span> <span data-ttu-id="31f23-203">Создание выписок по оплате для сотрудников</span><span class="sxs-lookup"><span data-stu-id="31f23-203">Create pay statements for employees</span></span>

<span data-ttu-id="31f23-204">После создания выписок по оплате с начальными сальдо необходимо проверить, что выписки по оплате точно отражают данные о заработной плате.</span><span class="sxs-lookup"><span data-stu-id="31f23-204">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="31f23-205">Необходимо также вручную обновить сведения о льготах и налогах, чтобы они соответствовали значения в предыдущей системе зарплаты.</span><span class="sxs-lookup"><span data-stu-id="31f23-205">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="31f23-206">Убедившись, что суммы из предыдущей системы заработной платы соответствуют суммам по текущим выпискам по оплате, необходимо финализировать выписки по оплате.</span><span class="sxs-lookup"><span data-stu-id="31f23-206">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="31f23-207">Откройте страницу **Все выписки по оплате**.</span><span class="sxs-lookup"><span data-stu-id="31f23-207">Open the **All pay statements** page.</span></span>
2. <span data-ttu-id="31f23-208">Выделите для последнюю созданную выписку по оплате для Майкла Редмонда</span><span class="sxs-lookup"><span data-stu-id="31f23-208">Highlight the last generated pay statement for Michael Redmond</span></span>
3. <span data-ttu-id="31f23-209">Щелкните **Изменит ь**, чтобы открыть страницу **Выписка по оплате**.</span><span class="sxs-lookup"><span data-stu-id="31f23-209">Click **Edit** to open the **Pay statement** page.</span></span>
4. <span data-ttu-id="31f23-210">Откройте вкладку **Льготные вычеты** и введите следующее:</span><span class="sxs-lookup"><span data-stu-id="31f23-210">Open the **Benefit deductions** tab and enter the following:</span></span>

    | <span data-ttu-id="31f23-211">Поле</span><span class="sxs-lookup"><span data-stu-id="31f23-211">Field</span></span>             | <span data-ttu-id="31f23-212">Стоимость</span><span class="sxs-lookup"><span data-stu-id="31f23-212">Value</span></span>            |
    |-------------------|------------------|
    | <span data-ttu-id="31f23-213">Льгота</span><span class="sxs-lookup"><span data-stu-id="31f23-213">Benefit</span></span>           | <span data-ttu-id="31f23-214">Сумма вычета</span><span class="sxs-lookup"><span data-stu-id="31f23-214">Deduction amount</span></span> |
    | <span data-ttu-id="31f23-215">401K</span><span class="sxs-lookup"><span data-stu-id="31f23-215">401K</span></span>              | <span data-ttu-id="31f23-216">Участие</span><span class="sxs-lookup"><span data-stu-id="31f23-216">Participate</span></span>      |
    | <span data-ttu-id="31f23-217">Dental</span><span class="sxs-lookup"><span data-stu-id="31f23-217">Dental</span></span>            | <span data-ttu-id="31f23-218">SubSp</span><span class="sxs-lookup"><span data-stu-id="31f23-218">SubSp</span></span>            |
    | <span data-ttu-id="31f23-219">Расходы на вуз care</span><span class="sxs-lookup"><span data-stu-id="31f23-219">Dep care spending</span></span> | <span data-ttu-id="31f23-220">Участие</span><span class="sxs-lookup"><span data-stu-id="31f23-220">Participate</span></span>      |
    | <span data-ttu-id="31f23-221">Vision</span><span class="sxs-lookup"><span data-stu-id="31f23-221">Vision</span></span>            | <span data-ttu-id="31f23-222">SupSp</span><span class="sxs-lookup"><span data-stu-id="31f23-222">SupSp</span></span>            |

5. <span data-ttu-id="31f23-223">На вкладке **Льготные вклады** и введите следующее:</span><span class="sxs-lookup"><span data-stu-id="31f23-223">In the **Benefit contributions** tab and enter the following:</span></span>

    | <span data-ttu-id="31f23-224">Поле</span><span class="sxs-lookup"><span data-stu-id="31f23-224">Field</span></span>   | <span data-ttu-id="31f23-225">Стоимость</span><span class="sxs-lookup"><span data-stu-id="31f23-225">Value</span></span>               |
    |---------|---------------------|
    | <span data-ttu-id="31f23-226">Льгота</span><span class="sxs-lookup"><span data-stu-id="31f23-226">Benefit</span></span> | <span data-ttu-id="31f23-227">Сумма вклада</span><span class="sxs-lookup"><span data-stu-id="31f23-227">Contribution amount</span></span> |
    | <span data-ttu-id="31f23-228">401K</span><span class="sxs-lookup"><span data-stu-id="31f23-228">401K</span></span>    | <span data-ttu-id="31f23-229">Участие</span><span class="sxs-lookup"><span data-stu-id="31f23-229">Participate</span></span>         |
    | <span data-ttu-id="31f23-230">Dental</span><span class="sxs-lookup"><span data-stu-id="31f23-230">Dental</span></span>  | <span data-ttu-id="31f23-231">SubSp</span><span class="sxs-lookup"><span data-stu-id="31f23-231">SubSp</span></span>               |
    | <span data-ttu-id="31f23-232">Vision</span><span class="sxs-lookup"><span data-stu-id="31f23-232">Vision</span></span>  | <span data-ttu-id="31f23-233">SubSp</span><span class="sxs-lookup"><span data-stu-id="31f23-233">SubSp</span></span>               |

6. <span data-ttu-id="31f23-234">На вкладке **Налоговые вычеты** введите следующее:</span><span class="sxs-lookup"><span data-stu-id="31f23-234">In the **Tax deductions** tab, enter the following:</span></span>

    | <span data-ttu-id="31f23-235">Поле</span><span class="sxs-lookup"><span data-stu-id="31f23-235">Field</span></span>           | <span data-ttu-id="31f23-236">Стоимость</span><span class="sxs-lookup"><span data-stu-id="31f23-236">Value</span></span>            |
    |-----------------|------------------|
    | <span data-ttu-id="31f23-237">Код налога</span><span class="sxs-lookup"><span data-stu-id="31f23-237">Tax code</span></span>        | <span data-ttu-id="31f23-238">Сумма вычета</span><span class="sxs-lookup"><span data-stu-id="31f23-238">Deduction amount</span></span> |
    | <span data-ttu-id="31f23-239">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="31f23-239">USA-FED-ER-FICA</span></span> | <span data-ttu-id="31f23-240">1600.00</span><span class="sxs-lookup"><span data-stu-id="31f23-240">1600.00</span></span>          |
    | <span data-ttu-id="31f23-241">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="31f23-241">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="31f23-242">825.75</span><span class="sxs-lookup"><span data-stu-id="31f23-242">825.75</span></span>           |

7. <span data-ttu-id="31f23-243">На вкладке **Налоговые вклады** введите следующее:</span><span class="sxs-lookup"><span data-stu-id="31f23-243">In the **Tax contributions** tab enter the following:</span></span>
8. <span data-ttu-id="31f23-244">Щелкните **Рассчитать**.</span><span class="sxs-lookup"><span data-stu-id="31f23-244">Click **Calculate**.</span></span>

    > [!IMPORTANT] 
    > <span data-ttu-id="31f23-245">Проверьте итоги в выписке по оплате,чтобы они соответствовали значениям с начала года в старой системе для работника.</span><span class="sxs-lookup"><span data-stu-id="31f23-245">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="31f23-246">Можно не торопиться с финализацией на следующем шаге, чтобы выполнить общую проверку всех выписок по оплате в совокупности.</span><span class="sxs-lookup"><span data-stu-id="31f23-246">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="31f23-247">После проверки просмотрите все выписки по оплате и финализируйте их.</span><span class="sxs-lookup"><span data-stu-id="31f23-247">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="31f23-248">При необходимости такой же процесс может выполняться с шагом по кварталу для всех предыдущих кварталов каждого года.</span><span class="sxs-lookup"><span data-stu-id="31f23-248">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="31f23-249">Это необходим только в том случае, если клиенту нужно просмотреть данные по кварталам без возвращения к старой системе.</span><span class="sxs-lookup"><span data-stu-id="31f23-249">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="31f23-250">Если была допущена ошибка при вводе начальных сальдо для сотрудника</span><span class="sxs-lookup"><span data-stu-id="31f23-250">If you make a mistake Entering Beginning Balances for an Employee</span></span>

<span data-ttu-id="31f23-251">Имеется возможность отменить ввод и повторить проводки.</span><span class="sxs-lookup"><span data-stu-id="31f23-251">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="31f23-252">Чтобы отменить проводку, необходимо выполнить следующие действия на странице **Все выписки по оплате**.</span><span class="sxs-lookup"><span data-stu-id="31f23-252">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="31f23-253">Щелкните **Отменить**.</span><span class="sxs-lookup"><span data-stu-id="31f23-253">Click **Reverse**.</span></span>
2. <span data-ttu-id="31f23-254">Щелкните **Да** при появлении сообщения "При сторнировании этой выписки по оплате будет создана сторнирующая выписка по оплате, корреспондирующая с данной выпиской.</span><span class="sxs-lookup"><span data-stu-id="31f23-254">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="31f23-255">Ни одну из выписок по оплате нельзя будет изменить.</span><span class="sxs-lookup"><span data-stu-id="31f23-255">Neither pay statement can be edited.</span></span> <span data-ttu-id="31f23-256">Вы действительно хотите сторнировать эту выписку по оплате?</span><span class="sxs-lookup"><span data-stu-id="31f23-256">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="31f23-257">.</span><span class="sxs-lookup"><span data-stu-id="31f23-257">displays.</span></span> 

<span data-ttu-id="31f23-258">После реверсирования выписки по оплате можно создать новую выписку по оплате для работника из выписке о доходах, созданной ранее.</span><span class="sxs-lookup"><span data-stu-id="31f23-258">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="31f23-259">Не забудьте исправить все неправильные строки в выписке о доходах перед созданием новой выписки по оплате, а затем создайте новую выписку по оплате с правильными суммами.</span><span class="sxs-lookup"><span data-stu-id="31f23-259">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 
