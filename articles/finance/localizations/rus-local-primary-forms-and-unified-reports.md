---
title: Наличные деньги — локальные основные формы и унифицированные отчеты
description: В этой теме приводятся сведения об отчетах по проводкам по кассе, доступных для компаний с русским контекстом.
author: v-nadyuz
manager: AnnBe
ms.date: 11/13/2019
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
ms.openlocfilehash: 45e5661e3103568c0b313450aa6eeb4b7ef432f3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4962537"
---
# <a name="cash---local-primary-forms-and-unified-reports"></a><span data-ttu-id="e5407-103">Наличные деньги — локальные основные формы и унифицированные отчеты</span><span class="sxs-lookup"><span data-stu-id="e5407-103">Cash - Local primary forms and unified reports</span></span>
[!include [banner](../includes/banner.md)]


<span data-ttu-id="e5407-104">Несколько отчетов о проводках по кассе доступны в компаниях с русским контекстом.</span><span class="sxs-lookup"><span data-stu-id="e5407-104">Several reports about cash transactions are available in companies that have Russian context.</span></span>

<span data-ttu-id="e5407-105">В разделе [Мелкие наличные деньги для Восточной Европы и России](emea-petty-cash.md) представлены сведения о следующих отчетах:</span><span class="sxs-lookup"><span data-stu-id="e5407-105">The [Petty cash for Eastern Europe and Russia](emea-petty-cash.md) topic provides information about the following reports:</span></span>

- <span data-ttu-id="e5407-106">Журнал кассовых ордеров</span><span class="sxs-lookup"><span data-stu-id="e5407-106">Slip journal</span></span>
- <span data-ttu-id="e5407-107">Отчет по кассовой книге</span><span class="sxs-lookup"><span data-stu-id="e5407-107">Cash book report</span></span>
- <span data-ttu-id="e5407-108">Касса — Выверка ГК</span><span class="sxs-lookup"><span data-stu-id="e5407-108">Cash – Ledger reconciliation</span></span>
- <span data-ttu-id="e5407-109">Отчет по выписке по кассе</span><span class="sxs-lookup"><span data-stu-id="e5407-109">Cash statement report</span></span>
- <span data-ttu-id="e5407-110">Отчет по проводкам по кассе</span><span class="sxs-lookup"><span data-stu-id="e5407-110">Cash transactions report</span></span>
- <span data-ttu-id="e5407-111">Отчет журнала регистрации документов</span><span class="sxs-lookup"><span data-stu-id="e5407-111">Journal of registration of documents report</span></span>

<span data-ttu-id="e5407-112">В данном разделе содержится информация о следующих дополнительных отчетах:</span><span class="sxs-lookup"><span data-stu-id="e5407-112">This topic provides information about following additional reports:</span></span>

- <span data-ttu-id="e5407-113">Объявление на взнос наличными</span><span class="sxs-lookup"><span data-stu-id="e5407-113">Cash due announcement</span></span>
- <span data-ttu-id="e5407-114">Акт инвентаризации денежных средств (ИНВ - 15)</span><span class="sxs-lookup"><span data-stu-id="e5407-114">Cash counting statement (INV-15)</span></span>

## <a name="preliminary-setup"></a><span data-ttu-id="e5407-115">Предварительная настройка</span><span class="sxs-lookup"><span data-stu-id="e5407-115">Preliminary setup</span></span>

### <a name="set-up-a-number-sequence"></a><span data-ttu-id="e5407-116">Настройка номерной серии</span><span class="sxs-lookup"><span data-stu-id="e5407-116">Set up a number sequence</span></span>

1. <span data-ttu-id="e5407-117">Перейдите в раздел **Управление банком и кассовыми операциями \> Настройка \> Параметры управления банком и кассовыми операциями**.</span><span class="sxs-lookup"><span data-stu-id="e5407-117">Go to **Cash and bank management \> Setup \> Cash and bank management parameters**.</span></span>
2. <span data-ttu-id="e5407-118">На вкладке **Номерные серии** в поле **Код номерной серии** для ссылки **Объявление на взнос наличными** выберите код номерной серии.</span><span class="sxs-lookup"><span data-stu-id="e5407-118">On the **Number sequences** tab, in the **Number sequence code** field for the **Cash due announcement** reference, select a number sequence code.</span></span>

### <a name="set-up-a-bank-transaction-type-to-allow-for-a-cash-due-announcement-report"></a><span data-ttu-id="e5407-119">Настройка типа банковской проводки, которая будет разрешена для отчета об объявлениях на взнос наличными</span><span class="sxs-lookup"><span data-stu-id="e5407-119">Set up a bank transaction type to allow for a Cash due announcement report</span></span>

1. <span data-ttu-id="e5407-120">Перейдите в раздел **Управление банком и кассовыми операциями \> Настройка \> Типы банковских проводок**.</span><span class="sxs-lookup"><span data-stu-id="e5407-120">Go to **Cash and bank management \> Setup \> Bank transaction types**.</span></span>
2. <span data-ttu-id="e5407-121">В строке для типа проводки установите флажок **Разрешить объявления на взнос наличными**, чтобы можно было создавать и распечатывать отчет **Объявление на взнос наличными** деньгах для ваучеров, использующих этот тип проводки.</span><span class="sxs-lookup"><span data-stu-id="e5407-121">In the row for the transaction type, select the **Allow cash due announcement** check box so that a **Cash due announcement** report can be generated and printed for vouchers that use that transaction type.</span></span>

## <a name="cash-due-announcement-report"></a><span data-ttu-id="e5407-122">Отчет объявления на взнос наличными</span><span class="sxs-lookup"><span data-stu-id="e5407-122">Cash due announcement report</span></span>

<span data-ttu-id="e5407-123">Отчет **Объявление на взнос наличными** используется для отправки мелких наличных денег в банк.</span><span class="sxs-lookup"><span data-stu-id="e5407-123">The **Cash due announcement** report is used to send petty cash to the bank.</span></span>

<span data-ttu-id="e5407-124">Отчет **Объявление на взнос наличными** может быть распечатан со страницы **Общие журналы** или **Журнал кассовых ордеров**.</span><span class="sxs-lookup"><span data-stu-id="e5407-124">You can print a **Cash due announcement** report from either the **General journals** page or the **Slip journal** page.</span></span>

### <a name="generate-and-print-a-cash-due-announcement-report-from-the-general-journals-page"></a><span data-ttu-id="e5407-125">Создание и печать отчета об объявлении на взнос наличными со страницы "Общие журналы"</span><span class="sxs-lookup"><span data-stu-id="e5407-125">Generate and print a Cash due announcement report from the General journals page</span></span>

1. <span data-ttu-id="e5407-126">Перейдите к **Главная книга \> Записи в журнале \> Общие журналы**.</span><span class="sxs-lookup"><span data-stu-id="e5407-126">Go to **General ledger \> Journal entries \> General journals**.</span></span>
2. <span data-ttu-id="e5407-127">Выберите журнал, затем в области действий выберите **Строки**.</span><span class="sxs-lookup"><span data-stu-id="e5407-127">Select a journal, and then, on the Action Pane, select **Lines**.</span></span>
3. <span data-ttu-id="e5407-128">Создайте строку для отправки мелких наличных денег в банк.</span><span class="sxs-lookup"><span data-stu-id="e5407-128">Create a line for sending petty cash to the bank.</span></span> <span data-ttu-id="e5407-129">Выберите банковский счет в поле **Счет** или **Корр.счет**.</span><span class="sxs-lookup"><span data-stu-id="e5407-129">Select a bank account in either the **Account** field or the **Offset account** field.</span></span>
4. <span data-ttu-id="e5407-130">На вкладке **Платеж** в поле **Тип банковской проводки** выберите тип проводки, для которого ранее был установлен флажок **Разрешить объявление на взнос наличными** для данного раздела.</span><span class="sxs-lookup"><span data-stu-id="e5407-130">On the **Payment** tab, in the **Bank transaction type** field, select the transaction type that you selected the **Allow cash due announcement** check box for earlier in this topic.</span></span>
5. <span data-ttu-id="e5407-131">В области действий выберите **Печать \> Объявление на взнос наличными** для создания и печати отчета.</span><span class="sxs-lookup"><span data-stu-id="e5407-131">On the Action Pane, select **Print \> Cash due announcement** to generate and print the report.</span></span> <span data-ttu-id="e5407-132">Отчет создается как документ Microsoft Excel, в котором используется шаблон для формы **0402001**.</span><span class="sxs-lookup"><span data-stu-id="e5407-132">The report is generated as a Microsoft Excel document that uses the template for form **0402001**.</span></span>

    ![Отчет объявления на взнос наличными](media/cash-primary-01.png)
    
    <span data-ttu-id="e5407-134">В созданной строке поле **Объявление на взнос наличными** задано и не может редактироваться.</span><span class="sxs-lookup"><span data-stu-id="e5407-134">On the line that you created, the **Cash due announcement** field is set and can't edited.</span></span>

6. <span data-ttu-id="e5407-135">В области действий выберите **Функции \> Отменить объявление на взнос наличными** для отмены документа, созданного для строки.</span><span class="sxs-lookup"><span data-stu-id="e5407-135">On the Action Pane, select **Functions \> Cancel cash due announcement** to cancel the document that was generated for the line.</span></span> <span data-ttu-id="e5407-136">Поле, содержащее ссылку на документ, удаляется, а строка становится редактируемой.</span><span class="sxs-lookup"><span data-stu-id="e5407-136">The field that contains a link to the document is cleared, and the line becomes editable.</span></span>

### <a name="generate-and-print-a-cash-due-announcement-report-from-the-slip-journal-page"></a><span data-ttu-id="e5407-137">Создание и печать отчета об объявлении на взнос наличными со страницы "Журнал кассовых ордеров"</span><span class="sxs-lookup"><span data-stu-id="e5407-137">Generate and print a Cash due announcement report from the Slip journal page</span></span>

1. <span data-ttu-id="e5407-138">Выберите **Управление банком и кассовыми операциями \> Проводки по кассе \> Журнал кассовых ордеров**.</span><span class="sxs-lookup"><span data-stu-id="e5407-138">Go to **Cash and bank management \> Cash transactions \> Slip journal**.</span></span>
2. <span data-ttu-id="e5407-139">Создайте строку журнала кассовых ордеров для отправки мелких наличных денег в банк, а затем утвердите ее.</span><span class="sxs-lookup"><span data-stu-id="e5407-139">Create a slip journal line for sending petty cash to the bank, and then approve it.</span></span>
3. <span data-ttu-id="e5407-140">Чтобы распечатать отчет **Объявление на взнос наличными**, используйте те же шаги, которые использовались для печати отчета на странице **Общие журналы**.</span><span class="sxs-lookup"><span data-stu-id="e5407-140">To print the **Cash due announcement** report, use the same steps that you used to print the report from the **General journals** page.</span></span>

### <a name="view-and-reprint-a-cash-due-announcement-report"></a><span data-ttu-id="e5407-141">Просмотр и повторная печать отчета об объявлении на взнос наличными</span><span class="sxs-lookup"><span data-stu-id="e5407-141">View and reprint a Cash due announcement report</span></span>

1.  <span data-ttu-id="e5407-142">Перейдите **Управление банком и кассовыми операциями \> Запросы и отчеты \> Объявление на взнос наличными**.</span><span class="sxs-lookup"><span data-stu-id="e5407-142">Go to **Cash and bank management \> Inquiries and reports \> Cash due announcement**.</span></span>
2.  <span data-ttu-id="e5407-143">На странице **Журнал объявления на взнос наличными** показаны все созданные отчеты **Объявления на взнос наличными**.</span><span class="sxs-lookup"><span data-stu-id="e5407-143">The **Cash due announcement journal** page shows all the **Cash due announcement** reports that have been generated.</span></span> <span data-ttu-id="e5407-144">Выберите документ на панели операций нажмите одну из следующих кнопок:</span><span class="sxs-lookup"><span data-stu-id="e5407-144">Select a document, and then, on the Action Pane, select one of the following buttons:</span></span>

    - <span data-ttu-id="e5407-145">**Журнал** — открыть журнал, в котором был создан документ.</span><span class="sxs-lookup"><span data-stu-id="e5407-145">**Journal** – Open the journal where you generated the document.</span></span>
    - <span data-ttu-id="e5407-146">**Печать** — печать документа.</span><span class="sxs-lookup"><span data-stu-id="e5407-146">**Print** – Print the document.</span></span>
    - <span data-ttu-id="e5407-147">**Отмена** — отмена документа.</span><span class="sxs-lookup"><span data-stu-id="e5407-147">**Cancel** – Cancel the document.</span></span>


> [!NOTE]  
> <span data-ttu-id="e5407-148">На странице **Банковские счета** можно просматривать и повторно печатать отчеты **Объявление на взнос наличными**, которые были созданы для конкретного банковского счета.</span><span class="sxs-lookup"><span data-stu-id="e5407-148">On the **Bank accounts** page, you can view and reprint **Cash due announcement** reports that were generated for a specific bank account.</span></span> <span data-ttu-id="e5407-149">В области действий на вкладке **Управление платежами** в группе **Связанные сведения** выберите **Объявление на взнос наличными**, чтобы открыть страницу **Журнал объявлений на взнос наличными**.</span><span class="sxs-lookup"><span data-stu-id="e5407-149">On the Action Pane, on the **Manage payments** tab, in the **Related information** group, select **Cash due announcement** to open the **Cash due announcement journal** page.</span></span>

## <a name="cash-counting-statement-inv-15-report"></a><span data-ttu-id="e5407-150">Отчет акта инвентаризации денежных средств (ИНВ-15)</span><span class="sxs-lookup"><span data-stu-id="e5407-150">Cash counting statement (INV-15) report</span></span>

<span data-ttu-id="e5407-151">Отчет **Акт инвентаризации денежных средств (ИНВ-15)** используется для акта инвентаризации денежных средств. Создание и печать акта инвентаризации запасов может потребоваться в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="e5407-151">The **Cash counting statement (INV-15)** report is used for the cash counting act. You might want to generate and print the inventory counting act in the following situations:</span></span>

-  <span data-ttu-id="e5407-152">Один счет мелких наличных денег включает в себя несколько валют.</span><span class="sxs-lookup"><span data-stu-id="e5407-152">A single petty cash account includes different currencies.</span></span>
-  <span data-ttu-id="e5407-153">Один кассовый счет включает различные типы активов, такие как **Наличные деньги**, **Марки**, **Ценные бумаги**.</span><span class="sxs-lookup"><span data-stu-id="e5407-153">A single cash account includes different asset types, such as **Cash**, **Stamps**, or **Securities**.</span></span>

<span data-ttu-id="e5407-154">Перед созданием акта инвентаризации денежных средств вычислите корректировку валютного курса.</span><span class="sxs-lookup"><span data-stu-id="e5407-154">Before you generate the cash counting act, calculate the exchange rate adjustment.</span></span> <span data-ttu-id="e5407-155">Затем выполняйте следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="e5407-155">Then follow these steps.</span></span>

1. <span data-ttu-id="e5407-156">Выберите **Управление банком и кассовыми операциями \> Запросы и отчеты \> Обороты по денежным счетам \> Отчет акта инвентаризации денежных средств**.</span><span class="sxs-lookup"><span data-stu-id="e5407-156">Go to **Cash and bank management \> Inquiries and reports \> Cash reports \> Cash counting statement report**.</span></span>
2. <span data-ttu-id="e5407-157">В верхней части страницы **Акт инвентаризации денежных средств (ИНВ-15)** выполните следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="e5407-157">In the upper part of the **Cash counting statement (INV – 15)** page, follow these steps:</span></span>
    
      <span data-ttu-id="e5407-158">a.</span><span class="sxs-lookup"><span data-stu-id="e5407-158">a.</span></span> <span data-ttu-id="e5407-159">В поле **Касса** выберите кассу для учета.</span><span class="sxs-lookup"><span data-stu-id="e5407-159">In the **Cash** field, select the cash account to count.</span></span>  
     
      <span data-ttu-id="e5407-160">b.</span><span class="sxs-lookup"><span data-stu-id="e5407-160">b.</span></span> <span data-ttu-id="e5407-161">В поле **Номер документа** укажите номер документа, на основе которого должен быть выполнен запас.</span><span class="sxs-lookup"><span data-stu-id="e5407-161">In the **Document number** field, specify the number of the document that the inventory that is done should be based on.</span></span>
      
      <span data-ttu-id="e5407-162">c.</span><span class="sxs-lookup"><span data-stu-id="e5407-162">c.</span></span> <span data-ttu-id="e5407-163">В поле **Дата инвентаризации** укажите дату инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="e5407-163">In the **Counting date** field, specify the date of counting.</span></span>
      
      <span data-ttu-id="e5407-164">дн.</span><span class="sxs-lookup"><span data-stu-id="e5407-164">d.</span></span> <span data-ttu-id="e5407-165">Установите для параметра **Печать названия кассового счета** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="e5407-165">Set the **Print cash account name** option to **Yes**.</span></span>
      
      <span data-ttu-id="e5407-166">e.</span><span class="sxs-lookup"><span data-stu-id="e5407-166">e.</span></span> <span data-ttu-id="e5407-167">Настройте для параметра **Приложение** значение **Да**, чтобы создать приложение к акту инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="e5407-167">Set the **Supplement** option to **Yes** to create the supplement to the counting act.</span></span>
            
<span data-ttu-id="e5407-168">Если касса позволяет выполнять учет в разных валютах, параметр **Разные валюты** устанавливается в значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="e5407-168">If the cash account allows for accounting in different currencies, the **More currencies** option is set to **Yes**.</span></span>

3. <span data-ttu-id="e5407-169">В нижней части страницы отображаются строки, в которых доступны вычисленные данные о денежных средствах.</span><span class="sxs-lookup"><span data-stu-id="e5407-169">The lower part of the page shows the lines where calculated data about cash is available.</span></span> <span data-ttu-id="e5407-170">Строки также можно создать вручную.</span><span class="sxs-lookup"><span data-stu-id="e5407-170">You can also manually create lines.</span></span> <span data-ttu-id="e5407-171">Эта часть страницы содержит следующие поля:</span><span class="sxs-lookup"><span data-stu-id="e5407-171">This part of the page includes the following fields:</span></span>

    - <span data-ttu-id="e5407-172">**Тип актива** — по умолчанию для этого поля установлено значение **Наличные деньги**.</span><span class="sxs-lookup"><span data-stu-id="e5407-172">**Asset type** – By default, this field is set to **Cash**.</span></span> <span data-ttu-id="e5407-173">Чтобы добавить строку, использующую другой тип актива, выберите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="e5407-173">To add a line that uses a different asset type, select **New**.</span></span> <span data-ttu-id="e5407-174">При создании новой строки можно выбрать одно из следующих значений: **Наличные деньги**, **Марки**, **Ценные бумаги** или **Другое**.</span><span class="sxs-lookup"><span data-stu-id="e5407-174">When you create a new line, you can select one of the following values: **Cash**, **Stamps**, **Securities**, or **Other**.</span></span>
    - <span data-ttu-id="e5407-175">**Текст** — указать тип актива.</span><span class="sxs-lookup"><span data-stu-id="e5407-175">**Text** – Specify the asset type.</span></span> <span data-ttu-id="e5407-176">Это поле доступно, только если выбрано значение **Другое** в поле **Тип актива**.</span><span class="sxs-lookup"><span data-stu-id="e5407-176">This field is available only if you select **Other** in the **Asset type** field.</span></span>
    - <span data-ttu-id="e5407-177">**Валюта** — валюта для выбранного типа актива.</span><span class="sxs-lookup"><span data-stu-id="e5407-177">**Currency** – The currency for the selected asset type.</span></span>
    - <span data-ttu-id="e5407-178">**Сумма инвентаризации (валюта)** — баланс указанного типа актива в указанной валюте.</span><span class="sxs-lookup"><span data-stu-id="e5407-178">**Counted amount (currency)** – The balance of the specified asset type in the specified currency.</span></span> <span data-ttu-id="e5407-179">Значение в этом поле можно изменять.</span><span class="sxs-lookup"><span data-stu-id="e5407-179">You can edit this field.</span></span>
    - <span data-ttu-id="e5407-180">**Разнесенная сумма (валюта)** — введите разнесенную сумму на основе результатов запасов.</span><span class="sxs-lookup"><span data-stu-id="e5407-180">**Posted amount (currency)** – Enter the posted amount, based on the results of the inventory.</span></span>
    - <span data-ttu-id="e5407-181">**Валютный курс** — валютный курс указанной валюты на дату инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="e5407-181">**Exchange rate** – The exchange rate of the specified currency on the counting date.</span></span>
    - <span data-ttu-id="e5407-182">**Сумма инвентаризации** — баланс указанного типа актива в основной валюте компании.</span><span class="sxs-lookup"><span data-stu-id="e5407-182">**Counted amount** – The balance of the specified asset type in the company's primary currency.</span></span>
    - <span data-ttu-id="e5407-183">**Разнесенная сумма** — сумма, указанная в поле **Разнесенная сумма (валюта)** в основной валюте компании.</span><span class="sxs-lookup"><span data-stu-id="e5407-183">**Posted amount** – The amount that is specified in the **Posted amount (currency)** field, in the company's primary currency.</span></span>
    - <span data-ttu-id="e5407-184">**Сумма курсовой разницы** — если корректировки валютного курса для указанной валюты были рассчитаны на дату запасов, это поле помечается.</span><span class="sxs-lookup"><span data-stu-id="e5407-184">**Exchange rate adjustment amount** – If the exchange rate adjustments for the specified currency were calculated on the date of inventory, this field is flagged.</span></span> <span data-ttu-id="e5407-185">Для основной валюты поле **Сумма корректировки валютного курса** всегда помечается.</span><span class="sxs-lookup"><span data-stu-id="e5407-185">For the primary currency, the **Exchange rate adjustment amount** field is always flagged.</span></span>

![Акт инвентаризации денежных средств](media/cash-primary-02.png)

4. <span data-ttu-id="e5407-187">Выберите **ОК**, чтобы создать акт инвентаризации денежных средств.</span><span class="sxs-lookup"><span data-stu-id="e5407-187">Select **OK** to generate the cash counting act.</span></span>

    ![Отчет акта инвентаризации денежных средств](media/cash-primary-03.png)
