---
title: Устранение неполадок поступления продуктов и выставления накладных
description: В этой теме описывается, как устранять проблемы, которые могут встретиться при работе с поступлениями продуктов и выставлением накладных.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: a89effb686d60dde9d11f99be51d4101897ad4ea
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018637"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a><span data-ttu-id="e2e8f-103">Устранение неполадок поступления продуктов и выставления накладных</span><span class="sxs-lookup"><span data-stu-id="e2e8f-103">Troubleshoot product receipts and invoicing</span></span>

<span data-ttu-id="e2e8f-104">В этой теме описывается, как устранять проблемы, которые могут встретиться при работе с поступлениями продуктов и выставлением накладных.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-104">This topic describes how to fix issues that you might encounter while you work with product receipts and invoicing.</span></span>

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a><span data-ttu-id="e2e8f-105">Я не могу разнести более одной накладной для строки заказа на покупку, имеющей номенклатуры, основанные на категориях.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-105">I can't post more than one invoice for a purchase order line that has category-based items.</span></span>

<span data-ttu-id="e2e8f-106">Если требуется разнести накладные, количество обязательно для заполнения.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-106">A quantity is mandatory if you want to post invoices.</span></span> <span data-ttu-id="e2e8f-107">Таким образом, если для полного количества строки выставляется накладная только по частичной сумме, вы не сможете выставить накладную для оставшейся суммы в другой накладной.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-107">Therefore, if the full quantity of a line has been invoiced for only a partial amount, you won't be able to invoice the remaining amount on another invoice.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="e2e8f-108">Во время подтверждения заказа на покупку я получаю ошибку "Ссылка на объект не указывает" или при разноске накладной поставщика возникает исключение "Адресат вызова создал исключение".</span><span class="sxs-lookup"><span data-stu-id="e2e8f-108">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="e2e8f-109">Эта проблема может возникнуть из-за несогласованности в распределениях заказов на покупку.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-109">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="e2e8f-110">Чтобы разблокировать эту проблему и сбросить заказ на покупку в состояние *Черновик* , перейдите в раздел **Закупки и источники \> Периодические задачи \> Очистка \> Сброс распределения заказов на покупку**.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-110">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="e2e8f-111">Дополнительные сведения см. в следующей записи блога: [Устранение ошибок распределения заказов на покупку в Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="e2e8f-111">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a><span data-ttu-id="e2e8f-112">Невозможно консолидировать несколько поступлений продуктов в один заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-112">I can't consolidate multiple product receipts into a single purchase order.</span></span>

<span data-ttu-id="e2e8f-113">Невозможно консолидировать несколько поступлений продуктов в один заказ на покупку, если различные строки поступлений продуктов имеют различные учетные даты.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-113">You can't consolidate multiple product receipts into a single purchase order if the different product receipt lines have different accounting dates.</span></span>

<span data-ttu-id="e2e8f-114">В предыдущих версиях Microsoft Dynamics 365 Supply Chain Management консолидация была разрешена в этой ситуации.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-114">In earlier versions of Microsoft Dynamics 365 Supply Chain Management, consolidation was allowed in this situation.</span></span> <span data-ttu-id="e2e8f-115">Однако такая практика подвержена ошибкам.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-115">However, the practice is prone to error.</span></span> <span data-ttu-id="e2e8f-116">Дата учета в создаваемых строках заказа на покупку не должна отличаться от даты учета в строках прихода продуктов, из которых были созданы эти строки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-116">The accounting date on the purchase order lines that are created should not differ from the accounting date on the product receipt lines that those purchase order lines were created from.</span></span> <span data-ttu-id="e2e8f-117">(Дата учета в строках заказа на покупку соответствует дате учета в заголовке заказа на покупку.) Таким образом, консолидация нескольких поступлений продуктов в один заказ на покупку больше не разрешена.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-117">(The accounting date on the purchase order lines matches the accounting date on the purchase order header.) Therefore, the consolidation of multiple product receipts into a single purchase orders is no longer allowed.</span></span>

<span data-ttu-id="e2e8f-118">Дата учета используется, например, для резервирований бюджета и бюджетного обязательства.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-118">The accounting date is used, for example, for budget reservations and encumbrance.</span></span> <span data-ttu-id="e2e8f-119">Поэтому она должна сохраняться во время перехода от прихода продукта к заказу на покупку.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-119">Therefore, it should be kept during the transition from product receipt to purchase order.</span></span>

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a><span data-ttu-id="e2e8f-120">После отмены поступлений продуктов проводки могут разноситься на приостановленный счет ГК.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-120">When product receipts are canceled, transactions can be posted to a suspended ledger account.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e2e8f-121">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="e2e8f-121">Issue description</span></span>

<span data-ttu-id="e2e8f-122">Если поступление продуктов отменено, система разрешает разноску проводок в приостановленные счета ГК, даже если счета ГК приостановлены.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-122">If a product receipt is canceled, the system allows transactions to be posted to suspended ledger accounts, even though the main accounts are suspended.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="e2e8f-123">Воспроизведение проблемы</span><span class="sxs-lookup"><span data-stu-id="e2e8f-123">Reproduce the issue</span></span>

<span data-ttu-id="e2e8f-124">Следующая процедура показывает один из способов воспроизведения проблемы.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-124">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="e2e8f-125">На странице **Параметры модуля расчетов с поставщиками** на вкладке **Общие** убедитесь, что для параметра **Разнести поступление продуктов в ГК** установлено значение *Да*.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-125">On the **Accounts payable parameters** page, on the **General** tab, make sure that the **Post product receipt in ledger** option is set to *Yes*.</span></span>
1. <span data-ttu-id="e2e8f-126">Создайте заказ на покупку и добавьте строку заказа с количеством *1000* для продукта.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-126">Create a purchase order, and add an order line that has a quantity of *1,000* for a product.</span></span>
1. <span data-ttu-id="e2e8f-127">Подтвердите заказ на покупку.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-127">Confirm the purchase order.</span></span>
1. <span data-ttu-id="e2e8f-128">Выполните разноску поступления продуктов и проверьте операции.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-128">Post the product receipt, and check the vouchers.</span></span>
1. <span data-ttu-id="e2e8f-129">Приостановите соответствующие счета ГК, *200140* и *140200*.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-129">Suspend the relevant main accounts, *200140* and *140200*.</span></span>
1. <span data-ttu-id="e2e8f-130">Отмените разнесенное поступление продуктов.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-130">Cancel the posted product receipt.</span></span>
1. <span data-ttu-id="e2e8f-131">Обратите внимание, что проводки могут разноситься по приостановленным счета книги учета.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-131">Notice that transactions can be posted to the suspended leger accounts.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e2e8f-132">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="e2e8f-132">Issue resolution</span></span>

<span data-ttu-id="e2e8f-133">Проводки могут быть разнесены по приостановленным счетам книги учета при отмене приемки продуктов, так как это поведение позволяет использовать правильные разноски.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-133">Transactions can be posted to the suspended leger accounts when product receipts are canceled, because this behavior allows for correct postings.</span></span>

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a><span data-ttu-id="e2e8f-134">Код операции прихода продукта потребляется даже в том случае, если финансовая операция во время поступления продуктов не создается.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-134">A product receipt voucher number is consumed even if no financial voucher is generated during product receipt.</span></span>

<span data-ttu-id="e2e8f-135">Если для параметра **Начисление задолженности при поступлении продуктов** задано значение *Нет* для группы моделей номенклатуры, разноска в главную книгу производиться не будет.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-135">If the **Accrue liability on product receipt** option is set to *No* for the item model group, no postings to the general ledger will occur.</span></span> <span data-ttu-id="e2e8f-136">Однако для учета в субкниге регистрируется физическое событие, а для этого события требуется код операции.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-136">However, a physical event will be recorded for the purpose of accounting in a subledger, and that event requires a voucher number.</span></span> <span data-ttu-id="e2e8f-137">Этот код операции является кодом операции, на который имеются ссылки в складских проводках.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-137">This voucher number is the voucher number that is referenced in the inventory transactions.</span></span>

<span data-ttu-id="e2e8f-138">Рекомендуется установить для параметра **Начисление задолженности при поступлении продуктов** значение *Да* , как описано в следующей записи блога: [Разноска накладных расходов во время получения продукта](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span><span class="sxs-lookup"><span data-stu-id="e2e8f-138">We recommend that you set the **Accrue liability on product receipt** option to *Yes* , as described in the following blog post: [Post Misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a><span data-ttu-id="e2e8f-139">Параметр "Выполнить разноску на счет накл. расходов в ГК" не включен.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-139">The Post to charge account in ledger setting isn't turned on.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e2e8f-140">Описание проблемы</span><span class="sxs-lookup"><span data-stu-id="e2e8f-140">Issue description</span></span>

<span data-ttu-id="e2e8f-141">Эта проблема возникает, когда по заказу на покупку выставляется накладная, если параметр **Выполнить разноску на счет накл. расходов в ГК** имеет значение *Да* на вкладке **Накладная** на странице **Параметры модуля расчетов с поставщиками**.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-141">This issue occurs when a purchase order is invoiced, if the **Post to charge account in ledger** option is set to *Yes* on the **Invoice** tab of the **Accounts payable parameters** page.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="e2e8f-142">Воспроизведение проблемы</span><span class="sxs-lookup"><span data-stu-id="e2e8f-142">Reproduce the issue</span></span>

<span data-ttu-id="e2e8f-143">Следующая процедура показывает один из способов воспроизведения проблемы.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-143">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="e2e8f-144">Перейдите в раздел **Расчеты с поставщиками \> Настройка \> Параметры расчетов с поставщиками**.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-144">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
1. <span data-ttu-id="e2e8f-145">На вкладке **Накладная** установите для параметра **Выполнить разноску на счет накл. расходов в ГК** значение *Да*.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-145">On the **Invoice** tab, set the **Post to charge account in ledger** option to *Yes*.</span></span>
1. <span data-ttu-id="e2e8f-146">Выберите **Управление запасами \> Настройка \> Разноска \> Разноска**.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-146">Go to **Inventory management \> Setup \> Posting \> Posting**.</span></span>
1. <span data-ttu-id="e2e8f-147">На вкладке **Заказ на покупку** убедитесь, что удалены все строки в расходах на покупку для продукта.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-147">On the **Purchase order** tab, make sure that you've deleted all the lines in the purchase expenditure for the product.</span></span>
1. <span data-ttu-id="e2e8f-148">Перейдите в раздел **Расчеты с поставщиками \> Заказы на покупку \> Все заказы на покупку**.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-148">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="e2e8f-149">Создание заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-149">Create a purchase order.</span></span> <span data-ttu-id="e2e8f-150">В поле **Счет поставщика** выберите *1001 Офисные принадлежности ACME*.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-150">In the **Vendor account** field, select *1001 Acme Office Supplies*.</span></span>
1. <span data-ttu-id="e2e8f-151">Добавьте строку заказа на покупку со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="e2e8f-151">Add a purchase order line that has the following settings:</span></span>

    - <span data-ttu-id="e2e8f-152">**Код номенклатуры:** *D0011 лазерный проектор*</span><span class="sxs-lookup"><span data-stu-id="e2e8f-152">**Item number:** *D0011 Laser Projector*</span></span>
    - <span data-ttu-id="e2e8f-153">**Сайт:** *1*</span><span class="sxs-lookup"><span data-stu-id="e2e8f-153">**Site:** *1*</span></span>
    - <span data-ttu-id="e2e8f-154">**Склад:** *11*</span><span class="sxs-lookup"><span data-stu-id="e2e8f-154">**Warehouse:** *11*</span></span>
    - <span data-ttu-id="e2e8f-155">**Количество:** *4*</span><span class="sxs-lookup"><span data-stu-id="e2e8f-155">**Quantity:** *4*</span></span>

1. <span data-ttu-id="e2e8f-156">В области действий на вкладке **Покупка** в группе **Действие** выберите **Подтвердить**.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-156">On the Action Pane, on the **Purchase** tab, in the **Action** group, select **Confirm**.</span></span>
1. <span data-ttu-id="e2e8f-157">В области действий на вкладке **Получить** в группе **Создать** выберите **Поступление продуктов**.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-157">On the Action Pane, on the **Receive** tab, in the **Generate** group, select **Product receipt**.</span></span>
1. <span data-ttu-id="e2e8f-158">В диалоговом окне **Разноска поступления продуктов** в поле **Поступление продукта** введите произвольный номер, затем выберите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-158">In the **Posting product receipt** dialog box, in the **Product receipt** field, enter an arbitrary number, and then select **OK**.</span></span>
1. <span data-ttu-id="e2e8f-159">На панели операций на вкладке **Накладная** в группе **Создать** выберите **Накладная**.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-159">On the Action Pane, on the **Invoice** tab, in the **Generate** group, select **Invoice**.</span></span>
1. <span data-ttu-id="e2e8f-160">В поле **Номер** введите произвольный номер в качестве номера накладной.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-160">In the **Number** field, enter an arbitrary number as the invoice number.</span></span>
1. <span data-ttu-id="e2e8f-161">Обновите статус сопоставления и выполните разноску.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-161">Update the match status, and post.</span></span>
1. <span data-ttu-id="e2e8f-162">Обратите внимание, что теперь при создании накладной из заказа на покупку появляется следующая ошибка: "Номер счета для типа проводки расходов на закупку продукта не существует".</span><span class="sxs-lookup"><span data-stu-id="e2e8f-162">Notice that you now receive the following error when you generate an invoice from a purchase order: "Account number for transaction type Purchase expenditure for product does not exist."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e2e8f-163">Устранение проблемы</span><span class="sxs-lookup"><span data-stu-id="e2e8f-163">Issue resolution</span></span>

<span data-ttu-id="e2e8f-164">Это зависит от настроек параметров для накладных и групп накладных.</span><span class="sxs-lookup"><span data-stu-id="e2e8f-164">This depends on the parameter settings for invoices and invoice groups.</span></span> <span data-ttu-id="e2e8f-165">Дополнительные сведения см. в следующей записи блога: [Учет накладных расходов на покупку и изменение запасов](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).</span><span class="sxs-lookup"><span data-stu-id="e2e8f-165">For more information, see the following blog post: [Accounting for Purchase charge and Stock variation](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).</span></span>
