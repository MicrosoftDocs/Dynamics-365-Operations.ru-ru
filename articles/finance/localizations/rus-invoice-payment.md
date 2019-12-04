---
title: Счета на оплату (Россия)
description: В этой теме поясняется, как разносить и печатать счета на оплату в Microsoft Dynamics 365 Finance в России.
author: ShylaThompson
manager: AnnBe
ms.date: 10/08/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Russia
ms.author: shylaw
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: e8ead0285f37144e55cc2a417183b7bdf0b7bfa9
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773486"
---
# <a name="invoices-for-payment-russia"></a><span data-ttu-id="cf59d-103">Счета на оплату (Россия)</span><span class="sxs-lookup"><span data-stu-id="cf59d-103">Invoices for payment (Russia)</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf59d-104">Счет на оплату — это дополнительный документ, содержащий подробности платежа получателя (продавец), для которого плательщик (покупатель) переводит деньги для целей, перечисленных в счете на оплату, например работы или услуги.</span><span class="sxs-lookup"><span data-stu-id="cf59d-104">Invoice for payment is an optional document containing payment details of the recipient (seller), for which the payer (buyer) transfers money for the purposes listed in the invoice for payment, such as work or services.</span></span> <span data-ttu-id="cf59d-105">Это документ, который используется для оплаты для купленных товаров от покупателя или передачи предоплаты (аванса).</span><span class="sxs-lookup"><span data-stu-id="cf59d-105">This is a document that serves to pay for the purchased goods by the buyer or to transfer a prepayment (advance).</span></span> 

<span data-ttu-id="cf59d-106">Перед разноской элемента **Счет на оплату** в модулях "Расчеты с поставщиками" и "Расчеты с клиентами" необходимо настроить номерные серии:</span><span class="sxs-lookup"><span data-stu-id="cf59d-106">Before posting **Invoice for payment** in the Account payable and Account receivable modules it is necessary to set up the number sequences:</span></span>
1.  <span data-ttu-id="cf59d-107">Щелкните **Расчеты с клиентами** \> **Настройка** \> **Параметры расчетов с клиентами** или **Расчеты с поставщиками** \> **Настройка** \> **Параметры расчетов с поставщиками**</span><span class="sxs-lookup"><span data-stu-id="cf59d-107">Click **Accounts receivable** \> **Setup** \> **Accounts receivable parameters** or **Accounts payable** \> **Setup** \> **Accounts payable parameters**</span></span>

2.  <span data-ttu-id="cf59d-108">Откройте вкладку **Номерные серии**.</span><span class="sxs-lookup"><span data-stu-id="cf59d-108">Click the **Number sequences** tab.</span></span>

3.  <span data-ttu-id="cf59d-109">В поле **Код номерной серии** выберите код номерной серии для **счета на оплату** (поле **Ссылка**).</span><span class="sxs-lookup"><span data-stu-id="cf59d-109">In the **Number sequence code** field, select the number sequence code for the **invoice for payment** (**Reference** field).</span></span>

## <a name="post-and-print-an-invoice-for-payment-from-a-sales-order"></a><span data-ttu-id="cf59d-110">Разноска и печать счета на оплату из заказа на продажу</span><span class="sxs-lookup"><span data-stu-id="cf59d-110">Post and print an invoice for payment from a sales order</span></span> 

<span data-ttu-id="cf59d-111">Используйте страницу **Разноска счета на оплату** для разноски счета на оплату.</span><span class="sxs-lookup"><span data-stu-id="cf59d-111">Use the **Posting invoice for payment** page to post an invoice for payment.</span></span>

1.  <span data-ttu-id="cf59d-112">Щелкните **Расчеты с клиентами** \> **Общий** \> **Заказы** \> **Все заказы на продажу**.</span><span class="sxs-lookup"><span data-stu-id="cf59d-112">Click **Accounts receivable** \> **Common** \> **Orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="cf59d-113">Создайте новый заказ на продажу и введите требуемую информацию.</span><span class="sxs-lookup"><span data-stu-id="cf59d-113">Create a new sales order, and enter the required details.</span></span>

3.  <span data-ttu-id="cf59d-114">В области действий щелкните вкладку **Продажа**, затем щелкните **Счет на оплату**.</span><span class="sxs-lookup"><span data-stu-id="cf59d-114">Click the **Sell** tab on the action pane, and then click **Invoice for payment**.</span></span>

4.  <span data-ttu-id="cf59d-115">В поле **Дата счета на оплату** выберите дату счета на оплату.</span><span class="sxs-lookup"><span data-stu-id="cf59d-115">In the **Invoice for payment date** field, select the date of the invoice for payment.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="cf59d-116">По умолчанию отображается текущая дата.</span><span class="sxs-lookup"><span data-stu-id="cf59d-116">By default, the current date is displayed.</span></span>

6.  <span data-ttu-id="cf59d-117">Щелкните вкладку **Строки**, а затем выберите строку, содержащую сведения о номенклатуре, основанную на значении, выбранном в поле **Количество**.</span><span class="sxs-lookup"><span data-stu-id="cf59d-117">Click the **Lines** tab, and then select the line that contains the item details, based on the value that is selected in the **Quantity** field.</span></span>

7.  <span data-ttu-id="cf59d-118">Задайте для параметра **Разноска** значение **Да**, чтобы разнести счет на оплату.</span><span class="sxs-lookup"><span data-stu-id="cf59d-118">Set the **Posting** option to **Yes** to post the invoice for payment.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="cf59d-119">Можно разнести и напечатать накладную для оплаты только для активных банковских счетов.</span><span class="sxs-lookup"><span data-stu-id="cf59d-119">You can post and print an invoice for payment only for active bank accounts.</span></span>

8.  <span data-ttu-id="cf59d-120">Задайте для параметра **Печатать счет на оплату** значение **Да**, чтобы распечатать счет на оплату после разноски.</span><span class="sxs-lookup"><span data-stu-id="cf59d-120">Set the **Print invoice for payment** option to **Yes** to print the invoice for payment after posting.</span></span>
8. <span data-ttu-id="cf59d-121">Задайте для параметра **Использовать назначение управления печатью** значение **Да**, чтобы распечатать накладную для платежа с помощью назначения управления печатью.</span><span class="sxs-lookup"><span data-stu-id="cf59d-121">Set the **Use print management destination** option to **Yes** to print the invoice for payment using print management destinations.</span></span> <span data-ttu-id="cf59d-122">Задайте для этого параметра значение **Нет**, чтобы использовать настройки печати по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cf59d-122">Set this option to **No** to use the default printer settings.</span></span>
9. <span data-ttu-id="cf59d-123">Задайте для параметра **Печать в основной валюте** значение **Да**, чтобы распечатать накладную для платежа в национальной валюте.</span><span class="sxs-lookup"><span data-stu-id="cf59d-123">Set the **Print in national currency** option **Yes** to print the invoice for payment in national currency.</span></span>

10. <span data-ttu-id="cf59d-124">Щелкните вкладку **Должностные лица**, чтобы проверить и обновить значения по умолчанию, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="cf59d-124">Click the **Officials** tab to validate and update default values, if needed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cf59d-125">Используйте страницу **Должностные лица** для настройки должностных лиц по умолчанию, которых необходимо включить в накладную для платежа.</span><span class="sxs-lookup"><span data-stu-id="cf59d-125">Use the **Officials** page to set up the default officials to be listed on the invoice for payment.</span></span> <span data-ttu-id="cf59d-126">Дополнительные сведения см. в разделе [Настройка должностных лиц](rus-officials.md).</span><span class="sxs-lookup"><span data-stu-id="cf59d-126">For more information, see [Set up officials](rus-officials.md).</span></span>

11.  <span data-ttu-id="cf59d-127">Щелкните **ОК**, чтобы разнести накладную для платежа.</span><span class="sxs-lookup"><span data-stu-id="cf59d-127">Click **OK** to post the invoice for payment.</span></span> <span data-ttu-id="cf59d-128">Сведения о разнесенном счете можно посмотреть в списке страницы **Журнал счетов на оплату**.</span><span class="sxs-lookup"><span data-stu-id="cf59d-128">You can view the details of the posted invoice in the **Journal of invoices for payment** page list.</span></span>

## <a name="post-and-print-an-invoice-for-payment-from-a-free-text-invoice"></a><span data-ttu-id="cf59d-129">Разноска и печать накладной для платежа из накладной с произвольным текстом</span><span class="sxs-lookup"><span data-stu-id="cf59d-129">Post and print an invoice for payment from a free text invoice</span></span> 

<span data-ttu-id="cf59d-130">Используйте страницу **Разноска счета на оплату** для разноски счета на оплату.</span><span class="sxs-lookup"><span data-stu-id="cf59d-130">Use the **Posting invoice for payment** page to post an invoice for payment.</span></span>

1.  <span data-ttu-id="cf59d-131">Щелкните **Расчеты с клиентами** \> **Обычные** \> **Накладные** \> **Все накладные с произвольным текстом**.</span><span class="sxs-lookup"><span data-stu-id="cf59d-131">Click **Accounts receivable** \> **Common** \> **Invoices** \> **All free text invoices**.</span></span>

2.  <span data-ttu-id="cf59d-132">Создайте новую накладную с произвольным текстом, затем введите требуемые сведения.</span><span class="sxs-lookup"><span data-stu-id="cf59d-132">Create a new free text invoice, and enter the required details.</span></span> <span data-ttu-id="cf59d-133">Дополнительные сведения см. в разделе [Создать накладные с произвольным текстом](../accounts-receivable/create-free-text-invoice-new.md).</span><span class="sxs-lookup"><span data-stu-id="cf59d-133">For more information, see [Create free text invoices](../accounts-receivable/create-free-text-invoice-new.md).</span></span>

3.  <span data-ttu-id="cf59d-134">В области действий щелкните **Разнести** \> **Счет на оплату**, чтобы открыть страницу **Разноска счета на оплату**.</span><span class="sxs-lookup"><span data-stu-id="cf59d-134">On the action pane, click **Post** \> **Invoice for payment** to open the **Posting invoice for payment** page.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="cf59d-135">Если накладная с произвольным текстом уже была разнесены, параметр **Счет на оплату** недоступен.</span><span class="sxs-lookup"><span data-stu-id="cf59d-135">If the free text invoice has already been posted, the **Invoice for payment** option is not available.</span></span>
    
4.  <span data-ttu-id="cf59d-136">В поле **Печать** выберите **Текущие**, чтобы напечатать каждую накладную, или выберите **После**, чтобы напечатать после того как все накладные будут разнесены.</span><span class="sxs-lookup"><span data-stu-id="cf59d-136">In the **Print** field, select **Current** to print each invoice, or select **After** to print after all of the invoices have been posted.</span></span>

5. <span data-ttu-id="cf59d-137">Задайте для параметра **Печатать** значение **Да**, чтобы распечатать счет на оплату после разноски.</span><span class="sxs-lookup"><span data-stu-id="cf59d-137">Set the **Print** option to **Yes** to print the invoice for payment after posting.</span></span>

6. <span data-ttu-id="cf59d-138">Задайте для параметра **Печать в основной валюте** значение **Да**, чтобы распечатать накладную для платежа в национальной валюте.</span><span class="sxs-lookup"><span data-stu-id="cf59d-138">Set the **Print in national currency** option **Yes** to print the invoice for payment in national currency.</span></span>

7. <span data-ttu-id="cf59d-139">Задайте для параметра **Использовать назначение управления печатью** значение **Да**, чтобы распечатать накладную для платежа с помощью назначения управления печатью.</span><span class="sxs-lookup"><span data-stu-id="cf59d-139">Set the **Use print management destination** option to **Yes** to print the invoice for payment using print management destinations.</span></span> <span data-ttu-id="cf59d-140">Задайте для этого параметра значение **Нет**, чтобы использовать настройки печати по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cf59d-140">Set this option to **No** to use the default printer settings.</span></span>
 
8. <span data-ttu-id="cf59d-141">Щелкните вкладку **Должностные лица**, чтобы проверить и обновить значения по умолчанию, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="cf59d-141">Click the **Officials** tab to validate and update default values, if needed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cf59d-142">Используйте страницу **Должностные лица** для настройки должностных лиц по умолчанию, которых необходимо включить в накладную для платежа.</span><span class="sxs-lookup"><span data-stu-id="cf59d-142">Use the **Officials** page to set up the default officials to be listed on the invoice for payment.</span></span> <span data-ttu-id="cf59d-143">Дополнительные сведения см. в разделе [Настройка должностных лиц](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/russia-81/articles/financials/localizations/rus-officials.md).</span><span class="sxs-lookup"><span data-stu-id="cf59d-143">For more information, see [Set up officials](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/russia-81/articles/financials/localizations/rus-officials.md).</span></span>

9. <span data-ttu-id="cf59d-144">Щелкните вкладку **Прочие**. В поле **Комментарии** введите примечание для накладной для платежа.</span><span class="sxs-lookup"><span data-stu-id="cf59d-144">Click the **Other** tab. In the **Comments** field, enter a comment for the invoice for payment.</span></span>

10. <span data-ttu-id="cf59d-145">Щелкните **ОК**, чтобы разнести и распечатать накладную для платежа.</span><span class="sxs-lookup"><span data-stu-id="cf59d-145">Click **OK** to post and print the invoice for payment.</span></span>
    

    > [!NOTE]
    > <span data-ttu-id="cf59d-146">Щелкните **Расчеты с клиентами** > **Обычные** > **Накладные** > **Все накладные с произвольным текстом**.</span><span class="sxs-lookup"><span data-stu-id="cf59d-146">Click **Accounts receivable** > **Common** > **Invoices** > **All free text invoices**.</span></span> <span data-ttu-id="cf59d-147">В области действий щелкните **Связанные сведения > Счет на оплату**, чтобы просмотреть разнесенные счета на оплату.</span><span class="sxs-lookup"><span data-stu-id="cf59d-147">On the action pane, click **Related information > Invoice for payment** to view the posted invoices for payment.</span></span> <span data-ttu-id="cf59d-148">Или щелкните **Расчеты с клиентами > Запросы и отчеты > Накладные > Счет на оплату**.</span><span class="sxs-lookup"><span data-stu-id="cf59d-148">Or, click **Accounts receivable > Inquiries and reports > Invoices > Invoice for payment**.</span></span>
    > <span data-ttu-id="cf59d-149">Можно также использовать список страницы **Журнал счетов на оплату**, чтобы распечатать накладную для платежа.</span><span class="sxs-lookup"><span data-stu-id="cf59d-149">You can also use the **Journal of invoice for payment** page list to print the invoice for payment.</span></span>

## <a name="post-and-print-an-invoice-for-payment-from-a-purchase-order"></a><span data-ttu-id="cf59d-150">Разноска и печать счета на оплату из заказа на покупку</span><span class="sxs-lookup"><span data-stu-id="cf59d-150">Post and print an invoice for payment from a purchase order</span></span> 

<span data-ttu-id="cf59d-151">Используйте страницу **Разноска счета на оплату** для разноски накладной по покупке для оплаты.</span><span class="sxs-lookup"><span data-stu-id="cf59d-151">Use the **Posting invoice for payment** page to post a purchase invoice for payment.</span></span>

1.  <span data-ttu-id="cf59d-152">Щелкните **Расчеты с поставщиками** \> **Общее** \> **Заказы на покупку** \> **Все заказы на покупку**.</span><span class="sxs-lookup"><span data-stu-id="cf59d-152">Click **Accounts payable** \> **Common** \> **Purchase orders** \> **All purchase orders**.</span></span>

2.  <span data-ttu-id="cf59d-153">Создайте новый заказ на покупку и введите требуемую информацию.</span><span class="sxs-lookup"><span data-stu-id="cf59d-153">Create a new purchase order, and enter the required details.</span></span>

3.  <span data-ttu-id="cf59d-154">В области действий щелкните вкладку **Покупка**, затем щелкните **Счет на оплату**.</span><span class="sxs-lookup"><span data-stu-id="cf59d-154">On the action pane, click the **Purchase** tab, and then click **Invoice for payment**.</span></span>

4.   <span data-ttu-id="cf59d-155">В поле **Накладная на дату оплаты** на странице **Разноска счета на оплату** введите дату счета на оплату и в поле **Счет на оплату** введите номер счета на оплату, полученного от поставщика.</span><span class="sxs-lookup"><span data-stu-id="cf59d-155">In the **Invoice for payment date** field, on the **Posting invoice for payment** page, enter the date of the invoice for payment and in the **Invoice for payment** field enter the number of the invoice for payment that you received from the vendor.</span></span> <span data-ttu-id="cf59d-156">По умолчанию отображается текущая дата.</span><span class="sxs-lookup"><span data-stu-id="cf59d-156">By default, the current date is displayed.</span></span>

5.  <span data-ttu-id="cf59d-157">Щелкните вкладку **Строки**, а затем выберите строку, содержащую сведения о номенклатуре, основанную на значении, выбранном в поле **Количество**.</span><span class="sxs-lookup"><span data-stu-id="cf59d-157">Click the **Lines** tab, and then select the line that contains the item details, based on the value that is selected in the **Quantity** field.</span></span>

6.  <span data-ttu-id="cf59d-158">Задайте для параметра **Разноска** значение **Да**, чтобы разнести счет на оплату.</span><span class="sxs-lookup"><span data-stu-id="cf59d-158">Set the **Posting** option to **Yes** to post the invoice for payment.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="cf59d-159">Можно разнести и напечатать накладную для оплаты только для активных банковских счетов.</span><span class="sxs-lookup"><span data-stu-id="cf59d-159">You can post and print an invoice for payment only for active bank accounts.</span></span>

8.  <span data-ttu-id="cf59d-160">Задайте для параметра **Печатать счет на оплату** значение **Да**, чтобы распечатать счет на оплату после разноски.</span><span class="sxs-lookup"><span data-stu-id="cf59d-160">Set the **Print invoice for payment** option to **Yes** to print the invoice for payment after posting.</span></span>

9.  <span data-ttu-id="cf59d-161">Щелкните **ОК**, чтобы разнести накладную для платежа.</span><span class="sxs-lookup"><span data-stu-id="cf59d-161">Click **OK** to post the invoice for payment.</span></span> <span data-ttu-id="cf59d-162">Можно просмотреть сведения о разнесенной накладной в списке страницы **Журнал счетов на оплату** (в области действий **Покупка** щелкните **Журналы** \> **Счет на оплату**).</span><span class="sxs-lookup"><span data-stu-id="cf59d-162">You can view the details of the posted invoice in the **Journal of invoices for payment** list page (on the **Purchase** action pane click **Journals** \> **Invoice for payment**).</span></span>
