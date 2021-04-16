---
title: Ввод начальных сальдо зарплат
description: В разделе описываются шаги, необходимые для ввода начальных сальдо для кодов дохода, вычетов, льгот и налогов.
author: andreabichsel
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9272828fe5d6e0bf131ea66353a0d5c3c7b1c4bd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752158"
---
# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="a6851-103">Ввод начальных сальдо зарплат</span><span class="sxs-lookup"><span data-stu-id="a6851-103">Enter payroll beginning balances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a6851-104">В разделе описываются шаги, необходимые для ввода начальных сальдо для кодов дохода, вычетов, льгот и налогов.</span><span class="sxs-lookup"><span data-stu-id="a6851-104">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="a6851-105">Эта информация полезна для партнеров, которые выполняют перенос данных для новой реализации зарплаты из другой системы.</span><span class="sxs-lookup"><span data-stu-id="a6851-105">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="a6851-106">Чтобы подготовиться к вводу начальных сальдо заработной платы, мы проверяем следующее:</span><span class="sxs-lookup"><span data-stu-id="a6851-106">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

- <span data-ttu-id="a6851-107">Записи сотрудников введены и доступны в системе</span><span class="sxs-lookup"><span data-stu-id="a6851-107">Employee records are entered and available in the system</span></span>
- <span data-ttu-id="a6851-108">Следующие После данные настроены и назначены сотрудникам:</span><span class="sxs-lookup"><span data-stu-id="a6851-108">The following data is set up and assigned to employees:</span></span>

    - <span data-ttu-id="a6851-109">Циклы оплаты и платежные периоды</span><span class="sxs-lookup"><span data-stu-id="a6851-109">Pay cycles and pay periods</span></span>
    - <span data-ttu-id="a6851-110">Коды прибыли</span><span class="sxs-lookup"><span data-stu-id="a6851-110">Earning codes</span></span>
    - <span data-ttu-id="a6851-111">Налоги</span><span class="sxs-lookup"><span data-stu-id="a6851-111">Taxes</span></span>
    - <span data-ttu-id="a6851-112">Льготы и вычеты</span><span class="sxs-lookup"><span data-stu-id="a6851-112">Benefits and deductions</span></span>

- <span data-ttu-id="a6851-113">Компании должны выбрать дату, где можно настроить начальные сальдо заработной платы.</span><span class="sxs-lookup"><span data-stu-id="a6851-113">The company should have chosen a date where payroll beginning balances can be set.</span></span>
- <span data-ttu-id="a6851-114">Сведения были собраны по всем доходам, льготами или вычетами, льготным вкладам, налогам сотрудников и налогам работодателя и их суммы с начала года из старой системы.</span><span class="sxs-lookup"><span data-stu-id="a6851-114">Information was gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="a6851-115">Перед вводом начальных сальдо решите, насколько подробные данные должны быть.</span><span class="sxs-lookup"><span data-stu-id="a6851-115">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="a6851-116">Большинство компаний вводят единую, консолидированную сумму с начала года.</span><span class="sxs-lookup"><span data-stu-id="a6851-116">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="a6851-117">Однако если требуется более подробная информация, сальдо можно вводить с шагом по кварталам.</span><span class="sxs-lookup"><span data-stu-id="a6851-117">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="a6851-118">Для каждого сотрудника необходимо выбрать уровень детализации, который определит количество выписок об оплате, создаваемых вручную.</span><span class="sxs-lookup"><span data-stu-id="a6851-118">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="a6851-119">Для единой суммы с начала года для сотрудника требуется только одна выписка по оплате.</span><span class="sxs-lookup"><span data-stu-id="a6851-119">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="a6851-120">Для этого используйте суммы с начала года из окончательной выписки по оплате из предыдущей системы как сумму, введенную в новую систему учета зарплаты.</span><span class="sxs-lookup"><span data-stu-id="a6851-120">To do this, use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="a6851-121">В следующем примере показано, каким образом вводятся начальные сальдо зарплаты сотрудников, включая коды дохода, льготы или вычеты и налоги.</span><span class="sxs-lookup"><span data-stu-id="a6851-121">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="a6851-122">В примере реальной ситуации у вас будет элемент строки для каждого кода дохода, льготного вычета, льготного вклада, налога сотрудника и налога работодателя с введенной суммой, которая будет являться суммой с начала года.</span><span class="sxs-lookup"><span data-stu-id="a6851-122">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="a6851-123">С помощью этого списка кодов и сумм выполните действия по созданию выписки до доходах и оплате вручную с отключенным учетом для начальных сальдо для целей зарплаты.</span><span class="sxs-lookup"><span data-stu-id="a6851-123">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span> <span data-ttu-id="a6851-124">Учет отключается, поскольку не требуется выполнять разноску этой выписки по оплате для начального сальдо в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="a6851-124">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="a6851-125">Эта делалось в старой системе и перейдет в новую систему при настройке начальных сальдо в главной книге.</span><span class="sxs-lookup"><span data-stu-id="a6851-125">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="a6851-126">A.</span><span class="sxs-lookup"><span data-stu-id="a6851-126">A.</span></span> <span data-ttu-id="a6851-127">Порядок настройки кодов доходов для использования на начальных сальдо зарплаты</span><span class="sxs-lookup"><span data-stu-id="a6851-127">How to set up earnings codes to be used on payroll beginning balances</span></span>

<span data-ttu-id="a6851-128">При вводе начальных сальдо заработной платы убедитесь, что используемые коды дохода настроены с включенным параметром "Разрешить изменение ставок выписки по оплате".</span><span class="sxs-lookup"><span data-stu-id="a6851-128">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="a6851-129">Это позволит вручную ввести сумму из старой системы.</span><span class="sxs-lookup"><span data-stu-id="a6851-129">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="a6851-130">B.</span><span class="sxs-lookup"><span data-stu-id="a6851-130">B.</span></span> <span data-ttu-id="a6851-131">Создание выписки о доходах для сотрудника для начального сальдо</span><span class="sxs-lookup"><span data-stu-id="a6851-131">Create earnings statement for an employee to have a beginning balance</span></span>

<span data-ttu-id="a6851-132">Этот шаг вручную создает выписку о доходах для каждого работника за последний период оплаты старой системы, которая создает строки выписки о доходах в новой системе расчета зарплаты.</span><span class="sxs-lookup"><span data-stu-id="a6851-132">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="a6851-133">Введите одну строку на код дохода, сумму с начала года и часы.</span><span class="sxs-lookup"><span data-stu-id="a6851-133">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="a6851-134">Операции из примера:</span><span class="sxs-lookup"><span data-stu-id="a6851-134">The sample steps are as follows:</span></span>

1. <span data-ttu-id="a6851-135">Откройте страницу **Выписки о всех доходах** и нажмите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="a6851-135">Open the **All earnings statements** page and click **New**.</span></span>

    <span data-ttu-id="a6851-136">Введите следующее:</span><span class="sxs-lookup"><span data-stu-id="a6851-136">Enter the following:</span></span> 

    | <span data-ttu-id="a6851-137">Поле</span><span class="sxs-lookup"><span data-stu-id="a6851-137">Field</span></span>      | <span data-ttu-id="a6851-138">Стоимость</span><span class="sxs-lookup"><span data-stu-id="a6851-138">Value</span></span>                 |
    |------------|-----------------------|
    | <span data-ttu-id="a6851-139">Рабочий</span><span class="sxs-lookup"><span data-stu-id="a6851-139">Worker</span></span>     | <span data-ttu-id="a6851-140">Майкл Редмонд</span><span class="sxs-lookup"><span data-stu-id="a6851-140">Michael Redmond</span></span>       |
    | <span data-ttu-id="a6851-141">Цикл оплаты</span><span class="sxs-lookup"><span data-stu-id="a6851-141">Pay cycle</span></span>  | <span data-ttu-id="a6851-142">sm</span><span class="sxs-lookup"><span data-stu-id="a6851-142">sm</span></span>                    |
    | <span data-ttu-id="a6851-143">Платежный период</span><span class="sxs-lookup"><span data-stu-id="a6851-143">Pay period</span></span> | <span data-ttu-id="a6851-144">6.16.2017 - 6.30.2017</span><span class="sxs-lookup"><span data-stu-id="a6851-144">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="a6851-145">На вкладке **Строка выписки о доходах** введите следующее:</span><span class="sxs-lookup"><span data-stu-id="a6851-145">In the **Earnings statement line** tab, enter the following:</span></span>

    <span data-ttu-id="a6851-146">Строка 1: вкладка **Строка выписки о доходах**</span><span class="sxs-lookup"><span data-stu-id="a6851-146">Line 1: **Earning statement line** tab</span></span>

    | <span data-ttu-id="a6851-147">Поле</span><span class="sxs-lookup"><span data-stu-id="a6851-147">Field</span></span>            | <span data-ttu-id="a6851-148">Стоимость</span><span class="sxs-lookup"><span data-stu-id="a6851-148">Value</span></span>       |
    |------------------|-------------|
    | <span data-ttu-id="a6851-149">Код доходов</span><span class="sxs-lookup"><span data-stu-id="a6851-149">Earnings code</span></span>    | <span data-ttu-id="a6851-150">Обычная оплата</span><span class="sxs-lookup"><span data-stu-id="a6851-150">Regular pay</span></span> |
    | <span data-ttu-id="a6851-151">Количество</span><span class="sxs-lookup"><span data-stu-id="a6851-151">Quantity</span></span>         | <span data-ttu-id="a6851-152">1.00</span><span class="sxs-lookup"><span data-stu-id="a6851-152">1.00</span></span>        |
    | <span data-ttu-id="a6851-153">Курс</span><span class="sxs-lookup"><span data-stu-id="a6851-153">Rate</span></span>             | <span data-ttu-id="a6851-154">30,000</span><span class="sxs-lookup"><span data-stu-id="a6851-154">30,000</span></span>      |
    | <span data-ttu-id="a6851-155">Вкладка "Сведения по строке"</span><span class="sxs-lookup"><span data-stu-id="a6851-155">Line details tab</span></span> |             |
    | <span data-ttu-id="a6851-156">Руководство</span><span class="sxs-lookup"><span data-stu-id="a6851-156">Manual</span></span>           | <span data-ttu-id="a6851-157">(отмечено)</span><span class="sxs-lookup"><span data-stu-id="a6851-157">(marked)</span></span>    |

    <span data-ttu-id="a6851-158">Строка 2: вкладка **Строка выписки о доходах**</span><span class="sxs-lookup"><span data-stu-id="a6851-158">Line 2: **Earning statement line** tab</span></span>

    | <span data-ttu-id="a6851-159">Поле</span><span class="sxs-lookup"><span data-stu-id="a6851-159">Field</span></span>            | <span data-ttu-id="a6851-160">Стоимость</span><span class="sxs-lookup"><span data-stu-id="a6851-160">Value</span></span>    |
    |------------------|----------|
    | <span data-ttu-id="a6851-161">Код доходов</span><span class="sxs-lookup"><span data-stu-id="a6851-161">Earnings code</span></span>    | <span data-ttu-id="a6851-162">Премия</span><span class="sxs-lookup"><span data-stu-id="a6851-162">Bonus</span></span>    |
    | <span data-ttu-id="a6851-163">Количество</span><span class="sxs-lookup"><span data-stu-id="a6851-163">Quantity</span></span>         | <span data-ttu-id="a6851-164">1.0000</span><span class="sxs-lookup"><span data-stu-id="a6851-164">1.0000</span></span>   |
    | <span data-ttu-id="a6851-165">По норме</span><span class="sxs-lookup"><span data-stu-id="a6851-165">Rate</span></span>             | <span data-ttu-id="a6851-166">4250.00</span><span class="sxs-lookup"><span data-stu-id="a6851-166">4250.00</span></span>  |
    | <span data-ttu-id="a6851-167">Вкладка "Сведения по строке"</span><span class="sxs-lookup"><span data-stu-id="a6851-167">Line details tab</span></span> |          |
    | <span data-ttu-id="a6851-168">Руководство</span><span class="sxs-lookup"><span data-stu-id="a6851-168">Manual</span></span>           | <span data-ttu-id="a6851-169">(отмечено)</span><span class="sxs-lookup"><span data-stu-id="a6851-169">(marked)</span></span> |

    <span data-ttu-id="a6851-170">Строка 3: вкладка **Строка выписки о доходах**</span><span class="sxs-lookup"><span data-stu-id="a6851-170">Line 3: **Earning statement line** tab</span></span>

    | <span data-ttu-id="a6851-171">Поле</span><span class="sxs-lookup"><span data-stu-id="a6851-171">Field</span></span>           | <span data-ttu-id="a6851-172">Стоимость</span><span class="sxs-lookup"><span data-stu-id="a6851-172">Value</span></span>      |
    |-----------------|------------|
    | <span data-ttu-id="a6851-173">Код доходов</span><span class="sxs-lookup"><span data-stu-id="a6851-173">Earnings code</span></span>   | <span data-ttu-id="a6851-174">Комиссия</span><span class="sxs-lookup"><span data-stu-id="a6851-174">Commission</span></span> |
    | <span data-ttu-id="a6851-175">Количество</span><span class="sxs-lookup"><span data-stu-id="a6851-175">Quantity</span></span>        | <span data-ttu-id="a6851-176">1.0000</span><span class="sxs-lookup"><span data-stu-id="a6851-176">1.0000</span></span>     |
    | <span data-ttu-id="a6851-177">По норме</span><span class="sxs-lookup"><span data-stu-id="a6851-177">Rate</span></span>            | <span data-ttu-id="a6851-178">!,299.00</span><span class="sxs-lookup"><span data-stu-id="a6851-178">!,299.00</span></span>   |
    | <span data-ttu-id="a6851-179">По норме</span><span class="sxs-lookup"><span data-stu-id="a6851-179">Rate</span></span>            | <span data-ttu-id="a6851-180">1,299.00</span><span class="sxs-lookup"><span data-stu-id="a6851-180">1,299.00</span></span>   |
    | <span data-ttu-id="a6851-181">Вкладка "Сведения по строке"</span><span class="sxs-lookup"><span data-stu-id="a6851-181">Line detail tab</span></span> |            |
    | <span data-ttu-id="a6851-182">Руководство</span><span class="sxs-lookup"><span data-stu-id="a6851-182">Manual</span></span>          | <span data-ttu-id="a6851-183">(отмечено)</span><span class="sxs-lookup"><span data-stu-id="a6851-183">(Marked)</span></span>   |

    > [!NOTE]
    > <span data-ttu-id="a6851-184">Установка ползунка **Вручную** на значение **Да** на вкладке **Сведения по строке** для каждой строки выписки о доходах требуется для того, чтобы начальные сальдо зарплаты были введены для каждого работника.</span><span class="sxs-lookup"><span data-stu-id="a6851-184">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="a6851-185">В области **Действия** нажмите **Запустить выписку о доходах** USA-FED-ER-FICA.</span><span class="sxs-lookup"><span data-stu-id="a6851-185">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>
4. <span data-ttu-id="a6851-186">В области **Действия** щелкните **Выписка по оплате** для открытия страницы **Создать выписки по оплате** и настройте следующее:</span><span class="sxs-lookup"><span data-stu-id="a6851-186">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

    | <span data-ttu-id="a6851-187">Поле</span><span class="sxs-lookup"><span data-stu-id="a6851-187">Field</span></span>              | <span data-ttu-id="a6851-188">Стоимость</span><span class="sxs-lookup"><span data-stu-id="a6851-188">Value</span></span>     |
    |--------------------|-----------|
    | <span data-ttu-id="a6851-189">Дата оплаты</span><span class="sxs-lookup"><span data-stu-id="a6851-189">Payment date</span></span>       | <span data-ttu-id="a6851-190">6.30.2017</span><span class="sxs-lookup"><span data-stu-id="a6851-190">6/30/2017</span></span> |
    | <span data-ttu-id="a6851-191">Тип выполнения платежа</span><span class="sxs-lookup"><span data-stu-id="a6851-191">Payment run type</span></span>   | <span data-ttu-id="a6851-192">Руководство</span><span class="sxs-lookup"><span data-stu-id="a6851-192">Manual</span></span>    |
    | <span data-ttu-id="a6851-193">Отключить учет</span><span class="sxs-lookup"><span data-stu-id="a6851-193">Disable accounting</span></span> |   <span data-ttu-id="a6851-194">Да</span><span class="sxs-lookup"><span data-stu-id="a6851-194">Yes</span></span>     |

    > [!NOTE] 
    > <span data-ttu-id="a6851-195">Это доступно, только если тип выполнения платежа — "вручную" и если пользователь хочет отключить учет на период оплаты.</span><span class="sxs-lookup"><span data-stu-id="a6851-195">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

    <span data-ttu-id="a6851-196">Щелкните **ОК** и закройте **Infolog**.</span><span class="sxs-lookup"><span data-stu-id="a6851-196">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="a6851-197">Почему ползунок "Отключить учет" необходимо установить на значение "Да" при создании выписок по оплате?</span><span class="sxs-lookup"><span data-stu-id="a6851-197">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>

<span data-ttu-id="a6851-198">Установка ползунка на значение **Да** предотвращает распределение строк в выписке по оплате в главную книгу.</span><span class="sxs-lookup"><span data-stu-id="a6851-198">Setting the slider to **Yes** prevents lines in the pay statement from being distributed to General ledger.</span></span> <span data-ttu-id="a6851-199">Суммы главной книги были обновлены ранее при вводе сальдо из старой системы.</span><span class="sxs-lookup"><span data-stu-id="a6851-199">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="a6851-200">Ввод начальных сальдо для заработной платы позволяет создавать отчеты, которые включают сведения из предыдущего года, а также для определения ограничений для льгот и в налоговых целях.</span><span class="sxs-lookup"><span data-stu-id="a6851-200">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="a6851-201">C.</span><span class="sxs-lookup"><span data-stu-id="a6851-201">C.</span></span> <span data-ttu-id="a6851-202">Создание выписок по оплате для сотрудников</span><span class="sxs-lookup"><span data-stu-id="a6851-202">Create pay statements for employees</span></span>

<span data-ttu-id="a6851-203">После создания выписок по оплате с начальными сальдо необходимо проверить, что выписки по оплате точно отражают данные о заработной плате.</span><span class="sxs-lookup"><span data-stu-id="a6851-203">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="a6851-204">Необходимо также вручную обновить сведения о льготах и налогах, чтобы они соответствовали значения в предыдущей системе зарплаты.</span><span class="sxs-lookup"><span data-stu-id="a6851-204">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="a6851-205">Убедившись, что суммы из предыдущей системы заработной платы соответствуют суммам по текущим выпискам по оплате, необходимо финализировать выписки по оплате.</span><span class="sxs-lookup"><span data-stu-id="a6851-205">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="a6851-206">Откройте страницу **Все выписки по оплате**.</span><span class="sxs-lookup"><span data-stu-id="a6851-206">Open the **All pay statements** page.</span></span>
2. <span data-ttu-id="a6851-207">Выделите для последнюю созданную выписку по оплате для Майкла Редмонда</span><span class="sxs-lookup"><span data-stu-id="a6851-207">Highlight the last generated pay statement for Michael Redmond</span></span>
3. <span data-ttu-id="a6851-208">Щелкните **Изменит ь**, чтобы открыть страницу **Выписка по оплате**.</span><span class="sxs-lookup"><span data-stu-id="a6851-208">Click **Edit** to open the **Pay statement** page.</span></span>
4. <span data-ttu-id="a6851-209">Откройте вкладку **Льготные вычеты** и введите следующее:</span><span class="sxs-lookup"><span data-stu-id="a6851-209">Open the **Benefit deductions** tab and enter the following:</span></span>

    | <span data-ttu-id="a6851-210">Поле</span><span class="sxs-lookup"><span data-stu-id="a6851-210">Field</span></span>             | <span data-ttu-id="a6851-211">Стоимость</span><span class="sxs-lookup"><span data-stu-id="a6851-211">Value</span></span>            |
    |-------------------|------------------|
    | <span data-ttu-id="a6851-212">Льгота</span><span class="sxs-lookup"><span data-stu-id="a6851-212">Benefit</span></span>           | <span data-ttu-id="a6851-213">Сумма вычета</span><span class="sxs-lookup"><span data-stu-id="a6851-213">Deduction amount</span></span> |
    | <span data-ttu-id="a6851-214">401K</span><span class="sxs-lookup"><span data-stu-id="a6851-214">401K</span></span>              | <span data-ttu-id="a6851-215">Участие</span><span class="sxs-lookup"><span data-stu-id="a6851-215">Participate</span></span>      |
    | <span data-ttu-id="a6851-216">Dental</span><span class="sxs-lookup"><span data-stu-id="a6851-216">Dental</span></span>            | <span data-ttu-id="a6851-217">SubSp</span><span class="sxs-lookup"><span data-stu-id="a6851-217">SubSp</span></span>            |
    | <span data-ttu-id="a6851-218">Расходы на вуз care</span><span class="sxs-lookup"><span data-stu-id="a6851-218">Dep care spending</span></span> | <span data-ttu-id="a6851-219">Участие</span><span class="sxs-lookup"><span data-stu-id="a6851-219">Participate</span></span>      |
    | <span data-ttu-id="a6851-220">Vision</span><span class="sxs-lookup"><span data-stu-id="a6851-220">Vision</span></span>            | <span data-ttu-id="a6851-221">SupSp</span><span class="sxs-lookup"><span data-stu-id="a6851-221">SupSp</span></span>            |

5. <span data-ttu-id="a6851-222">На вкладке **Льготные вклады** и введите следующее:</span><span class="sxs-lookup"><span data-stu-id="a6851-222">In the **Benefit contributions** tab and enter the following:</span></span>

    | <span data-ttu-id="a6851-223">Поле</span><span class="sxs-lookup"><span data-stu-id="a6851-223">Field</span></span>   | <span data-ttu-id="a6851-224">Стоимость</span><span class="sxs-lookup"><span data-stu-id="a6851-224">Value</span></span>               |
    |---------|---------------------|
    | <span data-ttu-id="a6851-225">Льгота</span><span class="sxs-lookup"><span data-stu-id="a6851-225">Benefit</span></span> | <span data-ttu-id="a6851-226">Сумма вклада</span><span class="sxs-lookup"><span data-stu-id="a6851-226">Contribution amount</span></span> |
    | <span data-ttu-id="a6851-227">401K</span><span class="sxs-lookup"><span data-stu-id="a6851-227">401K</span></span>    | <span data-ttu-id="a6851-228">Участие</span><span class="sxs-lookup"><span data-stu-id="a6851-228">Participate</span></span>         |
    | <span data-ttu-id="a6851-229">Dental</span><span class="sxs-lookup"><span data-stu-id="a6851-229">Dental</span></span>  | <span data-ttu-id="a6851-230">SubSp</span><span class="sxs-lookup"><span data-stu-id="a6851-230">SubSp</span></span>               |
    | <span data-ttu-id="a6851-231">Vision</span><span class="sxs-lookup"><span data-stu-id="a6851-231">Vision</span></span>  | <span data-ttu-id="a6851-232">SubSp</span><span class="sxs-lookup"><span data-stu-id="a6851-232">SubSp</span></span>               |

6. <span data-ttu-id="a6851-233">На вкладке **Налоговые вычеты** введите следующее:</span><span class="sxs-lookup"><span data-stu-id="a6851-233">In the **Tax deductions** tab, enter the following:</span></span>

    | <span data-ttu-id="a6851-234">Поле</span><span class="sxs-lookup"><span data-stu-id="a6851-234">Field</span></span>           | <span data-ttu-id="a6851-235">Стоимость</span><span class="sxs-lookup"><span data-stu-id="a6851-235">Value</span></span>            |
    |-----------------|------------------|
    | <span data-ttu-id="a6851-236">Код налога</span><span class="sxs-lookup"><span data-stu-id="a6851-236">Tax code</span></span>        | <span data-ttu-id="a6851-237">Сумма вычета</span><span class="sxs-lookup"><span data-stu-id="a6851-237">Deduction amount</span></span> |
    | <span data-ttu-id="a6851-238">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="a6851-238">USA-FED-ER-FICA</span></span> | <span data-ttu-id="a6851-239">1600.00</span><span class="sxs-lookup"><span data-stu-id="a6851-239">1600.00</span></span>          |
    | <span data-ttu-id="a6851-240">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="a6851-240">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="a6851-241">825.75</span><span class="sxs-lookup"><span data-stu-id="a6851-241">825.75</span></span>           |

7. <span data-ttu-id="a6851-242">На вкладке **Налоговые вклады** введите следующее:</span><span class="sxs-lookup"><span data-stu-id="a6851-242">In the **Tax contributions** tab enter the following:</span></span>
8. <span data-ttu-id="a6851-243">Щелкните **Рассчитать**.</span><span class="sxs-lookup"><span data-stu-id="a6851-243">Click **Calculate**.</span></span>

    > [!IMPORTANT] 
    > <span data-ttu-id="a6851-244">Проверьте итоги в выписке по оплате,чтобы они соответствовали значениям с начала года в старой системе для работника.</span><span class="sxs-lookup"><span data-stu-id="a6851-244">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="a6851-245">Можно не торопиться с финализацией на следующем шаге, чтобы выполнить общую проверку всех выписок по оплате в совокупности.</span><span class="sxs-lookup"><span data-stu-id="a6851-245">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="a6851-246">После проверки просмотрите все выписки по оплате и финализируйте их.</span><span class="sxs-lookup"><span data-stu-id="a6851-246">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="a6851-247">При необходимости такой же процесс может выполняться с шагом по кварталу для всех предыдущих кварталов каждого года.</span><span class="sxs-lookup"><span data-stu-id="a6851-247">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="a6851-248">Это необходим только в том случае, если клиенту нужно просмотреть данные по кварталам без возвращения к старой системе.</span><span class="sxs-lookup"><span data-stu-id="a6851-248">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="a6851-249">Если была допущена ошибка при вводе начальных сальдо для сотрудника</span><span class="sxs-lookup"><span data-stu-id="a6851-249">If you make a mistake Entering Beginning Balances for an Employee</span></span>

<span data-ttu-id="a6851-250">Имеется возможность отменить ввод и повторить проводки.</span><span class="sxs-lookup"><span data-stu-id="a6851-250">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="a6851-251">Чтобы отменить проводку, необходимо выполнить следующие действия на странице **Все выписки по оплате**.</span><span class="sxs-lookup"><span data-stu-id="a6851-251">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="a6851-252">Щелкните **Отменить**.</span><span class="sxs-lookup"><span data-stu-id="a6851-252">Click **Reverse**.</span></span>
2. <span data-ttu-id="a6851-253">Щелкните **Да** при появлении сообщения "При сторнировании этой выписки по оплате будет создана сторнирующая выписка по оплате, корреспондирующая с данной выпиской.</span><span class="sxs-lookup"><span data-stu-id="a6851-253">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="a6851-254">Ни одну из выписок по оплате нельзя будет изменить.</span><span class="sxs-lookup"><span data-stu-id="a6851-254">Neither pay statement can be edited.</span></span> <span data-ttu-id="a6851-255">Вы действительно хотите сторнировать эту выписку по оплате?</span><span class="sxs-lookup"><span data-stu-id="a6851-255">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="a6851-256">.</span><span class="sxs-lookup"><span data-stu-id="a6851-256">displays.</span></span> 

<span data-ttu-id="a6851-257">После реверсирования выписки по оплате можно создать новую выписку по оплате для работника из выписке о доходах, созданной ранее.</span><span class="sxs-lookup"><span data-stu-id="a6851-257">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="a6851-258">Не забудьте исправить все неправильные строки в выписке о доходах перед созданием новой выписки по оплате, а затем создайте новую выписку по оплате с правильными суммами.</span><span class="sxs-lookup"><span data-stu-id="a6851-258">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]