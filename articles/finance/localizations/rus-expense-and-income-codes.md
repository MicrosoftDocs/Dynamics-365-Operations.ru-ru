---
title: Коды расходов и доходов
description: В данном разделе содержится информация о кодов расходов и доходов, доступных для России.
author: anasyash
manager: AnnBe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.author: roschlom
ms.search.validFrom: 2019-03-01
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: d07f56fcd59c97fe3095a04a6245a0d70470aeb8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230178"
---
# <a name="expense-and-income-codes"></a><span data-ttu-id="0d11b-103">Коды расходов и доходов</span><span class="sxs-lookup"><span data-stu-id="0d11b-103">Expense and income codes</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d11b-104">Коды расходов и доходов создаются на странице **коды расходов и доходов**.</span><span class="sxs-lookup"><span data-stu-id="0d11b-104">Expense and income codes are created on the **Expense and income codes** page.</span></span> <span data-ttu-id="0d11b-105">Иерархическая структура позволяет группировать доходы и расходы в соответствии со строками декларации по налогу на прибыль.</span><span class="sxs-lookup"><span data-stu-id="0d11b-105">The hierarchical structure lets you group income and expenses according to the lines of the profit tax declaration.</span></span> <span data-ttu-id="0d11b-106">Таким образом, список кодов расходов и доходов содержит все коды доходов и расходов, которые используются в налоговой отчетности.</span><span class="sxs-lookup"><span data-stu-id="0d11b-106">Therefore, the list of expense and income codes contains all the income and expense codes that are used in tax reporting.</span></span> <span data-ttu-id="0d11b-107">Обороты по кодам родительских доходов и расходов состоят из оборотов по кодам дочерних доходов и расходов.</span><span class="sxs-lookup"><span data-stu-id="0d11b-107">Turnovers on parent income and expense codes consist of the turnovers on child income and expense codes.</span></span> <span data-ttu-id="0d11b-108">Список кодов расходов и доходов синхронизируется со списком финансовых аналитик, выбранных в поле **Налоговая аналитика** на вкладке **налог на прибыль** на странице **Параметры главной книги**.</span><span class="sxs-lookup"><span data-stu-id="0d11b-108">The list of expense and income codes is synced with the list of financial dimensions selected in the **Tax dimension** field on the **Profit tax** tab of the **General ledger parameters** page.</span></span> <span data-ttu-id="0d11b-109">Этот механизм используется для расчета декларации налога на прибыль.</span><span class="sxs-lookup"><span data-stu-id="0d11b-109">This mechanism is used to calculate the profit tax declaration.</span></span> <span data-ttu-id="0d11b-110">Дополнительные сведения см. в разделе [Декларация по налогу на прибыль](rus-profit-tax-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="0d11b-110">For more information, see [Profit tax declaration](rus-profit-tax-declaration.md).</span></span>

<span data-ttu-id="0d11b-111">Значение поля **ExpenseAndIncomeCode** должно быть установлено в следующих местах:</span><span class="sxs-lookup"><span data-stu-id="0d11b-111">You should set the value of the **ExpenseAndIncomeCode** field in the following places:</span></span>

- <span data-ttu-id="0d11b-112">В первичных документах, таких как заказы на покупку, заказы на продажу, авансовые отчеты и журналы запасов, а также в основные записи, например, счета ГК и основные средства.</span><span class="sxs-lookup"><span data-stu-id="0d11b-112">In primary documents such as purchase orders, sales orders, advance reports, and inventory journals, and in master records such as main accounts and fixed assets.</span></span>
- <span data-ttu-id="0d11b-113">В проводках поставщика, клиента, книге учета и проводках по запасам.</span><span class="sxs-lookup"><span data-stu-id="0d11b-113">In vendor, customer, ledger, and inventory transactions.</span></span>

## <a name="create-an-expense-or-income-code"></a><span data-ttu-id="0d11b-114">Создание кода расходов или доходов</span><span class="sxs-lookup"><span data-stu-id="0d11b-114">Create an expense or income code</span></span>

1.  <span data-ttu-id="0d11b-115">Перейдите к **Налог** \> **Настройка** \> **Налог на прибыль** \> **Коды расходов**.</span><span class="sxs-lookup"><span data-stu-id="0d11b-115">Go to **Tax** \> **Setup** \> **Profit tax** \> **Expense codes**.</span></span>

    ![Страница коды расходов](media/1_Expense_codes.png)

2.  <span data-ttu-id="0d11b-117">В области действий выберите **Древовидное представление**, чтобы просмотреть коды расходов и доходов в виде дерева, а затем выберите **создать**, чтобы создать код.</span><span class="sxs-lookup"><span data-stu-id="0d11b-117">On the Action Pane, select **Tree view** to view expense and income codes as a tree, and then select **New** to create a code.</span></span>
3.  <span data-ttu-id="0d11b-118">В поле **Код расхода** введите код расходов или доходов.</span><span class="sxs-lookup"><span data-stu-id="0d11b-118">In the **Expense code** field, enter the expense or income code.</span></span> <span data-ttu-id="0d11b-119">Код должен быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="0d11b-119">The code should be unique.</span></span>

    <span data-ttu-id="0d11b-120">Обычно при нумерации кодов следует придерживаться структурного принципа.</span><span class="sxs-lookup"><span data-stu-id="0d11b-120">Typically, when codes are numbered, you should adhere to a hierarchical principle.</span></span> <span data-ttu-id="0d11b-121">Например, при создании дочернего кода для кода **90100000** он должен начинаться с **901**, например **901010000** или **901020000**.</span><span class="sxs-lookup"><span data-stu-id="0d11b-121">For example, if you create a child code for code **90100000**, it should start with **901**, such as **901010000** or **901020000**.</span></span>

4.  <span data-ttu-id="0d11b-122">В поле **Имя** введите подробное описание кода расходов или дохода.</span><span class="sxs-lookup"><span data-stu-id="0d11b-122">In the **Name** field, enter a detailed description of the expense or income code.</span></span>
5.  <span data-ttu-id="0d11b-123">На экспресс-вкладке **Общие** настройте следующие поля:</span><span class="sxs-lookup"><span data-stu-id="0d11b-123">On the **General** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="0d11b-124">В поле **Краткое описание** введите краткое название кода расходов или дохода.</span><span class="sxs-lookup"><span data-stu-id="0d11b-124">In the **Short description** field, enter the short name of the expense or income code.</span></span>
    - <span data-ttu-id="0d11b-125">В поле **Тип кода** выберите тип кода: **доход**, **расход** или **неизвестное**.</span><span class="sxs-lookup"><span data-stu-id="0d11b-125">In the **Code type** field, select the type of code: **Income**, **Issue** or **Unknown**.</span></span>
    - <span data-ttu-id="0d11b-126">В разделе **Аналитика** установите для параметра **Блокировка** значение **Да**, чтобы остановить синхронизацию выбранного кода расходов или дохода.</span><span class="sxs-lookup"><span data-stu-id="0d11b-126">In the **Dimension** section, set the **Locked** option to **Yes** to stop synchronization of the selected expense or income code.</span></span>
    - <span data-ttu-id="0d11b-127">Необязательно: в разделе **родительский код** в поле **родительский код** выберите родительский код для создания иерархической структуры.</span><span class="sxs-lookup"><span data-stu-id="0d11b-127">Optional: In the **Parent code** section, in the **Parent code** field, select a parent code to create a hierarchical structure.</span></span>
    - <span data-ttu-id="0d11b-128">В разделе **подоходный налог** в поле **налоговый код** выберите налоговый код, который должен использоваться для расчета суммы налоговых активов и налоговых обязательств для кода расходов или доходов.</span><span class="sxs-lookup"><span data-stu-id="0d11b-128">In the **Income tax** section, in the **Sales tax code** field, select the sales tax code that should be used to calculate the amount of tax assets and tax liabilities for the expense or income code.</span></span>

6.  <span data-ttu-id="0d11b-129">На экспресс-вкладке **Настройка** можно выбрать регистры, которые будут использоваться для расчета сумм и итоговых значений для кодов расходов или доходов.</span><span class="sxs-lookup"><span data-stu-id="0d11b-129">On the **Set up** FastTab, you can select the registers that will be used to calculate the amounts and totals for expense or income codes.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0d11b-130">Можно выбрать регистры только для кодов, которые не являются родительскими кодами.</span><span class="sxs-lookup"><span data-stu-id="0d11b-130">You can select registers only for codes that aren't parent codes.</span></span>

    <span data-ttu-id="0d11b-131">В разделе **Доступные регистры** выберите регистры, а затем нажмите кнопку со стрелкой вправо, чтобы переместить их в раздел **выбранные регистры**.</span><span class="sxs-lookup"><span data-stu-id="0d11b-131">In the **Available registers** section, select the registers, and then select the right arrow button to move them to the **Selected registers** section.</span></span>

    <span data-ttu-id="0d11b-132">Или, на панели операций выберите **По умолчанию \> По умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="0d11b-132">Alternatively, on the Action Pane, select **Default \> Default**.</span></span> <span data-ttu-id="0d11b-133">В этом случае система автоматически предлагает регистры и переносит их в раздел **выбранные регистры**.</span><span class="sxs-lookup"><span data-stu-id="0d11b-133">In this case, the system automatically suggests registers and moves them to **Selected registers** section.</span></span> <span data-ttu-id="0d11b-134">Регистр для кода дохода или расхода будет предложен в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="0d11b-134">A register will be suggested for an income or expense code in the following situations:</span></span>

    -   <span data-ttu-id="0d11b-135">Код дохода или расхода или родительский код был выбран в параметрах регистра.</span><span class="sxs-lookup"><span data-stu-id="0d11b-135">The income or expense code, or its parent code, was selected in the register settings.</span></span>
    -   <span data-ttu-id="0d11b-136">Код дохода или расхода или родительский код использовался в последовательности расчета для параметров регистра оцененных расходов.</span><span class="sxs-lookup"><span data-stu-id="0d11b-136">The income or expense code, or its parent code, was used in the sequence of calculation for rated expense register settings.</span></span>
    -   <span data-ttu-id="0d11b-137">Регистр предварительно настроен таким образом, что он используется по умолчанию при расчете итоговых значений для кода расходов или доходов.</span><span class="sxs-lookup"><span data-stu-id="0d11b-137">The register is preconfigured so that it's used by default when totals are calculated for the expense or income code.</span></span> <span data-ttu-id="0d11b-138">Можно найти примерный список кодов расходов и доходов в юридическом лице **RUMF**.</span><span class="sxs-lookup"><span data-stu-id="0d11b-138">You can find an example list of expense and income codes in the **RUMF** legal entity.</span></span>

7.  <span data-ttu-id="0d11b-139">В области действий выберите **настройку счета ГК** для выбора счетов ГК, по которым будут назначены проводки для кода дохода или расхода.</span><span class="sxs-lookup"><span data-stu-id="0d11b-139">On the Action Pane, select **Ledger account setup** to select the ledger accounts that transactions will be assigned to for the income or expense code.</span></span>

    <span data-ttu-id="0d11b-140">Например, суммы для проводок ГК по **дебету 62.110** и по **кредиту 90.110**, где финансовая аналитика **ExpenseAndIncomeCode** установлена как **901010200** или оставлена пустой, будут назначены коду дохода **901010200** (**Выручка от продаж товаров**).</span><span class="sxs-lookup"><span data-stu-id="0d11b-140">For example, amounts for ledger transactions **Debit 62.110** and **Credit 90.110**, where the **ExpenseAndIncomeCode** financial dimension is either set to **901010200** or left blank, will be assigned to income code **901010200** (**Revenue from sales of goods**).</span></span>

    ![Страница связи кода расхода и главной книги, экспресс-вкладка Финансовые аналитики](media/2_Expense_code_and_ledger_relation.png)

8.  <span data-ttu-id="0d11b-142">На странице **связи кода расхода и главной книги** в заголовке установите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0d11b-142">On the **Expense code and ledger relation** page, in the header, set the following values:</span></span>

    - <span data-ttu-id="0d11b-143">В каждом из двух полей **Допустимо для**, выберите одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="0d11b-143">In each of the two **Valid for** fields, select one of the following values:</span></span>

       - <span data-ttu-id="0d11b-144">**Таблица** — параметр применяется к отдельному счету.</span><span class="sxs-lookup"><span data-stu-id="0d11b-144">**Table** – The setting applies to a separate account.</span></span>
       - <span data-ttu-id="0d11b-145">**Группа** — параметр применяется к группе диапазона счетов.</span><span class="sxs-lookup"><span data-stu-id="0d11b-145">**Group** – The setting applies to an account interval group.</span></span>
       - <span data-ttu-id="0d11b-146">**Все** — параметр применяется ко всем счетам.</span><span class="sxs-lookup"><span data-stu-id="0d11b-146">**All** – The setting applies to all accounts.</span></span>

    -   <span data-ttu-id="0d11b-147">Настройте поля **Дебетовый счет** и **кредитный счет** на основе значения соответствующего поля **Допустимо для**:</span><span class="sxs-lookup"><span data-stu-id="0d11b-147">Set the **Debit account** and **Credit account** fields, based on the value of the corresponding **Valid for** field:</span></span>

        - <span data-ttu-id="0d11b-148">Если в поле **Допустимо для** указано значение **Таблица**, выберите счет учета.</span><span class="sxs-lookup"><span data-stu-id="0d11b-148">If the **Valid for** field is set to **Table**, select a ledger account.</span></span>
        - <span data-ttu-id="0d11b-149">Если в поле **допустимо для** указано значение **Группа**, выберите код для группы диапазона счетов.</span><span class="sxs-lookup"><span data-stu-id="0d11b-149">If the **Valid for** field is set to **Group**, select the code for an account interval group.</span></span>
        - <span data-ttu-id="0d11b-150">Если в поле **допустимо для** указано значение **все**, оставьте поле пустым.</span><span class="sxs-lookup"><span data-stu-id="0d11b-150">If the **Valid for** field is set to **All**, leave the field blank.</span></span>

9.  <span data-ttu-id="0d11b-151">На экспресс-вкладке **финансовые аналитики** в разделах **Финансовые аналитики по умолчанию** и **корреспондирующие аналитики** можно указать коды финансовых аналитик, которые будут использоваться при расчете итоговых значений для кода расходов или доходов, в дополнение к настройке счетов ГК, выбранных ранее.</span><span class="sxs-lookup"><span data-stu-id="0d11b-151">On the **Financial dimensions** FastTab, in the **Default financial dimensions** and **Offset dimensions** sections, you can specify financial dimension codes that account entries will be used for when totals are calculated on the expense or income code, in addition to the setup of ledger accounts that you selected earlier.</span></span>

    <span data-ttu-id="0d11b-152">Например, в полях **соглашение**, **ExpenseAndIncomeCode** и **работник** выберите аналитики для счета и корр. счета.</span><span class="sxs-lookup"><span data-stu-id="0d11b-152">For example, in the **Agreement**, **ExpenseAndIncomeCode**, and **Worker** fields, select the dimensions for the account and the offset account.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0d11b-153">Аналитика **ExpenseAndIncomeCode** выбрана в качестве аналитики для кодов расходов и доходов на странице **Параметры главной книги**.</span><span class="sxs-lookup"><span data-stu-id="0d11b-153">The **ExpenseAndIncomeCode** dimension is selected as the dimension for expense and income codes on the **General ledger parameters** page.</span></span> <span data-ttu-id="0d11b-154">Это значение нельзя изменить.</span><span class="sxs-lookup"><span data-stu-id="0d11b-154">It can’t be changed.</span></span> <span data-ttu-id="0d11b-155">Если для параметра **Использовать пустое значение аналитики** установлено значение **Да**, код расхода или дохода также будет включать проводки с одинаковыми счетами ГК, но поле **ExpenseAndIncomeCode** остается пустым.</span><span class="sxs-lookup"><span data-stu-id="0d11b-155">If you set the **Empty dimension using** option to **Yes**, the expense or income code will also include transactions that have the same ledger accounts, but the **ExpenseAndIncomeCode** field is blank.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]