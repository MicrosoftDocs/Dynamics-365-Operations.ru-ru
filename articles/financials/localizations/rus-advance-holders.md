---
title: Подотчетные лица для России
description: В этой теме рассматривается регистрация и настройка подотчетных лиц для России.
author: ShylaThompson
manager: AnnBe
ms.date: 10/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorkerAdvHolderTableListPage_RU, HcmWorkerAdvHolderTable_RU
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Russia
ms.author: shylaw
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: d8e5b2ec55c6886edff1f5ce3a627974e93061ac
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545426"
---
# <a name="advance-holders-for-russia"></a><span data-ttu-id="29d89-103">Подотчетные лица для России</span><span class="sxs-lookup"><span data-stu-id="29d89-103">Advance holders for Russia</span></span>
[!include [banner](../includes/banner.md)]

## <a name="set-up-parameters-for-advance-holders"></a><span data-ttu-id="29d89-104">Настройка параметров для подотчетных лиц</span><span class="sxs-lookup"><span data-stu-id="29d89-104">Set up parameters for advance holders</span></span>

1. <span data-ttu-id="29d89-105">Выберите **Расчеты с поставщиками** \> **Настройка** \> **Параметры расчетов с поставщиками**.</span><span class="sxs-lookup"><span data-stu-id="29d89-105">Select **Accounts payable** \> **Setup** \> **Accounts payable parameters**.</span></span>
2. <span data-ttu-id="29d89-106">На вкладке **Подотчетные лица** в поле **Профиль разноски** выберите профиль разноски, который должен использоваться для выполнения проводок по подотчетным лицам по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="29d89-106">On the **Advance holders** tab, in the **Posting profile** field, select the default posting profile that should be used to complete transactions for advance holders.</span></span>

    > [!NOTE]
    > <span data-ttu-id="29d89-107">Дополнительные сведения см. в разделе "Настройка профилей разноски для учетных ваучеров" далее в данной теме.</span><span class="sxs-lookup"><span data-stu-id="29d89-107">For more information, see the "Set up posting profiles for accounting vouchers" section later in this topic.</span></span>

3. <span data-ttu-id="29d89-108">Установите для параметра **Подотчетное лицо по умолчанию** значение **Да**, чтобы установить текущего пользователя в качестве подотчетного лица.</span><span class="sxs-lookup"><span data-stu-id="29d89-108">Set the **Set default advance holder** option to **Yes** to set the current user as the advance holder.</span></span>
4. <span data-ttu-id="29d89-109">Установите для параметра **Сортировка подотчетных лиц** значение **Да**, чтобы подотчетные лица отображались вверху сетки на странице **Подотчетные лица**.</span><span class="sxs-lookup"><span data-stu-id="29d89-109">Set the **Advance holder sorting** option to **Yes** to show advance holders at the top of the grid on the **Advance holders** page.</span></span>
5. <span data-ttu-id="29d89-110">Установите для параметра **Выдача под отчет при открытом сальдо** значение **Да**, чтобы разрешить выдачу денежных авансов подотчетным лицам с открытым положительным сальдо.</span><span class="sxs-lookup"><span data-stu-id="29d89-110">Set the **Issue when balance is open** option to **Yes** to allow cash advances to be issued to advance holders who have an open positive balance.</span></span>
6. <span data-ttu-id="29d89-111">Установите для параметра **Автоматическое сопоставление** значение **Да**, если требуется автоматическое сопоставление проводок.</span><span class="sxs-lookup"><span data-stu-id="29d89-111">Set the **Automatic settlement** option to **Yes** if automatic transactions settlement is required.</span></span>
7. <span data-ttu-id="29d89-112">Установите для параметра **Сопоставление по профилям** значение **Да**, чтобы сопоставлялись только проводки с идентичным профилем разноски.</span><span class="sxs-lookup"><span data-stu-id="29d89-112">Set the **Settlement by profile** option to **Yes** to settle transactions only with an identical posting profile.</span></span>
8. <span data-ttu-id="29d89-113">На экспресс-вкладке **Закрытие сальдо** в области **Закрытие сальдо через кассу** в поле **Имя** выберите код журнала кассовых ордеров.</span><span class="sxs-lookup"><span data-stu-id="29d89-113">On the **Balance closing** FastTab, under **Balance closing via cash**, in the **Name** field, select the cash slip journal code.</span></span> <span data-ttu-id="29d89-114">Этот код журнала используется для создания расходных кассовых ордеров и приходных ордеров при закрытии сальдо подотчетного лица по кассе.</span><span class="sxs-lookup"><span data-stu-id="29d89-114">This journal code is used to generate cash disbursement slips and reimbursement slips when an advance holder's balances are closed through cash.</span></span>

    > [!NOTE]
    > <span data-ttu-id="29d89-115">Все журналы имеют тип **Денежные средства**.</span><span class="sxs-lookup"><span data-stu-id="29d89-115">All journals are of the **Cash** type.</span></span>

9. <span data-ttu-id="29d89-116">В поле **Денежные средства** выберите кассовый счет для определения ваучеров, которые используются для закрытия сальдо подотчетного лица.</span><span class="sxs-lookup"><span data-stu-id="29d89-116">In the **Cash** field, select the cash account to determine the vouchers that are used to close the balances for the advance holder.</span></span>
10. <span data-ttu-id="29d89-117">В области **Закрытие сальдо через банк** в поле **Имя** выберите код журнала для проводок для закрытия сальдо через банк.</span><span class="sxs-lookup"><span data-stu-id="29d89-117">Under **Balance closing via bank**, in the **Name** field, select the journal code for transactions to close the balances through a bank.</span></span>
11. <span data-ttu-id="29d89-118">В поле **Тип счета** выберите **Банк** для закрытия сальдо подотчетного лица через банк.</span><span class="sxs-lookup"><span data-stu-id="29d89-118">In the **Account type** field, select **Bank** to close the balances for an advance holder through a bank.</span></span>
12. <span data-ttu-id="29d89-119">В поле **Счет ГК** выберите код банковского счета для закрытия сальдо подотчетного лица через банк.</span><span class="sxs-lookup"><span data-stu-id="29d89-119">In the **Main account** field, select the bank account code to close the balances for an advance holder through a bank.</span></span>
13. <span data-ttu-id="29d89-120">На вкладке **Номерные серии** определите коды номерных серий для следующих ссылок:</span><span class="sxs-lookup"><span data-stu-id="29d89-120">On the **Number sequences** tab, define number sequences codes for the following references:</span></span>

    - <span data-ttu-id="29d89-121">Авансовый отчет</span><span class="sxs-lookup"><span data-stu-id="29d89-121">Advance report</span></span>
    - <span data-ttu-id="29d89-122">Ваучер ГК по АО</span><span class="sxs-lookup"><span data-stu-id="29d89-122">Advance report voucher</span></span>
    - <span data-ttu-id="29d89-123">Ваучер сопоставления</span><span class="sxs-lookup"><span data-stu-id="29d89-123">Settlement voucher</span></span>
    - <span data-ttu-id="29d89-124">Ваучер курсовой разницы (Подотчетные лица)</span><span class="sxs-lookup"><span data-stu-id="29d89-124">Exchange adjustment voucher (Advance holders)</span></span>

14. <span data-ttu-id="29d89-125">Выберите **Сохранить** или закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="29d89-125">Select **Save**, or close the page.</span></span>

## <a name="set-up-an-advance-holder-group"></a><span data-ttu-id="29d89-126">Настройка группы подотчетных лиц.</span><span class="sxs-lookup"><span data-stu-id="29d89-126">Set up an advance holder group</span></span>

<span data-ttu-id="29d89-127">Необходимо создать группу подотчетных лиц, чтобы сгруппировать подотчетные лица.</span><span class="sxs-lookup"><span data-stu-id="29d89-127">You must create an advance holder group to group advance holders.</span></span> <span data-ttu-id="29d89-128">Например, можно сгруппировать подотчетные лица по ваучерам, рассчитываемым в одном счете.</span><span class="sxs-lookup"><span data-stu-id="29d89-128">For example, you can group advance holders by vouchers that are calculated in a single account.</span></span>

1. <span data-ttu-id="29d89-129">Выберите **Расчеты с поставщиками** \> **Настройка** \> **Подотчетные лица** \> **Группы подотчетных лиц**.</span><span class="sxs-lookup"><span data-stu-id="29d89-129">Select **Accounts payable** \> **Setup** \> **Advance holders** \> **Advance holder groups**.</span></span>
2. <span data-ttu-id="29d89-130">Выберите **Создать**, чтобы создать новую группу подотчетных лиц, или **Редактировать** для корректировки существующей группы.</span><span class="sxs-lookup"><span data-stu-id="29d89-130">Select **New** to create a new advance holder group or **Edit** to adjust an existing group.</span></span>
3. <span data-ttu-id="29d89-131">В поле **Группа** введите код для новой группы подотчетных лиц.</span><span class="sxs-lookup"><span data-stu-id="29d89-131">In the **Group** field, enter the code for the advance holder group.</span></span>
4. <span data-ttu-id="29d89-132">В поле **Описание** введите описание группы подотчетных лиц.</span><span class="sxs-lookup"><span data-stu-id="29d89-132">In the **Description** field, enter a description of the advance holder group.</span></span>
5. <span data-ttu-id="29d89-133">В поле **Корр. счет** выберите корреспондентский счет ГК, используемый для группы подотчетных лиц.</span><span class="sxs-lookup"><span data-stu-id="29d89-133">In the **Offset account** field, select the general ledger offset account to use for the advance holder group.</span></span>
6. <span data-ttu-id="29d89-134">Выберите **Сохранить** или закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="29d89-134">Select **Save**, or close the page.</span></span>

## <a name="set-up-posting-profiles-for-accounting-vouchers"></a><span data-ttu-id="29d89-135">Настройка профилей разноски для учетных ваучеров</span><span class="sxs-lookup"><span data-stu-id="29d89-135">Set up posting profiles for accounting vouchers</span></span>

<span data-ttu-id="29d89-136">Для счета операций можно установить следующие профили разноски:</span><span class="sxs-lookup"><span data-stu-id="29d89-136">You can set up the following posting profiles for an account of operations:</span></span>

- <span data-ttu-id="29d89-137">Один счет ГК для всех подотчетных лиц</span><span class="sxs-lookup"><span data-stu-id="29d89-137">One ledger account for all advance holders</span></span>
- <span data-ttu-id="29d89-138">Отдельный счет ГК для каждой группы подотчетных лиц</span><span class="sxs-lookup"><span data-stu-id="29d89-138">A separate ledger account for each group of advance holders</span></span>
- <span data-ttu-id="29d89-139">Отдельный счет ГК для каждого подотчетного лица</span><span class="sxs-lookup"><span data-stu-id="29d89-139">A separate ledger account for each advance holder</span></span>

1. <span data-ttu-id="29d89-140">Выберите **Расчеты с поставщиками** \> **Настройка** \> **Подотчетные лица** \> **Профили разноски по подотч. лицам**.</span><span class="sxs-lookup"><span data-stu-id="29d89-140">Select **Accounts payable** \> **Setup** \> **Advance holders** \> **Employee posting profiles**.</span></span>
2. <span data-ttu-id="29d89-141">Выберите **Создать**, чтобы создать новый профиль разноски, или **Редактировать** для корректировки существующего профиля.</span><span class="sxs-lookup"><span data-stu-id="29d89-141">Select **New** to create a new posting profile or **Edit** to adjust an existing profile.</span></span>
3. <span data-ttu-id="29d89-142">В поле **Профиль разноски** введите идентификатор обрабатываемого профиля разноски.</span><span class="sxs-lookup"><span data-stu-id="29d89-142">In the **Posting profile** field, enter the profile ID of the posting profile that is being processed.</span></span>
4. <span data-ttu-id="29d89-143">В поле **Описание** введите описание профиля разноски.</span><span class="sxs-lookup"><span data-stu-id="29d89-143">In the **Description** field, enter a description of the posting profile.</span></span>
5. <span data-ttu-id="29d89-144">На экспресс-вкладке **Табличные ограничения** в поле **Разрешить пустое значение аналитики** выберите условие, при котором сопоставления проводок, связанных с начислениями и операциями закрывающих платежей, могут обрабатываться, если не указаны значения аналитик.</span><span class="sxs-lookup"><span data-stu-id="29d89-144">On the **Table restrictions** FastTab, in the **Allow empty dimension value** field, select the condition under which settlements that are related to accruals and closing payment operations can be processed if dimension values aren't specified.</span></span> <span data-ttu-id="29d89-145">Имеются следующие варианты:</span><span class="sxs-lookup"><span data-stu-id="29d89-145">The following options are available:</span></span>

    - <span data-ttu-id="29d89-146">**Нет** — проводки не сопоставляются независимо от того, указаны значения аналитик или нет.</span><span class="sxs-lookup"><span data-stu-id="29d89-146">**No** – Transactions aren't settled, regardless of whether the dimension values are specified.</span></span>
    - <span data-ttu-id="29d89-147">**Авто** — автоматические проводки сопоставляются независимо от того, указаны значения аналитик или нет.</span><span class="sxs-lookup"><span data-stu-id="29d89-147">**Auto** – Automatic transactions are settled, regardless of whether the dimension values are specified.</span></span>
    - <span data-ttu-id="29d89-148">**Вручную** — сделанные вручную проводки сопоставляются независимо от того, указаны значения аналитик или нет.</span><span class="sxs-lookup"><span data-stu-id="29d89-148">**Manual** – Manual transactions are settled, regardless of whether the dimension values are specified.</span></span>
    - <span data-ttu-id="29d89-149">**Всегда** — все проводки сопоставляются независимо от того, указаны значения аналитик или нет.</span><span class="sxs-lookup"><span data-stu-id="29d89-149">**Always** – All transactions are settled, regardless of whether the dimension values are specified.</span></span>

    > [!NOTE]
    > <span data-ttu-id="29d89-150">Это поле позволяет игнорировать значения аналитик при создании отдельных проводок.</span><span class="sxs-lookup"><span data-stu-id="29d89-150">This field lets you ignore the values of dimensions when individual transactions are created.</span></span>

6. <span data-ttu-id="29d89-151">На экспресс-вкладке **Настройка** выберите **Добавить**, чтобы создать новую запись для данных профиля разноски.</span><span class="sxs-lookup"><span data-stu-id="29d89-151">On the **Setup** FastTab, select **Add** to create a new record for posting profile details.</span></span>
7. <span data-ttu-id="29d89-152">В поле **Действительно для** выберите уровень группирования для настройки профиля разноски.</span><span class="sxs-lookup"><span data-stu-id="29d89-152">In the **Valid for** field, select the level of grouping for the setup of the posting profile.</span></span> <span data-ttu-id="29d89-153">Имеются следующие варианты:</span><span class="sxs-lookup"><span data-stu-id="29d89-153">The following options are available:</span></span>

    - <span data-ttu-id="29d89-154">**Таблица** – этот вариант устанавливается только для одного подотчетного лица.</span><span class="sxs-lookup"><span data-stu-id="29d89-154">**Table** – This option is set for only one advance holder.</span></span>
    - <span data-ttu-id="29d89-155">**Группа** – этот вариант устанавливается для группы подотчетных лиц.</span><span class="sxs-lookup"><span data-stu-id="29d89-155">**Group** – This option is set for a group of advance holders.</span></span>
    - <span data-ttu-id="29d89-156">**Все** – этот вариант устанавливается для всех подотчетных лиц.</span><span class="sxs-lookup"><span data-stu-id="29d89-156">**All** – This option is set for all advance holders.</span></span>

8. <span data-ttu-id="29d89-157">В поле **Ссылка** выберите соответствующую ссылку.</span><span class="sxs-lookup"><span data-stu-id="29d89-157">In the **Reference** field, select the corresponding reference.</span></span>

    > [!NOTE]
    > <span data-ttu-id="29d89-158">Значение в этом поле можно выбрать, только если выбран вариант **Таблица** или **Группа** в поле **Действительно для**.</span><span class="sxs-lookup"><span data-stu-id="29d89-158">You can select a value in this field only if you selected **Table** or **Group** in the **Valid for** field.</span></span>

9. <span data-ttu-id="29d89-159">В поле **Суммирующий счет** выберите счет для отображения проводок по подотчетным лицам.</span><span class="sxs-lookup"><span data-stu-id="29d89-159">In the **Summary account** field, select the account that should reflect transactions for the advance holders.</span></span>
10. <span data-ttu-id="29d89-160">В поле **Задать** выберите фокус аналитик для управления сопоставлением.</span><span class="sxs-lookup"><span data-stu-id="29d89-160">In the **Set** field, select the dimension focus for settlement control.</span></span>

    > [!NOTE]
    > <span data-ttu-id="29d89-161">Определенный набор аналитик показывает, что контроль аналитики активирован.</span><span class="sxs-lookup"><span data-stu-id="29d89-161">The specified dimension set indicates that dimension control is activated.</span></span>

11. <span data-ttu-id="29d89-162">Выберите **Сохранить** или закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="29d89-162">Select **Save**, or close the page.</span></span>

## <a name="set-up-the-terms-of-payment"></a><span data-ttu-id="29d89-163">Настройка условий оплаты</span><span class="sxs-lookup"><span data-stu-id="29d89-163">Set up the terms of payment</span></span>

<span data-ttu-id="29d89-164">Необходимо установить условия оплаты при регистрации покупки товаров у поставщика через подотчетное лицо.</span><span class="sxs-lookup"><span data-stu-id="29d89-164">You must set up the terms of payment when you register the purchase of goods from a vendor through an advance holder.</span></span> <span data-ttu-id="29d89-165">Закупку выполняет подотчетное лицо.</span><span class="sxs-lookup"><span data-stu-id="29d89-165">The advance holder makes the purchase.</span></span>

1. <span data-ttu-id="29d89-166">Выберите **Расчеты с поставщиками** \> **Настройка платежей** \> **Условия оплаты**.</span><span class="sxs-lookup"><span data-stu-id="29d89-166">Select **Accounts payable** \> **Payment setup** \> **Terms of payment**.</span></span>
2. <span data-ttu-id="29d89-167">Выберите **Создать**, чтобы создать новую запись условий оплаты, или **Редактировать** для корректировки существующей записи.</span><span class="sxs-lookup"><span data-stu-id="29d89-167">Select **New** to create a new terms of payment record or **Edit** to adjust an existing record.</span></span>
3. <span data-ttu-id="29d89-168">В поле **Условия оплаты** введите код для условий оплаты.</span><span class="sxs-lookup"><span data-stu-id="29d89-168">In the **Terms of payment** field, enter the code for the terms of payment.</span></span>
4. <span data-ttu-id="29d89-169">В поле **Описание** введите описание для условий оплаты.</span><span class="sxs-lookup"><span data-stu-id="29d89-169">In the **Description** field, enter a description of the terms of payment.</span></span>
5. <span data-ttu-id="29d89-170">На экспресс-вкладке **Настройка** в поле **Способ оплаты** выберите **Наложенный платеж**.</span><span class="sxs-lookup"><span data-stu-id="29d89-170">On the **Setup** FastTab, in the **Payment method** field, select **C.O.D.**</span></span>
6. <span data-ttu-id="29d89-171">Установите для параметра **Наличная оплата** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="29d89-171">Set the **Cash payment** option to **Yes**.</span></span>
7. <span data-ttu-id="29d89-172">Установите для параметра **От подотчетного лица** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="29d89-172">Set the **From advance holder** option to **Yes**.</span></span>
8. <span data-ttu-id="29d89-173">Выберите **Сохранить** или закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="29d89-173">Select **Save**, or close the page.</span></span>

## <a name="set-up-the-per-diem-expense-rates"></a><span data-ttu-id="29d89-174">Настройка ставок суточной оплаты расходов</span><span class="sxs-lookup"><span data-stu-id="29d89-174">Set up the per diem expense rates</span></span>

<span data-ttu-id="29d89-175">Ставки расходов используются для создания авансового отчета по суточным расходам.</span><span class="sxs-lookup"><span data-stu-id="29d89-175">Expense rates are used to generate an advance report for per diem expenses.</span></span> <span data-ttu-id="29d89-176">Они также могут использоваться для автоматического расчета стандартных сумм и сумм перерасхода.</span><span class="sxs-lookup"><span data-stu-id="29d89-176">They are also used for automatic calculation of standard and over-rate amounts.</span></span>

1. <span data-ttu-id="29d89-177">Выберите **Расчеты с поставщиками** \> **Настройка** \> **Подотчетные лица** \> **Ставки расходов**.</span><span class="sxs-lookup"><span data-stu-id="29d89-177">Select **Accounts payable** \> **Setup** \> **Advance holders** \> **Expense rates**.</span></span>
2. <span data-ttu-id="29d89-178">Выберите **Создать**, чтобы создать новый расход, или **Редактировать** для корректировки существующего расхода.</span><span class="sxs-lookup"><span data-stu-id="29d89-178">Select **New** to create a new expense or **Edit** to adjust an existing expense.</span></span>
3. <span data-ttu-id="29d89-179">В поле **Расход** введите код расхода.</span><span class="sxs-lookup"><span data-stu-id="29d89-179">In the **Expense** field, enter the expense code.</span></span>
4. <span data-ttu-id="29d89-180">В поле **Описание** введите описание расхода.</span><span class="sxs-lookup"><span data-stu-id="29d89-180">In the **Description** field, enter a description of the expense.</span></span>
5. <span data-ttu-id="29d89-181">В поле **Ставка** введите стандартное установленное значение для данного расхода.</span><span class="sxs-lookup"><span data-stu-id="29d89-181">In the **Rate** field, enter the standard established value for this expense.</span></span>
6. <span data-ttu-id="29d89-182">В поле **Валюта** выберите код валюты, в котором регистрируются операции для данного расхода.</span><span class="sxs-lookup"><span data-stu-id="29d89-182">In the **Currency** field, select the currency code that operations for this expense are registered in.</span></span>
7. <span data-ttu-id="29d89-183">На экспресс-вкладке **Настройка** в области **Норма** в поле **Счет ГК** выберите бухгалтерский отчет для отражения обычных расходов.</span><span class="sxs-lookup"><span data-stu-id="29d89-183">On the **Setup** FastTab, under **Rate**, in the **Main account** field, select the accounting statement that should reflect normal charges.</span></span>
8. <span data-ttu-id="29d89-184">В области **Сверх нормы** в поле **Счет ГК** выберите бухгалтерский отчет для отражения расходов сверх нормы.</span><span class="sxs-lookup"><span data-stu-id="29d89-184">Under **Over rate**, in the **Main account** field, select the accounting statement that should reflect over-rate charges.</span></span>
9. <span data-ttu-id="29d89-185">В области **Налог** и **Налоги сверх нормы** в поле **Налоговая группа** выберите налоговую группу для расчета налога для продаж и покупок на суммах в пределах нормы и сверх нормы.</span><span class="sxs-lookup"><span data-stu-id="29d89-185">Under both **Sales tax** and **Taxes over norm**, in the **Sales tax group** field, select the sales tax group that should be used to calculate sales tax for sales and purchases on normal and over-rate amounts.</span></span>
10. <span data-ttu-id="29d89-186">В области **Налог** и **Налоги сверх нормы** в поле **Налоговая группа номенклатур** выберите налоговую группу номенклатур для расчета налога для номенклатуры на суммах в пределах нормы и сверх нормы.</span><span class="sxs-lookup"><span data-stu-id="29d89-186">Under both **Sales tax** and **Taxes over norm**, in the **Item sales tax group** field, select the item sales tax group that should be used to calculate sales tax for an item on normal and over-rate amounts.</span></span>
11. <span data-ttu-id="29d89-187">Если суммы включают налог, в областях **Налог** и **Налоги сверх нормы** установите для параметра **Суммы включают налог** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="29d89-187">If the amounts include sales tax, under both **Sales tax** and **Taxes over norm**, set the **Amounts includes sales tax** option to **Yes**.</span></span>
12. <span data-ttu-id="29d89-188">В разделе **Налоги сверх нормы** в поле **Разноска сверх нормы** выберите операцию, которая должна использоваться для разноски расходов сверх нормы.</span><span class="sxs-lookup"><span data-stu-id="29d89-188">Under **Taxes over norm**, in the **Posting over norm** field, select the operation that should be used to post over-norm expenses.</span></span>
13. <span data-ttu-id="29d89-189">На экспресс-вкладке **Финансовые аналитики** в областях **Финансовые аналитики** и **Финансовые аналитики сверх нормы** выберите значения аналитик в проводке для связанных аналитик.</span><span class="sxs-lookup"><span data-stu-id="29d89-189">On the **Financial dimensions** FastTab, under both **Financial dimensions** and **Financial dimensions over rate**, select the transaction dimension values for the related dimensions.</span></span>
14. <span data-ttu-id="29d89-190">Выберите **Сохранить** или закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="29d89-190">Select **Save**, or close the page.</span></span>

## <a name="worker-table-numbers-for-advance-holders"></a><span data-ttu-id="29d89-191">Табельные номера работников для подотчетных лиц</span><span class="sxs-lookup"><span data-stu-id="29d89-191">Worker table numbers for advance holders</span></span>

<span data-ttu-id="29d89-192">Работник может являться сотрудником или подрядчиком и занимать в организации несколько должностей.</span><span class="sxs-lookup"><span data-stu-id="29d89-192">A worker can be an employee or a contractor, and can hold several positions in an organization.</span></span> <span data-ttu-id="29d89-193">Сотрудник или подрядчик также может являться подотчетным лицом, отвечающим за сумму расходов, предоставляемую организацией.</span><span class="sxs-lookup"><span data-stu-id="29d89-193">An employee or a contractor can also be an advance holder who is accountable for the expense amount that the organization provides.</span></span> <span data-ttu-id="29d89-194">Чтобы задать работника в качестве подотчетного лица, введите уникальный код работника в поле **Код работника** на странице **Работник**.</span><span class="sxs-lookup"><span data-stu-id="29d89-194">To specify a worker as an advance holder, you must enter a unique worker ID in the **Worker ID** field on the **Worker** page.</span></span> <span data-ttu-id="29d89-195">Также необходимо установить для параметра **Подотчетное лицо** значение **Да** на странице **Подотчетные лица**, чтобы указать, что выбранный работник является подотчетным лицом.</span><span class="sxs-lookup"><span data-stu-id="29d89-195">You must also set the **Advance holder** option to **Yes** on the **Advance holders** page, to indicate that the selected worker is an advance holder.</span></span>

<span data-ttu-id="29d89-196">Разноска проводок по таким работникам может выполняться при помощи счетов подотчетных лиц.</span><span class="sxs-lookup"><span data-stu-id="29d89-196">Transactions for these workers can be posted by using advance holder accounts.</span></span> <span data-ttu-id="29d89-197">Указанный для каждого подотчетного лица идентификатор работника можно использовать для отслеживания всех проводок подотчетного лица.</span><span class="sxs-lookup"><span data-stu-id="29d89-197">The worker ID that is specified for each advance holder can be used to track all advance holder transactions.</span></span> <span data-ttu-id="29d89-198">Этот номер используется в качестве номера счета для проводок по подотчетному лицу на страницах **Общие журналы** и **Проводки по подотч. лицам**.</span><span class="sxs-lookup"><span data-stu-id="29d89-198">This number is retrieved as an account number for advance holder transactions on the **General journals** and **Advance holder transactions** pages.</span></span>

## <a name="set-up-the-advance-holder"></a><span data-ttu-id="29d89-199">Настройка подотчетного лица</span><span class="sxs-lookup"><span data-stu-id="29d89-199">Set up the advance holder</span></span>

[<span data-ttu-id="29d89-200">Создание подотчетного лица</span><span class="sxs-lookup"><span data-stu-id="29d89-200">Create an advance holder</span></span>](emea-advance-holders.md#create-an-advance-holder)
