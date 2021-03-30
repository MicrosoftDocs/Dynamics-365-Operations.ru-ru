---
title: Настройка и создание договоров
description: В этой теме приводятся сведения о создании договоров покупки и продажи.
author: v-nadyuz
manager: AnnBe
ms.date: 02/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.author: roschlom
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: e75db9fbbef5e91a1ae25e1934e57385c71121cb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219838"
---
# <a name="set-up-and-create-agreements"></a><span data-ttu-id="b4af1-103">Настройка и создание договоров</span><span class="sxs-lookup"><span data-stu-id="b4af1-103">Set up and create agreements</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4af1-104">Все договоры покупки можно просмотреть на странице списка **Договоры покупки** и все договоры продажи на странице списка **Договоры продажи**.</span><span class="sxs-lookup"><span data-stu-id="b4af1-104">You can view all purchase agreements on the **Purchase agreements** list page and all sales agreements on the **Sales agreements** list page.</span></span> <span data-ttu-id="b4af1-105">Эти страницы списков хранят данные, такие как даты и суммы договоров, и условия оплаты.</span><span class="sxs-lookup"><span data-stu-id="b4af1-105">These list pages store data such as the dates and amounts of the agreements, and the payment terms.</span></span> <span data-ttu-id="b4af1-106">Все договоры группируются в классификации договоров.</span><span class="sxs-lookup"><span data-stu-id="b4af1-106">All agreements are grouped into agreement classifications.</span></span>

## <a name="create-sales-agreement-classifications"></a><span data-ttu-id="b4af1-107">Создание классификаций договоров продажи</span><span class="sxs-lookup"><span data-stu-id="b4af1-107">Create sales agreement classifications</span></span>

1. <span data-ttu-id="b4af1-108">Перейдите **Продажи и маркетинг** \> **Настройка** \> **Договоры продажи** \> **Классификации договоров продажи** или **Расчеты с клиентами** \> **Настройка** \> **Классификации договоров продажи**.</span><span class="sxs-lookup"><span data-stu-id="b4af1-108">Go to **Sales and marketing** \> **Setup** \> **Sales agreements** \> **Sales agreement classifications** or **Accounts receivable** \> **Setup** \> **Sales agreement classifications**.</span></span>
2. <span data-ttu-id="b4af1-109">Создайте классификацию договоров продажи.</span><span class="sxs-lookup"><span data-stu-id="b4af1-109">Create a sales agreement classification.</span></span>
3. <span data-ttu-id="b4af1-110">На экспресс-вкладке **Общие** в поле **Связанные классификации** выберите группу классификации договоров, связанную с классификацией договоров.</span><span class="sxs-lookup"><span data-stu-id="b4af1-110">On the **General** FastTab, in the **Associated classification** field, select the agreement classification group that is associated with the agreement classification.</span></span>
4. <span data-ttu-id="b4af1-111">В поле **Код номерной серии** выберите код номерной серии, который должен использоваться для нумерации договоров, относящихся к классификации договоров.</span><span class="sxs-lookup"><span data-stu-id="b4af1-111">In the **Number sequence code** field, select the code for the number sequence that should be used to number agreements that belong to the agreement classification.</span></span>
5.  <span data-ttu-id="b4af1-112">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b4af1-112">Select **Save**.</span></span>

![Страница классификации договоров продажи](media/1_Sales_agreement_classifications.png)

> [!NOTE]
> <span data-ttu-id="b4af1-114">Нельзя удалить классификацию договоров, используемую для существующих договоров.</span><span class="sxs-lookup"><span data-stu-id="b4af1-114">You can't delete an agreement classification that is used for existing agreements.</span></span>

## <a name="create-purchase-agreement-classifications"></a><span data-ttu-id="b4af1-115">Создание классификаций договоров покупки</span><span class="sxs-lookup"><span data-stu-id="b4af1-115">Create purchase agreement classifications</span></span>

1. <span data-ttu-id="b4af1-116">Перейдите в раздел **Закупки и источники** \> **Настройка** \> **Классификация договоров покупки**.</span><span class="sxs-lookup"><span data-stu-id="b4af1-116">Go to **Procurement and sourcing** \> **Setup** \> **Purchase agreement classification**.</span></span>
2. <span data-ttu-id="b4af1-117">Укажите сведения, как описано в предыдущем разделе данной темы, [Создание классификаций договоров продажи](#create-sales-agreement-classifications).</span><span class="sxs-lookup"><span data-stu-id="b4af1-117">Specify the details as described in the previous section of this topic, [Create sales agreement classifications](#create-sales-agreement-classifications).</span></span>

![Страница классификаций договоров покупки](media/2_Purchase_agreement_classifications.png)

## <a name="create-a-sales-agreement"></a><a name="create-sales-agreement"></a><span data-ttu-id="b4af1-119">Создание договора продажи</span><span class="sxs-lookup"><span data-stu-id="b4af1-119">Create a sales agreement</span></span>

<span data-ttu-id="b4af1-120">Дополнительные сведения о создании договоров продажи см. в разделе [Ввод договоров продажи](../../supply-chain/sales-marketing/tasks/enter-sales-agreements.md).</span><span class="sxs-lookup"><span data-stu-id="b4af1-120">For more information about how to create sales agreements, see [Enter sales agreements](../../supply-chain/sales-marketing/tasks/enter-sales-agreements.md).</span></span>

1. <span data-ttu-id="b4af1-121">Перейдите **Расчеты с клиентами** \> **Заказы** \> **Договоры продажи** или **Продажи и маркетинг** \> **Договоры продажи** \> **Договоры продажи**.</span><span class="sxs-lookup"><span data-stu-id="b4af1-121">Go to **Accounts receivable** \> **Orders** \> **Sales agreements** or **Sales and marketing** \> **Sales agreements** \> **Sales agreements**.</span></span>
2. <span data-ttu-id="b4af1-122">На панели операций выберите **Создать** для создания договора продажи.</span><span class="sxs-lookup"><span data-stu-id="b4af1-122">On the Action Pane, select **New** to create a sales agreement.</span></span>
3. <span data-ttu-id="b4af1-123">В диалоговом окне **Создание договора продажи** на экспресс-вкладке **Клиент** укажите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="b4af1-123">In the **Create sales agreement** dialog box, on the **Customer** FastTab, specify the following details:</span></span>

    -  <span data-ttu-id="b4af1-124">Выберите счет клиента в поле **Счет клиента**.</span><span class="sxs-lookup"><span data-stu-id="b4af1-124">In the **Customer account** field, select a customer account.</span></span>
    -  <span data-ttu-id="b4af1-125">В разделе **Документ** в поле **Классификация договоров продажи** выберите классификацию договоров продажи, к которой относится данный договор.</span><span class="sxs-lookup"><span data-stu-id="b4af1-125">In the **Document** section, in the **Sales agreement classification** field, select the sales agreement classification that the agreement belongs to.</span></span>

    <span data-ttu-id="b4af1-126">На экспресс-вкладке **Общие** в разделе **Документ** поле **Код договора продажи** заполнено на основе номерной серии, указанной для классификации соглашения.</span><span class="sxs-lookup"><span data-stu-id="b4af1-126">On the **General** FastTab, in the **Document** section, the **Sales agreement ID** field is set based on the number sequence that is specified for the agreement classification.</span></span>

4. <span data-ttu-id="b4af1-127">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b4af1-127">Select **OK**.</span></span>

    ![Диалоговое окно создания классификаций договоров продажи](media/3_Create_sales_agreement.png)

5. <span data-ttu-id="b4af1-129">На странице **Договоры продажи** на экспресс-вкладке **Заголовок договора продажи** укажите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="b4af1-129">On the **Sales agreements** page, on the **Sales agreement header** FastTab, specify the following details:</span></span>

    -  <span data-ttu-id="b4af1-130">В поле **Валюта** валюту договора.</span><span class="sxs-lookup"><span data-stu-id="b4af1-130">In the **Currency** field, specify the currency for the agreement.</span></span>
    -  <span data-ttu-id="b4af1-131">В поле **Действует с** укажите дату вступления в силу договора.</span><span class="sxs-lookup"><span data-stu-id="b4af1-131">In the **Effective date** field, specify the effective date for the agreement.</span></span>
    -  <span data-ttu-id="b4af1-132">В поле **Дата окончания срока действия** укажите дату окончания срока действия договора.</span><span class="sxs-lookup"><span data-stu-id="b4af1-132">In the **Expiration date** field, specify the expiration date for the agreement.</span></span>
    -  <span data-ttu-id="b4af1-133">В поле **Статус** выберите статус соглашения: **на удержании**, **действует** или **закрыто**.</span><span class="sxs-lookup"><span data-stu-id="b4af1-133">In the **Status** field, select the status of the agreement: **On-hold**, **Effective**, or **Closed**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b4af1-134">Проводки могут быть разнесены только для договоров со статусом **действует**.</span><span class="sxs-lookup"><span data-stu-id="b4af1-134">Transactions can be posted only for agreements that have a status of **Effective**.</span></span>

    ![Экспресс-вкладка заголовка договора продажи](media/4_Sales_agreements.png)

6. <span data-ttu-id="b4af1-136">Переключитесь в представление **Заголовок**, а затем на экспресс-вкладке **Общие** выполните следующие шаги:</span><span class="sxs-lookup"><span data-stu-id="b4af1-136">Switch to the **Header** view, and then, on the **General** FastTab, follow these steps:</span></span>

  - <span data-ttu-id="b4af1-137">В разделе **Документ** укажите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="b4af1-137">In the **Document** section, specify the following details:</span></span>

     - <span data-ttu-id="b4af1-138">В поле **Заголовок документа** укажите заголовок договора.</span><span class="sxs-lookup"><span data-stu-id="b4af1-138">In the **Document title** field, specify the title for the agreement.</span></span>
     - <span data-ttu-id="b4af1-139">В поле **Дата** укажите дату договора.</span><span class="sxs-lookup"><span data-stu-id="b4af1-139">In the **Date** field, specify the date of the agreement.</span></span>

  -   <span data-ttu-id="b4af1-140">В разделе **Предмет договора** в поле **Предмет договора** введите комментарий или примечания о договоре.</span><span class="sxs-lookup"><span data-stu-id="b4af1-140">In the **Subject of an agreement** section, in the **Subject of an agreement** field, enter a comment or notes about the agreement.</span></span>

   ![Экспресс-вкладка "Общее" договора продажи](media/5_Sales_agreements.png)

7. <span data-ttu-id="b4af1-142">На экспресс-вкладке **Финансы** выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b4af1-142">On the **Financial** FastTab, follow these steps:</span></span>

    - <span data-ttu-id="b4af1-143">В разделе **Сумма договора** в поле **Сумма договора** укажите сумму договора.</span><span class="sxs-lookup"><span data-stu-id="b4af1-143">In the **Agreement sum** section, in the **Agreement sum** field, specify the sum of the agreement.</span></span>
    - <span data-ttu-id="b4af1-144">В разделе **Кредит** в поле **Кредитный лимит** укажите кредитный лимит для договора.</span><span class="sxs-lookup"><span data-stu-id="b4af1-144">In the **Credit** section, in the **Credit limit** field, specify the credit limit for the agreement.</span></span> <span data-ttu-id="b4af1-145">Кредитный лимит комплексно проверяется для всех договоров контрагентов и для общего лимита контрагентов.</span><span class="sxs-lookup"><span data-stu-id="b4af1-145">The credit limit is comprehensively checked for all counterparty agreements and for the total counterparty limit.</span></span>


    > [!NOTE]
    > <span data-ttu-id="b4af1-146">При сопоставлении накладных с платежами, относящимися к разным договорам, контроль лимита выполняется в соответствии с договором, которому назначен платеж.</span><span class="sxs-lookup"><span data-stu-id="b4af1-146">When you settle invoices with payments that belong to different agreements, limit control is done according to the agreement that the payment is assigned to.</span></span>
    >
    > <span data-ttu-id="b4af1-147">При отмене сопоставления накладных и платежей, относящихся к разным договорам, контроль лимита выполняется в соответствии с договором, которому назначена накладная.</span><span class="sxs-lookup"><span data-stu-id="b4af1-147">If you cancel the settlement of invoices and payments that belong to different agreements, limit control is done according to the agreement that the invoice is assigned to.</span></span>
    >
    > <span data-ttu-id="b4af1-148">При сопоставлении накладных с платежами, которые не показывают, что они принадлежат договору, контроль лимита выполняется контрагентом.</span><span class="sxs-lookup"><span data-stu-id="b4af1-148">When you settle invoices with payments that don't indicate that they belong to the agreement, limit control is done by the counterparty.</span></span>
    >
    > <span data-ttu-id="b4af1-149">При сопоставлении накладных без указания, что они относятся к договору с платежами, относящимися к договору, контроль лимита выполняется в соответствии с договором, которому назначен платеж.</span><span class="sxs-lookup"><span data-stu-id="b4af1-149">When you settle invoices that don't indicate that they belong to the agreement with payments that belong to the agreement, limit control is done according to the agreement that the payment is assigned to.</span></span>
    >
    > <span data-ttu-id="b4af1-150">При отмене сопоставления накладных без указания, что они относятся к договору с платежами, и платежей, относящихся к договору, контроль лимита выполняется контрагентом.</span><span class="sxs-lookup"><span data-stu-id="b4af1-150">If you cancel the settlement of invoices that don't indicate that they belong to the agreement and payments that belong to the agreement, limit control is done by a contractor.</span></span> <span data-ttu-id="b4af1-151">Накладные с открытым сальдо и без указания на договор включаются.</span><span class="sxs-lookup"><span data-stu-id="b4af1-151">Invoices that have an open balance and don't indicate an agreement are included.</span></span>

   - <span data-ttu-id="b4af1-152">В разделе **Профиль разноски** укажите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="b4af1-152">In the **Posting profile** section, specify the following details:</span></span>

    - <span data-ttu-id="b4af1-153">Если в **Профиль разноски** указан договор для проводок, можно выбрать профиль разноски контрагента, который должен использоваться при разноске проводок.</span><span class="sxs-lookup"><span data-stu-id="b4af1-153">In the **Posting profile** field, if you specify an agreement for transactions, you can select the counterparty posting profile that should be used when transactions are posted.</span></span>
     - <span data-ttu-id="b4af1-154">В поле **Профиль разноски с ваучером журнала предоплат** можно выбрать отдельный профиль разноски, который должен использоваться при регистрации предоплаты для договора.</span><span class="sxs-lookup"><span data-stu-id="b4af1-154">In the **Posting profile with prepayment journal voucher** field, you can select a separate posting profile that should be used when a prepayment is registered for the agreement.</span></span> <span data-ttu-id="b4af1-155">Если это поле не задано, значение по умолчанию берется со страницы **Параметры модуля расчетов с клиентами**.</span><span class="sxs-lookup"><span data-stu-id="b4af1-155">If you don't set this field, a default value is taken from the **Accounts receivable parameters** page.</span></span>

   ![Страница договоров на продажу](media/6_Sales_agreements.png)

8. <span data-ttu-id="b4af1-157">На экспресс- вкладке **Условия** в разделе **Оплата** задайте поля для условий оплаты.</span><span class="sxs-lookup"><span data-stu-id="b4af1-157">On the **Terms** FastTab, in the **Payment** section, set the fields for payment terms.</span></span> <span data-ttu-id="b4af1-158">В поле **Платежный день** выберите календарь платежных дней.</span><span class="sxs-lookup"><span data-stu-id="b4af1-158">In the **Payment day** field, select a calendar of payment days.</span></span>
9. <span data-ttu-id="b4af1-159">На экспресс-вкладке **Контактная информация** укажите контактную информацию для договора.</span><span class="sxs-lookup"><span data-stu-id="b4af1-159">On the **Contact information** FastTab, specify contact information for the agreement.</span></span>

    ![Страница договоров продажи, экспресс-вкладка контактной информации](media/7_Sales_agreements.png)

10. <span data-ttu-id="b4af1-161">На экспресс-вкладке **Финансовые аналитики** укажите финансовые аналитики.</span><span class="sxs-lookup"><span data-stu-id="b4af1-161">On the **Financial dimensions** FastTab, specify financial dimensions.</span></span> <span data-ttu-id="b4af1-162">При указании договора в документе финансовые аналитики договора вводятся в аналитику документа.</span><span class="sxs-lookup"><span data-stu-id="b4af1-162">When you specify an agreement in a document, the financial dimensions of the agreement are entered into the document dimension.</span></span>
11. <span data-ttu-id="b4af1-163">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b4af1-163">Select **Save**.</span></span>

### <a name="set-up-a-commission"></a><span data-ttu-id="b4af1-164">Настройка комиссии</span><span class="sxs-lookup"><span data-stu-id="b4af1-164">Set up a commission</span></span>

1. <span data-ttu-id="b4af1-165">На странице **Договоры продажи** выберите соглашение, для которого необходимо настроить комиссию.</span><span class="sxs-lookup"><span data-stu-id="b4af1-165">On the **Sales agreements** page, select the agreement that you want to set up a commission for.</span></span>
2.  <span data-ttu-id="b4af1-166">На вкладке **Договор продажи** в разделе **Настройка** выберите **Расчет комиссии**.</span><span class="sxs-lookup"><span data-stu-id="b4af1-166">On the **Sales agreement** tab, in the **Setup** section, select **Commission calculation**.</span></span>
3.  <span data-ttu-id="b4af1-167">На странице **Расчет комиссии** настройте комиссию для выбранного договора.</span><span class="sxs-lookup"><span data-stu-id="b4af1-167">On the **Commission calculation** page, set up a commission for the selected agreement.</span></span> <span data-ttu-id="b4af1-168">Дополнительные сведения о настройке комиссий см. в [Регистрация комиссий продаж](../../supply-chain/sales-marketing/tasks/register-sales-commissions.md).</span><span class="sxs-lookup"><span data-stu-id="b4af1-168">For more information about how to set up commissions, see [Register sales commissions](../../supply-chain/sales-marketing/tasks/register-sales-commissions.md).</span></span>

![Страница расчета комиссии](media/8_Commission_calculation.png)

## <a name="create-a-purchase-agreement"></a><span data-ttu-id="b4af1-170">Создание договора покупки</span><span class="sxs-lookup"><span data-stu-id="b4af1-170">Create a purchase agreement</span></span>

<span data-ttu-id="b4af1-171">Для получения дополнительной информации о том, как создать договоры покупки, см. [Создание договора покупки](../../supply-chain/procurement/tasks/create-purchase-agreement.md).</span><span class="sxs-lookup"><span data-stu-id="b4af1-171">For more information about how to create purchase agreements, see [Create a purchase agreement](../../supply-chain/procurement/tasks/create-purchase-agreement.md).</span></span>

1. <span data-ttu-id="b4af1-172">Перейдите **Расчеты с поставщиками** \> **Заказы на покупку** \> **Договоры покупки** или **Закупки и источники** \> **Договоры покупки** \> **Договоры покупки**.</span><span class="sxs-lookup"><span data-stu-id="b4af1-172">Go to **Accounts payable** \> **Purchase orders** \> **Purchase agreements** or **Procurement and sourcing** \> **Purchase agreements** \> **Purchase agreements**.</span></span>
2. <span data-ttu-id="b4af1-173">На панели операций выберите **Создать** для создания договора.</span><span class="sxs-lookup"><span data-stu-id="b4af1-173">On the Action Pane, select **New** to create an agreement.</span></span>
3. <span data-ttu-id="b4af1-174">В диалоговом окне **Создание договора покупки** на экспресс-вкладке **Поставщик** укажите следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="b4af1-174">In the **Create purchase agreement** dialog box, on the **Vendor** FastTab, specify the following details:</span></span>

    - <span data-ttu-id="b4af1-175">В поле **Счет поставщика** выберите счет поставщика.</span><span class="sxs-lookup"><span data-stu-id="b4af1-175">In the **Vendor account** field, select a vendor account.</span></span>
    - <span data-ttu-id="b4af1-176">В разделе **Документ** в поле **Классификация договоров покупки** выберите классификацию договоров покупки, к которой относится данный договор.</span><span class="sxs-lookup"><span data-stu-id="b4af1-176">In the **Document** section, in the **Purchase agreement classification** field, select the purchase agreement classification that the agreement belongs to.</span></span>

    <span data-ttu-id="b4af1-177">На экспресс-вкладке **Общие** в разделе **Документ** поле **Код договора покупки** заполнено на основе номерной серии, указанной для классификации соглашения.</span><span class="sxs-lookup"><span data-stu-id="b4af1-177">On the **General** FastTab, in the **Document** section, the **Purchase agreement** field is set based on the number sequence that is specified for the agreement classification.</span></span>

4. <span data-ttu-id="b4af1-178">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b4af1-178">Select **OK**.</span></span>

    ![Диалоговое окно создания классификаций договоров покупки](media/9_Create_purchase_agreement.png)

5. <span data-ttu-id="b4af1-180">На странице **Договоры покупки** укажите сведения, как описано в разделе [Создание договора продажи](#create-sales-agreement) ранее в этой теме.</span><span class="sxs-lookup"><span data-stu-id="b4af1-180">On the **Purchase agreements** page, specify the details as described in the [Create a sales agreement](#create-sales-agreement) section earlier in this topic.</span></span>

## <a name="set-up-agreement-dimension-control-for-settlements"></a><span data-ttu-id="b4af1-181">Настройка контроля аналитик договоров для сопоставлений</span><span class="sxs-lookup"><span data-stu-id="b4af1-181">Set up agreement dimension control for settlements</span></span>

<span data-ttu-id="b4af1-182">Можно настроить контроль аналитик для сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="b4af1-182">You can set up dimension control for settlements.</span></span> <span data-ttu-id="b4af1-183">Дополнительные сведения см. в разделе [Настройка контроля аналитик для сопоставлений](rus-transactions-settlement-date.md) Для сопоставления в контексте договоров выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b4af1-183">For more information, see [Set up dimension control for settlements](rus-transactions-settlement-date.md) To do settlement in the context of agreements, follow these steps.</span></span>

1.  <span data-ttu-id="b4af1-184">Перейдите в раздел **Главная книга** \> **Настройка главной книги** \> **Параметры главной книги**.</span><span class="sxs-lookup"><span data-stu-id="b4af1-184">Go to **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span>
2.  <span data-ttu-id="b4af1-185">На вкладке **Договоры** установите для параметра **Отключить контроль аналитики договоров** значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="b4af1-185">On the **Agreements** tab, set the **Disable agreement dimension control** option to **No**.</span></span>

<span data-ttu-id="b4af1-186">Более подробную информацию см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="b4af1-186">Find more details in the following topics:</span></span>

- [<span data-ttu-id="b4af1-187">Договоры</span><span class="sxs-lookup"><span data-stu-id="b4af1-187">Agreements</span></span>](rus-agreements.md)
- [<span data-ttu-id="b4af1-188">Регистрация проводок со ссылками на договоры</span><span class="sxs-lookup"><span data-stu-id="b4af1-188">Register transactions with reference to agreements</span></span>](rus-register-transactions-with-reference-to-agreements.md)
- [<span data-ttu-id="b4af1-189">Запросы и отчеты с договорами</span><span class="sxs-lookup"><span data-stu-id="b4af1-189">Inquiries and reports with agreements</span></span>](rus-inquiries-reports-agreements.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]